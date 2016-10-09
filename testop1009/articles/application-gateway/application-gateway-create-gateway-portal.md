---
title: Create an application gateway using the portal | Microsoft Azure
description: Learn how to create an Application Gateway by using the portal
services: application-gateway
documentationcenter: na
author: georgewallace
manager: carmonm
editor: ''
tags: azure-resource-manager

ms.service: application-gateway
ms.devlang: na
ms.topic: article
ms.tgt_pltfrm: na
ms.workload: infrastructure-services
ms.date: 09/06/2016
ms.author: gwallace

---
# Create an application gateway by using the portal
Azure Application Gateway is a layer-7 load balancer. It provides failover, performance-routing HTTP requests between different servers, whether they are on the cloud or on-premises. 
Application provides many Application Delivery Controller (ADC) features including HTTP load balancing, cookie-based session affinity, Secure Sockets Layer (SSL) offload, custom health probes, support for multi-site, and many others. 
To find a complete list of supported features visit [Application Gateway Overview](application-gateway-introduction.md)

> [!div class="op_single_selector"]
> * [Azure portal](application-gateway-create-gateway-portal.md)
> * [Azure Resource Manager PowerShell](application-gateway-create-gateway-arm.md)
> * [Azure Classic PowerShell](application-gateway-create-gateway.md)
> * [Azure Resource Manager template](application-gateway-create-gateway-arm-template.md)
> * [Azure CLI](application-gateway-create-gateway-cli.md)
> 
> 

## Scenario
In this scenario, you learn how to create an application gateway using the Azure portal.

This scenario will:

* Create a medium application gateway with two instances.
* Create a virtual network named AdatumAppGatewayVNET with a reserved CIDR block of 10.0.0.0/16.
* Create a subnet called Appgatewaysubnet that uses 10.0.0.0/28 as its CIDR block.
* Configure a certificate for SSL offload.

![Scenario example][scenario]

> [!NOTE]
> Additional configuration of the application gateway, including custom health probes, backend pool addresses, and additional rules are configured after the application gateway is configured and not during initial deployment.
> 
> 

## Before you begin
Azure Application Gateway requires its own subnet. When creating a virtual network, ensure that you leave enough address space to have multiple subnets. Once you deploy an application gateway to a subnet,
only additional application gateways are able to be added to the subnet.

## Create the Application Gateway
### Step 1
Navigate to the Azure portal, click **New** > **Networking** > **Application Gateway**

![Creating Application Gateway][1]

### Step 2
Next fill out the basic information about the application gateway. When complete click **OK**

The information needed for the basic settings is:

* **Name** - The name for the application gateway.
* **SKU size** - This setting is the size of the application gateway, available options are (Small, Medium, and Large).
* **Instance count** - The number of instances, this value should be a number between 2 and 10.
* **Resource group** - The resource group to hold the application gateway, it can be an existing resource group or a new one.
* **Location** - The region for the application gateway, it is the same location at the resource group. *The location is important as the virtual network and public IP must be in the same location as the gateway*.

![blade showing basic settings][2]

> [!NOTE]
> An instance count of 1 can be chosen for testing purposes. It is important to know that any instance count under two instances is not covered by the SLA and are therefore not recommended. Small gateways are to be used for dev test and not for production purposes.
> 
> 

### Step 3
Once the basic settings are defined, the next step is to define the virtual network to be used. The virtual network houses the application that the application gateway does load balancing for.

Click **Choose a virtual network** to configure the virtual network.

![blade showing settings for application gateway][3]

### Step 4
In the *Choose Virtual Network* blade, click **Create New**

While not explained in this scenario, an existing Virtual Network could be selected at this point.  If an existing virtual network is used, it is important to know that the virtual network needs an empty subnet or a subnet of only application gateway resources in order to be used.

![choose virtual network blade][4]

### Step 5
Fill out the network information in the **Create Virtual Network** blade as described in the preceding [Scenario](#scenario) description.

![Create virtual network blade with information entered][5]

### Step 6
Once the virtual network is created, the next step is to define the front-end IP for the application gateway. At this point, the choice is between a public 
or a private IP address for the front-end. The choice depends on whether the application is internet facing or internal only. This scenario assumes 
using a public IP address. To choose a private IP address, the **Private** button can be clicked. An automatically assigned IP address is chosen or you 
can click the **Choose a specific private IP address** checkbox to enter one manually.

### Step 7
Click **Choose a public IP address**. If an existing public IP address is available it can be chosen at this point, in this scenario you create a new public IP address. Click **Create new**

![Choose public IP address blade][6]

### Step 8
Next give the public IP address a friendly name and click **OK**

![Create public IP Address blade][7]

### Step 9
The last setting to configure when creating an application gateway is the listener configuration.  If **http** is used, nothing is left to configure and **OK** can be clicked. To use **https**
further configuration is required.

To use **https**, a certificate is required. The private key of the certificate is needed so a .pfx export of the certificate needs to be provided and the password for the file.

![blank Listener Configuration section on Settings blade][8]

### Step 10
Click **HTTPS**, click the **folder** icon next to the **Upload PFX certificate** textbox.
Navigate to the .pfx certificate file on your file system. Once it is selected, give the certificate a friendly name and type the password for the .pfx file.

Once complete click **OK** to review the settings for the Application Gateway.

![Listener Configuration section on Settings blade][9]

### Step 11
Review the Summary page and click **OK**.  Now the application gateway is queued up and created.

### Step 12
Once the application gateway has been created, navigate to it in the portal to continue configuration of the application gateway.

![Application Gateway resource view][10]

These steps create a basic application gateway with default settings for the listener, backend pool, backend http settings, and rules. You can modify these settings to suit your deployment once the provisioning is successful

## Next steps
Learn how to create custom health probes by visiting [Create a custom health probe](application-gateway-create-probe-portal.md)

Learn how to configure SSL Offloading and take the costly SSL decryption off your web servers by visiting [Configure SSL Offload](application-gateway-ssl-portal.md)

<!--Image references-->
[1]: ./media/application-gateway-create-gateway-portal/figure1.png
[2]: ./media/application-gateway-create-gateway-portal/figure2.png
[3]: ./media/application-gateway-create-gateway-portal/figure3.png
[4]: ./media/application-gateway-create-gateway-portal/figure4.png
[5]: ./media/application-gateway-create-gateway-portal/figure5.png
[6]: ./media/application-gateway-create-gateway-portal/figure6.png
[7]: ./media/application-gateway-create-gateway-portal/figure7.png
[8]: ./media/application-gateway-create-gateway-portal/figure8.png
[9]: ./media/application-gateway-create-gateway-portal/figure9.png
[10]: ./media/application-gateway-create-gateway-portal/figure10.png
[scenario]: ./media/application-gateway-create-gateway-portal/scenario.png