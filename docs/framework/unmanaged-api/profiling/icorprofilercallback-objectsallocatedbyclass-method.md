---
title: ICorProfilerCallback::ObjectsAllocatedByClass, méthode
ms.date: 03/30/2017
api_name:
- ICorProfilerCallback.ObjectsAllocatedByClass
api_location:
- mscorwks.dll
api_type:
- COM
f1_keywords:
- ICorProfilerCallback::ObjectsAllocatedByClass
helpviewer_keywords:
- ObjectsAllocatedByClass method [.NET Framework profiling]
- ICorProfilerCallback::ObjectsAllocatedByClass method [.NET Framework profiling]
ms.assetid: 91d688f3-a80e-419d-9755-ff94bc04188a
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: b9f5d2c08abbcab6bc1a6d0569b8e70d7c919def
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59195863"
---
# <a name="icorprofilercallbackobjectsallocatedbyclass-method"></a><span data-ttu-id="936db-102">ICorProfilerCallback::ObjectsAllocatedByClass, méthode</span><span class="sxs-lookup"><span data-stu-id="936db-102">ICorProfilerCallback::ObjectsAllocatedByClass Method</span></span>
<span data-ttu-id="936db-103">Informe le profileur sur le nombre d’instances de chaque classe spécifiée qui ont été créés depuis le dernier garbage collection.</span><span class="sxs-lookup"><span data-stu-id="936db-103">Notifies the profiler about the number of instances of each specified class that have been created since the most recent garbage collection.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="936db-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="936db-104">Syntax</span></span>  
  
```  
HRESULT ObjectsAllocatedByClass(  
    [in] ULONG   cClassCount,  
    [in, size_is(cClassCount)] ClassID classIds[] ,  
    [in, size_is(cClassCount)] ULONG   cObjects[] );  
```  
  
## <a name="parameters"></a><span data-ttu-id="936db-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="936db-105">Parameters</span></span>  
 `cClassCount`  
 <span data-ttu-id="936db-106">[in] La taille de la `classIds` et `cObjects` tableaux.</span><span class="sxs-lookup"><span data-stu-id="936db-106">[in] The size of the `classIds` and `cObjects` arrays.</span></span>  
  
 `classIds`  
 <span data-ttu-id="936db-107">[in] Tableau d’ID, où chaque ID spécifie une classe avec une ou plusieurs instances de classe.</span><span class="sxs-lookup"><span data-stu-id="936db-107">[in] An array of class IDs, where each ID specifies a class with one or more instances.</span></span>  
  
 `cObjects`  
 <span data-ttu-id="936db-108">[in] Un tableau d’entiers, où chaque entier spécifie le nombre d’instances pour la classe correspondante dans le `classIds` tableau.</span><span class="sxs-lookup"><span data-stu-id="936db-108">[in] An array of integers, where each integer specifies the number of instances for the corresponding class in the `classIds` array.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="936db-109">Notes</span><span class="sxs-lookup"><span data-stu-id="936db-109">Remarks</span></span>  
 <span data-ttu-id="936db-110">Le `classIds` et `cObjects` tableaux sont des tableaux parallèles.</span><span class="sxs-lookup"><span data-stu-id="936db-110">The `classIds` and `cObjects` arrays are parallel arrays.</span></span> <span data-ttu-id="936db-111">Par exemple, `classIds[i]` et `cObjects[i]` référencent la même classe.</span><span class="sxs-lookup"><span data-stu-id="936db-111">For example, `classIds[i]` and `cObjects[i]` reference the same class.</span></span> <span data-ttu-id="936db-112">Si aucune instance d’une classe n’a été créé depuis le dernier garbage collection, la classe est omise.</span><span class="sxs-lookup"><span data-stu-id="936db-112">If no instance of a class has been created since the previous garbage collection, the class is omitted.</span></span> <span data-ttu-id="936db-113">Le `ObjectsAllocatedByClass` rappel ne signale pas les objets alloués dans le tas d’objets volumineux.</span><span class="sxs-lookup"><span data-stu-id="936db-113">The `ObjectsAllocatedByClass` callback will not report objects allocated in the large object heap.</span></span>  
  
 <span data-ttu-id="936db-114">Les nombres signalés par `ObjectsAllocatedByClass` ne sont que des estimations.</span><span class="sxs-lookup"><span data-stu-id="936db-114">The numbers reported by `ObjectsAllocatedByClass` are only estimates.</span></span> <span data-ttu-id="936db-115">Pour des nombres exacts, utilisez [ICorProfilerCallback::ObjectAllocated](../../../../docs/framework/unmanaged-api/profiling/icorprofilercallback-objectallocated-method.md).</span><span class="sxs-lookup"><span data-stu-id="936db-115">For exact counts, use [ICorProfilerCallback::ObjectAllocated](../../../../docs/framework/unmanaged-api/profiling/icorprofilercallback-objectallocated-method.md).</span></span>  
  
 <span data-ttu-id="936db-116">Le `classIds` tableau peut contenir une ou plusieurs entrées null si le correspondant `cObjects` tableau possède des types qui sont le déchargement.</span><span class="sxs-lookup"><span data-stu-id="936db-116">The `classIds` array may contain one or more null entries if the corresponding `cObjects` array has types that are unloading.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="936db-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="936db-117">Requirements</span></span>  
 <span data-ttu-id="936db-118">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="936db-118">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="936db-119">**En-tête :** CorProf.idl, CorProf.h</span><span class="sxs-lookup"><span data-stu-id="936db-119">**Header:** CorProf.idl, CorProf.h</span></span>  
  
 <span data-ttu-id="936db-120">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="936db-120">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="936db-121">**Versions du .NET Framework :** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="936db-121">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="936db-122">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="936db-122">See also</span></span>

- [<span data-ttu-id="936db-123">ICorProfilerCallback, interface</span><span class="sxs-lookup"><span data-stu-id="936db-123">ICorProfilerCallback Interface</span></span>](../../../../docs/framework/unmanaged-api/profiling/icorprofilercallback-interface.md)
