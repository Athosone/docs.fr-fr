---
title: Fonction PreBindAssemblyEx
ms.date: 03/30/2017
api_name:
- PreBindAssemblyEx
api_location:
- fusion.dll
api_type:
- DLLExport
f1_keywords:
- PreBindAssemblyEx
helpviewer_keywords:
- PreBindAssemblyEx function [.NET Framework fusion]
ms.assetid: bd285233-a4a2-4b52-bbca-0025a60e4864
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 8251d21fe535f85cc6abd0a7bc6c96ab320007f0
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59090236"
---
# <a name="prebindassemblyex-function"></a><span data-ttu-id="f82e7-102">Fonction PreBindAssemblyEx</span><span class="sxs-lookup"><span data-stu-id="f82e7-102">PreBindAssemblyEx Function</span></span>
<span data-ttu-id="f82e7-103">Obtient le nom complet de la stratégie après d’un assembly.</span><span class="sxs-lookup"><span data-stu-id="f82e7-103">Gets the post-policy display name for an assembly.</span></span>  
  
 <span data-ttu-id="f82e7-104">Cette fonction prend en charge l’infrastructure .NET Framework et n’est pas destinée à être utilisée directement depuis votre code.</span><span class="sxs-lookup"><span data-stu-id="f82e7-104">This function supports the .NET Framework infrastructure and is not intended to be used directly from your code.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="f82e7-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="f82e7-105">Syntax</span></span>  
  
```  
HRESULT PreBindAssemblyEx (  
    [in]  IApplicationContext *pAppCtx,  
    [in]  IAssemblyName       *pName,  
    [in]  IAssembly           *pAsmParent,  
    [in]  LPCWSTR             pwzRuntimeVersion,  
    [out] IAssemblyName       **ppNamePostPolicy,  
    [in]  LPVOID              pvReserved  
 );  
```  
  
## <a name="parameters"></a><span data-ttu-id="f82e7-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="f82e7-106">Parameters</span></span>  
 `pAppCtx`  
 <span data-ttu-id="f82e7-107">[in] Identifie le contexte de l’application.</span><span class="sxs-lookup"><span data-stu-id="f82e7-107">[in] Identifies the application context.</span></span>  
  
 `pName`  
 <span data-ttu-id="f82e7-108">[in] Identifie le nom de l’assembly.</span><span class="sxs-lookup"><span data-stu-id="f82e7-108">[in] Identifies the assembly name.</span></span>  
  
 `pAsmParent`  
 <span data-ttu-id="f82e7-109">[in] Identifie l’assembly parent.</span><span class="sxs-lookup"><span data-stu-id="f82e7-109">[in] Identifies the parent assembly.</span></span> <span data-ttu-id="f82e7-110">Ce paramètre est ignoré.</span><span class="sxs-lookup"><span data-stu-id="f82e7-110">This parameter is ignored.</span></span>  
  
 `pwzRuntimeVersion`  
 <span data-ttu-id="f82e7-111">[in] Identifie la version du runtime.</span><span class="sxs-lookup"><span data-stu-id="f82e7-111">[in] Identifies the runtime version.</span></span>  
  
 `ppNamePostPolicy`  
 <span data-ttu-id="f82e7-112">[out] Contient le nom complet de la stratégie après.</span><span class="sxs-lookup"><span data-stu-id="f82e7-112">[out] Contains the post-policy display name.</span></span>  
  
 `pvReserved`  
 <span data-ttu-id="f82e7-113">[in] Réservé pour une extensibilité future.</span><span class="sxs-lookup"><span data-stu-id="f82e7-113">[in] Reserved for future extensibility.</span></span> <span data-ttu-id="f82e7-114">`pvReserved` doit être une référence null.</span><span class="sxs-lookup"><span data-stu-id="f82e7-114">`pvReserved` must be a null reference.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="f82e7-115">Notes</span><span class="sxs-lookup"><span data-stu-id="f82e7-115">Remarks</span></span>  
 <span data-ttu-id="f82e7-116">Le `ppNamePostPolicy` paramètre de sortie est défini uniquement si la fonction retourne HRESULT FUSION_E_REF_DEF_MISMATCH.</span><span class="sxs-lookup"><span data-stu-id="f82e7-116">The `ppNamePostPolicy` output parameter is set only if the function returns HRESULT FUSION_E_REF_DEF_MISMATCH.</span></span> <span data-ttu-id="f82e7-117">Sinon, elle a la valeur null.</span><span class="sxs-lookup"><span data-stu-id="f82e7-117">Otherwise, it is null.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="f82e7-118">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="f82e7-118">Requirements</span></span>  
 <span data-ttu-id="f82e7-119">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="f82e7-119">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="f82e7-120">**En-tête :** Fusion.h</span><span class="sxs-lookup"><span data-stu-id="f82e7-120">**Header:** Fusion.h</span></span>  
  
 <span data-ttu-id="f82e7-121">**Bibliothèque :** Inclus en tant que ressource dans MsCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="f82e7-121">**Library:** Included as a resource in MsCorEE.dll</span></span>  
  
 <span data-ttu-id="f82e7-122">**Versions du .NET Framework :** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="f82e7-122">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="f82e7-123">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f82e7-123">See also</span></span>

- [<span data-ttu-id="f82e7-124">Fonctions statiques globales de fusion</span><span class="sxs-lookup"><span data-stu-id="f82e7-124">Fusion Global Static Functions</span></span>](../../../../docs/framework/unmanaged-api/fusion/fusion-global-static-functions.md)
