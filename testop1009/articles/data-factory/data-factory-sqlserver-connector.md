---
title: Move data to and from SQL Server | Azure Data Factory
description: Learn about how to move data to/from SQL Server database that is on-premises or in an Azure VM using Azure Data Factory.
services: data-factory
documentationcenter: ''
author: spelluru
manager: jhubbard
editor: monicar

ms.service: data-factory
ms.workload: data-services
ms.tgt_pltfrm: na
ms.devlang: na
ms.topic: article
ms.date: 08/31/2016
ms.author: spelluru

---
# Move data to and from SQL Server on-premises or on IaaS (Azure VM) using Azure Data Factory
This article outlines how you can use the Copy Activity to move data from/to SQL Server to/from another data store. This article builds on the [data movement activities](data-factory-data-movement-activities.md) article, which presents a general overview of data movement, and data stores supported as sources and sinks.

## Enabling connectivity
The concepts and steps needed for connecting with SQL Server hosted on-premises or in Azure IaaS (Infrastructure-as-a-Service) VMs are the same. In both cases, you need to use Data Management Gateway for connectivity.

See [moving data between on-premises locations and cloud](data-factory-move-data-between-onprem-and-cloud.md) article to learn about Data Management Gateway and step-by-step instructions on setting up the gateway. Setting up a gateway instance is a pre-requisite for connecting with SQL Server.

While you can install gateway on the same on-premises machine or cloud VM instance as the SQL Server for better performance, we recommended that you install them on separate machines. Having the gateway and SQL Server on separate machines reduces resource contention.

## Copy data wizard
The easiest way to create a pipeline that copies data from a SQL Server database to any of the supported sink data stores is to use the Copy data wizard. See [Tutorial: Create a pipeline using Copy Wizard](data-factory-copy-data-wizard-tutorial.md) for a quick walkthrough on creating a pipeline using the Copy data wizard. 

