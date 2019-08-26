---
title: Resource Groups Guidelines | Microsoft Azure
description: Learn about the key design and implementation guidelines for deploying Resource Groups in Azure infrastructure services.
documentationcenter: ''
services: virtual-machines-linux
author: iainfoulds
manager: timlt
editor: ''
tags: azure-resource-manager

ms.service: virtual-machines-linux
ms.workload: infrastructure-services
ms.tgt_pltfrm: vm-linux
ms.devlang: na
ms.topic: article
ms.date: 09/08/2016
ms.author: iainfou

---
# Azure resource group guidelines
[!INCLUDE [virtual-machines-linux-infrastructure-guidelines-intro](../../includes/virtual-machines-linux-infrastructure-guidelines-intro.md)]

This article focuses on understanding how to logically build out your environment and group all the components in Resource Groups.

## Implementation guidelines for Resource Groups
Decisions:

* Are you going to build out Resource Groups by the core infrastructure components, or by complete application deployment?
* Do you need to restrict access to Resource Groups using Role-Based Access Controls?

Tasks:

* Define what core infrastructure components and dedicated Resource Groups you need.
* Review how to implement Resource Manager templates for consistent, reproducible deployments.
* Define what user access roles you need for controlling access to Resource Groups.
* Create the set of Resource Groups using your naming convention. You can use the Azure CLI or portal.

## Resource Groups
In Azure, you logically group related resources such as storage accounts, virtual networks, and virtual machines (VMs) to deploy, manage, and maintain them as a single entity. This approach makes it easier to deploy applications while keeping all the related resources together from a management perspective, or to grant others access to that group of resources. For a more comprehensive understanding of Resource Groups, you can read the [Azure Resource Manager overview](../resource-group-overview.md).

A key feature to Resource Groups is the ability to build your environment using a JSON file that declares the storage, networking, and compute resources. You can also define any related custom scripts or configurations to apply. By using these JSON templates, you create consistent, reproducible deployments for your applications. This approach lets you build an environment in development and then use that same template to create a production deployment, or vice versa. For a better understanding about using templates, read [the template walkthrough](../resource-manager-template-walkthrough.md) that guides you through each step of building out a JSON template.

There are two different approaches you can take when designing your environment with Resource Groups:

* Resource Groups for each application deployment that combines the storage accounts, virtual networks, and subnets, VMs, load balancers, etc.
* Centralized Resource Groups that contain your core virtual networking and subnets or storage accounts. Your applications are then in their own Resource Groups that only contain VMs, load balancers, network interfaces, etc.

As you scale out, creating centralized Resource Groups for your virtual networking and subnets makes it easier to build cross-premises network connections for hybrid connectivity options. The alternative approach is for each application to have their own virtual network that requires configuration and maintenance. [Role-Based Access Controls](../active-directory/role-based-access-control-what-is.md) provide a granular way to control access to Resource Groups. For production applications, you can control the users that may access those resources, or for the core infrastructure resources you can limit only infrastructure engineers to work with them. Your application owners only have access to the application components within their Resource Group and not the core Azure infrastructure of your environment. As you design your environment, consider the users that require access to the resources and design your Resource Groups accordingly. 

## Next steps
[!INCLUDE [virtual-machines-linux-infrastructure-guidelines-next-steps](../../includes/virtual-machines-linux-infrastructure-guidelines-next-steps.md)]

