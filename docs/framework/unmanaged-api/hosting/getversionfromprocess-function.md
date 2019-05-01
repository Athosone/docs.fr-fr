---
title: GetVersionFromProcess, fonction
ms.date: 03/30/2017
api_name:
- GetVersionFromProcess
api_location:
- mscoree.dll
- mscoreei.dll
api_type:
- DLLExport
f1_keywords:
- GetVersionFromProcess
helpviewer_keywords:
- GetVersionFromProcess function [.NET Framework hosting]
ms.assetid: a9f7f824-64a1-408d-8607-91c7f19d21fe
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 452104939acf5de7bb151cba00d65fb6631c98d5
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61985632"
---
# <a name="getversionfromprocess-function"></a><span data-ttu-id="a6434-102">GetVersionFromProcess, fonction</span><span class="sxs-lookup"><span data-stu-id="a6434-102">GetVersionFromProcess Function</span></span>
<span data-ttu-id="a6434-103">Obtient le numéro de version du common language runtime (CLR) qui est associé au handle de processus spécifié.</span><span class="sxs-lookup"><span data-stu-id="a6434-103">Gets the version number of the common language runtime (CLR) that is associated with the specified process handle.</span></span>  
  
 <span data-ttu-id="a6434-104">Cette fonction a été déconseillée dans le [!INCLUDE[net_v40_long](../../../../includes/net-v40-long-md.md)].</span><span class="sxs-lookup"><span data-stu-id="a6434-104">This function has been deprecated in the [!INCLUDE[net_v40_long](../../../../includes/net-v40-long-md.md)].</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="a6434-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="a6434-105">Syntax</span></span>  
  
