---
title: "Compilerfehler CS0516 | Microsoft Docs"
ms.custom: ""
ms.date: "10/29/2016"
ms.prod: "visual-studio-dev14"
ms.reviewer: ""
ms.suite: ""
ms.technology: 
  - "devlang-csharp"
ms.tgt_pltfrm: ""
ms.topic: "article"
f1_keywords: 
  - "CS0516"
dev_langs: 
  - "CSharp"
helpviewer_keywords: 
  - "CS0516"
ms.assetid: a9de9d1d-9ee3-4533-ba31-b8cb9f9964a1
caps.latest.revision: 6
caps.handback.revision: 6
author: "BillWagner"
ms.author: "wiwagn"
manager: "wpickett"
---
# Compilerfehler CS0516
Konstruktor „constructor“ kann sich nicht selbst aufrufen.  
  
 Ein Programm kann nicht rekursiv Konstruktoren aufrufen.  
  
 Im folgenden Beispiel wird CS0516 generiert:  
  
```  
// CS0516.cs namespace x { public class clx { public clx() : this()   // CS0516, delete "this()" { } public static void Main() { } } }  
```