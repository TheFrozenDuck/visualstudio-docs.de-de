---
title: "&lt;signature&gt; (JavaScript) | Microsoft Docs"
ms.custom: ""
ms.date: "12/02/2016"
ms.prod: "visual-studio-dev14"
ms.reviewer: ""
ms.suite: ""
ms.technology: 
  - "vs-ide-general"
ms.tgt_pltfrm: ""
ms.topic: "article"
helpviewer_keywords: 
  - "<signature>-JavaScript-XML-Tag"
  - "signature-JavaScript-XML-Tag"
ms.assetid: 319138e7-cfbe-4b37-9643-2ddb7f9c63d4
caps.latest.revision: 12
caps.handback.revision: 12
author: "kempb"
ms.author: "kempb"
manager: "ghogen"
---
# &lt;signature&gt; (JavaScript)
[!INCLUDE[vs2017banner](../code-quality/includes/vs2017banner.md)]

Gruppiert einen Satz zugehöriger Elementen für eine Funktion oder Methode, um eine Dokumentation für überladene Funktionen bereitzustellen.  
  
## Syntax  
  
```  
<signature externalid="id" externalFile="filename"  
    helpKeyword="keyword" locid="descriptionID">  
</signature>  
  
```  
  
#### Parameter  
 `externalid`  
 Optional.  Wenn das `format`\-Attribut für das [\<loc\>](../ide/loc-javascript.md)\-Element `vsdoc` ist, gibt dieses Attribut die Member\-ID an, die verwendet wird, um den XML\-Code zu suchen, der der Signatur zugeordnet ist.  Anders als das `locid`\-Attribut gibt dieses Attribut an, dass alle Elemente im Member, der diese ID aufweist, geladen werden sollen.  Alle zugeordneten Beschreibungsinformationen, die im XML\-Code vorhanden sind, werden auch mit den Elementen zusammengeführt, die in der Signatur angegeben sind.  Dies ermöglicht es Ihnen, zusätzliche Elemente, wie `<capability>`, in der Sidecardatei anzugeben, ohne sie in der Quelldatei anzugeben.  `externalid` ist ein optionales Attribut.  
  
 `externalFile`  
 Optional.  Gibt den Namen der Datei an, in der `externalid` zu finden ist.  Dieses Attribut wird ignoriert, wenn kein `externalid` vorhanden ist.  Dies ist ein optionales Attribut.  Der Standardwert ist der Name der aktuellen Datei, jedoch mit einer XML\-Erweiterung anstelle von JS.  Standardmäßig werden Suchregeln für verwaltete Ressourcen für die Lokalisierung verwendet, um die Datei zu suchen.  
  
 `helpKeyword`  
 Optional.  Das Schlüsselwort für die F1\-Hilfe.  
  
 `locid`  
 Optional.  Der Bezeichner für Lokalisierungsinformationen über das Feld.  Der Bezeichner ist entweder eine Member\-ID, oder er entspricht dem `name`\-Attributwert in einem Meldungsbündel, das von OpenAjax\-Metadaten definiert wird.  Der Bezeichnertyp hängt vom Format ab, das im Tag [\<loc\>](../ide/loc-javascript.md) angegeben wird.  
  
## Hinweise  
 Verwenden Sie ein `<signature>`\-Element für jede der überladenen Funktionsbeschreibung in der JS\-Datei, oder verwenden Sie ein `<signature>`\-Element für jede angegebene externe Member\-ID.  
  
 Das `<signature>`\-Element muss im Funktionstext vor allen Anweisungen eingefügt werden.  Wenn Sie die Elemente [\<summary\>](../ide/summary-javascript.md), [\<param\>](../ide/param-javascript.md) oder [\<returns\>](../ide/returns-javascript.md) mit dem `<signature>`\-Element verwenden, fügen Sie die anderen Elemente innerhalb des `<signature>`\-Blocks ein.  
  
## Beispiel  
 Im folgenden Codebeispiel wird die Verwendung des Elements `<signature>` veranschaulicht.  
  
```javascript  
// Use of <signature> with externalid.  
// Requires use of the <loc> tag to identify the external functions.  
function illuminate(light) {  
    /// <signature externalid='M:Windows.Devices.Light.Illuminate()' />  
    /// <signature externalid='M:Windows.Devices.Light.Illuminate(System.Int32)'>  
    ///   <param name='light' type='Number' />  
    /// </signature>  
}  
  
// Use of <signature> for overloads implemented in JavaScript.  
function add(a, b) {  
    /// <signature>  
    /// <summary>function summary 1</summary>  
    /// <param name="a" type="Number">The first number</param>  
    /// <param name="b" type="Number">The second number</param>  
    /// <returns type="Number" />  
    /// </signature>  
    /// <signature>  
    /// <summary>function summary 2 – differ by number of params</summary>  
    /// <param name="a" type="Number">Only 1 parameter</param>  
    /// <returns type="Number" />  
    /// </signature>  
    /// <signature>  
    /// <summary>function summary 3 – differ by parameter type</summary>  
    /// <param name="a" type="Number">Number parameter</param>  
    /// <param name="b" type="String">String parameter</param>  
    /// <returns type="Number" />  
    /// </signature>  
    /// <signature>  
    /// <summary>function summary 4 – differ by return type</summary>  
    /// <param name="a" type="Number">The first number</param>  
    /// <param name="b" type="Number">The second number</param>  
    /// <returns type="String" />  
    /// </signature>  
  
    return a + b;  
}  
```  
  
## Siehe auch  
 [XML\-Dokumentationskommentare](../ide/xml-documentation-comments-javascript.md)