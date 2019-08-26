---
title: Using Windows client images for dev / test | Microsoft Azure
description: How to use Visual Studio subscription benefits to deploy Windows 7/8/10 in Azure for dev / test scenarios
services: virtual-machines-windowse
documentationcenter: ''
author: iainfoulds
manager: timlt
editor: ''

ms.service: virtual-machines-windows
ms.devlang: na
ms.topic: article
ms.tgt_pltfrm: vm-windows
ms.workload: infrastructure-services
ms.date: 08/31/2016
ms.author: iainfou

---
# Using Windows client in Azure for dev/test
You can use Windows 7, Windows 8, or Windows 10 in Azure for dev / test scenarios provided you have an appropriate Visual Studio (formerly MSDN) subscription. This article outlines the eligibility requirements for running Windows client in Azure and use of the Azure Gallery images.

## Subscription eligibility
Active Visual Studio subscribers (people who have acquired a Visual Studio subscription license) can use Windows client for development and testing purposes. Windows client can be used on your own hardware and Azure virtual machines running in any type of Azure subscription. Windows client may not be deployed to or used on Azure for normal production use, or used by people who are not active Visual Studio subscribers.

For your convenience, we have made certain Windows 10 images available from the Azure Gallery within [eligible dev/test offers](#eligible-offers). Visual Studio subscribers within any type of offer can also [adequately prepare and create](virtual-machines-windows-prepare-for-upload-vhd-image.md) a 64-bit Windows 7, Windows 8, or Windows 10 image and then [upload to Azure](virtual-machines-windows-upload-image.md). The use remains limited to dev/test by active Visual Studio subscribers.

## Eligible offers
The following table details the offer IDs that are eligible to deploy Windows 10 through the Azure Gallery. The Windows 10 images are only visible to the following offers. Visual Studio subscribers who need to run Windows client in a different offer type require you to [adequately prepare and create](virtual-machines-windows-prepare-for-upload-vhd-image.md) a 64-bit Windows 7, Windows 8, or Windows 10 image and [then upload to Azure](virtual-machines-windows-upload-image.md).

| Offer Name | Offer Number | Available client images |
|:--- |:---:|:---:|
| [Pay-As-You-Go Dev/Test](https://azure.microsoft.com/offers/ms-azr-0023p/) |0023P |Windows 10 |
| [Visual Studio Enterprise (MPN) subscribers](https://azure.microsoft.com/offers/ms-azr-0029p/) |0029P |Windows 10 |
| [Visual Studio Professional subscribers](https://azure.microsoft.com/offers/ms-azr-0059p/) |0059P |Windows 10 |
| [Visual Studio Test Professional subscribers](https://azure.microsoft.com/offers/ms-azr-0060p/) |0060P |Windows 10 |
| [Visual Studio Premium with MSDN (benefit)](https://azure.microsoft.com/offers/ms-azr-0061p/) |0061P |Windows 10 |
| [Visual Studio Enterprise subscribers](https://azure.microsoft.com/offers/ms-azr-0063p/) |0063P |Windows 10 |
| [Visual Studio Enterprise (BizSpark) subscribers](https://azure.microsoft.com/offers/ms-azr-0064p/) |0064P |Windows 10 |
| [Enterprise Dev/Test](https://azure.microsoft.com/ofers/ms-azr-0148p/) |0148P |Windows 10 |

## Check your Azure subscription
If you do not know your offer ID, you can obtain it through the Azure portal or the Account portal.

The subscription offer ID is noted on the 'Subscriptions' blade within the Azure portal:

![Offer ID details from the Azure portal](./media/virtual-machines-windows-client-images/offer_id_azure_portal.png) 

You can also view the offer ID from the ['Subscriptions' tab](http://account.windowsazure.com/Subscriptions) of the Azure Account portal:

![Offer ID details from the Azure Account portal](./media/virtual-machines-windows-client-images/offer_id_azure_account_portal.png) 

## Next steps
You can now deploy your VMs using [PowerShell](virtual-machines-windows-ps-create.md), [Resource Manager templates](virtual-machines-windows-ps-template.md), or [Visual Studio](../vs-azure-tools-resource-groups-deployment-projects-create-deploy.md).

