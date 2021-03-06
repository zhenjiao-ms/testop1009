---
title: Point a company Internet domain to a Traffic Manager domain | Microsoft Azure
description: This article will help you point your company domain name to a Traffic Manager domain name.
services: traffic-manager
documentationcenter: ''
author: sdwheeler
manager: carmonm
editor: tysonn

ms.service: traffic-manager
ms.devlang: na
ms.topic: get-started-article
ms.tgt_pltfrm: na
ms.workload: infrastructure-services
ms.date: 03/17/2016
ms.author: sewhee

---
# Point a company Internet domain to a Azure Traffic Manager domain
To point your company domain name to a Traffic Manager domain name, modify the DNS resource record on your Internet DNS server to use the CNAME record type, which maps your company domain name to the domain name of your Traffic Manager profile. You can see the Traffic Manager domain name in the **General** section on the Configuration page of the Traffic Manager profile.

For example, to point the company domain name www.contoso.com to the Traffic Manager domain name contoso.trafficmanager.net, you would update your DNS resource record to be the following:

    www.contoso.com IN CNAME contoso.trafficmanager.net

All traffic requests to *www.contoso.com* will now be directed to *contoso.trafficmanager.net*.

> [!IMPORTANT]
> You cannot point a second-level domain, such as *contoso.com*, to the Traffic Manager domain. This is a limitation of the DNS protocol, which does not allow CNAME records for second-level domain names.
> 
> 

## Next steps
[Traffic Manager routing methods](traffic-manager-routing-methods.md)

[Traffic Manager - Disable, enable or delete a profile](disable-enable-or-delete-a-profile.md)

[Traffic Manager - Disable or enable an endpoint](disable-or-enable-an-endpoint.md)

