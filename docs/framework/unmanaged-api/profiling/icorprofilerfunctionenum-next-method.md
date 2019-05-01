---
title: ICorProfilerFunctionEnum::Next, méthode
ms.date: 03/30/2017
api_name:
- ICorProfilerFunctionEnum.Next Method
api_location:
- mscorwks.dll
api_type:
- COM
f1_keywords:
- ICorProfilerFunctionEnum::Next
helpviewer_keywords:
- ICorProfilerFunctionEnum::Next method [.NET Framework profiling]
- Next method, ICorProfilerFunctionEnum interface [.NET Framework profiling]
ms.assetid: 5ed4aa83-ce56-4b9f-9237-5da7587787fe
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: 62e70a2fe421651aac9a4921ca885c53c864c4f7
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61991950"
---
# <a name="icorprofilerfunctionenumnext-method"></a><span data-ttu-id="3863a-102">ICorProfilerFunctionEnum::Next, méthode</span><span class="sxs-lookup"><span data-stu-id="3863a-102">ICorProfilerFunctionEnum::Next Method</span></span>
<span data-ttu-id="3863a-103">Obtient le nombre spécifié de fonctions contiguës dans une collection séquentielle de fonctions, à commencer par la position actuelle de l'énumérateur dans la séquence.</span><span class="sxs-lookup"><span data-stu-id="3863a-103">Gets the specified number of contiguous functions from a sequential collection of functions, starting at the enumerator's current position in the sequence.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="3863a-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="3863a-104">Syntax</span></span>  
  
```  
HRESULT Next([in]  ULONG      celt,  
             [out, size_is(celt), length_is(*pceltFetched)]  
                    COR_PRF_FUNCTION ids[],  
             [out] ULONG *   pceltFetched);  
```  
  
## <a name="parameters"></a><span data-ttu-id="3863a-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="3863a-105">Parameters</span></span>  
 `celt`  
 <span data-ttu-id="3863a-106">[in] Nombre de fonctions à récupérer.</span><span class="sxs-lookup"><span data-stu-id="3863a-106">[in] The number of functions to retrieve.</span></span>  
  
 `ids`  
 <span data-ttu-id="3863a-107">[out] Tableau de valeurs `COR_PRF_FUNCTION` qui représentent chacune une fonction récupérée.</span><span class="sxs-lookup"><span data-stu-id="3863a-107">[out] An array of `COR_PRF_FUNCTION` values, each of which represents a retrieved function.</span></span>  
  
 `pceltFetched`  
 <span data-ttu-id="3863a-108">[out] Pointeur vers le nombre de fonctions réellement retournées dans le tableau `ids`.</span><span class="sxs-lookup"><span data-stu-id="3863a-108">[out] A pointer to the number of functions actually returned in the `ids` array.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="3863a-109">Valeur de retour</span><span class="sxs-lookup"><span data-stu-id="3863a-109">Return Value</span></span>  
 <span data-ttu-id="3863a-110">Cette méthode retourne les HRESULT spécifiques suivants ainsi que les erreurs HRESULT indiquant l'échec de la méthode.</span><span class="sxs-lookup"><span data-stu-id="3863a-110">This method returns the following specific HRESULTs as well as HRESULT errors that indicate method failure.</span></span>  
  
|<span data-ttu-id="3863a-111">HRESULT</span><span class="sxs-lookup"><span data-stu-id="3863a-111">HRESULT</span></span>|<span data-ttu-id="3863a-112">Description</span><span class="sxs-lookup"><span data-stu-id="3863a-112">Description</span></span>|  
|-------------|-----------------|  
|<span data-ttu-id="3863a-113">S_OK</span><span class="sxs-lookup"><span data-stu-id="3863a-113">S_OK</span></span>|<span data-ttu-id="3863a-114">`celt` éléments ont été retournés.</span><span class="sxs-lookup"><span data-stu-id="3863a-114">`celt` elements were returned.</span></span>|  
|<span data-ttu-id="3863a-115">S_FALSE</span><span class="sxs-lookup"><span data-stu-id="3863a-115">S_FALSE</span></span>|<span data-ttu-id="3863a-116">Moins de `celt` éléments ont été retournés, ce qui indique que l'énumération est terminée.</span><span class="sxs-lookup"><span data-stu-id="3863a-116">Fewer than `celt` elements were returned, which indicates that the enumeration is complete.</span></span>|  
  
## <a name="requirements"></a><span data-ttu-id="3863a-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="3863a-117">Requirements</span></span>  
 <span data-ttu-id="3863a-118">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="3863a-118">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="3863a-119">**En-tête :** CorProf.idl, CorProf.h</span><span class="sxs-lookup"><span data-stu-id="3863a-119">**Header:** CorProf.idl, CorProf.h</span></span>  
  
 <span data-ttu-id="3863a-120">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="3863a-120">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="3863a-121">**Versions du .NET Framework :** [!INCLUDE[net_current_v40plus](../../../../includes/net-current-v40plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="3863a-121">**.NET Framework Versions:** [!INCLUDE[net_current_v40plus](../../../../includes/net-current-v40plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="3863a-122">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="3863a-122">See also</span></span>

- [<span data-ttu-id="3863a-123">ICorProfilerFunctionEnum, interface</span><span class="sxs-lookup"><span data-stu-id="3863a-123">ICorProfilerFunctionEnum Interface</span></span>](../../../../docs/framework/unmanaged-api/profiling/icorprofilerfunctionenum-interface.md)
- [<span data-ttu-id="3863a-124">Interfaces de profilage</span><span class="sxs-lookup"><span data-stu-id="3863a-124">Profiling Interfaces</span></span>](../../../../docs/framework/unmanaged-api/profiling/profiling-interfaces.md)
