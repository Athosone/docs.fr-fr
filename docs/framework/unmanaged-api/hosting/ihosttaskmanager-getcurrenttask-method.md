---
title: IHostTaskManager::GetCurrentTask, méthode
ms.date: 03/30/2017
api_name:
- IHostTaskManager.GetCurrentTask
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IHostTaskManager::GetCurrentTask
helpviewer_keywords:
- GetCurrentTask method, IHostTaskManager interface [.NET Framework hosting]
- IHostTaskManager::GetCurrentTask method [.NET Framework hosting]
ms.assetid: f17bca49-90bd-4dee-a5e1-b9a57ea46f85
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 2436288e2f2f241cab15b16abf4df99c73caec25
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59093720"
---
# <a name="ihosttaskmanagergetcurrenttask-method"></a><span data-ttu-id="19b1a-102">IHostTaskManager::GetCurrentTask, méthode</span><span class="sxs-lookup"><span data-stu-id="19b1a-102">IHostTaskManager::GetCurrentTask Method</span></span>
<span data-ttu-id="19b1a-103">Obtient un pointeur d’interface à la tâche en cours d’exécution sur le thread de système d’exploitation à partir de laquelle cet appel est effectué.</span><span class="sxs-lookup"><span data-stu-id="19b1a-103">Gets an interface pointer to the task that is currently executing on the operating system thread from which this call is made.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="19b1a-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="19b1a-104">Syntax</span></span>  
  
