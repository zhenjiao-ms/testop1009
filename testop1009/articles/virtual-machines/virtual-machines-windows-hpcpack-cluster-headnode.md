---
title: Create an HPC Pack head node in an Azure VM | Microsoft Azure
description: Learn how to use the Azure portal and the Resource Manager deployment model to create a Microsoft HPC Pack head node in an Azure VM.
services: virtual-machines-windows
documentationcenter: ''
author: dlepow
manager: timlt
editor: ''
tags: azure-resource-manager,hpc-pack

ms.service: virtual-machines-windows
ms.devlang: na
ms.topic: article
ms.tgt_pltfrm: vm-windows
ms.workload: big-compute
ms.date: 08/17/2016
ms.author: danlep

---
# Create the head node of an HPC Pack cluster in an Azure VM with a Marketplace image
Use a [Microsoft HPC Pack virtual machine image](https://azure.microsoft.com/marketplace/partners/microsoft/hpcpack2012r2onwindowsserver2012r2/) from the Azure Marketplace and the Azure portal
to create the head node of an HPC cluster. This HPC Pack
VM image is based on Windows Server 2012 R2 Datacenter with HPC
Pack 2012 R2 Update 3 pre-installed. Use this head node for a proof of concept deployment of HPC Pack in Azure. You can then add compute nodes to the cluster to run HPC workloads.

> [!TIP]
> To deploy a complete HPC Pack cluster in Azure that includes the head node and compute nodes, we recommend that you use an automated method. Options include the [HPC Pack IaaS deployment script](virtual-machines-windows-classic-hpcpack-cluster-powershell-script.md) and the [HPC Pack cluster for Windows workloads](https://azure.microsoft.com/marketplace/partners/microsofthpc/newclusterwindowscn/) Resource Manager template. See [HPC Pack cluster options in Azure](virtual-machines-windows-hpcpack-cluster-options.md) for additional templates. 
> 
> 

## Planning considerations
As shown in the following figure, you deploy the HPC Pack head node in an Active Directory domain in an Azure virtual network.

![HPC Pack head node][headnode]

* **Active Directory domain** - The HPC Pack head node must be joined to an Active Directory domain in Azure before you start the HPC services on the VM. As shown in this article, for a proof of concept deployment, you can promote the VM you create for the head node as a domain controller before starting the HPC services. Another option is to deploy a separate domain controller and forest in Azure to which you join the head node VM.
* **Azure virtual network** - When you use the Resource Manager deployment model to deploy the head node, you specify or create an Azure virtual network. You use the virtual network if you need to join the head node to an existing Active Directory domain. You also need it later to add compute node VMs to the cluster.

## Steps to create the head node
Following are high-level steps to use the Azure portal to create an Azure VM for the HPC
Pack head node by using the Resource Manager deployment model. 

1. If you want to create a new Active Directory forest in Azure with separate domain controller VMs, one option is to use a [Resource Manager template](https://azure.microsoft.com/documentation/templates/active-directory-new-domain-ha-2-dc/). For a simple proof of concept deployment, it's fine to omit this step and configure the head node VM itself as a domain controller. This option is described later in this article.
2. On the [HPC Pack 2012 R2 on Windows Server 2012 R2 page](https://azure.microsoft.com/marketplace/partners/microsoft/hpcpack2012r2onwindowsserver2012r2/) in the Azure Marketplace, click **Create Virtual Machine**. 
3. In the portal, on the **HPC Pack 2012 R2 on Windows Server 2012 R2** page, select the **Resource Manager** deployment model and then click **Create**.
   
    ![HPC Pack image][marketplace]
4. Use the portal to configure the settings and create the VM. If you're new to Azure, follow the tutorial [Create a Windows virtual machine in the Azure portal](virtual-machines-windows-hero-tutorial.md). For a proof of concept deployment, you can usually accept the default or recommended settings.
   
   > [!NOTE]
   > If you want to join the head node to an existing Active Directory domain in Azure, make sure you specify the virtual network for that domain when creating the VM.
   > 
   > 
5. After you create the VM and the VM is running, [connect to the VM](virtual-machines-windows-connect-logon.md) by Remote Desktop. 
6. Join the VM to an existing domain forest, or create a domain forest on the VM itself.
   
   * If you created the VM in an Azure virtual network with an existing domain forest, join the VM to the forest by using standard Server Manager or Windows PowerShell tools. Then restart.
   * If you created the VM in a new virtual network (without an existing domain forest), then promote the VM as a domain controller. Use standard steps to install and configure the Active Directory Domain Services role on the head node. For detailed steps, see [Install a New Windows Server 2012 Active Directory Forest](https://technet.microsoft.com/library/jj574166.aspx).
7. After the VM is running and is joined to an Active Directory forest, start the HPC Pack services as follows:
   
    a. Connect to the head node VM using a domain account that is a member of the local Administrators group. For example, use the administrator account you set up when you created the head node VM.
   
    b. For a default head node configuration, start Windows PowerShell as an administrator and type the following:
   
    ```
    & $env:CCP_HOME\bin\HPCHNPrepare.ps1 –DBServerInstance ".\ComputeCluster"
    ```
   
    It can take several minutes for the HPC Pack services to start.
   
    For additional head node configuration options, type `get-help HPCHNPrepare.ps1`.

## Next steps
* You can now work with the head node of your HPC Pack cluster. For
  example, start HPC Cluster Manager, and complete the [Deployment To-do List](https://technet.microsoft.com/library/jj884141.aspx).
* If you want to increase the cluster compute capacity on-demand, add [Azure burst nodes](virtual-machines-windows-classic-hpcpack-cluster-node-burst.md) in a cloud service. 
* Try running a test workload on the cluster. For an example, see the HPC Pack [getting started guide](https://technet.microsoft.com/library/jj884144).

<!--Image references-->
[headnode]: ./media/virtual-machines-windows-hpcpack-cluster-headnode/headnode.png
[marketplace]: ./media/virtual-machines-windows-hpcpack-cluster-headnode/marketplace.png
