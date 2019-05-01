---
title: ICLRDomainManager, interface
ms.date: 03/30/2017
api_name:
- ICLRDomainManager
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- ICLRDomainManager
helpviewer_keywords:
- ICLRDomainManager interface [.NET Framework hosting]
ms.assetid: f08b2390-d872-4521-a815-e9c237c4c45d
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: ce53149b92ca40ad50ecbefaf4701940e8567ae5
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61984748"
---
# <a name="iclrdomainmanager-interface"></a><span data-ttu-id="192f4-102">ICLRDomainManager, interface</span><span class="sxs-lookup"><span data-stu-id="192f4-102">ICLRDomainManager Interface</span></span>
<span data-ttu-id="192f4-103">Permet à l’hôte spécifier le Gestionnaire de domaine d’application qui sera utilisé pour initialiser le domaine d’application par défaut et pour spécifier les propriétés d’initialisation.</span><span class="sxs-lookup"><span data-stu-id="192f4-103">Enables the host to specify the application domain manager that will be used to initialize the default application domain, and to specify initialization properties.</span></span>  
  
## <a name="methods"></a><span data-ttu-id="192f4-104">Méthodes</span><span class="sxs-lookup"><span data-stu-id="192f4-104">Methods</span></span>  
  
|<span data-ttu-id="192f4-105">Méthode</span><span class="sxs-lookup"><span data-stu-id="192f4-105">Method</span></span>|<span data-ttu-id="192f4-106">Description</span><span class="sxs-lookup"><span data-stu-id="192f4-106">Description</span></span>|  
|------------|-----------------|  
|[<span data-ttu-id="192f4-107">SetAppDomainManagerType, méthode</span><span class="sxs-lookup"><span data-stu-id="192f4-107">SetAppDomainManagerType Method</span></span>](../../../../docs/framework/unmanaged-api/hosting/iclrdomainmanager-setappdomainmanagertype-method.md)|<span data-ttu-id="192f4-108">Spécifie le type, dérivé de la <xref:System.AppDomainManager?displayProperty=nameWithType> classe, du Gestionnaire de domaine qui sera utilisé pour initialiser le domaine d’application par défaut.</span><span class="sxs-lookup"><span data-stu-id="192f4-108">Specifies the type, derived from the <xref:System.AppDomainManager?displayProperty=nameWithType> class, of the application domain manager that will be used to initialize the default application domain.</span></span>|  
|[<span data-ttu-id="192f4-109">SetPropertiesForDefaultAppDomain, méthode</span><span class="sxs-lookup"><span data-stu-id="192f4-109">SetPropertiesForDefaultAppDomain Method</span></span>](../../../../docs/framework/unmanaged-api/hosting/iclrdomainmanager-setpropertiesfordefaultappdomain-method.md)|<span data-ttu-id="192f4-110">Définit les propriétés qui seront utilisées pour initialiser le domaine d’application par défaut.</span><span class="sxs-lookup"><span data-stu-id="192f4-110">Sets properties that will be used to initialize the default application domain.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="192f4-111">Notes</span><span class="sxs-lookup"><span data-stu-id="192f4-111">Remarks</span></span>  
 <span data-ttu-id="192f4-112">Pour obtenir une instance de cette interface, appelez le [ICLRControl::GetCLRManager](../../../../docs/framework/unmanaged-api/hosting/iclrcontrol-getclrmanager-method.md) méthode avec le type de gestionnaire IID `IID_ICLRDomainManager`.</span><span class="sxs-lookup"><span data-stu-id="192f4-112">To get an instance of this interface, call the [ICLRControl::GetCLRManager](../../../../docs/framework/unmanaged-api/hosting/iclrcontrol-getclrmanager-method.md) method with the manager type IID `IID_ICLRDomainManager`.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="192f4-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="192f4-113">Requirements</span></span>  
 <span data-ttu-id="192f4-114">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="192f4-114">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="192f4-115">**En-tête :** MetaHost.h</span><span class="sxs-lookup"><span data-stu-id="192f4-115">**Header:** MetaHost.h</span></span>  
  
 <span data-ttu-id="192f4-116">**Bibliothèque :** Inclus en tant que ressource dans MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="192f4-116">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="192f4-117">**Versions du .NET Framework :** [!INCLUDE[net_current_v40plus](../../../../includes/net-current-v40plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="192f4-117">**.NET Framework Versions:** [!INCLUDE[net_current_v40plus](../../../../includes/net-current-v40plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="192f4-118">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="192f4-118">See also</span></span>

- [<span data-ttu-id="192f4-119">Interfaces d’hébergement</span><span class="sxs-lookup"><span data-stu-id="192f4-119">Hosting Interfaces</span></span>](../../../../docs/framework/unmanaged-api/hosting/hosting-interfaces.md)
- [<span data-ttu-id="192f4-120">Hébergement</span><span class="sxs-lookup"><span data-stu-id="192f4-120">Hosting</span></span>](../../../../docs/framework/unmanaged-api/hosting/index.md)
