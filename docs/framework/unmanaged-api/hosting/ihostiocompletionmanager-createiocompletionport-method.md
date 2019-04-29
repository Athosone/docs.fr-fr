---
title: IHostIoCompletionManager::CreateIoCompletionPort, méthode
ms.date: 03/30/2017
api_name:
- IHostIoCompletionManager.CreateIoCompletionPort
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IHostIoCompletionManager::CreateIoCompletionPort
helpviewer_keywords:
- IHostIoCompletionManager::CreateIoCompletionPort method [.NET Framework hosting]
- CreateIoCompletionPort method [.NET Framework hosting]
ms.assetid: 907a2b43-68db-44a7-acac-89e792e7bb3c
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 8cf7978af4081b84a361e0a96a6c9da7180cb217
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61951721"
---
# <a name="ihostiocompletionmanagercreateiocompletionport-method"></a><span data-ttu-id="6f64b-102">IHostIoCompletionManager::CreateIoCompletionPort, méthode</span><span class="sxs-lookup"><span data-stu-id="6f64b-102">IHostIoCompletionManager::CreateIoCompletionPort Method</span></span>
<span data-ttu-id="6f64b-103">Demande que l’hôte crée un nouveau port de terminaison d’e/s.</span><span class="sxs-lookup"><span data-stu-id="6f64b-103">Requests that the host create a new I/O completion port.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="6f64b-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="6f64b-104">Syntax</span></span>  
  
