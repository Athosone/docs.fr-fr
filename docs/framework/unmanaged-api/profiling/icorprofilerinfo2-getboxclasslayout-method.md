---
title: ICorProfilerInfo2::GetBoxClassLayout, méthode
ms.date: 03/30/2017
api_name:
- ICorProfilerInfo2.GetBoxClassLayout
api_location:
- mscorwks.dll
api_type:
- COM
f1_keywords:
- ICorProfilerInfo2::GetBoxClassLayout
helpviewer_keywords:
- GetBoxClassLayout method [.NET Framework profiling]
- ICorProfilerInfo2::GetBoxClassLayout method [.NET Framework profiling]
ms.assetid: 624672b5-1189-488a-85d2-3e12b49617c1
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: 4dac7e38d1e767a3edeef932a0c0916daffe24b8
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62049568"
---
# <a name="icorprofilerinfo2getboxclasslayout-method"></a><span data-ttu-id="aec1a-102">ICorProfilerInfo2::GetBoxClassLayout, méthode</span><span class="sxs-lookup"><span data-stu-id="aec1a-102">ICorProfilerInfo2::GetBoxClassLayout Method</span></span>
<span data-ttu-id="aec1a-103">Obtient des informations sur l’emplacement du type valeur spécifié lorsqu’il est boxed.</span><span class="sxs-lookup"><span data-stu-id="aec1a-103">Gets information about where the specified value type is located when it is boxed.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="aec1a-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="aec1a-104">Syntax</span></span>  
  
```  
HRESULT GetBoxClassLayout(  
    [in] ClassID classId,  
    [out] ULONG32 *pBufferOffset);  
```  
  
## <a name="parameters"></a><span data-ttu-id="aec1a-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="aec1a-105">Parameters</span></span>  
 `classId`  
 <span data-ttu-id="aec1a-106">[in] L’ID de la classe qui décrit le type de valeur est boxed.</span><span class="sxs-lookup"><span data-stu-id="aec1a-106">[in] The ID of the class that describes the value type that is boxed.</span></span>  
  
 `pBufferOffset`  
 <span data-ttu-id="aec1a-107">[out] Entier qui est le décalage par rapport au pointeur de l’ID objet boxed, du type de valeur.</span><span class="sxs-lookup"><span data-stu-id="aec1a-107">[out] An integer that is the offset, relative to the boxed object ID pointer, of the value type.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="aec1a-108">Notes</span><span class="sxs-lookup"><span data-stu-id="aec1a-108">Remarks</span></span>  
 <span data-ttu-id="aec1a-109">Le `pBufferOffset` valeur est l’emplacement du type valeur dans une zone.</span><span class="sxs-lookup"><span data-stu-id="aec1a-109">The `pBufferOffset` value is the location of the value type within a box.</span></span> <span data-ttu-id="aec1a-110">Après avoir `pBufferOffset` est appliqué à un objet boxed, disposition de classe du type valeur peut être utilisée pour interpréter la valeur de l’objet.</span><span class="sxs-lookup"><span data-stu-id="aec1a-110">After `pBufferOffset` is applied to a boxed object, the value type's class layout can be used to interpret the object's value.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="aec1a-111">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="aec1a-111">Requirements</span></span>  
 <span data-ttu-id="aec1a-112">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="aec1a-112">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="aec1a-113">**En-tête :** CorProf.idl, CorProf.h</span><span class="sxs-lookup"><span data-stu-id="aec1a-113">**Header:** CorProf.idl, CorProf.h</span></span>  
  
 <span data-ttu-id="aec1a-114">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="aec1a-114">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="aec1a-115">**Versions du .NET Framework :** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="aec1a-115">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="aec1a-116">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="aec1a-116">See also</span></span>

- [<span data-ttu-id="aec1a-117">ICorProfilerInfo, interface</span><span class="sxs-lookup"><span data-stu-id="aec1a-117">ICorProfilerInfo Interface</span></span>](../../../../docs/framework/unmanaged-api/profiling/icorprofilerinfo-interface.md)
- [<span data-ttu-id="aec1a-118">ICorProfilerInfo2, interface</span><span class="sxs-lookup"><span data-stu-id="aec1a-118">ICorProfilerInfo2 Interface</span></span>](../../../../docs/framework/unmanaged-api/profiling/icorprofilerinfo2-interface.md)
