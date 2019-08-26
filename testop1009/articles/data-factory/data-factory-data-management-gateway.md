---
title: Data Management Gateway for Data Factory | Microsoft Azure
description: Set up a data gateway to move data between on-premises and the cloud. Use Data Management Gateway in Azure Data Factory to move your data.
services: data-factory
documentationcenter: ''
author: spelluru
manager: jhubbard
editor: monicar

ms.service: data-factory
ms.workload: data-services
ms.tgt_pltfrm: na
ms.devlang: na
ms.topic: article
ms.date: 08/30/2016
ms.author: spelluru

---
# Data Management Gateway
The Data Management Gateway is a client agent that you must install in your on-premises environment to copy data between cloud and on-premises data stores. The on-premises data stores supported by Data Factory are listed in the [Supported data sources](data-factory-data-movement-activities.md##supported-data-stores) section.

This article complements the walkthrough in the [Move data between on-premises and cloud data stores](data-factory-move-data-between-onprem-and-cloud.md) article. In the walkthrough, you create a pipeline that uses the gateway to move data from an on-premises SQL Server database to an Azure blob. This article provides detailed in-depth information about the Data Management Gateway.   

## Overview
### Capabilities of Data Management gateway
Data Management Gateway provides the following capabilities:

* Model on-premises data sources and cloud data sources within the same data factory and move data.
* Have a single pane of glass for monitoring and management with visibility into gateway status from the Data Factory blade.
* Manage access to on-premises data sources securely.
  * No changes required to corporate firewall. Gateway only makes outbound HTTP-based connections to open internet.
  * Encrypt credentials for your on-premises data stores with your certificate.
* Move data efficiently – data is transferred in parallel, resilient to intermittent network issues with auto retry logic.

### Command flow and data flow
When you use a copy activity to copy data between on-premises and cloud, the activity uses a gateway to transfer data from on-premises data source to cloud and vice versa.

Here high-level data flow for and summary of steps for copy with data gateway:
![Data flow using gateway](./media/data-factory-data-management-gateway/data-flow-using-gateway.png)

1. Data developer creates a gateway for an Azure Data Factory using either the [Azure portal](https://portal.azure.com) or [PowerShell Cmdlet](https://msdn.microsoft.com/library/dn820234.aspx). 
2. Data developer creates a linked service for an on-premises data store by specifying the gateway. As part of setting up the linked service, data developer uses the Setting Credentials application to specify authentication types and credentials.  The Setting Credentials application dialog communicates with the data store to test connection and the gateway to save credentials.
3. Gateway encrypts the credentials with the certificate associated with the gateway (supplied by data developer), before saving the credentials in the cloud.
4. Data Factory service communicates with the gateway for scheduling & management of jobs via a control channel that uses a shared Azure service bus queue. When a copy activity job needs to be kicked off, Data Factory queues the request along with credential information. Gateway kicks off the job after polling the queue.
5. The gateway decrypts the credentials with the same certificate and then connects to the on-premises data store with proper authentication type and credentials.
6. The gateway copies data from an on-premises store to a cloud storage, or vice versa depending on how the Copy Activity is configured in the data pipeline. For this step, the gateway directly communicates with cloud-based storage services such as Azure Blob Storage over a secure (HTTPS) channel.

### Considerations for using gateway
* A single instance of Data Management Gateway can be used for multiple on-premises data sources. However, **a single gateway instance is tied to only one Azure data factory** and cannot be shared with another data factory.
* You can have **only one instance of Data Management Gateway** installed on a single machine. Suppose, you have two data factories that need to access on-premises data sources, you need to install gateways on two on-premises computers. In other words, a gateway is tied to a specific data factory
* The **gateway does not need to be on the same machine as the data source**. However, having gateway closer to the data source reduces the time for the gateway to connect to the data source. We recommend that you install the gateway on a machine that is different from the one that hosts on-premises data source. When the gateway and data source are on different machines, the gateway does not compete for resources with data source.
* You can have **multiple gateways on different machines connecting to the same on-premises data source**. For example, you may have two gateways serving two data factories but the same on-premises data source is registered with both the data factories.
* If you already have a gateway installed on your computer serving a **Power BI** scenario, install a **separate gateway for Azure Data Factory** on another machine.
* Gateway must be used even when you use **ExpressRoute**.
* Treat your data source as an on-premises data source (that is behind a firewall) even when you use **ExpressRoute**. Use the gateway to establish connectivity between the service and the data source.
* You must **use the gateway** even if the data store is in the cloud on an **Azure IaaS VM**. 

## Installation
### Prerequisites
* The supported **Operating System** versions are Windows 7, Windows 8/8.1, Windows 10, Windows Server 2008 R2, Windows Server 2012, Windows Server 2012 R2. Installation of the Data Management Gateway on a domain controller is currently not supported.
* .NET Framework 4.5.1 or above is required. If you are installing gateway on a Windows 7 machine, install .NET Framework 4.5 or later. See [.NET Framework System Requirements](https://msdn.microsoft.com/library/8z6watww.aspx) for details. 
* The recommended **configuration** for the gateway machine is at least 2 GHz, 4 cores, 8-GB RAM, and 80-GB disk.
* If the host machine hibernates, the gateway does not respond to data requests. Therefore, configure an appropriate **power plan** on the computer before installing the gateway. If the machine is configured to hibernate, the gateway installation prompts a message.
* You must be an administrator on the machine to install and configure the Data Management Gateway successfully. You can add additional users to the **Data Management Gateway Users** local Windows group. The members of this group are able to use the Data Management Gateway Configuration Manager tool to configure the gateway. 

As copy activity runs happen on a specific frequency, the resource usage (CPU, memory) on the machine also follows the same pattern with peak and idle times. Resource utilization also depends heavily on the amount of data being moved. When multiple copy jobs are in progress, you see resource usage go up during peak times. 

### Installation options
Data Management Gateway can be installed in the following ways: 

* By downloading an MSI setup package from the [Microsoft Download Center](https://www.microsoft.com/download/details.aspx?id=39717).  The MSI can also be used to upgrade existing Data Management Gateway to the latest version, with all settings preserved.
* By clicking **Download and install data gateway** link under MANUAL SETUP or **Install directly on this computer** under EXPRESS SETUP. See [Move data between on-premises and cloud](data-factory-move-data-between-onprem-and-cloud.md) article for step-by-step instructions on using express setup. The manual step takes you to the download center.  The instructions for downloading and installing the gateway from download center are in the next section. 

### Installation best practices:
1. Configure power plan on the host machine for the gateway so that the machine does not hibernate. If the host machine hibernates, the gateway does not respond to data requests.
2. Back up the certificate associated with the gateway.

### Install gateway from download center
1. Navigate to [Microsoft Data Management Gateway download page](https://www.microsoft.com/download/details.aspx?id=39717). 
2. Click **Download**, select the appropriate version (**32-bit** vs. **64-bit**), and click **Next**. 
3. Run the **MSI** directly or save it to your hard disk and run.
4. On the **Welcome** page, select a **language** click **Next**.
5. **Accept** the End-User License Agreement and click **Next**. 
6. Select **folder** to install the gateway and click **Next**. 
7. On the **Ready to install** page, click **Install**. 
8. Click **Finish** to complete installation.
9. Get the key from the Azure portal. See the next section for step-by-step instructions. 
10. On the **Register gateway** page of **Data Management Gateway Configuration Manager** running on your machine, do the following: 
    1. Paste the key in the text.
    2. Optionally, click **Show gateway key** to see the key text.
    3. Click **Register**. 

### Register gateway using key
#### If you haven't already created a logical gateway in the portal
To create a gateway in the portal and get the key from the **Configure** blade, Follow steps from walkthrough in the [Move data between on-premises and cloud](data-factory-move-data-between-onprem-and-cloud.md) article.    

#### If you have already created the logical gateway in the portal
1. In Azure portal, navigate to the **Data Factory** blade, and click **Linked Services** tile.
   
    ![Data Factory blade](media/data-factory-data-management-gateway/data-factory-blade.png)
2. In the **Linked Services** blade, select the logical **gateway** you created in the portal. 
   
    ![logical gateway](media/data-factory-data-management-gateway/data-factory-select-gateway.png)  
3. In the **Data Gateway** blade, click **Download and install data gateway**.
   
    ![Download link in the portal](media/data-factory-data-management-gateway/download-and-install-link-on-portal.png)   
4. In the **Configure** blade, click **Recreate key**. Click Yes on the warning message after reading it carefully.
   
    ![Recreate key](media/data-factory-data-management-gateway/recreate-key-button.png)
5. Click Copy button next to the key. The key is copied to the clipboard.
   
    ![Copy key](media/data-factory-data-management-gateway/copy-gateway-key.png) 

### System tray icons/ notifications
The following image shows some of the tray icons that you see. 

![system tray icons](./media/data-factory-data-management-gateway/gateway-tray-icons.png)

If you move cursor over the system tray icon/notification message, you see details about the state of the gateway/update operation in a popup window.

### Ports and firewall
There are two firewalls you need to consider: **corporate firewall** running on the central router of the organization, and **Windows firewall** configured as a daemon on the local machine where the gateway is installed.  

![firewalls](./media/data-factory-data-management-gateway/firewalls.png)

At corporate firewall level, you need configure the following domains and outbound ports:

| Domain names | Ports | Description |
| --- | --- | --- |
| *.servicebus.windows.net |443, 80 |Listeners on Service Bus Relay over TCP (requires 443 for Access Control token acquisition) |
| *.servicebus.windows.net |9350-9354, 5671 |Optional service bus relay over TCP |
| *.core.windows.net |443 |HTTPS |
| *.clouddatahub.net |443 |HTTPS |
| graph.windows.net |443 |HTTPS |
| login.windows.net |443 |HTTPS |

At windows firewall level, these outbound ports are normally enabled. If not, you can configure the domains and ports accordingly on gateway machine.

#### Copy data from a source data store to a sink data store
Ensure that the firewall rules are enabled properly on the corporate firewall, Windows firewall on the gateway machine, and the data store itself. Enabling these rules allows the gateway to connect to both source and sink successfully. Enable rules for each data store that is involved in the copy operation.

For example, to copy from **an on-premises data store to an Azure SQL Database sink or an Azure SQL Data Warehouse sink**, you need to do the following: 

* Allow outbound **TCP** communication on port **1433** for both Windows firewall and corporate firewall
* Configure the firewall settings of Azure SQL server to add the IP address of the gateway machine to the list of allowed IP addresses. 

### Proxy server considerations
If your corporate network environment uses a proxy server to access the internet, configure Data Management Gateway to use appropriate proxy settings. You can set the proxy during the initial registration phase. 

![Set proxy during registration](media/data-factory-data-management-gateway/SetProxyDuringRegistration.png)

Gateway uses the proxy server to connect to the cloud service. Click **Change** link during initial setup. You see the **proxy setting** dialog.

![Set proxy using config manager](media/data-factory-data-management-gateway/SetProxySettings.png)

There are three configuration options: 

* **Do not use proxy**: Gateway does not explicitly use any proxy to connect to cloud services.
* **Use system proxy**: Gateway uses the proxy setting that is configured in diahost.exe.config.  If no proxy is configured in diahost.exe.config, gateway connects to cloud service directly without going through proxy.
* **Use custom proxy**: Configure the HTTP proxy setting to use for gateway, instead of using configurations in diahost.exe.config.  Address and Port are required.  User Name and Password are optional depending on your proxy’s authentication setting.  All settings are encrypted with the credential certificate of the gateway and stored locally on the gateway host machine.

The Data Management Gateway Host Service restarts automatically after you save the updated proxy settings. 

After gateway has been successfully registered, if you want to view or update proxy settings, use Data Management Gateway Configuration Manager. 

1. Launch Data Management Gateway Configuration Manager.
2. Switch to the **Settings** tab.
3. Click **Change** link in **HTTP Proxy** section to launch the **Set HTTP Proxy** dialog.  
4. After you click the **Next** button, you see a warning dialog asking for your permission to save the proxy setting and restart the Gateway Host Service.

You can view and update HTTP proxy by using Configuration Manager tool. 

![Set proxy using config manager](media/data-factory-data-management-gateway/SetProxyConfigManager.png)

> [!NOTE]
> If you set up a proxy server with NTLM authentication, Gateway Host Service runs under the domain account. If you change the password for the domain account later, remember to update configuration settings for the service and restart it accordingly. Due to this requirement, we suggest you use a dedicated domain account to access the proxy server that does not require you to update the password frequently.
> 
> 

### Configure proxy server settings in diahost.exe.config
If you select **Use system proxy** setting for the HTTP proxy, gateway uses the proxy setting in diahost.exe.config.  If no proxy is specified in diahost.exe.config, gateway connects to cloud service directly without going through proxy. The following procedure provides instructions for updating the config file. 

1. In File Explorer, make a safe copy of C:\Program Files\Microsoft Data Management Gateway\1.0\Shared\diahost.exe.config to back up the original file.
2. Launch Notepad.exe running as administrator, and open text file “C:\Program Files\Microsoft Data Management Gateway\2.0\Shared\diahost.exe.config. You find the default tag for system.net as following:
   
         <system.net>
             <defaultProxy useDefaultCredentials="true" />
         </system.net>    
   
   You can then add proxy server details as shown in the following example:
   
         <system.net>
               <defaultProxy enabled="true">
                     <proxy bypassonlocal="true" proxyaddress="http://proxy.domain.org:8888/" />
               </defaultProxy>
         </system.net>
   
   Additional properties are allowed inside the proxy tag to specify the required settings like scriptLocation. Refer to [proxy Element (Network Settings)](https://msdn.microsoft.com/library/sa91de1e.aspx) on syntax.
   
         <proxy autoDetect="true|false|unspecified" bypassonlocal="true|false|unspecified" proxyaddress="uriString" scriptLocation="uriString" usesystemdefault="true|false|unspecified "/>
3. Save the configuration file into the original location, then restart the Data Management Gateway Host service, which picks up the changes. To restart the service: use services applet from the control panel, or from the **Data Management Gateway Configuration Manager** > click the **Stop Service** button, then click the **Start Service**. If the service does not start, it is likely that an incorrect XML tag syntax has been added into the application configuration file that was edited.     

In addition to these points, you also need to make sure Microsoft Azure is in your company’s whitelist. The list of valid Microsoft Azure IP addresses can be downloaded from the [Microsoft Download Center](https://www.microsoft.com/download/details.aspx?id=41653).

#### Possible symptoms for firewall and proxy server-related issues
If you encounter errors similar to the following ones, it is likely due to improper configuration of the firewall or proxy server, which blocks gateway from connecting to Data Factory to authenticate itself. Refer to previous section to ensure your firewall and proxy server are properly configured.

1. When you try to register the gateway, you receive the following error: "Failed to register the gateway key. Before trying to register the gateway key again, confirm that the Data Management Gateway is in a connected state and the Data Management Gateway Host Service is Started."
2. When you open Configuration Manager, you see status as “Disconnected” or “Connecting.” When viewing Windows event logs, under “Event Viewer” > “Application and Services Logs” > “Data Management Gateway”, you see error messages such as the following:
   `Unable to connect to the remote server` 
   `A component of Data Management Gateway has become unresponsive and restarts automatically. Component name: Gateway.`

### Open port 8050 for credential encryption
The **Setting Credentials** application uses the inbound port **8050** to relay credentials to the gateway when you set up an on-premises linked service in the Azure portal. During gateway setup, by default, the Data Management Gateway installation opens it on the gateway machine.

If you are using a third-party firewall, you can manually open the port 8050. If you run into firewall issue during gateway setup, you can try using the following command to install the gateway without configuring the firewall.

    msiexec /q /i DataManagementGateway.msi NOFIREWALL=1

If you choose not to open the port 8050 on the gateway machine, use mechanisms other than using the **Setting Credentials** application to configure data store credentials. For example, you could use [New-AzureRmDataFactoryEncryptValue](https://msdn.microsoft.com/library/mt603802.aspx) PowerShell cmdlet. See [Setting Credentials and Security](#set-credentials-and-securityy) section on how data store credentials can be set.

## Update
By default, Data Management Gateway is automatically updated when a newer version of the gateway is available. The gateway is not updated until all the scheduled tasks are done. No further tasks are processed by the gateway until the update operation is completed. If the update fails, gateway is rolled back to the old version. 

You see the scheduled update time in the following places:

* The gateway properties blade in the Azure portal.
* Home page of the Data Management Gateway Configuration Manager
* System tray notification message. 

The Home tab of the Data Management Gateway Configuration Manager displays the update schedule and the last time the gateway was installed/updated. 

![Schedule updates](media/data-factory-data-management-gateway/UpdateSection.png)

You can install the update right away or wait for the gateway to be automatically updated at the scheduled time. For example, the following image shows you the notification message shown in the Gateway Configuration Manager along with the Update button that you can click to install it immediately. 

![Update in DMG Configuration Manager](./media/data-factory-data-management-gateway/gateway-auto-update-config-manager.png)

The notification message in the system tray would look like the following: 

![System Tray message](./media/data-factory-data-management-gateway/gateway-auto-update-tray-message.png)

You see the status of update operation (manual or automatic) in the system tray. When you launch Gateway Configuration Manager next time, you see a message on the notification bar that the gateway has been updated along with a link to [what's new topic](data-factory-gateway-release-notes.md).

### To disable/enable auto-update feature
You can disable/enable the auto-update feature by doing the following: 

1. Launch Windows PowerShell on the gateway machine. 
2. Switch to the C:\Program Files\Microsoft Data Management Gateway\1.0\PowerShellScript folder.
3. Run the following command to turn the auto-update feature OFF (disable).   
   
        .\GatewayAutoUpdateToggle.ps1  -off
4. To turn it back on: 
   
        .\GatewayAutoUpdateToggle.ps1  -on  

## Configuration Manager
Once you install the gateway, you can launch Data Management Gateway Configuration Manager in one of the following ways: 

* In the **Search** window, type **Data Management Gateway** to access this utility. 
* Run the executable **ConfigManager.exe** in the folder: **C:\Program Files\Microsoft Data Management Gateway\1.0\Shared** 

### Home page
The Home page allows you to do the following: 

* View status of the gateway (connected to the cloud service etc.). 
* **Register** using a key from the portal.
* **Stop** and start the **Data Management Gateway Host service** on the gateway machine.
* **Schedule updates** at a specific time of the days.
* View the date when the gateway was **last updated**. 

### Settings page
The Settings page allows you to do the following:

* View, change, and export **certificate** used by the gateway. This certificate is used to encrypt data source credentials.
* Change **HTTPS port** for the endpoint. The gateway opens a port for setting the data source credentials. 
* **Status** of the endpoint
* View **SSL certificate** is used for SSL communication between portal and the gateway to set credentials for data sources.  

### Diagnostics page
The Diagnostics page allows you to do the following:

* Enable verbose **logging**, view logs in event viewer, and send logs to Microsoft if there was a failure.
* **Test connection** to a data source.  

### Help page
The Help page displays the following: 

* Brief description of the gateway
* Version number
* Links to online help, privacy statement, and license agreement.  

## Troubleshooting
* You can find detailed information in gateway logs in Windows event logs. You can find them by using Windows **Event Viewer** under **Application and Services Logs** > **Data Management Gateway**. When troubleshooting gateway-related issues, look for error level events in the event viewer.
* If the gateway stops working after you **change the certificate**, restart the **Data Management Gateway Service** using the Microsoft Data Management Gateway Configuration Manager tool or Services control panel applet. If you still see an error, you may have to give explicit permissions for the Data Management Gateway service user to access the certificate in Certificates Manager (certmgr.msc).  The default user account for the service is: **NT Service\DIAHostService**. 
* If the **Credential Manager** application fails to **encrypt** credentials when you click Encrypt button in Data Factory Editor, verify that you are running this application on the **gateway machine**. If not, run the application on the gateway machine and try to encrypt credentials.  
* If you see data store connection or driver-related errors, do the following: 
  
  * Launch **Data Management Gateway Configuration Manager** on the gateway machine.
  * Switch to the **Diagnostics** tab
  * Select/enter appropriate values for fields in the **Test connection to an on-premises data source using this gateway** group
  * Click **Test connection** to see if you can connect to on-premises data source from the gateway machine using the connection information and credentials. If the test connection still fails after you install a driver, restart the gateway for it to pick up the latest change.  
    
    ![Test Connection](./media/data-factory-data-management-gateway/TestConnection.png)

### Send gateway logs to Microsoft
When you contact Microsoft Support to get help with troubleshooting gateway issues, you may be asked to share your gateway logs. The release of the gateway allows you to easily share required gateway logs through two button clicks in Gateway Configuration Manager.   

1. Switch to **Diagnostics** tab of gateway configuration manager.
   
    ![Data Management Gateway - Diagnostics tab](media/data-factory-data-management-gateway/data-management-gateway-diagnostics-tab.png)
2. Click **Send logs** link to see the following dialog box. 
   
    ![Data Management Gateway - Send logs](media/data-factory-data-management-gateway/data-management-gateway-send-logs-dialog.png)
3. (optional) Click **view logs** to review logs in the event viewer.
4. (optional) Click **privacy** to review Microsoft online services privacy statement. 
5. Once you are satisfied with what you are about to upload, click **Send logs** to actually send logs from last seven days to Microsoft for troubleshooting. You should see the status of the Send logs operation as shown in the following image.
   
    ![Data Management Gateway - Send logs status](media/data-factory-data-management-gateway/data-management-gateway-send-logs-status.png)
6. Once the operation is complete, you see a dialog box as shown in the following image.
   
    ![Data Management Gateway - Send logs status](media/data-factory-data-management-gateway/data-management-gateway-send-logs-result.png)
7. Note down the **report ID** and share it with Microsoft Support. The report ID is used to locate your gateway logs you uploaded for troubleshooting.  The report ID is also saved in event viewer for your reference.  You can find it by looking at the event ID “25” and check the date and time.
   
    ![Data Management Gateway - Send logs report ID](media/data-factory-data-management-gateway/data-management-gateway-send-logs-report-id.png)    

### Archive gateway logs on gateway host machine
There are some scenarios where you have gateway issues and you cannot share gateway logs directly: 

* You manually install the gateway and register the gateway;
* You try to register the gateway with a regenerated key on configuration manager; 
* You try to send logs and the gateway host service cannot be connected;

In such cases, you can save gateway logs as a zip file and share it when contacting Microsoft support later. For example, if you receive an error while registering the gateway as shown in the following image:   

![Data Management Gateway - Registration error](media/data-factory-data-management-gateway/data-management-gateway-registration-error.png)

Click **Archive gateway** logs link to archive and save logs and then share the zip file with Microsoft support. 

![Data Management Gateway - Archive logs](media/data-factory-data-management-gateway/data-management-gateway-archive-logs.png)

### Gateway is online with limited functionality
You see status of the gateway as **online with limited functionality** for one of the following reasons.

* Gateway cannot connect to cloud service through service bus.
* Cloud service cannot connect to gateway through service bus.

When gateway is online with limited functionality, you may not be able to use the Data Factory Copy Wizard to create data pipelines for copying data to/from on-premises data stores.

Resolution/workaround for this issue (online with limited functionality) is based on whether gateway cannot connect to cloud service or the other way. The following sections provide these workarounds. 

#### Gateway cannot connect to cloud service through service bus
Follow these steps to get the gateway back online: 

1. Enable outbound ports 9350-9354 on both the Windows Firewall on gateway machine and Corporate Firewall. See [Ports and firewall](#ports-and-firewall) section for detail.
2. Configure proxy settings on the gateway. See [Proxy server considerations](#proxy-server-considerations) section for detail. 

As a workaround, use Data Factory Editor in Azure portal (or) Visual Studio (or) Azure PowerShell.

#### Error: Cloud service cannot connect to gateway through service bus.
Follow these steps to get the gateway back online:

1. Enable outbound ports 5671 and 9350-9354 on both the Windows Firewall on gateway machine and Corporate Firewall. See [Ports and firewall](#ports-and-firewall) section for detail.
2. Configure proxy settings on the gateway. See [Proxy server considerations](#proxy-server-considerations) section for detail.
3. Remove static IP limitation on the proxy server. 

As a workaround, you can use Data Factory Editor in Azure portal (or) Visual Studio (or) Azure PowerShell.

## Move gateway from a machine to another
This section provides steps for moving gateway client from one machine to another machine. 

1. In the portal, navigate to the **Data Factory home page**, and click the **Linked Services** tile. 
   
    ![Data Gateways Link](./media/data-factory-data-management-gateway/DataGatewaysLink.png) 
2. Select your gateway in the **DATA GATEWAYS** section of the **Linked Services** blade.
   
    ![Linked Services blade with gateway selected](./media/data-factory-data-management-gateway/LinkedServiceBladeWithGateway.png)
3. In the **Data gateway** blade, click **Download and install data gateway**.
   
    ![Download gateway link](./media/data-factory-data-management-gateway/DownloadGatewayLink.png) 
4. In the **Configure** blade, click **Download and install data gateway**, and follow instructions to install the data gateway on the machine. 
   
    ![Configure blade](./media/data-factory-data-management-gateway/ConfigureBlade.png)
5. Keep the **Microsoft Data Management Gateway Configuration Manager** open. 
   
    ![Configuration Manager](./media/data-factory-data-management-gateway/ConfigurationManager.png)    
6. In the **Configure** blade in the portal, click **Recreate key** on the command bar, and click **Yes** for the warning message. Click **copy button** next to key text that copies the key to the clipboard. The gateway on the old machine stops functioning as soon you recreate the key.  
   
    ![Recreate key](./media/data-factory-data-management-gateway/RecreateKey.png)
7. Paste the **key** into text box in the **Register Gateway** page of the **Data Management Gateway Configuration Manager** on your machine. (optional) Click **Show gateway key** check box to see the key text. 
   
    ![Copy key and Register](./media/data-factory-data-management-gateway/CopyKeyAndRegister.png)
8. Click **Register** to register the gateway with the cloud service.
9. On the **Settings** tab, click **Change** to select the same certificate that was used with the old gateway, enter the **password**, and click **Finish**. 
   
   ![Specify Certificate](./media/data-factory-data-management-gateway/SpecifyCertificate.png)
   
   You can export a certificate from the old gateway by doing the following: launch Data Management Gateway Configuration Manager on the old machine, switch to the **Certificate** tab, click **Export** button and follow the instructions. 
10. After successful registration of the gateway, you should see the **Registration** set to **Registered** and **Status** set to **Started** on the Home page of the Gateway Configuration Manager. 

## Encrypting credentials
To encrypt credentials in the Data Factory Editor, do the following:

1. Launch web browser on the **gateway machine**, navigate to [Azure portal](http://portal.azure.com). Search for your data factory if needed, open data factory in the **DATA FACTORY** blade and then click **Author & Deploy** to launch Data Factory Editor.   
2. Click an existing **linked service** in the tree view to see its JSON definition or create a linked service that requires a Data Management Gateway (for example: SQL Server or Oracle). 
3. In the JSON editor, for the **gatewayName** property, enter the name of the gateway. 
4. Enter server name for the **Data Source** property in the **connectionString**.
5. Enter database name for the **Initial Catalog** property in the **connectionString**.    
6. Click **Encrypt** button on the command bar that launches the click-once **Credential Manager** application. You should see the **Setting Credentials** dialog box. 
    ![Setting credentials dialog](./media/data-factory-data-management-gateway/setting-credentials-dialog.png)
7. In the **Setting Credentials** dialog box, do the following:  
   1. Select **authentication** that you want the Data Factory service to use to connect to the database. 
   2. Enter name of the user who has access to the database for the **USERNAME** setting. 
   3. Enter password for the user for the **PASSWORD** setting.  
   4. Click **OK** to encrypt credentials and close the dialog box. 
8. You should see a **encryptedCredential** property in the **connectionString** now.        
   
         {
             "name": "SqlServerLinkedService",
             "properties": {
                 "type": "OnPremisesSqlServer",
                 "description": "",
                 "typeProperties": {
                     "connectionString": "data source=myserver;initial catalog=mydatabase;Integrated Security=False;EncryptedCredential=eyJDb25uZWN0aW9uU3R",
                     "gatewayName": "adftutorialgateway"
                 }
             }
         }

If you access the portal from a machine that is different from the gateway machine, you must make sure that the Credentials Manager application can connect to the gateway machine. If the application cannot reach the gateway machine, it does not allow you to set credentials for the data source and to test connection to the data source.  

When you use the **Setting Credentials** application, the portal encrypts the credentials with the certificate specified in the **Certificate** tab of the **Gateway Configuration Manager** on the gateway machine. 

If you are looking for an API-based approach for encrypting the credentials, you can use the [New-AzureRmDataFactoryEncryptValue](https://msdn.microsoft.com/library/mt603802.aspx) PowerShell cmdlet to encrypt credentials. The cmdlet uses the certificate that gateway is configured to use to encrypt the credentials. You add encrypted credentials to the **EncryptedCredential** element of the **connectionString** in the JSON. You use the JSON with the [New-AzureRmDataFactoryLinkedService](https://msdn.microsoft.com/library/mt603647.aspx) cmdlet or in the Data Factory Editor. 

    "connectionString": "Data Source=<servername>;Initial Catalog=<databasename>;Integrated Security=True;EncryptedCredential=<encrypted credential>",

There is one more approach for setting credentials using Data Factory Editor. If you create a SQL Server linked service by using the editor and you enter credentials in plain text, the credentials are encrypted using a certificate that the Data Factory service owns. It does NOT use the certificate that gateway is configured to use. While this approach might be a little faster in some cases, it is less secure. Therefore, we recommend that you follow this approach only for development/testing purposes. 

## PowerShell cmdlets
This section describes how to create and register a gateway using Azure PowerShell cmdlets. 

1. Launch **Azure PowerShell** in administrator mode. 
2. Log in to your Azure account by running the following command and entering your Azure credentials. 
   
    Login-AzureRmAccount
3. Use the **New-AzureRmDataFactoryGateway** cmdlet to create a logical gateway as follows:
   
        $MyDMG = New-AzureRmDataFactoryGateway -Name <gatewayName> -DataFactoryName <dataFactoryName> -ResourceGroupName ADF –Description <desc>
   
    **Example command and output**:

        PS C:\> $MyDMG = New-AzureRmDataFactoryGateway -Name MyGateway -DataFactoryName $df -ResourceGroupName ADF –Description “gateway for walkthrough”

        Name              : MyGateway
        Description       : gateway for walkthrough
        Version           :
        Status            : NeedRegistration
        VersionStatus     : None
        CreateTime        : 9/28/2014 10:58:22
        RegisterTime      :
        LastConnectTime   :
        ExpiryTime        :
        ProvisioningState : Succeeded
        Key               : ADF#00000000-0000-4fb8-a867-947877aef6cb@fda06d87-f446-43b1-9485-78af26b8bab0@4707262b-dc25-4fe5-881c-c8a7c3c569fe@wu#nfU4aBlq/heRyYFZ2Xt/CD+7i73PEO521Sj2AFOCmiI


1. In Azure PowerShell, switch to the folder: **C:\Program Files\Microsoft Data Management Gateway\1.0\PowerShellScript\**. Run **RegisterGateway.ps1** associated with the local variable **$Key** as shown in the following command. This script registers the client agent installed on your machine with the logical gateway you create earlier.
   
        PS C:\> .\RegisterGateway.ps1 $MyDMG.Key
   
        Agent registration is successful!
   
    You can register the gateway on a remote machine by using the IsRegisterOnRemoteMachine parameter. Example:
   
        .\RegisterGateway.ps1 $MyDMG.Key -IsRegisterOnRemoteMachine true
2. You can use the **Get-AzureRmDataFactoryGateway** cmdlet to get the list of Gateways in your data factory. When the **Status** shows **online**, it means your gateway is ready to use.
   
        Get-AzureRmDataFactoryGateway -DataFactoryName <dataFactoryName> -ResourceGroupName ADF

You can remove a gateway using the **Remove-AzureRmDataFactoryGateway** cmdlet and update description for a gateway using the **Set-AzureRmDataFactoryGateway** cmdlets. For syntax and other details about these cmdlets, see Data Factory Cmdlet Reference.  

### List gateways using PowerShell
    Get-AzureRmDataFactoryGateway -DataFactoryName jasoncopyusingstoredprocedure -ResourceGroupName ADF_ResourceGroup

### Remove gateway using PowerShell
    Remove-AzureRmDataFactoryGateway -Name JasonHDMG_byPSRemote -ResourceGroupName ADF_ResourceGroup -DataFactoryName jasoncopyusingstoredprocedure -Force 


## Next Steps
* See [Data Management Gateway](data-factory-data-management-gateway.md) article for detailed information about the gateway. 

