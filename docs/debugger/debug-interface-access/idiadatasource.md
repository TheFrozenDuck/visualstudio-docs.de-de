---
title: IDiaDataSource | Microsoft Docs
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology: vs-ide-debug
ms.tgt_pltfrm: 
ms.topic: article
dev_langs: C++
helpviewer_keywords: IDiaDataSource interface
ms.assetid: 6260ac76-4f9d-4144-ba22-32f8620b32c2
caps.latest.revision: "13"
author: mikejo5000
ms.author: mikejo
manager: ghogen
ms.workload: multiple
ms.openlocfilehash: 51a277d9ff1bf190aa87d7c4e9d8d852f8c38323
ms.sourcegitcommit: 32f1a690fc445f9586d53698fc82c7debd784eeb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/22/2017
---
# <a name="idiadatasource"></a>IDiaDataSource
Initiiert den Zugriff auf Debugsymbole Quelle.  
  
## <a name="syntax"></a>Syntax  
  
```  
IDiaDataSource : IUnknown  
```  
  
## <a name="methods-in-vtable-order"></a>Methoden in Vtable-Reihenfolge  
 Die folgende Tabelle zeigt die Methoden der `IDiaDataSource`.  
  
|Methode|Beschreibung|  
|------------|-----------------|  
|[IDiaDataSource::get_lastError](../../debugger/debug-interface-access/idiadatasource-get-lasterror.md)|Ruft den Dateinamen für die letzten Ladefehler ab.|  
|[IDiaDataSource::loadDataFromPdb](../../debugger/debug-interface-access/idiadatasource-loaddatafrompdb.md)|Wird geöffnet, und bereitet eine Programmdatenbankdatei (.pdb) als Datenquelle Debuggen.|  
|[IDiaDataSource::loadAndValidateDataFromPdb](../../debugger/debug-interface-access/idiadatasource-loadandvalidatedatafrompdb.md)|Wird geöffnet und überprüft, ob die Programmdatenbankdatei (.pdb) bereitgestellten Signaturinformationen übereinstimmt; Bereitet die PDB-Datei als Datenquelle Debuggen.|  
|[IDiaDataSource::loadDataForExe](../../debugger/debug-interface-access/idiadatasource-loaddataforexe.md)|Wird geöffnet, und bereitet die Debugdaten der.exe/.dll-Datei zugeordnet.|  
|[IDiaDataSource::loadDataFromIStream](../../debugger/debug-interface-access/idiadatasource-loaddatafromistream.md)|Bereitet die Debugdaten in ein Zugriff erfolgt über ein in-Memory-Datenstrom Programmdatenbankdatei (PDB) gespeichert.|  
|[IDiaDataSource::openSession](../../debugger/debug-interface-access/idiadatasource-opensession.md)|Öffnet eine Sitzung für die Abfrage von Symbolen.|  
  
## <a name="remarks"></a>Hinweise  
 Aufrufen einer der Load-Methoden in der die `IDiaDataSource` Schnittstelle öffnet die Symbol-Quelle. Ein erfolgreicher Aufruf der [idiadatasource:: OpenSession](../../debugger/debug-interface-access/idiadatasource-opensession.md) Methode gibt ein [IDiaSession](../../debugger/debug-interface-access/idiasession.md) -Schnittstelle, die unterstützt das Abfragen der Datenquelle. Wenn die Load-Methode einen Datei-bezogener Fehler zurückgibt und dann die [idiadatasource:: Get_lasterror](../../debugger/debug-interface-access/idiadatasource-get-lasterror.md) Methodenrückgabewert Wert enthält den Dateinamen, die dem Fehler zugeordnet.  
  
## <a name="notes-for-callers"></a>Hinweise für Aufrufer  
 Diese Schnittstelle wird abgerufen, durch den Aufruf der `CoCreateInstance` -Funktion mit dem Klassen-ID `CLSID_DiaSource` und die Schnittstellen-ID `IID_IDiaDataSource`. Im Beispiel wird gezeigt, wie diese Schnittstelle abgerufen wird.  
  
## <a name="example"></a>Beispiel  
  
```C++  
  
      IDiaDataSource* pSource;  
HRESULT hr = CoCreateInstance(CLSID_DiaSource,  
                              NULL,  
                              CLSCTX_INPROC_SERVER,  
                              IID_IDiaDataSource,  
                              (void**) &pSource);  
if (FAILED(hr))  
{  
    // Report error and exit  
}  
```  
  
## <a name="requirements"></a>Anforderungen  
 Header: Dia2.h  
  
 Bibliothek: diaguids.lib  
  
 DLL: "MSDIA80.dll"  
  
## <a name="see-also"></a>Siehe auch  
 [Schnittstellen (Debug Interface Access SDK)](../../debugger/debug-interface-access/interfaces-debug-interface-access-sdk.md)