---
title: Exploring HockeyApp data in Application Insights | Microsoft Azure
description: Analyze usage and performance of your Azure app with Application Insights.
services: application-insights
documentationcenter: windows
author: alancameronwills
manager: douge

ms.service: application-insights
ms.workload: tbd
ms.tgt_pltfrm: ibiza
ms.devlang: na
ms.topic: article
ms.date: 08/25/2016
ms.author: awills

---
# Exploring HockeyApp data in Application Insights
[HockeyApp](https://azure.microsoft.com/services/hockeyapp/) is the recommended platform for monitoring live desktop and mobile apps. From HockeyApp, you can send custom and trace telemetry to monitor usage and assist in diagnosis (in addition to getting crash data). This stream of telemetry can be queried using the powerful [Analytics](app-insights-analytics.md) feature of [Visual Studio Application Insights](app-insights-overview.md). In addition, you can [export the custom and trace telemetry](app-insights-export-telemetry.md). To enable these features, you set up a bridge that relays the HockeyApp data to Application Insights.

## The HockeyApp Bridge app
The HockeyApp Bridge App is the core feature that enables you to access your HockeyApp data in Application Insights through the Analytics and Continuous Export features. Any data collected by HockeyApp after the creation of the HockeyApp Bridge App will be accessible from these features. Let’s see how to set up one of these Bridge Apps.

In HockeyApp, open Account Settings, [API Tokens](https://rink.hockeyapp.net/manage/auth_tokens). Either create a new token or reuse an existing one. The minimum rights required are "read only". Take a copy of the API token.

![Get a HockeyApp API token](./media/app-insights-hockeyapp-bridge-app/01.png)

Open the Microsoft Azure portal and [create an Application Insights resource](app-insights-create-new-resource.md). Set Application Type to “HockeyApp bridge application”:

![New Application Insights resource](./media/app-insights-hockeyapp-bridge-app/02.png)

You don't need to set a name - this will automatically be set from the HockeyApp name.

The HockeyApp bridge fields appear. 

![Enter bridge fields](./media/app-insights-hockeyapp-bridge-app/03.png)

Enter the HockeyApp token you noted earlier. This action populates the “HockeyApp Application” dropdown menu with all your HockeyApp applications. Select the one you want to use, and complete the remainder of the fields. 

Open the new resource. 

Note that the data takes a while to start flowing.

![Application Insights resource waiting for data](./media/app-insights-hockeyapp-bridge-app/04.png)

That’s it! Any data collected in your HockeyApp-instrumented app from this point forward is now also available to you in the Analytics and Continuous Export features of Application Insights.

Let’s briefly review each of these features now available to you.

## Analytics
Analytics is a powerful tool for ad-hoc querying of your data, allowing you to diagnose and analyze your telemetry and quickly discover root causes and patterns.

![Analytics](./media/app-insights-hockeyapp-bridge-app/05.png)

* [Learn more about Analytics](app-insights-analytics-tour.md)
* [Introduction video](https://channel9.msdn.com/events/Build/2016/T666)
* [Advanced concepts video](https://channel9.msdn.com/Events/Build/2016/P591)

## Continuous export
Continuous Export allows you to export your data into an Azure Blob Storage container. This is very useful if you need to keep your data for longer than the retention period currently offered by Application Insights. You can keep the data in blob storage, process it into a SQL Database, or your preferred data warehousing solution.

[Learn more about Continuous Export](app-insights-export-telemetry.md)

## Next steps
* [Apply Analytics to your data](app-insights-analytics-tour.md)

