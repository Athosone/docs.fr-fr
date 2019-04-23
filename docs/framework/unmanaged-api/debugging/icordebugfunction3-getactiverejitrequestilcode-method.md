---
title: ICorDebugFunction3::GetActiveReJitRequestILCode, méthode
ms.date: 03/30/2017
dev_langs:
- cpp
api_name:
- ICorDebugFunction3.GetActiveReJitRequestILCode
api_location:
- mscordbi.dll
api_type:
- COM
ms.assetid: 88584574-ade5-45b2-9778-489ed5c4dd7f
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 6268019f2e65c7c9209e00c0b6065e91103980c6
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59115880"
---
# <a name="icordebugfunction3getactiverejitrequestilcode-method"></a><span data-ttu-id="b7269-102">ICorDebugFunction3::GetActiveReJitRequestILCode, méthode</span><span class="sxs-lookup"><span data-stu-id="b7269-102">ICorDebugFunction3::GetActiveReJitRequestILCode Method</span></span>
<span data-ttu-id="b7269-103">[Pris en charge dans .NET Framework 4.5.2 et ultérieur]</span><span class="sxs-lookup"><span data-stu-id="b7269-103">[Supported in the .NET Framework 4.5.2 and later versions]</span></span>  
  
 <span data-ttu-id="b7269-104">Obtient un pointeur d’interface vers un [ICorDebugILCode](../../../../docs/framework/unmanaged-api/debugging/icordebugilcode-interface.md) qui contient le langage intermédiaire à partir d’une demande ReJIT active.</span><span class="sxs-lookup"><span data-stu-id="b7269-104">Gets an interface pointer to an [ICorDebugILCode](../../../../docs/framework/unmanaged-api/debugging/icordebugilcode-interface.md) that contains the IL from an active ReJIT request.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="b7269-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="b7269-105">Syntax</span></span>  
  
```cpp
HRESULT GetActiveReJitRequestILCode(  
   ICorDebugILCode **ppReJitedILCode  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="b7269-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="b7269-106">Parameters</span></span>  
 `ppReJitedILCode`  
 <span data-ttu-id="b7269-107">Un pointeur depuis une demande ReJIT active vers le langage intermédiaire.</span><span class="sxs-lookup"><span data-stu-id="b7269-107">A pointer to the IL from an active ReJIT request.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="b7269-108">Notes</span><span class="sxs-lookup"><span data-stu-id="b7269-108">Remarks</span></span>  
 <span data-ttu-id="b7269-109">Si la méthode représentée par cet objet `ICorDebugFunction3` a une demande ReJIT active, `ppReJitedILCode` retourne un pointeur vers son langage intermédiaire.</span><span class="sxs-lookup"><span data-stu-id="b7269-109">If the method represented by this `ICorDebugFunction3` object has an active ReJIT request, `ppReJitedILCode` returns a pointer to its IL.</span></span> <span data-ttu-id="b7269-110">S’il n’existe aucune requête active, qui est un cas courant, puis `ppReJitedILCode` est **null**.</span><span class="sxs-lookup"><span data-stu-id="b7269-110">If there is no active request, which is a common case, then `ppReJitedILCode` is **null**.</span></span>  
  
 <span data-ttu-id="b7269-111">Une demande ReJIT devient active juste après l’exécution retourne à partir de la [ICorProfilerCallback4::GetReJITParameters](../../../../docs/framework/unmanaged-api/profiling/icorprofilercallback4-getrejitparameters-method.md) appel de méthode.</span><span class="sxs-lookup"><span data-stu-id="b7269-111">A ReJIT request becomes active just after execution returns from the [ICorProfilerCallback4::GetReJITParameters](../../../../docs/framework/unmanaged-api/profiling/icorprofilercallback4-getrejitparameters-method.md) method call.</span></span> <span data-ttu-id="b7269-112">Il est possible qu'elle ne soit pas encore compilée en mode juste-à-temps et que des threads soient toujours en cours d'exécution dans la version d'origine du code.</span><span class="sxs-lookup"><span data-stu-id="b7269-112">It may not yet be JIT-compiled, and threads may still be executing in the original version of the code.</span></span> <span data-ttu-id="b7269-113">Une demande ReJIT devient inactive pendant l’appel du profileur à le [ICorProfilerInfo4::RequestRevert](../../../../docs/framework/unmanaged-api/profiling/icorprofilerinfo4-requestrevert-method.md) (méthode).</span><span class="sxs-lookup"><span data-stu-id="b7269-113">A ReJIT request becomes inactive during the profiler's call to the [ICorProfilerInfo4::RequestRevert](../../../../docs/framework/unmanaged-api/profiling/icorprofilerinfo4-requestrevert-method.md) method.</span></span> <span data-ttu-id="b7269-114">Même après le rétablissement du langage intermédiaire, un thread peut toujours être en train d'exécuter le code ReJIT (recompilé en mode juste-à-temps).</span><span class="sxs-lookup"><span data-stu-id="b7269-114">Even after the IL is reverted, a thread can still be executing in the JIT-recompiled (ReJIT) code.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="b7269-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="b7269-115">Requirements</span></span>  
 <span data-ttu-id="b7269-116">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="b7269-116">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="b7269-117">**En-tête :** CorDebug.idl, CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="b7269-117">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="b7269-118">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="b7269-118">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="b7269-119">**Versions du .NET Framework :** [!INCLUDE[net_current_v452plus](../../../../includes/net-current-v452plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="b7269-119">**.NET Framework Versions:** [!INCLUDE[net_current_v452plus](../../../../includes/net-current-v452plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="b7269-120">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b7269-120">See also</span></span>

- [<span data-ttu-id="b7269-121">ICorDebugFunction3, interface</span><span class="sxs-lookup"><span data-stu-id="b7269-121">ICorDebugFunction3 Interface</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugfunction3-interface.md)
- [<span data-ttu-id="b7269-122">Interfaces de débogage</span><span class="sxs-lookup"><span data-stu-id="b7269-122">Debugging Interfaces</span></span>](../../../../docs/framework/unmanaged-api/debugging/debugging-interfaces.md)
- [<span data-ttu-id="b7269-123">ReJIT : Guide pratique</span><span class="sxs-lookup"><span data-stu-id="b7269-123">ReJIT: A How-To Guide</span></span>](https://blogs.msdn.com/b/davbr/archive/2011/10/12/rejit-a-how-to-guide.aspx)
