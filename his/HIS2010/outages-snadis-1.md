---
title: "Outages (SNADIS)1 | Microsoft Docs"
ms.custom: ""
ms.date: "11/30/2017"
ms.prod: "host-integration-server"
ms.reviewer: ""
ms.suite: ""
ms.tgt_pltfrm: ""
ms.topic: "article"
ms.assetid: f917787b-4335-44fe-8a29-916806abb764
caps.latest.revision: 4
---
# Outages (SNADIS)
If the SNALink detects a link or station failure, it reports the failure by sending an [Outage](../HIS2010/outage1.md) message to the node on either the LINK or STATION LPI connection depending on whether it is a link or station outage. Generally, a station outage indicates a problem at the remote station, and a link outage indicates a local or line problem.  
  
 When the local node receives an Outage message, it:  
  
-   Logs an error containing the outage code.  
  
-   Cleans up each session using the connection and informs applications of the failure (for instance, with a Comm Check code on a 3270 emulator).  
  
-   Sends a [Close(LINK) Request](../HIS2010/close-link-request2.md) to the SNALink.  
  
 On receipt of the **Close(LINK) Request**, the SNALink should clear up its internal resources for the connection and send back a [Close(LINK) Response](../HIS2010/close-link-response1.md).  
  
 ![](../core/media/dev3p.gif "dev3p")  
Local node receiving an Outage message and sending a Close(LINK) Request and a Close(LINK) response  
  
 There is a special case when the node loses contact with the SNALink software. In this case, the node is notified of this event (a lost locality) and performs outage processing apart from sending messages to the SNALink.  
  
 The outage codes are not distinguished by the node, but they are logged. For the sake of consistency across SNALink implementations, the values listed in the following topics should be used.  
  
## In This Section  
  
-   [SDLC Outage Codes](../HIS2010/sdlc-outage-codes1.md)  
  
-   [X.25 Outage Codes](../HIS2010/x-25-outage-codes1.md)