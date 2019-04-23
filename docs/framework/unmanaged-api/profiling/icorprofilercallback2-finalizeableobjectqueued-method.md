---
title: ICorProfilerCallback2::FinalizeableObjectQueued, méthode
ms.date: 03/30/2017
api_name:
- ICorProfilerCallback2.FinalizeableObjectQueued
api_location:
- mscorwks.dll
api_type:
- COM
f1_keywords:
- ICorProfilerCallback2::FinalizeableObjectQueued
helpviewer_keywords:
- FinalizeableObjectQueued method [.NET Framework profiling]
- ICorProfilerCallback2::FinalizeableObjectQueued method [.NET Framework profiling]
ms.assetid: 92d76893-683c-475d-9996-5bff03cdb10f
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: b99a942d5c5fb205a84dd3766c99cc1126998de8
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59190394"
---
# <a name="icorprofilercallback2finalizeableobjectqueued-method"></a><span data-ttu-id="30147-102">ICorProfilerCallback2::FinalizeableObjectQueued, méthode</span><span class="sxs-lookup"><span data-stu-id="30147-102">ICorProfilerCallback2::FinalizeableObjectQueued Method</span></span>
<span data-ttu-id="30147-103">Notifie le profileur de code qu’un objet avec un finaliseur a été en file d’attente pour le thread finaliseur pour l’exécution de son `Finalize` (méthode).</span><span class="sxs-lookup"><span data-stu-id="30147-103">Notifies the code profiler that an object with a finalizer has been queued to the finalizer thread for execution of its `Finalize` method.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="30147-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="30147-104">Syntax</span></span>  
  
```  
HRESULT FinalizeableObjectQueued(  
    [in] DWORD finalizerFlags,  
    [in] ObjectID objectID);  
```  
  
## <a name="parameters"></a><span data-ttu-id="30147-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="30147-105">Parameters</span></span>  
 `finalizerFlags`  
 <span data-ttu-id="30147-106">[in] Une valeur de la [COR_PRF_FINALIZER_FLAGS](../../../../docs/framework/unmanaged-api/profiling/cor-prf-finalizer-flags-enumeration.md) énumération qui décrit les aspects du finaliseur.</span><span class="sxs-lookup"><span data-stu-id="30147-106">[in] A value of the [COR_PRF_FINALIZER_FLAGS](../../../../docs/framework/unmanaged-api/profiling/cor-prf-finalizer-flags-enumeration.md) enumeration that describes aspects of the finalizer.</span></span>  
  
 `objectID`  
 <span data-ttu-id="30147-107">[in] L’ID de l’objet qui a été en file d’attente.</span><span class="sxs-lookup"><span data-stu-id="30147-107">[in] The ID of the object that has been queued.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="30147-108">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="30147-108">Requirements</span></span>  
 <span data-ttu-id="30147-109">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="30147-109">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="30147-110">**En-tête :** CorProf.idl, CorProf.h</span><span class="sxs-lookup"><span data-stu-id="30147-110">**Header:** CorProf.idl, CorProf.h</span></span>  
  
 <span data-ttu-id="30147-111">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="30147-111">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="30147-112">**Versions du .NET Framework :** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="30147-112">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="30147-113">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="30147-113">See also</span></span>

- [<span data-ttu-id="30147-114">ICorProfilerCallback, interface</span><span class="sxs-lookup"><span data-stu-id="30147-114">ICorProfilerCallback Interface</span></span>](../../../../docs/framework/unmanaged-api/profiling/icorprofilercallback-interface.md)
- [<span data-ttu-id="30147-115">ICorProfilerCallback2, interface</span><span class="sxs-lookup"><span data-stu-id="30147-115">ICorProfilerCallback2 Interface</span></span>](../../../../docs/framework/unmanaged-api/profiling/icorprofilercallback2-interface.md)
