---
title: "&#39;D&#39; kann nicht mehr zur Angabe von Exponenten verwendet werden. Verwenden Sie stattdessen &#39;E&#39;. | Microsoft Docs"
ms.custom: ""
ms.date: "11/16/2016"
ms.prod: "visual-studio-dev14"
ms.reviewer: ""
ms.suite: ""
ms.technology: 
  - "devlang-visual-basic"
ms.tgt_pltfrm: ""
ms.topic: "article"
f1_keywords: 
  - "vbc30827"
  - "bc30827"
helpviewer_keywords: 
  - "BC30827"
ms.assetid: 577f8c0b-9e8a-433f-b504-9ddaa936c250
caps.latest.revision: 9
caps.handback.revision: 9
author: "stevehoag"
ms.author: "shoag"
manager: "wpickett"
---
# &#39;D&#39; kann nicht mehr zur Angabe von Exponenten verwendet werden. Verwenden Sie stattdessen &#39;E&#39;.
Der Buchstabe 'D' kann nicht für die Angabe von Potenzierung verwendet werden.  
  
 **Fehler\-ID:** BC30827  
  
### So beheben Sie diesen Fehler  
  
-   Verwenden Sie den Operator `^` oder den Buchstaben `E+`, um anzuzeigen, dass ein Exponent vorhanden ist. Zum Beispiel:  
  
    ```  
    Const Mole = 6.02E+23 ' Same as 6.02D23 Const Mole2 = 6.02 * 10 ^ 23 ' Same as 6.02D23  
    ```  
  
## Siehe auch  
 [^ Operator](/dotnet/visual-basic/language-reference/operators/exponentiation-operator)   
 [Numeric Data Types](/dotnet/visual-basic/programming-guide/language-features/data-types/numeric-data-types)