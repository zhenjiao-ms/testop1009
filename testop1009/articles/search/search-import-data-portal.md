---
title: Import data to Azure Search using indexers in the Azure Portal | Microsoft Azure | Hosted cloud search service
description: Use the Azure Search Import Data Wizard in the Azure Portal to crawl data from Azure Blob storage, table stroage, SQL Database, and SQL Server on Azure VMs.
services: search
documentationcenter: ''
author: HeidiSteen
manager: paulettm
editor: ''
tags: Azure Portal

ms.service: search
ms.devlang: na
ms.workload: search
ms.topic: get-started-article
ms.tgt_pltfrm: na
ms.date: 08/29/2016
ms.author: heidist

---
# Import data to Azure Search using the portal
The Azure portal provides an **Import Data** wizard on the Azure Search dashboard for loading data into an index. 

  ![Import Data on the command bar][1]

Internally, the wizard configures and invokes an *indexer*, automating several steps of the indexing process: 

* Connect to an external data source in the current Azure subscription
* Autogenerate an index schema based on the source data structure
* Create documents based on a rowset retrieved from the data source
* Upload documents to the index in your search service

You can try out this workflow using sample data in DocumentDB. Visit [Get started with Azure Search in the Azure Portal](search-get-started-portal.md) for instructions.

## Data sources supported by the Import Data Wizard
Indexing automation and tooling is available for the following data sources: 

* Azure SQL Database
* SQL Server relational data on an Azure VM
* Azure DocumentDB
* Azure Blob storage (in preview)
* Azure Table storage (in preview)

A flattened dataset is a required input. You can only import from a single table, database view, or equivalent data structure. You should create this data structure before running the wizard.

Note that a few of the indexers are still in preview, which means the indexer definition is backed by the preview version of the API. See [Indexer overview](search-indexer-overview.md) for more information and links.

## Connect to your data
1. Sign in to the [Azure Portal](https://portal.azure.com) and open service dashboard. You can click **Search services** in the jump bar to show the existing services in the current subscription. 
2. Click **Import Data** on the command bar to slide open the Import Data blade.  
3. Click **Connect to your data** to specify a data source definition used by an indexer. For intra-subscription data sources, the wizard can usually detect and read connection information, minimizing overall configuration requirements.

|  |  |
| --- | --- |
| **Existing data source** |If you already have indexers defined in your search service, you can select an existing data source definition for another import. |
| **Azure SQL Database** |Service name, credentials for a database user with read permission, and a database name can be specified either on the page or via an ADO.NET connection string. Choose the connection string option to view or customize properties. <br/><br/>The table or view that provides the rowset must be specified on the page. This option appears after the connection succeeds, giving a drop-down list so that you can make a selection. |
| **SQL Server on Azure VM** |Specify a fully-qualified service name, user ID and password, and database as a connection string. To use this data source, you must have previously installed a certificate in the local store that encrypts the connection. <br/><br/>The table or view that provides the rowset must be specified on the page. This option appears after the connection succeeds, giving a drop-down list so that you can make a selection. |
| **DocumentDB** |Requirements include the account, database, and collection. All documents in the collection will be included in the index. You can define a query to flatten or filter the rowset, or to detect changed documents for subsequent data refresh operations. |
| **Azure Blob Storage** |Requirements include the storage account and a container. Optionally, if blob names follow a virtual naming convention for grouping purposes, you can specify the virtual directory portion of the name as a folder under container. See [Indexing Blob Storage (preview)](search-howto-indexing-azure-blob-storage.md) for more information. |
| **Azure Table Storage** |Requirements include the storage account and a table name. Optionally, you can specify a query to retrieve a subset of the tables. See [Indexing Table Storage (preview)](search-howto-indexing-azure-tables.md) for more information. |

## Customize target index
A preliminary index is typically inferred from the dataset. Add, edit, or delete fields to complete the schema. Additionally, set attributes at the field level to determine its subsequent search behaviors.

1. In **Customize target index**, specify the name and a **Key** used to uniquely identify each document. The Key must be a string. If field values include spaces or dashes be sure to set advanced options in **Import your data** to suppress the validation check for these characters.
2. Review and revise the remaining fields. Field name and type are typically filled in for you. You can change the data type.
3. Set index attributes for each field:
   
   * Retrievable returns the field in search results.
   * Filterable allows the field to be referenced in filter expressions.
   * Sortable allows the field to be used in a sort.
   * Facetable enables the field for faceted navigation.
   * Searchable enables full-text search.
4. Click the **Analyzer** tab if you want to specify a language analyzer at the field level. Only language analyzers can be specified at this time. Using a custom analyzer or a non-language analyzer like Keyword, Pattern, and so forth, will require code.
   
   * Click **Searchable** to designate full-text search on the field and enable the Analyzer drop-down list.
   * Choose the analyzer you want. See [Create an index for documents in multiple language](search-language-support.md) for details.
5. Click the **Suggester** to enable type-ahead query suggestions on selected fields.

## Import your data
1. In **Import your data**, provide a name for the indexer. Recall that the product of the Import Data wizard is an indexer. Later, if you want to view or edit it, you'll select it from the portal rather than by rerunning the wizard. 
2. Specify the schedule, which is based on the regional time zone in which the service is provisioned.
3. Set advanced options to specify thresholds on whether indexing can continue if a document is dropped. Additionally, you can specify whether **Key** fields are allowed to contain spaces and slashes.  

## Edit an existing indexer
In the service dashboard, double-click on the Indexer tile to slide out a list of all indexers created for your subscription. Double-click one of the indexers to run, edit or delete it. You can replace the index with another existing one, change the data source, and set options for error thresholds during indexing.

## Edit an existing index
In Azure Search, structural updates to an index will require a rebuild of that index, which consists of deleting the index, recreating the index, and reloading data. Structural updates include changing a data type and renaming or deleting a field.

Edits that don't require a rebuild include adding a new field, changing scoring profiles, changing suggesters, or changing language analyzers. See [Update Index](https://msdn.microsoft.com/library/azure/dn800964.aspx) for more information.

## Next step
Review these links to learn more about indexers:

* [Indexing Azure SQL Database](search-howto-connecting-azure-sql-database-to-azure-search-using-indexers-2015-02-28.md)
* [Indexing DocumentDB](../documentdb/documentdb-search-indexer.md)
* [Indexing Blob Storage (preview)](search-howto-indexing-azure-blob-storage.md)
* [Indexing Table Storage (preview)](search-howto-indexing-azure-tables.md)

<!--Image references-->
[1]: ./media/search-import-data-portal/search-import-data-command.png

