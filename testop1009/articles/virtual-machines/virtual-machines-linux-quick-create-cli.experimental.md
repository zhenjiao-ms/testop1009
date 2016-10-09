---
title: Create a Linux VM on Azure using the CLI | Microsoft Azure
description: Create a Linux VM on Azure using the CLI.
keywords: microsoft docs, Azure documentation
ms.service: virtual-machines-linux
ms.devlang: NA
ms.topic: hero-article
ms.tgt_pltfrm: vm-linux
ms.workload: infrastructure
ms.date: 05/03/2016
author: vlivech
ms.suite: azure
experiment_id: rasquill-09-24-2016-1600
---


# Create a Linux VM on Azure by using the CLI
This article shows how to quickly deploy a Linux virtual machine (VM) on Azure by using the [az vm create](https://stage.docs.microsoft.com/en-us/cli/azure/vm?branch=master#create) command in the Azure command-line interface (CLI). To create a VM, you'll need: 

* an Azure account ([get a free trial](https://azure.microsoft.com/pricing/free-trial/))
* the [Azure CLI v. 2.0](https://github.com/Azure/azure-cli#installation) installed
* to be logged in to your Azure account (type [az login](https://stage.docs.microsoft.com/en-us/cli/azure/?branch=master#login))

(You can also quickly deploy a Linux VM by using the [Azure portal](virtual-machines-linux-quick-create-portal.md).)

The following example shows how to deploy a Debian VM and attach your Secure Shell (SSH) key (your arguments might be different).

## Find an image

You can find other images by using the [az vm image list](https://stage.docs.microsoft.com/en-us/cli/azure/vm/image?branch=master#list) command. The following example shows `jq` writing the result in an easy-to-read list. 

```azurecli
az vm image list --query '[].urn' --output tsv
```

The result is:

```
You are viewing an offline list of images, use --all to retrieve an up-to-date list
MicrosoftWindowsServer:WindowsServer:2012-R2-Datacenter:latest
MicrosoftWindowsServer:WindowsServer:2008-R2-SP1:latest
MicrosoftWindowsServer:WindowsServer:2012-Datacenter:latest
Canonical:UbuntuServer:14.04.4-LTS:latest
OpenLogic:CentOS:7.2:latest
SUSE:openSUSE:13.2:latest
RedHat:RHEL:7.2:latest
SUSE:SLES:12-SP1:latest
credativ:Debian:8:latest
CoreOS:CoreOS:Stable:latest
```

## Create a resource group

First, type [az resource group create](https://stage.docs.microsoft.com/en-us/cli/azure/resource/group#create) to create your resource group that contains all deployed resources:

```azurecli
az resource group create -l westus -n newvirtualmachine 
```

The output looks like the following (you can choose a different `--output` option if you wish):

```json
{
  "id": "/subscriptions/<guid>/resourceGroups/newvirtualmachine",
  "location": "westus",
  "name": "newvirtualmachine",
  "properties": {
    "provisioningState": "Succeeded"
  },
  "tags": null
}
```

## Create your VM using the latest Debian image

Now you can create your VM and its environment. Remember to replace the `----public-ip-address-dns-name` value with a unique one; the one below may already be taken.

```azurecli
az vm create \
--image credativ:Debian:8:latest \
--admin-username ops \
--ssh-key-value ~/.ssh/id_rsa.pub \
--public-ip-address-dns-name azurecli2 \
--resource-group newvirtualmachine \
--location westus \
--name mynewvm
```


The output looks like the following. Note either the `publicIpAddress` or the `fqdn` value to **ssh** into your VM.


```json
{
  "fqdn": "azurecli2.westus.cloudapp.azure.com",
  "id": "/subscriptions/<guid>/resourceGroups/newvirtualmachine/providers/Microsoft.Compute/virtualMachines/mynewvm",
  "macAddress": "00-0D-3A-32-05-07",
  "privateIpAddress": "10.0.0.4",
  "publicIpAddress": "40.112.217.29",
  "resourceGroup": "newvirtualmachine"
}
```

Log in to your VM by using the public IP address listed in the output. You can also use the fully qualified domain name (FQDN) that's listed.

```
ssh ops@azurecli2.westus.cloudapp.azure.com
```

You should expect to see something like the following output, depending on the distributed you chose:

```
The authenticity of host 'azurecli2.westus.cloudapp.azure.com (40.112.217.29)' can't be established.
RSA key fingerprint is SHA256:xbVC//lciRvKild64lvup2qIRimr/GB8C43j0tSHWnY.
Are you sure you want to continue connecting (yes/no)? yes
Warning: Permanently added 'azurecli2.westus.cloudapp.azure.com,40.112.217.29' (RSA) to the list of known hosts.

The programs included with the Debian GNU/Linux system are free software;
the exact distribution terms for each program are described in the
individual files in /usr/share/doc/*/copyright.

Debian GNU/Linux comes with ABSOLUTELY NO WARRANTY, to the extent
permitted by applicable law.
ops@mynewvm:~$ ls /
bin  boot  dev  etc  home  initrd.img  lib  lib64  lost+found  media  mnt  opt  proc  root  run  sbin  srv  sys  tmp  usr  var  vmlinuz
```


## Next steps
The `az vm create` command is the way to quickly deploy a VM so you can log in to a bash shell and get working. However, using `az vm create` does not give you extensive control nor does it enable you to create a more complex environment.  To deploy a Linux VM that's customized for your infrastructure, you can follow any of these articles:


* [Use an Azure Resource Manager template to create a specific deployment](virtual-machines-linux-cli-deploy-templates.md)
* [Create your own custom environment for a Linux VM using Azure CLI commands directly](virtual-machines-linux-create-cli-complete.md)
* [Create an SSH Secured Linux VM on Azure using templates](virtual-machines-linux-create-ssh-secured-vm-from-template.md)

You can also [use the `docker-machine` Azure driver with various commands to quickly create a Linux VM as a docker host](virtual-machines-linux-docker-machine.md) as well, and if you're using Java, try the [create()](https://stage.docs.microsoft.com/en-us/java/api/com.microsoft.azure.management.compute._virtual_machine?branch=master) method.


