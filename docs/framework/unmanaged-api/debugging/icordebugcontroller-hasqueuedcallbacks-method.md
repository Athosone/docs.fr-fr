---
title: ICorDebugController::HasQueuedCallbacks, méthode
ms.date: 03/30/2017
api_name:
- ICorDebugController.HasQueuedCallbacks
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugController::HasQueuedCallbacks
helpviewer_keywords:
- HasQueuedCallbacks method [.NET Framework debugging]
- ICorDebugController::HasQueuedCallbacks method [.NET Framework debugging]
ms.assetid: 0d6a1cd9-370b-4462-adbf-e3980e897ea7
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: ce6ad24e5e670db21d3a6942ab4650a68ae44568
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59102690"
---
# <a name="icordebugcontrollerhasqueuedcallbacks-method"></a>ICorDebugController::HasQueuedCallbacks, méthode
Obtient une valeur qui indique si des rappels managés sont actuellement en file d’attente pour le thread spécifié.  
  
## <a name="syntax"></a>Syntaxe  
  
```  
HRESULT HasQueuedCallbacks (  
    [in] ICorDebugThread *pThread,  
    [out] BOOL           *pbQueued  
);  
```  
  
## <a name="parameters"></a>Paramètres  
 `pThread`  
 [in] Pointeur vers un objet « ICorDebugThread » qui représente le thread.  
  
 `pbQueued`  
 [out] Un pointeur vers une valeur qui est `true` si des rappels managés sont actuellement en file d’attente pour le thread spécifié ; sinon, `false`.  
  
 Si null est spécifié pour le `pThread` paramètre, `HasQueuedCallbacks` retournera `true` s’il existe actuellement géré les rappels en attente de n’importe quel thread.  
  
## <a name="remarks"></a>Notes  
 Les rappels sont distribués un par un, chaque fois [ICorDebugController::Continue](../../../../docs/framework/unmanaged-api/debugging/icordebugcontroller-continue-method.md) est appelée. Le débogueur peut contrôler cet indicateur si elle souhaite créer un rapport se produisent simultanément plusieurs événements de débogage.  
  
 Lorsque les événements de débogage sont en attente, ils ont déjà eu lieu, afin du débogueur doit vider la file d’attente entière pour être sûr que de l’état de l’élément débogué. (Appelez `ICorDebugController::Continue` pour vider la file d’attente.) Par exemple, si la file d’attente contient deux événements de débogage sur le thread *X*, et le débogueur suspend le thread *X* après le premier événement de débogage, puis appelle `ICorDebugController::Continue`, le deuxième événement de débogage pour thread *X* seront distribués bien que le thread a été suspendu.  
  
## <a name="requirements"></a>Configuration requise  
 **Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).  
  
 **En-tête :** CorDebug.idl, CorDebug.h  
  
 **Bibliothèque :** CorGuids.lib  
  
 **Versions du .NET Framework :** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]  
  
## <a name="see-also"></a>Voir aussi
