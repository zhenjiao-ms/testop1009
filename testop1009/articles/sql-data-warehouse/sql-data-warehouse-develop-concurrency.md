---
title: Concurrency and workload management in SQL Data Warehouse | Microsoft Azure
description: Understand concurrency and workload management in Azure SQL Data Warehouse for developing solutions.
services: sql-data-warehouse
documentationcenter: NA
author: sonyam
manager: barbkess
editor: ''

ms.service: sql-data-warehouse
ms.devlang: NA
ms.topic: article
ms.tgt_pltfrm: NA
ms.workload: data-services
ms.date: 08/30/2016
ms.author: sonyama;barbkess;jrj

---
# Concurrency and workload management in SQL Data Warehouse
To deliver predictable performance at scale, Microsoft Azure SQL Data Warehouse helps you control concurrency levels and resource allocations like memory and CPU prioritization. This article introduces you to the concepts of concurrency and workload management, explaining how both features have been implemented and how you can control them in your data warehouse. SQL Data Warehouse workload management is intended to help you support multiuser environments. It is not intended for multitenant workloads.

## Concurrency limits
SQL Data Warehouse allows up to 1,024 concurrent connections. All 1,024 connections can submit queries concurrently. However, to optimize throughput, SQL Data Warehouse may queue some queries to ensure that each query receives a minimal memory grant. Queuing occurs at query execution time. By queuing queries when concurrency limits are reached, SQL Data Warehouse can increase total throughput by ensuring that active queries get access to critically needed memory resources.  

Concurrency limits are governed by two concepts: *concurrent queries* and *concurrency slots*. For a query to execute, it must execute within both the query concurrency limit and the concurrency slot allocation.

