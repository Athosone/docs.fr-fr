---
title: ICLRAssemblyIdentityManager::GetBindingIdentityFromFile, méthode
ms.date: 03/30/2017
api_name:
- ICLRAssemblyIdentityManager.GetBindingIdentityFromFile
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- ICLRAssemblyIdentityManager::GetBindingIdentityFromFile
helpviewer_keywords:
- GetBindingIdentityFromFile method [.NET Framework hosting]
- ICLRAssemblyIdentityManager::GetBindingIdentifyFromFile method [.NET Framework hosting]
ms.assetid: 7797562d-7b4c-4bd9-8b93-f35e0e2869e4
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: a3d5e53dd0845fbd01dbd9d20ce8feef12748c04
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59213921"
---
# <a name="iclrassemblyidentitymanagergetbindingidentityfromfile-method"></a><span data-ttu-id="f60d4-102">ICLRAssemblyIdentityManager::GetBindingIdentityFromFile, méthode</span><span class="sxs-lookup"><span data-stu-id="f60d4-102">ICLRAssemblyIdentityManager::GetBindingIdentityFromFile Method</span></span>
<span data-ttu-id="f60d4-103">Obtient l’identité d’assembly une liaison de données pour l’assembly dans le chemin d’accès de fichier spécifié.</span><span class="sxs-lookup"><span data-stu-id="f60d4-103">Gets the assembly identity binding data for the assembly at the specified file path.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="f60d4-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="f60d4-104">Syntax</span></span>  
  
