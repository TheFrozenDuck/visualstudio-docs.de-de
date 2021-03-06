---
title: Standard-Befehl, Gruppen- und Symbolleiste Platzierung | Microsoft Docs
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology: vs-ide-sdk
ms.tgt_pltfrm: 
ms.topic: article
helpviewer_keywords:
- commands [Visual Studio], default groups
- toolbars [Visual Studio], default
- commands [Visual Studio], default editor
- command groups
- commands [Visual Studio], default IDE
- commands [Visual Studio], default product
ms.assetid: 35342110-d639-4577-8367-00b21dcc6f07
caps.latest.revision: "30"
author: gregvanl
ms.author: gregvanl
manager: ghogen
ms.workload: vssdk
ms.openlocfilehash: 84e850d44162a964ce6ef8b64be92ce4eeacb86e
ms.sourcegitcommit: 32f1a690fc445f9586d53698fc82c7debd784eeb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/22/2017
---
# <a name="default-command-group-and-toolbar-placement"></a>Standardbefehl, Gruppen- und Symbolleiste-Platzierung
Die Benutzeroberfläche zeigt für Produkt Einheitlichkeit und Stabilität bestimmter Befehlsgruppen standardmäßig und [!INCLUDE[vsprvs](../../code-quality/includes/vsprvs_md.md)] enthält Definitionen für Befehle und Befehlsgruppen. VSPackages können sich auch auf die Standardbefehle und Befehlsgruppen aus.  
  
 Die Standard-Befehlsgruppen fallen in drei Kategorien: IDE Befehle, Produkt und Editor-Befehle.  
  
## <a name="default-ide-commands"></a>Standard-IDE-Befehle  
 Die Standard-IDE-Symbolleiste enthält Befehle, die von allen Produkten enthalten, die freigegebenen [!INCLUDE[vsprvs](../../code-quality/includes/vsprvs_md.md)]. Hierzu gehören auch Befehle, die im Zusammenhang mit generischen Projektvorgänge, z. B. die **speichern** Befehl und die **Element hinzufügen** Befehl. VSPackages sollte nicht zum Hinzufügen oder davon subtrahiert dieser Symbolleiste, mit einer Ausnahme: Wenn das Produkt oder VSPackage ein neue Toolfenster fügt, das Fenster sollte der Liste der verfügbaren Toolfenster hinzugefügt werden, auf die **Ansicht** Menü. Neue Produkte oder VSPackages können ihre eigenen Symbolleiste hinzufügen.  
  
## <a name="default-product-commands"></a>Standardbefehle-Produkt  
 Jedes Produkt kann die IDE mit einem eigenen Standardsymbolleiste bereitstellen, die enthält wichtige und häufig verwendete Befehle. Es wird jedoch empfohlen, vorhandenen Menüs und Symbolleisten möglichst und ergänzen sie andere aufgabenspezifischen Symbolleisten, die nach Bedarf.  
  
 Das Feld "Priorität" für eine Symbolleiste bestimmt die Platzierung der Zeile. 0 (null) Priorität verwendet wird, wird die Symbolleiste auf die dritte Zeile (Spalte 3), unterhalb der Menüleiste platziert (Zeile 1) und die **Standard** Symbolleiste (Zeile 2). Aus diesem Grund andere Symbolleisten angezeigt werden, in Zeile (Priorität + 3). Nachfolgende Symbolleisten sind in der gleichen Zeile eingefügt, wenn genügend Platz vorhanden ist; Andernfalls werden sie automatisch auf die nächste Zeile verschoben.  
  
## <a name="default-editor-commands"></a>Standard-Editor-Befehle  
 Eine VSPackage, die einen benutzerdefinierten Editor bereitstellt, sollten eine Standardsymbolleiste bereitstellen, die enthält die wichtigsten und häufig verwendete Befehle in diesem Editor. Die Symbolleiste des Editors sollte angezeigt werden, wenn der Editor aktiv ist und ausgeblendet werden sollen, wenn der Editor nicht aktiv ist. Die Sichtbarkeit wird gesteuert, der `VisibilityConstraints Element` der VSCT-Datei.  
  
 Symbolleisten-Editor-sollten unter IDE und Produkt Symbolleisten platziert werden.  
  
## <a name="see-also"></a>Siehe auch  
 [IDE-definierte Befehle, Menüs und Gruppen](../../extensibility/internals/ide-defined-commands-menus-and-groups.md)   
 [Hinzufügen von Benutzeroberflächenelementen mit VSPackages](../../extensibility/internals/how-vspackages-add-user-interface-elements.md)