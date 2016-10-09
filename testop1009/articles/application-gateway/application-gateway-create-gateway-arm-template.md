
---
title: Create an application gateway by using Azure Resource Manager templates| Microsoft Azure
description: This page provides instructions to create an Azure application gateway by using the Azure Resource Manager template
documentationcenter: na
services: application-gateway
author: georgewallace
manager: carmonm
editor: tysonn

ms.service: application-gateway
ms.devlang: na
ms.topic: hero-article
ms.tgt_pltfrm: na
ms.workload: infrastructure-services
ms.date: 09/06/2016
ms.author: gwallace

---
# Create an application gateway by using the Azure Resource Manager template
Azure Application Gateway is a layer-7 load balancer. It provides failover, performance-routing HTTP requests between different servers, whether they are on the cloud or on-premises. Application Gateway has the following application delivery features: HTTP load balancing, cookie-based session affinity, and Secure Sockets Layer (SSL) offload.

> [!div class="op_single_selector"]
> * [Azure portal](application-gateway-create-gateway-portal.md)
> * [Azure Resource Manager PowerShell](application-gateway-create-gateway-arm.md)
> * [Azure Classic PowerShell](application-gateway-create-gateway.md)
> * [Azure Resource Manager template](application-gateway-create-gateway-arm-template.md)
> * [Azure CLI](application-gateway-create-gateway-cli.md)
> 
> 

You learn how to download and modify an existing Azure Resource Manager template from GitHub and deploy the template from GitHub, PowerShell, and the Azure CLI.

If you are simply deploying the Azure Resource Manager template directly from GitHub without any changes, skip to deploy a template from GitHub.

## Scenario
In this scenario you will:

* Create an application gateway with two instances.
* Create a virtual network named VirtualNetwork1 with a reserved CIDR block of 10.0.0.0/16.
* Create a subnet called Appgatewaysubnet that uses 10.0.0.0/28 as its CIDR block.
* Set up two previously configured back-end IPs for the web servers you want to load balance the traffic. In this template example, the back-end IPs are 10.0.1.10 and 10.0.1.11.

> [!NOTE]
> Those settings are the parameters for this template. To customize the template, you can change rules, the listener, and the SSL that opens the azuredeploy.json.
> 
> 

![Scenario](./media/application-gateway-create-gateway-arm-template/scenario-arm.png)

## Download and understand the Azure Resource Manager template
You can download the existing Azure Resource Manager template to create a virtual network and two subnets from GitHub, make any changes you might want, and reuse it. To do so, use the following steps:

