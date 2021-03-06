---
title: "Compilerfehler CS0209 | Microsoft Docs"
ms.custom: ""
ms.date: "11/16/2016"
ms.prod: "visual-studio-dev14"
ms.reviewer: ""
ms.suite: ""
ms.technology: 
  - "devlang-csharp"
ms.tgt_pltfrm: ""
ms.topic: "article"
f1_keywords: 
  - "CS0209"
dev_langs: 
  - "CSharp"
helpviewer_keywords: 
  - "CS0209"
ms.assetid: a408a869-02db-414f-97c1-bfb1637f6155
caps.latest.revision: 9
caps.handback.revision: 9
author: "BillWagner"
ms.author: "wiwagn"
manager: "wpickett"
---
# Compilerfehler CS0209
Der Typ einer in einer fixed\-Anweisung deklarierten lokalen Variablen muss ein Zeigertyp sein.  
  
 Die in einer [fixed\-Anweisung](/dotnet/csharp/language-reference/keywords/fixed-statement) deklarierte lokale Variable muss ein Zeiger sein. Weitere Informationen finden Sie unter [Unsicherer Code und Zeiger](/dotnet/csharp/programming-guide/unsafe-code-pointers/index).  
  
 Im folgenden Beispiel wird CS0209 generiert:  
  
```  
// CS0209.cs // compile with: /unsafe class Point { public int x, y; } public class MyClass { unsafe public static void Main() { Point pt = new Point(); fixed (int i)    // CS0209 { } // try the following lines instead /* fixed (int* p = &pt.x) { } fixed (int* q = &pt.y) { } */ } }  
```