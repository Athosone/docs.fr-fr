---
title: IHostSecurityContext, interface
ms.date: 03/30/2017
api_name:
- IHostSecurityContext
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IHostSecurityContext
helpviewer_keywords:
- IHostSecurityContext interface [.NET Framework hosting]
ms.assetid: 88e2eac0-8ccb-404f-abbc-287d55159842
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 9d71b7e1265110a70329377ce8ab7430e1943c49
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61984293"
---
# <a name="ihostsecuritycontext-interface"></a><span data-ttu-id="0c83c-102">IHostSecurityContext, interface</span><span class="sxs-lookup"><span data-stu-id="0c83c-102">IHostSecurityContext Interface</span></span>
<span data-ttu-id="0c83c-103">Permet le common language runtime (CLR) pour gérer les informations de contexte de sécurité implémentées par l’hôte.</span><span class="sxs-lookup"><span data-stu-id="0c83c-103">Allows the common language runtime (CLR) to maintain security context information implemented by the host.</span></span>  
  
## <a name="methods"></a><span data-ttu-id="0c83c-104">Méthodes</span><span class="sxs-lookup"><span data-stu-id="0c83c-104">Methods</span></span>  
  
|<span data-ttu-id="0c83c-105">Méthode</span><span class="sxs-lookup"><span data-stu-id="0c83c-105">Method</span></span>|<span data-ttu-id="0c83c-106">Description</span><span class="sxs-lookup"><span data-stu-id="0c83c-106">Description</span></span>|  
|------------|-----------------|  
|[<span data-ttu-id="0c83c-107">Capture, méthode</span><span class="sxs-lookup"><span data-stu-id="0c83c-107">Capture Method</span></span>](../../../../docs/framework/unmanaged-api/hosting/ihostsecuritycontext-capture-method.md)|<span data-ttu-id="0c83c-108">Obtient un clone de le `IHostSecurityContext` instance retournée à partir d’un appel à [IHostSecurityManager::GetSecurityContext](../../../../docs/framework/unmanaged-api/hosting/ihostsecuritymanager-getsecuritycontext-method.md).</span><span class="sxs-lookup"><span data-stu-id="0c83c-108">Gets a clone of the `IHostSecurityContext` instance returned from a call to [IHostSecurityManager::GetSecurityContext](../../../../docs/framework/unmanaged-api/hosting/ihostsecuritymanager-getsecuritycontext-method.md).</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="0c83c-109">Notes</span><span class="sxs-lookup"><span data-stu-id="0c83c-109">Remarks</span></span>  
 <span data-ttu-id="0c83c-110">Un hôte peut contrôler tous les accès de code aux jetons de thread par le code CLR et utilisateur.</span><span class="sxs-lookup"><span data-stu-id="0c83c-110">A host can control all code access to thread tokens by both the CLR and user code.</span></span> <span data-ttu-id="0c83c-111">Il peut également garantir que la sécurité complète des informations de contexte sont passées aux opérations asynchrones ou des points de code avec accès restreint au code.</span><span class="sxs-lookup"><span data-stu-id="0c83c-111">It can also ensure that complete security context information is passed across asynchronous operations or code points with restricted code access.</span></span> <span data-ttu-id="0c83c-112">`IHostSecurityContext` encapsule ces informations de contexte de sécurité, qui sont opaques à l’exécution.</span><span class="sxs-lookup"><span data-stu-id="0c83c-112">`IHostSecurityContext` encapsulates this security context information, which is opaque to the runtime.</span></span> <span data-ttu-id="0c83c-113">Le runtime intercepte cette information à l’aide de `Capture`, et les déplace dans la répartition d’élément de travail de pool de threads, l’exécution du finaliseur et les constructeurs de module et de classe.</span><span class="sxs-lookup"><span data-stu-id="0c83c-113">The runtime captures this information using `Capture`, and moves it across thread pool worker item dispatch, finalizer execution, and module and class constructors.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="0c83c-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="0c83c-114">Requirements</span></span>  
 <span data-ttu-id="0c83c-115">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="0c83c-115">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="0c83c-116">**En-tête :** MSCorEE.h</span><span class="sxs-lookup"><span data-stu-id="0c83c-116">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="0c83c-117">**Bibliothèque :** Inclus en tant que ressource dans MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="0c83c-117">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="0c83c-118">**Versions du .NET Framework :** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="0c83c-118">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="0c83c-119">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0c83c-119">See also</span></span>

- [<span data-ttu-id="0c83c-120">ICLRHostProtectionManager, interface</span><span class="sxs-lookup"><span data-stu-id="0c83c-120">ICLRHostProtectionManager Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/iclrhostprotectionmanager-interface.md)
- [<span data-ttu-id="0c83c-121">IHostSecurityManager, interface</span><span class="sxs-lookup"><span data-stu-id="0c83c-121">IHostSecurityManager Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/ihostsecuritymanager-interface.md)
- [<span data-ttu-id="0c83c-122">Interfaces d’hébergement</span><span class="sxs-lookup"><span data-stu-id="0c83c-122">Hosting Interfaces</span></span>](../../../../docs/framework/unmanaged-api/hosting/hosting-interfaces.md)
