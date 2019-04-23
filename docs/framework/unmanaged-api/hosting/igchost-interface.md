---
title: IGCHost, interface
ms.date: 03/30/2017
api_name:
- IGCHost
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IGCHost
helpviewer_keywords:
- IGCHost interface [.NET Framework hosting]
ms.assetid: 9ad70ffd-6963-4ab2-8c84-3d86c3fb8deb
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 3202aa25261863dae953e3edac36f3406fa001d8
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59228170"
---
# <a name="igchost-interface"></a><span data-ttu-id="eb26d-102">IGCHost, interface</span><span class="sxs-lookup"><span data-stu-id="eb26d-102">IGCHost Interface</span></span>
<span data-ttu-id="eb26d-103">Fournit des méthodes pour obtenir des informations sur le système de garbage collection et contrôler certains aspects du garbage collection.</span><span class="sxs-lookup"><span data-stu-id="eb26d-103">Provides methods for obtaining information about the garbage collection system and for controlling some aspects of garbage collection.</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="eb26d-104">En commençant par le [!INCLUDE[net_v45](../../../../includes/net-v45-md.md)], vous pouvez utiliser la [IGCHost2::SetGCStartupLimitsEx](../../../../docs/framework/unmanaged-api/hosting/igchost2-setgcstartuplimitsex-method.md) méthode pour définir la taille d’un segment de garbage collection et la taille maximale de la génération du système de nettoyage 0 pour les valeurs supérieure à la `DWORD` limite imposée par le [SetGCStartupLimits](../../../../docs/framework/unmanaged-api/hosting/igchost-setgcstartuplimits-method.md) (méthode).</span><span class="sxs-lookup"><span data-stu-id="eb26d-104">Starting with the [!INCLUDE[net_v45](../../../../includes/net-v45-md.md)], you can use the [IGCHost2::SetGCStartupLimitsEx](../../../../docs/framework/unmanaged-api/hosting/igchost2-setgcstartuplimitsex-method.md) method to set the size of a garbage collection segment and the maximum size of the garbage collection system's generation 0 to values greater than the `DWORD` limit that is imposed by the [SetGCStartupLimits](../../../../docs/framework/unmanaged-api/hosting/igchost-setgcstartuplimits-method.md) method.</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="eb26d-105">Cette interface est destinée uniquement à une utilisation expert.</span><span class="sxs-lookup"><span data-stu-id="eb26d-105">This interface is for expert usage only.</span></span> <span data-ttu-id="eb26d-106">Il peut affecter les performances d’une application pour une utilisation incorrecte.</span><span class="sxs-lookup"><span data-stu-id="eb26d-106">It can affect the performance of an application if used improperly.</span></span>  
  
## <a name="methods"></a><span data-ttu-id="eb26d-107">Méthodes</span><span class="sxs-lookup"><span data-stu-id="eb26d-107">Methods</span></span>  
  
|<span data-ttu-id="eb26d-108">Méthode</span><span class="sxs-lookup"><span data-stu-id="eb26d-108">Method</span></span>|<span data-ttu-id="eb26d-109">Description</span><span class="sxs-lookup"><span data-stu-id="eb26d-109">Description</span></span>|  
|------------|-----------------|  
|[<span data-ttu-id="eb26d-110">Collect, méthode</span><span class="sxs-lookup"><span data-stu-id="eb26d-110">Collect Method</span></span>](../../../../docs/framework/unmanaged-api/hosting/igchost-collect-method.md)|<span data-ttu-id="eb26d-111">Force une collection pour la génération donnée, quel que soit l’état du garbage collection en cours.</span><span class="sxs-lookup"><span data-stu-id="eb26d-111">Forces a collection to occur for the given generation, regardless of the state of the current garbage collection.</span></span>|  
|[<span data-ttu-id="eb26d-112">GetStats, méthode</span><span class="sxs-lookup"><span data-stu-id="eb26d-112">GetStats Method</span></span>](../../../../docs/framework/unmanaged-api/hosting/igchost-getstats-method.md)|<span data-ttu-id="eb26d-113">Obtient les statistiques pour l’état actuel du système garbage collection.</span><span class="sxs-lookup"><span data-stu-id="eb26d-113">Gets the statistics for the current state of the garbage collection system.</span></span>|  
|[<span data-ttu-id="eb26d-114">GetThreadStats, méthode</span><span class="sxs-lookup"><span data-stu-id="eb26d-114">GetThreadStats Method</span></span>](../../../../docs/framework/unmanaged-api/hosting/igchost-getthreadstats-method.md)|<span data-ttu-id="eb26d-115">Obtient les statistiques par thread pour le garbage collection.</span><span class="sxs-lookup"><span data-stu-id="eb26d-115">Gets the per-thread statistics for garbage collection.</span></span>|  
|[<span data-ttu-id="eb26d-116">SetGCStartupLimits, méthode</span><span class="sxs-lookup"><span data-stu-id="eb26d-116">SetGCStartupLimits Method</span></span>](../../../../docs/framework/unmanaged-api/hosting/igchost-setgcstartuplimits-method.md)|<span data-ttu-id="eb26d-117">Définit la taille du segment et la taille maximale pour la génération 0.</span><span class="sxs-lookup"><span data-stu-id="eb26d-117">Sets the segment size and the maximum size for generation 0.</span></span>|  
|[<span data-ttu-id="eb26d-118">SetVirtualMemLimit, méthode</span><span class="sxs-lookup"><span data-stu-id="eb26d-118">SetVirtualMemLimit Method</span></span>](../../../../docs/framework/unmanaged-api/hosting/igchost-setvirtualmemlimit-method.md)|<span data-ttu-id="eb26d-119">Définit la taille maximale de mémoire virtuelle du runtime.</span><span class="sxs-lookup"><span data-stu-id="eb26d-119">Sets the maximum size of the runtime's virtual memory.</span></span>|  
  
## <a name="requirements"></a><span data-ttu-id="eb26d-120">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="eb26d-120">Requirements</span></span>  
 <span data-ttu-id="eb26d-121">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="eb26d-121">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="eb26d-122">**En-tête :** GCHost.idl, GCHost.h</span><span class="sxs-lookup"><span data-stu-id="eb26d-122">**Header:** GCHost.idl, GCHost.h</span></span>  
  
 <span data-ttu-id="eb26d-123">**Bibliothèque :** Inclus en tant que ressource dans MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="eb26d-123">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="eb26d-124">**Versions du .NET Framework :** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="eb26d-124">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="eb26d-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="eb26d-125">See also</span></span>

- [<span data-ttu-id="eb26d-126">Interfaces d’hébergement</span><span class="sxs-lookup"><span data-stu-id="eb26d-126">Hosting Interfaces</span></span>](../../../../docs/framework/unmanaged-api/hosting/hosting-interfaces.md)
- [<span data-ttu-id="eb26d-127">CorRuntimeHost, coclasse</span><span class="sxs-lookup"><span data-stu-id="eb26d-127">CorRuntimeHost Coclass</span></span>](../../../../docs/framework/unmanaged-api/hosting/corruntimehost-coclass.md)
