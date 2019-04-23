---
title: ICorProfilerCallback::AssemblyLoadStarted, méthode
ms.date: 03/30/2017
api_name:
- ICorProfilerCallback.AssemblyLoadStarted
api_location:
- mscorwks.dll
api_type:
- COM
f1_keywords:
- ICorProfilerCallback::AssemblyLoadStarted
helpviewer_keywords:
- ICorProfilerCallback::AssemblyLoadStarted method [.NET Framework profiling]
- AssemblyLoadStarted method [.NET Framework profiling]
ms.assetid: 67e8209d-a0ca-4118-a6e6-c1ee0abc2221
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: a96a2a0d6e4bc48a46850aeaadd17c2669419cef
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59219354"
---
# <a name="icorprofilercallbackassemblyloadstarted-method"></a><span data-ttu-id="856fe-102">ICorProfilerCallback::AssemblyLoadStarted, méthode</span><span class="sxs-lookup"><span data-stu-id="856fe-102">ICorProfilerCallback::AssemblyLoadStarted Method</span></span>
<span data-ttu-id="856fe-103">Notifie le profileur qu’un assembly est chargé.</span><span class="sxs-lookup"><span data-stu-id="856fe-103">Notifies the profiler that an assembly is being loaded.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="856fe-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="856fe-104">Syntax</span></span>  
  
```  
HRESULT AssemblyLoadStarted(  
    [in] AssemblyID assemblyId);  
```  
  
## <a name="parameters"></a><span data-ttu-id="856fe-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="856fe-105">Parameters</span></span>  
 `assemblyId`  
 <span data-ttu-id="856fe-106">[in] Identifie l’assembly qui est en cours de chargement.</span><span class="sxs-lookup"><span data-stu-id="856fe-106">[in] Identifies the assembly that is being loaded.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="856fe-107">Notes</span><span class="sxs-lookup"><span data-stu-id="856fe-107">Remarks</span></span>  
 <span data-ttu-id="856fe-108">La valeur de `assemblyId` n’est pas valide pour une demande d’informations jusqu'à ce que le [ICorProfilerCallback::AssemblyLoadFinished](../../../../docs/framework/unmanaged-api/profiling/icorprofilercallback-assemblyloadfinished-method.md) méthode est appelée.</span><span class="sxs-lookup"><span data-stu-id="856fe-108">The value of `assemblyId` is not valid for an information request until the [ICorProfilerCallback::AssemblyLoadFinished](../../../../docs/framework/unmanaged-api/profiling/icorprofilercallback-assemblyloadfinished-method.md) method is called.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="856fe-109">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="856fe-109">Requirements</span></span>  
 <span data-ttu-id="856fe-110">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="856fe-110">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="856fe-111">**En-tête :** CorProf.idl, CorProf.h</span><span class="sxs-lookup"><span data-stu-id="856fe-111">**Header:** CorProf.idl, CorProf.h</span></span>  
  
 <span data-ttu-id="856fe-112">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="856fe-112">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="856fe-113">**Versions du .NET Framework :** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="856fe-113">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="856fe-114">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="856fe-114">See also</span></span>

- [<span data-ttu-id="856fe-115">ICorProfilerCallback, interface</span><span class="sxs-lookup"><span data-stu-id="856fe-115">ICorProfilerCallback Interface</span></span>](../../../../docs/framework/unmanaged-api/profiling/icorprofilercallback-interface.md)
