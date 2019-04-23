---
title: IGCHost2, interface
ms.date: 03/30/2017
api_name:
- IGCHost2
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IGCHost2
helpviewer_keywords:
- IGCHost2 interface [.NET Framework hosting]
ms.assetid: e5323fa4-18ac-424d-859d-a65a550d08d9
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 75bef91eb70c8109653741452362cd2e85f625ce
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59138136"
---
# <a name="igchost2-interface"></a><span data-ttu-id="e228e-102">IGCHost2, interface</span><span class="sxs-lookup"><span data-stu-id="e228e-102">IGCHost2 Interface</span></span>
<span data-ttu-id="e228e-103">Fournit des méthodes pour obtenir des informations sur le système de garbage collection et contrôler certains aspects du garbage collection.</span><span class="sxs-lookup"><span data-stu-id="e228e-103">Provides methods for obtaining information about the garbage collection system and for controlling some aspects of garbage collection.</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="e228e-104">Pour tout nouveau développement, nous vous recommandons d’utiliser le [ICLRGCManager2](../../../../docs/framework/unmanaged-api/hosting/iclrgcmanager2-interface.md) à la place de l’interface.</span><span class="sxs-lookup"><span data-stu-id="e228e-104">For new development, we recommend that you use the [ICLRGCManager2](../../../../docs/framework/unmanaged-api/hosting/iclrgcmanager2-interface.md) interface instead.</span></span>  
  
## <a name="methods"></a><span data-ttu-id="e228e-105">Méthodes</span><span class="sxs-lookup"><span data-stu-id="e228e-105">Methods</span></span>  
  
|<span data-ttu-id="e228e-106">Méthode</span><span class="sxs-lookup"><span data-stu-id="e228e-106">Method</span></span>|<span data-ttu-id="e228e-107">Description</span><span class="sxs-lookup"><span data-stu-id="e228e-107">Description</span></span>|  
|------------|-----------------|  
|[<span data-ttu-id="e228e-108">SetGCStartupLimitsEx, méthode</span><span class="sxs-lookup"><span data-stu-id="e228e-108">SetGCStartupLimitsEx Method</span></span>](../../../../docs/framework/unmanaged-api/hosting/igchost2-setgcstartuplimitsex-method.md)|<span data-ttu-id="e228e-109">Définit la taille du segment et la taille maximale pour la génération 0.</span><span class="sxs-lookup"><span data-stu-id="e228e-109">Sets the segment size and the maximum size for generation 0.</span></span> <span data-ttu-id="e228e-110">Permet la génération 0 et les tailles de segment supérieures à `DWORD`.</span><span class="sxs-lookup"><span data-stu-id="e228e-110">Enables generation 0 and segment sizes larger than `DWORD`.</span></span>|  
  
## <a name="requirements"></a><span data-ttu-id="e228e-111">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="e228e-111">Requirements</span></span>  
 <span data-ttu-id="e228e-112">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="e228e-112">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="e228e-113">**En-tête :** GCHost.idl, GCHost.h</span><span class="sxs-lookup"><span data-stu-id="e228e-113">**Header:** GCHost.idl, GCHost.h</span></span>  
  
 <span data-ttu-id="e228e-114">**Bibliothèque :** Inclus en tant que ressource dans MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="e228e-114">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="e228e-115">**Versions du .NET Framework :** [!INCLUDE[net_current_v45plus](../../../../includes/net-current-v45plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="e228e-115">**.NET Framework Versions:** [!INCLUDE[net_current_v45plus](../../../../includes/net-current-v45plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="e228e-116">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e228e-116">See also</span></span>

- [<span data-ttu-id="e228e-117">Interfaces d’hébergement</span><span class="sxs-lookup"><span data-stu-id="e228e-117">Hosting Interfaces</span></span>](../../../../docs/framework/unmanaged-api/hosting/hosting-interfaces.md)
- [<span data-ttu-id="e228e-118">Interfaces d’hébergement CLR</span><span class="sxs-lookup"><span data-stu-id="e228e-118">CLR Hosting Interfaces</span></span>](../../../../docs/framework/unmanaged-api/hosting/clr-hosting-interfaces.md)
- [<span data-ttu-id="e228e-119">CorRuntimeHost, coclasse</span><span class="sxs-lookup"><span data-stu-id="e228e-119">CorRuntimeHost Coclass</span></span>](../../../../docs/framework/unmanaged-api/hosting/corruntimehost-coclass.md)
