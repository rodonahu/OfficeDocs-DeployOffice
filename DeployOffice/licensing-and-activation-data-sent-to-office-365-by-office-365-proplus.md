---
title: "Licensing and activation data sent to Office 365 by Office 365 ProPlus"
ms.author: danbrown
author: DHB-MSFT
manager: laurawi
ms.date: 3/22/2017
ms.audience: ITPro
ms.topic: get-started-article
ms.service: o365-administration
localization_priority: Normal
ms.collection: Ent_O365
ms.custom:
- DeployProPlus
- DeployProPlus_SOConly
- Ent_Office_ProPlus
ms.assetid: f7d07a88-35c3-48f5-b30e-c842f2d911a5
description: "Summary: Describes what data Office 365 ProPlus sends to Office 365 services for licensing and activation purposes."
---

# Licensing and activation data sent to Office 365 by Office 365 ProPlus

 **Summary:** Describes what data Office 365 ProPlus sends to Office 365 services for licensing and activation purposes.
  
Computers that have Office 365 ProPlus installed occasionally need to send data to Office 365. This data helps Office 365 do the following:
  
- Register the computer and activate Office 365 ProPlus
    
- Check the status of the Office 365 subscription
    
- Manage product keys for Office 365 ProPlus
    
This article shows the data that is sent to Office 365 for each of these tasks, and which URLs it is sent to.
  
## Registering the computer and activating Office 365 ProPlus
<a name="BKMK_RegisterCompAndActivate"> </a>

During the installation and activation process, Office 365 ProPlus connects to the Office Licensing Service, and sends the following data:
  
****

|**Data**|**Description**|**Purpose**|
|:-----|:-----|:-----|
|OrgId user identity  <br/> |The OrgId ticket generated when the user signs in to Office 365.  <br/> |Used to authenticate the call with the Office Licensing Service. The user signs in to their subscription account to retrieve a license for Office 365.  <br/> |
|Machine Key  <br/> |The serial number of the Office 365 ProPlus product key for the computer.  <br/> |Used to uniquely identify the Office 365 ProPlus product key used by the computer.  <br/> |
|Machine Name  <br/> |The friendly name of the computer, as set by the user in the operating system. For example, if the full name of a computer is "computer1.contoso.com," only "computer1" is sent to Office 365.  <br/> |This value is needed so users can identify which computers they have activated Office 365 ProPlus on when they sign in to the Office 365 portal. On the software page, they see a list of their computers and can manage their Office 365 ProPlus installations.  <br/> |
|Machine ID  <br/> |The hardware ID of the computer.  <br/> |Used to uniquely identify that computer.  <br/> |
   
## Checking the status of the Office 365 subscription
<a name="BKMK_CheckSubscriptionStatus"> </a>

Once Office 365 ProPlus is installed and activated, a process runs once a day to connect to the Office Licensing Service. The purpose is to check whether the Office 365 subscription is still active or if it has changed in any way. The connection needs to succeed at least once a month for Office 365 ProPlus to remain fully functional.
  
Office 365 ProPlus connects to the Office Licensing Service, and sends the following data:
  
****

|**Data**|**Description**|**Purpose**|
|:-----|:-----|:-----|
|Machine Key  <br/> |The serial number of the Office 365 ProPlus product key for the computer.  <br/> |Used to uniquely identify the Office 365 ProPlus product key used by the computer.  <br/> |
   
## Managing product keys for Office 365 ProPlus
<a name="BKMK_ManageProductKeys"> </a>

Office 365 ProPlus uses a standard Microsoft technology called Activation &amp; Validation Service to activate and validate keys. Since Office 365 product keys need to be renewed every month, communication with the Activation &amp; Validation Service is necessary on a monthly basis.
  
For a description of the data sent, see the Activation section of the [Windows 8 and Windows Server 2012 Privacy Statement](https://go.microsoft.com/fwlink/p/?LinkId=313210)
  
## See also
<a name="BKMK_ManageProductKeys"> </a>

#### Other Resources

[Overview of licensing and activation in Office 365 ProPlus](overview-of-licensing-and-activation-in-office-365-proplus.md)
  
[Office 365 URLs and IP address ranges](https://go.microsoft.com/fwlink/p/?linkid=389789)

