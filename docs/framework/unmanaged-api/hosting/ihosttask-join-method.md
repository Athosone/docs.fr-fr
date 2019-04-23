---
title: IHostTask::Join, méthode
ms.date: 03/30/2017
api_name:
- IHostTask.Join
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IHostTask::Join
helpviewer_keywords:
- IHostTask::Join method [.NET Framework hosting]
- Join method, IHostTask interface [.NET Framework hosting]
ms.assetid: 2cffcc52-19e0-4ced-a440-fc7375078ac9
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 4373fc4e8a4c414c40e8d3c5547b5998b9300348
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59170757"
---
# <a name="ihosttaskjoin-method"></a><span data-ttu-id="c2085-102">IHostTask::Join, méthode</span><span class="sxs-lookup"><span data-stu-id="c2085-102">IHostTask::Join Method</span></span>
<span data-ttu-id="c2085-103">Bloque la tâche appelante jusqu'à ce que la tâche représentée par le [IHostTask](../../../../docs/framework/unmanaged-api/hosting/ihosttask-interface.md) instance se termine, l’intervalle de temps spécifié écoulé, ou [IHostTask::Alert](../../../../docs/framework/unmanaged-api/hosting/ihosttask-alert-method.md) est appelée.</span><span class="sxs-lookup"><span data-stu-id="c2085-103">Blocks the calling task until the task represented by the current [IHostTask](../../../../docs/framework/unmanaged-api/hosting/ihosttask-interface.md) instance completes, the specified time interval elapses, or [IHostTask::Alert](../../../../docs/framework/unmanaged-api/hosting/ihosttask-alert-method.md) is called.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="c2085-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="c2085-104">Syntax</span></span>  
  
