---
title: Automatically enable Diagnostic Settings using a Resource Manager template | Microsoft Azure
description: Learn how to use a Resource Manager template to create diagnostic settings that will enable you to stream your diagnostic logs to Event Hubs or store them in a storage account.
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
# Automatically enable Diagnostic Settings at resource creation using a Resource Manager template
In this article we show how you can use an [Azure Resource Manager template](../resource-group-authoring-templates.md) to configure Diagnostic Settings on a resource when it is created. This enables you to automatically start streaming your Diagnostic Logs and metrics to Event Hubs or archiving them in a Storage Account when a resource is created.

The method for enabling Diagnostic Logs using a Resource Manager template depends on the resource type.

* **Non-Compute** resources (for example, Network Security Groups, Logic Apps, Automation) use [Diagnostic Settings described in this article](monitoring-overview-of-diagnostic-logs.md#diagnostic-settings).
* **Compute** (WAD/LAD-based) resources use the [WAD/LAD configuration file described in this article](../vs-azure-tools-diagnostics-for-cloud-services-and-virtual-machines.md).

In this article we describe how to configure diagnostics using either method.

The basic steps are as follows:

1. Create a template as a JSON file that describes how to create the resource and enable diagnostics.
2. [Deploy the template using any deployment method](../resource-group-template-deploy.md).

Below we give an example of the template JSON file you need to generate for non-Compute and Compute resources.

## Non-Compute resource template
For non-Compute resources, you will need to do two things:

1. Add parameters to the parameters blob for the storage account name and service bus rule id (enabling archival of Diagnostic Logs in a storage account and/or streaming of logs to Event Hubs).
   
    ```
    "storageAccountName": {
      "type": "string",
      "metadata": {
        "description": "Name of the Storage Account in which Diagnostic Logs should be saved."
      }
    },
    "serviceBusRuleId": {
      "type": "string",
      "metadata": {
        "description": "Service Bus Rule Id for the Service Bus Namespace in which the Event Hub should be created or streamed to."
      }
    }
    ```
2. In the resources array of the resource for which you want to enable Diagnostic Logs, add a resource of type `[resource namespace]/providers/diagnosticSettings`.
   
    ```
    "resources": [
      {
        "type": "providers/diagnosticSettings",
        "name": "Microsoft.Insights/service",
        "dependsOn": [
          "[/*resource Id for which Diagnostic Logs will be enabled>*/]"
        ],
        "apiVersion": "2015-07-01",
        "properties": {
          "storageAccountId": "[resourceId('Microsoft.Storage/storageAccounts', parameters('storageAccountName'))]",
          "serviceBusRuleId": "[parameters('serviceBusRuleId')]",
          "logs": [ 
            {
              "category": "/* log category name */",
              "enabled": true,
              "retentionPolicy": {
                "days": 0,
                "enabled": false
              }
            }
          ]
        }
      }
    ]
    ```

The properties blob for the Diagnostic Setting follows [the format described in this article](https://msdn.microsoft.com/library/azure/dn931931.aspx).

Here is a full example that creates a Network Security Group and turns on streaming to Event Hubs and storage in a storage account.

```
{
    "$schema": "https://schema.management.azure.com/schemas/2015-01-01/deploymentTemplate.json#",
    "contentVersion": "1.0.0.0",
    "parameters": {
        "nsgName": {
            "type": "string",
            "metadata": {
                "description": "Name of the NSG that will be created."
            }
        },
        "storageAccountName": {
            "type": "string",
            "metadata": {
                "description":"Name of the Storage Account in which Diagnostic Logs should be saved."
            }
        },
        "serviceBusRuleId": {
            "type": "string",
            "metadata": {
                "description":"Service Bus Rule Id for the Service Bus Namespace in which the Event Hub should be created or streamed to."
            }
        }
    },
    "variables": {},
    "resources": [
        {
            "type": "Microsoft.Network/networkSecurityGroups",
            "name": "[parameters('nsgName')]",
            "apiVersion": "2016-03-30",
            "location": "westus",
            "properties": {
                "securityRules": []
            },
            "resources": [
                {
                    "type": "providers/diagnosticSettings",
                    "name": "Microsoft.Insights/service",
                    "dependsOn": [
                        "[resourceId('Microsoft.Network/networkSecurityGroups', parameters('nsgName'))]"
                    ],
                    "apiVersion": "2015-07-01",
                    "properties": {
                        "storageAccountId": "[resourceId('Microsoft.Storage/storageAccounts', parameters('storageAccountName'))]",
                        "serviceBusRuleId": "[parameters('serviceBusRuleId')]",
                        "logs": [
                            {
                                "category": "NetworkSecurityGroupEvent",
                                "enabled": true,
                                "retentionPolicy": {
                                    "days": 0,
                                    "enabled": false
                                }
                            },
                            {
                                "category": "NetworkSecurityGroupRuleCounter",
                                "enabled": true,
                                "retentionPolicy": {
                                    "days": 0,
                                    "enabled": false
                                }
                            }
                        ]
                    }
                }
            ],
            "dependsOn": []
        }
    ]
}
```

## Compute resource template
To enable diagnostics on a Compute resource, for example a Virtual Machine or Service Fabric cluster, you need to:

1. Add the Azure Diagnostics extension to the VM resource definition.
2. Specify a storage account and/or event hub as a parameter.
3. Add the contents of your WADCfg XML file into the XMLCfg property, escaping all XML characters properly.

> [!WARNING]
> This last step can be tricky to get right. [See this article](../virtual-machines/virtual-machines-windows-extensions-diagnostics-template.md#diagnostics-configuration-variables) for an example that splits the Diagnostics Configuration Schema into variables that are escaped and formatted correctly.
> 
> 

The entire process, including samples, is described [in this document](../virtual-machines/virtual-machines-windows-extensions-diagnostics-template.md).

## Next Steps
* [Read more about Azure Diagnostic Logs](monitoring-overview-of-diagnostic-logs.md)
* [Stream Azure Diagnostic Logs to Event Hubs](monitoring-stream-diagnostic-logs-to-event-hubs.md)

