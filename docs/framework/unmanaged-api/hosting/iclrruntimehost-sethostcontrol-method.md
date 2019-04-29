---
title: ICLRRuntimeHost::SetHostControl, méthode
ms.date: 03/30/2017
api_name:
- ICLRRuntimeHost.SetHostControl
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- ICLRRuntimeHost::SetHostControl
helpviewer_keywords:
- SetHostControl method [.NET Framework hosting]
- ICLRRuntimeHost::SetHostControl method [.NET Framework hosting]
ms.assetid: 6136be87-e631-4756-81ed-74b66581bad4
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 6817a2154e876dfa83540e3496f42acdcdb25a83
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61771811"
---
# <a name="iclrruntimehostsethostcontrol-method"></a><span data-ttu-id="0c797-102">ICLRRuntimeHost::SetHostControl, méthode</span><span class="sxs-lookup"><span data-stu-id="0c797-102">ICLRRuntimeHost::SetHostControl Method</span></span>
<span data-ttu-id="0c797-103">Définit le pointeur d’interface que le common language runtime (CLR) peut utiliser pour obtenir l’implémentation de l’hôte de [IHostControl, Interface](../../../../docs/framework/unmanaged-api/hosting/ihostcontrol-interface.md).</span><span class="sxs-lookup"><span data-stu-id="0c797-103">Sets the interface pointer that the common language runtime (CLR) can use to get the host's implementation of [IHostControl Interface](../../../../docs/framework/unmanaged-api/hosting/ihostcontrol-interface.md).</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="0c797-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="0c797-104">Syntax</span></span>  
  
