---
title: ICLRPolicyManager::SetActionOnTimeout, méthode
ms.date: 03/30/2017
api_name:
- ICLRPolicyManager.SetActionOnTimeout
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- ICLRPolicyManager::SetActionOnTimeout
helpviewer_keywords:
- SetActionOnTimeout method [.NET Framework hosting]
- ICLRPolicyManager::SetActionOnTimeout method [.NET Framework hosting]
ms.assetid: 38439fa1-2b99-4fa8-a6ec-08afc0f83b9c
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 30ab869ed6b06f5c9e53d819e20d3307ccc0e8f1
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61638994"
---
# <a name="iclrpolicymanagersetactionontimeout-method"></a><span data-ttu-id="80b32-102">ICLRPolicyManager::SetActionOnTimeout, méthode</span><span class="sxs-lookup"><span data-stu-id="80b32-102">ICLRPolicyManager::SetActionOnTimeout Method</span></span>
<span data-ttu-id="80b32-103">Spécifie l’action de stratégie que le common language runtime (CLR) doit prendre lorsque l’opération spécifiée a expiré.</span><span class="sxs-lookup"><span data-stu-id="80b32-103">Specifies the policy action the common language runtime (CLR) should take when the specified operation times out.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="80b32-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="80b32-104">Syntax</span></span>  
  
