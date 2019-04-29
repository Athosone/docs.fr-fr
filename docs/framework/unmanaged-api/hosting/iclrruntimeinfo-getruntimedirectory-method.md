---
title: ICLRRuntimeInfo::GetRuntimeDirectory, méthode
ms.date: 03/30/2017
api_name:
- ICLRRuntimeInfo.GetRuntimeDirectory
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- ICLRRuntimeInfo::GetRuntimeDirectory
helpviewer_keywords:
- GetRuntimeDirectory method [.NET Framework hosting]
- ICLRRuntimeInfo::GetRuntimeDirectory method [.NET Framework hosting]
ms.assetid: 4401546e-4d48-453f-a1fb-b2ebda54df5c
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 5c09f57ad805b4ba17b4bdafd3ced533199277a0
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61771700"
---
# <a name="iclrruntimeinfogetruntimedirectory-method"></a><span data-ttu-id="dc69b-102">ICLRRuntimeInfo::GetRuntimeDirectory, méthode</span><span class="sxs-lookup"><span data-stu-id="dc69b-102">ICLRRuntimeInfo::GetRuntimeDirectory Method</span></span>
<span data-ttu-id="dc69b-103">Obtient le répertoire d’installation du common language runtime (CLR) associé à cette interface.</span><span class="sxs-lookup"><span data-stu-id="dc69b-103">Gets the installation directory of the common language runtime (CLR) associated with this interface.</span></span>  
  
 <span data-ttu-id="dc69b-104">Cette méthode remplace la [GetCORSystemDirectory](../../../../docs/framework/unmanaged-api/hosting/getcorsystemdirectory-function.md) fournie dans les versions de .NET Framework 2.0, 3.0 et 3.5.</span><span class="sxs-lookup"><span data-stu-id="dc69b-104">This method supersedes the [GetCORSystemDirectory](../../../../docs/framework/unmanaged-api/hosting/getcorsystemdirectory-function.md) function provided in the .NET Framework versions 2.0, 3.0, and 3.5.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="dc69b-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="dc69b-105">Syntax</span></span>  
  
```  
HRESULT GetRuntimeDirectory(  
[out, size_is(*pcchBuffer)] LPWSTR pwzBuffer,  
[in, out]  DWORD *pcchBuffer);  
```  
  
## <a name="parameters"></a><span data-ttu-id="dc69b-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="dc69b-106">Parameters</span></span>  
 `pwzBuffer`  
 <span data-ttu-id="dc69b-107">[out] Retourne le répertoire d’installation de CLR.</span><span class="sxs-lookup"><span data-stu-id="dc69b-107">[out] Returns the CLR installation directory.</span></span> <span data-ttu-id="dc69b-108">Le chemin d’installation est complet ; par exemple, « c:\windows\microsoft.net\framework\v1.0.3705\\».</span><span class="sxs-lookup"><span data-stu-id="dc69b-108">The installation path is fully qualified; for example, "c:\windows\microsoft.net\framework\v1.0.3705\\".</span></span>  
  
 `pchBuffer`  
 <span data-ttu-id="dc69b-109">[in, out] Spécifie la taille du `pwzBuffer` pour éviter les dépassements de mémoire tampon.</span><span class="sxs-lookup"><span data-stu-id="dc69b-109">[in, out] Specifies the size of `pwzBuffer` to avoid buffer overruns.</span></span> <span data-ttu-id="dc69b-110">Si `pwzBuffer` a la valeur null, `pchBuffer` retourne la taille requise de `pwzBuffer`.</span><span class="sxs-lookup"><span data-stu-id="dc69b-110">If `pwzBuffer` is null, `pchBuffer` returns the required size of `pwzBuffer`.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="dc69b-111">Valeur de retour</span><span class="sxs-lookup"><span data-stu-id="dc69b-111">Return Value</span></span>  
 <span data-ttu-id="dc69b-112">Cette méthode retourne les HRESULT spécifiques suivants ainsi que les erreurs HRESULT indiquant l'échec de la méthode.</span><span class="sxs-lookup"><span data-stu-id="dc69b-112">This method returns the following specific HRESULTs as well as HRESULT errors that indicate method failure.</span></span>  
  
|<span data-ttu-id="dc69b-113">HRESULT</span><span class="sxs-lookup"><span data-stu-id="dc69b-113">HRESULT</span></span>|<span data-ttu-id="dc69b-114">Description</span><span class="sxs-lookup"><span data-stu-id="dc69b-114">Description</span></span>|  
|-------------|-----------------|  
|<span data-ttu-id="dc69b-115">S_OK</span><span class="sxs-lookup"><span data-stu-id="dc69b-115">S_OK</span></span>|<span data-ttu-id="dc69b-116">La commande s'est correctement terminée.</span><span class="sxs-lookup"><span data-stu-id="dc69b-116">The method completed successfully.</span></span>|  
|<span data-ttu-id="dc69b-117">E_POINTER</span><span class="sxs-lookup"><span data-stu-id="dc69b-117">E_POINTER</span></span>|<span data-ttu-id="dc69b-118">`pwzBuffer` ou `pchBuffer` est null.</span><span class="sxs-lookup"><span data-stu-id="dc69b-118">`pwzBuffer` or `pchBuffer` is null.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="dc69b-119">Notes</span><span class="sxs-lookup"><span data-stu-id="dc69b-119">Remarks</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="dc69b-120">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="dc69b-120">Requirements</span></span>  
 <span data-ttu-id="dc69b-121">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="dc69b-121">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="dc69b-122">**En-tête :** MetaHost.h</span><span class="sxs-lookup"><span data-stu-id="dc69b-122">**Header:** MetaHost.h</span></span>  
  
 <span data-ttu-id="dc69b-123">**Bibliothèque :** Inclus en tant que ressource dans MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="dc69b-123">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="dc69b-124">**Versions du .NET Framework :** [!INCLUDE[net_current_v40plus](../../../../includes/net-current-v40plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="dc69b-124">**.NET Framework Versions:** [!INCLUDE[net_current_v40plus](../../../../includes/net-current-v40plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="dc69b-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="dc69b-125">See also</span></span>

- [<span data-ttu-id="dc69b-126">ICLRRuntimeInfo, interface</span><span class="sxs-lookup"><span data-stu-id="dc69b-126">ICLRRuntimeInfo Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/iclrruntimeinfo-interface.md)
- [<span data-ttu-id="dc69b-127">Hébergement</span><span class="sxs-lookup"><span data-stu-id="dc69b-127">Hosting</span></span>](../../../../docs/framework/unmanaged-api/hosting/index.md)
