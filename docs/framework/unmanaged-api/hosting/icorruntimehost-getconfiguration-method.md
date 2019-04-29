---
title: ICorRuntimeHost::GetConfiguration, méthode
ms.date: 03/30/2017
api_name:
- ICorRuntimeHost.GetConfiguration
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- ICorRuntimeHost::GetConfiguration
helpviewer_keywords:
- ICorRuntimeHost::GetConfiguration method [.NET Framework hosting]
- GetConfiguration method [.NET Framework hosting]
ms.assetid: c431617a-b055-44a0-8730-48b7a86d9610
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: cf74da6eb0e7ce0215023a9a58d6b88c57c4fe8b
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61936940"
---
# <a name="icorruntimehostgetconfiguration-method"></a><span data-ttu-id="12eca-102">ICorRuntimeHost::GetConfiguration, méthode</span><span class="sxs-lookup"><span data-stu-id="12eca-102">ICorRuntimeHost::GetConfiguration Method</span></span>
<span data-ttu-id="12eca-103">Obtient un objet qui permet à l’hôte spécifier la configuration de rappel du common language runtime (CLR).</span><span class="sxs-lookup"><span data-stu-id="12eca-103">Gets an object that allows the host to specify the callback configuration of the common language runtime (CLR).</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="12eca-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="12eca-104">Syntax</span></span>  
  
```  
HRESULT GetConfiguration(  
    [out] ICorConfiguration** pConfiguration  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="12eca-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="12eca-105">Parameters</span></span>  
 `pConfiguration`  
 <span data-ttu-id="12eca-106">[out] Un pointeur vers l’adresse d’un [ICorConfiguration](../../../../docs/framework/unmanaged-api/hosting/icorconfiguration-interface.md) objet qui peut être utilisé pour configurer le CLR.</span><span class="sxs-lookup"><span data-stu-id="12eca-106">[out] A pointer to the address of an [ICorConfiguration](../../../../docs/framework/unmanaged-api/hosting/icorconfiguration-interface.md) object that can be used to configure the CLR.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="12eca-107">Notes</span><span class="sxs-lookup"><span data-stu-id="12eca-107">Remarks</span></span>  
 <span data-ttu-id="12eca-108">Le CLR doit être configuré avant son initialisation ; Sinon, le `GetConfiguration` méthode retourne une valeur HRESULT indiquant une erreur.</span><span class="sxs-lookup"><span data-stu-id="12eca-108">The CLR must be configured prior to its initialization; otherwise, the `GetConfiguration` method returns an HRESULT indicating an error.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="12eca-109">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="12eca-109">Requirements</span></span>  
 <span data-ttu-id="12eca-110">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="12eca-110">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="12eca-111">**En-tête :** MSCorEE.h</span><span class="sxs-lookup"><span data-stu-id="12eca-111">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="12eca-112">**Bibliothèque :** Inclus en tant que ressource dans MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="12eca-112">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="12eca-113">**Versions du .NET framework :** 1.0, 1.1</span><span class="sxs-lookup"><span data-stu-id="12eca-113">**.NET Framework Versions:** 1.0, 1.1</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="12eca-114">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="12eca-114">See also</span></span>

- [<span data-ttu-id="12eca-115">ICorRuntimeHost, interface</span><span class="sxs-lookup"><span data-stu-id="12eca-115">ICorRuntimeHost Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/icorruntimehost-interface.md)
