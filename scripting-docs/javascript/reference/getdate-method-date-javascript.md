---
title: GetDate-Methode (Datum) (JavaScript) | Microsoft Docs
ms.custom: 
ms.date: 01/18/2017
ms.prod: windows-client-threshold
ms.reviewer: 
ms.suite: 
ms.technology: devlang-javascript
ms.tgt_pltfrm: 
ms.topic: language-reference
f1_keywords: getDate
dev_langs:
- JavaScript
- TypeScript
- DHTML
helpviewer_keywords:
- Date object
- dates, returning day of the month
- getDate method
ms.assetid: 67e7f07c-dd46-4b42-82d6-e53e4bd33703
caps.latest.revision: "20"
author: mikejo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: bfb3a8ad3ba433dc776f0831d1eac4787b8aea90
ms.sourcegitcommit: aadb9588877418b8b55a5612c1d3842d4520ca4c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2017
---
# <a name="getdate-method-date-javascript"></a>getDate-Methode (Datum) (JavaScript)
Ruft die Tag-des-Monats, unter Verwendung der Ortszeit ab.  
  
## <a name="syntax"></a>Syntax  
  
```  
  
dateObj.getDate()   
```  
  
#### <a name="parameters"></a>Parameter  
 Der erforderliche `dateObj` -Verweis ist ein `Date` -Objekt.  
  
## <a name="return-value"></a>Rückgabewert  
 Eine ganze Zahl zwischen 1 und 31, die den Tag-des-Monats darstellt.  
  
## <a name="remarks"></a>Hinweise  
 Verwenden Sie zum Abrufen der Tag-des-Monats Universal Coordinated Time (UTC) mithilfe der `getUTCDate` Methode.  
  
## <a name="example"></a>Beispiel  
 Im folgenden Beispiel wird die Verwendung der `getDate`-Methode veranschaulicht.  
  
```JavaScript  
var date = new Date("Jan 01, 2001");  
var str = "Today's date is: ";  
   str += (date.getMonth() + 1) + "/";  
   str += date.getDate() + "/";  
   str += date.getFullYear();  
document.write(str);  
  
// Output: Today's date is: 1/1/2001  
  
```  
  
## <a name="requirements"></a>Anforderungen  
 [!INCLUDE[jsv1](../../javascript/misc/includes/jsv1-md.md)]  
  
 **Gilt für**: [Date Object](../../javascript/reference/date-object-javascript.md)  
  
## <a name="see-also"></a>Siehe auch  
 [GetUTCDate-Methode (Datum)](../../javascript/reference/getutcdate-method-date-javascript.md)   
 [SetDate-Methode (Datum)](../../javascript/reference/setdate-method-date-javascript.md)   
 [setUTCDate-Methode (Datum)](../../javascript/reference/setutcdate-method-date-javascript.md)