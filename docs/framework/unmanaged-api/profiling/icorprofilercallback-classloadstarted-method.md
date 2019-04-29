---
title: ICorProfilerCallback::ClassLoadStarted, méthode
ms.date: 03/30/2017
api_name:
- ICorProfilerCallback.ClassLoadStarted
api_location:
- mscorwks.dll
api_type:
- COM
f1_keywords:
- ICorProfilerCallback::ClassLoadStarted
helpviewer_keywords:
- ICorProfilerCallback::ClassLoadStarted method [.NET Framework profiling]
- ClassLoadStarted method [.NET Framework profiling]
ms.assetid: 9f728de8-45c2-45a5-ac4a-45660bd36ecf
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: db7a033944272756a739dec39d4df11fde1d48b3
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61598014"
---
# <a name="icorprofilercallbackclassloadstarted-method"></a><span data-ttu-id="a907f-102">ICorProfilerCallback::ClassLoadStarted, méthode</span><span class="sxs-lookup"><span data-stu-id="a907f-102">ICorProfilerCallback::ClassLoadStarted Method</span></span>
<span data-ttu-id="a907f-103">Informe le profileur qu’une classe est chargée.</span><span class="sxs-lookup"><span data-stu-id="a907f-103">Notifies the profiler that a class is being loaded.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="a907f-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="a907f-104">Syntax</span></span>  
  
```  
HRESULT ClassLoadStarted(  
    [in] ClassID classId);  
```  
  
## <a name="parameters"></a><span data-ttu-id="a907f-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="a907f-105">Parameters</span></span>  
 `classId`  
 <span data-ttu-id="a907f-106">[in] Identifie la classe qui est en cours de chargement.</span><span class="sxs-lookup"><span data-stu-id="a907f-106">[in] Identifies the class that is being loaded.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="a907f-107">Notes</span><span class="sxs-lookup"><span data-stu-id="a907f-107">Remarks</span></span>  
 <span data-ttu-id="a907f-108">La valeur de `classId` n’est pas valide pour une demande d’informations jusqu'à ce que le [ICorProfilerCallback::ClassLoadFinished](../../../../docs/framework/unmanaged-api/profiling/icorprofilercallback-classloadfinished-method.md) méthode est appelée.</span><span class="sxs-lookup"><span data-stu-id="a907f-108">The value of `classId` is not valid for an information request until the [ICorProfilerCallback::ClassLoadFinished](../../../../docs/framework/unmanaged-api/profiling/icorprofilercallback-classloadfinished-method.md) method is called.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="a907f-109">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="a907f-109">Requirements</span></span>  
 <span data-ttu-id="a907f-110">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="a907f-110">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="a907f-111">**En-tête :** CorProf.idl, CorProf.h</span><span class="sxs-lookup"><span data-stu-id="a907f-111">**Header:** CorProf.idl, CorProf.h</span></span>  
  
 <span data-ttu-id="a907f-112">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="a907f-112">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="a907f-113">**Versions du .NET Framework :** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="a907f-113">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="a907f-114">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a907f-114">See also</span></span>

- [<span data-ttu-id="a907f-115">ICorProfilerCallback, interface</span><span class="sxs-lookup"><span data-stu-id="a907f-115">ICorProfilerCallback Interface</span></span>](../../../../docs/framework/unmanaged-api/profiling/icorprofilercallback-interface.md)
