---
title: Configure Load Balancer TCP idle timeout | Microsoft Azure
description: Configure Load Balancer TCP idle timeout
services: load-balancer
documentationcenter: na
author: sdwheeler
manager: carmonm
editor: ''

ms.service: load-balancer
ms.devlang: na
ms.topic: article
ms.tgt_pltfrm: na
ms.workload: infrastructure-services
ms.date: 03/03/2016
ms.author: sewhee

---
# Change TCP idle timeout settings for Load Balancer
In its default configuration, Azure Load Balancer has an idle timeout setting of 4 minutes.

This means that if a period of inactivity is longer than the timeout value, there's no guarantee that the TCP or HTTP session between the client and your cloud service still exists.

When the connection is closed, your client application will get an error message like "The underlying connection was closed: A connection that was expected to be kept alive was closed by the server."

A common practice to keep the connection active for a longer period is to use a TCP keep-alive. (You can find [.NET examples](https://msdn.microsoft.com/library/system.net.servicepoint.settcpkeepalive.aspx).) Packets are sent when no activity is detected on the connection. This network activity ensures that the idle timeout value is never reached and the connection is maintained for a long period.

To avoid losing the connection, you must configure the TCP keep-alive with an interval less than the idle timeout setting or increase the idle timeout value.

Although a TCP keep-alive works well for scenarios where a battery is not a constraint, we generally don't recommend it for mobile applications. Using a TCP keep-alive from a mobile application will likely drain the device battery faster.

To support such scenarios, we've added support for a configurable idle timeout. You can now set it for a duration of 4 to 30 minutes. This setting works for inbound connections only.

![TCP timeout](./media/load-balancer-tcp-idle-timeout/image1.png)

The following sections describe how to change idle timeout settings in virtual machines and cloud services.

> [!NOTE]
> To support the configuration of these settings, ensure that you have installed the latest Azure PowerShell package.
> 
> 

## Configure the TCP timeout for your instance-level public IP to 15 minutes
    Set-AzurePublicIP -PublicIPName webip -VM MyVM -IdleTimeoutInMinutes 15

`IdleTimeoutInMinutes` is optional. If it isn't set, the default timeout is 4 minutes.

> [!NOTE]
> The acceptable timeout range is 4 to 30 minutes.
> 
> 

## Set the idle timeout when creating an Azure endpoint on a virtual machine
Change the timeout setting for an endpoint:

    Get-AzureVM -ServiceName "mySvc" -Name "MyVM1" | Add-AzureEndpoint -Name "HttpIn" -Protocol "tcp" -PublicPort 80 -LocalPort 8080 -IdleTimeoutInMinutes 15| Update-AzureVM

Retrieve your idle timeout configuration:

    PS C:\> Get-AzureVM -ServiceName "MyService" -Name "MyVM" | Get-AzureEndpoint
    VERBOSE: 6:43:50 PM - Completed Operation: Get Deployment
    LBSetName : MyLoadBalancedSet
    LocalPort : 80
    Name : HTTP
    Port : 80
    Protocol : tcp
    Vip : 65.52.xxx.xxx
    ProbePath :
    ProbePort : 80
    ProbeProtocol : tcp
    ProbeIntervalInSeconds : 15
    ProbeTimeoutInSeconds : 31
    EnableDirectServerReturn : False
    Acl : {}
    InternalLoadBalancerName :
    IdleTimeoutInMinutes : 15

## Set the TCP timeout on a load-balanced endpoint set
If endpoints are part of a load-balanced endpoint set, the TCP timeout must be set on the load-balanced endpoint set:

    Set-AzureLoadBalancedEndpoint -ServiceName "MyService" -LBSetName "LBSet1" -Protocol tcp -LocalPort 80 -ProbeProtocolTCP -ProbePort 8080 -IdleTimeoutInMinutes 15

## Change timeout settings for cloud services
You can use the Azure SDK for .NET 2.4 to update your cloud service.

You make endpoint settings for cloud services in the .csdef file. Updating the TCP timeout for deployment of a cloud service requires a deployment upgrade. An exception is if the TCP timeout is specified only for a public IP. Public IP settings are in the .cscfg file, and you can update them through deployment update and upgrade.

The .csdef changes for endpoint settings are:

    <WorkerRole name="worker-role-name" vmsize="worker-role-size" enableNativeCodeExecution="[true|false]">
      <Endpoints>
    <InputEndpoint name="input-endpoint-name" protocol="[http|https|tcp|udp]" localPort="local-port-number" port="port-number" certificate="certificate-name" loadBalancerProbe="load-balancer-probe-name" idleTimeoutInMinutes="tcp-timeout" />
      </Endpoints>
    </WorkerRole>

The .cscfg changes for the timeout setting on public IPs are:

    <NetworkConfiguration>
      <VirtualNetworkSite name="VNet"/>
      <AddressAssignments>
    <InstanceAddress roleName="VMRolePersisted">
      <PublicIPs>
        <PublicIP name="public-ip-name" idleTimeoutInMinutes="timeout-in-minutes"/>
      </PublicIPs>
    </InstanceAddress>
      </AddressAssignments>
    </NetworkConfiguration>

## REST API example
You can configure the TCP idle timeout by using the service management API.
Make sure that the x-ms-version header is set to version 2014-06-01 or later.

Update the configuration of the specified load-balanced input endpoints on all virtual machines in a deployment.

    Request:

    POST https://management.core.windows.net/<subscription-id>/services/hostedservices/<cloudservice-name>/deployments/<deployment-name>
<BR>

    Response:

    <LoadBalancedEndpointList xmlns="http://schemas.microsoft.com/windowsazure" xmlns:i="http://www.w3.org/2001/XMLSchema-instance">
    <InputEndpoint>
    <LoadBalancedEndpointSetName>endpoint-set-name</LoadBalancedEndpointSetName>
    <LocalPort>local-port-number</LocalPort>
    <Port>external-port-number</Port>
    <LoadBalancerProbe>
    <Path>path-of-probe</Path>
    <Port>port-assigned-to-probe</Port>
    <Protocol>probe-protocol</Protocol>
    <IntervalInSeconds>interval-of-probe</IntervalInSeconds>
    <TimeoutInSeconds>timeout-for-probe</TimeoutInSeconds>
    </LoadBalancerProbe>
    <LoadBalancerName>name-of-internal-loadbalancer</LoadBalancerName>
    <Protocol>endpoint-protocol</Protocol>
    <IdleTimeoutInMinutes>15</IdleTimeoutInMinutes>
    <EnableDirectServerReturn>enable-direct-server-return</EnableDirectServerReturn>
    <EndpointACL>
    <Rules>
    <Rule>
    <Order>priority-of-the-rule</Order>
    <Action>permit-rule</Action>
    <RemoteSubnet>subnet-of-the-rule</RemoteSubnet>
    <Description>description-of-the-rule</Description>
    </Rule>
    </Rules>
    </EndpointACL>
    </InputEndpoint>
    </LoadBalancedEndpointList>

## Next steps
[Internal load balancer overview](load-balancer-internal-overview.md)

[Get started configuring an Internet-facing load balancer](load-balancer-get-started-internet-arm-ps.md)

[Configure a load balancer distribution mode](load-balancer-distribution-mode.md)

