---
title: "TextFieldParser unterst&#252;tzt keine Kommentartoken, die Leerzeichen enthalten. | Microsoft Docs"
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
  - "vbrTextFieldParser_WhitespaceInToken"
ms.assetid: 55107656-270e-4bbb-841a-478904df8e07
caps.latest.revision: 8
caps.handback.revision: 8
author: "stevehoag"
ms.author: "shoag"
manager: "wpickett"
---
# TextFieldParser unterst&#252;tzt keine Kommentartoken, die Leerzeichen enthalten.
Es wurde ein Kommentartoken bereitgestellt, das Leerzeichen enthält. Der `TextFieldParser` unterstützt keine Kommentartoken, die Leerzeichen enthalten, es sei denn, die Leerzeichen befinden sich am Anfang des Tokens. Leerzeichen, die sich am Anfang eines Tokens befinden, werden ignoriert.  
  
### So beheben Sie diesen Fehler  
  
-   Geben Sie ein ordnungsgemäßes Kommentartoken an.  
  
## Siehe auch  
 [TextFieldParser.CommentTokens\-Eigenschaft](http://msdn.microsoft.com/de-de/2e6b6435-4bee-4c14-a353-e8f2c82e2d61)   
 [Parsing Text Files with the TextFieldParser Object](/dotnet/visual-basic/developing-apps/programming/drives-directories-files/parsing-text-files-with-the-textfieldparser-object)   
 [TextFieldParser Object](/dotnet/visual-basic/language-reference/objects/textfieldparser-object)