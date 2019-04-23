---
title: EApiCategories, énumération
ms.date: 03/30/2017
api_name:
- EApiCategories
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- EApiCategories
helpviewer_keywords:
- EApiCategories enumeration [.NET Framework hosting]
ms.assetid: 3c4a8a5a-8a46-4ac9-947f-4959bc9d6ac6
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 3debd3f13d78841188dd8c900f51c0110e1d4c67
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59086453"
---
# <a name="eapicategories-enumeration"></a><span data-ttu-id="2c510-102">EApiCategories, énumération</span><span class="sxs-lookup"><span data-stu-id="2c510-102">EApiCategories Enumeration</span></span>
<span data-ttu-id="2c510-103">Décrit les catégories de fonctionnalités que l’hôte peut bloquer l’exécution dans du code partiellement fiable.</span><span class="sxs-lookup"><span data-stu-id="2c510-103">Describes the categories of capabilities that the host can block from running in partially trusted code.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="2c510-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="2c510-104">Syntax</span></span>  
  
```  
typedef enum {  
    eNoCategory               = 0,  
    eSynchronization          = 0x1,  
    eSharedState              = 0x2,  
    eExternalProcessMgmt      = 0x4,  
    eSelfAffectingProcessMgmt = 0x8,  
    eExternalThreading        = 0x10,  
    eSelfAffectingThreading   = 0x20,  
    eSecurityInfrastructure   = 0x40,  
    eUI                       = 0x80,  
    eMayLeakOnAbort           = 0x100,  
    eAll                      = 0x1ff  
} EHostProtectionCategories;  
```  
  
## <a name="members"></a><span data-ttu-id="2c510-105">Membres</span><span class="sxs-lookup"><span data-stu-id="2c510-105">Members</span></span>  
  
