---
title: 'SQL Database performance & options: Service tiers | Microsoft Azure'
description: Compare SQL Database performance and business continuity features of the service tiers to balance cost and capability as you scale.
keywords: database options,database performance
services: sql-database
documentationcenter: ''
author: CarlRabeler
manager: jhubbard
editor: CarlRabeler

ms.service: sql-database
ms.devlang: na
ms.topic: get-started-article
ms.tgt_pltfrm: na
ms.workload: data-management
ms.date: 08/10/2016
ms.author: carlrab

---
# SQL Database options and performance: Understand what's available in each service tier
[Azure SQL Database](sql-database-technical-overview.md) offers three service tiers with multiple performance levels to handle different workloads. Each performance level provides an increasing set of resources designed to deliver increasingly higher throughput. You can manage each database in its own [service tier](sql-database-service-tiers.md#standalone-database-service-tiers-and-performance-levels) with its own performance level. You can also manage multiple databases in an [elastic pool](sql-database-service-tiers.md#elastic-pool-service-tiers-and-performance-in-edtus) with a shared set of resources. The resources available for standalone databases are expressed in terms of Database Transaction Units (DTUs) and for elastic pools in terms of elastic DTUs or eDTUs. For more on DTUs and eDTUs, see [What is a DTU](sql-database-what-is-a-DTU.md). 

In both cases, the service tiers include **Basic**, **Standard**, and **Premium**. Database options in these tiers are similar for standalone databases and elastic pools, but there are additional considerations for elastic pools. This article provides detail of service tiers for standalone databases and elastic pools.

## Service tiers and database options
Basic, Standard, and Premium service tiers all have an uptime SLA of 99.99% and offer predictable performance, flexible business continuity options, security features, and hourly billing. The following table provides examples of the tiers best suited for different application workloads.

| Service tier | Target workloads |
| --- | --- |
| **Basic** |Best suited for a small database, supporting typically one single active operation at a given time. Examples include databases used for development or testing, or small-scale infrequently used applications. |
| **Standard** |The go-to option for most cloud applications, supporting multiple concurrent queries. Examples include workgroup or web applications. |
| **Premium** |Designed for high transactional volume, supporting many concurrent users and requiring the highest level of business continuity capabilities. Examples are databases supporting mission critical applications. |

> [!NOTE]
> Web and Business editions are retired. Read the [Sunset FAQ](https://azure.microsoft.com/pricing/details/sql-database/web-business/) if you plan to continue using Web and Business editions.
> 
> 

## Standalone database service tiers and performance levels
For standalone databases, there are multiple performance levels within each service tier. You have the flexibility to choose the level that best meets your workload’s demands. If you need to scale up or down, you can easily change the tiers of your database. See [Changing Database Service Tiers and Performance Levels](sql-database-scale-up.md) for details.

Performance characteristics listed here apply to databases created using [SQL Database V12](sql-database-v12-whats-new.md). Regardless of the number of databases hosted, your database gets a guaranteed set of resources and the expected performance characteristics of your database are not affected.

[!INCLUDE [SQL DB service tiers table](../../includes/sql-database-service-tiers-table.md)]

> [!NOTE]
> For a detailed explanation of all other rows in this service tiers table, see [Service tier capabilities and limits](sql-database-performance-guidance.md#service-tier-capabilities-and-limits).
> 
> 

## Elastic pool service tiers and performance in eDTUs
In addition to creating and scaling a standalone database, you also have the option of managing multiple databases within an [elastic pool](sql-database-elastic-pool.md). All the databases in an elastic pool share a common set of resources. The performance characteristics are measured by *elastic Database Transaction Units* (eDTUs). As with standalone databases, pools come in three service tiers: **Basic**, **Standard**, and **Premium**. For pools, these three service tiers still define the overall performance limits and several features.

Pools allow databases to share and consume DTU resources without needing to assign a specific performance level to each database in the pool. For example, a standalone database in a Standard pool can go from using 0 eDTUs to the maximum database eDTU you set up when you configure the pool. Pools allow multiple databases with varying workloads to efficiently use eDTU resources available to the entire pool. See [Price and performance considerations for an elastic pool](sql-database-elastic-pool-guidance.md) for details.

The following table describes the characteristics of pool service tiers.

[!INCLUDE [SQL DB service tiers table for elastic pools](../../includes/sql-database-service-tiers-table-elastic-db-pools.md)]

Each database within a pool also adheres to the standalone database characteristics for that tier. For example, the Basic pool has a limit for max sessions per pool of 4800 - 28800, but an individual database within a Basic pool has a database limit of 300 sessions.

## Choosing a service tier
To decide on a service tier, start by determining whether the database should be a standalone database or be part of an elastic pool. 

### Choosing a service tier for a standalone database
To decide on a service tier for a standalone database, start by determining the database features that you need to choose your SQL Database edition:

* Database size (5 GB maximum for Basic, 250 GB maximum for Standard, and 500 GB to 1 TB maximum for Premium - depending on the performance level)
* Database backup retention period (7 days for Basic, 35 days for Standard, and 35 days for Premium)

Once you have determined the SQL Database edition, you are ready to determine the performance level for the database (the number of DTUs). You can guess and then [scale up or down dynamically](sql-database-scale-up.md) based on actual experience. You can also use the [DTU Calculator](http://dtucalculator.azurewebsites.net/) to approximate the number of DTUs needed. 

### Choosing a service tier for an elastic database pool.
To decide on the service tier for an elastic database pool, start by determining the database features that you need to choose the service tier for your pool.

* Database size (2 GB for Basic, 250 GB for Standard, and 500 GB for Premium)
* Database backup retention period (7 days for Basic, 35 days for Standard, and 35 days for Premium)
* Number of databases per pool (400 for Basic, 400 for Standard, and 50 for Premium)
* Maximum storage per pool (117 GB for Basic, 1200 for Standard, and 750 for Premium)

Once you have determined the service tier for your pool, you are ready to determine the performance level for the pool (eDTUs). You can guess and then [scale up or scale down dynamically](sql-database-elastic-pool-manage-portal.md#change-performance-settings-of-a-pool) based on actual experience. You can use the [DTU Calculator](http://dtucalculator.azurewebsites.net/) to approximate the number of DTUs needed for each database in a pool to help determine the upper limit for the pool.

## Next steps
* Find out more about the pricing for these tiers on [SQL Database Pricing](https://azure.microsoft.com/pricing/details/sql-database/).
* Learn the details of [elastic pools](sql-database-elastic-pool-guidance.md) and [price and performance considerations for elastic pools](sql-database-elastic-pool-guidance.md).
* Learn how to [Monitor, manage, and resize elastic pools](sql-database-elastic-pool-manage-portal.md) and [Monitor the performance of standalone databases](sql-database-single-database-monitor.md).
* Now that you know about the SQL Database tiers, try them out with a [free account](https://azure.microsoft.com/pricing/free-trial/) and learn [how to create your first SQL database](sql-database-get-started.md).

## Additional resources
For information on common data architecture patterns of multi-tenant software-as-a-service (SaaS) database applications, see [Design Patterns for Multi-tenant SaaS Applications with Azure SQL Database](sql-database-design-patterns-multi-tenancy-saas-applications.md).

