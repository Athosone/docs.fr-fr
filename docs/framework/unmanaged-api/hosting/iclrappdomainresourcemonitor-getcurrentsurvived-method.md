---
title: ICLRAppDomainResourceMonitor::GetCurrentSurvived, méthode
ms.date: 03/30/2017
api_name:
- ICLRAppDomainResourceMonitor.GetCurrentSurvived
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- ICLRAppDomainResourceMonitor::GetCurrentSurvived
helpviewer_keywords:
- ICLRAppDomainResourceMonitor::GetCurrentSurvived method [.NET Framework hosting]
- GetCurrentSurvived method [.NET Framework hosting]
ms.assetid: 392e9009-40ef-40e3-ad4d-7ce93a989e78
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 408ef5419fbc2081d25ad442986ec8155bcb4c62
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59141542"
---
# <a name="iclrappdomainresourcemonitorgetcurrentsurvived-method"></a><span data-ttu-id="96d29-102">ICLRAppDomainResourceMonitor::GetCurrentSurvived, méthode</span><span class="sxs-lookup"><span data-stu-id="96d29-102">ICLRAppDomainResourceMonitor::GetCurrentSurvived Method</span></span>
<span data-ttu-id="96d29-103">Obtient le nombre d’octets qui ont survécu à la dernière complète, le garbage collection de blocage et qui sont référencés par le domaine d’application actuel.</span><span class="sxs-lookup"><span data-stu-id="96d29-103">Gets the number of bytes that survived the last full, blocking garbage collection and that are referenced by the current application domain.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="96d29-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="96d29-104">Syntax</span></span>  
  
```  
HRESULT STDMETHODCALLTYPE GetCurrentSurvived(  
             [in]  DWORD dwAppDomainId,  
             [out] ULONGLONG *pAppDomainBytesSurvived,  
             [out] ULONGLONG *pTotalBytesSurvived);  
```  
  
## <a name="parameters"></a><span data-ttu-id="96d29-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="96d29-105">Parameters</span></span>  
 `dwAppDomainId`  
 <span data-ttu-id="96d29-106">[in] L’ID du domaine d’application demandée.</span><span class="sxs-lookup"><span data-stu-id="96d29-106">[in] The ID of the requested application domain.</span></span>  
  
 `pAppDomainBytesSurvived`  
 <span data-ttu-id="96d29-107">[out] Pointeur vers le nombre d’octets ayant survécu après le dernier garbage collection et qui sont détenus par ce domaine d’application.</span><span class="sxs-lookup"><span data-stu-id="96d29-107">[out] A pointer to the number of bytes that survived after the last garbage collection that are held by this application domain.</span></span> <span data-ttu-id="96d29-108">Après une collection complète, ce nombre est exact et complet.</span><span class="sxs-lookup"><span data-stu-id="96d29-108">After a full collection, this number is accurate and complete.</span></span> <span data-ttu-id="96d29-109">Après une collection éphémère, ce nombre est potentiellement incomplet.</span><span class="sxs-lookup"><span data-stu-id="96d29-109">After an ephemeral collection, this number is potentially incomplete.</span></span> <span data-ttu-id="96d29-110">Ce paramètre peut être `null`.</span><span class="sxs-lookup"><span data-stu-id="96d29-110">This parameter can be `null`.</span></span>  
  
 `pRuntimeBytesSurvived`  
 <span data-ttu-id="96d29-111">[out] Pointeur vers le nombre total d’octets ayant survécu à partir du dernier garbage collection.</span><span class="sxs-lookup"><span data-stu-id="96d29-111">[out] A pointer to the total number of bytes that survived from the last garbage collection.</span></span> <span data-ttu-id="96d29-112">Après une collection complète, ce nombre représente le nombre d’octets qui sont conservées dans les tas managés.</span><span class="sxs-lookup"><span data-stu-id="96d29-112">After a full collection, this number represents the number of the bytes that are held in managed heaps.</span></span> <span data-ttu-id="96d29-113">Après une collection éphémère, ce nombre représente le nombre d’octets qui sont maintenus actifs dans les générations éphémères.</span><span class="sxs-lookup"><span data-stu-id="96d29-113">After an ephemeral collection, this number represents the number of bytes that are held live in ephemeral generations.</span></span> <span data-ttu-id="96d29-114">Ce paramètre peut être `null`.</span><span class="sxs-lookup"><span data-stu-id="96d29-114">This parameter can be `null`.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="96d29-115">Valeur de retour</span><span class="sxs-lookup"><span data-stu-id="96d29-115">Return Value</span></span>  
 <span data-ttu-id="96d29-116">Cette méthode retourne les HRESULT spécifiques suivants ainsi que les erreurs HRESULT indiquant l'échec de la méthode.</span><span class="sxs-lookup"><span data-stu-id="96d29-116">This method returns the following specific HRESULTs as well as HRESULT errors that indicate method failure.</span></span>  
  
