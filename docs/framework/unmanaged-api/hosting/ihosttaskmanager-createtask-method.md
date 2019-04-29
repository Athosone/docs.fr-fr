---
title: IHostTaskManager::CreateTask, méthode
ms.date: 03/30/2017
api_name:
- IHostTaskManager.CreateTask
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IHostTaskManager::CreateTask
helpviewer_keywords:
- CreateTask method, IHostTaskManager interface [.NET Framework hosting]
- IHostTaskManager::CreateTask method [.NET Framework hosting]
ms.assetid: a6f8ad36-61e1-42b0-9db2-add575646d18
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 2eddb11ab56bae5243ea7d00614090bbfe774f71
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61789444"
---
# <a name="ihosttaskmanagercreatetask-method"></a><span data-ttu-id="b6f4c-102">IHostTaskManager::CreateTask, méthode</span><span class="sxs-lookup"><span data-stu-id="b6f4c-102">IHostTaskManager::CreateTask Method</span></span>
<span data-ttu-id="b6f4c-103">Demande que l’hôte crée une nouvelle tâche.</span><span class="sxs-lookup"><span data-stu-id="b6f4c-103">Requests that the host create a new task.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="b6f4c-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="b6f4c-104">Syntax</span></span>  
  
```  
HRESULT CreateTask (  
    [in]  DWORD stacksize,   
    [in]  LPTHREAD_START_ROUTINE pStartAddress,  
    [in]  PVOID pParameter,  
    [out] IHostTask **ppTask  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="b6f4c-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="b6f4c-105">Parameters</span></span>  
 `stacksize`  
 <span data-ttu-id="b6f4c-106">[in] La taille demandée, en octets, de la pile demandée, ou 0 (zéro) pour la taille par défaut.</span><span class="sxs-lookup"><span data-stu-id="b6f4c-106">[in] The requested size, in bytes, of the requested stack, or 0 (zero) for the default size.</span></span>  
  
 `pStartAddress`  
 <span data-ttu-id="b6f4c-107">[in] Un pointeur vers la fonction de la tâche consiste à exécuter.</span><span class="sxs-lookup"><span data-stu-id="b6f4c-107">[in] A pointer to the function the task is to execute.</span></span>  
  
 `pParameter`  
 <span data-ttu-id="b6f4c-108">[in] Un pointeur vers les données utilisateur à passer à la fonction, ou null si la fonction ne prend aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="b6f4c-108">[in] A pointer to the user data to be passed to the function, or null if the function takes no parameters.</span></span>  
  
 `ppTask`  
 <span data-ttu-id="b6f4c-109">[out] Un pointeur vers l’adresse d’un [IHostTask](../../../../docs/framework/unmanaged-api/hosting/ihosttask-interface.md) instance créée par l’hôte, ou null si la tâche ne peut pas être créée.</span><span class="sxs-lookup"><span data-stu-id="b6f4c-109">[out] A pointer to the address of an [IHostTask](../../../../docs/framework/unmanaged-api/hosting/ihosttask-interface.md) instance created by the host, or null if the task cannot be created.</span></span> <span data-ttu-id="b6f4c-110">La tâche reste dans un état suspendu jusqu'à ce qu’elle soit démarrée explicitement par un appel à [IHostTask::Start](../../../../docs/framework/unmanaged-api/hosting/ihosttask-start-method.md).</span><span class="sxs-lookup"><span data-stu-id="b6f4c-110">The task remains in a suspended state until it is explicitly started by a call to [IHostTask::Start](../../../../docs/framework/unmanaged-api/hosting/ihosttask-start-method.md).</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="b6f4c-111">Valeur de retour</span><span class="sxs-lookup"><span data-stu-id="b6f4c-111">Return Value</span></span>  
  
|<span data-ttu-id="b6f4c-112">HRESULT</span><span class="sxs-lookup"><span data-stu-id="b6f4c-112">HRESULT</span></span>|<span data-ttu-id="b6f4c-113">Description</span><span class="sxs-lookup"><span data-stu-id="b6f4c-113">Description</span></span>|  
|-------------|-----------------|  
|<span data-ttu-id="b6f4c-114">S_OK</span><span class="sxs-lookup"><span data-stu-id="b6f4c-114">S_OK</span></span>|<span data-ttu-id="b6f4c-115">`CreateTask` retourné avec succès.</span><span class="sxs-lookup"><span data-stu-id="b6f4c-115">`CreateTask` returned successfully.</span></span>|  
|<span data-ttu-id="b6f4c-116">HOST_E_CLRNOTAVAILABLE</span><span class="sxs-lookup"><span data-stu-id="b6f4c-116">HOST_E_CLRNOTAVAILABLE</span></span>|<span data-ttu-id="b6f4c-117">Le common language runtime (CLR) n’a pas été chargé dans un processus ou le CLR est dans un état dans lequel il ne peut pas exécuter le code managé ou traiter l’appel avec succès.</span><span class="sxs-lookup"><span data-stu-id="b6f4c-117">The common language runtime (CLR) has not been loaded into a process, or the CLR is in a state in which it cannot run managed code or process the call successfully.</span></span>|  
|<span data-ttu-id="b6f4c-118">HOST_E_TIMEOUT</span><span class="sxs-lookup"><span data-stu-id="b6f4c-118">HOST_E_TIMEOUT</span></span>|<span data-ttu-id="b6f4c-119">L’appel a expiré.</span><span class="sxs-lookup"><span data-stu-id="b6f4c-119">The call timed out.</span></span>|  
|<span data-ttu-id="b6f4c-120">HOST_E_NOT_OWNER</span><span class="sxs-lookup"><span data-stu-id="b6f4c-120">HOST_E_NOT_OWNER</span></span>|<span data-ttu-id="b6f4c-121">L’appelant ne possède pas le verrou.</span><span class="sxs-lookup"><span data-stu-id="b6f4c-121">The caller does not own the lock.</span></span>|  
|<span data-ttu-id="b6f4c-122">HOST_E_ABANDONED</span><span class="sxs-lookup"><span data-stu-id="b6f4c-122">HOST_E_ABANDONED</span></span>|<span data-ttu-id="b6f4c-123">Un événement a été annulé alors qu’un thread bloqué ou Fibre l’attendait.</span><span class="sxs-lookup"><span data-stu-id="b6f4c-123">An event was canceled while a blocked thread or fiber was waiting on it.</span></span>|  
|<span data-ttu-id="b6f4c-124">E_FAIL</span><span class="sxs-lookup"><span data-stu-id="b6f4c-124">E_FAIL</span></span>|<span data-ttu-id="b6f4c-125">Une défaillance catastrophique inconnue s’est produite.</span><span class="sxs-lookup"><span data-stu-id="b6f4c-125">An unknown catastrophic failure occurred.</span></span> <span data-ttu-id="b6f4c-126">Lorsqu’une méthode retourne E_FAIL, le CLR n’est plus utilisable au sein du processus.</span><span class="sxs-lookup"><span data-stu-id="b6f4c-126">When a method returns E_FAIL, the CLR is no longer usable within the process.</span></span> <span data-ttu-id="b6f4c-127">Les appels suivants aux méthodes d’hébergement retournent HOST_E_CLRNOTAVAILABLE.</span><span class="sxs-lookup"><span data-stu-id="b6f4c-127">Subsequent calls to hosting methods return HOST_E_CLRNOTAVAILABLE.</span></span>|  
|<span data-ttu-id="b6f4c-128">E_OUTOFMEMORY</span><span class="sxs-lookup"><span data-stu-id="b6f4c-128">E_OUTOFMEMORY</span></span>|<span data-ttu-id="b6f4c-129">Pas assez de mémoire n’était disponible pour créer la tâche demandée.</span><span class="sxs-lookup"><span data-stu-id="b6f4c-129">Not enough memory was available to create the requested task.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="b6f4c-130">Notes</span><span class="sxs-lookup"><span data-stu-id="b6f4c-130">Remarks</span></span>  
 <span data-ttu-id="b6f4c-131">Le CLR appelle `CreateTask` pour demander que l’hôte crée une nouvelle tâche.</span><span class="sxs-lookup"><span data-stu-id="b6f4c-131">The CLR calls `CreateTask` to request that the host create a new task.</span></span> <span data-ttu-id="b6f4c-132">L’hôte retourne un pointeur d’interface vers un `IHostTask` instance.</span><span class="sxs-lookup"><span data-stu-id="b6f4c-132">The host returns an interface pointer to an `IHostTask` instance.</span></span> <span data-ttu-id="b6f4c-133">La tâche retournée doit rester suspendue jusqu'à ce qu’elle soit démarrée explicitement par un appel à `IHostTask::Start`.</span><span class="sxs-lookup"><span data-stu-id="b6f4c-133">The returned task must remain suspended until it is explicitly started by a call to `IHostTask::Start`.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="b6f4c-134">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="b6f4c-134">Requirements</span></span>  
 <span data-ttu-id="b6f4c-135">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="b6f4c-135">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="b6f4c-136">**En-tête :** MSCorEE.h</span><span class="sxs-lookup"><span data-stu-id="b6f4c-136">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="b6f4c-137">**Bibliothèque :** Inclus en tant que ressource dans MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="b6f4c-137">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="b6f4c-138">**Versions du .NET Framework :** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="b6f4c-138">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="b6f4c-139">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b6f4c-139">See also</span></span>

- [<span data-ttu-id="b6f4c-140">ICLRTask, interface</span><span class="sxs-lookup"><span data-stu-id="b6f4c-140">ICLRTask Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/iclrtask-interface.md)
- [<span data-ttu-id="b6f4c-141">ICLRTaskManager, interface</span><span class="sxs-lookup"><span data-stu-id="b6f4c-141">ICLRTaskManager Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/iclrtaskmanager-interface.md)
- [<span data-ttu-id="b6f4c-142">IHostTask, interface</span><span class="sxs-lookup"><span data-stu-id="b6f4c-142">IHostTask Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/ihosttask-interface.md)
- [<span data-ttu-id="b6f4c-143">IHostTaskManager, interface</span><span class="sxs-lookup"><span data-stu-id="b6f4c-143">IHostTaskManager Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/ihosttaskmanager-interface.md)
