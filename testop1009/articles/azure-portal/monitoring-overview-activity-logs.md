---
title: Overview of the Azure Activity Log | Microsoft Azure
description: Learn what the Azure Activity Log is and how you can use it to understand events occurring within your Azure subscription.
author: johnkemnetz
manager: rboucher
editor: ''
services: monitoring-and-diagnostics
documentationcenter: monitoring-and-diagnostics

ms.service: monitoring-and-diagnostics
ms.workload: na
ms.tgt_pltfrm: na
ms.devlang: na
ms.topic: article
ms.date: 08/17/2016
ms.author: johnkem

---
# Overview of the Azure Activity Log
The **Azure Activity Log** is a log that provides insight into the operations that were performed on resources in your subscription. The Activity Log was previously known as “Audit Logs” or “Operational Logs,” since it reports control-plane events for your subscriptions. Using the Activity Log, you can determine the ‘what, who, and when’ for any write (PUT, POST, DELETE) operations taken on the resources in your subscription, plus understand the status of the operation and other relevant properties. The Activity Log does not include read (GET) operations.

The Activity Log differs from [Diagnostic Logs](monitoring-overview-of-diagnostic-logs.md), which are all logs emitted by a resource. These logs provide data about the operation of that resource, rather than operations on that resource. 

You can retrieve events from your Activity Log using the Azure portal, CLI, PowerShell cmdlets, and Insights REST API.

## What you can do with the Activity Log
Here are some of the things you can do with the Activity Log:

