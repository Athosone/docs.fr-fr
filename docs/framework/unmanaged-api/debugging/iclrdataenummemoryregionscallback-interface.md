---
title: ICLRDataEnumMemoryRegionsCallback, interface
ms.date: 03/30/2017
api_name:
- ICLRDataEnumMemoryRegionsCallback
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICLRDataEnumMemoryRegionsCallback
helpviewer_keywords:
- ICLRDataEnumMemoryRegionsCallback interface [.NET Framework debugging]
ms.assetid: 3f1af8b0-8478-48e0-a7ec-3e90e0b97649
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: dad66c8a55982762ede754a4b3cd747b7a91b87d
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59225428"
---
# <a name="iclrdataenummemoryregionscallback-interface"></a><span data-ttu-id="3aba2-102">ICLRDataEnumMemoryRegionsCallback, interface</span><span class="sxs-lookup"><span data-stu-id="3aba2-102">ICLRDataEnumMemoryRegionsCallback Interface</span></span>
<span data-ttu-id="3aba2-103">Fournit une méthode de rappel pour [ICLRDataEnumMemoryRegions::EnumMemoryRegions](../../../../docs/framework/unmanaged-api/debugging/iclrdataenummemoryregions-enummemoryregions-method.md) pour signaler au débogueur le résultat d’une tentative d’énumération d’une région spécifiée de mémoire.</span><span class="sxs-lookup"><span data-stu-id="3aba2-103">Provides a callback method for [ICLRDataEnumMemoryRegions::EnumMemoryRegions](../../../../docs/framework/unmanaged-api/debugging/iclrdataenummemoryregions-enummemoryregions-method.md) to report to the debugger the result of an attempt to enumerate a specified region of memory.</span></span>  
  
## <a name="methods"></a><span data-ttu-id="3aba2-104">Méthodes</span><span class="sxs-lookup"><span data-stu-id="3aba2-104">Methods</span></span>  
  
|<span data-ttu-id="3aba2-105">Méthode</span><span class="sxs-lookup"><span data-stu-id="3aba2-105">Method</span></span>|<span data-ttu-id="3aba2-106">Description</span><span class="sxs-lookup"><span data-stu-id="3aba2-106">Description</span></span>|  
|------------|-----------------|  
|[<span data-ttu-id="3aba2-107">EnumMemoryRegion, méthode</span><span class="sxs-lookup"><span data-stu-id="3aba2-107">EnumMemoryRegion Method</span></span>](../../../../docs/framework/unmanaged-api/debugging/iclrdataenummemoryregionscallback-enummemoryregion-method.md)|<span data-ttu-id="3aba2-108">Appelé par `ICLRDataEnumMemoryRegions::EnumMemoryRegions` pour signaler au débogueur le résultat d’une tentative d’énumération d’une région spécifiée de mémoire.</span><span class="sxs-lookup"><span data-stu-id="3aba2-108">Called by `ICLRDataEnumMemoryRegions::EnumMemoryRegions` to report to the debugger the result of an attempt to enumerate a specified region of memory.</span></span>|  
  
## <a name="requirements"></a><span data-ttu-id="3aba2-109">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="3aba2-109">Requirements</span></span>  
 <span data-ttu-id="3aba2-110">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="3aba2-110">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="3aba2-111">**En-tête :** ClrData.idl, ClrData.h</span><span class="sxs-lookup"><span data-stu-id="3aba2-111">**Header:** ClrData.idl, ClrData.h</span></span>  
  
 <span data-ttu-id="3aba2-112">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="3aba2-112">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="3aba2-113">**Versions du .NET Framework :** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="3aba2-113">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="3aba2-114">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="3aba2-114">See also</span></span>

- [<span data-ttu-id="3aba2-115">Interfaces de débogage</span><span class="sxs-lookup"><span data-stu-id="3aba2-115">Debugging Interfaces</span></span>](../../../../docs/framework/unmanaged-api/debugging/debugging-interfaces.md)
