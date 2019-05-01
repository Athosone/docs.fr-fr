---
title: ICorDebugManagedCallback::BreakpointSetError, méthode
ms.date: 03/30/2017
api_name:
- ICorDebugManagedCallback.BreakpointSetError
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugManagedCallback::BreakpointSetError
helpviewer_keywords:
- BreakpointSetError method [.NET Framework debugging]
- ICorDebugManagedCallback::BreakpointSetError method [.NET Framework debugging]
ms.assetid: f2b773a4-c4d0-429c-9717-51d6e2ed86af
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 27d5b8e0127971cc3a46560590fd9d95f0ffd1f0
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61988323"
---
# <a name="icordebugmanagedcallbackbreakpointseterror-method"></a>ICorDebugManagedCallback::BreakpointSetError, méthode
Notifie le débogueur que le common language runtime n’a pas pu lier correctement un point d’arrêt a été défini avant une fonction compilée juste-à-temps (JIT).  
  
## <a name="syntax"></a>Syntaxe  
  
```  
HRESULT BreakpointSetError (  
    [in] ICorDebugAppDomain  *pAppDomain,  
    [in] ICorDebugThread     *pThread,  
    [in] ICorDebugBreakpoint *pBreakpoint,  
    [in] DWORD                dwError  
);  
```  
  
## <a name="parameters"></a>Paramètres  
 `pAppDomain`  
 [in] Pointeur vers un objet ICorDebugAppDomain qui représente le domaine d’application qui contient le point d’arrêt indépendant.  
  
 `pThread`  
 [in] Pointeur vers un objet ICorDebugThread qui représente le thread qui contient le point d’arrêt indépendant.  
  
 `pBreakpoint`  
 [in] Pointeur vers un objet ICorDebugBreakpoint qui représente le point d’arrêt indépendant.  
  
 `dwError`  
 [in] Entier qui indique l’erreur.  
  
## <a name="remarks"></a>Notes  
 Le point d’arrêt donné ne sera jamais atteint. Le débogueur doit désactiver et reconnectez-la.  
  
## <a name="requirements"></a>Configuration requise  
 **Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).  
  
 **En-tête :** CorDebug.idl, CorDebug.h  
  
 **Bibliothèque :** CorGuids.lib  
  
 **Versions du .NET Framework :** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]  
  
## <a name="see-also"></a>Voir aussi

- [ICorDebugManagedCallback, interface](../../../../docs/framework/unmanaged-api/debugging/icordebugmanagedcallback-interface.md)
