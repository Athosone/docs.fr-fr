---
title: ICorProfilerCallback::ExceptionSearchFilterEnter, méthode
ms.date: 03/30/2017
api_name:
- ICorProfilerCallback.ExceptionSearchFilterEnter
api_location:
- mscorwks.dll
api_type:
- COM
f1_keywords:
- ICorProfilerCallback::ExceptionSearchFilterEnter
helpviewer_keywords:
- ExceptionSearchFilterEnter method [.NET Framework profiling]
- ICorProfilerCallback::ExceptionSearchFilterEnter method [.NET Framework profiling]
ms.assetid: acc239ce-3eef-418c-b1df-c5a6dd8e8a4c
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: be91772f07e1a06c7df5b16fd70812e6a522d736
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59192587"
---
# <a name="icorprofilercallbackexceptionsearchfilterenter-method"></a><span data-ttu-id="f6f04-102">ICorProfilerCallback::ExceptionSearchFilterEnter, méthode</span><span class="sxs-lookup"><span data-stu-id="f6f04-102">ICorProfilerCallback::ExceptionSearchFilterEnter Method</span></span>
<span data-ttu-id="f6f04-103">Notifie le profileur que la phase de recherche de gestion des exceptions a commencé l’exécution d’un filtre d’exception définis par l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="f6f04-103">Notifies the profiler that the search phase of exception handling has begun executing a user-defined exception filter.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="f6f04-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="f6f04-104">Syntax</span></span>  
  
```  
HRESULT ExceptionSearchFilterEnter(  
    [in] FunctionID functionId);  
```  
  
## <a name="parameters"></a><span data-ttu-id="f6f04-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="f6f04-105">Parameters</span></span>  
 `functionId`  
 <span data-ttu-id="f6f04-106">[in] L’ID de la fonction qui contient le filtre.</span><span class="sxs-lookup"><span data-stu-id="f6f04-106">[in] The ID of the function that contains the filter.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="f6f04-107">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="f6f04-107">Requirements</span></span>  
 <span data-ttu-id="f6f04-108">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="f6f04-108">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="f6f04-109">**En-tête :** CorProf.idl, CorProf.h</span><span class="sxs-lookup"><span data-stu-id="f6f04-109">**Header:** CorProf.idl, CorProf.h</span></span>  
  
 <span data-ttu-id="f6f04-110">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="f6f04-110">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="f6f04-111">**Versions du .NET Framework :** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="f6f04-111">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="f6f04-112">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f6f04-112">See also</span></span>

- [<span data-ttu-id="f6f04-113">ICorProfilerCallback, interface</span><span class="sxs-lookup"><span data-stu-id="f6f04-113">ICorProfilerCallback Interface</span></span>](../../../../docs/framework/unmanaged-api/profiling/icorprofilercallback-interface.md)
- [<span data-ttu-id="f6f04-114">ExceptionSearchFilterLeave, méthode</span><span class="sxs-lookup"><span data-stu-id="f6f04-114">ExceptionSearchFilterLeave Method</span></span>](../../../../docs/framework/unmanaged-api/profiling/icorprofilercallback-exceptionsearchfilterleave-method.md)
