---
title: ICorProfilerCallback::AssemblyUnloadFinished, méthode
ms.date: 03/30/2017
api_name:
- ICorProfilerCallback.AssemblyUnloadFinished
api_location:
- mscorwks.dll
api_type:
- COM
f1_keywords:
- ICorProfilerCallback::AssemblyUnloadFinished
helpviewer_keywords:
- AssemblyUnloadFinished method [.NET Framework profiling]
- ICorProfilerCallback::AssemblyUnloadFinished method [.NET Framework profiling]
ms.assetid: 53fca564-84b1-44d4-9e21-17a492d2aae7
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: b9ee87c926d2377ff8eef53f930fe75251b28ceb
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61597870"
---
# <a name="icorprofilercallbackassemblyunloadfinished-method"></a><span data-ttu-id="76ff5-102">ICorProfilerCallback::AssemblyUnloadFinished, méthode</span><span class="sxs-lookup"><span data-stu-id="76ff5-102">ICorProfilerCallback::AssemblyUnloadFinished Method</span></span>
<span data-ttu-id="76ff5-103">Informe le profileur qu’un assembly a été déchargé.</span><span class="sxs-lookup"><span data-stu-id="76ff5-103">Notifies the profiler that an assembly has been unloaded.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="76ff5-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="76ff5-104">Syntax</span></span>  
  
```  
HRESULT AssemblyUnloadFinished(  
    [in] AssemblyID assemblyId,  
    [in] HRESULT    hrStatus);  
```  
  
## <a name="parameters"></a><span data-ttu-id="76ff5-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="76ff5-105">Parameters</span></span>  
 `assemblyId`  
 <span data-ttu-id="76ff5-106">[in] Identifie l’assembly qui est en cours de déchargement.</span><span class="sxs-lookup"><span data-stu-id="76ff5-106">[in] Identifies the assembly that is being unloaded.</span></span>  
  
 `hrStatus`  
 <span data-ttu-id="76ff5-107">[in] HRESULT qui indique si l’assembly a été déchargé.</span><span class="sxs-lookup"><span data-stu-id="76ff5-107">[in] An HRESULT that indicates whether the assembly was unloaded successfully.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="76ff5-108">Notes</span><span class="sxs-lookup"><span data-stu-id="76ff5-108">Remarks</span></span>  
 <span data-ttu-id="76ff5-109">La valeur de `assemblyId` n’est pas valide pour une demande d’informations après la [ICorProfilerCallback::AssemblyUnloadStarted](../../../../docs/framework/unmanaged-api/profiling/icorprofilercallback-assemblyunloadstarted-method.md) méthode retourne.</span><span class="sxs-lookup"><span data-stu-id="76ff5-109">The value of `assemblyId` is not valid for an information request after the [ICorProfilerCallback::AssemblyUnloadStarted](../../../../docs/framework/unmanaged-api/profiling/icorprofilercallback-assemblyunloadstarted-method.md) method returns.</span></span>  
  
 <span data-ttu-id="76ff5-110">Certaines parties du déchargement de l’assembly peuvent continuer après le `AssemblyUnloadFinished` rappel.</span><span class="sxs-lookup"><span data-stu-id="76ff5-110">Some parts of unloading the assembly might continue after the `AssemblyUnloadFinished` callback.</span></span> <span data-ttu-id="76ff5-111">Un HRESULT d’échec dans `hrStatus` indique un échec.</span><span class="sxs-lookup"><span data-stu-id="76ff5-111">A failure HRESULT in `hrStatus` indicates a failure.</span></span> <span data-ttu-id="76ff5-112">Toutefois, un HRESULT de réussite dans `hrStatus` indique uniquement que la première partie du déchargement de l’assembly a réussi.</span><span class="sxs-lookup"><span data-stu-id="76ff5-112">However, a success HRESULT in `hrStatus` indicates only that the first part of unloading the assembly has succeeded.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="76ff5-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="76ff5-113">Requirements</span></span>  
 <span data-ttu-id="76ff5-114">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="76ff5-114">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="76ff5-115">**En-tête :** CorProf.idl, CorProf.h</span><span class="sxs-lookup"><span data-stu-id="76ff5-115">**Header:** CorProf.idl, CorProf.h</span></span>  
  
 <span data-ttu-id="76ff5-116">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="76ff5-116">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="76ff5-117">**Versions du .NET Framework :** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="76ff5-117">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="76ff5-118">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="76ff5-118">See also</span></span>

- [<span data-ttu-id="76ff5-119">ICorProfilerCallback, interface</span><span class="sxs-lookup"><span data-stu-id="76ff5-119">ICorProfilerCallback Interface</span></span>](../../../../docs/framework/unmanaged-api/profiling/icorprofilercallback-interface.md)
