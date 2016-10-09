---
title: Overview of autoscale in Microsoft Azure Virtual Machines, Cloud Services, and Web Apps | Microsoft Azure
description: Overview of autoscale in Microsoft Azure. Applies to Virtual Machines, Cloud Services and Web Apps.
author: rboucher
manager: ''
editor: ''
services: monitoring-and-diagnostics
documentationcenter: monitoring-and-diagnostics

ms.service: monitoring-and-diagnostics
ms.workload: na
ms.tgt_pltfrm: na
ms.devlang: na
ms.topic: article
ms.date: 09/06/2016
ms.author: robb

---
# Overview of autoscale in Microsoft Azure Virtual Machines, Cloud Services, and Web Apps
This article describes what Microsoft Azure autoscale is, its benefits, and how to get started using it.  

Azure Insights autoscale applies only to [Virtual Machine Scale Sets](https://azure.microsoft.com/services/virtual-machine-scale-sets/), [Cloud Services](https://azure.microsoft.com/services/cloud-services/), and [App Service - Web Apps](https://azure.microsoft.com/services/app-service/web/). 

> [!NOTE]
> Azure has two autoscale methods. An older version of autoscale applies to Virtual Machines (availability sets). This feature has limited support and we recommend migrating to VM Scale Sets for faster and more reliable autoscale support. A link on how to use the older technology is included in this article.  
> 
> 

## What is autoscale?
Autoscale allows you to have the right amount of resources running to handle the load on your application. It allows you to add resources to handle increases in load and also save money by removing resources which are sitting idle. You specify a minimum and maximum number of instances to run and add or remove VMs automatically based on a set of rules. Having a minimum makes sure your application is always running even under no load. Having a maximum limits your total possible hourly cost. You automatically scale between these two extremes using rules you create. 

 ![Autoscale explained. Add and remove VMs](./media/monitoring-autoscale-overview/AutoscaleConcept.png)

When rule conditions are met, one or more autoscale actions is triggered. You can add and remove VMs, or perform other actions. The following conceptual diagram shows this process.  

 ![Conceptual Autoscale Flow Diagram](./media/monitoring-autoscale-overview/AutoscaleOverview3.png)

## Autoscale Process Explained
The following explanation apply to the pieces of the previous diagram.   

### Resource metrics
Resources emit metrics, which are later processed by rules. Metrics come via different methods.
VM Scale Sets uses telemetry data from Azure diagnostics agents whereas telemetry for Web apps and Cloud services comes directly from the Azure Infrastructure. Some commonly used statistics include CPU Usage, memory usage, thread counts, queue length, and disk usage. For a list of what telemetry data you can use, see [Autoscale Common Metrics](insights-autoscale-common-metrics.md). 

### Time
Schedule-based rules are based on UTC. You must set your time zone properly when setting up your rules.  

### Rules
The diagram shows only one autoscale rule, but you can have many of them. You can create complex overlapping rules as needed for your situation.  Rule types include  

* **Metric-based** - For example, do this action when CPU usage is above 50%. 
* **Time-based** - For example, trigger a webhook every 8am on Saturday in a given time zone.

Metric-based rules measure application load and add or remove VMs based on that load. Schedule-based rules allow you to scale when you see time patterns in your load and want to scale before a possible load increase or decrease occurs.  

### Actions and automation
Rules can trigger one or more types of actions.

* **Scale** - Scale VMs in or out
* **Email** - Send email to subscription admins, co-admins, and/or additional email address you specify
* **Automate via webhooks** - Call webhooks, which can trigger multiple complex actions inside or outside Azure. Inside Azure, you can start an Azure Automation runbook, Azure Function, or Azure Logic App. Example 3rd party URL outside Azure include services like Slack and Twilio. 

## Autoscale Settings
Autoscale use the following terminology and structure. 

* An **autoscale setting** is read by the autoscale engine to determine whether to scale up or down. It contains one or more profiles, information about the target resource, and notification settings.
  * An **autoscale profile** is a combination of a capacity setting, a set of rules governing the triggers, and scale actions for the profile, and a recurrence. You can have multiple profiles, which allow you to take care of different overlapping requirements. 
    * A **capacity setting** indicates the minimum, maximum, and default values for number of instances. [appropriate place to use fig 1]
    * A **rule** includes a trigger—either a metric trigger or a time trigger—and a scale action, indicating whether autoscale should scale up or down when that rule is satisfied. 
    * A **recurrence** indicates when autoscale should put this profile into effect. You can have different autoscale profiles for different times of day or days of the week, for example.
* A **notification setting** defines what notifications should occur when an autoscale event occurs based on satisfying the criteria of one of the autoscale setting’s profiles. Autoscale can notify one or more email addresses or make calls to one or more webhooks.

![Azure autoscale setting, profile, and rule structure](./media/monitoring-autoscale-overview/AzureResourceManagerRuleStructure3.png)

The full list of configurable fields and descriptions is available in the [Autoscale REST API](https://msdn.microsoft.com/library/dn931928.aspx).

For code examples, see

* [Advanced Autoscale configuration using Resource Manager templates for VM Scale Sets](insights-advanced-autoscale-virtual-machine-scale-sets.md)  
* [Autoscale REST API](https://msdn.microsoft.com/library/dn931953.aspx) 

## Horizontal vs vertical scaling
Autoscale increases resources in only scales horizontally, which is an increase ("out") or decrease ("in") in the number of VM instances.  Horizontal scaling, which is more flexible in a cloud situation as it allows you to run potentially thousands of VMs to handle load. Vertical scaling is different. It keeps the same number of VMs, but makes the VM more ("up") or less ("down") powerful. Power is measured in memory, CPU speed, disk space, etc.  Vertical scaling has more limitations. It's dependent on the availability of larger hardware, which can vary by region and quickly hits and upper limit. Vertical scaling also usually requires a VM stop and start. For more information, see [Vertically scale Azure virtual machine with Azure Automation](../virtual-machines/virtual-machines-linux-vertical-scaling-automation.md). 

## Methods of access
You can set up autoscale via 

* [Azure portal](insights-how-to-scale.md)
* [PowerShell](insights-powershell-samples.md#create-and-manage-autoscale-settings) 
* [Cross-platform Command Line Interface (CLI)](insights-cli-samples.md#autoscale)
* [Insights REST API](https://msdn.microsoft.com/library/azure/dn931953.aspx)

## Supported services for autoscale
| Service | Schema & Docs |
| --- | --- |
| Web Apps |[Scaling Web Apps](insights-how-to-scale.md) |
| Cloud Services |[Autoscale a Cloud Service](../cloud-services/cloud-services-how-to-scale.md) |
| Virtual Machines : Classic |[Scaling Classic Virtual Machine Availability Sets](https://blogs.msdn.microsoft.com/kaevans/2015/02/20/autoscaling-azurevirtual-machines/) |
| Virtual Machines : Windows Scale Sets |[Scaling VM Scale Sets in Windows](../virtual-machine-scale-sets/virtual-machine-scale-sets-windows-autoscale.md) |
| Virtual Machines : Linux Scale Sets |[Scaling VM Scale Sets in Linux](../virtual-machine-scale-sets/virtual-machine-scale-sets-linux-autoscale.md) |
| Virtual Machines : Windows Example |[Advanced Autoscale configuration using Resource Manager templates for VM Scale Sets](insights-advanced-autoscale-virtual-machine-scale-sets.md) |

## Next steps
To learn more about autoscale, use the Autoscale Walkthroughs listed previously or refer to the following resources: 

* [Azure Insights autoscale common metrics](insights-autoscale-common-metrics.md)
* [Best practices for Azure Insights autoscale](insights-autoscale-best-practices.md)
* [Use autoscale actions to send email and webhook alert notifications](insights-autoscale-to-webhook-email.md)
* [Autoscale REST API](https://msdn.microsoft.com/library/dn931953.aspx)
* [Troubleshooting Virtual Machine Scale Sets Autoscale](../virtual-machine-scale-sets/virtual-machine-scale-sets-troubleshoot.md) 