* Concurrent queries are the queries executing at the same time. SQL Data Warehouse supports up to 32 concurrent queries on the larger DWU sizes.
* Concurrency slots are allocated based on DWU. Each 100 DWU provides 4 concurrency slots. For example, a DW100 allocates 4 concurrency slots and DW1000 allocates 40. Each query consumes one or more concurrency slots, dependent on the [resource class](#resource-classes) of the query. Queries running in the smallrc resource class consume one concurrency slot. Queries running in a higher resource class  consume more concurrency slots.

The following table describes the limits for both concurrent queries and concurrency slots at the various DWU sizes.

### Concurrency limits
| DWU | Max concurrent queries | Concurrency slots allocated |
|:--- |:---:|:---:|
| DW100 |4 |4 |
| DW200 |8 |8 |
| DW300 |12 |12 |
| DW400 |16 |16 |
| DW500 |20 |20 |
| DW600 |24 |24 |
| DW1000 |32 |40 |
| DW1200 |32 |48 |
| DW1500 |32 |60 |
| DW2000 |32 |80 |
| DW3000 |32 |120 |
| DW6000 |32 |240 |

When one of these thresholds is met, new queries are queued. SQL Data Warehouse executes queued queries on a first-in, first-out basis as other queries finish and the number of queries and slots falls below the limits.  

> [!NOTE]
> *Select* queries executing exclusively on dynamic management views (DMVs) or catalog views are not governed by any of the concurrency limits. Users can monitor the system regardless of the number of queries executing on it.
> 
> 

## Resource classes
Resource classes help you control memory allocation and CPU cycles given to a query. You can assign four resource classes to a user in the form of *database roles*. The four resource classes are **smallrc**, **mediumrc**, **largerc**, and **xlargerc**. Users in smallrc are given a smaller amount of memory and can take advantage of higher concurrency. In contrast, users assigned to xlargerc are given large amounts of memory, and therefore fewer of their queries can run concurrently.

By default, each user is a member of the small resource class, smallrc. The procedure `sp_addrolemember` is used to increase the resource class, and `sp_droprolemember` is used to decrease the resource class. For example, this command would increase the resource class of loaduser to largerc:

```sql
EXEC sp_addrolemember 'largerc', 'loaduser'
```

A good practice is to permanently assign users to a resource class rather than changing their resource classes. For example, loads to clustered columnstore tables create higher-quality indexes when allocated more memory. To ensure that loads have access to higher memory, create a user specifically for loading data and permanently assign this user to a higher resource class.

There are a few types of queries that do not benefit from a larger memory allocation. The system will ignore their resource class allocation and always run these queries in the small resource class instead. If these queries always run in the small resource class, they can run when concurrency slots are under pressure and they won't consume more slots than needed. See [Resource class exceptions](#query-exceptions-to-concurrency-limits) for more information.

A few more details on resource class:

* *Alter role* permission is required to change the resource class of a user.  
* Although you can add a user to one or more of the higher resource classes, users will take on the attributes of the highest resource class to which they are assigned. That is, if a user is assigned to both mediumrc and largerc, the higher resource class (largerc) is the resource class that will be honored.  
* The resource class of the system administrative user cannot be changed.

For a detailed example, see [Changing user resource class example](#changing-user-resource-class-example).

## Memory allocation
There are pros and cons to increasing a user's resource class. Although increasing a resource class for a user may mean that their queries have access to more memory and may execute faster, higher resource classes also reduce the number of concurrent queries that can run. This is the trade-off between allocating large amounts of memory to a single query and allowing other queries (which also need memory allocations) to run concurrently. If one user is given high allocations of memory for a query, other users will not have access to that same memory to run a query.

The following table maps the memory allocated to each distribution by DWU and resource class. In SQL Data Warehouse, there are 60 distributions. For example, a query running on a DW2000 in the xlargerc resource class would have access to 6,400 MB of memory within each of the 60 distributed databases.

### Memory allocations per distribution (MB)
| DWU | smallrc | mediumrc | largerc | xlargerc |
|:--- |:---:|:---:|:---:|:---:|
| DW100 |100 |100 |200 |400 |
| DW200 |100 |200 |400 |800 |
| DW300 |100 |200 |400 |800 |
| DW400 |100 |400 |800 |1,600 |
| DW500 |100 |400 |800 |1,600 |
| DW600 |100 |400 |800 |1,600 |
| DW1000 |100 |800 |1,600 |3,200 |
| DW1200 |100 |800 |1,600 |3,200 |
| DW1500 |100 |800 |1,600 |3,200 |
| DW2000 |100 |1,600 |3,200 |6,400 |
| DW3000 |100 |1,600 |3,200 |6,400 |
| DW6000 |100 |3,200 |6,400 |12,800 |

In the preceding example, a query running on a DW2000 in the xlargerc resource class is allocated a total of 375 GB of memory (6,400 MB * 60 distributions / 1,024 to convert to GB) over the entirety of SQL Data Warehouse.

### Memory allocations system-wide (GB)
| DWU | smallrc | mediumrc | largerc | xlargerc |
|:--- |:---:|:---:|:---:|:---:|
| DW100 |6 |6 |12 |23 |
| DW200 |6 |12 |23 |47 |
| DW300 |6 |12 |23 |47 |
| DW400 |6 |23 |47 |94 |
| DW500 |6 |23 |47 |94 |
| DW600 |6 |23 |47 |94 |
| DW1000 |6 |47 |94 |188 |
| DW1200 |6 |47 |94 |188 |
| DW1500 |6 |47 |94 |188 |
| DW2000 |6 |94 |188 |375 |
| DW3000 |6 |94 |188 |375 |
| DW6000 |6 |188 |375 |750 |

## Concurrency slot consumption
SQL Data Warehouse grants more memory to queries running in higher resource classes. Because memory is a fixed resource, the more memory allocated per query, the less concurrency can be supported. The following table reiterates all of the previous concepts in a single view that shows the number of concurrency slots available by DWU and the slots consumed by each resource class.

### Allocation and consumption of concurrency slots
| DWU | Maximum concurrent queries | Concurrency slots allocated | Slots used by smallrc | Slots used by mediumrc | Slots used by largerc | Slots used by xlargerc |
|:--- |:---:|:---:|:---:|:---:|:---:|:---:|
| DW100 |4 |4 |1 |1 |2 |4 |
| DW200 |8 |8 |1 |2 |4 |8 |
| DW300 |12 |12 |1 |2 |4 |8 |
| DW400 |16 |16 |1 |4 |8 |16 |
| DW500 |20 |20 |1 |4 |8 |16 |
| DW600 |24 |24 |1 |4 |8 |16 |
| DW1000 |32 |40 |1 |8 |16 |32 |
| DW1200 |32 |48 |1 |8 |16 |32 |
| DW1500 |32 |60 |1 |8 |16 |32 |
| DW2000 |32 |80 |1 |16 |32 |64 |
| DW3000 |32 |120 |1 |16 |32 |64 |
| DW6000 |32 |240 |1 |32 |64 |128 |

From this table, you can see that SQL Data Warehouse running as DW1000 allocates a maximum of 32 concurrent queries and a total of 40 concurrency slots. If all users are running in smallrc, 32 concurrent queries would be allowed because each query would consume 1 concurrency slot. If all users on a DW1000 were running in mediumrc, each query would be allocated 800 MB per distribution for a total memory allocation of 47 GB per query, and concurrency would be limited to 5 users (40 concurrency slots / 8 slots per mediumrc user).

## Query importance
SQL Data Warehouse implements resource classes by using workload groups. There are a total of eight workload groups that control the behavior of the resource classes across the various DWU sizes. For any DWU, SQL Data Warehouse uses only four of the eight workload groups. This makes sense because each workload group is assigned to one of four resource classes: smallrc, mediumrc, largerc, or xlargerc. The importance of understanding the workload groups is that some of these workload groups are set to higher *importance*. Importance is used for CPU scheduling. Queries run with high importance will get three times more CPU cycles than those with medium importance. Therefore, concurrency slot mappings also determine CPU priority. When a query consumes 16 or more slots, it runs as high importance.

The following table shows the importance mappings for each workload group.

### Workload group mappings to concurrency slots and importance
| Workload groups | Concurrency slot mapping | Importance mapping |
|:--- |:---:|:--- |
| SloDWGroupC00 |1 |Medium |
| SloDWGroupC01 |2 |Medium |
| SloDWGroupC02 |4 |Medium |
| SloDWGroupC03 |8 |Medium |
| SloDWGroupC04 |16 |High |
| SloDWGroupC05 |32 |High |
| SloDWGroupC06 |64 |High |
| SloDWGroupC07 |128 |High |

From the **Allocation and consumption of concurrency slots** chart, you can see that a DW500 uses 1, 4, 8 or 16 concurrency slots for smallrc, mediumrc, largerc, and xlargerc, respectively. You can look those values up in the preceding chart to find the importance for each resource class.

### DW500 mapping of resource classes to importance
| Resource class | Workload group | Concurrency slots used | Importance |
|:--- |:--- |:---:|:--- |
| smallrc |SloDWGroupC00 |1 |Medium |
| mediumrc |SloDWGroupC02 |4 |Medium |
| largerc |SloDWGroupC03 |8 |Medium |
| xlargerc |SloDWGroupC04 |16 |High |

You can use the following DMV query to look at the differences in memory resource allocation in detail from the perspective of the resource governor, or to analyze active and historic usage of the workload groups when troubleshooting.

```sql
WITH rg
AS
(   SELECT  
     pn.name                        AS node_name
    ,pn.[type]                        AS node_type
    ,pn.pdw_node_id                    AS node_id
    ,rp.name                        AS pool_name
    ,rp.max_memory_kb*1.0/1024                AS pool_max_mem_MB
    ,wg.name                        AS group_name
    ,wg.importance                    AS group_importance
    ,wg.request_max_memory_grant_percent        AS group_request_max_memory_grant_pcnt
    ,wg.max_dop                        AS group_max_dop
    ,wg.effective_max_dop                AS group_effective_max_dop
    ,wg.total_request_count                AS group_total_request_count
    ,wg.total_queued_request_count            AS group_total_queued_request_count
    ,wg.active_request_count                AS group_active_request_count
    ,wg.queued_request_count                AS group_queued_request_count
    FROM    sys.dm_pdw_nodes_resource_governor_workload_groups wg
    JOIN    sys.dm_pdw_nodes_resource_governor_resource_pools rp    
            ON  wg.pdw_node_id  = rp.pdw_node_id
            AND wg.pool_id      = rp.pool_id
    JOIN    sys.dm_pdw_nodes pn
            ON    wg.pdw_node_id    = pn.pdw_node_id
    WHERE   wg.name like 'SloDWGroup%'
        AND     rp.name = 'SloDWPool'
)
SELECT    pool_name
,        pool_max_mem_MB
,        group_name
,        group_importance
,        (pool_max_mem_MB/100)*group_request_max_memory_grant_pcnt AS max_memory_grant_MB
,        node_name
,        node_type
,       group_total_request_count
,       group_total_queued_request_count
,       group_active_request_count
,       group_queued_request_count
FROM    rg
ORDER BY
    node_name
,    group_request_max_memory_grant_pcnt
,    group_importance
;
```

## Queries that honor concurrency limits
Most queries are governed by resource classes. These queries must fit inside both the concurrent query and concurrency slot thresholds. A user cannot choose to exclude a query from the concurrency slot model.

To reiterate, the following statements honor resource classes:

* INSERT-SELECT
* UPDATE
* DELETE
* SELECT (when querying user tables)
* ALTER INDEX REBUILD
* ALTER INDEX REORGANIZE
* ALTER TABLE REBUILD
* CREATE INDEX
* CREATE CLUSTERED COLUMNSTORE INDEX
* CREATE TABLE AS SELECT (CTAS)
* Data loading
* Data movement operations conducted by the Data Movement Service (DMS)

## Query exceptions to concurrency limits
Some queries do not honor the resource class to which the user is assigned. These exceptions to the concurrency limits are made when the memory resources needed for a particular command are low, often because the command is a metadata operation. The goal of these exceptions is to avoid larger memory allocations for queries that will never need them. In these cases, the default small resource class (smallrc) is always used regardless of the actual resource class assigned to the user. For example, `CREATE LOGIN` will always run in smallrc. The resources required to fulfil this operation are very low, so it does not make sense to include the query in the concurrency slot model.  These queries are also not limited by the 32 user concurrency limit, an unlimited number of these queries can run up to the session limit of 1,024 sessions.

The following statements do not honor resource classes:

* CREATE or DROP TABLE
* ALTER TABLE ... SWITCH, SPLIT, or MERGE PARTITION
* ALTER INDEX DISABLE
* DROP INDEX
* CREATE, UPDATE, or DROP STATISTICS
* TRUNCATE TABLE
* ALTER AUTHORIZATION
* CREATE LOGIN
* CREATE, ALTER or DROP USER
* CREATE, ALTER or DROP PROCEDURE
* CREATE or DROP VIEW
* INSERT VALUES
* SELECT from system views and DMVs
* EXPLAIN
* DBCC

<!--
Removed as these two are not confirmed / supported under SQLDW
- CREATE REMOTE TABLE AS SELECT
- CREATE EXTERNAL TABLE AS SELECT
- REDISTRIBUTE
-->

## Change a user resource class example
1. **Create login:** Open a connection to your **master** database on the SQL server hosting your SQL Data Warehouse database and execute the following commands.
   
    ```sql
    CREATE LOGIN newperson WITH PASSWORD = 'mypassword';
    CREATE USER newperson for LOGIN newperson;
    ```
   
   > [!NOTE]
   > It is a good idea to create a user in the master database for Azure SQL Data Warehouse users. Creating a user in master allows a user to login using tools like SSMS without specifying a database name.  It also allows them to use the object explorer to view all databases on a SQL server.  For more details about creating and managing users, see [Secure a database in SQL Data Warehouse][Secure a database in SQL Data Warehouse].
   > 
   > 
2. **Create SQL Data Warehouse user:** Open a connection to the **SQL Data Warehouse** database and execute the following command.
   
    ```sql
    CREATE USER newperson FOR LOGIN newperson;
    ```
3. **Grant permissions:** The following example grants `CONTROL` on the **SQL Data Warehouse** database. `CONTROL` at the database level is the equivalent of db_owner in SQL Server.
   
    ```sql
    GRANT CONTROL ON DATABASE::MySQLDW to newperson;
    ```
4. **Increase resource class:** Use the following query to add a user to a higher workload management role.
   
    ```sql
    EXEC sp_addrolemember 'largerc', 'newperson'
    ```
5. **Decrease resource class:** Use the following query to remove a user from a workload management role.
   
    ```sql
    EXEC sp_droprolemember 'largerc', 'newperson';
    ```
   
   > [!NOTE]
   > It is not possible to remove a user from smallrc.
   > 
   > 

## Queued query detection and other DMVs
You can use the `sys.dm_pdw_exec_requests` DMV to identify queries that are waiting in a concurrency queue. Queries waiting for a concurrency slot will have a status of **suspended**.

```sql
SELECT      r.[request_id]                 AS Request_ID
        ,r.[status]                 AS Request_Status
        ,r.[submit_time]             AS Request_SubmitTime
        ,r.[start_time]                 AS Request_StartTime
        ,DATEDIFF(ms,[submit_time],[start_time]) AS Request_InitiateDuration_ms
        ,r.resource_class                         AS Request_resource_class
FROM    sys.dm_pdw_exec_requests r;
```

Workload management roles can be viewed with `sys.database_principals`.

```sql
SELECT  ro.[name]           AS [db_role_name]
FROM    sys.database_principals ro
WHERE   ro.[type_desc]      = 'DATABASE_ROLE'
AND     ro.[is_fixed_role]  = 0;
```

The following query shows which role each user is assigned to.

```sql
SELECT     r.name AS role_principal_name
        ,m.name AS member_principal_name
FROM    sys.database_role_members rm
JOIN    sys.database_principals AS r            ON rm.role_principal_id        = r.principal_id
JOIN    sys.database_principals AS m            ON rm.member_principal_id    = m.principal_id
WHERE    r.name IN ('mediumrc','largerc', 'xlargerc');
```

SQL Data Warehouse has the following wait types:

* **LocalQueriesConcurrencyResourceType**: Queries that sit outside of the concurrency slot framework. DMV queries and system functions such as `SELECT @@VERSION` are examples of local queries.
* **UserConcurrencyResourceType**: Queries that sit inside the concurrency slot framework. Queries against end-user tables represent examples that would use this resource type.
* **DmsConcurrencyResourceType**: Waits resulting from data movement operations.
* **BackupConcurrencyResourceType**: This wait indicates that a database is being backed up. The maximum value for this resource type is 1. If multiple backups have been requested at the same time, the others will queue.

The `sys.dm_pdw_waits` DMV can be used to see which resources a request is waiting for.

```sql
SELECT  w.[wait_id]
,       w.[session_id]
,       w.[type]            AS Wait_type
,       w.[object_type]
,       w.[object_name]
,       w.[request_id]
,       w.[request_time]
,       w.[acquire_time]
,       w.[state]
,       w.[priority]
,    SESSION_ID()            AS Current_session
,    s.[status]            AS Session_status
,    s.[login_name]
,    s.[query_count]
,    s.[client_id]
,    s.[sql_spid]
,    r.[command]            AS Request_command
,    r.[label]
,    r.[status]            AS Request_status
,    r.[submit_time]
,    r.[start_time]
,    r.[end_compile_time]
,    r.[end_time]
,    DATEDIFF(ms,r.[submit_time],r.[start_time])        AS Request_queue_time_ms
,    DATEDIFF(ms,r.[start_time],r.[end_compile_time])    AS Request_compile_time_ms
,    DATEDIFF(ms,r.[end_compile_time],r.[end_time])        AS Request_execution_time_ms
,    r.[total_elapsed_time]
FROM    sys.dm_pdw_waits w
JOIN    sys.dm_pdw_exec_sessions s  ON w.[session_id] = s.[session_id]
JOIN    sys.dm_pdw_exec_requests r  ON w.[request_id] = r.[request_id]
WHERE    w.[session_id] <> SESSION_ID();
```

The `sys.dm_pdw_resource_waits` DMV shows only the resource waits consumed by a given query. Resource wait time only measures the time waiting for resources to be provided, as opposed to signal wait time, which is the time it takes for the underlying SQL servers to schedule the query onto the CPU.

```sql
SELECT  [session_id]
,       [type]
,       [object_type]
,       [object_name]
,       [request_id]
,       [request_time]
,       [acquire_time]
,       DATEDIFF(ms,[request_time],[acquire_time])  AS acquire_duration_ms
,       [concurrency_slots_used]                    AS concurrency_slots_reserved
,       [resource_class]
,       [wait_id]                                   AS queue_position
FROM    sys.dm_pdw_resource_waits
WHERE    [session_id] <> SESSION_ID();
```

The `sys.dm_pdw_wait_stats` DMV can be used for historic trend analysis of waits.

```sql
SELECT    w.[pdw_node_id]
,        w.[wait_name]
,        w.[max_wait_time]
,        w.[request_count]
,        w.[signal_time]
,        w.[completed_count]
,        w.[wait_time]
FROM    sys.dm_pdw_wait_stats w;
```

## Next steps
For more information about managing database users and security, see [Secure a database in SQL Data Warehouse][Secure a database in SQL Data Warehouse]. For more information about how larger resource classes can improve clustered columnstore index quality, see [Rebuilding indexes to improve segment quality].

<!--Image references-->

<!--Article references-->
[Secure a database in SQL Data Warehouse]: ./sql-data-warehouse-overview-manage-security.md
[Rebuilding indexes to improve segment quality]: ./sql-data-warehouse-tables-index.md#rebuilding-indexes-to-improve-segment-quality
[Secure a database in SQL Data Warehouse]: ./sql-data-warehouse-overview-manage-security.md

<!--MSDN references-->
[Managing Databases and Logins in Azure SQL Database]:https://msdn.microsoft.com/library/azure/ee336235.aspx

<!--Other Web references-->
