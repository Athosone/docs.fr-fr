---
title: ICorDebugStepper::Step, méthode
ms.date: 03/30/2017
api_name:
- ICorDebugStepper.Step
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugStepper::Step
helpviewer_keywords:
- Step method, ICorDebugStepper interface [.NET Framework debugging]
- ICorDebugStepper::Step method [.NET Framework debugging]
ms.assetid: 38c1940b-ada1-40ba-8295-4c0833744e1e
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 444390622ca68244661b91dc85814b05556b12a2
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61994316"
---
# <a name="icordebugstepperstep-method"></a><span data-ttu-id="6ccac-102">ICorDebugStepper::Step, méthode</span><span class="sxs-lookup"><span data-stu-id="6ccac-102">ICorDebugStepper::Step Method</span></span>
<span data-ttu-id="6ccac-103">Provoque ICorDebugStepper à pas son thread conteneur et éventuellement, continuez le pas à pas via des fonctions appelées dans le thread.</span><span class="sxs-lookup"><span data-stu-id="6ccac-103">Causes this ICorDebugStepper to single-step through its containing thread, and optionally, to continue single-stepping through functions that are called within the thread.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="6ccac-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="6ccac-104">Syntax</span></span>  
  
```  
HRESULT Step (  
    [in] BOOL   bStepIn  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="6ccac-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="6ccac-105">Parameters</span></span>  
 `bStepIn`  
 <span data-ttu-id="6ccac-106">[in] La valeur `true` à l’étape dans une fonction qui est appelée dans le thread.</span><span class="sxs-lookup"><span data-stu-id="6ccac-106">[in] Set to `true` to step into a function that is called within the thread.</span></span> <span data-ttu-id="6ccac-107">La valeur `false` pour ignorer la fonction.</span><span class="sxs-lookup"><span data-stu-id="6ccac-107">Set to `false` to step over the function.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="6ccac-108">Notes</span><span class="sxs-lookup"><span data-stu-id="6ccac-108">Remarks</span></span>  
 <span data-ttu-id="6ccac-109">L’étape se termine lorsque le common language runtime exécute l’instruction managée suivante dans le frame de cette exécution pas à pas.</span><span class="sxs-lookup"><span data-stu-id="6ccac-109">The step completes when the common language runtime performs the next managed instruction in this stepper's frame.</span></span> <span data-ttu-id="6ccac-110">Si `Step` est appelée sur une exécution pas à pas, ce qui n’est pas dans le code managé, l’étape se termine lorsque l’instruction de code managé suivante est exécutée par le thread.</span><span class="sxs-lookup"><span data-stu-id="6ccac-110">If `Step` is called on a stepper, which is not in managed code, the step will complete when the next managed code instruction is executed by the thread.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="6ccac-111">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="6ccac-111">Requirements</span></span>  
 <span data-ttu-id="6ccac-112">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="6ccac-112">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="6ccac-113">**En-tête :** CorDebug.idl, CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="6ccac-113">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="6ccac-114">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="6ccac-114">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="6ccac-115">**Versions du .NET Framework :** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="6ccac-115">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>
