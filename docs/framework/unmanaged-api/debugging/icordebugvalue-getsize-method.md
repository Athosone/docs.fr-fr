---
title: ICorDebugValue::GetSize, méthode
ms.date: 03/30/2017
api_name:
- ICorDebugValue.GetSize
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugValue::GetSize
helpviewer_keywords:
- GetSize method, ICorDebugValue interface [.NET Framework debugging]
- ICorDebugValue::GetSize method [.NET Framework debugging]
ms.assetid: 445a9ee3-e050-4f3a-931a-96b0efb00110
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 41a9ff2c94c98a5acc930d68e648b0ea577a82c3
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61986841"
---
# <a name="icordebugvaluegetsize-method"></a>ICorDebugValue::GetSize, méthode
Obtient la taille, en octets, de cet objet « ICorDebugValue ».  
  
## <a name="syntax"></a>Syntaxe  
  
```  
HRESULT GetSize (  
    [out] ULONG32   *pSize  
);  
```  
  
## <a name="parameters"></a>Paramètres  
 `pSize`  
 [out] La taille, en octets, de cet objet de valeur.  
  
## <a name="remarks"></a>Notes  
 Si le type de valeur est un type référence, cette méthode retourne la taille du pointeur plutôt que la taille de l’objet.  
  
 Le `ICorDebugValue::GetSize` retourne de la méthode `COR_E_OVERFLOW` pour les objets qui sont supérieurs à 4 Go sur les plateformes 64 bits. Utilisez le [ICorDebugValue3::GetSize64](../../../../docs/framework/unmanaged-api/debugging/icordebugvalue3-getsize64-method.md) méthode à la place pour les objets qui sont supérieurs à 4 Go.  
  
## <a name="requirements"></a>Configuration requise  
 **Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).  
  
 **En-tête :** CorDebug.idl, CorDebug.h  
  
 **Bibliothèque :** CorGuids.lib  
  
 **Versions du .NET Framework :** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]  
  
## <a name="see-also"></a>Voir aussi

- [GetSize64, méthode](../../../../docs/framework/unmanaged-api/debugging/icordebugvalue3-getsize64-method.md)
