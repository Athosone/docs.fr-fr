---
title: ICorProfilerCallback4::GetReJITParameters, méthode
ms.date: 03/30/2017
api_name:
- ICorProfilerCallback4.GetReJITParameters
api_location:
- mscorwks.dll
api_type:
- COM
f1_keywords:
- ICorProfilerCallback4::GetReJITParameters
helpviewer_keywords:
- ICorProfilerCallback4::GetReJITParameters method [.NET Framework profiling]
- GetReJITParameters method, ICorProfilerCallback4 interface [.NET Framework profiling]
ms.assetid: 0e9bfe07-9f20-498c-b568-9017c8f6056c
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: ca176be93b92e44228d9b4063e87a62263e83e04
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61782504"
---
# <a name="icorprofilercallback4getrejitparameters-method"></a><span data-ttu-id="72c69-102">ICorProfilerCallback4::GetReJITParameters, méthode</span><span class="sxs-lookup"><span data-stu-id="72c69-102">ICorProfilerCallback4::GetReJITParameters Method</span></span>
<span data-ttu-id="72c69-103">Permet au profileur de code définir les indicateurs de génération de code de remplacement pour un nouveau corps de méthode recompilée.</span><span class="sxs-lookup"><span data-stu-id="72c69-103">Allows the code profiler to set alternate code generation flags for a new recompiled method body.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="72c69-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="72c69-104">Syntax</span></span>  
  
```  
HRESULT GetReJITParameters(     [in] ModuleID moduleId,     [in] mdMethodDef methodId,     [in] ICorProfilerFunctionControl *pFunctionControl);  
```  
  
## <a name="parameters"></a><span data-ttu-id="72c69-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="72c69-105">Parameters</span></span>  
 `moduleID`  
 <span data-ttu-id="72c69-106">[in] Le module qui contient la méthode pour laquelle le CLR doit les paramètres de recompilation JIT.</span><span class="sxs-lookup"><span data-stu-id="72c69-106">[in] The module that contains the method for which the CLR needs JIT recompilation parameters.</span></span>  
  
 `methodId`  
 <span data-ttu-id="72c69-107">[in] Le `MethodDef` de la méthode pour laquelle le CLR doit les paramètres de recompilation JIT.</span><span class="sxs-lookup"><span data-stu-id="72c69-107">[in] The `MethodDef` of the method for which the CLR needs JIT recompilation parameters.</span></span>  
  
 `pFunctionControl`  
 <span data-ttu-id="72c69-108">[in] Un pointeur vers un [ICorProfilerFunctionControl](../../../../docs/framework/unmanaged-api/profiling/icorprofilerfunctioncontrol-interface.md) interface que le profileur peut utiliser pour fournir des informations de recompilation JIT pour la méthode en cours de recompilation.</span><span class="sxs-lookup"><span data-stu-id="72c69-108">[in] A pointer to an [ICorProfilerFunctionControl](../../../../docs/framework/unmanaged-api/profiling/icorprofilerfunctioncontrol-interface.md) interface that the profiler can use to provide JIT recompilation information for the method being recompiled.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="72c69-109">Notes</span><span class="sxs-lookup"><span data-stu-id="72c69-109">Remarks</span></span>  
 <span data-ttu-id="72c69-110">Les problèmes CLR un `GetReJITParameters` rappel afin que le profileur peut spécifier les paramètres pour la recompilation d’une méthode donnée.</span><span class="sxs-lookup"><span data-stu-id="72c69-110">The CLR issues a `GetReJITParameters` callback so that the profiler can specify the parameters for recompiling a given method.</span></span> <span data-ttu-id="72c69-111">Le `GetReJITParameters` rappel est émis une seule fois par la fonction ; les paramètres fournis par le profileur s’appliquent à toutes les instances de cette fonction.</span><span class="sxs-lookup"><span data-stu-id="72c69-111">The `GetReJITParameters` callback is issued only once per function; the parameters supplied by the profiler apply to all instances of that function.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="72c69-112">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="72c69-112">Requirements</span></span>  
 <span data-ttu-id="72c69-113">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="72c69-113">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="72c69-114">**En-tête :** CorProf.idl, CorProf.h</span><span class="sxs-lookup"><span data-stu-id="72c69-114">**Header:** CorProf.idl, CorProf.h</span></span>  
  
 <span data-ttu-id="72c69-115">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="72c69-115">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="72c69-116">**Versions du .NET Framework :** [!INCLUDE[net_current_v45plus](../../../../includes/net-current-v45plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="72c69-116">**.NET Framework Versions:** [!INCLUDE[net_current_v45plus](../../../../includes/net-current-v45plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="72c69-117">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="72c69-117">See also</span></span>

- [<span data-ttu-id="72c69-118">ICorProfilerCallback, interface</span><span class="sxs-lookup"><span data-stu-id="72c69-118">ICorProfilerCallback Interface</span></span>](../../../../docs/framework/unmanaged-api/profiling/icorprofilercallback-interface.md)
- [<span data-ttu-id="72c69-119">ICorProfilerCallback4, interface</span><span class="sxs-lookup"><span data-stu-id="72c69-119">ICorProfilerCallback4 Interface</span></span>](../../../../docs/framework/unmanaged-api/profiling/icorprofilercallback4-interface.md)
- [<span data-ttu-id="72c69-120">JITCompilationStarted, méthode</span><span class="sxs-lookup"><span data-stu-id="72c69-120">JITCompilationStarted Method</span></span>](../../../../docs/framework/unmanaged-api/profiling/icorprofilercallback-jitcompilationstarted-method.md)
- [<span data-ttu-id="72c69-121">ReJITCompilationStarted, méthode</span><span class="sxs-lookup"><span data-stu-id="72c69-121">ReJITCompilationStarted Method</span></span>](../../../../docs/framework/unmanaged-api/profiling/icorprofilercallback4-rejitcompilationstarted-method.md)
