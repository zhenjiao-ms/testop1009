---
title: About VPN Gateway settings for virtual network gateways| Microsoft Azure
description: Learn about VPN Gateway settings for Azure Virtual Network.
services: vpn-gateway
documentationcenter: na
author: cherylmc
manager: carmonm
editor: ''
tags: azure-resource-manager,azure-service-management

ms.service: vpn-gateway
ms.devlang: na
ms.topic: article
ms.tgt_pltfrm: na
ms.workload: infrastructure-services
ms.date: 08/29/2016
ms.author: cherylmc

---
# About VPN Gateway settings
A VPN gateway connection solution relies on the configuration of multiple resources in order to send network traffic between virtual networks and on-premises locations. Each resource contains configurable settings. The combination of the resources and settings determines the connection outcome. 

The sections in this article discuss the resources and settings that relate to a VPN gateway. You may find it helpful to view the available configurations by using connection topology diagrams. You can find the descriptions and topology diagrams for each connection solution in the [About VPN Gateway](vpn-gateway-about-vpngateways.md) article. 

## <a name="gwtype"></a>Gateway types
The gateway type specifies how the gateway connects and is a required configuration setting for the Resource Manager deployment model. Each virtual network can only have one virtual network gateway of each type. The available values for `-GatewayType` are: 

* Vpn
* ExpressRoute

A VPN gateway requires the -GatewayType *Vpn*, as shown in the following PowerShell example for the Resource Manager deployment model. When you are creating a virtual network gateway, you must make sure that the gateway type is correct for your configuration. 

    New-AzureRmVirtualNetworkGateway -Name vnetgw1 -ResourceGroupName testrg `
    -Location 'West US' -IpConfigurations $gwipconfig -GatewayType Vpn `
    -VpnType RouteBased


