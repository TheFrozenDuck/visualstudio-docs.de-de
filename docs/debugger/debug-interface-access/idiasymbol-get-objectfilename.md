---
title: IDiaSymbol::get_objectFileName | Microsoft Docs
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology: vs-ide-debug
ms.tgt_pltfrm: 
ms.topic: article
dev_langs: C++
ms.assetid: 21793872-4879-4e4d-b527-dcf70aa7fb31
caps.latest.revision: "3"
author: mikejo5000
ms.author: mikejo
manager: ghogen
ms.workload: multiple
ms.openlocfilehash: e29812460d78c3b22db2c6a9941077a0fea00f70
ms.sourcegitcommit: 32f1a690fc445f9586d53698fc82c7debd784eeb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/22/2017
---
# <a name="idiasymbolgetobjectfilename"></a>IDiaSymbol::get_objectFileName
Ruft ab, der Name der Objektdatei.  
  
## <a name="syntax"></a>Syntax  
  
```C++  
HRESULT get_objectFilename(   
   BSTR *pRetVal);  
```  
  
#### <a name="parameters"></a>Parameter  
 `pRetVal`  
 [out] Ein Zeiger auf eine `BSTR` , enthält der Name der Objektdatei.  
  
## <a name="return-value"></a>Rückgabewert  
 Im Erfolgsfall gibt `S_OK`ist, andernfalls gibt `S_FALSE` oder ein Fehlercode.  
  
## <a name="see-also"></a>Siehe auch  
 [IDiaSymbol](../../debugger/debug-interface-access/idiasymbol.md)