1. Navigate to [Create Application Gateway](https://github.com/Azure/azure-quickstart-templates/tree/master/101-application-gateway-create).
2. Click **azuredeploy.json**, and then click **RAW**.
3. Save the file to a local folder on your computer.
4. If you are familiar with Azure Resource Manager templates, skip to step 7.
5. Open the file that you saved and look at the contents under **parameters** in line 5. Azure Resource Manager template parameters provide a placeholder for values that can be filled out during deployment.
   
   | Parameter | Description |
   | --- | --- |
   | **location** |Azure region where the application gateway is created |
   | **VirtualNetwork1** |Name for the new virtual network |
   | **addressPrefix** |Address space for the virtual network, in CIDR format |
   | **ApplicationGatewaysubnet** |Name for the application gateway subnet |
   | **subnetPrefix** |CIDR block for the application gateway subnet |
   | **skuname** |SKU instance size |
   | **capacity** |Number of instances |
   | **backendaddress1** |IP address of the first web server |
   | **backendaddress2** |IP address of the second web server |

    >[AZURE.IMPORTANT] Azure Resource Manager templates maintained in GitHub can change over time. Make sure that you check the template before using it.

1. Check the content under **resources** and notice the following:
   
   * **type**. Type of resource being created by the template. In this case, the type is **Microsoft.Network/applicationGateways**, which represents an application gateway.
   * **name**. Name for the resource. Notice the use of **[parameters('applicationGatewayName')]**, which means that the name is provided as input by you or by a parameter file during deployment.
   * **properties**. List of properties for the resource. This template uses the virtual network and public IP address during application gateway creation.
2. Navigate back to [https://github.com/Azure/azure-quickstart-templates/blob/master/101-application-gateway-create/](https://github.com/Azure/azure-quickstart-templates/blob/master/101-application-gateway-create).
3. Click **azuredeploy-paremeters.json**, and then click **RAW**.
4. Save the file to a local folder on your computer.
5. Open the file that you saved and edit the values for the parameters. Use the following values to deploy the application gateway described in our scenario.
   
       {
       "$schema": "http://schema.management.azure.com/schemas/2015-01-01/deploymentParameters.json#",
       {
       "location" : {
       "value" : "West US"
       },
       "addressPrefix": {
       "value": "10.0.0.0/16"
       },
       "subnetPrefix": {
       "value": "10.0.0.0/24"
       },
       "skuName": {
       "value": "Standard_Small"
       },
       "capacity": {
       "value": 2
       },
       "backendIpAddress1": {
       "value": "10.0.1.10"
       },
       "backendIpAddress2": {
       "value": "10.0.1.11"
       }
       }
6. Save the file. You can test the JSON template and parameter template by using online JSON validation tools like [JSlint.com](http://www.jslint.com/).

## Deploy the Azure Resource Manager template by using PowerShell
If you have never used Azure PowerShell, see [How to install and configure Azure PowerShell](../powershell-install-configure.md) and follow the instructions to sign into Azure and select your subscription.

### Step 1
    Login-AzureRmAccount

### Step 2
Check the subscriptions for the account.

    Get-AzureRmSubscription

You are prompted to authenticate with your credentials.<BR>

### Step 3
Choose which of your Azure subscriptions to use. <BR>

    Select-AzureRmSubscription -Subscriptionid "GUID of subscription"


### Step 4
If needed, create a resource group by using the **New-AzureResourceGroup** cmdlet. In the following example, you create a resource group called AppgatewayRG in East US location.

    New-AzureRmResourceGroup -Name AppgatewayRG -Location "East US"

Run the **New-AzureRmResourceGroupDeployment** cmdlet to deploy the new virtual network by using the preceding template and parameter files you downloaded and modified.

    New-AzureRmResourceGroupDeployment -Name TestAppgatewayDeployment -ResourceGroupName AppgatewayRG `
         -TemplateFile C:\ARM\azuredeploy.json -TemplateParameterFile C:\ARM\azuredeploy-parameters.json

## Deploy the Azure Resource Manager template by using the Azure CLI
To deploy the Azure Resource Manager template you downloaded by using Azure CLI, follow the steps below:

### Step 1
If you have never used Azure CLI, see [Install and configure the Azure CLI](../xplat-cli-install.md) and follow the instructions up to the point where you select your Azure account and subscription.

### Step 2
Run the **azure config mode** command to switch to Resource Manager mode, as shown below.

    azure config mode arm

Here is the expected output for the command above:

    info:    New mode is arm

### Step 3
If necessary, run the **azure group create** command to create a new resource group, as shown below. Notice the output of the command. The list shown after the output explains the parameters used. For more information about resource groups, visit [Azure Resource Manager overview](../resource-group-overview.md).

    azure group create -n appgatewayRG -l eastus

**-n (or --name)**. Name for the new resource group. For our scenario, it's *appgatewayRG*.

**-l (or --location)**. Azure region where the new resource group is created. For our scenario, it's *eastus*.

### Step 4
Run the **azure group deployment create** cmdlet to deploy the new virtual network by using the template and parameter files you downloaded and modified above. The list shown after the output explains the parameters used.

    azure group deployment create -g appgatewayRG -n TestAppgatewayDeployment -f C:\ARM\azuredeploy.json -e C:\ARM\azuredeploy-parameters.json

## Deploy the Azure Resource Manager template by using click-to-deploy
Click-to-deploy is another way to use Azure Resource Manager templates. It's an easy way to use templates with the Azure portal.

### Step 1
Go to [Create an application gateway with public IP](https://azure.microsoft.com/documentation/templates/101-application-gateway-public-ip/).

### Step 2
Click **Deploy to Azure**.

![Deploy to Azure](./media/application-gateway-create-gateway-arm-template/deploytoazure.png)

### Step 3
Fill out the parameters for the deployment template on the portal and click **OK**.

![Parameters](./media/application-gateway-create-gateway-arm-template/ibiza1.png)

### Step 4
Select **Legal terms** and click **Buy**.

### Step 5
On the Custom deployment blade, click **Create**.

## Next steps
If you want to configure SSL offload, see [Configure an application gateway for SSL offload](application-gateway-ssl.md).

If you want to configure an application gateway to use with an internal load balancer, see [Create an application gateway with an internal load balancer (ILB)](application-gateway-ilb.md).

If you want more information about load balancing options in general, see:

* [Azure Load Balancer](https://azure.microsoft.com/documentation/services/load-balancer/)
* [Azure Traffic Manager](https://azure.microsoft.com/documentation/services/traffic-manager/)

