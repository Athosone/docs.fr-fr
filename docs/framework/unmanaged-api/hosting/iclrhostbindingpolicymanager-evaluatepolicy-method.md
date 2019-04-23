---
title: ICLRHostBindingPolicyManager::EvaluatePolicy, méthode
ms.date: 03/30/2017
api_name:
- ICLRHostBindingPolicyManager.EvaluatePolicy
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- ICLRHostBindingPolicyManager::EvaluatePolicy
helpviewer_keywords:
- ICLRHostBindingPolicyManager::EvaluatePolicy method [.NET Framework hosting]
- EvaluatePolicy method [.NET Framework hosting]
ms.assetid: 3a3a9446-7a4e-4836-9b27-5c536c15993d
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: ad7856a9376880f867e35f1e63bc2cac1ca216fa
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59130135"
---
# <a name="iclrhostbindingpolicymanagerevaluatepolicy-method"></a><span data-ttu-id="c0c48-102">ICLRHostBindingPolicyManager::EvaluatePolicy, méthode</span><span class="sxs-lookup"><span data-stu-id="c0c48-102">ICLRHostBindingPolicyManager::EvaluatePolicy Method</span></span>
<span data-ttu-id="c0c48-103">Évalue la stratégie de liaison pour le compte de l’hôte.</span><span class="sxs-lookup"><span data-stu-id="c0c48-103">Evaluates binding policy on behalf of the host.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="c0c48-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="c0c48-104">Syntax</span></span>  
  
