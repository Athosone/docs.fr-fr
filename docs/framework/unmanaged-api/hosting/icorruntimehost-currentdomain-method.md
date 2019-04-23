---
title: ICorRuntimeHost::CurrentDomain, méthode
ms.date: 03/30/2017
api_name:
- ICorRuntimeHost.CurrentDomain
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- ICorRuntimeHost::CurrentDomain
helpviewer_keywords:
- ICorRuntimeHost::CreateDomain method [.NET Framework hosting]
- CurrentDomain method [.NET Framework hosting]
ms.assetid: dd2afb38-675b-4c3c-a9f3-8ab3b133eb02
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 1cb5ff5300a7fd2577e602b3077dd816cf7dfbe2
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59181379"
---
# <a name="icorruntimehostcurrentdomain-method"></a><span data-ttu-id="ab911-102">ICorRuntimeHost::CurrentDomain, méthode</span><span class="sxs-lookup"><span data-stu-id="ab911-102">ICorRuntimeHost::CurrentDomain Method</span></span>
<span data-ttu-id="ab911-103">Obtient un pointeur d’interface de type <xref:System.AppDomain?displayProperty=nameWithType> qui représente le domaine chargé sur le thread actuel.</span><span class="sxs-lookup"><span data-stu-id="ab911-103">Gets an interface pointer of type <xref:System.AppDomain?displayProperty=nameWithType> that represents the domain loaded on the current thread.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="ab911-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="ab911-104">Syntax</span></span>  
  
```  
HRESULT CurrentDomain (  
    [out] IUnknown** pAppDomain  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="ab911-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="ab911-105">Parameters</span></span>  
 `pAppDomain`  
 <span data-ttu-id="ab911-106">[out] Un pointeur de type <xref:System.AppDomain?displayProperty=nameWithType> qui représente le domaine d’application actuel du thread.</span><span class="sxs-lookup"><span data-stu-id="ab911-106">[out] A pointer of type <xref:System.AppDomain?displayProperty=nameWithType> that represents the thread's current application domain.</span></span> <span data-ttu-id="ab911-107">Ce pointeur est tapé `IUnknown`, de sorte que les appelants doivent généralement appeler `QueryInterface` pour obtenir un pointeur de type <xref:System._AppDomain>.</span><span class="sxs-lookup"><span data-stu-id="ab911-107">This pointer is typed `IUnknown`, so callers should generally call `QueryInterface` to obtain a pointer of type <xref:System._AppDomain>.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="ab911-108">Valeur de retour</span><span class="sxs-lookup"><span data-stu-id="ab911-108">Return Value</span></span>  
  
|<span data-ttu-id="ab911-109">HRESULT</span><span class="sxs-lookup"><span data-stu-id="ab911-109">HRESULT</span></span>|<span data-ttu-id="ab911-110">Description</span><span class="sxs-lookup"><span data-stu-id="ab911-110">Description</span></span>|  
|-------------|-----------------|  
|<span data-ttu-id="ab911-111">S_OK</span><span class="sxs-lookup"><span data-stu-id="ab911-111">S_OK</span></span>|<span data-ttu-id="ab911-112">L’opération a réussi.</span><span class="sxs-lookup"><span data-stu-id="ab911-112">The operation was successful.</span></span>|  
|<span data-ttu-id="ab911-113">S_FALSE</span><span class="sxs-lookup"><span data-stu-id="ab911-113">S_FALSE</span></span>|<span data-ttu-id="ab911-114">L’opération a échoué.</span><span class="sxs-lookup"><span data-stu-id="ab911-114">The operation failed to complete.</span></span>|  
|<span data-ttu-id="ab911-115">E_FAIL</span><span class="sxs-lookup"><span data-stu-id="ab911-115">E_FAIL</span></span>|<span data-ttu-id="ab911-116">Une défaillance grave et inconnue s’est produite.</span><span class="sxs-lookup"><span data-stu-id="ab911-116">An unknown, catastrophic failure occurred.</span></span> <span data-ttu-id="ab911-117">Si une méthode retourne E_FAIL, le common language runtime (CLR) n’est plus utilisable dans le processus.</span><span class="sxs-lookup"><span data-stu-id="ab911-117">If a method returns E_FAIL, the common language runtime (CLR) is no longer usable in the process.</span></span> <span data-ttu-id="ab911-118">Les appels suivants à toute API d’hébergement retournent HOST_E_CLRNOTAVAILABLE.</span><span class="sxs-lookup"><span data-stu-id="ab911-118">Subsequent calls to any hosting APIs return HOST_E_CLRNOTAVAILABLE.</span></span>|  
|<span data-ttu-id="ab911-119">HOST_E_CLRNOTAVAILABLE</span><span class="sxs-lookup"><span data-stu-id="ab911-119">HOST_E_CLRNOTAVAILABLE</span></span>|<span data-ttu-id="ab911-120">Le CLR n’a pas été chargé dans un processus ou le CLR est dans un état dans lequel il ne peut pas exécuter le code managé ou traiter l’appel avec succès.</span><span class="sxs-lookup"><span data-stu-id="ab911-120">The CLR has not been loaded into a process, or the CLR is in a state in which it cannot run managed code or process the call successfully.</span></span>|  
  
## <a name="requirements"></a><span data-ttu-id="ab911-121">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="ab911-121">Requirements</span></span>  
 <span data-ttu-id="ab911-122">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="ab911-122">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="ab911-123">**En-tête :** MSCorEE.h</span><span class="sxs-lookup"><span data-stu-id="ab911-123">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="ab911-124">**Bibliothèque :** Inclus en tant que ressource dans MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="ab911-124">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="ab911-125">**Versions du .NET framework :** 1.0, 1.1</span><span class="sxs-lookup"><span data-stu-id="ab911-125">**.NET Framework Versions:** 1.0, 1.1</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="ab911-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ab911-126">See also</span></span>

- <xref:System._AppDomain>
- <xref:System.AppDomain>
- [<span data-ttu-id="ab911-127">ICorRuntimeHost, interface</span><span class="sxs-lookup"><span data-stu-id="ab911-127">ICorRuntimeHost Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/icorruntimehost-interface.md)
