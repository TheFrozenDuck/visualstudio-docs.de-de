---
title: IDebugComPlusSymbolProvider::GetNameFromToken | Microsoft Docs
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology: vs-ide-sdk
ms.tgt_pltfrm: 
ms.topic: article
helpviewer_keywords:
- IDebugComPlusSymbolProvider::GetNameFromToken
- GetNameFromToken
ms.assetid: 6e8cf468-5fd1-4655-93ed-88828d6068b7
caps.latest.revision: "9"
author: gregvanl
ms.author: gregvanl
manager: ghogen
ms.workload: vssdk
ms.openlocfilehash: 0cf48986fad6d445043f0c55602811f33efef3a6
ms.sourcegitcommit: 32f1a690fc445f9586d53698fc82c7debd784eeb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/22/2017
---
# <a name="idebugcomplussymbolprovidergetnamefromtoken"></a>IDebugComPlusSymbolProvider::GetNameFromToken
Gibt den Namen, die dem angegebenen Token erhält ihr Metadatenobjekt zugeordnet.  
  
## <a name="syntax"></a>Syntax  
  
```cpp  
HRESULT GetNameFromToken (  
   IUnknown* pMetadataImport,  
   DWORD     dwToken,  
   BSTR*     pbstrName  
);  
```  
  
```csharp  
int GetNameFromToken (  
   object     pMetadataImport,  
   uint       dwToken,  
   out string pbstrName  
);  
```  
  
#### <a name="parameters"></a>Parameter  
 `pMetadataImport`  
 [in] Ein Objekt, das die Metadateninformationen enthält.  
  
 `dwToken`  
 [in] Token benannt werden.  
  
 `pbstrName`  
 [out] Der Name, der das Token entspricht.  
  
## <a name="return-value"></a>Rückgabewert  
 Im Erfolgsfall gibt `S_OK`ist, andernfalls wird ein Fehlercode zurückgegeben.  
  
## <a name="example"></a>Beispiel  
 Das folgende Beispiel veranschaulicht die Implementierung dieser Methode für eine **CDebugSymbolProvider** -Objekt, das macht die [IDebugComPlusSymbolProvider](../../../extensibility/debugger/reference/idebugcomplussymbolprovider.md) Schnittstelle.  
  
```cpp  
HRESULT CDebugSymbolProvider::GetNameFromToken(  
    IUnknown* pMetadataImport,  
    DWORD dwToken,  
    BSTR* pbstrName  
)  
{  
    HRESULT hr = S_OK;  
    CComPtr<IMetaDataImport> pMetaData;  
  
    ASSERT(IsValidObjectPtr(this, CDebugSymbolProvider));  
    ASSERT(IsValidInterfacePtr(pMetadataImport, IUnknown));  
  
    METHOD_ENTRY(CDebugSymbolProvider::GetNameFromToken);  
  
    IfFalseGo( pMetadataImport && pbstrName, E_INVALIDARG );  
  
    *pbstrName = NULL;  
    IfFailGo( pMetadataImport->QueryInterface( IID_IMetaDataImport,  
              (void**) &pMetaData ) );  
  
    switch ( TypeFromToken(dwToken) )  
    {  
        case mdtModule:  
            IfFailGo( GetModuleName( pMetaData, dwToken, pbstrName) );  
            break;  
  
        case mdtTypeDef:  
            IfFailGo( GetTypeName( pMetaData, dwToken, pbstrName) );  
            break;  
  
        case mdtFieldDef:  
            IfFailGo( GetFieldName( pMetaData, dwToken, pbstrName) );  
            break;  
  
        case mdtMethodDef:  
            IfFailGo( GetMethodName( pMetaData, dwToken, pbstrName) );  
            break;  
  
        case mdtEvent:  
            IfFailGo( GetEventName( pMetaData, dwToken, pbstrName) );  
            break;  
  
        case mdtProperty:  
            IfFailGo( GetPropertyName( pMetaData, dwToken, pbstrName) );  
            break;  
  
        case mdtAssembly:  
            IfFailGo( GetAssemblyName( pMetaData, dwToken, pbstrName) );  
            break;  
  
        default:  
            ASSERT(!"Unsupported token passed to GetNameFromToken");  
            hr = E_FAIL;  
            break;  
    }  
  
Error:  
  
    METHOD_EXIT(CDebugSymbolProvider::GetNameFromToken, hr);  
    return hr;  
}  
```  
  
## <a name="see-also"></a>Siehe auch  
 [IDebugComPlusSymbolProvider](../../../extensibility/debugger/reference/idebugcomplussymbolprovider.md)