|<span data-ttu-id="96d29-117">HRESULT</span><span class="sxs-lookup"><span data-stu-id="96d29-117">HRESULT</span></span>|<span data-ttu-id="96d29-118">Description</span><span class="sxs-lookup"><span data-stu-id="96d29-118">Description</span></span>|  
|-------------|-----------------|  
|<span data-ttu-id="96d29-119">S_OK</span><span class="sxs-lookup"><span data-stu-id="96d29-119">S_OK</span></span>|<span data-ttu-id="96d29-120">La commande s'est correctement terminée.</span><span class="sxs-lookup"><span data-stu-id="96d29-120">The method completed successfully.</span></span>|  
|<span data-ttu-id="96d29-121">COR_E_APPDOMAINUNLOADED</span><span class="sxs-lookup"><span data-stu-id="96d29-121">COR_E_APPDOMAINUNLOADED</span></span>|<span data-ttu-id="96d29-122">Le domaine d’application a été déchargé ou n’existe pas.</span><span class="sxs-lookup"><span data-stu-id="96d29-122">The application domain has been unloaded or does not exist.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="96d29-123">Notes</span><span class="sxs-lookup"><span data-stu-id="96d29-123">Remarks</span></span>  
 <span data-ttu-id="96d29-124">Les statistiques sont mises à jour uniquement après un blocage de garbage collection de ; complet Autrement dit, une collection qui inclut toutes les générations et qui arrête l’application lors de la collection se produit.</span><span class="sxs-lookup"><span data-stu-id="96d29-124">Statistics are updated only after a full, blocking garbage collection; that is, a collection that includes all generations and that stops the application while collection occurs.</span></span> <span data-ttu-id="96d29-125">Par exemple, le <xref:System.GC.Collect?displayProperty=nameWithType> surcharge de méthode effectue une collecte bloquante complète.</span><span class="sxs-lookup"><span data-stu-id="96d29-125">For example, the <xref:System.GC.Collect?displayProperty=nameWithType> method overload performs a full, blocking collection.</span></span> <span data-ttu-id="96d29-126">Le garbage collection simultané se produit en arrière-plan et ne bloque pas l’application.</span><span class="sxs-lookup"><span data-stu-id="96d29-126">Concurrent garbage collection occurs in the background and does not block the application.</span></span>  
  
 <span data-ttu-id="96d29-127">Le `GetCurrentSurvived` méthode est l’équivalent non managé de managé <xref:System.AppDomain.MonitoringSurvivedMemorySize%2A?displayProperty=nameWithType> propriété.</span><span class="sxs-lookup"><span data-stu-id="96d29-127">The `GetCurrentSurvived` method is the unmanaged equivalent of the managed <xref:System.AppDomain.MonitoringSurvivedMemorySize%2A?displayProperty=nameWithType> property.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="96d29-128">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="96d29-128">Requirements</span></span>  
 <span data-ttu-id="96d29-129">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="96d29-129">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="96d29-130">**En-tête :** MetaHost.h</span><span class="sxs-lookup"><span data-stu-id="96d29-130">**Header:** MetaHost.h</span></span>  
  
 <span data-ttu-id="96d29-131">**Bibliothèque :** Inclus en tant que ressource dans MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="96d29-131">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="96d29-132">**Versions du .NET Framework :** [!INCLUDE[net_current_v40plus](../../../../includes/net-current-v40plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="96d29-132">**.NET Framework Versions:** [!INCLUDE[net_current_v40plus](../../../../includes/net-current-v40plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="96d29-133">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="96d29-133">See also</span></span>

- [<span data-ttu-id="96d29-134">ICLRAppDomainResourceMonitor, interface</span><span class="sxs-lookup"><span data-stu-id="96d29-134">ICLRAppDomainResourceMonitor Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/iclrappdomainresourcemonitor-interface.md)
- [<span data-ttu-id="96d29-135">Analyse de ressource de domaine d'application</span><span class="sxs-lookup"><span data-stu-id="96d29-135">Application Domain Resource Monitoring</span></span>](../../../../docs/standard/garbage-collection/app-domain-resource-monitoring.md)
- [<span data-ttu-id="96d29-136">Interfaces d’hébergement</span><span class="sxs-lookup"><span data-stu-id="96d29-136">Hosting Interfaces</span></span>](../../../../docs/framework/unmanaged-api/hosting/hosting-interfaces.md)
- [<span data-ttu-id="96d29-137">Hébergement</span><span class="sxs-lookup"><span data-stu-id="96d29-137">Hosting</span></span>](../../../../docs/framework/unmanaged-api/hosting/index.md)