```  
HRESULT GetCurrentTask (  
    [out] IHostTask **pTask  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="19b1a-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="19b1a-105">Parameters</span></span>  
 `pTask`  
 <span data-ttu-id="19b1a-106">[out] Un pointeur vers l’adresse d’un [IHostTask](../../../../docs/framework/unmanaged-api/hosting/ihosttask-interface.md) instance qui représente la tâche en cours d’exécution, ou null, si aucune tâche n’est en cours d’exécution.</span><span class="sxs-lookup"><span data-stu-id="19b1a-106">[out] A pointer to the address of an [IHostTask](../../../../docs/framework/unmanaged-api/hosting/ihosttask-interface.md) instance that represents the currently executing task, or null, if no task is currently executing.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="19b1a-107">Valeur de retour</span><span class="sxs-lookup"><span data-stu-id="19b1a-107">Return Value</span></span>  
  
|<span data-ttu-id="19b1a-108">HRESULT</span><span class="sxs-lookup"><span data-stu-id="19b1a-108">HRESULT</span></span>|<span data-ttu-id="19b1a-109">Description</span><span class="sxs-lookup"><span data-stu-id="19b1a-109">Description</span></span>|  
|-------------|-----------------|  
|<span data-ttu-id="19b1a-110">S_OK</span><span class="sxs-lookup"><span data-stu-id="19b1a-110">S_OK</span></span>|<span data-ttu-id="19b1a-111">`GetCurrentTask` retourné avec succès.</span><span class="sxs-lookup"><span data-stu-id="19b1a-111">`GetCurrentTask` returned successfully.</span></span>|  
|<span data-ttu-id="19b1a-112">HOST_E_CLRNOTAVAILABLE</span><span class="sxs-lookup"><span data-stu-id="19b1a-112">HOST_E_CLRNOTAVAILABLE</span></span>|<span data-ttu-id="19b1a-113">Le common language runtime (CLR) n’a pas été chargé dans un processus ou le CLR est dans un état dans lequel il ne peut pas exécuter le code managé ou traiter l’appel avec succès.</span><span class="sxs-lookup"><span data-stu-id="19b1a-113">The common language runtime (CLR) has not been loaded into a process, or the CLR is in a state in which it cannot run managed code or process the call successfully.</span></span>|  
|<span data-ttu-id="19b1a-114">HOST_E_TIMEOUT</span><span class="sxs-lookup"><span data-stu-id="19b1a-114">HOST_E_TIMEOUT</span></span>|<span data-ttu-id="19b1a-115">L’appel a expiré.</span><span class="sxs-lookup"><span data-stu-id="19b1a-115">The call timed out.</span></span>|  
|<span data-ttu-id="19b1a-116">HOST_E_NOT_OWNER</span><span class="sxs-lookup"><span data-stu-id="19b1a-116">HOST_E_NOT_OWNER</span></span>|<span data-ttu-id="19b1a-117">L’appelant ne possède pas le verrou.</span><span class="sxs-lookup"><span data-stu-id="19b1a-117">The caller does not own the lock.</span></span>|  
|<span data-ttu-id="19b1a-118">HOST_E_ABANDONED</span><span class="sxs-lookup"><span data-stu-id="19b1a-118">HOST_E_ABANDONED</span></span>|<span data-ttu-id="19b1a-119">Un événement a été annulé alors qu’un thread bloqué ou Fibre l’attendait.</span><span class="sxs-lookup"><span data-stu-id="19b1a-119">An event was canceled while a blocked thread or fiber was waiting on it.</span></span>|  
|<span data-ttu-id="19b1a-120">E_FAIL</span><span class="sxs-lookup"><span data-stu-id="19b1a-120">E_FAIL</span></span>|<span data-ttu-id="19b1a-121">Une défaillance catastrophique inconnue s’est produite.</span><span class="sxs-lookup"><span data-stu-id="19b1a-121">An unknown catastrophic failure occurred.</span></span> <span data-ttu-id="19b1a-122">Lorsqu’une méthode retourne E_FAIL, le CLR n’est plus utilisable au sein du processus.</span><span class="sxs-lookup"><span data-stu-id="19b1a-122">When a method returns E_FAIL, the CLR is no longer usable within the process.</span></span> <span data-ttu-id="19b1a-123">Les appels suivants aux méthodes d’hébergement retournent HOST_E_CLRNOTAVAILABLE.</span><span class="sxs-lookup"><span data-stu-id="19b1a-123">Subsequent calls to hosting methods return HOST_E_CLRNOTAVAILABLE.</span></span>|  
|<span data-ttu-id="19b1a-124">HOST_E_INVALIDOPERATION</span><span class="sxs-lookup"><span data-stu-id="19b1a-124">HOST_E_INVALIDOPERATION</span></span>|<span data-ttu-id="19b1a-125">`GetCurrentTask` a été appelé sur un thread de système d’exploitation en dehors du contrôle de l’hôte.</span><span class="sxs-lookup"><span data-stu-id="19b1a-125">`GetCurrentTask` was called on an operating system thread outside the control of the host.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="19b1a-126">Notes</span><span class="sxs-lookup"><span data-stu-id="19b1a-126">Remarks</span></span>  
 <span data-ttu-id="19b1a-127">L’hôte peut également affecter la `pTask` paramètre null pour empêcher une tâche qu’il n’a pas été lancé à partir de l’entrer dans le CLR.</span><span class="sxs-lookup"><span data-stu-id="19b1a-127">The host can also set the `pTask` parameter to null to prevent a task that it did not initiate from entering the CLR.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="19b1a-128">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="19b1a-128">Requirements</span></span>  
 <span data-ttu-id="19b1a-129">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="19b1a-129">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="19b1a-130">**En-tête :** MSCorEE.h</span><span class="sxs-lookup"><span data-stu-id="19b1a-130">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="19b1a-131">**Bibliothèque :** Inclus en tant que ressource dans MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="19b1a-131">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="19b1a-132">**Versions du .NET Framework :** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="19b1a-132">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="19b1a-133">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="19b1a-133">See also</span></span>

- [<span data-ttu-id="19b1a-134">ICLRTask, interface</span><span class="sxs-lookup"><span data-stu-id="19b1a-134">ICLRTask Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/iclrtask-interface.md)
- [<span data-ttu-id="19b1a-135">ICLRTaskManager, interface</span><span class="sxs-lookup"><span data-stu-id="19b1a-135">ICLRTaskManager Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/iclrtaskmanager-interface.md)
- [<span data-ttu-id="19b1a-136">IHostTask, interface</span><span class="sxs-lookup"><span data-stu-id="19b1a-136">IHostTask Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/ihosttask-interface.md)
- [<span data-ttu-id="19b1a-137">IHostTaskManager, interface</span><span class="sxs-lookup"><span data-stu-id="19b1a-137">IHostTaskManager Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/ihosttaskmanager-interface.md)
