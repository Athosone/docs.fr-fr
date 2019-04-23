---
title: ICorDebugManagedCallback::StepComplete, méthode
ms.date: 03/30/2017
api_name:
- ICorDebugManagedCallback.StepComplete
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugManagedCallback::StepComplete
helpviewer_keywords:
- StepComplete method [.NET Framework debugging]
- ICorDebugManagedCallback::StepComplete method [.NET Framework debugging]
ms.assetid: 5e1f2c47-81df-4530-826d-96489cd68719
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: fd784cb3322423e9309e8a5632822831b4e44cdf
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59184793"
---
# <a name="icordebugmanagedcallbackstepcomplete-method"></a><span data-ttu-id="a7a59-102">ICorDebugManagedCallback::StepComplete, méthode</span><span class="sxs-lookup"><span data-stu-id="a7a59-102">ICorDebugManagedCallback::StepComplete Method</span></span>
<span data-ttu-id="a7a59-103">Notifie le débogueur qu’une étape terminée.</span><span class="sxs-lookup"><span data-stu-id="a7a59-103">Notifies the debugger that a step has completed.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="a7a59-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="a7a59-104">Syntax</span></span>  
  
```  
HRESULT StepComplete (  
    [in] ICorDebugAppDomain  *pAppDomain,  
    [in] ICorDebugThread     *pThread,  
    [in] ICorDebugStepper    *pStepper,  
    [in] CorDebugStepReason   reason  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="a7a59-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="a7a59-105">Parameters</span></span>  
 `pAppDomain`  
 <span data-ttu-id="a7a59-106">[in] Pointeur vers un objet ICorDebugAppDomain qui représente le domaine d’application contenant le thread dans lequel l’étape est terminée.</span><span class="sxs-lookup"><span data-stu-id="a7a59-106">[in] A pointer to an ICorDebugAppDomain object that represents the application domain containing the thread in which the step has completed.</span></span>  
  
 `pThread`  
 <span data-ttu-id="a7a59-107">[in] Pointeur vers un objet ICorDebugThread qui représente le thread dans lequel l’étape est terminée.</span><span class="sxs-lookup"><span data-stu-id="a7a59-107">[in] A pointer to an ICorDebugThread object that represents the thread in which the step has completed.</span></span>  
  
 `pStepper`  
 <span data-ttu-id="a7a59-108">[in] Pointeur vers un objet ICorDebugStepper qui représente l’étape dans l’exécution de code.</span><span class="sxs-lookup"><span data-stu-id="a7a59-108">[in] A pointer to an ICorDebugStepper object that represents the step in code execution.</span></span>  
  
 `reason`  
 <span data-ttu-id="a7a59-109">[in] Une valeur de l’énumération CorDebugStepReason qui indique le résultat d’une étape individuelle.</span><span class="sxs-lookup"><span data-stu-id="a7a59-109">[in] A value of the CorDebugStepReason enumeration that indicates the outcome of an individual step.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="a7a59-110">Notes</span><span class="sxs-lookup"><span data-stu-id="a7a59-110">Remarks</span></span>  
 <span data-ttu-id="a7a59-111">L’exécution pas à pas permet de continuer pas à pas détaillé si vous le souhaitez, à moins que le débogage est arrêté.</span><span class="sxs-lookup"><span data-stu-id="a7a59-111">The stepper may be used to continue stepping if desired, unless the debugging is terminated.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="a7a59-112">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="a7a59-112">Requirements</span></span>  
 <span data-ttu-id="a7a59-113">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="a7a59-113">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="a7a59-114">**En-tête :** CorDebug.idl, CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="a7a59-114">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="a7a59-115">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="a7a59-115">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="a7a59-116">**Versions du .NET Framework :** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="a7a59-116">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="a7a59-117">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a7a59-117">See also</span></span>

- [<span data-ttu-id="a7a59-118">ICorDebugManagedCallback, interface</span><span class="sxs-lookup"><span data-stu-id="a7a59-118">ICorDebugManagedCallback Interface</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugmanagedcallback-interface.md)
