---
title: "Remote Environment Selection with the SelectionHint Property1 | Microsoft Docs"
ms.custom: ""
ms.date: "11/30/2017"
ms.prod: "host-integration-server"
ms.reviewer: ""
ms.suite: ""
ms.tgt_pltfrm: ""
ms.topic: "article"
ms.assetid: 6336b17e-0e05-4d5b-b117-953c2306bc22
caps.latest.revision: 3
---
# Remote Environment Selection with the SelectionHint Property
Developers can use the `SelectionHint` property to specify a remote environment (RE) programmatically.  
  
 By setting the `SelectionHint` property, applications can specify which CICS or IMS RE should be used when servicing Transaction Integrator (TI) requests. The algorithm used by an application in selecting an RE is determined by the application code. For example, a business enterprise can use separate CICS or IMS regions when handling requests from different branches. In this case, the application chooses the RE that identifies the region suitable for the current branch.  
  
 To specify an RE in an application, set the `SelectionHint` property to the name of the RE you want to use. TI Designer automatically adds the write-only `SelectionHint` property to each TI component.  
  
 Before you can use the `SelectionHint` property to specify a remote environment (RE) programmatically, the following must be in place:  
  
-   [!INCLUDE[hisHostIntServNoVersion](../includes/hishostintservnoversion-md.md)] must be installed on all computers running the TI run-time environment or TI Designer.  
  
-   The TI component must be assigned to an RE even though RE selection is in use. The RE assigned to the component is used when an application that has a TI component does not explicitly set the `SelectionHint` property.  
  
 To assign a TI component to an RE, use TI Manager and follow the instructions provided in the TI online Help.  
  
## In This Section  
 [Remote Environment Selection Guidelines](../HIS2010/remote-environment-selection-guidelines2.md)  
  
 [Writing Code that Specifies a Remote Environment](../HIS2010/writing-code-that-specifies-a-remote-environment2.md)  
  
 [Cost of Remote Environment Selection](../HIS2010/cost-of-remote-environment-selection1.md)