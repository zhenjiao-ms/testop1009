---
title: Install Symantec Endpoint Protection on a VM | Microsoft Azure
description: Learn how to install and configure the Symantec Endpoint Protection security extension on a new or existing Azure VM created with the classic deployment model.
services: virtual-machines-windows
documentationcenter: ''
author: iainfoulds
manager: timlt
editor: ''
tags: azure-service-management

ms.service: virtual-machines-windows
ms.workload: infrastructure-services
ms.tgt_pltfrm: vm-multiple
ms.devlang: na
ms.topic: article
ms.date: 08/24/2016
ms.author: iainfou

---
# How to install and configure Symantec Endpoint Protection on a Windows VM
[!INCLUDE [learn-about-deployment-models](../../includes/learn-about-deployment-models-classic-include.md)]

This article shows you how to install and configure the Symantec Endpoint Protection client on an existing virtual machine (VM) running Windows Server. This is the full client, which includes services such as virus and spyware protection, firewall, and intrusion prevention. The client is installed as a security extension by using the VM Agent.

If you have an existing subscription from Symantec for an on-premises solution, you can use it to protect your Azure virtual machines. If you're not a customer yet, you can sign up for a trial subscription. For more information about this solution, see [Symantec Endpoint Protection on Microsoft's Azure platform][Symantec]. This page also has links to licensing information and instructions for installing the client if you're already a Symantec customer.

## Install Symantec Endpoint Protection on an existing VM
Before you begin, you need the following:

* The Azure PowerShell module, version 0.8.2 or later, on your work computer. You can check the version of Azure PowerShell that you have installed with the **Get-Module azure | format-table version** command. For instructions and a link to the latest version, see [How to Install and Configure Azure PowerShell][PS]. Log in to your Azure subscription using `Add-AzureAccount`.
* The VM Agent running on the Azure Virtual Machine.

First, verify that the VM Agent is already installed on the virtual machine. Fill in the cloud service name and virtual machine name, and then run the following commands at an administrator-level Azure PowerShell command prompt. Replace everything within the quotes, including the < and > characters.

> [!TIP]
> If you don't know the cloud service and virtual machine names, run **Get-AzureVM** to list the names for all virtual machines in your current subscription.
> 
> 

    $CSName = "<cloud service name>"
    $VMName = "<virtual machine name>"
    $vm = Get-AzureVM -ServiceName $CSName -Name $VMName
    write-host $vm.VM.ProvisionGuestAgent

If the **write-host** command displays **True**, the VM Agent is installed. If it displays **False**, see the instructions and a link to the download in the Azure blog post [VM Agent and Extensions - Part 2][Agent].

If the VM Agent is installed, run these commands to install the Symantec Endpoint Protection agent.

    $Agent = Get-AzureVMAvailableExtension -Publisher Symantec -ExtensionName SymantecEndpointProtection

    Set-AzureVMExtension -Publisher Symantec –Version $Agent.Version -ExtensionName SymantecEndpointProtection -VM $vm | Update-AzureVM

To verify that the Symantec security extension has been installed and is up-to-date:

1. Log on to the virtual machine. For instructions, see [How to Log on to a Virtual Machine Running Windows Server][Logon].
2. For Windows Server 2008 R2, click **Start > Symantec Endpoint Protection**. For Windows Server 2012 or Windows Server 2012 R2, from the start screen, type **Symantec**, and then click **Symantec Endpoint Protection**.
3. From the **Status** tab of the **Status-Symantec Endpoint Protection** window, apply updates or restart if needed.

## Additional resources
[How to Log on to a Virtual Machine Running Windows Server][Logon]

[Azure VM Extensions and Features][Ext]

<!--Link references-->
[Symantec]: http://www.symantec.com/connect/blogs/symantec-endpoint-protection-now-microsoft-azure

[Portal]: http://manage.windowsazure.com

[Create]: virtual-machines-windows-classic-tutorial.md

[PS]: ../powershell-install-configure.md

[Agent]: http://go.microsoft.com/fwlink/p/?LinkId=403947

[Logon]: virtual-machines-windows-classic-connect-logon.md

[Ext]: http://go.microsoft.com/fwlink/p/?linkid=390493