The following example provides sample JSON definitions that you can use to create a pipeline by using [Azure portal](data-factory-copy-activity-tutorial-using-azure-portal.md) or [Visual Studio](data-factory-copy-activity-tutorial-using-visual-studio.md) or [Azure PowerShell](data-factory-copy-activity-tutorial-using-powershell.md). The following samples show how to copy data to and from SQL Server and Azure Blob Storage. However, data can be copied **directly** from any of sources to any of the sinks stated [here](data-factory-data-movement-activities.md#supported-data-stores) using the Copy Activity in Azure Data Factory.     

## Sample: Copy data from SQL Server to Azure Blob
The following sample shows:

1. A linked service of type [OnPremisesSqlServer](data-factory-sqlserver-connector.md#sql-server-linked-service-properties).
2. A linked service of type [AzureStorage](data-factory-azure-blob-connector.md#azure-storage-linked-service-properties).
3. An input [dataset](data-factory-create-datasets.md) of type [SqlServerTable](data-factory-sqlserver-connector.md#sql-server-dataset-type-properties).
4. An output [dataset](data-factory-create-datasets.md) of type [AzureBlob](data-factory-azure-blob-connector.md#azure-blob-dataset-type-properties).
5. The [pipeline](data-factory-create-pipelines.md) with Copy activity that uses [SqlSource](data-factory-sqlserver-connector.md#sql-server-copy-activity-type-properties) and [BlobSink](data-factory-azure-blob-connector.md#azure-blob-copy-activity-type-properties).

The sample copies time-series data from a SQL Server table to an Azure blob every hour. The JSON properties used in these samples are described in sections following the samples.

As a first step, setup the data management gateway. The instructions are in the [moving data between on-premises locations and cloud](data-factory-move-data-between-onprem-and-cloud.md) article.

**SQL Server linked service**

    {
      "Name": "SqlServerLinkedService",
      "properties": {
        "type": "OnPremisesSqlServer",
        "typeProperties": {
          "connectionString": "Data Source=<servername>;Initial Catalog=<databasename>;Integrated Security=False;User ID=<username>;Password=<password>;",
          "gatewayName": "<gatewayname>"
        }
      }
    }

**Azure Blob storage linked service**

    {
      "name": "StorageLinkedService",
      "properties": {
        "type": "AzureStorage",
        "typeProperties": {
          "connectionString": "DefaultEndpointsProtocol=https;AccountName=<accountname>;AccountKey=<accountkey>"
        }
      }
    }

**SQL Server input dataset**

The sample assumes you have created a table “MyTable” in SQL Server and it contains a column called “timestampcolumn” for time series data. You can query over multiple tables within the same database using a single dataset, but a single table must be used for the dataset's tableName typeProperty.

Setting “external”: ”true” informs Data Factory service that the dataset is external to the data factory and is not produced by an activity in the data factory.

    {
      "name": "SqlServerInput",
      "properties": {
        "type": "SqlServerTable",
        "linkedServiceName": "SqlServerLinkedService",
        "typeProperties": {
          "tableName": "MyTable"
        },
        "external": true,
        "availability": {
          "frequency": "Hour",
          "interval": 1
        },
        "policy": {
          "externalData": {
            "retryInterval": "00:01:00",
            "retryTimeout": "00:10:00",
            "maximumRetry": 3
          }
        }
      }
    }

**Azure Blob output dataset**

Data is written to a new blob every hour (frequency: hour, interval: 1). The folder path for the blob is dynamically evaluated based on the start time of the slice that is being processed. The folder path uses year, month, day, and hours parts of the start time.

    {
      "name": "AzureBlobOutput",
      "properties": {
        "type": "AzureBlob",
        "linkedServiceName": "StorageLinkedService",
        "typeProperties": {
          "folderPath": "mycontainer/myfolder/yearno={Year}/monthno={Month}/dayno={Day}/hourno={Hour}",
          "partitionedBy": [
            {
              "name": "Year",
              "value": {
                "type": "DateTime",
                "date": "SliceStart",
                "format": "yyyy"
              }
            },
            {
              "name": "Month",
              "value": {
                "type": "DateTime",
                "date": "SliceStart",
                "format": "MM"
              }
            },
            {
              "name": "Day",
              "value": {
                "type": "DateTime",
                "date": "SliceStart",
                "format": "dd"
              }
            },
            {
              "name": "Hour",
              "value": {
                "type": "DateTime",
                "date": "SliceStart",
                "format": "HH"
              }
            }
          ],
          "format": {
            "type": "TextFormat",
            "columnDelimiter": "\t",
            "rowDelimiter": "\n"
          }
        },
        "availability": {
          "frequency": "Hour",
          "interval": 1
        }
      }
    }

**Pipeline with Copy activity**

The pipeline contains a Copy Activity that is configured to use these input and output datasets and is scheduled to run every hour. In the pipeline JSON definition, the **source** type is set to **SqlSource** and **sink** type is set to **BlobSink**. The SQL query specified for the **SqlReaderQuery** property selects the data in the past hour to copy.

    {  
        "name":"SamplePipeline",
        "properties":{  
        "start":"2014-06-01T18:00:00",
        "end":"2014-06-01T19:00:00",
        "description":"pipeline for copy activity",
        "activities":[  
          {
            "name": "SqlServertoBlob",
            "description": "copy activity",
            "type": "Copy",
            "inputs": [
              {
                "name": " SqlServerInput"
              }
            ],
            "outputs": [
              {
                "name": "AzureBlobOutput"
              }
            ],
            "typeProperties": {
              "source": {
                "type": "SqlSource",
                "SqlReaderQuery": "$$Text.Format('select * from MyTable where timestampcolumn >= \\'{0:yyyy-MM-dd HH:mm}\\' AND timestampcolumn < \\'{1:yyyy-MM-dd HH:mm}\\'', WindowStart, WindowEnd)"
              },
              "sink": {
                "type": "BlobSink"
              }
            },
           "scheduler": {
              "frequency": "Hour",
              "interval": 1
            },
            "policy": {
              "concurrency": 1,
              "executionPriorityOrder": "OldestFirst",
              "retry": 0,
              "timeout": "01:00:00"
            }
          }
         ]
       }
    }


In this example, **sqlReaderQuery** is specified for the SqlSource. The Copy Activity runs this query against the SQL Server Database source to get the data. Alternatively, you can specify a stored procedure by specifying the **sqlReaderStoredProcedureName** and **storedProcedureParameters** (if the stored procedure takes parameters). The sqlReaderQuery can reference multiple tables within the database referenced by the input dataset. It is not limited to only the table set as the dataset's tableName typeProperty.

If you do not specify sqlReaderQuery or sqlReaderStoredProcedureName, the columns defined in the structure section are used to build a select query to run against the SQL Server Database. If the dataset definition does not have the structure, all columns are selected from the table.

See the [Sql Source](#sqlsource) section and [BlobSink](data-factory-azure-blob-connector.md#azure-blob-copy-activity-type-properties) for the list of properties supported by SqlSource and BlobSink.

## Sample: Copy data from Azure Blob to SQL Server
The following sample shows:

1. The linked service of type [OnPremisesSqlServer](data-factory-sqlserver-connector.md#sql-server-linked-service-properties).
2. The linked service of type [AzureStorage](data-factory-azure-blob-connector.md#azure-storage-linked-service-properties).
3. An input [dataset](data-factory-create-datasets.md) of type [AzureBlob](data-factory-azure-blob-connector.md#azure-blob-dataset-type-properties).
4. An output [dataset](data-factory-create-datasets.md) of type [SqlServerTable](data-factory-sqlserver-connector.md#sql-server-dataset-type-properties).
5. The [pipeline](data-factory-create-pipelines.md) with Copy activity that uses [BlobSource](data-factory-azure-blob-connector.md#azure-blob-copy-activity-type-properties) and [SqlSink](data-factory-sqlserver-connector.md#sql-server-copy-activity-type-properties).

The sample copies time-series data from an Azure blob to a SQL Server table every hour. The JSON properties used in these samples are described in sections following the samples.

**SQL Server linked service**

    {
      "Name": "SqlServerLinkedService",
      "properties": {
        "type": "OnPremisesSqlServer",
        "typeProperties": {
          "connectionString": "Data Source=<servername>;Initial Catalog=<databasename>;Integrated Security=False;User ID=<username>;Password=<password>;",
          "gatewayName": "<gatewayname>"
        }
      }
    }

**Azure Blob storage linked service**

    {
      "name": "StorageLinkedService",
      "properties": {
        "type": "AzureStorage",
        "typeProperties": {
          "connectionString": "DefaultEndpointsProtocol=https;AccountName=<accountname>;AccountKey=<accountkey>"
        }
      }
    }

**Azure Blob input dataset**

Data is picked up from a new blob every hour (frequency: hour, interval: 1). The folder path and file name for the blob are dynamically evaluated based on the start time of the slice that is being processed. The folder path uses year, month, and day part of the start time and file name uses the hour part of the start time. “external”: “true” setting informs the Data Factory service that the dataset is external to the data factory and is not produced by an activity in the data factory.

    {
      "name": "AzureBlobInput",
      "properties": {
        "type": "AzureBlob",
        "linkedServiceName": "StorageLinkedService",
        "typeProperties": {
          "folderPath": "mycontainer/myfolder/yearno={Year}/monthno={Month}/dayno={Day}",
          "fileName": "{Hour}.csv",
          "partitionedBy": [
            {
              "name": "Year",
              "value": {
                "type": "DateTime",
                "date": "SliceStart",
                "format": "yyyy"
              }
            },
            {
              "name": "Month",
              "value": {
                "type": "DateTime",
                "date": "SliceStart",
                "format": "MM"
              }
            },
            {
              "name": "Day",
              "value": {
                "type": "DateTime",
                "date": "SliceStart",
                "format": "dd"
              }
            },
            {
              "name": "Hour",
              "value": {
                "type": "DateTime",
                "date": "SliceStart",
                "format": "HH"
              }
            }
          ],
          "format": {
            "type": "TextFormat",
            "columnDelimiter": ",",
            "rowDelimiter": "\n"
          }
        },
        "external": true,
        "availability": {
          "frequency": "Hour",
          "interval": 1
        },
        "policy": {
          "externalData": {
            "retryInterval": "00:01:00",
            "retryTimeout": "00:10:00",
            "maximumRetry": 3
          }
        }
      }
    }

**SQL Server output dataset**

The sample copies data to a table named “MyTable” in SQL Server. Create the table in SQL Server with the same number of columns as you expect the Blob CSV file to contain. New rows are added to the table every hour.

    {
      "name": "SqlServerOutput",
      "properties": {
        "type": "SqlServerTable",
        "linkedServiceName": "SqlServerLinkedService",
        "typeProperties": {
          "tableName": "MyOutputTable"
        },
        "availability": {
          "frequency": "Hour",
          "interval": 1
        }
      }
    }

**Pipeline with Copy activity**

The pipeline contains a Copy Activity that is configured to use these input and output datasets and is scheduled to run every hour. In the pipeline JSON definition, the **source** type is set to **BlobSource** and **sink** type is set to **SqlSink**.

    {  
        "name":"SamplePipeline",
        "properties":{  
        "start":"2014-06-01T18:00:00",
        "end":"2014-06-01T19:00:00",
        "description":"pipeline with copy activity",
        "activities":[  
          {
            "name": "AzureBlobtoSQL",
            "description": "Copy Activity",
            "type": "Copy",
            "inputs": [
              {
                "name": "AzureBlobInput"
              }
            ],
            "outputs": [
              {
                "name": " SqlServerOutput "
              }
            ],
            "typeProperties": {
              "source": {
                "type": "BlobSource",
                "blobColumnSeparators": ","
              },
              "sink": {
                "type": "SqlSink"
              }
            },
           "scheduler": {
              "frequency": "Hour",
              "interval": 1
            },
            "policy": {
              "concurrency": 1,
              "executionPriorityOrder": "OldestFirst",
              "retry": 0,
              "timeout": "01:00:00"
            }
          }
          ]
       }
    }

## SQL Server linked service properties
The following table provides description for JSON elements specific to SQL Server linked service.

| Property | Description | Required |
| --- | --- | --- |
| type |The type property should be set to: **OnPremisesSqlServer**. |Yes |
| connectionString |Specify connectionString information needed to connect to the on-premises SQL Server database using either SQL authentication or Windows authentication. |Yes |
| gatewayName |Name of the gateway that the Data Factory service should use to connect to the on-premises SQL Server database. |Yes |
| username |Specify user name if you are using Windows Authentication. Example: **domainname\\username**. |No |
| password |Specify password for the user account you specified for the username. |No |

You can encrypt credentials using the **New-AzureRmDataFactoryEncryptValue** cmdlet and use them in the connection string as shown in the following example (**EncryptedCredential** property):  

    "connectionString": "Data Source=<servername>;Initial Catalog=<databasename>;Integrated Security=True;EncryptedCredential=<encrypted credential>",

### Samples
**JSON for using SQL Authentication**

    {
        "name": "MyOnPremisesSQLDB",
        "properties":
        {
            "type": "OnPremisesSqlLinkedService",
            "typeProperties": {
                "connectionString": "Data Source=<servername>;Initial Catalog=MarketingCampaigns;Integrated Security=False;User ID=<username>;Password=<password>;",
                "gatewayName": "<gateway name>"
            }
        }
    }

**JSON for using Windows Authentication**

If username and password are specified, gateway uses them to impersonate the specified user account to connect to the on-premises SQL Server database. Otherwise, gateway connects to the SQL Server directly with the security context of Gateway (its startup account).

    {
         "Name": " MyOnPremisesSQLDB",
         "Properties":
         {
             "type": "OnPremisesSqlLinkedService",
             "typeProperties": {
                 "ConnectionString": "Data Source=<servername>;Initial Catalog=MarketingCampaigns;Integrated Security=True;",
                 "username": "<domain\\username>",
                 "password": "<password>",
                 "gatewayName": "<gateway name>"
            }
         }
    }

See [Setting Credentials and Security](data-factory-move-data-between-onprem-and-cloud.md#set-credentials-and-security) for details about setting credentials for an SQL Server data source.

## SQL Server dataset type properties
For a full list of sections & properties available for defining datasets, see the [Creating datasets](data-factory-create-datasets.md) article. Sections such as structure, availability, and policy of a dataset JSON are similar for all dataset types (SQL Server, Azure blob, Azure table, etc.).

The typeProperties section is different for each type of dataset and provides information about the location of the data in the data store. The **typeProperties** section for the dataset of type **SqlServerTable** has the following properties.

| Property | Description | Required |
| --- | --- | --- |
| tableName |Name of the table in the SQL Server Database instance that linked service refers to. |Yes |

## SQL Server copy activity type properties
For a full list of sections & properties available for defining activities, see the [Creating Pipelines](data-factory-create-pipelines.md) article. Properties such as name, description, input and output tables, and policies are available for all types of activities.

> [!NOTE]
> The Copy Activity takes only one input and produces only one output.
> 
> 

Properties available in the typeProperties section of the activity on the other hand vary with each activity type. For Copy activity, they vary depending on the types of sources and sinks.

### SqlSource
When source in a copy activity is of type **SqlSource**, the following properties are available in **typeProperties** section:

| Property | Description | Allowed values | Required |
| --- | --- | --- | --- |
| sqlReaderQuery |Use the custom query to read data. |SQL query string. For example: select * from MyTable. May reference multiple tables from the database referenced by the input dataset. If not specified, the SQL statement that is executed: select from MyTable. |No |
| sqlReaderStoredProcedureName |Name of the stored procedure that reads data from the source table. |Name of the stored procedure. |No |
| storedProcedureParameters |Parameters for the stored procedure. |Name/value pairs. Names and casing of parameters must match the names and casing of the stored procedure parameters. |No |

If the **sqlReaderQuery** is specified for the SqlSource, the Copy Activity runs this query against the SQL Server Database source to get the data.

Alternatively, you can specify a stored procedure by specifying the **sqlReaderStoredProcedureName** and **storedProcedureParameters** (if the stored procedure takes parameters).

If you do not specify either sqlReaderQuery or sqlReaderStoredProcedureName, the columns defined in the structure section are used to build a select query to run against the SQL Server Database. If the dataset definition does not have the structure, all columns are selected from the table.

> [!NOTE]
> When you use **sqlReaderStoredProcedureName**, you still need to specify a value for the **tableName** property in the dataset JSON. There are no validations performed against this table though.
> 
> 

### SqlSink
**SqlSink** supports the following properties:

| Property | Description | Allowed values | Required |
| --- | --- | --- | --- |
| writeBatchTimeout |Wait time for the batch insert operation to complete before it times out. |timespan<br/><br/> Example: “00:30:00” (30 minutes). |No |
| writeBatchSize |Inserts data into the SQL table when the buffer size reaches writeBatchSize. |Integer (number of rows) |No (default: 10000) |
| sqlWriterCleanupScript |Specify query for Copy Activity to execute such that data of a specific slice is cleaned up. See repeatability section for more details. |A query statement. |No |
| sliceIdentifierColumnName |Specify column name for Copy Activity to fill with auto generated slice identifier, which is used to clean up data of a specific slice when rerun. See repeatability section for more details. |Column name of a column with data type of binary(32). |No |
| sqlWriterStoredProcedureName |Name of the stored procedure that upserts (updates/inserts) data into the target table. |Name of the stored procedure. |No |
| storedProcedureParameters |Parameters for the stored procedure. |Name/value pairs. Names and casing of parameters must match the names and casing of the stored procedure parameters. |No |
| sqlWriterTableType |Specify table type name to be used in the stored procedure. Copy activity makes the data being moved available in a temp table with this table type. Stored procedure code can then merge the data being copied with existing data. |A table type name. |No |

## Troubleshooting connection issues
1. Configure your SQL Server to accept remote connections. Launch **SQL Server Management Studio**, right-click **server**, and click **Properties**. Select **Connections** from the list and check **Allow remote connections to the server**.
   
    ![Enable remote connections](.\\media\\data-factory-sqlserver-connector\\AllowRemoteConnections.png)
   
    See [Configure the remote access Server Configuration Option](https://msdn.microsoft.com/library/ms191464.aspx) for detailed steps.
2. Launch **SQL Server Configuration Manager**. Expand **SQL Server Network Configuration** for the instance you want, and select **Protocols for MSSQLSERVER**. You should see protocols in the right-pane. Enable TCP/IP by right-clicking **TCP/IP** and clicking **Enable**.
   
    ![Enable TCP/IP](.\\media\\data-factory-sqlserver-connector\\EnableTCPProptocol.png)
   
    See [Enable or Disable a Server Network Protocol](https://msdn.microsoft.com/library/ms191294.aspx) for details and alternate ways of enabling TCP/IP protocol.
3. In the same window, double-click **TCP/IP** to launch **TCP/IP Properties** window.
4. Switch to the **IP Addresses** tab. Scroll down to see **IPAll** section. Note down the **TCP Port **(default is **1433**).
5. Create a **rule for the Windows Firewall** on the machine to allow incoming traffic through this port.  
6. **Verify connection**: To connect to the SQL Server using fully qualified name, use SQL Server Management Studio from a different machine. For example: "<machine>.<domain>.corp.<company>.com,1433."
   
   > [!IMPORTANT]
   > See [Ports and Security Considerations](data-factory-move-data-between-onprem-and-cloud.md#port-and-security-considerations) for detailed information.
   > 
   > See [Troubleshoot gateway issues](data-factory-data-management-gateway.md#troubleshoot-gateway-issues) for tips on troubleshooting connection/gateway related issues. 
   > 
   > 

## Identity columns in the target database
This section provides an example that copies data from a source table with no identity column to a destination table with an identity column.

**Source table:**

    create table dbo.SourceTbl
    (
           name varchar(100),
           age int
    )

**Destination table:**

    create table dbo.TargetTbl
    (
           id int identity(1,1),
           name varchar(100),
           age int
    )


Notice that the target table has an identity column.

**Source dataset JSON definition**

    {
        "name": "SampleSource",
        "properties": {
            "published": false,
            "type": " SqlServerTable",
            "linkedServiceName": "TestIdentitySQL",
            "typeProperties": {
                "tableName": "SourceTbl"
            },
            "availability": {
                "frequency": "Hour",
                "interval": 1
            },
            "external": true,
            "policy": {}
        }
    }

**Destination dataset JSON definition**

    {
        "name": "SampleTarget",
        "properties": {
            "structure": [
                { "name": "name" },
                { "name": "age" }
            ],
            "published": false,
            "type": "AzureSqlTable",
            "linkedServiceName": "TestIdentitySQLSource",
            "typeProperties": {
                "tableName": "TargetTbl"
            },
            "availability": {
                "frequency": "Hour",
                "interval": 1
            },
            "external": false,
            "policy": {}
        }
    }


Notice that as your source and target table have different schema (target has an additional column with identity). In this scenario, you need to specify **structure** property in the target dataset definition, which doesn’t include the identity column.

[!INCLUDE [data-factory-type-repeatability-for-sql-sources](../../includes/data-factory-type-repeatability-for-sql-sources.md)]

[!INCLUDE [data-factory-sql-invoke-stored-procedure](../../includes/data-factory-sql-invoke-stored-procedure.md)]

[!INCLUDE [data-factory-structure-for-rectangualr-datasets](../../includes/data-factory-structure-for-rectangualr-datasets.md)]

### Type mapping for SQL server & Azure SQL
As mentioned in the [data movement activities](data-factory-data-movement-activities.md) article, the Copy activity performs automatic type conversions from source types to sink types with the following 2-step approach:

1. Convert from native source types to .NET type
2. Convert from .NET type to native sink type

When moving data to & from Azure SQL, SQL server, Sybase the following mappings are used from SQL type to .NET type and vice versa.

The mapping is same as the SQL Server Data Type Mapping for ADO.NET.

| SQL Server Database Engine type | .NET Framework type |
| --- | --- |
| bigint |Int64 |
| binary |Byte[] |
| bit |Boolean |
| char |String, Char[] |
| date |DateTime |
| Datetime |DateTime |
| datetime2 |DateTime |
| Datetimeoffset |DateTimeOffset |
| Decimal |Decimal |
| FILESTREAM attribute (varbinary(max)) |Byte[] |
| Float |Double |
| image |Byte[] |
| int |Int32 |
| money |Decimal |
| nchar |String, Char[] |
| ntext |String, Char[] |
| numeric |Decimal |
| nvarchar |String, Char[] |
| real |Single |
| rowversion |Byte[] |
| smalldatetime |DateTime |
| smallint |Int16 |
| smallmoney |Decimal |
| sql_variant |Object * |
| text |String, Char[] |
| time |TimeSpan |
| timestamp |Byte[] |
| tinyint |Byte |
| uniqueidentifier |Guid |
| varbinary |Byte[] |
| varchar |String, Char[] |
| xml |Xml |

[!INCLUDE [data-factory-type-conversion-sample](../../includes/data-factory-type-conversion-sample.md)]

[!INCLUDE [data-factory-column-mapping](../../includes/data-factory-column-mapping.md)]

## Performance and Tuning
See [Copy Activity Performance & Tuning Guide](data-factory-copy-activity-performance.md) to learn about key factors that impact performance of data movement (Copy Activity) in Azure Data Factory and various ways to optimize it.

