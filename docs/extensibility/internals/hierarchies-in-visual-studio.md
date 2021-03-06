---
title: Hierarchien in Visual Studio | Microsoft Docs
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology: vs-ide-sdk
ms.tgt_pltfrm: 
ms.topic: article
helpviewer_keywords:
- hierarchies, Visual Studio IDE
- IDE, hierarchies
ms.assetid: 0a029a7c-79fd-4b54-bd63-bd0f21aa8d30
caps.latest.revision: "14"
author: gregvanl
ms.author: gregvanl
manager: ghogen
ms.workload: vssdk
ms.openlocfilehash: e4b0bc2e7c60a4b474f54fd32fd522712326c157
ms.sourcegitcommit: 32f1a690fc445f9586d53698fc82c7debd784eeb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/22/2017
---
# <a name="hierarchies-in-visual-studio"></a>Hierarchien in Visual Studio
Die [!INCLUDE[vsprvs](../../code-quality/includes/vsprvs_md.md)] integrierten Entwicklungsumgebung (IDE) zeigt an, ein Projekt als eine *Hierarchie*. In der IDE ist eine Hierarchie eine Struktur der Knoten, wobei jeder Knoten einen Satz von zugeordnete Eigenschaften aufweist. Ein *Projekt Hierarchie* ist ein Container, der Projektelemente angezeigt, die Elemente Beziehungen, und die Elemente zugeordnete Eigenschaften und Befehle enthält.  
  
 In [!INCLUDE[vsprvs](../../code-quality/includes/vsprvs_md.md)], Verwalten von Hierarchien Projekt mithilfe der Benutzeroberfläche Hierarchie <xref:Microsoft.VisualStudio.Shell.Interop.IVsHierarchy>. Die <xref:Microsoft.VisualStudio.Shell.Interop.IVsUIHierarchy> Schnittstelle leitet Befehle, die Sie an der entsprechenden Hierarchiefenster anstelle der standardmäßigen Befehlshandler von Projektelementen aufrufen.  
  
## <a name="project-hierarchies"></a>Projekt-Hierarchien  
 Jedes Projekthierarchie enthält Elemente, die Sie anzeigen und bearbeiten können. Diese Elemente hängen vom Projekttyp ab. Ein Datenbankprojekt kann z. B. gespeicherte Prozeduren, Ansichten und Datenbanktabellen enthalten. Eine Programmiersprache Projekt umfasst wahrscheinlich andererseits, Quelldateien und Ressourcendateien für Bitmaps und zu den Dialogfeldern. Hierarchien können geschachtelt werden, wo Sie einige zusätzliche Flexibilität bei der Erstellung einer Projekthierarchie.  
  
 Wenn Sie einen neuen Projekttyp erstellen, steuert der Projekttyp den vollständigen Satz von Elementen, die Sie bearbeitet werden kann. Projekte können jedoch Elemente enthalten, für die keine Bearbeitung. Visual C++-Projekten können z. B. HTML-Dateien enthalten, obwohl Visual C++ keine benutzerdefinierten Editor für den HTML-Dateityp bietet.  
  
 Hierarchien verwalten die Persistenz der darin enthaltenen Elemente. Die Implementierung der Hierarchie muss keine besonderen Eigenschaften steuern, die die Persistenz der Elemente innerhalb der Hierarchie auswirken. Z. B. muss Elemente Objekte in einem Repository anstelle von Dateien darzustellen, die Hierarchie-Implementierung die Persistenz dieser Objekte steuern. Die IDE selbst leitet die Hierarchie der Elemente in Übereinstimmung mit Benutzereingaben zu speichern, aber die IDE steuert keine Aktionen erforderlich, um diese Elemente zu speichern. Stattdessen wird das Projekt im Steuerelement ein.  
  
 Wenn ein Benutzer ein Element in einem Editor geöffnet wird, wird die Hierarchie, die dieses Element steuert ausgewählt ist, und wird von der aktiven Hierarchie. Die ausgewählte Hierarchie bestimmt den Satz von Befehlen verfügbar, das für das Element fungiert. Nachverfolgen der den Benutzerfokus auf diese Weise kann die Hierarchie, um den aktuellen Kontext des Benutzers entsprechen.  
  
## <a name="see-also"></a>Siehe auch  
 [Projekttypen](../../extensibility/internals/project-types.md)   
 [Auswahl und Währung, in der IDE](../../extensibility/internals/selection-and-currency-in-the-ide.md)   
 [VSSDK-Beispiele](http://aka.ms/vs2015sdksamples)