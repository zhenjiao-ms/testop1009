---
title: All topics for SQL Database service | Microsoft Azure
description: Table of all topics for the Azure service named SQL Database that exist on http://azure.microsoft.com/documentation/articles/, Title and description.
services: sql-database
documentationcenter: ''
author: MightyPen
manager: jhubbard
editor: ''

ms.service: sql-database
ms.workload: sql-database
ms.tgt_pltfrm: na
ms.devlang: na
ms.topic: article
ms.date: 08/21/2016
ms.author: genemi

---
# All topics for Azure SQL Database service
This topic lists every topic that applies directly to the **SQL Database** service of Azure. You can search this webpage for keywords by using **Ctrl+F**, to find the topics of current interest.

## New
| &nbsp; | Title | Description |
| ---:|:--- |:--- |
| 1 |[Getting started with JSON features in Azure SQL Database](sql-database-json-features.md) |Azure SQL Database enables you to parse, query, and format data in JavaScript Object Notation (JSON) notation. |
| 2 |[SSMS support for Azure AD MFA with SQL Database and SQL Data Warehouse](sql-database-ssms-mfa-authentication.md) |Use Multi-Factored Authentication with SSMS for SQL Database and SQL Data Warehouse. |

## Updated articles
This section lists articles which were updated recently, where the update was big or significant. For each updated article, a rough snippet of the added markdown text is displayed. The articles were updated within the date range of **2016-07-26** to **2016-08-21**.

