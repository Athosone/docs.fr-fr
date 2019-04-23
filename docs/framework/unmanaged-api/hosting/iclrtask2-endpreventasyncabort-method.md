---
title: ICLRTask2::EndPreventAsyncAbort, méthode
ms.date: 03/30/2017
api_name:
- ICLRTask2.EndPreventAsyncAbort
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- ICLRTask2::EndPreventAsyncAbort
helpviewer_keywords:
- EndPreventAsyncAbort method [.NET Framework hosting]
- ICLRTask2::EndPreventAsyncAbort method [.NET Framework hosting]
ms.assetid: d8013659-e3df-44b3-814f-a6b534ce62f8
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 60997717baf70e10366e7f0ba6a06daa1f35f8cd
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59121665"
---
# <a name="iclrtask2endpreventasyncabort-method"></a><span data-ttu-id="dccd1-102">ICLRTask2::EndPreventAsyncAbort, méthode</span><span class="sxs-lookup"><span data-stu-id="dccd1-102">ICLRTask2::EndPreventAsyncAbort Method</span></span>
<span data-ttu-id="dccd1-103">Permet à nouveau ou en attente de demandes d’abandon de thread pour le thread sur abandonnée sur le thread actuel.</span><span class="sxs-lookup"><span data-stu-id="dccd1-103">Allows new or pending thread abort requests to result in thread aborts on the current thread.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="dccd1-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="dccd1-104">Syntax</span></span>  
  
```  
HRESULT EndPreventAsyncAbort();  
```  
  
## <a name="return-value"></a><span data-ttu-id="dccd1-105">Valeur de retour</span><span class="sxs-lookup"><span data-stu-id="dccd1-105">Return Value</span></span>  
 <span data-ttu-id="dccd1-106">Cette méthode retourne les HRESULT spécifiques suivants ainsi que les erreurs HRESULT indiquant l'échec de la méthode.</span><span class="sxs-lookup"><span data-stu-id="dccd1-106">This method returns the following specific HRESULTs as well as HRESULT errors that indicate method failure.</span></span>  
  
