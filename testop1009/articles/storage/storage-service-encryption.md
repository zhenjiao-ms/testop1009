---
title: Azure Storage Service Encryption for Data at Rest | Microsoft Azure
description: Use the Azure Storage Service Encryption feature to encrypt your Azure Blob Storage on the service side when storing the data, and decrypt it when retrieving the data.
services: storage
documentationcenter: .net
author: robinsh
manager: carmonm
editor: tysonn

ms.service: storage
ms.workload: storage
ms.tgt_pltfrm: na
ms.devlang: na
ms.topic: article
ms.date: 09/08/2016
ms.author: robinsh

---
# Azure Storage Service Encryption for Data at Rest
Azure Storage Service Encryption (SSE) for Data at Rest helps you protect and safeguard your data to meet your organizational security and compliance commitments. With this feature, Azure Storage automatically encrypts your data prior to persisting to storage and decrypts prior to retrieval. The encryption, decryption, and key management are totally transparent to users.

The following sections provide detailed guidance on how to use the Storage Service Encryption features as well as the supported scenarios and user experiences.

## Overview
Azure Storage provides a comprehensive set of security capabilities which together enable developers to build secure applications. Data can be secured in transit between an application and Azure by using [Client-Side Encryption](storage-client-side-encryption.md), HTTPs, or SMB 3.0. Storage Service Encryption provides encryption at rest, handling encryption, decryption, and key management in a totally transparent fashion. All data is encrypted using 256-bit [AES encryption](https://en.wikipedia.org/wiki/Advanced_Encryption_Standard), one of the strongest block ciphers available.

SSE works by encrypting the data when it is written to Azure Storage, and can be used  for block blobs, page blobs and append blobs. It works for the following:

    - General purpose storage accounts and Blob storage accounts
    - Standard storage and Primary storage 
    - All redundancy levels (LRS, ZRS, GRS, RA-GRS)
    - Azure Resource Manager storage accounts (but not classic) 
    - All regions

This screenshot shows where to find the Storage Service Encryption setting using the [Azure portal](https://azure.portal.com). On this screen, you would click Encryption to continue.

![Portal Screenshot showing Encryption option](./media/storage-service-encryption/image1.png)

After you click the Encryption setting, you can enable or disable Storage Service Encryption.

![Portal Screenshot showing Encryption properties](./media/storage-service-encryption/image2.png)

## Encryption Scenarios
Storage Service Encryption can be enabled at a storage account level. It supports the following customer scenarios:

* Encryption of block blobs, append blobs, and page blobs.
* Encryption of archived VHDs and templates brought to Azure from on-premises.
* Encryption of underlying OS and data disks for IaaS VMs created using your VHDs.

SSE has the following limitations:

* Encryption of classic storage accounts is not supported.
* Encryption of classic storage accounts migrated to Resource Manager storage accounts is not supported.
* Existing Data - SSE only encrypts newly created data after the encryption is enabled. If for example you create a new Resource Manager storage account but don’t turn on encryption, and then you upload blobs or archived VHDs to that storage account and then turn on SSE, those blobs will not be encrypted unless they are rewritten or copied.
* Marketplace Support - Enable encryption of VMs created from the Marketplace using the [Azure portal](https://portal.azure.com), PowerShell, and Azure CLI. The VHD base image will remain unencrypted; however, any writes done after the VM has spun up will be encrypted.
* Table, Queues, and Files data will not be encrypted.

## Getting Started
### Step 1: [Create a new storage account](storage-create-storage-account.md).
### Step 2: Enable encryption.
You can enable encryption using the [Azure portal](https://portal.azure.com).

> [!NOTE]
> If you want to programmatically enable or disable the Storage Service Encryption on a storage account, you can use the [Azure Storage Resource Provider REST API](https://msdn.microsoft.com/library/azure/mt163683.aspx), the [Storage Resource Provider Client Library for .NET](https://msdn.microsoft.com/library/azure/mt131037.aspx), [Azure PowerShell](../powershell-install-configure.md), or the [Azure CLI](storage-azure-cli.md).
> 
> 

### Step 3: Copy data to storage account
If you enable SSE on a storage account and then write blobs to that storage account, the blobs will be encrypted. Any blobs already located in that storage account will not be encrypted until they are rewritten. You can copy the data from one storage account to one with SSE encrypted, or even enable SSE and copy the blobs from one container to another to sure that previous data is encrypted. You can use any of the following tools to accomplish this.

#### Using AzCopy
AzCopy is a Windows command-line utility designed for copying data to and from Microsoft Azure Blob, File, and Table storage using simple commands with optimal performance. You can use this to copy your blobs from one storage account to another one that has SSE enabled. 

To learn more, please visit [Transfer data with the AzCopy Command-Line Utility](storage-use-azcopy.md).

#### Using the Storage Client Libraries
You can copy blob data to and from blob storage or between storage accounts using our rich set of Storage Client Libraries including .NET, C++, Java, Android, Node.js, PHP, Python, and Ruby.

To learn more, please visit our [Get started with Azure Blob storage using .NET](storage-dotnet-how-to-use-blobs.md).

#### Using a Storage Explorer
You can use a Storage explorer to create storage accounts, upload and download data, view contents of blobs, and navigate through directories. You can use one of these to upload blobs to your storage account with encryption enabled. With some storage explorers, you can also copy data from existing blob storage to a different container in the storage account or a new storage account that has SSE enabled.

To learn more, please visit [Azure Storage Explorers](storage-explorers.md).

### Step 4: Query the status of the encrypted data
An updated version of the Storage Client libraries has been deployed that allows you to query the state of an object to determine if it is encrypted or not. Examples will be added to this document in the near future.

In the meantime, you can call [Get Account Properties](https://msdn.microsoft.com/library/azure/mt163553.aspx) to verify that the storage account has encryption enabled or view the storage account properties in the Azure portal.

## Encryption and Decryption Workflow
Here is a brief description of the encryption/decryption workflow:

* The customer enables encryption on the storage account.
* When the customer writes new data (PUT Blob, PUT Block, PUT Page, etc.) to Blob storage; every write is encrypted using 256-bit [AES encryption](https://en.wikipedia.org/wiki/Advanced_Encryption_Standard), one of the strongest block ciphers available.
* When the customer needs to access data (GET Blob, etc.), data is automatically decrypted before returning to the user.
* If encryption is disabled, new writes are no longer encrypted and existing encrypted data remains encrypted until rewritten by the user. While encryption is enabled, writes to Blob storage will be encrypted. The state of data does not change with the user toggling between enabling/disabling encryption for the storage account.
* All encryption keys are stored, encrypted, and managed by Microsoft.

## Frequently asked questions about Storage Service Encryption for Data at Rest
**Q: I have an existing classic storage account. Can I enable SSE on it?**

A: No, SSE is only supported on Resource Manager storage accounts.

**Q: How can I encrypt data in my classic storage account?**

A: You can create a new Resource Manager storage account and copy your data using [AzCopy](storage-use-azcopy.md) from your existing classic storage account to your newly created Resource Manager storage account.

**Q: I have an existing Resource Manager storage account. Can I enable SSE on it?**

A: Yes, but only newly written blobs will be encrypted. It does not go back and encrypt data that was already present. 

**Q: I would like to encrypt the current data in an existing Resource Manager storage account?**

A: You can enable SSE at any time in a Resource Manager storage account. However, blobs that were already present will not be encrypted. To encrypt those blobs, you can copy them to another name or another container and then remove the unencrypted versions.

**Q: I’m using Premium storage; can I use SSE?**

A: Yes, SSE is supported on both Standard Storage and Premium Storage.

**Q: If I create a new storage account and enable SSE, then create a new VM using that storage account, does that mean my VM is encrypted?**

A: Yes. Any disks created that use the new storage account will be encrypted, as long as they are created after SSE is enabled. If the VM was created using Azure Market Place, the VHD base image will remain unencrypted; however, any writes done after the VM has spun up will be encrypted.

**Q: Can I create new storage accounts with SSE enabled using Azure PowerShell and Azure CLI?**

A: Yes.

**Q: How much more does Azure Storage cost if SSE is enabled?**

A: There is no additional cost.

**Q: Who manages the encryption keys?**

A: The keys are managed by Microsoft.

**Q: Can I use my own encryption keys?**

A: We are working on providing capabilities for customers to bring their own encryption keys.

**Q: Can I revoke access to the encryption keys?**

A: Not at this time; the keys are fully managed by Microsoft.

**Q: Is SSE enabled by default when I create a new storage account?**

A: SSE is not enabled by default; you can use the Azure portal to enable it. You can also programmatically enable this feature using the Storage Resource Provider REST API.

**Q: How is this different from Azure Drive Encryption?**

A: This feature is used to encrypt data in Azure Blob storage. The Azure Disk Encryption is used to encrypt OS and Data disks in IaaS VMs. For more details, please visit our [Storage Security Guide](storage-security-guide.md).

**Q: What if I enable SSE, and then go in and enable Azure Disk Encryption on the disks?**

A: This will work seamlessly. Your data will be encrypted by both methods.

**Q: My storage account is set up to be replicated geo-redundantly. If I enable SSE, will my redundant copy also be encrypted?**

A: Yes, all copies of the storage account are encrypted, and all redundancy options – Locally Redundant Storage (LRS), Zone-Redundant Storage (ZRS), Geo-Redundant Storage (GRS), and Read Access Geo-Redundant Storage (RA-GRS) – are supported.

**Q: I can’t enable encryption on my storage account.**

A: Is it a Resource Manager storage account? Classic storage accounts are not supported. 

**Q: Is SSE only permitted in specific regions?**

A: The SSE is available in all regions. 

**Q: How do I contact someone if I have any issues or want to provide feedback?**

A: Please contact [ssediscussions@microsoft.com](mailto:ssediscussions@microsoft.com) for any issues related to Storage Service Encryption.

## Next Steps
Azure Storage provides a comprehensive set of security capabilities which together enable developers to build secure applications. For more details, visit the [Storage Security Guide](storage-security-guide.md).

