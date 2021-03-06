---
title: "Assembly &#39;&lt;Dateipfad1&gt;&#39; verweist auf Assembly &#39;&lt;Assemblyidentit&#228;t&gt;&#39;, die zwischen &#39;&lt; Dateipfad2&gt;&#39; (Verweis durch Projekt &#39;&lt;Projektnamen1&gt;&#39;) und &#39;&lt;Dateipfad3&gt;&#39; (Verweis durch Projekt &#39;&lt; Projektname2&gt;&#39;) mehrdeutig ist | Microsoft Docs"
ms.custom: ""
ms.date: "12/14/2016"
ms.prod: "visual-studio-dev14"
ms.reviewer: ""
ms.suite: ""
ms.technology: 
  - "devlang-visual-basic"
ms.tgt_pltfrm: ""
ms.topic: "article"
f1_keywords: 
  - "bc42204"
  - "vbc42204"
helpviewer_keywords: 
  - "BC42204"
ms.assetid: b0c3d2b6-2776-4981-b79e-2e36f03d4123
caps.latest.revision: 12
caps.handback.revision: 12
author: "stevehoag"
ms.author: "shoag"
manager: "wpickett"
---
# Assembly &#39;&lt;Dateipfad1&gt;&#39; verweist auf Assembly &#39;&lt;Assemblyidentit&#228;t&gt;&#39;, die zwischen &#39;&lt; Dateipfad2&gt;&#39; (Verweis durch Projekt &#39;&lt;Projektnamen1&gt;&#39;) und &#39;&lt;Dateipfad3&gt;&#39; (Verweis durch Projekt &#39;&lt; Projektname2&gt;&#39;) mehrdeutig ist
Assembly '\<Dateipfad1\>' verweist auf Assembly '\<Assemblyidentität\>', die zwischen '\< Dateipfad2\>' \(Verweis durch Projekt '\<Projektnamen1\>'\) und '\<Dateipfad3\>' \(Verweis durch Projekt '\< Projektname2\>'\) mehrdeutig ist. '\<Dateipfad2\>' wird verwendet. Wenn beide Assemblys identisch sind, ändern Sie die Verweise auf denselben Speicherort.  
  
 Eine Assembly greift auf einen Typ in einer anderen Assembly zu, für die sie über mehrere Dateiverweise verfügt.  
  
 Der Compiler kann nicht garantieren, dass die Dateien an den verschiedenen Speicherorten dieselbe Version derselben Assembly enthalten. Daher sind die Dateiverweise mehrdeutig und der Compiler muss einen Verweis auswählen.  
  
 Die *Identität der Assembly* enthält den Namen, die Version, ggf. den öffentlichen Schlüssel sowie die Kultur der Assembly. Diese Information kennzeichnet die Assembly eindeutig.  
  
 Standardmäßig ist diese Meldung eine Warnung. Informationen zum Ausblenden von Warnungen oder zum Behandeln von Warnungen als Fehler finden Sie unter [Konfigurieren von Warnungen in Visual Basic](../ide/configuring-warnings-in-visual-basic.md).  
  
 **Fehler\-ID:** BC42204  
  
### So beheben Sie diesen Fehler  
  
1.  Bestimmen Sie, welche Datei die beste Wahl für die Assembly darstellt. Sie können Kriterien wie die neueste Version, die Verfügbarkeit der Datei und die Wahrscheinlichkeit einer angemessenen Aktualisierung verwenden.  
  
2.  Ändern Sie alle Dateiverweise auf diese Assembly, damit sie denselben Dateipfad für die ausgewählte Datei verwenden.  
  
## Siehe auch  
 [NICHT im BUILD: Assemblys](http://msdn.microsoft.com/de-de/6c5c7b30-fa78-4f40-b908-120d0743b0e6)   
 [Assemblys in der Common Language Runtime \(CLR\)](../Topic/Assemblies%20in%20the%20Common%20Language%20Runtime.md)   
 [Vorteile von Assemblys](../Topic/Assembly%20Benefits.md)   
 [Verwalten von Verweisen in einem Projekt](../ide/managing-references-in-a-project.md)   
 [NIB: Verwalten von Verweisen](http://msdn.microsoft.com/de-de/910912ce-0dc9-4569-9274-32c44a20cb2c)   
 [NICHT IM BUILD: Gewusst wie: Hinzufügen oder Entfernen von Verweisen mithilfe des Dialogfelds „Verweis hinzufügen“](http://msdn.microsoft.com/de-de/3bd75d61-f00c-47c0-86a2-dd1f20e231c9)