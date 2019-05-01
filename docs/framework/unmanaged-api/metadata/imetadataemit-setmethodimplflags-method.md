---
title: IMetaDataEmit::SetMethodImplFlags, méthode
ms.date: 03/30/2017
api_name:
- IMetaDataEmit.SetMethodImplFlags
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IMetaDataEmit::SetMethodImplFlags
helpviewer_keywords:
- IMetaDataEmit::SetMethodImplFlags method [.NET Framework metadata]
- SetMethodImpFlags method [.NET Framework metadata]
ms.assetid: 4bc82d9b-9544-4be3-ba51-a2d4d806158a
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: 28c0aa37bdcae2a09a4d53f920efd3ffe7117bd3
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61992457"
---
# <a name="imetadataemitsetmethodimplflags-method"></a><span data-ttu-id="8f0a2-102">IMetaDataEmit::SetMethodImplFlags, méthode</span><span class="sxs-lookup"><span data-stu-id="8f0a2-102">IMetaDataEmit::SetMethodImplFlags Method</span></span>
<span data-ttu-id="8f0a2-103">Définit ou met à jour de la signature de métadonnées de l’implémentation de méthode héritée qui est référencée par le jeton spécifié.</span><span class="sxs-lookup"><span data-stu-id="8f0a2-103">Sets or updates the metadata signature of the inherited method implementation that is referenced by the specified token.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="8f0a2-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="8f0a2-104">Syntax</span></span>  
  
```  
HRESULT SetMethodImplFlags (   
    [in]  mdMethodDef   md,   
    [in]  DWORD         dwImplFlags   
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="8f0a2-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="8f0a2-105">Parameters</span></span>  
 `md`  
 <span data-ttu-id="8f0a2-106">[in] Le jeton pour la méthode à modifier.</span><span class="sxs-lookup"><span data-stu-id="8f0a2-106">[in] The token for the method to be changed.</span></span>  
  
 `dwImplFlags`  
 <span data-ttu-id="8f0a2-107">[in] Une combinaison des valeurs de la [CorMethodImpl](../../../../docs/framework/unmanaged-api/metadata/cormethodimpl-enumeration.md) énumération qui spécifie les fonctionnalités d’implémentation de méthode.</span><span class="sxs-lookup"><span data-stu-id="8f0a2-107">[in] A combination of the values of the [CorMethodImpl](../../../../docs/framework/unmanaged-api/metadata/cormethodimpl-enumeration.md) enumeration that specifies the method implementation features.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="8f0a2-108">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="8f0a2-108">Requirements</span></span>  
 <span data-ttu-id="8f0a2-109">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="8f0a2-109">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="8f0a2-110">**En-tête :** Cor.h</span><span class="sxs-lookup"><span data-stu-id="8f0a2-110">**Header:** Cor.h</span></span>  
  
 <span data-ttu-id="8f0a2-111">**Bibliothèque :** Utilisé en tant que ressource dans MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="8f0a2-111">**Library:** Used as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="8f0a2-112">**Versions du .NET Framework :** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="8f0a2-112">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="8f0a2-113">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="8f0a2-113">See also</span></span>

- [<span data-ttu-id="8f0a2-114">IMetaDataEmit, interface</span><span class="sxs-lookup"><span data-stu-id="8f0a2-114">IMetaDataEmit Interface</span></span>](../../../../docs/framework/unmanaged-api/metadata/imetadataemit-interface.md)
- [<span data-ttu-id="8f0a2-115">IMetaDataEmit2, interface</span><span class="sxs-lookup"><span data-stu-id="8f0a2-115">IMetaDataEmit2 Interface</span></span>](../../../../docs/framework/unmanaged-api/metadata/imetadataemit2-interface.md)