```  
HRESULT CreateIoCompletionPort (  
    [out] HANDLE *phPort  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="6f64b-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="6f64b-105">Parameters</span></span>  
 `phPort`  
 <span data-ttu-id="6f64b-106">[out] Pointeur vers un handle vers le port de terminaison d’e/s qui vient d’être créé, ou 0 (zéro), si le port n’a pas pu être créé.</span><span class="sxs-lookup"><span data-stu-id="6f64b-106">[out] A pointer to a handle to the newly created I/O completion port, or 0 (zero), if the port could not be created.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="6f64b-107">Valeur de retour</span><span class="sxs-lookup"><span data-stu-id="6f64b-107">Return Value</span></span>  
  
|<span data-ttu-id="6f64b-108">HRESULT</span><span class="sxs-lookup"><span data-stu-id="6f64b-108">HRESULT</span></span>|<span data-ttu-id="6f64b-109">Description</span><span class="sxs-lookup"><span data-stu-id="6f64b-109">Description</span></span>|  
|-------------|-----------------|  
|<span data-ttu-id="6f64b-110">S_OK</span><span class="sxs-lookup"><span data-stu-id="6f64b-110">S_OK</span></span>|<span data-ttu-id="6f64b-111">`CreateIoCompletionPort` retourné avec succès.</span><span class="sxs-lookup"><span data-stu-id="6f64b-111">`CreateIoCompletionPort` returned successfully.</span></span>|  
|<span data-ttu-id="6f64b-112">HOST_E_CLRNOTAVAILABLE</span><span class="sxs-lookup"><span data-stu-id="6f64b-112">HOST_E_CLRNOTAVAILABLE</span></span>|<span data-ttu-id="6f64b-113">Le common language runtime (CLR) n’a pas été chargé dans un processus ou le CLR est dans un état dans lequel il ne peut pas exécuter le code managé ou traiter l’appel avec succès.</span><span class="sxs-lookup"><span data-stu-id="6f64b-113">The common language runtime (CLR) has not been loaded into a process, or the CLR is in a state in which it cannot run managed code or process the call successfully.</span></span>|  
|<span data-ttu-id="6f64b-114">HOST_E_TIMEOUT</span><span class="sxs-lookup"><span data-stu-id="6f64b-114">HOST_E_TIMEOUT</span></span>|<span data-ttu-id="6f64b-115">L’appel a expiré.</span><span class="sxs-lookup"><span data-stu-id="6f64b-115">The call timed out.</span></span>|  
|<span data-ttu-id="6f64b-116">HOST_E_NOT_OWNER</span><span class="sxs-lookup"><span data-stu-id="6f64b-116">HOST_E_NOT_OWNER</span></span>|<span data-ttu-id="6f64b-117">L’appelant ne possède pas le verrou.</span><span class="sxs-lookup"><span data-stu-id="6f64b-117">The caller does not own the lock.</span></span>|  
|<span data-ttu-id="6f64b-118">HOST_E_ABANDONED</span><span class="sxs-lookup"><span data-stu-id="6f64b-118">HOST_E_ABANDONED</span></span>|<span data-ttu-id="6f64b-119">Un événement a été annulé alors qu’un thread bloqué ou Fibre l’attendait.</span><span class="sxs-lookup"><span data-stu-id="6f64b-119">An event was canceled while a blocked thread or fiber was waiting on it.</span></span>|  
|<span data-ttu-id="6f64b-120">E_FAIL</span><span class="sxs-lookup"><span data-stu-id="6f64b-120">E_FAIL</span></span>|<span data-ttu-id="6f64b-121">Une défaillance catastrophique inconnue s’est produite.</span><span class="sxs-lookup"><span data-stu-id="6f64b-121">An unknown catastrophic failure occurred.</span></span> <span data-ttu-id="6f64b-122">Lorsqu’une méthode retourne E_FAIL, le CLR n’est plus utilisable au sein du processus.</span><span class="sxs-lookup"><span data-stu-id="6f64b-122">When a method returns E_FAIL, the CLR is no longer usable within the process.</span></span> <span data-ttu-id="6f64b-123">Les appels suivants aux méthodes d’hébergement retournent HOST_E_CLRNOTAVAILABLE.</span><span class="sxs-lookup"><span data-stu-id="6f64b-123">Subsequent calls to hosting methods return HOST_E_CLRNOTAVAILABLE.</span></span>|  
|<span data-ttu-id="6f64b-124">E_OUTOFMEMORY</span><span class="sxs-lookup"><span data-stu-id="6f64b-124">E_OUTOFMEMORY</span></span>|<span data-ttu-id="6f64b-125">Mémoire était insuffisante pour allouer la ressource demandée.</span><span class="sxs-lookup"><span data-stu-id="6f64b-125">Not enough memory was available to allocate the requested resource.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="6f64b-126">Notes</span><span class="sxs-lookup"><span data-stu-id="6f64b-126">Remarks</span></span>  
 <span data-ttu-id="6f64b-127">Le CLR appelle le `CreateIoCompletionPort` méthode pour demander que l’hôte crée un nouveau port de terminaison d’e/s.</span><span class="sxs-lookup"><span data-stu-id="6f64b-127">The CLR calls the `CreateIoCompletionPort` method to request that the host create a new I/O completion port.</span></span> <span data-ttu-id="6f64b-128">Il lie des opérations d’e/s à ce port via un appel à la [IHostIoCompletionManager::Bind](../../../../docs/framework/unmanaged-api/hosting/ihostiocompletionmanager-bind-method.md) (méthode).</span><span class="sxs-lookup"><span data-stu-id="6f64b-128">It binds I/O operations to this port through a call to the [IHostIoCompletionManager::Bind](../../../../docs/framework/unmanaged-api/hosting/ihostiocompletionmanager-bind-method.md) method.</span></span> <span data-ttu-id="6f64b-129">L’hôte signale l’état au CLR en appelant [ICLRIoCompletionManager::OnComplete](../../../../docs/framework/unmanaged-api/hosting/iclriocompletionmanager-oncomplete-method.md).</span><span class="sxs-lookup"><span data-stu-id="6f64b-129">The host reports status back to the CLR by calling [ICLRIoCompletionManager::OnComplete](../../../../docs/framework/unmanaged-api/hosting/iclriocompletionmanager-oncomplete-method.md).</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="6f64b-130">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="6f64b-130">Requirements</span></span>  
 <span data-ttu-id="6f64b-131">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="6f64b-131">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="6f64b-132">**En-tête :** MSCorEE.h</span><span class="sxs-lookup"><span data-stu-id="6f64b-132">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="6f64b-133">**Bibliothèque :** Inclus en tant que ressource dans MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="6f64b-133">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="6f64b-134">**Versions du .NET Framework :** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="6f64b-134">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="6f64b-135">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="6f64b-135">See also</span></span>

- [<span data-ttu-id="6f64b-136">ICLRIoCompletionManager, interface</span><span class="sxs-lookup"><span data-stu-id="6f64b-136">ICLRIoCompletionManager Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/iclriocompletionmanager-interface.md)
- [<span data-ttu-id="6f64b-137">IHostIoCompletionManager, interface</span><span class="sxs-lookup"><span data-stu-id="6f64b-137">IHostIoCompletionManager Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/ihostiocompletionmanager-interface.md)
