---
title: CertFreeAuthenticodeSignerInfo, fonction
ms.date: 03/30/2017
api_name:
- CertFreeAuthenticodeSignerInfo
api_location:
- clr.dll
api_type:
- DLLExport
ms.assetid: 8029633c-b6e4-4665-a7c2-89607c3247ef
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: bdb764417b757cd7388c49d7e5cac9a960074820
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59142400"
---
# <a name="certfreeauthenticodesignerinfo-function"></a><span data-ttu-id="79c76-102">CertFreeAuthenticodeSignerInfo, fonction</span><span class="sxs-lookup"><span data-stu-id="79c76-102">CertFreeAuthenticodeSignerInfo Function</span></span>
<span data-ttu-id="79c76-103">Libère les ressources allouées pour le [AXL_AUTHENTICODE_SIGNER_INFO](../../../../docs/framework/unmanaged-api/authenticode/axl-authenticode-signer-info-structure.md) structure.</span><span class="sxs-lookup"><span data-stu-id="79c76-103">Frees resources allocated for the [AXL_AUTHENTICODE_SIGNER_INFO](../../../../docs/framework/unmanaged-api/authenticode/axl-authenticode-signer-info-structure.md) structure.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="79c76-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="79c76-104">Syntax</span></span>  
  
```  
HRESULT CertFreeAuthenticodeSignerInfo (  
    [in, out]  PAXL_AUTHENTICODE_SIGNER_INFO   pSignerInfo);  
```  
  
## <a name="parameters"></a><span data-ttu-id="79c76-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="79c76-105">Parameters</span></span>  
 `pSignerInfo`  
 <span data-ttu-id="79c76-106">[en entrée, en sortie] Les informations du signataire à libérer.</span><span class="sxs-lookup"><span data-stu-id="79c76-106">[in, out] Signer information to be released.</span></span> <span data-ttu-id="79c76-107">Consultez le [AXL_AUTHENTICODE_SIGNER_INFO](../../../../docs/framework/unmanaged-api/authenticode/axl-authenticode-signer-info-structure.md) structure.</span><span class="sxs-lookup"><span data-stu-id="79c76-107">See the [AXL_AUTHENTICODE_SIGNER_INFO](../../../../docs/framework/unmanaged-api/authenticode/axl-authenticode-signer-info-structure.md) structure.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="79c76-108">Valeur de retour</span><span class="sxs-lookup"><span data-stu-id="79c76-108">Return Value</span></span>  
 <span data-ttu-id="79c76-109">`S_OK` si la fonction réussit.</span><span class="sxs-lookup"><span data-stu-id="79c76-109">`S_OK` if the function succeeds.</span></span> <span data-ttu-id="79c76-110">Sinon, retourne un code d'erreur.</span><span class="sxs-lookup"><span data-stu-id="79c76-110">Otherwise, returns an error code.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="79c76-111">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="79c76-111">See also</span></span>

- [<span data-ttu-id="79c76-112">Authenticode</span><span class="sxs-lookup"><span data-stu-id="79c76-112">Authenticode</span></span>](../../../../docs/framework/unmanaged-api/authenticode/index.md)
