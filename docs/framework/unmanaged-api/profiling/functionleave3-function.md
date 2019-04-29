---
title: FunctionLeave3, fonction
ms.date: 03/30/2017
api_name:
- FunctionLeave3
api_location:
- mscorwks.dll
api_type:
- COM
f1_keywords:
- FunctionLeave3
helpviewer_keywords:
- FunctionLeave3 function [.NET Framework profiling]
ms.assetid: 5d798088-7992-48a0-ae55-d2a7ee31913f
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: b31c3045b021bd3b00d2b2e42bf7a118110305b1
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61598829"
---
# <a name="functionleave3-function"></a><span data-ttu-id="1f60d-102">FunctionLeave3, fonction</span><span class="sxs-lookup"><span data-stu-id="1f60d-102">FunctionLeave3 Function</span></span>
<span data-ttu-id="1f60d-103">Notifie le profileur que le contrôle a été renvoyé à partir d’une fonction.</span><span class="sxs-lookup"><span data-stu-id="1f60d-103">Notifies the profiler that control is being returned from a function.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="1f60d-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="1f60d-104">Syntax</span></span>  
  
```  
void __stdcall FunctionLeave3(FunctionOrRemappedID functionOrRemappedID);  
```  
  
## <a name="parameters"></a><span data-ttu-id="1f60d-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="1f60d-105">Parameters</span></span>  
 `functionOrRemappedID`  
 <span data-ttu-id="1f60d-106">[in] L’identificateur de la fonction à partir de laquelle le contrôle est retourné.</span><span class="sxs-lookup"><span data-stu-id="1f60d-106">[in] The identifier of the function from which control is returned.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="1f60d-107">Notes</span><span class="sxs-lookup"><span data-stu-id="1f60d-107">Remarks</span></span>  
 <span data-ttu-id="1f60d-108">Le `FunctionLeave3` fonction de rappel notifie le profileur que les fonctions sont appelées, mais ne prend pas en charge l’inspection de valeur de retour.</span><span class="sxs-lookup"><span data-stu-id="1f60d-108">The `FunctionLeave3` callback function notifies the profiler as functions are being called, but does not support return value inspection.</span></span> <span data-ttu-id="1f60d-109">Utilisez le [ICorProfilerInfo3::SetEnterLeaveFunctionHooks3, méthode](../../../../docs/framework/unmanaged-api/profiling/icorprofilerinfo3-setenterleavefunctionhooks3-method.md) pour enregistrer votre implémentation de cette fonction.</span><span class="sxs-lookup"><span data-stu-id="1f60d-109">Use the [ICorProfilerInfo3::SetEnterLeaveFunctionHooks3 method](../../../../docs/framework/unmanaged-api/profiling/icorprofilerinfo3-setenterleavefunctionhooks3-method.md) to register your implementation of this function.</span></span>  
  
 <span data-ttu-id="1f60d-110">Le `FunctionLeave3` fonction est un rappel ; vous devez l’implémenter.</span><span class="sxs-lookup"><span data-stu-id="1f60d-110">The `FunctionLeave3` function is a callback; you must implement it.</span></span> <span data-ttu-id="1f60d-111">L’implémentation doit utiliser le `__declspec(naked)` attribut de classe de stockage.</span><span class="sxs-lookup"><span data-stu-id="1f60d-111">The implementation must use the `__declspec(naked)` storage-class attribute.</span></span>  
  
 <span data-ttu-id="1f60d-112">Le moteur d’exécution n’enregistre pas les registres avant d’appeler cette fonction.</span><span class="sxs-lookup"><span data-stu-id="1f60d-112">The execution engine does not save any registers before calling this function.</span></span>  
  
- <span data-ttu-id="1f60d-113">À l’entrée, vous devez enregistrer tous les registres que vous utilisez, y compris celles dans l’unité de virgule flottante (FPU).</span><span class="sxs-lookup"><span data-stu-id="1f60d-113">On entry, you must save all registers that you use, including those in the floating-point unit (FPU).</span></span>  
  
