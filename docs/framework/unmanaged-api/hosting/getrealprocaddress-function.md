---
title: GetRealProcAddress, fonction
ms.date: 03/30/2017
api_name:
- GetRealProcAddress
api_location:
- mscoree.dll
api_type:
- DLLExport
f1_keywords:
- GetRealProcAddress
helpviewer_keywords:
- GetRealProcAddress function [.NET Framework hosting]
ms.assetid: f1f2fab1-400b-488f-95f2-d49c4fca3556
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 5d4723fbf2311316184cb77c90754d7e037badcd
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59089580"
---
# <a name="getrealprocaddress-function"></a><span data-ttu-id="00c22-102">GetRealProcAddress, fonction</span><span class="sxs-lookup"><span data-stu-id="00c22-102">GetRealProcAddress Function</span></span>
<span data-ttu-id="00c22-103">Obtient l’adresse de la fonction spécifiée qui est exportée à partir de la dernière version installée pour le common language runtime (CLR).</span><span class="sxs-lookup"><span data-stu-id="00c22-103">Gets the address of the specified function that is exported from the latest installed version of the common language runtime (CLR).</span></span>  
  
 <span data-ttu-id="00c22-104">Cette fonction a été déconseillée dans le [!INCLUDE[net_v40_long](../../../../includes/net-v40-long-md.md)].</span><span class="sxs-lookup"><span data-stu-id="00c22-104">This function has been deprecated in the [!INCLUDE[net_v40_long](../../../../includes/net-v40-long-md.md)].</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="00c22-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="00c22-105">Syntax</span></span>  
  
```  
HRESULT GetRealProcAddress (  
    [in]  LPCSTR  pwszProcName,   
    [out] VOID  **ppv  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="00c22-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="00c22-106">Parameters</span></span>  
 `pwszProcName`  
 <span data-ttu-id="00c22-107">[in] Le nom de la fonction.</span><span class="sxs-lookup"><span data-stu-id="00c22-107">[in] The name of the function.</span></span>  
  
 `ppv`  
 <span data-ttu-id="00c22-108">[out] L’emplacement qui reçoit un pointeur vers l’adresse de la fonction.</span><span class="sxs-lookup"><span data-stu-id="00c22-108">[out] The location that receives a pointer to the address of the function.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="00c22-109">Valeur de retour</span><span class="sxs-lookup"><span data-stu-id="00c22-109">Return Value</span></span>  
 <span data-ttu-id="00c22-110">Cette méthode retourne des codes d’erreur de composant COM (Object Model) standard, tel que défini dans WinError.h, en plus des valeurs suivantes définies dans CorError.h.</span><span class="sxs-lookup"><span data-stu-id="00c22-110">This method returns standard Component Object Model (COM) error codes, as defined in WinError.h, in addition to the following values defined in CorError.h.</span></span>  
  
|<span data-ttu-id="00c22-111">Code de retour</span><span class="sxs-lookup"><span data-stu-id="00c22-111">Return code</span></span>|<span data-ttu-id="00c22-112">Description</span><span class="sxs-lookup"><span data-stu-id="00c22-112">Description</span></span>|  
|-----------------|-----------------|  
|<span data-ttu-id="00c22-113">S_OK</span><span class="sxs-lookup"><span data-stu-id="00c22-113">S_OK</span></span>|<span data-ttu-id="00c22-114">La commande s'est correctement terminée.</span><span class="sxs-lookup"><span data-stu-id="00c22-114">The method completed successfully.</span></span>|  
|<span data-ttu-id="00c22-115">E_POINTER</span><span class="sxs-lookup"><span data-stu-id="00c22-115">E_POINTER</span></span>|<span data-ttu-id="00c22-116">`ppv` n'est pas valide.</span><span class="sxs-lookup"><span data-stu-id="00c22-116">`ppv` is not valid.</span></span>|  
|<span data-ttu-id="00c22-117">CLR_E_SHIM_RUNTIMEEXPORT</span><span class="sxs-lookup"><span data-stu-id="00c22-117">CLR_E_SHIM_RUNTIMEEXPORT</span></span>|<span data-ttu-id="00c22-118">La fonction n’est pas exportée à partir de l’exécution.</span><span class="sxs-lookup"><span data-stu-id="00c22-118">The function is not exported from the runtime.</span></span>|  
  
## <a name="requirements"></a><span data-ttu-id="00c22-119">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="00c22-119">Requirements</span></span>  
 <span data-ttu-id="00c22-120">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="00c22-120">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="00c22-121">**En-tête :** MSCorEE.h</span><span class="sxs-lookup"><span data-stu-id="00c22-121">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="00c22-122">**Bibliothèque :** MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="00c22-122">**Library:** MSCorEE.dll</span></span>  
  
 <span data-ttu-id="00c22-123">**Versions du .NET Framework :** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="00c22-123">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="00c22-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="00c22-124">See also</span></span>

- [<span data-ttu-id="00c22-125">Fonctions d’hébergement CLR dépréciées</span><span class="sxs-lookup"><span data-stu-id="00c22-125">Deprecated CLR Hosting Functions</span></span>](../../../../docs/framework/unmanaged-api/hosting/deprecated-clr-hosting-functions.md)