* Query and view it in the **Azure portal**.
* Query it via REST API, PowerShell Cmdlet, or CLI.
* [Create an email or webhook alert that triggers off an Activity Log event.](insights-auditlog-to-webhook-email.md)
* [Save it to a **Storage Account** for archival or manual inspection](monitoring-archive-activity-log.md). You can specify the retention time (in days) using **Log Profiles**.
* Analyze it in PowerBI using the [**PowerBI content pack**](https://powerbi.microsoft.com/en-us/documentation/powerbi-content-pack-azure-audit-logs/).
* [Stream it to an **Event Hub**](monitoring-stream-activity-logs-event-hubs.md) for ingestion by a third party service or custom analytics solution such as PowerBI.

## Export the Activity Log with Log Profiles
A **Log Profile** controls how your Activity Log is exported. Using a Log Profile, you can configure:

* Where the Activity Log should be sent (Storage Account or Event Hubs)
* Which event categories (eg. Write, Delete, Action) should be sent
* Which regions (locations) should be exported
* How long the Activity Log should be retained in a Storage Account – a retention of zero days means logs are kept forever. Otherwise, the value can be any number of days between 1 and 2147483647. If retention policies are set but storing logs in a Storage Account is disabled (eg. if only Event Hubs or OMS options are selected), the retention policies have no effect.

These settings can be configured via the “Export” option in the Activity Log blade in the portal, or programmatically [using the REST API](https://msdn.microsoft.com/library/azure/dn931927.aspx), PowerShell cmdlets, or CLI. A subscription can only have one log profile.

### Configure log profiles using the Azure portal
You can stream the Activity Log to an Event Hub or store them in a Storage Account by using the “Export” option in the Azure portal.

1. Navigate to the **Activity Log** blade using the menu on the left side of the portal.
   
    ![Navigate to Activity Log in portal](./media/monitoring-overview-activity-logs/activity-logs-portal-navigate.png)
2. Click the **Export** button at the top of the blade.
   
    ![Export button in portal](./media/monitoring-overview-activity-logs/activity-logs-portal-export.png)
3. In the blade that appears, you can select the regions for which you would like to export events, the Storage Account to which you would like to save events (as well as the number of days you want to retain these events in storage--0 days will retain the logs forever), and the Service Bus Namespace in which you would like an Event Hub to be created for streaming these events.
   
    ![Export Activity Log blade](./media/monitoring-overview-activity-logs/activity-logs-portal-export-blade.png)
4. Click **Save** to save these settings. The settings are immediately be applied to your subscription.

### Configure log profiles using the Azure PowerShell Cmdlets
#### Get existing log profile
```
Get-AzureRmLogProfile
```

#### Add a log profile
```
Add-AzureRmLogProfile -Name my_log_profile -StorageAccountId /subscriptions/s1/resourceGroups/myrg1/providers/Microsoft.Storage/storageAccounts/my_storage -serviceBusRuleId /subscriptions/s1/resourceGroups/Default-ServiceBus-EastUS/providers/Microsoft.ServiceBus/namespaces/mytestSB/authorizationrules/RootManageSharedAccessKey -Locations global,westus,eastus -RetentionInDays 90 -Categories Write,Delete,Action
```

| Property | Required | Description |
| --- | --- | --- |
| Name |Yes |Name of your log profile. |
| StorageAccountId |No |Resource ID of the Storage Account to which the Activity Log should be saved. |
| serviceBusRuleId |No |Service Bus Rule ID for the Service Bus namespace you would like to have event hubs created in. Will be a string with this format: `{service bus resource ID}/authorizationrules/{key name}`. |
| Locations |Yes |Comma-separated list of regions for which you would like to collect Activity Log events. |
| RetentionInDays |Yes |Number of days for which events should be retained, between 1 and 2147483647. A value of zero will store the logs indefinitely (forever). |
| Categories |No |Comma-separated list of event categories that should be collected. Possible values are Write, Delete, and Action. |

#### Remove a log profile
```
Remove-AzureRmLogProfile -name my_log_profile
```

### Configure log profiles Using the Azure Cross-Platform CLI
#### Get existing log profile
```
azure insights logprofile list
```
```
azure insights logprofile get --name my_log_profile
```
The `name` property should be the name of your log profile.

#### Add a log profile
``` 
azure insights logprofile add --name my_log_profile --storageId /subscriptions/s1/resourceGroups/insights-integration/providers/Microsoft.Storage/storageAccounts/my_storage --serviceBusRuleId /subscriptions/s1/resourceGroups/Default-ServiceBus-EastUS/providers/Microsoft.ServiceBus/namespaces/mytestSB/authorizationrules/RootManageSharedAccessKey --locations global,westus,eastus,northeurope --retentionInDays 90 –categories Write,Delete,Action
```

| Property | Required | Description |
| --- | --- | --- |
| name |Yes |Name of your log profile. |
| storageId |No |Resource ID of the Storage Account to which the Activity Log should be saved. |
| serviceBusRuleId |No |Service Bus Rule ID for the Service Bus namespace you would like to have event hubs created in. Will be a string with this format: `{service bus resource ID}/authorizationrules/{key name}`. |
| locations |Yes |Comma-separated list of regions for which you would like to collect Activity Log events. |
| retentionInDays |Yes |Number of days for which events should be retained, between 1 and 2147483647. A value of zero stores the logs indefinitely (forever). |
| categories |No |Comma-separated list of event categories that should be collected. Possible values are Write, Delete, and Action. |

#### Remove a log profile
```
azure insights logprofile delete --name my_log_profile
```

## Event schema
Each event in the Activity Log has a JSON blob like this one:

```
{
  "value": [ {
    "authorization": {
      "action": "microsoft.support/supporttickets/write",
      "role": "Subscription Admin",
      "scope": "/subscriptions/s1/resourceGroups/MSSupportGroup/providers/microsoft.support/supporttickets/115012112305841"
    },
    "caller": "admin@contoso.com",
    "channels": "Operation",
    "claims": {
      "aud": "https://management.core.windows.net/",
      "iss": "https://sts.windows.net/72f988bf-86f1-41af-91ab-2d7cd011db47/",
      "iat": "1421876371",
      "nbf": "1421876371",
      "exp": "1421880271",
      "ver": "1.0",
      "http://schemas.microsoft.com/identity/claims/tenantid": "1e8d8218-c5e7-4578-9acc-9abbd5d23315 ",
      "http://schemas.microsoft.com/claims/authnmethodsreferences": "pwd",
      "http://schemas.microsoft.com/identity/claims/objectidentifier": "2468adf0-8211-44e3-95xq-85137af64708",
      "http://schemas.xmlsoap.org/ws/2005/05/identity/claims/upn": "admin@contoso.com",
      "puid": "20030000801A118C",
      "http://schemas.xmlsoap.org/ws/2005/05/identity/claims/nameidentifier": "9vckmEGF7zDKk1YzIY8k0t1_EAPaXoeHyPRn6f413zM",
      "http://schemas.xmlsoap.org/ws/2005/05/identity/claims/givenname": "John",
      "http://schemas.xmlsoap.org/ws/2005/05/identity/claims/surname": "Smith",
      "name": "John Smith",
      "groups": "cacfe77c-e058-4712-83qw-f9b08849fd60,7f71d11d-4c41-4b23-99d2-d32ce7aa621c,31522864-0578-4ea0-9gdc-e66cc564d18c",
      "http://schemas.xmlsoap.org/ws/2005/05/identity/claims/name": " admin@contoso.com",
      "appid": "c44b4083-3bq0-49c1-b47d-974e53cbdf3c",
      "appidacr": "2",
      "http://schemas.microsoft.com/identity/claims/scope": "user_impersonation",
      "http://schemas.microsoft.com/claims/authnclassreference": "1"
    },
    "correlationId": "1e121103-0ba6-4300-ac9d-952bb5d0c80f",
    "description": "",
    "eventDataId": "44ade6b4-3813-45e6-ae27-7420a95fa2f8",
    "eventName": {
      "value": "EndRequest",
      "localizedValue": "End request"
    },
    "eventSource": {
      "value": "Microsoft.Resources",
      "localizedValue": "Microsoft Resources"
    },
    "httpRequest": {
      "clientRequestId": "27003b25-91d3-418f-8eb1-29e537dcb249",
      "clientIpAddress": "192.168.35.115",
      "method": "PUT"
    },
    "id": "/subscriptions/s1/resourceGroups/MSSupportGroup/providers/microsoft.support/supporttickets/115012112305841/events/44ade6b4-3813-45e6-ae27-7420a95fa2f8/ticks/635574752669792776",
    "level": "Informational",
    "resourceGroupName": "MSSupportGroup",
    "resourceProviderName": {
      "value": "microsoft.support",
      "localizedValue": "microsoft.support"
    },
    "resourceUri": "/subscriptions/s1/resourceGroups/MSSupportGroup/providers/microsoft.support/supporttickets/115012112305841",
    "operationId": "1e121103-0ba6-4300-ac9d-952bb5d0c80f",
    "operationName": {
      "value": "microsoft.support/supporttickets/write",
      "localizedValue": "microsoft.support/supporttickets/write"
    },
    "properties": {
      "statusCode": "Created"
    },
    "status": {
      "value": "Succeeded",
      "localizedValue": "Succeeded"
    },
    "subStatus": {
      "value": "Created",
      "localizedValue": "Created (HTTP Status Code: 201)"
    },
    "eventTimestamp": "2015-01-21T22:14:26.9792776Z",
    "submissionTimestamp": "2015-01-21T22:14:39.9936304Z",
    "subscriptionId": "s1"
  } ],
"nextLink": "https://management.azure.com/########-####-####-####-############$skiptoken=######"
}
```

| Element Name | Description |
| --- | --- |
| authorization |Blob of RBAC properties of the event. Usually includes the “action”, “role” and “scope” properties. |
| caller |Email address of the user who has performed the operation, UPN claim, or SPN claim based on availability. |
| channels |One of the following values: “Admin”, “Operation” |
| correlationId |Usually a GUID in the string format. Events that share a correlationId belong to the same uber action. |
| description |Static text description of an event. |
| eventDataId |Unique identifier of an event. |
| eventSource |Name of the Azure service or infrastructure that has generated this event. |
| httpRequest |Blob describing the Http Request. Usually includes the “clientRequestId”, “clientIpAddress” and “method” (HTTP method e.g. PUT). |
| level |Level of the event. One of the following values: “Critical”, “Error”, “Warning”, “Informational” and “Verbose” |
| resourceGroupName |Name of the resource group for the impacted resource. |
| resourceProviderName |Name of the resource provider for the impacted resource |
| resourceUri |Resource id of the impacted resource. |
| operationId |A GUID shared among the events that correspond to a single operation. |
| operationName |Name of the operation. |
| properties |Set of `<Key, Value>` pairs (i.e. Dictionary) describing the details of the event. |
| status |String describing the status of the operation. Some common values are: Started, In Progress, Succeeded, Failed, Active, Resolved. |
| subStatus |Usually the HTTP status code of the corresponding REST call, but can also include other strings describing a substatus, such as these common values: OK (HTTP Status Code: 200), Created (HTTP Status Code: 201), Accepted (HTTP Status Code: 202), No Content (HTTP Status Code: 204), Bad Request (HTTP Status Code: 400), Not Found (HTTP Status Code: 404), Conflict (HTTP Status Code: 409), Internal Server Error (HTTP Status Code: 500), Service Unavailable (HTTP Status Code: 503), Gateway Timeout (HTTP Status Code: 504). |
| eventTimestamp |Timestamp when the event was generated by the Azure service processing the request corresponding the event. |
| submissionTimestamp |Timestamp when the event became available for querying. |
| subscriptionId |Azure Subscription Id. |
| nextLink |Continuation token to fetch the next set of results when they are broken up into multiple responses. This is usually the case if there are more than 200 records. |

## Next Steps
* [Learn more about the Activity Log (formerly Audit Logs)](../resource-group-audit.md)
* [Stream the Azure Activity Log to Event Hubs](monitoring-stream-activity-logs-event-hubs.md)

