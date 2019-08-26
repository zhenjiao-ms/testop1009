---
title: Use Case - Customer Profiling
description: Learn how Azure Data Factory is used to create a data-driven workflow (pipeline) to profile gaming customers.
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
ms.date: 09/06/2016
ms.author: spelluru

---
# Use Case - Customer Profiling
Azure Data Factory is one of many services used to implement the Cortana Intelligence Suite of solution accelerators.  For more information about Cortana Intelligence, visit [Cortana Intelligence Suite](http://www.microsoft.com/cortanaanalytics). In this document, we describe a simple use case to help you get started with understanding how Azure Data Factory can solve common analytics problems.

All you need to access and try out this simple use case is an [Azure subscription](https://azure.microsoft.com/pricing/free-trial/).  You can deploy a sample that implements this use case by following the steps described in the [Samples](data-factory-samples.md) article.

## Scenario
Contoso is a gaming company that creates games for multiple platforms: game consoles, hand held devices, and personal computers (PCs). As players play these games, large volume of log data is produced that tracks the usage patterns, gaming style, and preferences of the user.  When combined with demographic, regional, and product data, Contoso can perform analytics to guide them about how to enhance players’ experience and target them for upgrades and in-game purchases. 

Contoso’s goal is to identify up-sell/cross-sell opportunities based on the gaming history of its players and add compelling features to drive business growth and provide a better experience to customers. For this use case, we use a gaming company as an example of a business. The company wants to optimize its games based on players’ behavior. These principles apply to any business that wants to engage its customers around its goods and services and enhance their customers’ experience.

## Challenges
## Solution Overview
This simple use case can be used as an example of how you can use Azure Data Factory to ingest, prepare, transform, analyze, and publish data.

![End-to-end workflow](./media/data-factory-customer-profiling-usecase/EndToEndWorkflow.png)

This Figure depicts how the data pipelines appear in the Azure portal after they have been deployed.

1. The **PartitionGameLogsPipeline** reads the raw game events from blob storage and creates partitions based on year, month, and day.
2. The **EnrichGameLogsPipeline** joins partitioned game events with geo code reference data and enriches the data by mapping IP addresses to the corresponding geo-locations.
3. The **AnalyzeMarketingCampaignPipeline** pipeline uses the enriched data and processes it with the advertising data to create the final output that contains marketing campaign effectiveness.

In this example, Data Factory is used to orchestrate activities that copy input data, transform, and process the data, and output the final data to an Azure SQL Database.  You can also visualize the network of data pipelines, manage them, and monitor their status from the UI.

## Benefits
By optimizing their user profile analytics and aligning it with business goals, gaming company is able to quickly collect usage patterns, and analyze the effectiveness of its marketing campaigns.

