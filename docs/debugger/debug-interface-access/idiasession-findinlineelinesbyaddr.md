---
title: IDiaSession::findInlineeLinesByAddr | Microsoft Docs
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology: vs-ide-debug
ms.tgt_pltfrm: 
ms.topic: article
dev_langs: C++
ms.assetid: bb70e408-eed1-4c9c-b5b1-44323125f48b
caps.latest.revision: "3"
author: mikejo5000
ms.author: mikejo
manager: ghogen
ms.workload: multiple
ms.openlocfilehash: 18767e591d2fa22c78207b109861ed3ea4c091c0
ms.sourcegitcommit: 32f1a690fc445f9586d53698fc82c7debd784eeb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/22/2017
---
# <a name="idiasessionfindinlineelinesbyaddr"></a>IDiaSession::findInlineeLinesByAddr
Ruft eine Enumeration, die ermöglicht einem Client zu durchlaufen und die Zeilennummerninformationen aller Funktionen, die inline erweitert wird, direkt oder indirekt mit dem angegebenen übergeordneten-Symbol, und innerhalb der angegebenen Adressbereich enthalten sind.  
  
## <a name="syntax"></a>Syntax  
  
```C++  
HRESULT findInlineeLinesByAddr (   
   IDiaSymbol*           parent,   DWORD                 isect,   DWORD                 offset,   DWORD                 length,  
   IDiaEnumLineNumbers** ppResult  
);  
```  
  
#### <a name="parameters"></a>Parameter  
 `parent`  
 [in] Ein `IDiaSymbol` Objekt, das das übergeordnete Element darstellt.  
  
 `isect`  
 [in] Gibt die Komponente im Abschnitt der Adresse.  
  
 `offset`  
 [in] Gibt den Offset-Komponente der Adresse an.  
  
 `length`  
 [in] Gibt an, der Adressbereich in Anzahl von Bytes, die mit dieser Abfrage abzudecken.  
  
 `ppResult`  
 [out] Enthält eine `IDiaEnumLineNumbers` -Objekt, das die Liste der Zeilennummern enthält, die abgerufen werden.  
  
## <a name="return-value"></a>Rückgabewert  
 Im Erfolgsfall gibt `S_OK`ist, andernfalls wird ein Fehlercode zurückgegeben.  
  
## <a name="see-also"></a>Siehe auch  
 [IDiaSession](../../debugger/debug-interface-access/idiasession.md)   
 [IDiaSymbol](../../debugger/debug-interface-access/idiasymbol.md)   
 [SymTagEnum-Enumeration](../../debugger/debug-interface-access/symtagenum.md)   
 [IDiaEnumLineNumbers](../../debugger/debug-interface-access/idiaenumlinenumbers.md)