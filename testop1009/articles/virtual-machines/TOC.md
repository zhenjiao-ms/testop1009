# Overview
## [Linux and Azure](virtual-machines-linux-azure-overview.md)
## [VMs](virtual-machines-linux-azure-overview.md)
### [Sizes](virtual-machines-linux-sizes.md)
### [Compute-intensive sizes](virtual-machines-linux-a8-a9-a10-a11-specs.md)
### [Disks and VHDs](virtual-machines-linux-about-disks-vhds.md)
### [Availability](virtual-machines-linux-manage-availability.md)
### [Find VM images](virtual-machines-linux-cli-ps-findimage.md)
### [Create VMs](virtual-machines-linux-creation-choices.md)
### [Multiple VMs and clusters](../../articles/virtual-machine-scale-sets/virtual-machine-scale-sets-linux-create-cli.md)
### [Azure-endorsed images](virtual-machines-linux-endorsed-distros.md)
### [Custom images](virtual-machines-linux-create-upload-generic.md)
### [Using root privileges](virtual-machines-linux-use-root-privileges.md)
### [VMs and Containers](virtual-machines-linux-containers.md)
## [VM Extensions](virtual-machines-linux-extensions-features.md)
### [The CustomScriptExtension and Azure templates](virtual-machines-linux-extensions-customscript.md)
### [The VM Access extension](virtual-machines-linux-using-vmaccess-extension.md)
### [Monitoring your VM](virtual-machines-linux-vm-monitoring.md)
### [Using templates with VM extensions](virtual-machines-linux-extensions-authoring-templates.md)
### [Configuration samples](virtual-machines-linux-extensions-configuration-samples.md)

## Networking
### [Virtual Network Overview](../virtual-network/virtual-networks-overview?toc=%2fazure%2farticles%2fvirtual-machines%2ftoc.json)

## Storage
### [Use Azure Files](https://stage.docs.microsoft.com/en-us/azure/articles/storage/storage-how-to-use-files-linux?toc=%2fazure%2farticles%2fvirtual-machines%2ftoc.json)
### [Configure Software RAID](virtual-machines-linux-configure-raid.md)
### [Configure LVM](virtual-machines-linux-configure-lvm.md)

## Azure Resources
### [How to Tag a VM in Azure](virtual-machines-linux-tag.md)
## Prepping Images
### [Azure Linux Agent User Guide](virtual-machines-linux-agent-user-guide.md)
### [Capture a VM](virtual-machines-linux-capture-image.md)
### [App frameworks using Azure templates](virtual-machines-linux-app-frameworks.md)
### [Deploy Azure templates with the CLI](virtual-machines-linux-cli-deploy-templates.md)
### [CentOS](virtual-machines-linux-create-upload-centos.md)
### [Ubuntu](virtual-machines-linux-create-upload-ubuntu.md)
### [Debian](virtual-machines-linux-debian-create-upload-vhd.md)
### [RedHat](virtual-machines-linux-redhat-create-upload-vhd.md)
### [Red Hat Enterprise Linux Update infrastructure](virtual-machines-linux-update-infrastructure-redhat.md)
### [Create SSH keys on Linux and Mac](virtual-machines-linux-mac-create-ssh-keys.md)
# Get Started
## [Get free account](https://azure.microsoft.com/pricing/free-trial/)
## [Install Azure CLI](../xplat-cli-install.md)
## [Create VM using the CLI](virtual-machines-linux-quick-create-cli.md)
## [Create VM using the portal](virtual-machines-linux-quick-create-portal.md)

# Plan and Design
## [Azure Deployment Models](virtual-machines-linux-compare-deployment-models.md)
## [Infrastructure services implementation guidelines](virtual-machines-linux-infrastructure-service-guidelines.md)
## [Planned maintenance for VMs](virtual-machines-linux-planned-maintenance.md)
## [Planned maintenance schedule for VMs](virtual-machines-linux-planned-maintenance-schedule.md)
## Management and Migration
### [Azure Disk Encryption](../security/azure-security-disk-encryption?toc=%2fazure%2farticles%2fvirtual-machines%2ftoc.json)
### [Migrate from Classic to Resource Deployments](virtual-machines-linux-cli-migration-classic-resource-manager.md)
### [Migrate from Classic deployments deep-dive](virtual-machines-linux-migration-classic-resource-manager-deep-dive.md)

