---
title: "Operatoren m&#252;ssen als „Shared“ deklariert werden. | Microsoft Docs"
ms.custom: ""
ms.date: "11/17/2016"
ms.prod: "visual-studio-dev14"
ms.reviewer: ""
ms.suite: ""
ms.technology: 
  - "devlang-visual-basic"
ms.tgt_pltfrm: ""
ms.topic: "article"
f1_keywords: 
  - "vbc33012"
  - "bc33012"
helpviewer_keywords: 
  - "BC33012"
ms.assetid: 5ad97616-4032-46cd-aaf7-517db5d1195f
caps.latest.revision: 9
caps.handback.revision: 9
author: "stevehoag"
ms.author: "shoag"
manager: "wpickett"
---
# Operatoren m&#252;ssen als „Shared“ deklariert werden.
Ein [Operator Statement](/dotnet/visual-basic/language-reference/statements/operator-statement) enthält das Schlüsselwort [Shared](/dotnet/visual-basic/language-reference/modifiers/shared) nicht.  
  
 Eine `Operator`\-Prozedur erfordert sowohl das [Public](/dotnet/visual-basic/language-reference/modifiers/public)\-Schlüsselwort als auch das `Shared`\-Schlüsselwort, und ein Konvertierungsoperator erfordert auch entweder das [Widening](/dotnet/visual-basic/language-reference/modifiers/widening)\-Schlüsselwort oder das [Narrowing](/dotnet/visual-basic/language-reference/modifiers/narrowing)\-Schlüsselwort.  
  
 **Fehler\-ID:** BC33012  
  
### So beheben Sie diesen Fehler  
  
-   Fügen Sie der `Operator`\-Anweisung das `Shared`\-Schlüsselwort hinzu.  
  
## Siehe auch  
 [Operator Procedures](/dotnet/visual-basic/programming-guide/language-features/procedures/operator-procedures)   
 [Operator Statement](/dotnet/visual-basic/language-reference/statements/operator-statement)   
 [How to: Define an Operator](../Topic/How%20to:%20Define%20an%20Operator%20\(Visual%20Basic\).md)   
 [How to: Define a Conversion Operator](../Topic/How%20to:%20Define%20a%20Conversion%20Operator%20\(Visual%20Basic\).md)