## <a name="gwsku"></a>Gateway SKUs
When you create a VPN gateway, you need to specify the virtual network gateway SKU that you want to use. Gateway SKUs apply to both ExpressRoute and Vpn gateway types. Pricing does differ between gateway SKUs. For information about pricing, see [VPN Gateway Pricing](https://azure.microsoft.com/pricing/details/vpn-gateway/). For more information about ExpressRoute, see the [ExpressRoute Technical Overview](../expressroute/expressroute-introduction.md).

There are 3 VPN Gateway SKUs:

* Basic
* Standard
* HighPerformance

The following PowerShell example specifies the `-GatewaySku` as *Standard*.

    New-AzureRmVirtualNetworkGateway -Name vnetgw1 -ResourceGroupName testrg `
    -Location 'West US' -IpConfigurations $gwipconfig -GatewaySku Standard `
    -GatewayType Vpn -VpnType RouteBased


### <a name="aggthroughput"></a>Estimated aggregate throughput by SKU and gateway type
The following table shows the gateway types and the estimated aggregate throughput. This table applies to both the Resource Manager and classic deployment models.

[!INCLUDE [vpn-gateway-table-gwtype-aggthroughput](../../includes/vpn-gateway-table-gwtype-aggtput-include.md)]

## <a name="connectiontype"></a>Connection types
Each configuration requires a specific virtual network gateway connection type. The available Resource Manager PowerShell values for `-ConnectionType` are:

* IPsec
* Vnet2Vnet
* ExpressRoute
* VPNClient

In the following PowerShell example, we create a S2S connection that requires the connection type *IPsec*.

    New-AzureRmVirtualNetworkGatewayConnection -Name localtovon -ResourceGroupName testrg `
    -Location 'West US' -VirtualNetworkGateway1 $gateway1 -LocalNetworkGateway2 $local `
    -ConnectionType IPsec -RoutingWeight 10 -SharedKey 'abc123'


## <a name="vpntype"></a>VPN types
When you create the virtual network gateway for a VPN gateway configuration, you must specify a VPN type. The VPN type that you choose depends on the connection topology that you want to create. For example, a P2S connection requires a RouteBased VPN type. A VPN type can also depend on the hardware that you will be using. S2S configurations require a VPN device. Some VPN devices will only support a certain VPN type.

The VPN type you select must satisfy all of the connection requirements for the solution you want to create. For example, if you want to create a S2S VPN gateway connection and a P2S VPN gateway connection for the same virtual network, you would use VPN type *RouteBased* because P2S requires a RouteBased VPN type. You would also need to verify that your VPN device supported a RouteBased VPN connection. 

Once a virtual network gateway has been created, you can't change the VPN type. You have to delete the virtual network gateway and create a new one. 
There are two VPN types:

[!INCLUDE [vpn-gateway-vpntype](../../includes/vpn-gateway-vpntype-include.md)]

The following PowerShell example for the Resource Manager deployment model specifies the `-VpnType` as *RouteBased*. When you are creating a gateway, you must make sure that the -VpnType is correct for your configuration. 

    New-AzureRmVirtualNetworkGateway -Name vnetgw1 -ResourceGroupName testrg `
    -Location 'West US' -IpConfigurations $gwipconfig `
    -GatewayType Vpn -VpnType RouteBased

## <a name="requirements"></a>Gateway requirements
[!INCLUDE [vpn-gateway-table-requirements](../../includes/vpn-gateway-table-requirements-include.md)]

## <a name="gwsub"></a>Gateway subnet
To configure a virtual network gateway, you first need to create a gateway subnet for your VNet. The gateway subnet must be named *GatewaySubnet* to work properly. This name lets Azure know that this subnet should be used for the gateway. If you are using the classic portal, the gateway subnet is automatically named *Gateway* in the portal interface. This is specific to viewing the gateway subnet in the classic portal only. In this case, the subnet is actually created with the value *GatewaySubnet* and can be viewed this way in the Azure portal and in PowerShell.

The minimum size of your gateway subnet depends entirely on the configuration that you want to create. Although it is possible to create a gateway subnet as small as /29, we recommend that you create a gateway subnet of /28 or larger (/28, /27, /26, etc.). 

Creating a larger gateway size prevents you from running up against gateway size limitations. For example, you may have created a virtual network gateway with a gateway subnet size /29 for a S2S connection. You now want to configure a S2S/ExpressRoute coexist configuration. That configuration requires a gateway subnet minimum size /28. To create your configuration, you would have to modify the gateway subnet to accommodate the minimum requirement for the connection, which is /28.

The following Resource Manager PowerShell example shows a gateway subnet named GatewaySubnet. You can see the CIDR notation specifies a /27, which allows for enough IP addresses for most configurations that currently exist.

    Add-AzureRmVirtualNetworkSubnetConfig -Name 'GatewaySubnet' -AddressPrefix 10.0.3.0/27

> [!IMPORTANT]
> Verify that the gateway subnet does not have a Network Security Group (NSG) applied to it, as this may cause connections to fail.
> 
> 

## <a name="lng"></a>Local network gateways
When creating a VPN gateway solution, the local network gateway often represents your on-premises location. In the classic deployment model, the local network gateway was referred to as a Local Site. 

You give the local network gateway a name, the public IP address of the on-premises VPN device, and specify the address prefixes that are located on the on-premises location. Azure looks at the destination address prefixes for network traffic, consults the configuration that you have specified for your local network gateway, and routes packets accordingly. You also specify local network gateways for VNet-to-VNet configurations that use a VPN gateway connection.

The following Resource Manager PowerShell example creates a new local network gateway:

    New-AzureRmLocalNetworkGateway -Name LocalSite -ResourceGroupName testrg `
    -Location 'West US' -GatewayIpAddress '23.99.221.164' -AddressPrefix '10.5.51.0/24'

Sometimes you need to modify the local network gateway settings. For example, when you add or modify the address range, or if the IP address of the VPN device changes. For a classic VNet, you can change these settings in the classic portal on the Local Networks page. For Resource Manager, see [Modify local network gateway settings using PowerShell](vpn-gateway-modify-local-network-gateway.md).

## <a name="resources"></a>REST APIs and PowerShell cmdlets
For additional technical resources and specific syntax requirements when using REST APIs and PowerShell cmdlets for VPN Gateway configurations, see the following pages:

| **Classic** | **Resource Manager** |
| --- | --- |
| [PowerShell](https://msdn.microsoft.com/library/mt270335.aspx) |[PowerShell](https://msdn.microsoft.com/library/mt163510.aspx) |
| [REST API](https://msdn.microsoft.com/library/jj154113.aspx) |[REST API](https://msdn.microsoft.com/library/mt163859.aspx) |

## Next steps
See [About VPN Gateway](vpn-gateway-about-vpngateways.md) for more information about available connection configurations. 