|<span data-ttu-id="2c510-106">Membre</span><span class="sxs-lookup"><span data-stu-id="2c510-106">Member</span></span>|<span data-ttu-id="2c510-107">Description</span><span class="sxs-lookup"><span data-stu-id="2c510-107">Description</span></span>|  
|------------|-----------------|  
|`eAll`|<span data-ttu-id="2c510-108">Spécifie que tous les gérés classes et membres qui sont couverts par d’autres `EApiCategories` champs pas s’exécuter dans du code partiellement fiable.</span><span class="sxs-lookup"><span data-stu-id="2c510-108">Specifies that all managed classes and members that are covered by other `EApiCategories` fields be blocked from running in partially trusted code.</span></span>|  
|`eExternalProcessMgmt`|<span data-ttu-id="2c510-109">Spécifie que les classes managées et membres qui permettent la création, la manipulation et la destruction de processus externes doit être bloquée en cours d’exécution dans du code partiellement fiable.</span><span class="sxs-lookup"><span data-stu-id="2c510-109">Specifies that managed classes and members that allow the creation, manipulation, and destruction of external processes be blocked from running in partially trusted code.</span></span>|  
|`eExternalThreading`|<span data-ttu-id="2c510-110">Spécifie que les classes managées et les membres qui permettent la création, la manipulation et la destruction de threads externes doit être bloquée en cours d’exécution dans du code partiellement fiable.</span><span class="sxs-lookup"><span data-stu-id="2c510-110">Specifies that managed classes and members that allow the creation, manipulation, and destruction of external threads be blocked from running in partially trusted code.</span></span>|  
|`eMayLeakOnAbort`|<span data-ttu-id="2c510-111">Spécifie que les types managés et les membres qui pourraient provoquer potentiellement une fuite de mémoire sur abandon doit être bloquée en cours d’exécution dans du code partiellement fiable.</span><span class="sxs-lookup"><span data-stu-id="2c510-111">Specifies that managed types and members that could potentially leak memory on abort be blocked from running in partially trusted code.</span></span>|  
|`eNoCategory`|<span data-ttu-id="2c510-112">Spécifie qu’aucune catégorie de code managé doit être bloquée en cours d’exécution dans du code partiellement fiable.</span><span class="sxs-lookup"><span data-stu-id="2c510-112">Specifies that no managed code categories be blocked from running in partially trusted code.</span></span>|  
|`eSecurityInfrastructure`|<span data-ttu-id="2c510-113">Spécifie que l’infrastructure de sécurité du common language runtime (CLR) doit être bloquée utilisé par du code partiellement fiable.</span><span class="sxs-lookup"><span data-stu-id="2c510-113">Specifies that the common language runtime (CLR) security infrastructure be blocked from being used by partially trusted code.</span></span>|  
|`eSelfAffectingProcessMgmt`|<span data-ttu-id="2c510-114">Spécifie que les classes managées et membres dont les fonctionnalités peuvent affecter le processus hébergé doit être bloquée en cours d’exécution dans du code partiellement fiable.</span><span class="sxs-lookup"><span data-stu-id="2c510-114">Specifies that managed classes and members whose capabilities can affect the hosted process be blocked from running in partially trusted code.</span></span>|  
|`eSelfAffectingThreading`|<span data-ttu-id="2c510-115">Spécifie que les classes managées et les membres dont les fonctionnalités peuvent affecter des threads dans le processus hébergé doit être bloquée en cours d’exécution dans du code partiellement fiable.</span><span class="sxs-lookup"><span data-stu-id="2c510-115">Specifies that managed classes and members whose capabilities can affect threads in the hosted process be blocked from running in partially trusted code.</span></span>|  
|`eSharedState`|<span data-ttu-id="2c510-116">Spécifie que les classes managées et les membres qui exposent l’état partagé doit être bloquée en cours d’exécution dans du code partiellement fiable.</span><span class="sxs-lookup"><span data-stu-id="2c510-116">Specifies that managed classes and members that expose shared state be blocked from running in partially trusted code.</span></span>|  
|`eSynchronization`|<span data-ttu-id="2c510-117">Spécifie que le common language runtime classes et membres qui donner au code utilisateur à maintenir les verrous doit être bloquée à partir de l’exécution dans du code partiellement approuvé.</span><span class="sxs-lookup"><span data-stu-id="2c510-117">Specifies that common language runtime classes and members that allow user code to hold locks be blocked from running in partially trusted code.</span></span>|  
|`eUI`|<span data-ttu-id="2c510-118">Spécifie que les classes managées et les membres qui autorisent ou nécessitent une interaction humaine doit être bloquée en cours d’exécution dans du code partiellement fiable.</span><span class="sxs-lookup"><span data-stu-id="2c510-118">Specifies that managed classes and members that allow or require human interaction be blocked from running in partially trusted code.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="2c510-119">Notes</span><span class="sxs-lookup"><span data-stu-id="2c510-119">Remarks</span></span>  
 <span data-ttu-id="2c510-120">Le [ICLRHostProtectionManager::SetProtectedCategories](../../../../docs/framework/unmanaged-api/hosting/iclrhostprotectionmanager-setprotectedcategories-method.md) méthode prend un paramètre de type `EApiCategories`.</span><span class="sxs-lookup"><span data-stu-id="2c510-120">The [ICLRHostProtectionManager::SetProtectedCategories](../../../../docs/framework/unmanaged-api/hosting/iclrhostprotectionmanager-setprotectedcategories-method.md) method takes a parameter of type `EApiCategories`.</span></span>  
  
 <span data-ttu-id="2c510-121">Le `EApiCategories` énumération et la `SetProtectedCategories` méthode sont directement liés à managé <xref:System.Security.Permissions.HostProtectionAttribute?displayProperty=nameWithType> classe.</span><span class="sxs-lookup"><span data-stu-id="2c510-121">The `EApiCategories` enumeration and the `SetProtectedCategories` method are directly related to the managed <xref:System.Security.Permissions.HostProtectionAttribute?displayProperty=nameWithType> class.</span></span> <span data-ttu-id="2c510-122">La classe managée est utilisée avec le <xref:System.Security.Permissions.HostProtectionResource?displayProperty=nameWithType> énumération, dont les valeurs correspondent directement à la `EApiCategories` pour marquer des types managés et les membres qui exposent des fonctions correspondant aux catégories décrites par les valeurs `EApiCategories`.</span><span class="sxs-lookup"><span data-stu-id="2c510-122">The managed class is used with the <xref:System.Security.Permissions.HostProtectionResource?displayProperty=nameWithType> enumeration, whose values correspond directly to the `EApiCategories` values, to mark managed types and members that expose capabilities corresponding to the categories described by `EApiCategories`.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="2c510-123">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="2c510-123">Requirements</span></span>  
 <span data-ttu-id="2c510-124">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="2c510-124">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="2c510-125">**En-tête :** MSCorEE.h</span><span class="sxs-lookup"><span data-stu-id="2c510-125">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="2c510-126">**Bibliothèque :** MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="2c510-126">**Library:** MSCorEE.dll</span></span>  
  
 <span data-ttu-id="2c510-127">**Versions du .NET Framework :** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="2c510-127">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="2c510-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="2c510-128">See also</span></span>

- [<span data-ttu-id="2c510-129">ICLRHostProtectionManager, interface</span><span class="sxs-lookup"><span data-stu-id="2c510-129">ICLRHostProtectionManager Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/iclrhostprotectionmanager-interface.md)
- [<span data-ttu-id="2c510-130">Énumérations d’hébergement</span><span class="sxs-lookup"><span data-stu-id="2c510-130">Hosting Enumerations</span></span>](../../../../docs/framework/unmanaged-api/hosting/hosting-enumerations.md)
