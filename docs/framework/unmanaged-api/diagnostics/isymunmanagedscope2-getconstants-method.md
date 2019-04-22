---
title: ISymUnmanagedScope2::GetConstants, méthode
ms.date: 03/30/2017
api_name:
- ISymUnmanagedScope2.GetConstants
api_location:
- diasymreader.dll
api_type:
- COM
f1_keywords:
- ISymUnmanagedScope2::GetConstants
helpviewer_keywords:
- ISymUnmanagedScope2::GetConstants method [.NET Framework debugging]
- GetConstants method [.NET Framework debugging]
ms.assetid: f241b620-9ec5-42fd-92ef-3b22329db72a
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: 08bc85c7a5b53c145375ca34f11ec499e5e7528f
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59096821"
---
# <a name="isymunmanagedscope2getconstants-method"></a>ISymUnmanagedScope2::GetConstants, méthode
Obtient les variables constantes définies dans cette portée.  
  
## <a name="syntax"></a>Syntaxe  
  
```  
HRESULT GetConstants(  
     [in]  ULONG32  cConstants,  
     [out] ULONG32  *pcConstants,  
     [out, size_is(cConstants),  
         length_is(*pcConstants)] ISymUnmanagedConstant*   
             constants[]);  
```  
  
## <a name="parameters"></a>Paramètres  
 `cConstants`  
 [in] La longueur de la mémoire tampon qui le `pcConstants` paramètre pointe vers.  
  
 `pcConstants`  
 [out] Un pointeur vers un `ULONG32` qui reçoit la taille, en caractères, de la mémoire tampon requise pour contenir les constantes.  
  
 `constants`  
 [out] La mémoire tampon qui stocke les constantes.  
  
## <a name="return-value"></a>Valeur de retour  
 S_OK si la méthode réussit ; Sinon, E_FAIL ou un autre code d’erreur.  
  
## <a name="requirements"></a>Configuration requise  
 **En-tête :** CorSym.idl, CorSym.h  
  
## <a name="see-also"></a>Voir aussi

- [ISymUnmanagedScope2, interface](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedscope2-interface.md)
