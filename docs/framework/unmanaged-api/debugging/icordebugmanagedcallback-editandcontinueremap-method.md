---
title: ICorDebugManagedCallback::EditAndContinueRemap, méthode
ms.date: 03/30/2017
api_name:
- ICorDebugManagedCallback.EditAndContinueRemap
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugManagedCallback::EditAndContinueRemap
helpviewer_keywords:
- EditAndContinueRemap method [.NET Framework debugging]
- ICorDebugManagedCallback::EditAndContinueRemap method [.NET Framework debugging]
ms.assetid: 24a8fcce-317e-48ff-aefc-d86123ada935
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: d1bdb14e8c3a61a2b94cef778660eeb5c85c34df
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61988238"
---
# <a name="icordebugmanagedcallbackeditandcontinueremap-method"></a><span data-ttu-id="47529-102">ICorDebugManagedCallback::EditAndContinueRemap, méthode</span><span class="sxs-lookup"><span data-stu-id="47529-102">ICorDebugManagedCallback::EditAndContinueRemap Method</span></span>
<span data-ttu-id="47529-103">Cette méthode est dépréciée.</span><span class="sxs-lookup"><span data-stu-id="47529-103">This method has been deprecated.</span></span> <span data-ttu-id="47529-104">Informe le débogueur qu’un événement de remappage a été envoyé à l’environnement de développement intégré (IDE).</span><span class="sxs-lookup"><span data-stu-id="47529-104">It notifies the debugger that a remap event has been sent to the integrated development environment (IDE).</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="47529-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="47529-105">Syntax</span></span>  
  
```  
HRESULT EditAndContinueRemap (  
    [in] ICorDebugAppDomain *pAppDomain,  
    [in] ICorDebugThread *pThread,  
    [in] ICorDebugFunction *pFunction,  
    [in] BOOL fAccurate  
);  
```  
  
## <a name="remarks"></a><span data-ttu-id="47529-106">Notes</span><span class="sxs-lookup"><span data-stu-id="47529-106">Remarks</span></span>  
 <span data-ttu-id="47529-107">Le `EditAndContinueRemap` méthode est appelée lorsque l’exécution du code dans une ancienne version d’une fonction de mise à jour a été tentée.</span><span class="sxs-lookup"><span data-stu-id="47529-107">The `EditAndContinueRemap` method is called when the execution of the code in an old version of an updated function has been attempted.</span></span> <span data-ttu-id="47529-108">Le common language runtime appelle le `EditAndContinueRemap` méthode pour envoyer un événement de remappage à l’IDE.</span><span class="sxs-lookup"><span data-stu-id="47529-108">The common language runtime calls the `EditAndContinueRemap` method to send a remap event to the IDE.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="47529-109">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="47529-109">Requirements</span></span>  
 <span data-ttu-id="47529-110">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="47529-110">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="47529-111">**En-tête :** CorDebug.idl, CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="47529-111">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="47529-112">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="47529-112">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="47529-113">**Versions du .NET Framework :** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="47529-113">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="47529-114">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="47529-114">See also</span></span>

- [<span data-ttu-id="47529-115">ICorDebugManagedCallback, interface</span><span class="sxs-lookup"><span data-stu-id="47529-115">ICorDebugManagedCallback Interface</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugmanagedcallback-interface.md)
