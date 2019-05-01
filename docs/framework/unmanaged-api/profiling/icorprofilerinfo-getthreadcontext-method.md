---
title: ICorProfilerInfo::GetThreadContext, méthode
ms.date: 03/30/2017
api_name:
- ICorProfilerInfo.GetThreadContext
api_location:
- mscorwks.dll
api_type:
- COM
f1_keywords:
- ICorProfilerInfo::GetThreadContext
helpviewer_keywords:
- ICorProfilerInfo::GetThreadContext method [.NET Framework profiling]
- GetThreadContext method, ICorProfilerInfo interface [.NET Framework profiling]
ms.assetid: 79446216-4b8b-484c-8fe3-e87dbf9df2fd
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: f26fd93d42a709249936815d3c29ae572482f427
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61992041"
---
# <a name="icorprofilerinfogetthreadcontext-method"></a><span data-ttu-id="3e8eb-102">ICorProfilerInfo::GetThreadContext, méthode</span><span class="sxs-lookup"><span data-stu-id="3e8eb-102">ICorProfilerInfo::GetThreadContext Method</span></span>
<span data-ttu-id="3e8eb-103">Obtient l’identité de contexte actuellement associée au thread spécifié.</span><span class="sxs-lookup"><span data-stu-id="3e8eb-103">Gets the context identity currently associated with the specified thread.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="3e8eb-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="3e8eb-104">Syntax</span></span>  
  
```  
HRESULT GetThreadContext(  
    [in]  ThreadID  threadId,  
    [out] ContextID *pContextId);  
```  
  
## <a name="parameters"></a><span data-ttu-id="3e8eb-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="3e8eb-105">Parameters</span></span>  
 `threadId`  
 <span data-ttu-id="3e8eb-106">[in] L’ID du thread.</span><span class="sxs-lookup"><span data-stu-id="3e8eb-106">[in] The ID of the thread.</span></span>  
  
 `pContextId`  
 <span data-ttu-id="3e8eb-107">[out] Pointeur vers l’ID de contexte actuellement associé au thread spécifié.</span><span class="sxs-lookup"><span data-stu-id="3e8eb-107">[out] A pointer to the context ID currently associated with the specified thread.</span></span> <span data-ttu-id="3e8eb-108">Si le thread a aucun contexte actuellement associé, cette fonction retournera CORPROF_E_DATAINCOMPLETE.</span><span class="sxs-lookup"><span data-stu-id="3e8eb-108">If the thread has no context currently associated with it, this function will return CORPROF_E_DATAINCOMPLETE.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="3e8eb-109">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="3e8eb-109">Requirements</span></span>  
 <span data-ttu-id="3e8eb-110">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="3e8eb-110">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="3e8eb-111">**En-tête :** CorProf.idl, CorProf.h</span><span class="sxs-lookup"><span data-stu-id="3e8eb-111">**Header:** CorProf.idl, CorProf.h</span></span>  
  
 <span data-ttu-id="3e8eb-112">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="3e8eb-112">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="3e8eb-113">**Versions du .NET Framework :** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="3e8eb-113">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="3e8eb-114">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="3e8eb-114">See also</span></span>

- [<span data-ttu-id="3e8eb-115">ICorProfilerInfo, interface</span><span class="sxs-lookup"><span data-stu-id="3e8eb-115">ICorProfilerInfo Interface</span></span>](../../../../docs/framework/unmanaged-api/profiling/icorprofilerinfo-interface.md)