```  
HRESULT GetBindingIdentityFromFile(  
    [in] LPCWSTR     pwzFilePath,  
    [in] DWORD       dwFlags,  
    [out, size_is(*pcchBufferSize)] LPWSTR pwzBuffer,  
    [in, out] DWORD *pcchBufferSize  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="f60d4-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="f60d4-105">Parameters</span></span>  
 `pwzFilePath`  
 <span data-ttu-id="f60d4-106">[in] Le chemin d’accès au fichier à évaluer.</span><span class="sxs-lookup"><span data-stu-id="f60d4-106">[in] The path to the file to be evaluated.</span></span>  
  
 `dwFlags`  
 <span data-ttu-id="f60d4-107">[in] Une valeur de la [ECLRAssemblyIdentityFlags](../../../../docs/framework/unmanaged-api/hosting/eclrassemblyidentityflags-enumeration.md) énumération qui indique le type d’identité d’un assembly.</span><span class="sxs-lookup"><span data-stu-id="f60d4-107">[in] A value of the [ECLRAssemblyIdentityFlags](../../../../docs/framework/unmanaged-api/hosting/eclrassemblyidentityflags-enumeration.md) enumeration that indicates an assembly's identity type.</span></span> <span data-ttu-id="f60d4-108">Fourni pour des extensibilités futures.</span><span class="sxs-lookup"><span data-stu-id="f60d4-108">Provided for future extensibility.</span></span> <span data-ttu-id="f60d4-109">CLR_ASSEMBLY_IDENTITY_FLAGS_DEFAULT est la seule valeur qui prend en charge par le common language runtime (CLR) version 2.0.</span><span class="sxs-lookup"><span data-stu-id="f60d4-109">CLR_ASSEMBLY_IDENTITY_FLAGS_DEFAULT is the only value that the common language runtime (CLR) version 2.0 supports.</span></span>  
  
 `pwzBuffer`  
 <span data-ttu-id="f60d4-110">[out] Une mémoire tampon contenant les données d’identité assembly opaque.</span><span class="sxs-lookup"><span data-stu-id="f60d4-110">[out] A buffer containing the opaque assembly identity data.</span></span>  
  
 `pcchBufferSize`  
 <span data-ttu-id="f60d4-111">[in, out] Un pointeur vers la taille de `pwzBuffer`.</span><span class="sxs-lookup"><span data-stu-id="f60d4-111">[in, out] A pointer to the size of `pwzBuffer`.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="f60d4-112">Valeur de retour</span><span class="sxs-lookup"><span data-stu-id="f60d4-112">Return Value</span></span>  
  
|<span data-ttu-id="f60d4-113">HRESULT</span><span class="sxs-lookup"><span data-stu-id="f60d4-113">HRESULT</span></span>|<span data-ttu-id="f60d4-114">Description</span><span class="sxs-lookup"><span data-stu-id="f60d4-114">Description</span></span>|  
|-------------|-----------------|  
|<span data-ttu-id="f60d4-115">S_OK</span><span class="sxs-lookup"><span data-stu-id="f60d4-115">S_OK</span></span>|<span data-ttu-id="f60d4-116">La méthode a été retourné avec succès.</span><span class="sxs-lookup"><span data-stu-id="f60d4-116">The method returned successfully.</span></span>|  
|<span data-ttu-id="f60d4-117">E_INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="f60d4-117">E_INVALIDARG</span></span>|<span data-ttu-id="f60d4-118">Fourni `pwzFilePath` a la valeur null.</span><span class="sxs-lookup"><span data-stu-id="f60d4-118">The supplied `pwzFilePath` is null.</span></span>|  
|<span data-ttu-id="f60d4-119">ERROR_INSUFFICIENT_BUFFER</span><span class="sxs-lookup"><span data-stu-id="f60d4-119">ERROR_INSUFFICIENT_BUFFER</span></span>|<span data-ttu-id="f60d4-120">La taille de `pwzBuffer` est trop petite.</span><span class="sxs-lookup"><span data-stu-id="f60d4-120">The size of `pwzBuffer` is too small.</span></span>|  
|<span data-ttu-id="f60d4-121">HOST_E_CLRNOTAVAILABLE</span><span class="sxs-lookup"><span data-stu-id="f60d4-121">HOST_E_CLRNOTAVAILABLE</span></span>|<span data-ttu-id="f60d4-122">Le CLR n’a pas été chargé dans un processus ou le CLR est dans un état dans lequel il ne peut pas exécuter le code managé ou traiter l’appel avec succès.</span><span class="sxs-lookup"><span data-stu-id="f60d4-122">The CLR has not been loaded into a process, or the CLR is in a state in which it cannot run managed code or process the call successfully.</span></span>|  
|<span data-ttu-id="f60d4-123">HOST_E_TIMEOUT</span><span class="sxs-lookup"><span data-stu-id="f60d4-123">HOST_E_TIMEOUT</span></span>|<span data-ttu-id="f60d4-124">L’appel a expiré.</span><span class="sxs-lookup"><span data-stu-id="f60d4-124">The call timed out.</span></span>|  
|<span data-ttu-id="f60d4-125">HOST_E_NOT_OWNER</span><span class="sxs-lookup"><span data-stu-id="f60d4-125">HOST_E_NOT_OWNER</span></span>|<span data-ttu-id="f60d4-126">L’appelant ne possède pas le verrou.</span><span class="sxs-lookup"><span data-stu-id="f60d4-126">The caller does not own the lock.</span></span>|  
|<span data-ttu-id="f60d4-127">HOST_E_ABANDONED</span><span class="sxs-lookup"><span data-stu-id="f60d4-127">HOST_E_ABANDONED</span></span>|<span data-ttu-id="f60d4-128">Un événement a été annulé alors qu’un thread bloqué ou Fibre l’attendait.</span><span class="sxs-lookup"><span data-stu-id="f60d4-128">An event was canceled while a blocked thread or fiber was waiting on it.</span></span>|  
|<span data-ttu-id="f60d4-129">E_FAIL</span><span class="sxs-lookup"><span data-stu-id="f60d4-129">E_FAIL</span></span>|<span data-ttu-id="f60d4-130">Une défaillance catastrophique inconnue s’est produite.</span><span class="sxs-lookup"><span data-stu-id="f60d4-130">An unknown catastrophic failure occurred.</span></span> <span data-ttu-id="f60d4-131">Si une méthode retourne E_FAIL, le CLR n’est plus utilisable au sein du processus.</span><span class="sxs-lookup"><span data-stu-id="f60d4-131">If a method returns E_FAIL, the CLR is no longer usable within the process.</span></span> <span data-ttu-id="f60d4-132">Les appels suivants aux méthodes d’hébergement retournent HOST_E_CLRNOTAVAILABLE.</span><span class="sxs-lookup"><span data-stu-id="f60d4-132">Subsequent calls to hosting methods return HOST_E_CLRNOTAVAILABLE.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="f60d4-133">Notes</span><span class="sxs-lookup"><span data-stu-id="f60d4-133">Remarks</span></span>  
 <span data-ttu-id="f60d4-134">`GetBindingIdentityFromFile` est généralement appelée deux fois.</span><span class="sxs-lookup"><span data-stu-id="f60d4-134">`GetBindingIdentityFromFile` is typically called twice.</span></span> <span data-ttu-id="f60d4-135">Le premier appel fournit une valeur null pour `pwzBuffer`, et la méthode retourne la taille appropriée dans `pcchBufferSize`.</span><span class="sxs-lookup"><span data-stu-id="f60d4-135">The first call supplies a null value for `pwzBuffer`, and the method returns the appropriate size in `pcchBufferSize`.</span></span> <span data-ttu-id="f60d4-136">Le deuxième appel fournit une mémoire tampon allouée de manière appropriée, et la méthode est retournée avec les données de la mémoire tampon à l’achèvement.</span><span class="sxs-lookup"><span data-stu-id="f60d4-136">The second call supplies an appropriately allocated buffer, and the method returns with the actual buffer data upon completion.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="f60d4-137">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="f60d4-137">Requirements</span></span>  
 <span data-ttu-id="f60d4-138">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="f60d4-138">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="f60d4-139">**En-tête :** MSCorEE.h</span><span class="sxs-lookup"><span data-stu-id="f60d4-139">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="f60d4-140">**Bibliothèque :** Inclus en tant que ressource dans MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="f60d4-140">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="f60d4-141">**Versions du .NET Framework :** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="f60d4-141">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="f60d4-142">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f60d4-142">See also</span></span>

- [<span data-ttu-id="f60d4-143">ICLRAssemblyIdentityManager, interface</span><span class="sxs-lookup"><span data-stu-id="f60d4-143">ICLRAssemblyIdentityManager Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/iclrassemblyidentitymanager-interface.md)
- [<span data-ttu-id="f60d4-144">ICLRAssemblyReferenceList, interface</span><span class="sxs-lookup"><span data-stu-id="f60d4-144">ICLRAssemblyReferenceList Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/iclrassemblyreferencelist-interface.md)
- [<span data-ttu-id="f60d4-145">ICLRHostBindingPolicyManager, interface</span><span class="sxs-lookup"><span data-stu-id="f60d4-145">ICLRHostBindingPolicyManager Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/iclrhostbindingpolicymanager-interface.md)