```  
HRESULT Join (  
    [in] DWORD milliseconds,  
    [in] DWORD option  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="c2085-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="c2085-105">Parameters</span></span>  
 `milliseconds`  
 <span data-ttu-id="c2085-106">[in] L’intervalle de temps, en millisecondes, pour attendre la tâche ne se termine.</span><span class="sxs-lookup"><span data-stu-id="c2085-106">[in] The time interval, in milliseconds, to wait for the task to terminate.</span></span> <span data-ttu-id="c2085-107">Si cet intervalle s’écoule avant que la tâche se termine, la tâche appelante se débloque.</span><span class="sxs-lookup"><span data-stu-id="c2085-107">If this interval elapses before the task terminates, the calling task unblocks.</span></span>  
  
 `option`  
 <span data-ttu-id="c2085-108">[in] Parmi les [WAIT_OPTION](../../../../docs/framework/unmanaged-api/hosting/wait-option-enumeration.md) valeurs.</span><span class="sxs-lookup"><span data-stu-id="c2085-108">[in] One of the [WAIT_OPTION](../../../../docs/framework/unmanaged-api/hosting/wait-option-enumeration.md) values.</span></span> <span data-ttu-id="c2085-109">Une valeur WAIT_ALERTABLE indique à réactiver la tâche si l’hôte `Alert` est appelée avant `milliseconds` s’écoule.</span><span class="sxs-lookup"><span data-stu-id="c2085-109">A value of WAIT_ALERTABLE instructs the host to wake the task if `Alert` is called before `milliseconds` elapses.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="c2085-110">Valeur de retour</span><span class="sxs-lookup"><span data-stu-id="c2085-110">Return Value</span></span>  
  
|<span data-ttu-id="c2085-111">HRESULT</span><span class="sxs-lookup"><span data-stu-id="c2085-111">HRESULT</span></span>|<span data-ttu-id="c2085-112">Description</span><span class="sxs-lookup"><span data-stu-id="c2085-112">Description</span></span>|  
|-------------|-----------------|  
|<span data-ttu-id="c2085-113">S_OK</span><span class="sxs-lookup"><span data-stu-id="c2085-113">S_OK</span></span>|<span data-ttu-id="c2085-114">`Join` retourné avec succès.</span><span class="sxs-lookup"><span data-stu-id="c2085-114">`Join` returned successfully.</span></span>|  
|<span data-ttu-id="c2085-115">HOST_E_CLRNOTAVAILABLE</span><span class="sxs-lookup"><span data-stu-id="c2085-115">HOST_E_CLRNOTAVAILABLE</span></span>|<span data-ttu-id="c2085-116">Le common language runtime (CLR) n’a pas été chargé dans un processus ou le CLR est dans un état dans lequel il ne peut pas exécuter le code managé ou traiter l’appel avec succès.</span><span class="sxs-lookup"><span data-stu-id="c2085-116">The common language runtime (CLR) has not been loaded into a process, or the CLR is in a state in which it cannot run managed code or process the call successfully.</span></span>|  
|<span data-ttu-id="c2085-117">HOST_E_TIMEOUT</span><span class="sxs-lookup"><span data-stu-id="c2085-117">HOST_E_TIMEOUT</span></span>|<span data-ttu-id="c2085-118">L’appel a expiré.</span><span class="sxs-lookup"><span data-stu-id="c2085-118">The call timed out.</span></span>|  
|<span data-ttu-id="c2085-119">HOST_E_NOT_OWNER</span><span class="sxs-lookup"><span data-stu-id="c2085-119">HOST_E_NOT_OWNER</span></span>|<span data-ttu-id="c2085-120">L’appelant ne possède pas le verrou.</span><span class="sxs-lookup"><span data-stu-id="c2085-120">The caller does not own the lock.</span></span>|  
|<span data-ttu-id="c2085-121">HOST_E_ABANDONED</span><span class="sxs-lookup"><span data-stu-id="c2085-121">HOST_E_ABANDONED</span></span>|<span data-ttu-id="c2085-122">Un événement a été annulé alors qu’un thread bloqué ou une fibre attendait, ou en cours `IHostTask` instance n’est pas associée à une tâche.</span><span class="sxs-lookup"><span data-stu-id="c2085-122">An event was canceled while a blocked thread or fiber was waiting on it, or the current `IHostTask` instance is not associated with a task.</span></span>|  
|<span data-ttu-id="c2085-123">E_FAIL</span><span class="sxs-lookup"><span data-stu-id="c2085-123">E_FAIL</span></span>|<span data-ttu-id="c2085-124">Une défaillance catastrophique inconnue s’est produite.</span><span class="sxs-lookup"><span data-stu-id="c2085-124">An unknown catastrophic failure occurred.</span></span> <span data-ttu-id="c2085-125">Lorsqu’une méthode retourne E_FAIL, le CLR n’est plus utilisable au sein du processus.</span><span class="sxs-lookup"><span data-stu-id="c2085-125">When a method returns E_FAIL, the CLR is no longer usable within the process.</span></span> <span data-ttu-id="c2085-126">Les appels suivants aux méthodes d’hébergement retournent HOST_E_CLRNOTAVAILABLE.</span><span class="sxs-lookup"><span data-stu-id="c2085-126">Subsequent calls to hosting methods return HOST_E_CLRNOTAVAILABLE.</span></span>|  
  
## <a name="requirements"></a><span data-ttu-id="c2085-127">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="c2085-127">Requirements</span></span>  
 <span data-ttu-id="c2085-128">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="c2085-128">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="c2085-129">**En-tête :** MSCorEE.h</span><span class="sxs-lookup"><span data-stu-id="c2085-129">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="c2085-130">**Bibliothèque :** Inclus en tant que ressource dans MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="c2085-130">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="c2085-131">**Versions du .NET Framework :** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="c2085-131">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="c2085-132">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c2085-132">See also</span></span>

- [<span data-ttu-id="c2085-133">ICLRTask, interface</span><span class="sxs-lookup"><span data-stu-id="c2085-133">ICLRTask Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/iclrtask-interface.md)
- [<span data-ttu-id="c2085-134">ICLRTaskManager, interface</span><span class="sxs-lookup"><span data-stu-id="c2085-134">ICLRTaskManager Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/iclrtaskmanager-interface.md)
- [<span data-ttu-id="c2085-135">IHostTask, interface</span><span class="sxs-lookup"><span data-stu-id="c2085-135">IHostTask Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/ihosttask-interface.md)
- [<span data-ttu-id="c2085-136">IHostTaskManager, interface</span><span class="sxs-lookup"><span data-stu-id="c2085-136">IHostTaskManager Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/ihosttaskmanager-interface.md)
- [<span data-ttu-id="c2085-137">WAIT_OPTION, énumération</span><span class="sxs-lookup"><span data-stu-id="c2085-137">WAIT_OPTION Enumeration</span></span>](../../../../docs/framework/unmanaged-api/hosting/wait-option-enumeration.md)
