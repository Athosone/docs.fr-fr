---
title: ICLRControl::GetCLRManager, méthode
ms.date: 03/30/2017
api_name:
- ICLRControl.GetCLRManager
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- ICLRControl::GetCLRManager
helpviewer_keywords:
- GetCLRManager method [.NET Framework hosting]
- ICLRControl::GetCLRManager method [.NET Framework hosting]
ms.assetid: 8a11bfa4-cbb0-4082-82b5-f9fba66c93f5
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 33c790bf2721f09b263494e845356ef6b6712f99
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59177136"
---
# <a name="iclrcontrolgetclrmanager-method"></a><span data-ttu-id="3977d-102">ICLRControl::GetCLRManager, méthode</span><span class="sxs-lookup"><span data-stu-id="3977d-102">ICLRControl::GetCLRManager Method</span></span>
<span data-ttu-id="3977d-103">Obtient un pointeur d’interface vers une instance d’un des types de gestionnaires que l’hôte peut utiliser pour configurer le common language runtime (CLR).</span><span class="sxs-lookup"><span data-stu-id="3977d-103">Gets an interface pointer to an instance of any of the manager types the host can use to configure the common language runtime (CLR).</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="3977d-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="3977d-104">Syntax</span></span>  
  
```  
HRESULT GetCLRManager (  
    [in]  REFIID  riid,  
    [out] void  **ppObject  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="3977d-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="3977d-105">Parameters</span></span>  
 `riid`  
 <span data-ttu-id="3977d-106">[in] Le `IID` du type de gestionnaire à retourner.</span><span class="sxs-lookup"><span data-stu-id="3977d-106">[in] The `IID` of the manager type to return.</span></span> <span data-ttu-id="3977d-107">Ce qui suit `IID` valeurs sont prises en charge.</span><span class="sxs-lookup"><span data-stu-id="3977d-107">The following `IID` values are supported.</span></span>  
  
-   <span data-ttu-id="3977d-108">IID_ICLRDebugManager: Spécifie que `ppObject` sera de type [ICLRDebugManager](../../../../docs/framework/unmanaged-api/hosting/iclrdebugmanager-interface.md).</span><span class="sxs-lookup"><span data-stu-id="3977d-108">IID_ICLRDebugManager: Specifies that `ppObject` will be of type [ICLRDebugManager](../../../../docs/framework/unmanaged-api/hosting/iclrdebugmanager-interface.md).</span></span>  
  
-   <span data-ttu-id="3977d-109">IID_ICLRErrorReportingManager: Spécifie que `ppObject` sera de type [ICLRErrorReportingManager](../../../../docs/framework/unmanaged-api/hosting/iclrerrorreportingmanager-interface.md).</span><span class="sxs-lookup"><span data-stu-id="3977d-109">IID_ICLRErrorReportingManager: Specifies that `ppObject` will be of type [ICLRErrorReportingManager](../../../../docs/framework/unmanaged-api/hosting/iclrerrorreportingmanager-interface.md).</span></span>  
  
-   <span data-ttu-id="3977d-110">IID_ICLRGCManager : Spécifie que `ppObject` sera de type [ICLRGCManager](../../../../docs/framework/unmanaged-api/hosting/iclrgcmanager-interface.md).</span><span class="sxs-lookup"><span data-stu-id="3977d-110">IID_ICLRGCManager: Specifies that `ppObject` will be of type [ICLRGCManager](../../../../docs/framework/unmanaged-api/hosting/iclrgcmanager-interface.md).</span></span>  
  
-   <span data-ttu-id="3977d-111">IID_ICLRHostProtectionManager: Spécifie que `ppObject` sera de type [ICLRHostProtectionManager](../../../../docs/framework/unmanaged-api/hosting/iclrhostprotectionmanager-interface.md).</span><span class="sxs-lookup"><span data-stu-id="3977d-111">IID_ICLRHostProtectionManager: Specifies that `ppObject` will be of type [ICLRHostProtectionManager](../../../../docs/framework/unmanaged-api/hosting/iclrhostprotectionmanager-interface.md).</span></span>  
  
-   <span data-ttu-id="3977d-112">IID_ICLROnEventManager: Spécifie que `ppObject` sera de type [ICLROnEventManager](../../../../docs/framework/unmanaged-api/hosting/iclroneventmanager-interface.md).</span><span class="sxs-lookup"><span data-stu-id="3977d-112">IID_ICLROnEventManager: Specifies that `ppObject` will be of type [ICLROnEventManager](../../../../docs/framework/unmanaged-api/hosting/iclroneventmanager-interface.md).</span></span>  
  
-   <span data-ttu-id="3977d-113">IID_ICLRPolicyManager: Spécifie que `ppObject` sera de type [ICLRPolicyManager](../../../../docs/framework/unmanaged-api/hosting/iclrpolicymanager-interface.md).</span><span class="sxs-lookup"><span data-stu-id="3977d-113">IID_ICLRPolicyManager: Specifies that `ppObject` will be of type [ICLRPolicyManager](../../../../docs/framework/unmanaged-api/hosting/iclrpolicymanager-interface.md).</span></span>  
  
-   <span data-ttu-id="3977d-114">IID_ICLRTaskManager : Spécifies qui `ppObject` sera de type [ICLRTaskManager](../../../../docs/framework/unmanaged-api/hosting/iclrtaskmanager-interface.md).</span><span class="sxs-lookup"><span data-stu-id="3977d-114">IID_ICLRTaskManager: speciries that `ppObject` will be of type [ICLRTaskManager](../../../../docs/framework/unmanaged-api/hosting/iclrtaskmanager-interface.md).</span></span>  
  
 `ppObject`  
 <span data-ttu-id="3977d-115">[out] Un pointeur d’interface vers le gestionnaire demandé, ou null, si un type de gestionnaire non valide a été demandé.</span><span class="sxs-lookup"><span data-stu-id="3977d-115">[out] An interface pointer to the requested manager, or null, if an invalid manager type was requested.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="3977d-116">Valeur de retour</span><span class="sxs-lookup"><span data-stu-id="3977d-116">Return Value</span></span>  
  
|<span data-ttu-id="3977d-117">HRESULT</span><span class="sxs-lookup"><span data-stu-id="3977d-117">HRESULT</span></span>|<span data-ttu-id="3977d-118">Description</span><span class="sxs-lookup"><span data-stu-id="3977d-118">Description</span></span>|  
|-------------|-----------------|  
|<span data-ttu-id="3977d-119">S_OK</span><span class="sxs-lookup"><span data-stu-id="3977d-119">S_OK</span></span>|<span data-ttu-id="3977d-120">La méthode a été retourné avec succès.</span><span class="sxs-lookup"><span data-stu-id="3977d-120">The method returned successfully.</span></span>|  
|<span data-ttu-id="3977d-121">HOST_E_CLRNOTAVAILABLE</span><span class="sxs-lookup"><span data-stu-id="3977d-121">HOST_E_CLRNOTAVAILABLE</span></span>|<span data-ttu-id="3977d-122">Le CLR n’a pas été chargé dans un processus ou le CLR est dans un état dans lequel il ne peut pas exécuter le code managé ou traiter l’appel avec succès.</span><span class="sxs-lookup"><span data-stu-id="3977d-122">The CLR has not been loaded into a process, or the CLR is in a state in which it cannot run managed code or process the call successfully.</span></span>|  
|<span data-ttu-id="3977d-123">HOST_E_TIMEOUT</span><span class="sxs-lookup"><span data-stu-id="3977d-123">HOST_E_TIMEOUT</span></span>|<span data-ttu-id="3977d-124">L’appel a expiré.</span><span class="sxs-lookup"><span data-stu-id="3977d-124">The call timed out.</span></span>|  
|<span data-ttu-id="3977d-125">HOST_E_NOT_OWNER</span><span class="sxs-lookup"><span data-stu-id="3977d-125">HOST_E_NOT_OWNER</span></span>|<span data-ttu-id="3977d-126">L’appelant ne possède pas le verrou.</span><span class="sxs-lookup"><span data-stu-id="3977d-126">The caller does not own the lock.</span></span>|  
|<span data-ttu-id="3977d-127">HOST_E_ABANDONED</span><span class="sxs-lookup"><span data-stu-id="3977d-127">HOST_E_ABANDONED</span></span>|<span data-ttu-id="3977d-128">Un événement a été annulé alors qu’un thread bloqué ou Fibre l’attendait.</span><span class="sxs-lookup"><span data-stu-id="3977d-128">An event was canceled while a blocked thread or fiber was waiting on it.</span></span>|  
|<span data-ttu-id="3977d-129">E_FAIL</span><span class="sxs-lookup"><span data-stu-id="3977d-129">E_FAIL</span></span>|<span data-ttu-id="3977d-130">Une défaillance catastrophique inconnue s’est produite.</span><span class="sxs-lookup"><span data-stu-id="3977d-130">An unknown catastrophic failure occurred.</span></span> <span data-ttu-id="3977d-131">Une fois une méthode retourne E_FAIL, le CLR n’est plus utilisable au sein du processus.</span><span class="sxs-lookup"><span data-stu-id="3977d-131">After a method returns E_FAIL, the CLR is no longer usable within the process.</span></span> <span data-ttu-id="3977d-132">Les appels suivants aux méthodes d’hébergement retournent HOST_E_CLRNOTAVAILABLE.</span><span class="sxs-lookup"><span data-stu-id="3977d-132">Subsequent calls to hosting methods return HOST_E_CLRNOTAVAILABLE.</span></span>|  
|<span data-ttu-id="3977d-133">E_NOINTERFACE</span><span class="sxs-lookup"><span data-stu-id="3977d-133">E_NOINTERFACE</span></span>|<span data-ttu-id="3977d-134">Le type d’interface n’est pas pris en charge.</span><span class="sxs-lookup"><span data-stu-id="3977d-134">The interface type is not supported.</span></span>|  
  
## <a name="requirements"></a><span data-ttu-id="3977d-135">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="3977d-135">Requirements</span></span>  
 <span data-ttu-id="3977d-136">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="3977d-136">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="3977d-137">**En-tête :** MSCorEE.h</span><span class="sxs-lookup"><span data-stu-id="3977d-137">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="3977d-138">**Bibliothèque :** Inclus en tant que ressource dans MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="3977d-138">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="3977d-139">**Versions du .NET Framework :** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="3977d-139">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="3977d-140">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="3977d-140">See also</span></span>

- [<span data-ttu-id="3977d-141">ICLRControl, interface</span><span class="sxs-lookup"><span data-stu-id="3977d-141">ICLRControl Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/iclrcontrol-interface.md)
- [<span data-ttu-id="3977d-142">IHostControl, interface</span><span class="sxs-lookup"><span data-stu-id="3977d-142">IHostControl Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/ihostcontrol-interface.md)
