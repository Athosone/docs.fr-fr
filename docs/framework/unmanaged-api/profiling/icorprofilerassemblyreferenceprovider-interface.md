---
title: ICorProfilerAssemblyReferenceProvider, interface
ms.date: 03/30/2017
api_name:
- ICorProfilerAssemblyReferenceProvider
api_location:
- mscorwks.dll
api_type:
- COM
ms.assetid: 17205116-66e1-4acc-8f01-532fb3867028
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 3bad1cc71b9a27896141837a6d342f2cfe068fc5
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61598659"
---
# <a name="icorprofilerassemblyreferenceprovider-interface"></a><span data-ttu-id="009d7-102">ICorProfilerAssemblyReferenceProvider, interface</span><span class="sxs-lookup"><span data-stu-id="009d7-102">ICorProfilerAssemblyReferenceProvider Interface</span></span>
<span data-ttu-id="009d7-103">[Pris en charge dans .NET Framework 4.5.2 et ultérieur]</span><span class="sxs-lookup"><span data-stu-id="009d7-103">[Supported in the .NET Framework 4.5.2 and later versions]</span></span>  
  
 <span data-ttu-id="009d7-104">Permet au profileur d’informer le common language runtime (CLR) des références d’assembly que le profileur ajoutera dans le [ICorProfilerCallback::ModuleLoadFinished](../../../../docs/framework/unmanaged-api/profiling/icorprofilercallback-moduleloadfinished-method.md) rappel.</span><span class="sxs-lookup"><span data-stu-id="009d7-104">Enables the profiler to inform the common language runtime (CLR) of assembly references that the profiler will add in the [ICorProfilerCallback::ModuleLoadFinished](../../../../docs/framework/unmanaged-api/profiling/icorprofilercallback-moduleloadfinished-method.md) callback.</span></span>  
  
## <a name="methods"></a><span data-ttu-id="009d7-105">Méthodes</span><span class="sxs-lookup"><span data-stu-id="009d7-105">Methods</span></span>  
  
|<span data-ttu-id="009d7-106">Méthode</span><span class="sxs-lookup"><span data-stu-id="009d7-106">Method</span></span>|<span data-ttu-id="009d7-107">Description</span><span class="sxs-lookup"><span data-stu-id="009d7-107">Description</span></span>|  
|------------|-----------------|  
|[<span data-ttu-id="009d7-108">AddAssemblyReference, méthode</span><span class="sxs-lookup"><span data-stu-id="009d7-108">AddAssemblyReference Method</span></span>](../../../../docs/framework/unmanaged-api/profiling/icorprofilerassemblyreferenceprovider-addassemblyreference-method.md)|<span data-ttu-id="009d7-109">Informe le CLR d’une référence d’assembly que le profileur prévoit d’ajouter dans le [ModuleLoadFinished](../../../../docs/framework/unmanaged-api/profiling/icorprofilercallback-moduleloadfinished-method.md) rappel.</span><span class="sxs-lookup"><span data-stu-id="009d7-109">Informs the CLR of an assembly reference that the profiler plans to add in the [ModuleLoadFinished](../../../../docs/framework/unmanaged-api/profiling/icorprofilercallback-moduleloadfinished-method.md) callback.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="009d7-110">Notes</span><span class="sxs-lookup"><span data-stu-id="009d7-110">Remarks</span></span>  
 <span data-ttu-id="009d7-111">Le CLR passe au profileur un `ICorProfilerAssemblyReferenceProvider` objet d’interface dans le [ICorProfilerCallback6::GetAssemblyReferences](../../../../docs/framework/unmanaged-api/profiling/icorprofilercallback6-getassemblyreferences-method.md) rappel.</span><span class="sxs-lookup"><span data-stu-id="009d7-111">The CLR passes the profiler an `ICorProfilerAssemblyReferenceProvider` interface object in the [ICorProfilerCallback6::GetAssemblyReferences](../../../../docs/framework/unmanaged-api/profiling/icorprofilercallback6-getassemblyreferences-method.md) callback.</span></span> <span data-ttu-id="009d7-112">Cela permet au profileur d’informer le CLR de références d’assembly que le profileur prévoit d’ajouter plus tard dans le [ICorProfilerCallback::ModuleLoadFinished](../../../../docs/framework/unmanaged-api/profiling/icorprofilercallback-moduleloadfinished-method.md).</span><span class="sxs-lookup"><span data-stu-id="009d7-112">This enables the profiler to inform the CLR of assembly references that the profiler plans to add later in the [ICorProfilerCallback::ModuleLoadFinished](../../../../docs/framework/unmanaged-api/profiling/icorprofilercallback-moduleloadfinished-method.md).</span></span> <span data-ttu-id="009d7-113">rappel.</span><span class="sxs-lookup"><span data-stu-id="009d7-113">callback.</span></span> <span data-ttu-id="009d7-114">Ceci améliore la précision de l'analyseur de fermeture de référence d'assembly du CLR et de ses algorithmes pour déterminer si les assemblys peuvent être partagés.</span><span class="sxs-lookup"><span data-stu-id="009d7-114">This improves the accuracy of the CLR's assembly reference closure walker and its algorithms for determining whether assemblies may be shared.</span></span>  
  
 <span data-ttu-id="009d7-115">Cette interface peut être utilisée uniquement dans le [ICorProfilerCallback6::GetAssemblyReferences](../../../../docs/framework/unmanaged-api/profiling/icorprofilercallback6-getassemblyreferences-method.md) rappel qui passe cet objet d’interface au profileur.</span><span class="sxs-lookup"><span data-stu-id="009d7-115">This interface can be used only in the [ICorProfilerCallback6::GetAssemblyReferences](../../../../docs/framework/unmanaged-api/profiling/icorprofilercallback6-getassemblyreferences-method.md) callback that passes this interface object to the profiler.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="009d7-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="009d7-116">Requirements</span></span>  
 <span data-ttu-id="009d7-117">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="009d7-117">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="009d7-118">**En-tête :** CorProf.idl, CorProf.h</span><span class="sxs-lookup"><span data-stu-id="009d7-118">**Header:** CorProf.idl, CorProf.h</span></span>  
  
 <span data-ttu-id="009d7-119">**Versions du .NET Framework :** [!INCLUDE[net_current_v452plus](../../../../includes/net-current-v452plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="009d7-119">**.NET Framework Versions:** [!INCLUDE[net_current_v452plus](../../../../includes/net-current-v452plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="009d7-120">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="009d7-120">See also</span></span>

- [<span data-ttu-id="009d7-121">Interfaces de profilage</span><span class="sxs-lookup"><span data-stu-id="009d7-121">Profiling Interfaces</span></span>](../../../../docs/framework/unmanaged-api/profiling/profiling-interfaces.md)
