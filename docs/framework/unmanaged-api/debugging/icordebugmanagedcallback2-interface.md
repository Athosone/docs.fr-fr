---
title: ICorDebugManagedCallback2, interface
ms.date: 03/30/2017
api_name:
- ICorDebugManagedCallback2
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugManagedCallback2
helpviewer_keywords:
- ICorDebugManagedCallback2 interface [.NET Framework debugging]
ms.assetid: cf7b7cfa-1c4b-4d8c-be70-4f9ed15a788b
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: f1ecfea208f87f53f15fcc4cdafb58341c293e43
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61763813"
---
# <a name="icordebugmanagedcallback2-interface"></a>ICorDebugManagedCallback2, interface
Fournit des méthodes pour prendre en charge la gestion des exceptions et les Assistants Débogage managé (MDA) du débogueur. `ICorDebugManagedCallback2` est une extension logique de la [ICorDebugManagedCallback](../../../../docs/framework/unmanaged-api/debugging/icordebugmanagedcallback-interface.md) interface.  
  
## <a name="methods"></a>Méthodes  
  
|Méthode|Description|  
|------------|-----------------|  
|[ChangeConnection, méthode](../../../../docs/framework/unmanaged-api/debugging/icordebugmanagedcallback2-changeconnection-method.md)|Notifie le débogueur que l’ensemble des tâches associées à la connexion spécifiée a changé.|  
|[CreateConnection, méthode](../../../../docs/framework/unmanaged-api/debugging/icordebugmanagedcallback2-createconnection-method.md)|Notifie le débogueur qu’une nouvelle connexion a été créée.|  
|[DestroyConnection, méthode](../../../../docs/framework/unmanaged-api/debugging/icordebugmanagedcallback2-destroyconnection-method.md)|Notifie le débogueur que la connexion spécifiée a été arrêtée.|  
|[Exception, méthode](../../../../docs/framework/unmanaged-api/debugging/icordebugmanagedcallback2-exception-method.md)|Notifie le débogueur qu’une recherche pour un gestionnaire d’exceptions a démarré.|  
|[ExceptionUnwind, méthode](../../../../docs/framework/unmanaged-api/debugging/icordebugmanagedcallback2-exceptionunwind-method.md)|Fournit une notification d’état pendant le processus de déroulement d’exception.|  
|[FunctionRemapComplete, méthode](../../../../docs/framework/unmanaged-api/debugging/icordebugmanagedcallback2-functionremapcomplete-method.md)|Notifie le débogueur que l’exécution de code a basculé vers une nouvelle version d’une fonction modifiée.|  
|[FunctionRemapOpportunity, méthode](../../../../docs/framework/unmanaged-api/debugging/icordebugmanagedcallback2-functionremapopportunity-method.md)|Notifie le débogueur que l’exécution de code a atteint un point de séquence dans une version antérieure d’une fonction modifiée.|  
|[MDANotification, méthode](../../../../docs/framework/unmanaged-api/debugging/icordebugmanagedcallback2-mdanotification-method.md)|Fournit une notification que l’exécution de code a rencontré un message (MDA) de l’assistant débogage managé.|  
  
## <a name="remarks"></a>Notes  
 Le `ICorDebugManagedCallback2` interface étend la `ICorDebugManagedCallback` permettant de gérer les nouveaux événements de débogage introduites dans le .NET Framework version 2.0.  
  
 Un débogueur doit implémenter `ICorDebugManagedCallback2` s’il débogue des applications .NET Framework 2.0. Une instance de `ICorDebugManagedCallback` ou `ICorDebugManagedCallback2` est passé en tant qu’objet de rappel à [ICorDebug::SetManagedHandler](../../../../docs/framework/unmanaged-api/debugging/icordebug-setmanagedhandler-method.md).  
  
> [!NOTE]
>  Cette interface ne prend pas en charge l'appel à distance, que ce soit entre ordinateurs ou entre processus.  
  
## <a name="requirements"></a>Configuration requise  
 **Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).  
  
 **En-tête :** CorDebug.idl, CorDebug.h  
  
 **Bibliothèque :** CorGuids.lib  
  
 **Versions du .NET Framework :** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]  
  
## <a name="see-also"></a>Voir aussi

- [Diagnostic d’erreurs avec les Assistants Débogage managé](../../../../docs/framework/debug-trace-profile/diagnosing-errors-with-managed-debugging-assistants.md)
- [Interfaces de débogage](../../../../docs/framework/unmanaged-api/debugging/debugging-interfaces.md)
- [ICorDebugManagedCallback, interface](../../../../docs/framework/unmanaged-api/debugging/icordebugmanagedcallback-interface.md)