```  
HRESULT SetHostControl(  
    [in] IHostControl* pHostControl  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="0c797-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="0c797-105">Parameters</span></span>  
 `pHostControl`  
 <span data-ttu-id="0c797-106">[in] Pointeur d’interface vers l’implémentation de l’hôte de [IHostControl, Interface](../../../../docs/framework/unmanaged-api/hosting/ihostcontrol-interface.md).</span><span class="sxs-lookup"><span data-stu-id="0c797-106">[in] An interface pointer to the host's implementation of [IHostControl Interface](../../../../docs/framework/unmanaged-api/hosting/ihostcontrol-interface.md).</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="0c797-107">Valeur de retour</span><span class="sxs-lookup"><span data-stu-id="0c797-107">Return Value</span></span>  
  
|<span data-ttu-id="0c797-108">HRESULT</span><span class="sxs-lookup"><span data-stu-id="0c797-108">HRESULT</span></span>|<span data-ttu-id="0c797-109">Description</span><span class="sxs-lookup"><span data-stu-id="0c797-109">Description</span></span>|  
|-------------|-----------------|  
|<span data-ttu-id="0c797-110">S_OK</span><span class="sxs-lookup"><span data-stu-id="0c797-110">S_OK</span></span>|<span data-ttu-id="0c797-111">`SetHostControl` retourné avec succès.</span><span class="sxs-lookup"><span data-stu-id="0c797-111">`SetHostControl` returned successfully.</span></span>|  
|<span data-ttu-id="0c797-112">HOST_E_CLRNOTAVAILABLE</span><span class="sxs-lookup"><span data-stu-id="0c797-112">HOST_E_CLRNOTAVAILABLE</span></span>|<span data-ttu-id="0c797-113">Le CLR n’a pas été chargé dans un processus ou le CLR est dans un état dans lequel il ne peut pas exécuter le code managé ou traiter l’appel avec succès.</span><span class="sxs-lookup"><span data-stu-id="0c797-113">The CLR has not been loaded into a process, or the CLR is in a state in which it cannot run managed code or process the call successfully.</span></span>|  
|<span data-ttu-id="0c797-114">HOST_E_TIMEOUT</span><span class="sxs-lookup"><span data-stu-id="0c797-114">HOST_E_TIMEOUT</span></span>|<span data-ttu-id="0c797-115">L’appel a expiré.</span><span class="sxs-lookup"><span data-stu-id="0c797-115">The call timed out.</span></span>|  
|<span data-ttu-id="0c797-116">HOST_E_NOT_OWNER</span><span class="sxs-lookup"><span data-stu-id="0c797-116">HOST_E_NOT_OWNER</span></span>|<span data-ttu-id="0c797-117">L’appelant ne possède pas le verrou.</span><span class="sxs-lookup"><span data-stu-id="0c797-117">The caller does not own the lock.</span></span>|  
|<span data-ttu-id="0c797-118">HOST_E_ABANDONED</span><span class="sxs-lookup"><span data-stu-id="0c797-118">HOST_E_ABANDONED</span></span>|<span data-ttu-id="0c797-119">Un événement a été annulé alors qu’un thread bloqué ou Fibre l’attendait.</span><span class="sxs-lookup"><span data-stu-id="0c797-119">An event was canceled while a blocked thread or fiber was waiting on it.</span></span>|  
|<span data-ttu-id="0c797-120">E_FAIL</span><span class="sxs-lookup"><span data-stu-id="0c797-120">E_FAIL</span></span>|<span data-ttu-id="0c797-121">Une défaillance catastrophique inconnue s’est produite.</span><span class="sxs-lookup"><span data-stu-id="0c797-121">An unknown catastrophic failure occurred.</span></span> <span data-ttu-id="0c797-122">Si une méthode retourne E_FAIL, le CLR n’est plus utilisable au sein du processus.</span><span class="sxs-lookup"><span data-stu-id="0c797-122">If a method returns E_FAIL, the CLR is no longer usable within the process.</span></span> <span data-ttu-id="0c797-123">Les appels suivants aux méthodes d’hébergement retournent HOST_E_CLRNOTAVAILABLE.</span><span class="sxs-lookup"><span data-stu-id="0c797-123">Subsequent calls to hosting methods return HOST_E_CLRNOTAVAILABLE.</span></span>|  
|<span data-ttu-id="0c797-124">E_CLR_ALREADY_STARTED</span><span class="sxs-lookup"><span data-stu-id="0c797-124">E_CLR_ALREADY_STARTED</span></span>|<span data-ttu-id="0c797-125">Le CLR a déjà été initialisé.</span><span class="sxs-lookup"><span data-stu-id="0c797-125">The CLR has already been initialized.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="0c797-126">Notes</span><span class="sxs-lookup"><span data-stu-id="0c797-126">Remarks</span></span>  
 <span data-ttu-id="0c797-127">Vous devez appeler `SetHostControl` avant que le CLR est initialisé, autrement dit, avant d’appeler [méthode Start](../../../../docs/framework/unmanaged-api/hosting/iclrruntimehost-start-method.md) ou utiliser une de la [Interfaces de métadonnées](../../../../docs/framework/unmanaged-api/metadata/metadata-interfaces.md).</span><span class="sxs-lookup"><span data-stu-id="0c797-127">You must call `SetHostControl` before the CLR is initialized, that is, before you call [Start Method](../../../../docs/framework/unmanaged-api/hosting/iclrruntimehost-start-method.md) or use any of the [Metadata Interfaces](../../../../docs/framework/unmanaged-api/metadata/metadata-interfaces.md).</span></span> <span data-ttu-id="0c797-128">Il est recommandé d’appeler `SetHostControl` immédiatement après l’appel [CorBindToCurrentRuntime, fonction](../../../../docs/framework/unmanaged-api/hosting/corbindtocurrentruntime-function.md) ou [fonction CorBindToRuntimeEx](../../../../docs/framework/unmanaged-api/hosting/corbindtoruntimeex-function.md).</span><span class="sxs-lookup"><span data-stu-id="0c797-128">It is recommended that you call `SetHostControl` immediately after calling [CorBindToCurrentRuntime Function](../../../../docs/framework/unmanaged-api/hosting/corbindtocurrentruntime-function.md) or [CorBindToRuntimeEx Function](../../../../docs/framework/unmanaged-api/hosting/corbindtoruntimeex-function.md).</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="0c797-129">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="0c797-129">Requirements</span></span>  
 <span data-ttu-id="0c797-130">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="0c797-130">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="0c797-131">**En-tête :** MSCorEE.h</span><span class="sxs-lookup"><span data-stu-id="0c797-131">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="0c797-132">**Bibliothèque :** Inclus en tant que ressource dans MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="0c797-132">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="0c797-133">**Versions du .NET Framework :** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="0c797-133">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="0c797-134">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0c797-134">See also</span></span>

- [<span data-ttu-id="0c797-135">ICLRRuntimeHost, interface</span><span class="sxs-lookup"><span data-stu-id="0c797-135">ICLRRuntimeHost Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/iclrruntimehost-interface.md)
- [<span data-ttu-id="0c797-136">IHostControl, interface</span><span class="sxs-lookup"><span data-stu-id="0c797-136">IHostControl Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/ihostcontrol-interface.md)
