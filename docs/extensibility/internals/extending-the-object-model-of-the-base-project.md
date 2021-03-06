---
title: Erweitern das Objektmodell der Basisprojekt | Microsoft Docs
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology: vs-ide-sdk
ms.tgt_pltfrm: 
ms.topic: article
helpviewer_keywords:
- automation object model, extending
- project subtypes, extending automation object model
- automation object model
ms.assetid: 2f95cc53-dff6-476c-bacd-500fb0ff7725
caps.latest.revision: "17"
author: gregvanl
ms.author: gregvanl
manager: ghogen
ms.workload: vssdk
ms.openlocfilehash: 44bb1eebecbec036572a9bb8857c87db8e4e4817
ms.sourcegitcommit: 32f1a690fc445f9586d53698fc82c7debd784eeb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/22/2017
---
# <a name="extending-the-object-model-of-the-base-project"></a>Erweitern Sie das Objektmodell des Basis-Projekts
Ein Projektuntertyp verlängert die Automatisierungsobjektmodell des Basis-Projekts in den folgenden Stellen:  
  
-   Project.Extender ("\<ProjectSubtypeName >") – Dies ermöglicht einen Projektuntertyp auf ein Objekt mit benutzerdefinierten Methoden aus bieten die <xref:EnvDTE.Project>. Ein Projektuntertyp können Automatisierungsextender verfügbar machen die `Project` Objekt. Die <xref:EnvDTE80.IInternalExtenderProvider>Schnittstelle implementiert wird, auf dem Hauptprojekt Untertyp Aggregator bieten das Objekt für die `VSHPROPID_ExtObjectCATID` aus <xref:Microsoft.VisualStudio.Shell.Interop.__VSSPROPID2> (entspricht einer `itemid` Wert VSITEMID_ROOT, aus `VSITEMID`) CATID.  
  
-   ProjectItem.Extender ("\<ProjectSubtypeName >") – Dies ermöglicht einen Projektuntertyp auf ein Objekt mit benutzerdefinierten Methoden aus einem bestimmten bieten <xref:EnvDTE.ProjectItem> Objekt innerhalb des Projekts. Ein Projektuntertyp können Automatisierungsextender, dieses Objekt verfügbar gemacht wird. Die <xref:EnvDTE80.IInternalExtenderProvider> Schnittstelle implementiert wird, auf dem Hauptprojekt Untertyp Aggregator muss das Objekt für bieten die `VSHPROPID_ExtObjectCATID` aus <xref:Microsoft.VisualStudio.Shell.Interop.__VSHPROPID2> (entspricht einem gewünschten `VSITEMID`) CATID.  
  
-   Project.Properties - diese Auflistung macht die Konfigurationseigenschaften unabhängig von der `Project` Objekt. Weitere Informationen zu Projekteigenschaften, finden Sie unter <xref:EnvDTE.Project.Properties%2A>. Ein Projektuntertyp können Automatisierungsextender, seine Eigenschaften, die dieser Sammlung hinzufügen. Die <xref:EnvDTE80.IInternalExtenderProvider> Schnittstelle implementiert wird, auf dem Hauptprojekt Untertyp Aggregator muss das Objekt für bieten die `VSHPROPID_BrowseObjectCATID` aus VSHPROPID2 (entspricht einer `itemid` Wert VSITEMID_ROOT, aus <xref:Microsoft.VisualStudio.Shell.Interop.__VSHPROPID2>) CATID.  
  
-   Configuration.Properties - diese Auflistung macht die abhängigen Konfigurationseigenschaften des Projekts für eine bestimmte Konfiguration (z. B. "Debug"). Weitere Informationen finden Sie unter <xref:EnvDTE.Configuration>. Ein Projektuntertyp können Automatisierungsextender, seine Eigenschaften, die dieser Sammlung hinzufügen. Die <xref:EnvDTE80.IInternalExtenderProvider> Schnittstelle implementiert wird, auf dem Hauptprojekt Untertyp Aggregator bietet das Objekt für die CATID `VSHPROPID_CfgBrowseObjectCATID` (entspricht einer `itemid` Wert <xref:Microsoft.VisualStudio.VSConstants.VSITEMID_ROOT>). Die <xref:Microsoft.VisualStudio.Shell.Interop.IVsCfgBrowseObject>Schnittstelle wird verwendet, um ein Konfigurationsobjekt durchsuchen voneinander zu unterscheiden.  
  
## <a name="see-also"></a>Siehe auch  
 <xref:Microsoft.VisualStudio.Shell.Interop.__VSFPROPID>