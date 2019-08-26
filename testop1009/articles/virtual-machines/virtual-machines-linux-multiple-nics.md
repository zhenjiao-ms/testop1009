---
title: Configure multiple NICs on a Linux VM | Microsoft Azure
description: Learn how to create a VM with multiple NICs attached to it using the Azure CLI or Resource Manager templates.
services: virtual-machines-linux
documentationcenter: ''
author: iainfoulds
manager: timlt
editor: ''

ms.service: virtual-machines-linux
ms.devlang: na
ms.topic: article
ms.tgt_pltfrm: vm-linux
ms.workload: infrastructure
ms.date: 08/02/2016
ms.author: iainfou

---
# Creating a VM with multiple NICs
You can create a virtual machine (VM) in Azure that has multiple virtual network interfaces (NICs) attached to it. A common scenario would be to have different subnets for front-end and back-end connectivity, or a network dedicated to a monitoring or backup solution. This article provides quick commands to create a VM with multiple NICs attached to it. For detailed information, including how to create multiple NICs within your own Bash scripts, read more about [deploying multi-NIC VMs](../virtual-network/virtual-network-deploy-multinic-arm-cli.md). Different [VM sizes](virtual-machines-linux-sizes.md) support a varying number of NICs, so size your VM accordingly.

> [!WARNING]
> You must attach multiple NICs when you create a VM - you cannot add NICs to an existing VM. You can [create a new VM based on the original virtual disk(s)](virtual-machines-linux-copy-vm.md) and create multiple NICs as you deploy the VM.
> 
> 

## Quick commands
Make sure that you have the [Azure CLI](../xplat-cli-install.md) logged in and using Resource Manager mode (`azure config mode arm`).

First, create a resource group:

```bash
azure group create TestRG --location WestUS
```

Create a storage account to hold your VMs:

```bash
azure storage account create teststorage --resource-group TestRG \
    --location WestUS --kind Storage --sku-name PLRS
```

Create a virtual network to connect your VMs to:

```bash
azure network vnet create --resource-group TestRG --location WestUS \
    --name TestVNet --address-prefixes 192.168.0.0/16 
```

Create two virtual network subnets - one for front-end traffic and one for back-end traffic:

```bash
azure network vnet subnet create --resource-group TestRG --vnet-name TestVNet \
    --name FrontEnd --address-prefix 192.168.1.0/24
azure network vnet subnet create --resource-group TestRG --vnet-name TestVNet \
    --name BackEnd --address-prefix 192.168.2.0/24
```

Create two NICs, attaching one NIC to the front-end subnet and one NIC to the back-end subnet:

```bash
azure network nic create --resource-group TestRG --location WestUS \
    -n NIC1 --subnet-vnet-name TestVNet --subnet-name FrontEnd
azure network nic create --resource-group TestRG --location WestUS \
    -n NIC2 --subnet-vnet-name TestVNet --subnet-name BackEnd
```

Finally create your VM, attaching the two NICs you previously created:

```bash
azure vm create \            
    --resource-group TestRG \
    --name TestVM1 \
    --location WestUS \
    --os-type linux \
    --nic-names NIC1,NIC2 \
    --vm-size Standard_DS2_v2
    --storage-account-name teststorage \
    --image-urn UbuntuLTS \
    --admin-username ops \
    --ssh-publickey-file ~/.ssh/id_rsa.pub
```

## Creating multiple NICs using Azure CLI
If you have previously created a VM using the Azure CLI, the quick commands should be familiar. The process is the same to create one NIC or multiple NICs. You can read more details about [deploying multiple NICs using the Azure CLI](../virtual-network/virtual-network-deploy-multinic-arm-cli.md), including scripting the process of looping through to create all the NICs.

The following example creates two NICs, with one NIC connecting to each subnet:

```bash
azure network nic create --resource-group TestRG --location WestUS \
    -n NIC1 --subnet-vnet-name TestVNet --subnet-name FrontEnd
azure network nic create --resource-group TestRG --location WestUS \
    -n NIC2 --subnet-vnet-name TestVNet --subnet-name BackEnd
```

Typically you would also create a [network security group](../virtual-network/virtual-networks-nsg.md) or [load balancer](../load-balancer/load-balancer-overview.md) to help manage and distribute traffic across your VMs. Again, the commands are the same when working with multiple NICs. The NICs you create get bound to a network security group or load balancer using `azure network nic set`, such as in the following example:

```bash
azure network nic set --resource-group TestRG --name NIC1 \
    --network-security-group-name TestNSG
```

When creating the VM, you now specify multiple NICs. Rather using `--nic-name` to provide a single NIC, instead you use `--nic-names` and provide a comma-separated list of NICs. You also need to take care when you select the VM size. There are limits for the total number of NICs that you can add to a VM. Read more about [Linux VM sizes](virtual-machines-linux-sizes.md). The following example shows how to specify multiple NICs and then a VM size that supports using multiple NICs (`Standard_DS2_v2`):

```bash
azure vm create \            
    --resource-group TestRG \
    --name TestVM1 \
    --location WestUS \
    --os-type linux \
    --nic-names NIC1,NIC2 \
    --vm-size Standard_DS2_v2
    --storage-account-name teststorage \
    --image-urn UbuntuLTS \
    --admin-username ops \
    --ssh-publickey-file ~/.ssh/id_rsa.pub
```

## Creating multiple NICs using Resource Manager templates
Azure Resource Manager templates use declarative JSON files to define your environment. You can read an [overview of Azure Resource Manager](../resource-group-overview.md). Resource Manager templates provide a way to create multiple instances of a resource during deployment, such as creating multiple NICs. You use *copy* to specify the number of instances to create:

```bash
"copy": {
    "name": "multiplenics"
    "count": "[parameters('count')]"
}
```

Read more about [creating multiple instances using *copy*](../resource-group-create-multiple.md). 

You can also use a `copyIndex()` to then append a number to a resource name, which allows you to create `NIC1`, `NIC2`, etc. The following shows an example of appending the index value:

```bash
"name": "[concat('NIC-', copyIndex())]", 
```

You can read a complete example of [creating multiple NICs using Resource Manager templates](../virtual-network/virtual-network-deploy-multinic-arm-template.md).

## Next steps
Make sure to review [Linux VM sizes](virtual-machines-linux-sizes.md) when trying to creating a VM with multiple NICs. Pay attention to the maximum number of NICs each VM size supports. 

Remember that you cannot add additional NICs to an existing VM, you must create all the NICs when you deploy the VM. Take care when planning your deployments to make sure that you have all the required network connectivity from the outset.

