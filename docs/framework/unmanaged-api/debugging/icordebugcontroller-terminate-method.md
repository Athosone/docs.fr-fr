---
title: ICorDebugController::Terminate, méthode
ms.date: 03/30/2017
api_name:
- ICorDebugController.Terminate
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugController::Terminate
helpviewer_keywords:
- Terminate method, ICorDebugController interface [.NET Framework debugging]
- ICorDebugController::Terminate method [.NET Framework debugging]
ms.assetid: 4275af0c-b5a7-4e4c-97c9-7e41f36b2dd8
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: c4c8dd8795fc3699176490ea0bb9b2e999038afb
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61749062"
---
# <a name="icordebugcontrollerterminate-method"></a>ICorDebugController::Terminate, méthode
Met fin au processus avec le code de sortie spécifié.  
  
> [!NOTE]
>  Cette méthode est un wrapper pour Win32 `TerminateProcess` (fonction). Par conséquent, `Terminate` utilise le code de sortie de la même façon que Win32 `TerminateProcess` utilise la fonction.  
  
## <a name="syntax"></a>Syntaxe  
  
```  
HRESULT Terminate (  
    [in] UINT exitCode  
);  
```  
  
## <a name="parameters"></a>Paramètres  
 `exitCode`  
 [in] Valeur numérique qui est le code de sortie. Les valeurs numériques valides sont définis dans Winbase.h.  
  
## <a name="remarks"></a>Notes  
 Si le processus est arrêté lorsque `Terminate` est appelée, le processus doit être poursuivi à l’aide de la [ICorDebugController::Continue](../../../../docs/framework/unmanaged-api/debugging/icordebugcontroller-continue-method.md) méthode afin que le débogueur reçoive confirmation de l’arrêt via le [ ICorDebugManagedCallback::ExitProcess](../../../../docs/framework/unmanaged-api/debugging/icordebugmanagedcallback-exitprocess-method.md) ou [ICorDebugManagedCallback::ExitAppDomain](../../../../docs/framework/unmanaged-api/debugging/icordebugmanagedcallback-exitappdomain-method.md) rappel.  
  
> [!NOTE]
>  Cette méthode n’est pas implémentée par un domaine d’application. Autrement dit, il n’est pas implémentée à le <xref:System.AppDomain> niveau.  
  
## <a name="requirements"></a>Configuration requise  
 **Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).  
  
 **En-tête :** CorDebug.idl, CorDebug.h  
  
 **Bibliothèque :** CorGuids.lib  
  
 **Versions du .NET Framework :** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]  
  
## <a name="see-also"></a>Voir aussi