| &nbsp; | Article | Updated text, snippet |
| ---:|:--- |:--- |
| 3 |[Archive an Azure SQL database to a BACPAC file by using PowerShell](sql-database-export-powershell.md) |$subscriptionId = "YOUR AZURE SUBSCRIPTION ID"     Login-AzureRmAccount     Set-AzureRmContext -SubscriptionId $subscriptionId       Database to export     $DatabaseName = "DATABASE-NAME"     $ResourceGroupName = "RESOURCE-GROUP-NAME"     $ServerName = "SERVER-NAME"     $serverAdmin = "ADMIN-NAME"     $serverPassword = "ADMIN-PASSWORD"     $securePassword = ConvertTo-SecureString ΓÇôString $serverPassword ΓÇôAsPlainText -Force     $creds = New-Object ΓÇôTypeName System.Management.Automation.PSCredential ΓÇôArgumentList $serverAdmin, $securePassword       Generate a unique filename for the BACPAC     $bacpacFilename = $DatabaseName + (Get-Date).ToString("yyyyMMddHHmm") + ".bacpac"       Storage account info for the BACPAC     $BaseStorageUri = "https://STORAGE-NAME.blob.core.windows.net/BLOB-CONTAINER-NAME/"     $BacpacUri = $BaseStorageUri + $bacpacFilename     $StorageKeytype = "StorageAccessKey"     $StorageKey = "YOUR STORAGE KEY"     $exportRequest = New-AzureRmSqlDatabaseExpo |
| 4 |[SQL Database options and performance: Understand what's available in each service tier](sql-database-service-tiers.md) |** Choosing a service tier** To decide on a service tier, start by determining whether the database will be a standalone database or will be part of an elastic pool. ** Choosing a service tier for a standalone database** To decide on a service tier for a standalone database, start by determining the database features that you need in order to choose your SQL Database edition: / Database size (5 GB maximum for Basic, 250 GB maximum for Standard, and 500 GB to 1 TB maximum for Premium - depending on the performance level) / Database backup retention period (7 days for Basic, 35 days for Standard, and 35 days for Premium) Once you have determined the SQL Database edition, you are ready to determine the performance level for the database (the number of DTUs). You can guess and then  scale up or down dynamically (sql-database-scale-up.md) based on actual experience. You can also use the  DTU Calculator (http://dtucalculator.azurewebsites.net/) to approximate the number of DTUs needed. ** C |

## Get started
| &nbsp; | Title | Description |
| ---:|:--- |:--- |
| 5 |[Builds Multi-tenant Apps with Azure SQL Database With Isolation and Efficiency](sql-database-build-multi-tenant-apps.md) |Learn how SQL Database builds multi-tenant apps |
| 6 |[Connect to SQL Database with SQL Server Management Studio and execute a sample T-SQL query](sql-database-connect-query-ssms.md) |Learn how to connect to SQL Database on Azure by using SQL Server Management Studio (SSMS). Then, run a sample query using Transact-SQL (T-SQL). |
| 7 |[Connect to SQL Database by using .NET (C#)](sql-database-develop-dotnet-simple.md) |Use the sample code in this quick start to build a modern application with C# and backed by a powerful relational database in the cloud with Azure SQL Database. |
| 8 |[Create a new elastic database pool with the Azure portal](sql-database-elastic-pool-create-portal.md) |How to add a scalable elastic database pool to your SQL database configuration for easier administration and resource sharing across many databases. |
| 9 |[Explore Azure SQL Database Tutorials](sql-database-explore-tutorials.md) |Learn about SQL Database features and capabilities |
| 10 |[SQL Database tutorial: Create a SQL database in minutes using the Azure portal](sql-database-get-started.md) |Learn how to set up a SQL Database logical server, server firewall rule, SQL database, sample data, connect with client tools, configure users, and database firewall rule. |
| 11 |[Azure SQL Database Secures and Protects](sql-database-helps-secures-and-protects.md) |Learn how SQL Database helps secure and protect |
| 12 |[Azure SQL Database Learns &amp; Adapts](sql-database-learn-and-adapt.md) |Learn how SQL Database learns and adapts |
| 13 |[Choose a cloud SQL Server option: Azure SQL (PaaS) Database  or SQL Server on Azure VMs (IaaS)](sql-database-paas-vs-sql-server-iaas.md) |Learn which cloud SQL Server option fits your application: Azure SQL (PaaS) Database or SQL Server in the cloud on Azure Virtual Machines. |
| 14 |[Azure SQL Database Scales on the fly](sql-database-scale-on-the-fly.md) |Learn how SQL Database scales on the fly |
| 15 |[Explore Azure SQL Database Solution Quick Starts](sql-database-solution-quick-starts.md) |Learn about Azure SQL Database Solutions |
| 16 |[Azure SQL Database Works in your Environment](sql-database-works-in-your-environment.md) |Learn how SQL Database helps, secures and protects |

## Build an app
| &nbsp; | Title | Description |
| ---:|:--- |:--- |
| 17 |[Troubleshoot, diagnose, and prevent SQL connection errors and transient errors for SQL Database](sql-database-connectivity-issues.md) |Learn how to troubleshoot, diagnose, and prevent a SQL connection error or transient error in Azure SQL Database. |
| 18 |[Connect to a SQL Database with Visual Studio](sql-database-connect-query.md) |Write a program in C# to query and connect to SQL database. Info about IP addresses, connection strings, secure login, and free Visual Studio. |
| 19 |[Ports beyond 1433 for ADO.NET 4.5 and SQL Database V12](sql-database-develop-direct-route-ports-adonet-v12.md) |Client connections from ADO.NET to Azure SQL Database V12 sometimes bypass the proxy and interact directly with the database. Ports other than 1433 become important. |
| 20 |[SQL error codes for SQL Database client applications: Database connection error and other issues](sql-database-develop-error-messages.md) |Learn about SQL error codes for SQL Database client applications, such as common database connection errors, database copy issues, and general errors. |
| 21 |[Connect to SQL Database by using PHP on Windows](sql-database-develop-php-simple.md) |Presents a sample PHP program that connects to Azure SQL Database from a Windows client, and provides links to the necessary software components needed by the client. |
| 22 |[Try SQL Database: Use C# to create a SQL database with the SQL Database Library for .NET](sql-database-get-started-csharp.md) |Try SQL Database for developing SQL and C# apps, and create an Azure SQL Database with C# using the SQL Database Library for .NET. |
| 23 |[Troubleshoot connection issues to Azure SQL Database](sql-database-troubleshoot-common-connection-issues.md) |Steps to identify and resolve common connection errors for Azure SQL Database. |
| 24 |[Error "Database on server is not currently available" when connecting to sql database](sql-database-troubleshoot-connection.md) |Troubleshoot the database on server is not currently available error when an application connects to SQL Database. |

## Develop
| &nbsp; | Title | Description |
| ---:|:--- |:--- |
| 25 |[Get the client id and key for connecting to SQL Database from code](sql-database-client-id-keys.md) |Get the client id and key for accessing SQL Database from code. |
| 26 |[Connect to SQL Database by using Java with JDBC on Windows](sql-database-develop-java-simple.md) |Presents a Java code sample you can use to connect to Azure SQL Database. The sample uses JDBC, and it runs on a Windows client computer. |
| 27 |[Connect to SQL Database by using Node.js](sql-database-develop-nodejs-simple.md) |Presents a Node.js code sample you can use to connect to Azure SQL Database. |
| 28 |[SQL Database Development Overview](sql-database-develop-overview.md) |Learn about available connectivity libraries and best practices for applications connecting to SQL Database. |
| 29 |[Connect to SQL Database by using Python](sql-database-develop-python-simple.md) |Presents a Python code sample you can use to connect to Azure SQL Database. |
| 30 |[Connect to SQL Database by using Ruby](sql-database-develop-ruby-simple.md) |Give a Ruby code sample you can run to connect to Azure SQL Database. |
| 31 |[Getting Started with Temporal Tables in Azure SQL Database](sql-database-temporal-tables.md) |Learn how to get started with using Temporal Tables in Azure SQL Database. |

## Performance and scale
| &nbsp; | Title | Description |
| ---:|:--- |:--- |
| 32 |[SQL Database Advisor](sql-database-advisor.md) |The Azure SQL Database Advisor provides recommendations for your existing SQL Databases that can improve current query performance. |
| 33 |[SQL Database Advisor](sql-database-advisor-portal.md) |You can use the Azure SQL Database Advisor in the Azure portal to review and implement recommendations for your existing SQL Databases that can improve current query performance. |
| 34 |[Azure SQL Database benchmark overview](sql-database-benchmark-overview.md) |This topic describes the Azure SQL Database Benchmark used in measuring the performance of Azure SQL Database. |
| 35 |[When should an elastic database pool be used?](sql-database-elastic-pool-guidance.md) |An elastic database pool is a collection of available resources that are shared by a group of elastic databases. This document provides guidance to help assess the suitability of using an elastic database pool for a group of databases. |
| 36 |[Get started with Elastic Database tools](sql-database-elastic-scale-get-started.md) |Basic explanation of elastic database tools feature of Azure SQL Database, including easy to run sample app. |
| 37 |[SQL Database FAQ](sql-database-faq.md) |Answers to common questions customers ask about cloud databases and Azure SQL Database, Microsoft's relational database management system (RDBMS) and database as a service in the cloud. |
| 38 |[Get started with In-Memory (Preview) in SQL Database](sql-database-in-memory.md) |SQL In-Memory technologies greatly improve the performance of transactional and analytics workloads. Learn how to take advantage of these technologies. |
| 39 |[Use In-Memory OLTP (preview) to improve your application performance in SQL Database](sql-database-in-memory-oltp-migration.md) |Adopt In-Memory OLTP to improve transactional performance in an existing SQL database. |
| 40 |[Monitor In-Memory OLTP Storage](sql-database-in-memory-oltp-monitoring.md) |Estimate and monitor XTP in-memory storage use, capacity; resolve capacity error 41823 |
| 41 |[Operating the Query Store in Azure SQL Database](sql-database-operate-query-store.md) |Learn how to operate the Query Store in Azure SQL Database |
| 42 |[SQL Database Performance Insight](sql-database-performance.md) |The Azure SQL Database provides performance tools to help you identify areas that can improve current query performance. |
| 43 |[Azure SQL Database performance guidance for single databases](sql-database-performance-guidance.md) |This topic provides guidance to help you determine which service tier is right for your application and provides recommendations for tuning your application to get the most out of your Azure SQL Database. |
| 44 |[Azure SQL Database Query Performance Insight](sql-database-query-performance.md) |Query performance monitoring identifies the most CPU-consuming queries for an Azure SQL Database. |
| 45 |[Change the service tier and performance level (pricing tier) of a SQL database](sql-database-scale-up.md) |Change the service tier and performance level of an Azure SQL database shows how to scale your SQL database up or down. Changing the pricing tier of an Azure SQL database. |
| 46 |[Monitoring database performance in Azure SQL Database](sql-database-single-database-monitor.md) |Learn about the options for monitoring your database with Azure tools and dynamic management views. |
| 47 |[SQL Database performance tuning tips](sql-database-troubleshoot-performance.md) |Tips for performance tuning in Azure SQL Database through evaluation and improvement. |
| 48 |[How to use batching to improve SQL Database application performance](sql-database-use-batching-to-improve-performance.md) |The topic provides evidence that batching database operations greatly imroves the speed and scalability of your Azure SQL Database applications. Although these batching techniques work for any SQL Server database, the focus of the article is on Azure. |

## Tools for scaling out
| &nbsp; | Title | Description |
| ---:|:--- |:--- |
| 49 |[Design patterns for multitenant SaaS applications and Azure SQL Database](sql-database-design-patterns-multi-tenancy-saas-applications.md) |This article discusses the requirements and common data architecture patterns of multitenant database applications running in a cloud environment need to consider and the various tradeoffs associated with these patterns. It also explains how Azure SQL Database, with its elastic database pools and elastic tools, help address these requirements in a no-compromise fashion. |
| 50 |[Migrate existing databases to scale-out](sql-database-elastic-convert-to-use-elastic-tools.md) |Convert sharded databases to use elastic database tools by creating a shard map manager |
| 51 |[Building scalable cloud databases](sql-database-elastic-database-client-library.md) |Build scalable .NET database apps with the elastic database client library |
| 52 |[Performance counters for shard map manager](sql-database-elastic-database-perf-counters.md) |ShardMapManager class and data dependent routing performance counters |
| 53 |[Adding a shard using Elastic Database tools](sql-database-elastic-scale-add-a-shard.md) |How to use Elastic Scale APIs to add new shards to a shard set. |
| 54 |[Deploy a split-merge service](sql-database-elastic-scale-configure-deploy-split-and-merge.md) |Splitting and Merging with elastic database tools |
| 55 |[Data dependent routing](sql-database-elastic-scale-data-dependent-routing.md) |How to use the ShardMapManager class in .NET apps for data-dependent routing, a feature of elastic databases for Azure SQL Database |
| 56 |[Elastic database tools FAQ](sql-database-elastic-scale-faq.md) |Frequently Asked Questions about Azure SQL Database Elastic Scale. |
| 57 |[Elastic Database tools glossary](sql-database-elastic-scale-glossary.md) |Explanation of terms used for elastic database tools |
| 58 |[Scaling out with Azure SQL Database](sql-database-elastic-scale-introduction.md) |Software as a Service (SaaS) developers can easily create elastic, scalable databases in the cloud using these tools |
| 59 |[Credentials used to access the Elastic Database client library](sql-database-elastic-scale-manage-credentials.md) |How to set the right level of credentials, admin to read-only, for elastic database apps |
| 60 |[Multi-shard querying](sql-database-elastic-scale-multishard-querying.md) |Run queries across shards using the elastic database client library. |
| 61 |[Moving data between scaled-out cloud databases](sql-database-elastic-scale-overview-split-and-merge.md) |Explains how to manipulate shards and move data via a self-hosted service using elastic database APIs. |
| 62 |[Scale out databases with the shard map manager](sql-database-elastic-scale-shard-map-management.md) |How to use the ShardMapManager, elastic database client library |
| 63 |[Split-merge security configuration](sql-database-elastic-scale-split-merge-security-configuration.md) |Set up x409 certificates for encryption |
| 64 |[Upgrade an app to use the latest elastic database client library](sql-database-elastic-scale-upgrade-client-library.md) |Upgrade apps and libraries using Nuget |
| 65 |[Elastic Database client library with Entity Framework](sql-database-elastic-scale-use-entity-framework-applications-visual-studio.md) |Use Elastic Database client library and Entity Framework for coding databases |
| 66 |[Using elastic database client library with Dapper](sql-database-elastic-scale-working-with-dapper.md) |Using elastic database client library with Dapper. |
| 67 |[Multi-tenant applications with elastic database tools and row-level security](sql-database-elastic-tools-multi-tenant-row-level-security.md) |Learn how to use elastic database tools together with row-level security to build an application with a highly scalable data tier on Azure SQL Database that supports multi-tenant shards. |

## Elastic jobs
| &nbsp; | Title | Description |
| ---:|:--- |:--- |
| 68 |[Create and manage scaled out Azure SQL Databases using elastic jobs (preview)](sql-database-elastic-jobs-create-and-manage.md) |Walk through creation and management of an elastic database job. |
| 69 |[Getting started with Elastic Database jobs](sql-database-elastic-jobs-getting-started.md) |how to use elastic database jobs |
| 70 |[Managing scaled-out cloud databases](sql-database-elastic-jobs-overview.md) |Illustrates the elastic database job service |
| 71 |[Create and manage a SQL Database elastic database jobs using PowerShell (preview)](sql-database-elastic-jobs-powershell.md) |PowerShell used to manage Azure SQL Database pools |
| 72 |[Installing Elastic Database jobs overview](sql-database-elastic-jobs-service-installation.md) |Walk through installation of the elastic job feature. |
| 73 |[Uninstall Elastic Database jobs components](sql-database-elastic-jobs-uninstall.md) |How to uninstall the elastic database jobs tool |

## Elastic pools
| &nbsp; | Title | Description |
| ---:|:--- |:--- |
| 74 |[What is an Azure elastic database pool?](sql-database-elastic-pool.md) |Manage hundreds or thousands of databases using a pool. One price for a set of performance units can be distributed over the pool. Move databases in or out at will. |
| 75 |[Create a new elastic database pool with C#](sql-database-elastic-pool-create-csharp.md) |Use C# database development techniques to create a scalable elastic database pool in Azure SQL Database so you can share resources across many databases. |
| 76 |[Create a new elastic database pool with PowerShell](sql-database-elastic-pool-create-powershell.md) |Learn how to use PowerShell to scale-out Azure SQL Database resources by creating a scalable elastic database pool to manage multiple databases. |
| 77 |[C# database development: Create and configure an elastic database pool for SQL database](sql-database-elastic-pool-csharp.md) |Use C# database development techniques to create an Azure SQL Database elastic database pool so you can share resources across many databases. |
| 78 |[PowerShell script for identifying databases suitable for an elastic database pool](sql-database-elastic-pool-database-assessment-powershell.md) |An elastic database pool is a collection of available resources that are shared by a group of elastic databases. This document provides a Powershell script to help assess the suitability of using an elastic database pool for a group of databases. |
| 79 |[Monitor and manage an elastic database pool with C#](sql-database-elastic-pool-manage-csharp.md) |Use C# database development techniques to manage an Azure SQL Database elastic database pool. |
| 80 |[Monitor and manage an elastic database pool with the Azure portal](sql-database-elastic-pool-manage-portal.md) |Learn how to use the Azure portal and SQL Database's built-in intelligence to manage, monitor, and right-size a scalable elastic database pool to optimize database performance and manage cost. |
| 81 |[Monitor and manage an elastic database pool with PowerShell](sql-database-elastic-pool-manage-powershell.md) |Learn how to use PowerShell to manage an elastic database pool. |
| 82 |[Monitor and manage an elastic database pool with Transact-SQL](sql-database-elastic-pool-manage-tsql.md) |Use T-SQL to create an Azure SQL database in an elastic pool. Or use T-SQL to move the datbase in and out of pools. |
| 83 |[Elastic database pool billing and pricing information](sql-database-elastic-pool-price.md) |Pricing information specific to elastic database pools. |

## Elastic query
| &nbsp; | Title | Description |
| ---:|:--- |:--- |
| 84 |[Report across scaled-out cloud databases (preview)](sql-database-elastic-query-getting-started.md) |how to use cross database database queries |
| 85 |[Get started with cross-database queries (vertical partitioning) (preview)](sql-database-elastic-query-getting-started-vertical.md) |how to use elastic database query with vertically partitioned databases |
| 86 |[Reporting across scaled-out cloud databases (preview)](sql-database-elastic-query-horizontal-partitioning.md) |how to set up elastic queries over horizontal partitions |
| 87 |[Azure SQL Database elastic database query overview (preview)](sql-database-elastic-query-overview.md) |Overview of the elastic query feature |
| 88 |[Query across cloud databases with different schemas (preview)](sql-database-elastic-query-vertical-partitioning.md) |how to set up cross-database queries over vertical partitions |

## Elastic transaction
| &nbsp; | Title | Description |
| ---:|:--- |:--- |
| 89 |[Distributed transactions across cloud databases](sql-database-elastic-transactions-overview.md) |Overview of Elastic Database Transactions with Azure SQL Database |

## Backup and recovery
| &nbsp; | Title | Description |
| ---:|:--- |:--- |
| 90 |[SQL Database automated backups](sql-database-automated-backups.md) |Learn about SQL Database buiit-in backups that enable you to roll back an Azure SQL Database to a previous point in time or copy a database to a new database in an geographic region (up to 35 days). |
| 91 |[Overview of business continuity with Azure SQL Database](sql-database-business-continuity.md) |Learn how Azure SQL Database supports cloud business continuity and database recovery and helps keep mission-critical cloud applications running. |
| 92 |[How to restore a single table from an Azure SQL Database backup](sql-database-cloud-migrate-restore-single-table-azure-backup.md) |Learn how to restore a single table from Azure SQL Database backup. |
| 93 |[Design an application for cloud disaster recovery using Active Geo-Replication in SQL Database](sql-database-designing-cloud-solutions-for-disaster-recovery.md) |Learn how to design cloud disaster recovery solutions for business continuity planning using geo-replication for app data backup with Azure SQL Database. |
| 94 |[Restore an Azure SQL Database or failover to a secondary](sql-database-disaster-recovery.md) |Learn how to recover a database from a regional datacenter outage or failure with the Azure SQL Database Active Geo-Replication, and Geo-Restore capabilities. |
| 95 |[Performing Disaster Recovery Drill](sql-database-disaster-recovery-drills.md) |Learn guidance and best practices for using Azure SQL Database to perform disaster recovery drills that will help keep your mission critical business applications resilient to failures and outages. |
| 96 |[Disaster recovery strategies for applications using SQL Database Elastic Pool](sql-database-disaster-recovery-strategies-for-applications-with-elastic-pool.md) |Learn how to design your cloud solution for disaster recovery by choosing the right failover pattern. |
| 97 |[Using the RecoveryManager class to fix shard map problems](sql-database-elastic-database-recovery-manager.md) |Use the RecoveryManager class to solve problems with shard maps |
| 98 |[Import a BACPAC file to create a new Azure SQL database](sql-database-import.md) |Create a new Azure SQL database by importing an existing BACPAC file. |
| 99 |[Restore an Azure SQL Database to a previous point in time with the Azure Portal](sql-database-point-in-time-restore-portal.md) |Restore an Azure SQL Database to a previous point in time. |
| 100 |[Restore an Azure SQL Database to a previous point in time with PowerShell](sql-database-point-in-time-restore-powershell.md) |Restore an Azure SQL Database to a previous point in time |
| 101 |[Finalize your recovered Azure SQL Database](sql-database-recovered-finalize.md) |Point in Time Restore, Microsoft Azure SQL Database, restore database, recover database, Azure Classic Portal, Azure Classic Portal |
| 102 |[Recover an Azure SQL database using automated database backups](sql-database-recovery-using-backups.md) |Learn about Point-in-Time Restore, that enables you to roll back an Azure SQL Database to a previous point in time (up to 35 days). |
| 103 |[Restore a deleted Azure SQL database using the Azure Portal](sql-database-restore-deleted-database-portal.md) |Restore a deleted Azure SQL database (Azure Portal). |
| 104 |[Restore a deleted Azure SQL Database by using PowerShell](sql-database-restore-deleted-database-powershell.md) |Restore a deleted Azure SQL Database (PowerShell). |
| 105 |[Restore a database to a previous point in time, restore a deleted database, or recover from a data center outage](sql-database-troubleshoot-backup-and-restore.md) |Learn how to recover a cloud database from errors and outages using backups and replicas in Azure SQL Database. |

## Migrate
| &nbsp; | Title | Description |
| ---:|:--- |:--- |
| 106 |[Export a SQL Server database to a BACPAC file using SqlPackage](sql-database-cloud-migrate-compatible-export-bacpac-sqlpackage.md) |Microsoft Azure SQL Database, database migration, export database, export BACPAC file, sqlpackage |
| 107 |[Export a SQL Server database to a BACPAC file using SQL Server Management Studio](sql-database-cloud-migrate-compatible-export-bacpac-ssms.md) |Microsoft Azure SQL Database, database migration, export database, export BACPAC file, Export Data Tier Application wizard |
| 108 |[Import to SQL Database from a BACPAC file using SqlPackage](sql-database-cloud-migrate-compatible-import-bacpac-sqlpackage.md) |Microsoft Azure SQL Database, database migration, import database, import BACPAC file, sqlpackage |
| 109 |[Import from BACPAC to SQL Database using SSMS](sql-database-cloud-migrate-compatible-import-bacpac-ssms.md) |Microsoft Azure SQL Database, database deploy, database migration, import database, export database, migration wizard |
| 110 |[Migrate SQL Server database to SQL Database using Deploy Database to Microsoft Azure Database Wizard](sql-database-cloud-migrate-compatible-using-ssms-migration-wizard.md) |Microsoft Azure SQL Database, database migration, Microsoft Azure Database Wizard |
| 111 |[Migrate SQL Server database to Azure SQL Database using transactional replication](sql-database-cloud-migrate-compatible-using-transactional-replication.md) |Microsoft Azure SQL Database, database migration, import database, transactional replication |
| 112 |[Determine SQL Database compatibility using SqlPackage.exe](sql-database-cloud-migrate-determine-compatibility-sqlpackage.md) |Microsoft Azure SQL Database, database migration, SQL Database compatibility, SqlPackage |
| 113 |[Use SQL Server Management Studio to Determine SQL Database compatibility before migration to Azure SQL Database](sql-database-cloud-migrate-determine-compatibility-ssms.md) |Microsoft Azure SQL Database, database migration, SQL Database compatibility, Export Data Tier Application Wizard |
| 114 |[Use SQL Azure Migration Wizard to Fix SQL Server database compatibility issues before migration to Azure SQL Database](sql-database-cloud-migrate-fix-compatibility-issues.md) |Microsoft Azure SQL Database, database migration, compatibility, SQL Azure Migration Wizard |
| 115 |[Migrate a SQL Server Database to Azure SQL Database Using SQL Server Data Tools for Visual Studio](sql-database-cloud-migrate-fix-compatibility-issues-ssdt.md) |Microsoft Azure SQL Database, database migration, compatibility, SQL Azure Migration Wizard, SSDT |
| 116 |[Fix SQL Server database compatibility issues using SQL Server Management Studio before migration to SQL Database](sql-database-cloud-migrate-fix-compatibility-issues-ssms.md) |Microsoft Azure SQL Database, database migration, compatibility, SQL Azure Migration Wizard |
| 117 |[Archive an Azure SQL database to a BACPAC file by using PowerShell](sql-database-export-powershell.md) |Archive an Azure SQL database to a BACPAC file by using PowerShell |
| 118 |[Import a BACPAC file to create a new Azure SQL database by using PowerShell](sql-database-import-powershell.md) |Import a BACPAC file to create a new Azure SQL database by using PowerShell |
| 119 |[Load data from CSV into Azure SQL Data Warehouse (flat files)](sql-database-load-from-csv-with-bcp.md) |For a small data size, uses bcp to import data into Azure SQL Database. |
| 120 |[Move databases between servers, between subscriptions, and in and out of Azure](sql-database-troubleshoot-moving-data.md) |Quick steps to copy, move, and migrate data and databases in Azure SQL Database. |

## Move data in and out
| &nbsp; | Title | Description |
| ---:|:--- |:--- |
| 121 |[SQL Server database migration to SQL Database in the cloud](sql-database-cloud-migrate.md) |Learn how about on-premises SQL Server database migration to Azure SQL Database in the cloud. Use database migration tools to test compatibility prior to database migration. |
| 122 |[Copy an Azure SQL Database](sql-database-copy.md) |Create a copy of an Azure SQL database |
| 123 |[Archive an Azure SQL database to a BACPAC file using the Azure Portal](sql-database-export.md) |Archive an Azure SQL database to a BACPAC file  using the Azure Portal |

## Security
| &nbsp; | Title | Description |
| ---:|:--- |:--- |
| 124 |[Connecting to SQL Database or SQL Data Warehouse By Using Azure Active Directory Authentication](sql-database-aad-authentication.md) |Learn how to connect to SQL Database by using Azure Active Directory Authentication. |
| 125 |[Always Encrypted: Protect sensitive data in SQL Database and store your encryption keys in the Windows certificate store](sql-database-always-encrypted.md) |Protect sensitive data in your SQL database in minutes. |
| 126 |[Always Encrypted: Protect sensitive data in SQL Database and store your encryption keys in Azure Key Vault](sql-database-always-encrypted-azure-key-vault.md) |Protect sensitive data in your SQL database in minutes. |
| 127 |[SQL Database -  Downlevel clients support and IP endpoint changes for Auditing](sql-database-auditing-and-dynamic-data-masking-downlevel-clients.md) |Learn about SQL Database downlevel clients support and IP endpoint changes for Auditing. |
| 128 |[Configure Azure SQL Database server-level firewall rules by using PowerShell](sql-database-configure-firewall-settings-powershell.md) |Learn how to configure the firewall for IP addresses that access Azure SQL databases. |
| 129 |[Configure Azure SQL Database server-level firewall rules using the REST API](sql-database-configure-firewall-settings-rest.md) |Learn how to configure the firewall for IP addresses that access Azure SQL databases. |
| 130 |[Configure Azure SQL Database server-level and database-level firewall rules using T-SQL](sql-database-configure-firewall-settings-tsql.md) |Learn how to configure the firewall for IP addresses that access Azure SQL databases. |
| 131 |[Get started with SQL Database Dynamic Data Masking (Azure Portal)](sql-database-dynamic-data-masking-get-started.md) |How to get started with SQL Database Dynamic Data Masking in the Azure Portal |
| 132 |[Get started with SQL Database Dynamic Data Masking (Azure Classic Portal)](sql-database-dynamic-data-masking-get-started-portal.md) |How to get started with SQL Database Dynamic Data Masking in the Azure Classic Portal |
| 133 |[Configure Azure SQL Database firewall rules \- overview](sql-database-firewall-configure.md) |Learn how to configure a SQL database firewall with server-level and database-level firewall rules to manage access. |
| 134 |[SQL Database tutorial: Create SQL database user accounts to access and manage a database](sql-database-get-started-security.md) |Learn how to create user accounts to access and to manage a database. |
| 135 |[SQL Database Authentication and Authorization: Granting Access](sql-database-manage-logins.md) |Learn about SQL Database security management, specifically how to manage database access and login security through the server-level principal account. |
| 136 |[Azure SQL Database security guidelines and limitations](sql-database-security-guidelines.md) |Learn about Microsoft Azure SQL Database guidelines and limitations related to security. |
| 137 |[Get started with SQL Database Threat Detection](sql-database-threat-detection-get-started.md) |How to get started with SQL Database Threat Detection in the Azure Portal |
| 138 |[How to perform common administrative tasks such as resetting admin password in Azure SQL Database](sql-database-troubleshoot-permissions.md) |Describes how to perform common administrative tasks in SQL Database. For example, resetting admin password, granting and removing access. |

## Manage your database
| &nbsp; | Title | Description |
| ---:|:--- |:--- |
| 139 |[Get started with SQL database auditing](sql-database-auditing-get-started.md) |Get started with SQL database auditing |
| 140 |[Configure an Azure SQL Database server-level firewall rule using the Azure Portal](sql-database-configure-firewall-settings.md) |Learn how to configure the firewall for IP addresses that access Azure SQL server. |
| 141 |[Copy an Azure SQL Database using the Azure portal](sql-database-copy-portal.md) |Create a copy of an Azure SQL database |
| 142 |[Managing Azure SQL Databases using Azure Automation](sql-database-manage-automation.md) |Learn about how the Azure Automation service can be used to manage Azure SQL databases at scale. |
| 143 |[Overview: management tools for SQL Database](sql-database-manage-overview.md) |Compares tools and options for managing Azure SQL Database |
| 144 |[Monitoring Azure SQL Database using dynamic management views](sql-database-monitoring-with-dmvs.md) |Learn how to detect and diagnose common performance problems by using dynamic management views to monitor Microsoft Azure SQL Database. |
| 145 |[Securing your SQL Database](sql-database-security.md) |Learn about Azure SQL Database and SQL Server security, including the differences between the cloud and SQL Server on-premises when it comes to authentication, authorization, connection security, encryption, and compliance. |

## Extended Events
| &nbsp; | Title | Description |
| ---:|:--- |:--- |
| 146 |[Event File target code for extended events in SQL Database](sql-database-xevent-code-event-file.md) |Provides PowerShell and Transact-SQL for a two-phase code sample that demonstrates the Event File target in an extended event on Azure SQL Database. Azure Storage is a required part of this scenario. |
| 147 |[Ring Buffer target code for extended events in SQL Database](sql-database-xevent-code-ring-buffer.md) |Provides a Transact-SQL code sample that is made easy and quick by use of the Ring Buffer target, in Azure SQL Database. |
| 148 |[Extended events in SQL Database](sql-database-xevent-db-diff-from-svr.md) |Describes extended events (XEvents) in Azure SQL Database, and how event sessions differ slightly from event sessions in Microsoft SQL Server. |

## Geo replication
| &nbsp; | Title | Description |
| ---:|:--- |:--- |
| 149 |[Initiate a planned or unplanned failover for Azure SQL Database with the Azure portal](sql-database-geo-replication-failover-portal.md) |Initiate a planned or unplanned failover for Azure SQL Database using the Azure portal |
| 150 |[Initiate a planned or unplanned failover for Azure SQL Database with PowerShell](sql-database-geo-replication-failover-powershell.md) |Initiate a planned or unplanned failover for Azure SQL Database using PowerShell |
| 151 |[Initiate a planned or unplanned failover for Azure SQL Database with Transact-SQL](sql-database-geo-replication-failover-transact-sql.md) |Initiate a planned or unplanned failover for Azure SQL Database using Transact-SQL |
| 152 |[Overview: SQL Database Active Geo-Replication](sql-database-geo-replication-overview.md) |Active Geo-Replication enables you to setup 4 replicas of your database in any of the Azure datacenters. |
| 153 |[Configure Geo-Replication for Azure SQL Database with the Azure portal](sql-database-geo-replication-portal.md) |Configure Geo-Replication for Azure SQL Database using the Azure portal |
| 154 |[Configure Geo-Replication for Azure SQL Database with PowerShell](sql-database-geo-replication-powershell.md) |Configure Active Geo-replication for Azure SQL Database using PowerShell |
| 155 |[How to manage Azure SQL Database security after disaster recovery](sql-database-geo-replication-security-config.md) |This topic explains security considerations for managing security after a database restore or a failover. |
| 156 |[Configure Geo-Replication for Azure SQL Database with Transact-SQL](sql-database-geo-replication-transact-sql.md) |Configure Geo-Replication for Azure SQL Database using Transact-SQL |
| 157 |[Geo-Restore an Azure SQL Database from a geo-redundant backup using the Azure Portal](sql-database-geo-restore-portal.md) |Geo-Restore an Azure SQL Database from a geo-redundant backup (Azure Portal). |
| 158 |[Restore an Azure SQL Database from a geo-redundant backup by using PowerShell](sql-database-geo-restore-powershell.md) |Restore an Azure SQL Database into a new server from a geo-redundant backup |

## Upgrade
| &nbsp; | Title | Description |
| ---:|:--- |:--- |
| 159 |[Improved query performance with compatibility Level 130 in Azure SQL Database](sql-database-compatibility-level-query-performance-130.md) |Steps and tools for determining which compatibility level is best for your database on Azure SQL Database or Microsoft SQL Server |
| 160 |[Managing rolling upgrades of cloud applications using SQL Database Active Geo-Replication](sql-database-manage-application-rolling-upgrade.md) |Learn how to use Azure SQL Database geo-replication to support online upgrades of your cloud application. |
| 161 |[Upgrade to Azure SQL Database V12 using the Azure portal](sql-database-upgrade-server-portal.md) |Explains how to upgrade to Azure SQL Database V12 including how to upgrade Web and Business databases, and how to upgrade a V11 server migrating its databases directly into an elastic database pool using the Azure portal. |
| 162 |[Upgrade to Azure SQL Database V12 using PowerShell](sql-database-upgrade-server-powershell.md) |Explains how to upgrade to Azure SQL Database V12 including how to upgrade Web and Business databases, and how to upgrade a V11 server migrating its databases directly into an elastic database pool using PowerShell. |
| 163 |[Plan and prepare to upgrade to SQL Database V12](sql-database-v12-plan-prepare-upgrade.md) |Describes the preparations and limitations involved in upgrading to version V12 of Azure SQL Database. |
| 164 |[What's new in SQL Database V12](sql-database-v12-whats-new.md) |Describes why business systems that are using Azure SQL Database in the cloud will benefit by upgrading to version V12 now. |
| 165 |[Web and Business Edition sunset FAQ](sql-database-web-business-sunset-faq.md) |Find out when the Azure SQL Web and Business databases will be retired and learn about the features and functionality of the new service tiers. |

## Tools
| &nbsp; | Title | Description |
| ---:|:--- |:--- |
| 166 |[Manage Azure SQL Database with PowerShell](sql-database-command-line-tools.md) |Azure SQL Database management with PowerShell. |
| 167 |[SQL Database tutorial: Connect Excel to an Azure SQL database and create a report](sql-database-connect-excel.md) |Learn how to connect Microsoft Excel to Azure SQL database in the cloud. Import data into Excel for reporting and data exploration. |
| 168 |[Create a SQL database and perform common database setup tasks with PowerShell cmdlets](sql-database-get-started-powershell.md) |Learn now to create a SQL database with PowerShell. Common database setup tasks can be managed through PowerShell cmdlets. |
| 169 |[Getting Started with Azure SQL Data Sync (Preview)](sql-database-get-started-sql-data-sync.md) |This tutorial helps you get started with the Azure SQL Data Sync (Preview). |
| 170 |[Managing Azure SQL Database using SQL Server Management Studio](sql-database-manage-azure-ssms.md) |Learn how to use SQL Server Management Studio to manage SQL Database servers and databases. |
| 171 |[Managing Azure SQL Databases using the Azure portal](sql-database-manage-portal.md) |Learn how to use the Azure Portal to manage a relational database in the cloud using the Azure Portal. |
| 172 |[Change the service tier and performance level (pricing tier) of a SQL database with PowerShell](sql-database-scale-up-powershell.md) |Change the service tier and performance level of an Azure SQL database shows how to scale your SQL database up or down with PowerShell. Changing the pricing tier of an Azure SQL database with PowerShell. |
| 173 |[Use SQL Server Management Studio in Azure RemoteApp to connect to SQL Database](sql-database-ssms-remoteapp.md) |Use this tutorial to learn how to use SQL Server Management Studio in Azure RemoteApp for security and performance when connecting to SQL Database |

## Reference
| &nbsp; | Title | Description |
| ---:|:--- |:--- |
| 174 |[Connection libraries for SQL Database and SQL Server](sql-database-libraries.md) |Lists the minimum version number for each driver that client programs can use to connect to Azure SQL Database or to Microsoft SQL Server. A link is provided for version information about drivers that are released by the community rather than by Microsoft. |
| 175 |[Azure SQL Database resource limits](sql-database-resource-limits.md) |This page describes some common resource limits for Azure SQL Database. |
| 176 |[Azure SQL Database Transact-SQL differences](sql-database-transact-sql-information.md) |Transact-SQL statements that are less than fully supported in Azure SQL Database |

## Miscellaneous
| &nbsp; | Title | Description |
| ---:|:--- |:--- |
| 177 |[Copy an Azure SQL database using PowerShell](sql-database-copy-powershell.md) |Create copy of an Azure SQL database using PowerShell |
| 178 |[Copy an Azure SQL database using Transact-SQL](sql-database-copy-transact-sql.md) |Create copy of an Azure SQL database using Transact-SQL |
| 179 |[Azure SQL Database General Limitations and Guidelines](sql-database-general-limitations.md) |This page describes some general limitations for Azure SQL Database as well as areas of interoperability and support. |
| 180 |[SQL Database pricing tier recommendations](sql-database-service-tier-advisor.md) |When changing pricing tiers in the Azure portal, pricing tier recommendations are provided that recommend the tier that is best suited for running an existing Azure SQL Database’s workload. Pricing tiers describe the service tier and performance level of a SQL database. |

&nbsp;

<hr/>

<a name="extras_append"></a>

## Extras
<a name="extra_related_articles"></a>

### Related articles from other Azure services
* [Back up your Azure App Services app in Azure](../app-service-web/web-sites-backup.md)

<a name="extra_documentation_tools"></a>

### Documentation tools
* [Updates announced for Azure SQL Database](http://azure.microsoft.com/updates/?service=sql-database)
* [Search all the documentation types of Microsoft Azure, with filters](http://azure.microsoft.com/search/documentation/)

<a name="extra_learning_path_graphics"></a>

### Learning path graphics
* [Learning Path graphics for all Microsoft Azure services](http://azure.microsoft.com/documentation/learning-paths/)
* [Learning Path: Learn Azure SQL Database](http://azure.microsoft.com/documentation/learning-paths/sql-database-training-learn-sql-database/)
* [Learning Path: SQL Database elastic scale](http://azure.microsoft.com/documentation/learning-paths/sql-database-elastic-scale/)

<!--
AzIxAA.ExtraAppend.sql-database.txt
C:\_MainW\VS15\AzureIndexAllArticles\AzureIndexAllArticles\In-Out\In\

This bullet link is improperly disallowed by publishing automation due to presence of string 'docuXXmentation/arXXticles':
- [Search SQL Database documentation, with filters](http://azure.microsoft.com/docuXXmentation/arXXticles/?service=sql-database)
-->