- <span data-ttu-id="1f60d-114">À la sortie, vous devez restaurer la pile en dépilant tous les paramètres qui ont été envoyés par son appelant.</span><span class="sxs-lookup"><span data-stu-id="1f60d-114">On exit, you must restore the stack by popping off all the parameters that were pushed by its caller.</span></span>  
  
 <span data-ttu-id="1f60d-115">L’implémentation de `FunctionLeave3` ne doivent pas bloquer, car il sera retarder le garbage collection.</span><span class="sxs-lookup"><span data-stu-id="1f60d-115">The implementation of `FunctionLeave3` should not block, because it will delay garbage collection.</span></span> <span data-ttu-id="1f60d-116">L’implémentation ne doit pas tenter un garbage collection, car la pile est peut-être pas dans un état de la collection convivial garbage.</span><span class="sxs-lookup"><span data-stu-id="1f60d-116">The implementation should not attempt a garbage collection, because the stack may not be in a garbage collection-friendly state.</span></span> <span data-ttu-id="1f60d-117">Si un garbage collection est tenté, le runtime bloque jusqu'à ce que `FunctionLeave3` retourne.</span><span class="sxs-lookup"><span data-stu-id="1f60d-117">If a garbage collection is attempted, the runtime will block until `FunctionLeave3` returns.</span></span>  
  
 <span data-ttu-id="1f60d-118">Le `FunctionLeave3` (fonction) ne doit pas appeler dans du code managé ou provoquer une allocation de mémoire managée en aucune façon.</span><span class="sxs-lookup"><span data-stu-id="1f60d-118">The `FunctionLeave3` function must not call into managed code or cause a managed memory allocation in any way.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="1f60d-119">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="1f60d-119">Requirements</span></span>  
 <span data-ttu-id="1f60d-120">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="1f60d-120">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="1f60d-121">**En-tête :** CorProf.idl</span><span class="sxs-lookup"><span data-stu-id="1f60d-121">**Header:** CorProf.idl</span></span>  
  
 <span data-ttu-id="1f60d-122">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="1f60d-122">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="1f60d-123">**Versions du .NET Framework :** [!INCLUDE[net_current_v40plus](../../../../includes/net-current-v40plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="1f60d-123">**.NET Framework Versions:** [!INCLUDE[net_current_v40plus](../../../../includes/net-current-v40plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="1f60d-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1f60d-124">See also</span></span>

- [<span data-ttu-id="1f60d-125">FunctionEnter3</span><span class="sxs-lookup"><span data-stu-id="1f60d-125">FunctionEnter3</span></span>](../../../../docs/framework/unmanaged-api/profiling/functionenter3-function.md)
- [<span data-ttu-id="1f60d-126">FunctionTailcall3</span><span class="sxs-lookup"><span data-stu-id="1f60d-126">FunctionTailcall3</span></span>](../../../../docs/framework/unmanaged-api/profiling/functiontailcall3-function.md)
- [<span data-ttu-id="1f60d-127">FunctionEnter3WithInfo</span><span class="sxs-lookup"><span data-stu-id="1f60d-127">FunctionEnter3WithInfo</span></span>](../../../../docs/framework/unmanaged-api/profiling/functiontailcall3-function.md)
- [<span data-ttu-id="1f60d-128">FunctionLeave3WithInfo</span><span class="sxs-lookup"><span data-stu-id="1f60d-128">FunctionLeave3WithInfo</span></span>](../../../../docs/framework/unmanaged-api/profiling/functionleave3withinfo-function.md)
- [<span data-ttu-id="1f60d-129">FunctionTailcall3WithInfo</span><span class="sxs-lookup"><span data-stu-id="1f60d-129">FunctionTailcall3WithInfo</span></span>](../../../../docs/framework/unmanaged-api/profiling/functiontailcall3withinfo-function.md)
- [<span data-ttu-id="1f60d-130">SetEnterLeaveFunctionHooks3</span><span class="sxs-lookup"><span data-stu-id="1f60d-130">SetEnterLeaveFunctionHooks3</span></span>](../../../../docs/framework/unmanaged-api/profiling/icorprofilerinfo3-setenterleavefunctionhooks3-method.md)
- [<span data-ttu-id="1f60d-131">SetEnterLeaveFunctionHooks3WithInfo</span><span class="sxs-lookup"><span data-stu-id="1f60d-131">SetEnterLeaveFunctionHooks3WithInfo</span></span>](../../../../docs/framework/unmanaged-api/profiling/icorprofilerinfo3-setenterleavefunctionhooks3withinfo-method.md)
- [<span data-ttu-id="1f60d-132">SetFunctionIDMapper</span><span class="sxs-lookup"><span data-stu-id="1f60d-132">SetFunctionIDMapper</span></span>](../../../../docs/framework/unmanaged-api/profiling/icorprofilerinfo-setfunctionidmapper-method.md)
- [<span data-ttu-id="1f60d-133">SetFunctionIDMapper2</span><span class="sxs-lookup"><span data-stu-id="1f60d-133">SetFunctionIDMapper2</span></span>](../../../../docs/framework/unmanaged-api/profiling/icorprofilerinfo3-setfunctionidmapper2-method.md)
- [<span data-ttu-id="1f60d-134">Fonctions statiques globales de profilage</span><span class="sxs-lookup"><span data-stu-id="1f60d-134">Profiling Global Static Functions</span></span>](../../../../docs/framework/unmanaged-api/profiling/profiling-global-static-functions.md)
