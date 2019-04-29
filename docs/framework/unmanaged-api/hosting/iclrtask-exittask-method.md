---
title: ICLRTask::ExitTask, méthode
ms.date: 03/30/2017
api_name:
- ICLRTask.ExitTask
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- ICLRTask::ExitTask
helpviewer_keywords:
- ExitTask method [.NET Framework hosting]
- ICLRTask::ExitTask method [.NET Framework hosting]
ms.assetid: 746c85a6-4b33-4f72-a2e9-379fdf2e96af
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 6a55b62c7c71510435b980a4e5938c20628046f4
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61763625"
---
# <a name="iclrtaskexittask-method"></a><span data-ttu-id="48888-102">ICLRTask::ExitTask, méthode</span><span class="sxs-lookup"><span data-stu-id="48888-102">ICLRTask::ExitTask Method</span></span>
<span data-ttu-id="48888-103">Notifie le common language runtime (CLR) que la tâche représentée par l’actuel [ICLRTask](../../../../docs/framework/unmanaged-api/hosting/iclrtask-interface.md) instance se termine et tente d’arrêter correctement.</span><span class="sxs-lookup"><span data-stu-id="48888-103">Notifies the common language runtime (CLR) that the task represented by the current [ICLRTask](../../../../docs/framework/unmanaged-api/hosting/iclrtask-interface.md) instance is ending, and attempts to shut the task down gracefully.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="48888-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="48888-104">Syntax</span></span>  
  
```  
HRESULT ExitTask ();  
```  
  
## <a name="return-value"></a><span data-ttu-id="48888-105">Valeur de retour</span><span class="sxs-lookup"><span data-stu-id="48888-105">Return Value</span></span>  
  
|<span data-ttu-id="48888-106">HRESULT</span><span class="sxs-lookup"><span data-stu-id="48888-106">HRESULT</span></span>|<span data-ttu-id="48888-107">Description</span><span class="sxs-lookup"><span data-stu-id="48888-107">Description</span></span>|  
|-------------|-----------------|  
|<span data-ttu-id="48888-108">S_OK</span><span class="sxs-lookup"><span data-stu-id="48888-108">S_OK</span></span>|<span data-ttu-id="48888-109">`ExitTask` retourné avec succès.</span><span class="sxs-lookup"><span data-stu-id="48888-109">`ExitTask` returned successfully.</span></span>|  
|<span data-ttu-id="48888-110">HOST_E_CLRNOTAVAILABLE</span><span class="sxs-lookup"><span data-stu-id="48888-110">HOST_E_CLRNOTAVAILABLE</span></span>|<span data-ttu-id="48888-111">Le CLR n’a pas été chargé dans un processus ou le CLR est dans un état dans lequel il ne peut pas exécuter le code managé ou traiter l’appel avec succès.</span><span class="sxs-lookup"><span data-stu-id="48888-111">The CLR has not been loaded into a process, or the CLR is in a state in which it cannot run managed code or process the call successfully.</span></span>|  
|<span data-ttu-id="48888-112">HOST_E_TIMEOUT</span><span class="sxs-lookup"><span data-stu-id="48888-112">HOST_E_TIMEOUT</span></span>|<span data-ttu-id="48888-113">L’appel a expiré.</span><span class="sxs-lookup"><span data-stu-id="48888-113">The call timed out.</span></span>|  
|<span data-ttu-id="48888-114">HOST_E_NOT_OWNER</span><span class="sxs-lookup"><span data-stu-id="48888-114">HOST_E_NOT_OWNER</span></span>|<span data-ttu-id="48888-115">L’appelant ne possède pas le verrou.</span><span class="sxs-lookup"><span data-stu-id="48888-115">The caller does not own the lock.</span></span>|  
|<span data-ttu-id="48888-116">HOST_E_ABANDONED</span><span class="sxs-lookup"><span data-stu-id="48888-116">HOST_E_ABANDONED</span></span>|<span data-ttu-id="48888-117">Un événement a été annulé alors qu’un thread bloqué ou Fibre l’attendait.</span><span class="sxs-lookup"><span data-stu-id="48888-117">An event was canceled while a blocked thread or fiber was waiting on it.</span></span>|  
|<span data-ttu-id="48888-118">E_FAIL</span><span class="sxs-lookup"><span data-stu-id="48888-118">E_FAIL</span></span>|<span data-ttu-id="48888-119">Une défaillance catastrophique inconnue s’est produite.</span><span class="sxs-lookup"><span data-stu-id="48888-119">An unknown catastrophic failure occurred.</span></span> <span data-ttu-id="48888-120">Lorsqu’une méthode retourne E_FAIL, le CLR n’est plus utilisable au sein du processus.</span><span class="sxs-lookup"><span data-stu-id="48888-120">When a method returns E_FAIL, the CLR is no longer usable within the process.</span></span> <span data-ttu-id="48888-121">Les appels suivants aux méthodes d’hébergement retournent HOST_E_CLRNOTAVAILABLE.</span><span class="sxs-lookup"><span data-stu-id="48888-121">Subsequent calls to hosting methods return HOST_E_CLRNOTAVAILABLE.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="48888-122">Notes</span><span class="sxs-lookup"><span data-stu-id="48888-122">Remarks</span></span>  
 <span data-ttu-id="48888-123">`ExitTask` tente un arrêt propre d’une tâche, de manière détachement d’un thread à partir d’une bibliothèque de type non managé.</span><span class="sxs-lookup"><span data-stu-id="48888-123">`ExitTask` attempts a clean shutdown of a task, in a manner analogous to detaching a thread from an unmanaged type library.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="48888-124">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="48888-124">Requirements</span></span>  
 <span data-ttu-id="48888-125">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="48888-125">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="48888-126">**En-tête :** MSCorEE.h</span><span class="sxs-lookup"><span data-stu-id="48888-126">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="48888-127">**Bibliothèque :** Inclus en tant que ressource dans MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="48888-127">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="48888-128">**Versions du .NET Framework :** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="48888-128">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="48888-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="48888-129">See also</span></span>

- [<span data-ttu-id="48888-130">ICLRTask, interface</span><span class="sxs-lookup"><span data-stu-id="48888-130">ICLRTask Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/iclrtask-interface.md)
- [<span data-ttu-id="48888-131">ICLRTaskManager, interface</span><span class="sxs-lookup"><span data-stu-id="48888-131">ICLRTaskManager Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/iclrtaskmanager-interface.md)
- [<span data-ttu-id="48888-132">IHostTask, interface</span><span class="sxs-lookup"><span data-stu-id="48888-132">IHostTask Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/ihosttask-interface.md)
- [<span data-ttu-id="48888-133">IHostTaskManager, interface</span><span class="sxs-lookup"><span data-stu-id="48888-133">IHostTaskManager Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/ihosttaskmanager-interface.md)
