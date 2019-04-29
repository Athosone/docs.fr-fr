---
title: IHostSecurityManager::SetThreadToken, méthode
ms.date: 03/30/2017
api_name:
- IHostSecurityManager.SetThreadToken
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IHostSecurityManager::SetThreadToken
helpviewer_keywords:
- SetThreadToken method [.NET Framework hosting]
- IHostSecurityManager::SetThreadToken method [.NET Framework hosting]
ms.assetid: e951c345-8a86-4587-911b-a1a57bc6428a
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: c67471c0d88ccffbfe9b7c77809124452ccc2e5b
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61696637"
---
# <a name="ihostsecuritymanagersetthreadtoken-method"></a><span data-ttu-id="bfd17-102">IHostSecurityManager::SetThreadToken, méthode</span><span class="sxs-lookup"><span data-stu-id="bfd17-102">IHostSecurityManager::SetThreadToken Method</span></span>
<span data-ttu-id="bfd17-103">Définit un handle pour le thread en cours d’exécution.</span><span class="sxs-lookup"><span data-stu-id="bfd17-103">Sets a handle for the currently executing thread.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="bfd17-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="bfd17-104">Syntax</span></span>  
  
```  
HRESULT SetThreadToken (  
    [in] HANDLE hToken  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="bfd17-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="bfd17-105">Parameters</span></span>  
 `hToken`  
 <span data-ttu-id="bfd17-106">[in] Handle vers le jeton à définir pour le thread en cours d’exécution.</span><span class="sxs-lookup"><span data-stu-id="bfd17-106">[in] A handle to the token to set for the currently executing thread.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="bfd17-107">Valeur de retour</span><span class="sxs-lookup"><span data-stu-id="bfd17-107">Return Value</span></span>  
  
|<span data-ttu-id="bfd17-108">HRESULT</span><span class="sxs-lookup"><span data-stu-id="bfd17-108">HRESULT</span></span>|<span data-ttu-id="bfd17-109">Description</span><span class="sxs-lookup"><span data-stu-id="bfd17-109">Description</span></span>|  
|-------------|-----------------|  
|<span data-ttu-id="bfd17-110">S_OK</span><span class="sxs-lookup"><span data-stu-id="bfd17-110">S_OK</span></span>|<span data-ttu-id="bfd17-111">`SetThreadToken` retourné avec succès.</span><span class="sxs-lookup"><span data-stu-id="bfd17-111">`SetThreadToken` returned successfully.</span></span>|  
|<span data-ttu-id="bfd17-112">HOST_E_CLRNOTAVAILABLE</span><span class="sxs-lookup"><span data-stu-id="bfd17-112">HOST_E_CLRNOTAVAILABLE</span></span>|<span data-ttu-id="bfd17-113">Le common language runtime (CLR) n’a pas été chargé dans un processus ou le CLR est dans un état dans lequel il ne peut pas exécuter le code managé ou traiter l’appel avec succès.</span><span class="sxs-lookup"><span data-stu-id="bfd17-113">The common language runtime (CLR) has not been loaded into a process, or the CLR is in a state in which it cannot run managed code or process the call successfully.</span></span>|  
|<span data-ttu-id="bfd17-114">HOST_E_TIMEOUT</span><span class="sxs-lookup"><span data-stu-id="bfd17-114">HOST_E_TIMEOUT</span></span>|<span data-ttu-id="bfd17-115">L’appel a expiré.</span><span class="sxs-lookup"><span data-stu-id="bfd17-115">The call timed out.</span></span>|  
|<span data-ttu-id="bfd17-116">HOST_E_NOT_OWNER</span><span class="sxs-lookup"><span data-stu-id="bfd17-116">HOST_E_NOT_OWNER</span></span>|<span data-ttu-id="bfd17-117">L’appelant ne possède pas le verrou.</span><span class="sxs-lookup"><span data-stu-id="bfd17-117">The caller does not own the lock.</span></span>|  
|<span data-ttu-id="bfd17-118">HOST_E_ABANDONED</span><span class="sxs-lookup"><span data-stu-id="bfd17-118">HOST_E_ABANDONED</span></span>|<span data-ttu-id="bfd17-119">Un événement a été annulé alors qu’un thread bloqué ou Fibre l’attendait.</span><span class="sxs-lookup"><span data-stu-id="bfd17-119">An event was canceled while a blocked thread or fiber was waiting on it.</span></span>|  
|<span data-ttu-id="bfd17-120">E_FAIL</span><span class="sxs-lookup"><span data-stu-id="bfd17-120">E_FAIL</span></span>|<span data-ttu-id="bfd17-121">Une défaillance catastrophique inconnue s’est produite.</span><span class="sxs-lookup"><span data-stu-id="bfd17-121">An unknown catastrophic failure occurred.</span></span> <span data-ttu-id="bfd17-122">Lorsqu’une méthode retourne E_FAIL, le CLR n’est plus utilisable au sein du processus.</span><span class="sxs-lookup"><span data-stu-id="bfd17-122">When a method returns E_FAIL, the CLR is no longer usable within the process.</span></span> <span data-ttu-id="bfd17-123">Les appels suivants aux méthodes d’hébergement retournent HOST_E_CLRNOTAVAILABLE.</span><span class="sxs-lookup"><span data-stu-id="bfd17-123">Subsequent calls to hosting methods return HOST_E_CLRNOTAVAILABLE.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="bfd17-124">Notes</span><span class="sxs-lookup"><span data-stu-id="bfd17-124">Remarks</span></span>  
 <span data-ttu-id="bfd17-125">`IHostSecurityManager::SetThreadToken` se comporte de la même façon pour la fonction Win32 correspondante du même nom, sauf que la fonction Win32 permet à l’appelant de passer un handle à un thread arbitraire, tandis que `IHostSecurityManager::SetThreadToken` peut associer un jeton uniquement avec le thread en cours d’exécution.</span><span class="sxs-lookup"><span data-stu-id="bfd17-125">`IHostSecurityManager::SetThreadToken` behaves similarly to the corresponding Win32 function of the same name, except that the Win32 function allows the caller to pass in a handle to an arbitrary thread, while `IHostSecurityManager::SetThreadToken` can associate a token only with the currently executing thread.</span></span>  
  
 <span data-ttu-id="bfd17-126">Le `HANDLE` type n’est pas conforme à COM ; autrement dit, sa taille est spécifique à un système d’exploitation et il requiert le marshaling personnalisé.</span><span class="sxs-lookup"><span data-stu-id="bfd17-126">The `HANDLE` type is not COM-compliant; that is, its size is specific to an operating system and it requires custom marshaling.</span></span> <span data-ttu-id="bfd17-127">Par conséquent, ce jeton est utilisé que dans le processus, entre le CLR et l’hôte.</span><span class="sxs-lookup"><span data-stu-id="bfd17-127">Thus, this token is for use only within the process, between the CLR and the host.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="bfd17-128">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="bfd17-128">Requirements</span></span>  
 <span data-ttu-id="bfd17-129">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="bfd17-129">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="bfd17-130">**En-tête :** MSCorEE.h</span><span class="sxs-lookup"><span data-stu-id="bfd17-130">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="bfd17-131">**Bibliothèque :** Inclus en tant que ressource dans MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="bfd17-131">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="bfd17-132">**Versions du .NET Framework :** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="bfd17-132">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="bfd17-133">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="bfd17-133">See also</span></span>

- [<span data-ttu-id="bfd17-134">IHostSecurityManager, interface</span><span class="sxs-lookup"><span data-stu-id="bfd17-134">IHostSecurityManager Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/ihostsecuritymanager-interface.md)
- [<span data-ttu-id="bfd17-135">IHostThreadPoolManager, interface</span><span class="sxs-lookup"><span data-stu-id="bfd17-135">IHostThreadPoolManager Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/ihostthreadpoolmanager-interface.md)
