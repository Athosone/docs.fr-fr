---
title: ICLRControl, interface
ms.date: 03/30/2017
api_name:
- ICLRControl
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- ICLRControl
helpviewer_keywords:
- ICLRControl interface [.NET Framework hosting]
ms.assetid: a24fd905-1fa6-45a0-ad65-e9e2ee58861e
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: f70e7958cc9ac198738ed72732fe7b6563c89067
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61970064"
---
# <a name="iclrcontrol-interface"></a><span data-ttu-id="e7f1a-102">ICLRControl, interface</span><span class="sxs-lookup"><span data-stu-id="e7f1a-102">ICLRControl Interface</span></span>
<span data-ttu-id="e7f1a-103">Fournit des méthodes qui permettent à un hôte obtenir des références à et configurez les aspects de, le common language runtime (CLR).</span><span class="sxs-lookup"><span data-stu-id="e7f1a-103">Provides methods that allow a host to get references to, and configure aspects of, the common language runtime (CLR).</span></span>  
  
## <a name="methods"></a><span data-ttu-id="e7f1a-104">Méthodes</span><span class="sxs-lookup"><span data-stu-id="e7f1a-104">Methods</span></span>  
  
|<span data-ttu-id="e7f1a-105">Méthode</span><span class="sxs-lookup"><span data-stu-id="e7f1a-105">Method</span></span>|<span data-ttu-id="e7f1a-106">Description</span><span class="sxs-lookup"><span data-stu-id="e7f1a-106">Description</span></span>|  
|------------|-----------------|  
|[<span data-ttu-id="e7f1a-107">GetCLRManager, méthode</span><span class="sxs-lookup"><span data-stu-id="e7f1a-107">GetCLRManager Method</span></span>](../../../../docs/framework/unmanaged-api/hosting/iclrcontrol-getclrmanager-method.md)|<span data-ttu-id="e7f1a-108">Obtient un pointeur d’interface à une instance d’un des types de manager que l’hôte peut utiliser pour configurer le CLR.</span><span class="sxs-lookup"><span data-stu-id="e7f1a-108">Gets an interface pointer to an instance of any of the manager types the host can use to configure the CLR.</span></span>|  
|[<span data-ttu-id="e7f1a-109">SetAppDomainManagerType, méthode</span><span class="sxs-lookup"><span data-stu-id="e7f1a-109">SetAppDomainManagerType Method</span></span>](../../../../docs/framework/unmanaged-api/hosting/iclrcontrol-setappdomainmanagertype-method.md)|<span data-ttu-id="e7f1a-110">Définit un type dérivé <xref:System.AppDomainManager> comme type pour les gestionnaires de domaine d’application.</span><span class="sxs-lookup"><span data-stu-id="e7f1a-110">Sets a type derived from <xref:System.AppDomainManager> as the type for application domain managers.</span></span>|  
  
## <a name="requirements"></a><span data-ttu-id="e7f1a-111">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="e7f1a-111">Requirements</span></span>  
 <span data-ttu-id="e7f1a-112">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="e7f1a-112">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="e7f1a-113">**En-tête :** MSCorEE.h</span><span class="sxs-lookup"><span data-stu-id="e7f1a-113">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="e7f1a-114">**Bibliothèque :** Inclus en tant que ressource dans MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="e7f1a-114">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="e7f1a-115">**Versions du .NET Framework :** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="e7f1a-115">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="e7f1a-116">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e7f1a-116">See also</span></span>

- [<span data-ttu-id="e7f1a-117">ICLRAssemblyIdentityManager, interface</span><span class="sxs-lookup"><span data-stu-id="e7f1a-117">ICLRAssemblyIdentityManager Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/iclrassemblyidentitymanager-interface.md)
- [<span data-ttu-id="e7f1a-118">ICLRDebugManager, interface</span><span class="sxs-lookup"><span data-stu-id="e7f1a-118">ICLRDebugManager Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/iclrdebugmanager-interface.md)
- [<span data-ttu-id="e7f1a-119">ICLRGCManager, interface</span><span class="sxs-lookup"><span data-stu-id="e7f1a-119">ICLRGCManager Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/iclrgcmanager-interface.md)
- [<span data-ttu-id="e7f1a-120">ICLRHostBindingPolicyManager, interface</span><span class="sxs-lookup"><span data-stu-id="e7f1a-120">ICLRHostBindingPolicyManager Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/iclrhostbindingpolicymanager-interface.md)
- [<span data-ttu-id="e7f1a-121">ICLRHostProtectionManager, interface</span><span class="sxs-lookup"><span data-stu-id="e7f1a-121">ICLRHostProtectionManager Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/iclrhostprotectionmanager-interface.md)
- [<span data-ttu-id="e7f1a-122">ICLROnEventManager, interface</span><span class="sxs-lookup"><span data-stu-id="e7f1a-122">ICLROnEventManager Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/iclroneventmanager-interface.md)
- [<span data-ttu-id="e7f1a-123">ICLRPolicyManager, interface</span><span class="sxs-lookup"><span data-stu-id="e7f1a-123">ICLRPolicyManager Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/iclrpolicymanager-interface.md)
- [<span data-ttu-id="e7f1a-124">IHostControl, interface</span><span class="sxs-lookup"><span data-stu-id="e7f1a-124">IHostControl Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/ihostcontrol-interface.md)
- [<span data-ttu-id="e7f1a-125">Interfaces d’hébergement</span><span class="sxs-lookup"><span data-stu-id="e7f1a-125">Hosting Interfaces</span></span>](../../../../docs/framework/unmanaged-api/hosting/hosting-interfaces.md)
