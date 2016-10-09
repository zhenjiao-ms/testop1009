---
title: Operations Management Suite Security and Audit Solution Data Security | Microsoft Azure
description: This document explains how data is managed and safeguarded in Operations Management Suite Security and Audit Solution.
services: operations-management-suite
documentationcenter: na
author: YuriDio
manager: swadhwa
editor: ''

ms.service: operations-management-suite
ms.devlang: na
ms.topic: hero-article
ms.tgt_pltfrm: na
ms.workload: na
ms.date: 08/15/2016
ms.author: yurid

---
# Operations Management Suite Security and Audit solution data security
To help customers prevent, detect, and respond to threats, [Operations Management Suite  (OMS) Security and Audit Solution](operations-management-suite-overview.md) collects and processes data about your resources, which includes:

* Security event log
* Event Tracing for Windows (ETW) events
* AppLocker auditing events
* Windows Firewall log
* Advanced Threat Analytics events
* Results of baseline assessment
* Results of antimalware assessment
* Results of update/patch assessment
* Syslogs streams that are explicitly enabled on the agent

We make strong commitments to protect the privacy and security of this data. Microsoft adheres to strict compliance and security guidelines—from coding to operating a service.
This article explains how data is managed and safeguarded in OMS Security and Audit Solution.

## Data sources
OMS Security and Audit Solution analyze data from your Virtual Machines and physical computers where the OMS Agent is installed. OMS Security and Audit Solution can collect configuration information about security events, such as Windows event, audit logs, IIS logs and syslog messages. Examples of such data are: operating system type and version, running processes, machine name, IP addresses, logged in user, and tenant ID.  

## Data protection
**Data segregation**: Data is kept logically separate on each component throughout the service. All data is tagged per organization. This tagging persists throughout the data lifecycle, and it is enforced at each layer of the service. 

**Data access**: To provide security recommendations and investigate potential security threats, Microsoft personnel may access information collected or analyzed by services. We adhere to the [Microsoft Online Services Terms](http://www.microsoftvolumelicensing.com/DocumentSearch.aspx?Mode=3&DocumentTypeId=31) and [Privacy Statement](https://www.microsoft.com/privacystatement/en-us/OnlineServices/Default.aspx), which state that Microsoft will not use Customer Data or derive information from it for any advertising or similar commercial purposes. To provide security recommendations and investigate potential security threats, Microsoft personnel may access information collected or analyzed by services. We only use Customer Data as needed to provide you with Azure services, including purposes compatible with providing those services. You retain all rights to your own data.

**Data use**: Microsoft uses patterns and threat intelligence seen across multiple tenants to enhance our prevention and detection capabilities; we do so in accordance with the privacy commitments described in our [Privacy Statement](https://www.microsoft.com/privacystatement/en-us/OnlineServices/Default.aspx).

> [!NOTE]
> Data location is configured at the OMS workspace level, during the workspace creation, which is part of the initial OMS Security and Audit configuration process.
> 
> 

## See also
In this document, you learned how data is managed and safeguarded in OMS. To learn more about OMS Security and Audit solution, see:

* [Operations Management Suite (OMS) overview](operations-management-suite-overview.md)
* [Monitoring and Responding to Security Alerts in Operations Management Suite Security and Audit Solution](oms-security-responding-alerts.md)
* [Monitoring Resources in Operations Management Suite Security and Audit Solution](oms-security-monitoring-resources.md)