```  
HRESULT GetVersionFromProcess (  
    [in]  HANDLE  hProcess,   
    [out] LPWSTR  pVersion,   
    [in]  DWORD   cchBuffer,   
    [out] DWORD  *dwLength  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="a6434-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="a6434-106">Parameters</span></span>  
 `hProcess`  
 <span data-ttu-id="a6434-107">[in] Un handle à un processus.</span><span class="sxs-lookup"><span data-stu-id="a6434-107">[in] A handle to a process.</span></span>  
  
 `pVersion`  
 <span data-ttu-id="a6434-108">[out] Une mémoire tampon qui contient la chaîne de numéro de version en cas de réussite de la méthode.</span><span class="sxs-lookup"><span data-stu-id="a6434-108">[out] A buffer that contains the version number string upon successful completion of the method.</span></span>  
  
 `cchBuffer`  
 <span data-ttu-id="a6434-109">[in] La longueur de la mémoire tampon de version.</span><span class="sxs-lookup"><span data-stu-id="a6434-109">[in] The length of the version buffer.</span></span>  
  
 `pdwLength`  
 <span data-ttu-id="a6434-110">[out] Pointeur vers la longueur de la chaîne de numéro de version.</span><span class="sxs-lookup"><span data-stu-id="a6434-110">[out] A pointer to the length of the version number string.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="a6434-111">Valeur de retour</span><span class="sxs-lookup"><span data-stu-id="a6434-111">Return Value</span></span>  
 <span data-ttu-id="a6434-112">Cette méthode retourne des codes d’erreur de composant COM (Object Model) standard, tel que défini dans WinError.h, en plus des valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="a6434-112">This method returns standard Component Object Model (COM) error codes, as defined in WinError.h, in addition to the following values.</span></span>  
  
|<span data-ttu-id="a6434-113">Code de retour</span><span class="sxs-lookup"><span data-stu-id="a6434-113">Return code</span></span>|<span data-ttu-id="a6434-114">Description</span><span class="sxs-lookup"><span data-stu-id="a6434-114">Description</span></span>|  
|-----------------|-----------------|  
|<span data-ttu-id="a6434-115">S_OK</span><span class="sxs-lookup"><span data-stu-id="a6434-115">S_OK</span></span>|<span data-ttu-id="a6434-116">La commande s'est correctement terminée.</span><span class="sxs-lookup"><span data-stu-id="a6434-116">The method completed successfully.</span></span>|  
|<span data-ttu-id="a6434-117">E_INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="a6434-117">E_INVALIDARG</span></span>|<span data-ttu-id="a6434-118">`pVersion` a la valeur null et `cchBuffer` n’est pas null, ou vice versa.</span><span class="sxs-lookup"><span data-stu-id="a6434-118">`pVersion` is null and `cchBuffer` is not null, or vice versa.</span></span><br /><br /> <span data-ttu-id="a6434-119">- ou -</span><span class="sxs-lookup"><span data-stu-id="a6434-119">-or-</span></span><br /><br /> <span data-ttu-id="a6434-120">`hProcess` n’est pas un handle valide à un processus.</span><span class="sxs-lookup"><span data-stu-id="a6434-120">`hProcess` is not a valid handle to a process.</span></span><br /><br /> <span data-ttu-id="a6434-121">- ou -</span><span class="sxs-lookup"><span data-stu-id="a6434-121">-or-</span></span><br /><br /> <span data-ttu-id="a6434-122">Le CLR n’est pas chargé.</span><span class="sxs-lookup"><span data-stu-id="a6434-122">The CLR is not loaded.</span></span>|  
|<span data-ttu-id="a6434-123">ERROR_INSUFFICIENT_BUFFER</span><span class="sxs-lookup"><span data-stu-id="a6434-123">ERROR_INSUFFICIENT_BUFFER</span></span>|<span data-ttu-id="a6434-124">`cchBuffer` est null ou inférieure à la longueur de la chaîne de version.</span><span class="sxs-lookup"><span data-stu-id="a6434-124">`cchBuffer` is null or less than the length of the version string.</span></span>|  
|<span data-ttu-id="a6434-125">E_NOTIMPL</span><span class="sxs-lookup"><span data-stu-id="a6434-125">E_NOTIMPL</span></span>|<span data-ttu-id="a6434-126">Cette méthode n’est pas disponible sur le système d’exploitation Microsoft Windows 95, Microsoft Windows 98 ou Microsoft Windows Millennium Edition.</span><span class="sxs-lookup"><span data-stu-id="a6434-126">This method is not available on the Microsoft Windows 95, Microsoft Windows 98, or Microsoft Windows Millennium Edition operating system.</span></span>|  
  
## <a name="requirements"></a><span data-ttu-id="a6434-127">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="a6434-127">Requirements</span></span>  
 <span data-ttu-id="a6434-128">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="a6434-128">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="a6434-129">**En-tête :** MSCorEE.h</span><span class="sxs-lookup"><span data-stu-id="a6434-129">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="a6434-130">**Bibliothèque :** MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="a6434-130">**Library:** MSCorEE.dll</span></span>  
  
 <span data-ttu-id="a6434-131">**Versions du .NET Framework :** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="a6434-131">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="a6434-132">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a6434-132">See also</span></span>

- [<span data-ttu-id="a6434-133">GetRequestedRuntimeInfo, fonction</span><span class="sxs-lookup"><span data-stu-id="a6434-133">GetRequestedRuntimeInfo Function</span></span>](../../../../docs/framework/unmanaged-api/hosting/getrequestedruntimeinfo-function.md)
- [<span data-ttu-id="a6434-134">GetRequestedRuntimeVersion, fonction</span><span class="sxs-lookup"><span data-stu-id="a6434-134">GetRequestedRuntimeVersion Function</span></span>](../../../../docs/framework/unmanaged-api/hosting/getrequestedruntimeversion-function.md)
- [<span data-ttu-id="a6434-135">Fonctions d’hébergement CLR dépréciées</span><span class="sxs-lookup"><span data-stu-id="a6434-135">Deprecated CLR Hosting Functions</span></span>](../../../../docs/framework/unmanaged-api/hosting/deprecated-clr-hosting-functions.md)
