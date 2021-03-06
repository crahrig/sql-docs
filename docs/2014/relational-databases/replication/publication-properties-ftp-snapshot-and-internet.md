---
title: "Publication Properties, FTP Snapshot and Internet | Microsoft Docs"
ms.custom: ""
ms.date: "06/13/2017"
ms.prod: "sql-server-2014"
ms.reviewer: ""
ms.technology: replication
ms.topic: conceptual
f1_keywords: 
  - "sql12.rep.newpubwizard.pubproperties.internetsynchronization.f1"
ms.assetid: 8e0198c3-5e4e-418c-9920-78ccbbfc1323
author: MashaMSFT
ms.author: mathoma
manager: craigg
---
# Publication Properties, FTP Snapshot and Internet
  This page allows you to:  
  
-   Set properties for delivering the snapshot through File Transfer Protocol (FTP). For more information, see [Transfer Snapshots Through FTP](transfer-snapshots-through-ftp.md) Windows documentation for more information.  
  
    > [!NOTE]  
    >  Changes to any FTP settings require a new snapshot to be generated.  
  
-   Set properties for Web synchronization for merge replication on [!INCLUDE[ssVersion2005](../../includes/ssversion2005-md.md)] and later versions, which allows subscriptions to be synchronized over HTTPS (secure hypertext transfer protocol). To use Web synchronization, you must configure an [!INCLUDE[msCoName](../../includes/msconame-md.md)] Internet Information Services (IIS) server. For more information, see [Web Synchronization for Merge Replication](web-synchronization-for-merge-replication.md).  
  
## Options  
 **Access snapshot files via FTP**  
 Select **Allow Subscribers to download snapshot files using FTP (File Transfer Protocol)**, and specify **FTP server name**, **Port number**, **Path from the FTP root folder**, **Login**, and **Password**, to allow Subscribers to use FTP for snapshot delivery.  
  
 This option allows Subscribers to use FTP to retrieve snapshot files, but does not require them to do so. If you select this option, the New Subscription Wizard defaults to having the Subscriber retrieve snapshot files through FTP. To change the setting, use the **Subscription Properties** dialog box. If you allow Subscribers to access the snapshot files through FTP, specify the FTP folder as the location for snapshot files on the **Snapshot** page of the **Publication Properties** dialog box. Doing so will cause the Snapshot Agent to update the files in the FTP folder automatically when a new snapshot is generated. If the location is not set to the FTP folder, you will have to update the files manually when new snapshots are generated. For more information, see [Deliver a Snapshot Through FTP](publish/deliver-a-snapshot-through-ftp.md).  
  
 **Web Synchronization**  
 Merge replication only. Select **Allow Subscribers to synchronize by connecting to a Web server**, and specify a Web server address to allow merge Subscribers to use Web synchronization. The Web server must use Secure Sockets Layer (SSL), and the Web address must be fully qualified, such as https://server.domain.com/synchronize. For more information, see [Configure Web Synchronization](configure-web-synchronization.md).  
  
## See Also  
 [Create a Publication](publish/create-a-publication.md)   
 [View and Modify Publication Properties](publish/view-and-modify-publication-properties.md)   
 [View and Modify Pull Subscription Properties](view-and-modify-pull-subscription-properties.md)   
 [View and Modify Push Subscription Properties](view-and-modify-push-subscription-properties.md)   
 [Create and Apply the Initial Snapshot](create-and-apply-the-initial-snapshot.md)   
 [Publish Data and Database Objects](publish/publish-data-and-database-objects.md)  
  
  