## Best Practices
### [Running Single VMs](../guidance/guidance-compute-single-vm-linux?toc=%2fazure%2farticles%2fvirtual-machines%2ftoc.json) 

# How to
## Compute
### [Add a disk](virtual-machines-linux-add-disk.md)
### [Add disk using the portal](virtual-machines-linux-attach-disk-portal.md)
### [Scale multiple VMs with Scale Sets](virtual-machines-linux-cli-vmss-create.md)
### [Create VM with custom environment](virtual-machines-linux-create-cli-complete.md)
### [Create VM from an Azure template](virtual-machines-linux-create-ssh-secured-vm-from-template.md)
### [Use docker-machine with Azure driver](virtual-machines-linux-docker-machine.md)
### [Copy a VM](virtual-machines-linux-copy-vm.md)
### [Capture a VM](virtual-machines-linux-capture-image.md)
### [Using cloud-init](virtual-machines-linux-using-cloud-init.md)
### [Create SSH keys on Linux and Mac](virtual-machines-linux-mac-create-ssh-keys.md)
### [Resetting SSH access, managing users, and checking disks](virtual-machines-linux-using-vmaccess-extension.md)
### [Use a unique ID for your Linux VM](virtual-machines-linux-unique-vm-id.md)

## Networking
### [Virtual Network Overview](../virtual-network/virtual-networks-overview?toc=%2fazure%2farticles%2fvirtual-machines%2ftoc.json)
### [Create a load balancer](../load-balancer/load-balancer-get-started-internet-arm-ps?toc=%2fazure%2farticles%2fvirtual-machines%2ftoc.json)
### [Create User Defined Routes using the Azure CLI](../virtual-network/virtual-network-create-udr-arm-cli?toc=%2fazure%2farticles%2fvirtual-machines%2ftoc.json)
### [Create NSGs using the Azure CLI](../virtual-network/virtual-networks-create-nsg-arm-cli?toc=%2fazure%2farticles%2fvirtual-machines%2ftoc.json)
### [Create VNETs using the Azure CLI](..virtual-network/virtual-networks-create-vnet-arm-cli?toc=%2fazure%2farticles%2fvirtual-machines%2ftoc.json)
### [Create a Static public IP](../virtual-network/virtual-network-deploy-static-pip-arm-cli?toc=%2fazure%2farticles%2fvirtual-machines%2ftoc.json)

## Storage
### [Use Azure Files](../storage/storage-how-to-use-files-linux?toc=%2fazure%2farticles%2fvirtual-machines%2ftoc.json)
### [Configure Software RAID](virtual-machines-linux-configure-raid.md)
### [Configure LVM](virtual-machines-linux-configure-lvm.md)


## [Create Docker Hosts in Azure with docker-machine](../vs-azure-tools-docker-machine-azure-config?toc=%2fazure%2farticles%2fdotnet%2ftoc.json&branch=master)

# Workloads
## [SAP on Azure](virtual-machines-linux-sap-get-started?toc=%2fazure%2farticles%2fsap%2ftoc.json)


# Reference
## [Azure CLI](https://stage.docs.microsoft.com/en-us/cli/azure/vm?branch=master)
## [Java SDK](https://stage.docs.microsoft.com/en-us/java/api/com.microsoft.azure.management.compute._virtual_machine?branch=master)
## [Compute REST API](https://stage.docs.microsoft.com/en-us/rest/azure/api/compute/2016-03-30?branch=master#Virtual-Machines)
## [Network REST API](https://stage.docs.microsoft.com/en-us/rest/azure/api/network/2016-09-01?branch=master#)
## [Storage REST API ](https://stage.docs.microsoft.com/en-us/rest/azure/api/storage/2016-01-01?branch=master)
## [Community templates](https://azure.microsoft.com/documentation/templates/)

# Related
# VMs (Classic)
## [Table of contents](virtual-machines-linux-opensource-links.md)
## [Searchable article index](https://azure.microsoft.com/documentation/articles/?product=virtual-machines-linux&tag=azure-service-management)

# Resources
## Troubleshooting
### [Troubleshoot allocation failures](virtual-machines-linux-allocation-failure.md)
### [Troubleshooting Azure VM Extension failures](virtual-machines-linux-extensions-troubleshoot.md)
### [Troubleshoot Access to Applications](virtual-machines-linux-troubleshoot-app-connection.md)
### [Troubleshoot Secure Shell (SSH) connections to a Linux-based VM](virtual-machines-linux-troubleshoot-ssh-connection.md)

