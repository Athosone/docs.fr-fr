---
title: GetCORRequiredVersion, fonction
ms.date: 03/30/2017
api_name:
- GetCORRequiredVersion
api_location:
- mscoree.dll
api_type:
- DLLExport
f1_keywords:
- GetCORRequiredVersion
helpviewer_keywords:
- GetCORRequiredVersion function [.NET Framework hosting]
ms.assetid: 1588fe7b-c378-4f4b-9c4b-48647f1119cc
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: b5786444c36fcfc9547be1db0006757b0a9376c6
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59175186"
---
# <a name="getcorrequiredversion-function"></a><span data-ttu-id="9a00b-102">GetCORRequiredVersion, fonction</span><span class="sxs-lookup"><span data-stu-id="9a00b-102">GetCORRequiredVersion Function</span></span>
<span data-ttu-id="9a00b-103">Obtient le numéro de version de runtime (CLR) de langage commun requis.</span><span class="sxs-lookup"><span data-stu-id="9a00b-103">Gets the required common language runtime (CLR) version number.</span></span>  
  
 <span data-ttu-id="9a00b-104">Cette fonction a été déconseillée dans le [!INCLUDE[net_v40_long](../../../../includes/net-v40-long-md.md)].</span><span class="sxs-lookup"><span data-stu-id="9a00b-104">This function has been deprecated in the [!INCLUDE[net_v40_long](../../../../includes/net-v40-long-md.md)].</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="9a00b-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="9a00b-105">Syntax</span></span>  
  
```  
HRESULT GetCORRequiredVersion (  
    [out] LPWSTR   pbuffer,  
    [in]  DWORD    cchBuffer,  
    [out] DWORD   *dwLength  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="9a00b-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="9a00b-106">Parameters</span></span>  
 `pbuffer`  
 <span data-ttu-id="9a00b-107">[out] Une mémoire tampon qui contient une chaîne qui spécifie le numéro de version.</span><span class="sxs-lookup"><span data-stu-id="9a00b-107">[out] A buffer containing a string that specifies the version number.</span></span>  
  
 `cchBuffer`  
 <span data-ttu-id="9a00b-108">[in] La taille, en octets, de la mémoire tampon.</span><span class="sxs-lookup"><span data-stu-id="9a00b-108">[in] The size, in bytes, of the buffer.</span></span>  
  
 `dwLength`  
 <span data-ttu-id="9a00b-109">[out] Le nombre d’octets retournés dans la mémoire tampon.</span><span class="sxs-lookup"><span data-stu-id="9a00b-109">[out] The number of bytes returned in the buffer.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="9a00b-110">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="9a00b-110">Requirements</span></span>  
 <span data-ttu-id="9a00b-111">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="9a00b-111">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="9a00b-112">**En-tête :** MSCorEE.h</span><span class="sxs-lookup"><span data-stu-id="9a00b-112">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="9a00b-113">**Bibliothèque :** MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="9a00b-113">**Library:** MSCorEE.dll</span></span>  
  
 <span data-ttu-id="9a00b-114">**Versions du .NET Framework :** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="9a00b-114">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="9a00b-115">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="9a00b-115">See also</span></span>

- [<span data-ttu-id="9a00b-116">Fonctions d’hébergement CLR dépréciées</span><span class="sxs-lookup"><span data-stu-id="9a00b-116">Deprecated CLR Hosting Functions</span></span>](../../../../docs/framework/unmanaged-api/hosting/deprecated-clr-hosting-functions.md)
