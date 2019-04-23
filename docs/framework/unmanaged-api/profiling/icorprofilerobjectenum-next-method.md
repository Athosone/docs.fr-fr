---
title: ICorProfilerObjectEnum::Next, méthode
ms.date: 03/30/2017
api_name:
- ICorProfilerObjectEnum.Next
api_location:
- mscorwks.dll
api_type:
- COM
f1_keywords:
- ICorProfilerObjectEnum::Next
helpviewer_keywords:
- Next method, ICorProfilerObjectEnum interface [.NET Framework profiling]
- ICorProfilerObjectEnum::Next method [.NET Framework profiling]
ms.assetid: b420433c-5ebe-4986-bba1-97902e6db819
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: 221752b537cd3a890ad646290a64a7022692f625
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59173938"
---
# <a name="icorprofilerobjectenumnext-method"></a><span data-ttu-id="d44bb-102">ICorProfilerObjectEnum::Next, méthode</span><span class="sxs-lookup"><span data-stu-id="d44bb-102">ICorProfilerObjectEnum::Next Method</span></span>
<span data-ttu-id="d44bb-103">Obtient le nombre spécifié d’objets contigus dans une collection séquentielle d’objets, en commençant à la position actuelle de l’énumérateur dans la séquence.</span><span class="sxs-lookup"><span data-stu-id="d44bb-103">Gets the specified number of contiguous objects from a sequential collection of objects, starting at the enumerator's current position in the sequence.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="d44bb-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="d44bb-104">Syntax</span></span>  
  
```  
HRESULT Next (  
    [in] ULONG                    celt,  
    [out, size_is(celt), length_is(*pceltFetched)]    
        ObjectID                  objects[],  
    [out] ULONG                   *pceltFetched  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="d44bb-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="d44bb-105">Parameters</span></span>  
 `celt`  
 <span data-ttu-id="d44bb-106">[in] Nombre d'objets à récupérer.</span><span class="sxs-lookup"><span data-stu-id="d44bb-106">[in] The number of objects to be retrieved.</span></span>  
  
 `objects`  
 <span data-ttu-id="d44bb-107">[out] Un tableau de `ObjectID` valeurs, chacune représentant un objet récupéré.</span><span class="sxs-lookup"><span data-stu-id="d44bb-107">[out] An array of `ObjectID` values, each of which represents a retrieved object.</span></span>  
  
 `pceltFetched`  
 <span data-ttu-id="d44bb-108">[out] Pointeur vers le nombre d'éléments réellement retournés dans le tableau `objects`.</span><span class="sxs-lookup"><span data-stu-id="d44bb-108">[out] A pointer to the number of elements actually returned in the `objects` array.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="d44bb-109">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="d44bb-109">Requirements</span></span>  
 <span data-ttu-id="d44bb-110">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="d44bb-110">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="d44bb-111">**En-tête :** CorProf.idl, CorProf.h</span><span class="sxs-lookup"><span data-stu-id="d44bb-111">**Header:** CorProf.idl, CorProf.h</span></span>  
  
 <span data-ttu-id="d44bb-112">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="d44bb-112">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="d44bb-113">**Versions du .NET Framework :** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="d44bb-113">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="d44bb-114">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d44bb-114">See also</span></span>

- [<span data-ttu-id="d44bb-115">ICorProfilerObjectEnum, interface</span><span class="sxs-lookup"><span data-stu-id="d44bb-115">ICorProfilerObjectEnum Interface</span></span>](../../../../docs/framework/unmanaged-api/profiling/icorprofilerobjectenum-interface.md)
