---
title: Azure Government documentation | Microsoft Azure
description: This provides a comparision of features and guidance on developing applications for Azure Government
services: Azure-Government
cloud: gov
documentationcenter: ''
author: ryansoc
manager: zakramer
editor: ''

ms.service: multiple
ms.devlang: na
ms.topic: article
ms.tgt_pltfrm: na
ms.workload: azure-government
ms.date: 08/25/2016
ms.author: ryansoc

---
# Azure Government Management and Security
## Key Vault
The following information identifies the Azure Government boundary for Azure Key Vault:

| Regulated/controlled data permitted | Regulated/controlled data not permitted |
| --- | --- |
| All data encrypted with an Azure Key Vault key may contain Regulated/controlled data. |Azure Key Vault metadata is not permitted to contain export controlled data. This metadata includes all configuration data entered when creating and maintaining your Key Vault.  Do not enter Regulated/controlled data into the following fields: Resource group names, Key Vault names, Subscription name |

Key Vault is generally available in Azure Government. Just as in public, there is no extension, so Key Vault is available through PowerShell and CLI only.

For additional information, please see the [Azure Key Vault public documentation](/key-vault-get-started).

For supplemental information and updates please subscribe to the
<a href="https://blogs.msdn.microsoft.com/azuregov/">Microsoft Azure Government Blog. </a>

