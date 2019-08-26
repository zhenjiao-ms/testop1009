---
title: Introduction to Application Gateway | Microsoft Azure
description: This page provides an overview of the Application Gateway service for layer-7 load balancing, including gateway sizes, HTTP load balancing, cookie-based session affinity, and SSL offload.
documentationcenter: na
services: application-gateway
author: georgewallace
manager: carmonm
editor: tysonn

ms.service: application-gateway
ms.devlang: na
ms.topic: article
ms.tgt_pltfrm: na
ms.workload: infrastructure-services
ms.date: 09/06/2016
ms.author: gwallace

---
# Application Gateway overview
Microsoft Azure Application Gateway provides an Azure-managed HTTP load-balancing service based on layer-7 load balancing. In simple terms it works by accepting traffic and based on rules that are defined with it, routes the traffic to the appropriate back-end instances.

Application load balancing enables IT administrators and developers to create routing rules for network traffic based on the HTTP protocol.  The Application Gateway service is highly available and metered. For the SLA and pricing, refer to the [SLA](https://azure.microsoft.com/support/legal/sla/) and [Pricing](https://azure.microsoft.com/pricing/details/application-gateway/) pages.

Application Gateway currently supports layer-7 application delivery with the following features:

* **HTTP load balancing** - The primary feature of Application gateway is to provide load balancing. Load balancing is done at Layer 7 and is used for HTTP traffic only.
* **Cookie-based session affinity** - This feature is useful when you want to keep a user session on the same back-end. By using cookies, the Application Gateway is able to direct subsequent traffic from a user session to the same back-end for processing. This feature is important in cases where something is saved locally on the back-end server for a user session.
* **[Secure Sockets Layer (SSL) offload](application-gateway-ssl-arm.md)** - This feature takes the costly task of decrypting HTTPS traffic off your web servers. By terminating the SSL connection at the Application Gateway and forwarding the request to server un-encrypted, the web server is unburdened by the decryption.  Application Gateway re-encrypts the response before sending it back the to client. This feature is useful in scenarios where the back-end is located in the same secured virtual network as the Application Gateway in Azure.
* **[URL-based content routing](application-gateway-url-route-overview.md)** - This feature provides the capability to use different back-end servers for different traffic. Traffic for a folder on the web server or for a CDN could be routed to a different back-end, reducing unneeded load on backends that don't server specific content.
* **[Multi-site routing](application-gateway-multi-site-overview.md)** - Application gateway allows for you to consolidate up to 20 websites on a single application gateway.
* **[Websocket support](application-gateway-websocket.md)** - Another great feature of Application Gateway is the native support for Websocket.

## HTTP layer 7 load balancing
The Application Gateway applies the routing rules to HTTP traffic, providing layer 7 (HTTP) load balancing. When you create an application gateway, an endpoint (VIP) is associated and used as public IP for ingress network traffic. 
Azure provides layer 4 load balancing through Azure load balancer working at the transport level (TCP/UDP) and having all incoming network traffic being load balanced to the Application Gateway service. 
The Application Gateway routes the HTTP traffic based on its configuration whether it's a virtual machine, cloud service, web app, or an external IP address.

HTTP layer 7 load balancing is useful for:

* Applications that require requests from the same user/client session to reach the same back-end virtual machine. Examples of these applications would be shopping cart apps and web mail servers.
* Applications that want to free web server farms from SSL termination overhead.
* Applications, such as a content delivery network, that requires multiple HTTP requests on the same long-running TCP connection to be routed or load balanced to different back-end servers.
* Applications that support websocket traffic, but still have an http endpoint for monitoring.

[!INCLUDE [load-balancer-compare-tm-ag-lb-include.md](../../includes/load-balancer-compare-tm-ag-lb-include.md)]

## Gateway sizes and instances
Application Gateway is currently offered in three sizes: Small, Medium, and Large. Small instance sizes are intended for development and testing scenarios.

You can create up to 50 application gateways per subscription, and each application gateway can have up to 10 instances each. Application Gateway load balancing as an Azure-managed service allows the provisioning of a layer-7 load balancer behind the Azure software load balancer.

The following table shows an average performance throughput for each application gateway instance:

| Back-end page response | Small | Medium | Large |
| --- | --- | --- | --- |
| 6 K |7.5 Mbps |13 Mbps |50 Mbps |
| 100 K |35 Mbps |100 Mbps |200 Mbps |

> [!NOTE]
> These values are approximate values for an application gateway throughput. The actual throughput depends on various environment details, such as average page size, location of back-end instances, and processing time to serve a page.
> 
> 

## Health monitoring
Azure Application Gateway automatically monitors the health of the back-end instances through basic or custom health probes. For more information, see [Application Gateway health monitoring overview](application-gateway-probe-overview.md).

## Configuring and managing
For its endpoint application gateway can have a public IP, private IP, or both when it is configured. Application Gateway is configured inside a virtual network in its own subnet. The subnet created or used for application gateway cannot contain any other types of resources, the only resources that are allowed in the subnet are other application gateways.

You can create and manage an application gateway by using REST APIs, PowerShell cmdlets, Azure CLI, or [Azure portal](https://portal.azure.com/).

## Next steps
After learning about Application gateway, you can [create an application gateway](application-gateway-create-gateway-portal.md) or you can [create an application gateway SSL offload](application-gateway-ssl-arm.md) to load-balance HTTPS connections.

To learn how to create an application gateway using URL-based content routing, go to [Create an application gateway using URL-based routing](application-gateway-create-url-route-arm-ps.md) for more information.