```  
HRESULT EvaluatePolicy (  
    [in] LPCWSTR     pwzReferenceIdentity,  
    [in] BYTE       *pbApplicationPolicy,  
    [in] DWORD       cbAppPolicySize,  
    [out, size_is(*pcchPostPolicyReferenceIdentity)] LPWSTR pwzPostPolicyReferenceIdentity,  
    [in, out] DWORD *pcchPostPolicyReferenceIdentity,  
    [out] DWORD     *pdwPoliciesApplied  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="c0c48-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="c0c48-105">Parameters</span></span>  
 `pwzReferenceIdentity`  
 <span data-ttu-id="c0c48-106">[in] Une référence à l’assembly avant l’évaluation de stratégie.</span><span class="sxs-lookup"><span data-stu-id="c0c48-106">[in] A reference to the assembly before the policy evaluation.</span></span>  
  
 `pbApplicationPolicy`  
 <span data-ttu-id="c0c48-107">[in] Pointeur vers une mémoire tampon qui contient les données de la stratégie.</span><span class="sxs-lookup"><span data-stu-id="c0c48-107">[in] A pointer to a buffer that contains the policy data.</span></span>  
  
 `cbAppPolicySize`  
 <span data-ttu-id="c0c48-108">[in] La taille de la `pbApplicationPolicy` mémoire tampon.</span><span class="sxs-lookup"><span data-stu-id="c0c48-108">[in] The size of the `pbApplicationPolicy` buffer.</span></span>  
  
 `pwzPostPolicyReferenceIdentity`  
 <span data-ttu-id="c0c48-109">[out] Une référence à l’assembly après l’évaluation des nouvelles données de stratégie.</span><span class="sxs-lookup"><span data-stu-id="c0c48-109">[out] A reference to the assembly after the evaluation of the new policy data.</span></span>  
  
 `pcchPostPolicyReferenceIdentity`  
 <span data-ttu-id="c0c48-110">[in, out] Un pointeur vers la taille du tampon de référence d’identité assembly après l’évaluation des nouvelles données de stratégie.</span><span class="sxs-lookup"><span data-stu-id="c0c48-110">[in, out] A pointer to the size of the assembly identity reference buffer after the evaluation of the new policy data.</span></span>  
  
 `pdwPoliciesApplied`  
 <span data-ttu-id="c0c48-111">[out] Un pointeur vers une combinaison OR logique de [EBindPolicyLevels](../../../../docs/framework/unmanaged-api/hosting/ebindpolicylevels-enumeration.md) valeurs indiquant quelles stratégies ont été appliquées.</span><span class="sxs-lookup"><span data-stu-id="c0c48-111">[out] A pointer to a logical OR combination of [EBindPolicyLevels](../../../../docs/framework/unmanaged-api/hosting/ebindpolicylevels-enumeration.md) values, indicating which policies have been applied.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="c0c48-112">Valeur de retour</span><span class="sxs-lookup"><span data-stu-id="c0c48-112">Return Value</span></span>  
  
|<span data-ttu-id="c0c48-113">HRESULT</span><span class="sxs-lookup"><span data-stu-id="c0c48-113">HRESULT</span></span>|<span data-ttu-id="c0c48-114">Description</span><span class="sxs-lookup"><span data-stu-id="c0c48-114">Description</span></span>|  
|-------------|-----------------|  
|<span data-ttu-id="c0c48-115">S_OK</span><span class="sxs-lookup"><span data-stu-id="c0c48-115">S_OK</span></span>|<span data-ttu-id="c0c48-116">L’évaluation s’est terminée correctement.</span><span class="sxs-lookup"><span data-stu-id="c0c48-116">The evaluation completed successfully.</span></span>|  
|<span data-ttu-id="c0c48-117">E_INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="c0c48-117">E_INVALIDARG</span></span>|<span data-ttu-id="c0c48-118">Soit `pwzReferenceIdentity` ou `pbApplicationPolicy` est une référence null.</span><span class="sxs-lookup"><span data-stu-id="c0c48-118">Either `pwzReferenceIdentity` or `pbApplicationPolicy` is a null reference.</span></span>|  
|<span data-ttu-id="c0c48-119">ERROR_INSUFFICIENT_BUFFER</span><span class="sxs-lookup"><span data-stu-id="c0c48-119">ERROR_INSUFFICIENT_BUFFER</span></span>|<span data-ttu-id="c0c48-120">`cbAppPolicySize` est trop petit.</span><span class="sxs-lookup"><span data-stu-id="c0c48-120">`cbAppPolicySize` is too small.</span></span>|  
|<span data-ttu-id="c0c48-121">HOST_E_CLRNOTAVAILABLE</span><span class="sxs-lookup"><span data-stu-id="c0c48-121">HOST_E_CLRNOTAVAILABLE</span></span>|<span data-ttu-id="c0c48-122">Le common language runtime (CLR) n’a pas été chargé dans un processus ou le CLR est dans un état dans lequel il ne peut pas exécuter le code managé ou traiter l’appel avec succès.</span><span class="sxs-lookup"><span data-stu-id="c0c48-122">The common language runtime (CLR) has not been loaded into a process, or the CLR is in a state in which it cannot run managed code or process the call successfully.</span></span>|  
|<span data-ttu-id="c0c48-123">HOST_E_TIMEOUT</span><span class="sxs-lookup"><span data-stu-id="c0c48-123">HOST_E_TIMEOUT</span></span>|<span data-ttu-id="c0c48-124">L’appel a expiré.</span><span class="sxs-lookup"><span data-stu-id="c0c48-124">The call timed out.</span></span>|  
|<span data-ttu-id="c0c48-125">HOST_E_NOT_OWNER</span><span class="sxs-lookup"><span data-stu-id="c0c48-125">HOST_E_NOT_OWNER</span></span>|<span data-ttu-id="c0c48-126">L’appelant ne possède pas le verrou.</span><span class="sxs-lookup"><span data-stu-id="c0c48-126">The caller does not own the lock.</span></span>|  
|<span data-ttu-id="c0c48-127">HOST_E_ABANDONED</span><span class="sxs-lookup"><span data-stu-id="c0c48-127">HOST_E_ABANDONED</span></span>|<span data-ttu-id="c0c48-128">Un événement a été annulé alors qu’un thread bloqué ou Fibre l’attendait.</span><span class="sxs-lookup"><span data-stu-id="c0c48-128">An event was canceled while a blocked thread or fiber was waiting on it.</span></span>|  
|<span data-ttu-id="c0c48-129">E_FAIL</span><span class="sxs-lookup"><span data-stu-id="c0c48-129">E_FAIL</span></span>|<span data-ttu-id="c0c48-130">Une défaillance catastrophique inconnue s’est produite.</span><span class="sxs-lookup"><span data-stu-id="c0c48-130">An unknown catastrophic failure occurred.</span></span> <span data-ttu-id="c0c48-131">Une fois une méthode retourne E_FAIL, le CLR n’est plus utilisable au sein du processus.</span><span class="sxs-lookup"><span data-stu-id="c0c48-131">After a method returns E_FAIL, the CLR is no longer usable within the process.</span></span> <span data-ttu-id="c0c48-132">Les appels suivants aux méthodes d’hébergement retournent HOST_E_CLRNOTAVAILABLE.</span><span class="sxs-lookup"><span data-stu-id="c0c48-132">Subsequent calls to hosting methods return HOST_E_CLRNOTAVAILABLE.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="c0c48-133">Notes</span><span class="sxs-lookup"><span data-stu-id="c0c48-133">Remarks</span></span>  
 <span data-ttu-id="c0c48-134">Le `EvaluatePolicy` méthode permet à l’hôte d’influencer la stratégie de liaison pour maintenir les assembly spécifique à l’hôte les exigences de contrôle de version.</span><span class="sxs-lookup"><span data-stu-id="c0c48-134">The `EvaluatePolicy` method allows the host to influence binding policy to maintain host-specific assembly versioning requirements.</span></span> <span data-ttu-id="c0c48-135">Le moteur de stratégie reste à l’intérieur du CLR.</span><span class="sxs-lookup"><span data-stu-id="c0c48-135">The policy engine itself remains inside the CLR.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="c0c48-136">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="c0c48-136">Requirements</span></span>  
 <span data-ttu-id="c0c48-137">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="c0c48-137">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="c0c48-138">**En-tête :** MSCorEE.h</span><span class="sxs-lookup"><span data-stu-id="c0c48-138">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="c0c48-139">**Bibliothèque :** Inclus en tant que ressource dans MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="c0c48-139">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="c0c48-140">**Versions du .NET Framework :** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="c0c48-140">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="c0c48-141">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c0c48-141">See also</span></span>

- [<span data-ttu-id="c0c48-142">ICLRHostBindingPolicyManager, interface</span><span class="sxs-lookup"><span data-stu-id="c0c48-142">ICLRHostBindingPolicyManager Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/iclrhostbindingpolicymanager-interface.md)
