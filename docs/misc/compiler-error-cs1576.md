---
title: "Compilerfehler CS1576 | Microsoft Docs"
ms.custom: ""
ms.date: "11/17/2016"
ms.prod: "visual-studio-dev14"
ms.reviewer: ""
ms.suite: ""
ms.technology: 
  - "devlang-csharp"
ms.tgt_pltfrm: ""
ms.topic: "article"
f1_keywords: 
  - "CS1576"
dev_langs: 
  - "CSharp"
helpviewer_keywords: 
  - "CS1576"
ms.assetid: 3e39cb80-e7de-4c78-a22a-57e267121a96
caps.latest.revision: 7
caps.handback.revision: 7
author: "BillWagner"
ms.author: "wiwagn"
manager: "wpickett"
---
# Compilerfehler CS1576
Die Zeilennummer, die für die \#line\-Direktive angegeben wurde, fehlt oder ist ungültig.  
  
 Der Compiler hat einen Fehler bei dem an die [\#line](/dotnet/csharp/language-reference/preprocessor-directives/preprocessor-line)\-Direktive übergebenen Wert erkannt.  
  
 Im folgenden Beispiel wird CS1576 generiert:  
  
```  
// CS1576.cs public class MyClass { static void Main() { #line "abc.sc"         // CS1576 // try the following line instead //#line  101 "abc.sc" intt i;  // error will be reported on line 101 } }  
```