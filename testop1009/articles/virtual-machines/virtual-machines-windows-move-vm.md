---
title: Move a Windows VM | Microsoft Azure
description: Move a Windows VM to another Azure subscription or resource group in the Resource Manager deployment model.
services: virtual-machines-windows
documentationcenter: ''
author: cynthn
manager: timlt
editor: ''
tags: azure-resource-manager

ms.service: virtual-machines-windows
ms.workload: infrastructure-services
ms.tgt_pltfrm: na
ms.devlang: na
ms.topic: article
ms.date: 08/08/2016
ms.author: cynthn

---
# Move a Windows VM to another Azure subscription or resource group
This article walks you through how to move a Windows VM between resource groups or subscriptions. Moving between subscriptions can be handy if you originally created a VM in a personal subscription and now want to move it to your company's subscription to continue your work.

> [!NOTE]
> New resource IDs will be created as part of the move. Once the VM has been moved, you will need to update your tools and scripts to use the new resource IDs. 
> 
> 

[!INCLUDE [virtual-machines-common-move-vm](../../includes/virtual-machines-common-move-vm.md)]

## Use Powershell to move a VM
To move a virtual machine to another resource group, you need to make sure that you also move all of the dependent resources. To use the Move-AzureRMResource cmdlet, you need the resource name and the type of resource. You can get both from the Find-AzureRMResource cmdlet.

    Find-AzureRMResource -ResourceGroupNameContains "<sourceResourceGroupName>"


To move a VM we need to move multiple resources. We can just create separate variables for each resource and then list them. This example includes most of the basic resources for a VM, but you can add more as needed.

    $sourceRG = "<sourceResourceGroupName>"
    $destinationRG = "<destinationResourceGroupName>"

    $vm = Get-AzureRmResource -ResourceGroupName $sourceRG -ResourceType "Microsoft.Compute/virtualMachines" -ResourceName "<vmName>"
    $storageAccount = Get-AzureRmResource -ResourceGroupName $sourceRG -ResourceType "Microsoft.Storage/storageAccounts" -ResourceName "<storageAccountName>"
    $diagStorageAccount = Get-AzureRmResource -ResourceGroupName $sourceRG -ResourceType "Microsoft.Storage/storageAccounts" -ResourceName "<diagnosticStorageAccountName>"
    $vNet = Get-AzureRmResource -ResourceGroupName $sourceRG -ResourceType "Microsoft.Network/virtualNetworks" -ResourceName "<vNetName>"
    $nic = Get-AzureRmResource -ResourceGroupName $sourceRG -ResourceType "Microsoft.Network/networkInterfaces" -ResourceName "<nicName>"
    $ip = Get-AzureRmResource -ResourceGroupName $sourceRG -ResourceType "Microsoft.Network/publicIPAddresses" -ResourceName "<ipName>"
    $nsg = Get-AzureRmResource -ResourceGroupName $sourceRG -ResourceType "Microsoft.Network/networkSecurityGroups" -ResourceName "<nsgName>"

    Move-AzureRmResource -DestinationResourceGroupName $destinationRG -ResourceId $vm.ResourceId, $storageAccount.ResourceId, $diagStorageAccount.ResourceId, $vNet.ResourceId, $nic.ResourceId, $ip.ResourceId, $nsg.ResourceId

To move the resources to different subscription, include the **-DestinationSubscriptionId** parameter. 

    Move-AzureRmResource -DestinationSubscriptionId "<destinationSubscriptionID>" -DestinationResourceGroupName $destinationRG -ResourceId $vm.ResourceId, $storageAccount.ResourceId, $diagStorageAccount.ResourceId, $vNet.ResourceId, $nic.ResourceId, $ip.ResourceId, $nsg.ResourceId



You will be asked to confirm that you want to move the specified resources. Type **Y** to confirm that you want to move the resources.

## Next steps
You can move many different types of resources between resource groups and subscriptions. For more information, see [Move resources to new resource group or subscription](../resource-group-move-resources.md).    

