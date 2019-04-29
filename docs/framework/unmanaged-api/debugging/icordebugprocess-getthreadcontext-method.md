---
title: ICorDebugProcess::GetThreadContext, méthode
ms.date: 03/30/2017
api_name:
- ICorDebugProcess.GetThreadContext
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugProcess::GetThreadContext
helpviewer_keywords:
- ICorDebugProcess::GetThreadContext method [.NET Framework debugging]
- GetThreadContext method, ICorDebugProcess interface [.NET Framework debugging]
ms.assetid: 5b132ef1-8d4b-4525-89b3-54123596c194
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 28d54becc2d7cd4359c78415f25f579b968cb3f4
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61775598"
---
# <a name="icordebugprocessgetthreadcontext-method"></a>ICorDebugProcess::GetThreadContext, méthode
Obtient le contexte pour le thread donné dans ce processus.  
  
## <a name="syntax"></a>Syntaxe  
  
```  
HRESULT GetThreadContext(  
    [in] DWORD threadID,  
    [in] ULONG32 contextSize,  
    [in, out, length_is(contextSize), size_is(contextSize)]  
    BYTE context[]);  
```  
  
## <a name="parameters"></a>Paramètres  
 `threadID`  
 [in] L’ID du thread pour lequel récupérer le contexte.  
  
 `contextSize`  
 [in] Taille du tableau `context`.  
  
 `context`  
 [in, out] Un tableau d’octets qui décrivent le contexte du thread.  
  
 Le contexte spécifie l’architecture du processeur sur lequel le thread s’exécute.  
  
## <a name="remarks"></a>Notes  
 Le débogueur doit appeler cette méthode plutôt que Win32 `GetThreadContext` (méthode), car le thread peut être dans un état « infiltré », son contexte dans lequel a été temporairement modifié. Cette méthode doit être utilisée uniquement lorsqu’un thread est en code natif. Utilisez [ICorDebugRegisterSet](../../../../docs/framework/unmanaged-api/debugging/icordebugregisterset-interface.md) pour les threads en code managé.  
  
 Les données retournées sont une structure de contexte pour la plateforme actuelle. Comme avec Win32 `GetThreadContext` (méthode), l’appelant doit initialiser le `context` paramètre avant d’appeler cette méthode.  
  
## <a name="requirements"></a>Configuration requise  
 **Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).  
  
 **En-tête :** CorDebug.idl, CorDebug.h  
  
 **Bibliothèque :** CorGuids.lib  
  
 **Versions du .NET Framework :** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]
