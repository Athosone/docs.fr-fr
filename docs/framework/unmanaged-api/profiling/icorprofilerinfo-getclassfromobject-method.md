---
title: ICorProfilerInfo::GetClassFromObject, méthode
ms.date: 03/30/2017
api_name:
- ICorProfilerInfo.GetClassFromObject
api_location:
- mscorwks.dll
api_type:
- COM
f1_keywords:
- ICorProfilerInfo::GetClassFromObject
helpviewer_keywords:
- GetClassFromObject method [.NET Framework profiling]
- ICorProfilerInfo::GetClassFromObject method [.NET Framework profiling]
ms.assetid: b97493fb-713e-49d5-a73e-5688b2ad0700
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: 81afb9b40269b04a59c54636c7e88c1f67189593
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59189545"
---
# <a name="icorprofilerinfogetclassfromobject-method"></a><span data-ttu-id="e45bc-102">ICorProfilerInfo::GetClassFromObject, méthode</span><span class="sxs-lookup"><span data-stu-id="e45bc-102">ICorProfilerInfo::GetClassFromObject Method</span></span>
<span data-ttu-id="e45bc-103">Obtient le `ClassID` d’un objet, étant donné son `ObjectID`.</span><span class="sxs-lookup"><span data-stu-id="e45bc-103">Gets the `ClassID` of an object, given its `ObjectID`.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="e45bc-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="e45bc-104">Syntax</span></span>  
  
```  
HRESULT GetClassFromObject(  
    [in]  ObjectID objectId,  
    [out] ClassID *pClassId);  
```  
  
## <a name="parameters"></a><span data-ttu-id="e45bc-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="e45bc-105">Parameters</span></span>  
 `objectId`  
 <span data-ttu-id="e45bc-106">[in] L’ID de l’objet pour lequel obtenir le `ClassID`.</span><span class="sxs-lookup"><span data-stu-id="e45bc-106">[in] The ID of the object for which to get the `ClassID`.</span></span>  
  
 `pClassId`  
 <span data-ttu-id="e45bc-107">[out] Un pointeur vers le texte retourné `ClassID`.</span><span class="sxs-lookup"><span data-stu-id="e45bc-107">[out] A pointer to the returned `ClassID`.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="e45bc-108">Notes</span><span class="sxs-lookup"><span data-stu-id="e45bc-108">Remarks</span></span>  
 <span data-ttu-id="e45bc-109">Une valeur null `pClassId` indique que `objectId` a un type qui est déchargement.</span><span class="sxs-lookup"><span data-stu-id="e45bc-109">A null `pClassId` indicates that `objectId` has a type that is unloading.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="e45bc-110">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="e45bc-110">Requirements</span></span>  
 <span data-ttu-id="e45bc-111">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="e45bc-111">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="e45bc-112">**En-tête :** CorProf.idl, CorProf.h</span><span class="sxs-lookup"><span data-stu-id="e45bc-112">**Header:** CorProf.idl, CorProf.h</span></span>  
  
 <span data-ttu-id="e45bc-113">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="e45bc-113">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="e45bc-114">**Versions du .NET Framework :** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="e45bc-114">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="e45bc-115">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e45bc-115">See also</span></span>

- [<span data-ttu-id="e45bc-116">ICorProfilerInfo, interface</span><span class="sxs-lookup"><span data-stu-id="e45bc-116">ICorProfilerInfo Interface</span></span>](../../../../docs/framework/unmanaged-api/profiling/icorprofilerinfo-interface.md)
