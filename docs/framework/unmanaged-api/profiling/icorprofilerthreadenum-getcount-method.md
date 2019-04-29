---
title: ICorProfilerThreadEnum::GetCount, méthode
ms.date: 03/30/2017
api_name:
- ICorProfilerThreadEnum.GetCount
api_location:
- mscorwks.dll
api_type:
- COM
f1_keywords:
- ICorProfilerThreadEnum::GetCount
helpviewer_keywords:
- ICorProfilerThreadEnum::GetCount method [.NET Framework profiling]
- GetCount method, ICorProfilerThreadEnum interface [.NET Framework profiling]
ms.assetid: d6dbdc4a-6115-455d-a3f3-704a81d3646b
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: 8b02f70f22a7d35bf0fe7816a52c490f88b31217
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61597126"
---
# <a name="icorprofilerthreadenumgetcount-method"></a><span data-ttu-id="8ef34-102">ICorProfilerThreadEnum::GetCount, méthode</span><span class="sxs-lookup"><span data-stu-id="8ef34-102">ICorProfilerThreadEnum::GetCount Method</span></span>
<span data-ttu-id="8ef34-103">Obtient le nombre de threads utilisés par l'application.</span><span class="sxs-lookup"><span data-stu-id="8ef34-103">Gets the number of threads that are used by the application.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="8ef34-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="8ef34-104">Syntax</span></span>  
  
```  
HRESULT GetCount (    [out] ULONG * pcelt  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="8ef34-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="8ef34-105">Parameters</span></span>  
 `celt`  
 <span data-ttu-id="8ef34-106">[out] Le nombre de threads utilisés par l’application.</span><span class="sxs-lookup"><span data-stu-id="8ef34-106">[out] The number of threads used by the application.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="8ef34-107">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="8ef34-107">Requirements</span></span>  
 <span data-ttu-id="8ef34-108">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="8ef34-108">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="8ef34-109">**En-tête :** CorProf.idl, CorProf.h</span><span class="sxs-lookup"><span data-stu-id="8ef34-109">**Header:** CorProf.idl, CorProf.h</span></span>  
  
 <span data-ttu-id="8ef34-110">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="8ef34-110">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="8ef34-111">**Versions du .NET Framework :** [!INCLUDE[net_current_v45plus](../../../../includes/net-current-v45plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="8ef34-111">**.NET Framework Versions:** [!INCLUDE[net_current_v45plus](../../../../includes/net-current-v45plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="8ef34-112">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="8ef34-112">See also</span></span>

- [<span data-ttu-id="8ef34-113">ICorProfilerThreadEnum, interface</span><span class="sxs-lookup"><span data-stu-id="8ef34-113">ICorProfilerThreadEnum Interface</span></span>](../../../../docs/framework/unmanaged-api/profiling/icorprofilerthreadenum-interface.md)
- [<span data-ttu-id="8ef34-114">Interfaces de profilage</span><span class="sxs-lookup"><span data-stu-id="8ef34-114">Profiling Interfaces</span></span>](../../../../docs/framework/unmanaged-api/profiling/profiling-interfaces.md)
