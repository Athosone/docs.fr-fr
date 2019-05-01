---
title: ICLRRuntimeInfo::IsStarted, méthode
ms.date: 03/30/2017
api_name:
- ICLRRuntimeInfo.IsStarted
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- ICLRRuntimeInfo::IsStarted
helpviewer_keywords:
- IsStarted method [.NET Framework hosting]
- ICLRRuntimeInfo::IsStarted method [.NET Framework hosting]
ms.assetid: ef6f2662-323b-4534-aa82-6d1afb7b9309
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 1297c84acadf0a53b418b06afe806237d374ee25
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61993159"
---
# <a name="iclrruntimeinfoisstarted-method"></a><span data-ttu-id="8fdc3-102">ICLRRuntimeInfo::IsStarted, méthode</span><span class="sxs-lookup"><span data-stu-id="8fdc3-102">ICLRRuntimeInfo::IsStarted Method</span></span>
<span data-ttu-id="8fdc3-103">Indique si le runtime a été démarré (autrement dit, si le [méthode ICLRRuntimeHost::Start](../../../../docs/framework/unmanaged-api/hosting/iclrruntimehost-start-method.md) a été appelé et a réussi).</span><span class="sxs-lookup"><span data-stu-id="8fdc3-103">Indicates whether the runtime has been started (that is, whether the [ICLRRuntimeHost::Start method](../../../../docs/framework/unmanaged-api/hosting/iclrruntimehost-start-method.md) has been called and has succeeded).</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="8fdc3-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="8fdc3-104">Syntax</span></span>  
  
```  
HRESULT IsStarted(  
        [out] BOOL     *pbStarted,  
        [out] DWORD    *pdwStartupFlags);  
```  
  
## <a name="parameters"></a><span data-ttu-id="8fdc3-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="8fdc3-105">Parameters</span></span>  
 `pbStarted`  
 <span data-ttu-id="8fdc3-106">[out] `true` si cette exécution est démarrée ; sinon, `false`.</span><span class="sxs-lookup"><span data-stu-id="8fdc3-106">[out] `true` if this runtime is started; otherwise, `false`.</span></span>  
  
 `pdwStartupFlags`  
 <span data-ttu-id="8fdc3-107">[out] Retourne les indicateurs qui ont été utilisés pour démarrer le runtime.</span><span class="sxs-lookup"><span data-stu-id="8fdc3-107">[out] Returns the flags that were used to start the runtime.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="8fdc3-108">Valeur de retour</span><span class="sxs-lookup"><span data-stu-id="8fdc3-108">Return Value</span></span>  
 <span data-ttu-id="8fdc3-109">Cette méthode retourne les HRESULT spécifiques suivants ainsi que les erreurs HRESULT indiquant l'échec de la méthode.</span><span class="sxs-lookup"><span data-stu-id="8fdc3-109">This method returns the following specific HRESULTs as well as HRESULT errors that indicate method failure.</span></span>  
  
|<span data-ttu-id="8fdc3-110">HRESULT</span><span class="sxs-lookup"><span data-stu-id="8fdc3-110">HRESULT</span></span>|<span data-ttu-id="8fdc3-111">Description</span><span class="sxs-lookup"><span data-stu-id="8fdc3-111">Description</span></span>|  
|-------------|-----------------|  
|<span data-ttu-id="8fdc3-112">S_OK</span><span class="sxs-lookup"><span data-stu-id="8fdc3-112">S_OK</span></span>|<span data-ttu-id="8fdc3-113">La commande s'est correctement terminée.</span><span class="sxs-lookup"><span data-stu-id="8fdc3-113">The method completed successfully.</span></span>|  
|<span data-ttu-id="8fdc3-114">E_NOTIMPL</span><span class="sxs-lookup"><span data-stu-id="8fdc3-114">E_NOTIMPL</span></span>|<span data-ttu-id="8fdc3-115">La version du common language runtime (CLR) est antérieure à la version du CLR dans le [!INCLUDE[net_v40_long](../../../../includes/net-v40-long-md.md)].</span><span class="sxs-lookup"><span data-stu-id="8fdc3-115">The common language runtime (CLR) version is earlier than the CLR version in the [!INCLUDE[net_v40_long](../../../../includes/net-v40-long-md.md)].</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="8fdc3-116">Notes</span><span class="sxs-lookup"><span data-stu-id="8fdc3-116">Remarks</span></span>  
 <span data-ttu-id="8fdc3-117">Cette méthode ne fonctionne pas antérieure à la version du CLR avec les versions CLR le [!INCLUDE[net_v40_short](../../../../includes/net-v40-short-md.md)].</span><span class="sxs-lookup"><span data-stu-id="8fdc3-117">This method does not work with CLR versions earlier than the CLR version in the [!INCLUDE[net_v40_short](../../../../includes/net-v40-short-md.md)].</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="8fdc3-118">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="8fdc3-118">Requirements</span></span>  
 <span data-ttu-id="8fdc3-119">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="8fdc3-119">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="8fdc3-120">**En-tête :** MetaHost.h</span><span class="sxs-lookup"><span data-stu-id="8fdc3-120">**Header:** MetaHost.h</span></span>  
  
 <span data-ttu-id="8fdc3-121">**Bibliothèque :** Inclus en tant que ressource dans MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="8fdc3-121">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="8fdc3-122">**Versions du .NET Framework :** [!INCLUDE[net_current_v40plus](../../../../includes/net-current-v40plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="8fdc3-122">**.NET Framework Versions:** [!INCLUDE[net_current_v40plus](../../../../includes/net-current-v40plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="8fdc3-123">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="8fdc3-123">See also</span></span>

- [<span data-ttu-id="8fdc3-124">ICLRRuntimeInfo, interface</span><span class="sxs-lookup"><span data-stu-id="8fdc3-124">ICLRRuntimeInfo Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/iclrruntimeinfo-interface.md)
- [<span data-ttu-id="8fdc3-125">Interfaces d’hébergement</span><span class="sxs-lookup"><span data-stu-id="8fdc3-125">Hosting Interfaces</span></span>](../../../../docs/framework/unmanaged-api/hosting/hosting-interfaces.md)
- [<span data-ttu-id="8fdc3-126">Hébergement</span><span class="sxs-lookup"><span data-stu-id="8fdc3-126">Hosting</span></span>](../../../../docs/framework/unmanaged-api/hosting/index.md)
