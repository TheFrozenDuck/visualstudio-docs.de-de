---
title: "Compilerfehler CS1621 | Microsoft Docs"
ms.custom: ""
ms.date: "11/23/2016"
ms.prod: "visual-studio-dev14"
ms.reviewer: ""
ms.suite: ""
ms.technology: 
  - "devlang-csharp"
ms.tgt_pltfrm: ""
ms.topic: "article"
f1_keywords: 
  - "CS1621"
dev_langs: 
  - "CSharp"
helpviewer_keywords: 
  - "CS1621"
ms.assetid: 11b4fb94-0dd7-4484-99aa-e06eacc6a658
caps.latest.revision: 10
caps.handback.revision: 10
author: "BillWagner"
ms.author: "wiwagn"
manager: "wpickett"
---
# Compilerfehler CS1621
Die yield\-Anweisung kann nicht in einer anonymen Methode oder einem Lambda\-Ausdruck verwendet werden.  
  
 Die yield\-Anweisung kann nicht in einem anonymen Methodenblock in einem Iterator sein.  
  
## Beispiel  
 Im folgenden Beispiel wird CS1621 generiert:  
  
```  
// CS1621.cs using System.Collections; delegate object MyDelegate(); class C : IEnumerable { public IEnumerator GetEnumerator() { MyDelegate d = delegate { yield return this; // CS1621 return this; }; d(); // Try this instead: // MyDelegate d = delegate { return this; }; // yield return d(); } public static void Main() { } }  
```  
  
## Siehe auch  
 [Iteratoren](../Topic/Iterators%20\(C%23%20and%20Visual%20Basic\).md)   
 [yield](/dotnet/csharp/language-reference/keywords/yield)   
 [Lambda\-Ausdrücke](/dotnet/csharp/programming-guide/statements-expressions-operators/lambda-expressions)   
 [Anonyme Methoden](/dotnet/csharp/programming-guide/statements-expressions-operators/anonymous-methods)