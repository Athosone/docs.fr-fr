---
title: ICorProfilerCallback::ExceptionCLRCatcherExecute, méthode
ms.date: 03/30/2017
api_name:
- ICorProfilerCallback.ExceptionCLRCatcherExecute
api_location:
- mscorwks.dll
api_type:
- COM
f1_keywords:
- ICorProfilerCallback::ExceptionCLRCatcherExecute
helpviewer_keywords:
- ExceptionCLRCatcherExecute method [.NET Framework profiling]
- ICorProfilerCallback::ExceptionCLRCatcherExecute method [.NET Framework profiling]
ms.assetid: aaac8f98-5cf4-42c7-b04b-556cce367e36
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: b640a6dee9ae50278d6a844d20d21eae156e9dd7
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59200959"
---
# <a name="icorprofilercallbackexceptionclrcatcherexecute-method"></a><span data-ttu-id="ab2fa-102">ICorProfilerCallback::ExceptionCLRCatcherExecute, méthode</span><span class="sxs-lookup"><span data-stu-id="ab2fa-102">ICorProfilerCallback::ExceptionCLRCatcherExecute Method</span></span>
<span data-ttu-id="ab2fa-103">Appelé lorsqu’un `catch` block pour une exception est exécutée dans le common language runtime (CLR) lui-même.</span><span class="sxs-lookup"><span data-stu-id="ab2fa-103">Called when a `catch` block for an exception is executed inside the common language runtime (CLR) itself.</span></span> <span data-ttu-id="ab2fa-104">Cette méthode est obsolète dans le .NET Framework version 2.0.</span><span class="sxs-lookup"><span data-stu-id="ab2fa-104">This method is obsolete in the .NET Framework version 2.0.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="ab2fa-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="ab2fa-105">Syntax</span></span>  
  
```  
HRESULT ExceptionCLRCatcherExecute();  
```  
  
## <a name="requirements"></a><span data-ttu-id="ab2fa-106">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="ab2fa-106">Requirements</span></span>  
 <span data-ttu-id="ab2fa-107">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="ab2fa-107">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="ab2fa-108">**En-tête :** CorProf.idl, CorProf.h</span><span class="sxs-lookup"><span data-stu-id="ab2fa-108">**Header:** CorProf.idl, CorProf.h</span></span>  
  
 <span data-ttu-id="ab2fa-109">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="ab2fa-109">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="ab2fa-110">**Versions du .NET framework :** 1.1, 1.0</span><span class="sxs-lookup"><span data-stu-id="ab2fa-110">**.NET Framework Versions:** 1.1, 1.0</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="ab2fa-111">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ab2fa-111">See also</span></span>

- [<span data-ttu-id="ab2fa-112">ICorProfilerCallback, interface</span><span class="sxs-lookup"><span data-stu-id="ab2fa-112">ICorProfilerCallback Interface</span></span>](../../../../docs/framework/unmanaged-api/profiling/icorprofilercallback-interface.md)
- [<span data-ttu-id="ab2fa-113">ExceptionCLRCatcherFound, méthode</span><span class="sxs-lookup"><span data-stu-id="ab2fa-113">ExceptionCLRCatcherFound Method</span></span>](../../../../docs/framework/unmanaged-api/profiling/icorprofilercallback-exceptionclrcatcherfound-method.md)