```  
HRESULT SetActionOnTimeout (  
    [in] EClrOperation operation,  
    [in] EPolicyAction action  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="80b32-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="80b32-105">Parameters</span></span>  
 `operation`  
 <span data-ttu-id="80b32-106">[in] Parmi les [EClrOperation](../../../../docs/framework/unmanaged-api/hosting/eclroperation-enumeration.md) valeurs, indiquant que l’opération pour laquelle spécifier l’action de délai d’attente.</span><span class="sxs-lookup"><span data-stu-id="80b32-106">[in] One of the [EClrOperation](../../../../docs/framework/unmanaged-api/hosting/eclroperation-enumeration.md) values, indicating the operation for which to specify the timeout action.</span></span> <span data-ttu-id="80b32-107">Les valeurs suivantes sont prises en charge :</span><span class="sxs-lookup"><span data-stu-id="80b32-107">The following values are supported:</span></span>  
  
- <span data-ttu-id="80b32-108">OPR_AppDomainUnload</span><span class="sxs-lookup"><span data-stu-id="80b32-108">OPR_AppDomainUnload</span></span>  
  
- <span data-ttu-id="80b32-109">OPR_ProcessExit</span><span class="sxs-lookup"><span data-stu-id="80b32-109">OPR_ProcessExit</span></span>  
  
- <span data-ttu-id="80b32-110">OPR_ThreadRudeAbortInCriticalRegion</span><span class="sxs-lookup"><span data-stu-id="80b32-110">OPR_ThreadRudeAbortInCriticalRegion</span></span>  
  
- <span data-ttu-id="80b32-111">OPR_ThreadRudeAbortInNonCriticalRegion</span><span class="sxs-lookup"><span data-stu-id="80b32-111">OPR_ThreadRudeAbortInNonCriticalRegion</span></span>  
  
 `action`  
 <span data-ttu-id="80b32-112">[in] Parmi les [EPolicyAction](../../../../docs/framework/unmanaged-api/hosting/epolicyaction-enumeration.md) valeurs indiquant l’action à entreprendre lorsque l’opération arrive à expiration de stratégie.</span><span class="sxs-lookup"><span data-stu-id="80b32-112">[in] One of the [EPolicyAction](../../../../docs/framework/unmanaged-api/hosting/epolicyaction-enumeration.md) values, indicating the policy action to be taken when the operation times out.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="80b32-113">Valeur de retour</span><span class="sxs-lookup"><span data-stu-id="80b32-113">Return Value</span></span>  
  
|<span data-ttu-id="80b32-114">HRESULT</span><span class="sxs-lookup"><span data-stu-id="80b32-114">HRESULT</span></span>|<span data-ttu-id="80b32-115">Description</span><span class="sxs-lookup"><span data-stu-id="80b32-115">Description</span></span>|  
|-------------|-----------------|  
|<span data-ttu-id="80b32-116">S_OK</span><span class="sxs-lookup"><span data-stu-id="80b32-116">S_OK</span></span>|<span data-ttu-id="80b32-117">`SetActionOnTimeout` retourné avec succès.</span><span class="sxs-lookup"><span data-stu-id="80b32-117">`SetActionOnTimeout` returned successfully.</span></span>|  
|<span data-ttu-id="80b32-118">HOST_E_CLRNOTAVAILABLE</span><span class="sxs-lookup"><span data-stu-id="80b32-118">HOST_E_CLRNOTAVAILABLE</span></span>|<span data-ttu-id="80b32-119">Le CLR n’a pas été chargé dans un processus ou le CLR est dans un état dans lequel il ne peut pas exécuter le code managé ou traiter l’appel avec succès.</span><span class="sxs-lookup"><span data-stu-id="80b32-119">The CLR has not been loaded into a process, or the CLR is in a state in which it cannot run managed code or process the call successfully.</span></span>|  
|<span data-ttu-id="80b32-120">HOST_E_TIMEOUT</span><span class="sxs-lookup"><span data-stu-id="80b32-120">HOST_E_TIMEOUT</span></span>|<span data-ttu-id="80b32-121">L’appel a expiré.</span><span class="sxs-lookup"><span data-stu-id="80b32-121">The call timed out.</span></span>|  
|<span data-ttu-id="80b32-122">HOST_E_NOT_OWNER</span><span class="sxs-lookup"><span data-stu-id="80b32-122">HOST_E_NOT_OWNER</span></span>|<span data-ttu-id="80b32-123">L’appelant ne possède pas le verrou.</span><span class="sxs-lookup"><span data-stu-id="80b32-123">The caller does not own the lock.</span></span>|  
|<span data-ttu-id="80b32-124">HOST_E_ABANDONED</span><span class="sxs-lookup"><span data-stu-id="80b32-124">HOST_E_ABANDONED</span></span>|<span data-ttu-id="80b32-125">Un événement a été annulé alors qu’un thread bloqué ou Fibre l’attendait.</span><span class="sxs-lookup"><span data-stu-id="80b32-125">An event was canceled while a blocked thread or fiber was waiting on it.</span></span>|  
|<span data-ttu-id="80b32-126">E_FAIL</span><span class="sxs-lookup"><span data-stu-id="80b32-126">E_FAIL</span></span>|<span data-ttu-id="80b32-127">Une défaillance catastrophique inconnue s’est produite.</span><span class="sxs-lookup"><span data-stu-id="80b32-127">An unknown catastrophic failure occurred.</span></span> <span data-ttu-id="80b32-128">Une fois une méthode retourne E_FAIL, le CLR n’est plus utilisable au sein du processus.</span><span class="sxs-lookup"><span data-stu-id="80b32-128">After a method returns E_FAIL, the CLR is no longer usable within the process.</span></span> <span data-ttu-id="80b32-129">Les appels suivants aux méthodes d’hébergement retournent HOST_E_CLRNOTAVAILABLE.</span><span class="sxs-lookup"><span data-stu-id="80b32-129">Subsequent calls to hosting methods return HOST_E_CLRNOTAVAILABLE.</span></span>|  
|<span data-ttu-id="80b32-130">E_INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="80b32-130">E_INVALIDARG</span></span>|<span data-ttu-id="80b32-131">Impossible de définir un délai d’expiration spécifié `operation`, ou une valeur non valide a été fournie pour `operation`.</span><span class="sxs-lookup"><span data-stu-id="80b32-131">A timeout cannot be set for the specified `operation`, or an invalid value was supplied for `operation`.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="80b32-132">Notes</span><span class="sxs-lookup"><span data-stu-id="80b32-132">Remarks</span></span>  
 <span data-ttu-id="80b32-133">La valeur de délai d’attente peut être soit le délai d’expiration par défaut défini par le CLR, soit une valeur spécifiée par l’hôte dans un appel à la [ICLRPolicyManager::SetTimeout](../../../../docs/framework/unmanaged-api/hosting/iclrpolicymanager-settimeout-method.md) (méthode).</span><span class="sxs-lookup"><span data-stu-id="80b32-133">The timeout value can be either the default timeout set by the CLR, or a value specified by the host in a call to the [ICLRPolicyManager::SetTimeout](../../../../docs/framework/unmanaged-api/hosting/iclrpolicymanager-settimeout-method.md) method.</span></span>  
  
 <span data-ttu-id="80b32-134">Toutes les valeurs d’action de stratégie peuvent être spécifiés en tant que le comportement de délai d’expiration pour les opérations CLR.</span><span class="sxs-lookup"><span data-stu-id="80b32-134">Not all policy action values can be specified as the timeout behavior for CLR operations.</span></span> <span data-ttu-id="80b32-135">`SetActionOnTimeout` est généralement utilisé uniquement pour transmettre le comportement.</span><span class="sxs-lookup"><span data-stu-id="80b32-135">`SetActionOnTimeout` is typically used only to escalate behavior.</span></span> <span data-ttu-id="80b32-136">Par exemple, un hôte peut spécifier que les abandons de thread soit transformé en brutal abandons de thread, mais ne pouvez pas spécifier le contraire.</span><span class="sxs-lookup"><span data-stu-id="80b32-136">For example, a host can specify that thread aborts be turned into rude thread aborts, but cannot specify the opposite.</span></span> <span data-ttu-id="80b32-137">Le tableau ci-dessous décrit le valide `action` des valeurs valides `operation` valeurs.</span><span class="sxs-lookup"><span data-stu-id="80b32-137">The table below describes the valid `action` values for valid `operation` values.</span></span>  
  
|<span data-ttu-id="80b32-138">Valeur pour `operation`</span><span class="sxs-lookup"><span data-stu-id="80b32-138">Value for `operation`</span></span>|<span data-ttu-id="80b32-139">Valeurs valides pour `action`</span><span class="sxs-lookup"><span data-stu-id="80b32-139">Valid values for `action`</span></span>|  
|---------------------------|-------------------------------|  
|<span data-ttu-id="80b32-140">OPR_ThreadRudeAbortInNonCriticalRegion</span><span class="sxs-lookup"><span data-stu-id="80b32-140">OPR_ThreadRudeAbortInNonCriticalRegion</span></span><br /><br /> <span data-ttu-id="80b32-141">OPR_ThreadRudeAbortInCriticalRegion</span><span class="sxs-lookup"><span data-stu-id="80b32-141">OPR_ThreadRudeAbortInCriticalRegion</span></span>|<span data-ttu-id="80b32-142">-   eRudeAbortThread</span><span class="sxs-lookup"><span data-stu-id="80b32-142">-   eRudeAbortThread</span></span><br /><span data-ttu-id="80b32-143">-   eUnloadAppDomain</span><span class="sxs-lookup"><span data-stu-id="80b32-143">-   eUnloadAppDomain</span></span><br /><span data-ttu-id="80b32-144">-   eRudeUnloadAppDomain</span><span class="sxs-lookup"><span data-stu-id="80b32-144">-   eRudeUnloadAppDomain</span></span><br /><span data-ttu-id="80b32-145">-   eExitProcess</span><span class="sxs-lookup"><span data-stu-id="80b32-145">-   eExitProcess</span></span><br /><span data-ttu-id="80b32-146">-   eFastExitProcess</span><span class="sxs-lookup"><span data-stu-id="80b32-146">-   eFastExitProcess</span></span><br /><span data-ttu-id="80b32-147">-   eRudeExitProcess</span><span class="sxs-lookup"><span data-stu-id="80b32-147">-   eRudeExitProcess</span></span><br /><span data-ttu-id="80b32-148">-   eDisableRuntime</span><span class="sxs-lookup"><span data-stu-id="80b32-148">-   eDisableRuntime</span></span>|  
|<span data-ttu-id="80b32-149">OPR_AppDomainUnload</span><span class="sxs-lookup"><span data-stu-id="80b32-149">OPR_AppDomainUnload</span></span>|<span data-ttu-id="80b32-150">-   eUnloadAppDomain</span><span class="sxs-lookup"><span data-stu-id="80b32-150">-   eUnloadAppDomain</span></span><br /><span data-ttu-id="80b32-151">-   eRudeUnloadAppDomain</span><span class="sxs-lookup"><span data-stu-id="80b32-151">-   eRudeUnloadAppDomain</span></span><br /><span data-ttu-id="80b32-152">-   eExitProcess</span><span class="sxs-lookup"><span data-stu-id="80b32-152">-   eExitProcess</span></span><br /><span data-ttu-id="80b32-153">-   eFastExitProcess</span><span class="sxs-lookup"><span data-stu-id="80b32-153">-   eFastExitProcess</span></span><br /><span data-ttu-id="80b32-154">-   eRudeExitProcess</span><span class="sxs-lookup"><span data-stu-id="80b32-154">-   eRudeExitProcess</span></span><br /><span data-ttu-id="80b32-155">-   eDisableRuntime</span><span class="sxs-lookup"><span data-stu-id="80b32-155">-   eDisableRuntime</span></span>|  
|<span data-ttu-id="80b32-156">OPR_ProcessExit</span><span class="sxs-lookup"><span data-stu-id="80b32-156">OPR_ProcessExit</span></span>|<span data-ttu-id="80b32-157">-   eExitProcess</span><span class="sxs-lookup"><span data-stu-id="80b32-157">-   eExitProcess</span></span><br /><span data-ttu-id="80b32-158">-   eFastExitProcess</span><span class="sxs-lookup"><span data-stu-id="80b32-158">-   eFastExitProcess</span></span><br /><span data-ttu-id="80b32-159">-   eRudeExitProcess</span><span class="sxs-lookup"><span data-stu-id="80b32-159">-   eRudeExitProcess</span></span><br /><span data-ttu-id="80b32-160">-   eDisableRuntime</span><span class="sxs-lookup"><span data-stu-id="80b32-160">-   eDisableRuntime</span></span>|  
  
## <a name="requirements"></a><span data-ttu-id="80b32-161">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="80b32-161">Requirements</span></span>  
 <span data-ttu-id="80b32-162">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="80b32-162">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="80b32-163">**En-tête :** MSCorEE.h</span><span class="sxs-lookup"><span data-stu-id="80b32-163">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="80b32-164">**Bibliothèque :** Inclus en tant que ressource dans MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="80b32-164">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="80b32-165">**Versions du .NET Framework :** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="80b32-165">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="80b32-166">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="80b32-166">See also</span></span>

- [<span data-ttu-id="80b32-167">EClrOperation, énumération</span><span class="sxs-lookup"><span data-stu-id="80b32-167">EClrOperation Enumeration</span></span>](../../../../docs/framework/unmanaged-api/hosting/eclroperation-enumeration.md)
- [<span data-ttu-id="80b32-168">EPolicyAction, énumération</span><span class="sxs-lookup"><span data-stu-id="80b32-168">EPolicyAction Enumeration</span></span>](../../../../docs/framework/unmanaged-api/hosting/epolicyaction-enumeration.md)
- [<span data-ttu-id="80b32-169">ICLRControl, interface</span><span class="sxs-lookup"><span data-stu-id="80b32-169">ICLRControl Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/iclrcontrol-interface.md)
- [<span data-ttu-id="80b32-170">ICLRPolicyManager, interface</span><span class="sxs-lookup"><span data-stu-id="80b32-170">ICLRPolicyManager Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/iclrpolicymanager-interface.md)