|<span data-ttu-id="dccd1-107">HRESULT</span><span class="sxs-lookup"><span data-stu-id="dccd1-107">HRESULT</span></span>|<span data-ttu-id="dccd1-108">Description</span><span class="sxs-lookup"><span data-stu-id="dccd1-108">Description</span></span>|  
|-------------|-----------------|  
|<span data-ttu-id="dccd1-109">S_OK</span><span class="sxs-lookup"><span data-stu-id="dccd1-109">S_OK</span></span>|<span data-ttu-id="dccd1-110">La commande s'est correctement terminée.</span><span class="sxs-lookup"><span data-stu-id="dccd1-110">The method completed successfully.</span></span>|  
|<span data-ttu-id="dccd1-111">HOST_E_INVALIDOPERATION</span><span class="sxs-lookup"><span data-stu-id="dccd1-111">HOST_E_INVALIDOPERATION</span></span>|<span data-ttu-id="dccd1-112">La méthode a été appelée sur un thread qui n’est pas le thread actuel.</span><span class="sxs-lookup"><span data-stu-id="dccd1-112">The method was called on a thread which is not the current thread.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="dccd1-113">Notes</span><span class="sxs-lookup"><span data-stu-id="dccd1-113">Remarks</span></span>  
 <span data-ttu-id="dccd1-114">Appel de ce compteur décrémente l’abandon de thread de délai de méthode pour le thread actuel d’une unité.</span><span class="sxs-lookup"><span data-stu-id="dccd1-114">Calling this method decrements the delay-thread-abort counter for the current thread by one.</span></span>  
  
 <span data-ttu-id="dccd1-115">Les appels à [ICLRTask2::BeginPreventAsyncAbort](../../../../docs/framework/unmanaged-api/hosting/iclrtask2-beginpreventasyncabort-method.md) et `EndPreventAsyncAbort` peuvent être imbriqués.</span><span class="sxs-lookup"><span data-stu-id="dccd1-115">Calls to [ICLRTask2::BeginPreventAsyncAbort](../../../../docs/framework/unmanaged-api/hosting/iclrtask2-beginpreventasyncabort-method.md) and `EndPreventAsyncAbort` can be nested.</span></span> <span data-ttu-id="dccd1-116">Tant que le compteur est supérieur à zéro, pour le thread actuel abandons de thread.</span><span class="sxs-lookup"><span data-stu-id="dccd1-116">As long as the counter is greater than zero, thread aborts for the current thread are delayed.</span></span>  
  
 <span data-ttu-id="dccd1-117">La fonctionnalité exposée par cette fonctionnalité est utilisée en interne par la machine virtuelle (VM).</span><span class="sxs-lookup"><span data-stu-id="dccd1-117">The functionality that is exposed by this feature is used internally by the virtual machine (VM).</span></span> <span data-ttu-id="dccd1-118">Une mauvaise utilisation de ces méthodes peut-être provoquer un comportement non spécifié dans la machine virtuelle.</span><span class="sxs-lookup"><span data-stu-id="dccd1-118">Misuse of these methods may cause unspecified behavior in the VM.</span></span> <span data-ttu-id="dccd1-119">Par exemple, l’appel `EndPreventAsyncAbort` sans appeler d’abord `BeginPreventAsyncAbort` Impossible de définir le compteur à zéro lors de la machine virtuelle a précédemment incrémenté.</span><span class="sxs-lookup"><span data-stu-id="dccd1-119">For example, calling `EndPreventAsyncAbort` without first calling `BeginPreventAsyncAbort` could set the counter to zero when the VM has previously incremented it.</span></span> <span data-ttu-id="dccd1-120">De même, le compteur interne n’est pas vérifié pour dépassement de capacité.</span><span class="sxs-lookup"><span data-stu-id="dccd1-120">Similarly, the internal counter is not checked for overflow.</span></span> <span data-ttu-id="dccd1-121">S’il dépasse sa limite intégrale, car il est incrémenté par l’hôte et la machine virtuelle, le comportement résultant n’est pas spécifié.</span><span class="sxs-lookup"><span data-stu-id="dccd1-121">If it exceeds its integral limit because it is incremented by both the host and the VM, the resulting behavior is unspecified.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="dccd1-122">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="dccd1-122">Requirements</span></span>  
 <span data-ttu-id="dccd1-123">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="dccd1-123">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="dccd1-124">**En-tête :** MSCorEE.h</span><span class="sxs-lookup"><span data-stu-id="dccd1-124">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="dccd1-125">**Bibliothèque :** Inclus en tant que ressource dans MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="dccd1-125">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="dccd1-126">**Versions du .NET Framework :** [!INCLUDE[net_current_v40plus](../../../../includes/net-current-v40plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="dccd1-126">**.NET Framework Versions:** [!INCLUDE[net_current_v40plus](../../../../includes/net-current-v40plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="dccd1-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="dccd1-127">See also</span></span>

- [<span data-ttu-id="dccd1-128">BeginPreventAsyncAbort, méthode</span><span class="sxs-lookup"><span data-stu-id="dccd1-128">BeginPreventAsyncAbort Method</span></span>](../../../../docs/framework/unmanaged-api/hosting/iclrtask2-beginpreventasyncabort-method.md)
- [<span data-ttu-id="dccd1-129">ICLRTask2, interface</span><span class="sxs-lookup"><span data-stu-id="dccd1-129">ICLRTask2 Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/iclrtask2-interface.md)
- [<span data-ttu-id="dccd1-130">ICLRTaskManager, interface</span><span class="sxs-lookup"><span data-stu-id="dccd1-130">ICLRTaskManager Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/iclrtaskmanager-interface.md)
- [<span data-ttu-id="dccd1-131">IHostTask, interface</span><span class="sxs-lookup"><span data-stu-id="dccd1-131">IHostTask Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/ihosttask-interface.md)
- [<span data-ttu-id="dccd1-132">IHostTaskManager, interface</span><span class="sxs-lookup"><span data-stu-id="dccd1-132">IHostTaskManager Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/ihosttaskmanager-interface.md)
- [<span data-ttu-id="dccd1-133">Interfaces d’hébergement</span><span class="sxs-lookup"><span data-stu-id="dccd1-133">Hosting Interfaces</span></span>](../../../../docs/framework/unmanaged-api/hosting/hosting-interfaces.md)
