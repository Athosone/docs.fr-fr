---
title: IMetaDataImport::EnumSignatures, méthode
ms.date: 03/30/2017
api_name:
- IMetaDataImport.EnumSignatures
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IMetaDataImport::EnumSignatures
helpviewer_keywords:
- EnumSignatures method [.NET Framework metadata]
- IMetaDataImport::EnumSignatures method [.NET Framework metadata]
ms.assetid: d0d65060-6f90-42a2-95cf-6ffb04352996
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: 193abe173b259ff2679642e229fce96151e37872
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61992301"
---
# <a name="imetadataimportenumsignatures-method"></a><span data-ttu-id="5dcd8-102">IMetaDataImport::EnumSignatures, méthode</span><span class="sxs-lookup"><span data-stu-id="5dcd8-102">IMetaDataImport::EnumSignatures Method</span></span>
<span data-ttu-id="5dcd8-103">Énumère les jetons Signature représentant des signatures autonomes dans la portée actuelle.</span><span class="sxs-lookup"><span data-stu-id="5dcd8-103">Enumerates Signature tokens representing stand-alone signatures in the current scope.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="5dcd8-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="5dcd8-104">Syntax</span></span>  
  
```  
HRESULT EnumSignatures (  
   [in, out] HCORENUM     *phEnum,  
   [out]     mdSignature  rSignatures[],  
   [in]      ULONG        cMax,  
   [out]     ULONG        *pcSignatures  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="5dcd8-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="5dcd8-105">Parameters</span></span>  
 `phEnum`  
 <span data-ttu-id="5dcd8-106">[in, out] Pointeur vers l’énumérateur.</span><span class="sxs-lookup"><span data-stu-id="5dcd8-106">[in, out] A pointer to the enumerator.</span></span> <span data-ttu-id="5dcd8-107">Cela doit être NULL pour le premier appel de cette méthode.</span><span class="sxs-lookup"><span data-stu-id="5dcd8-107">This must be NULL for the first call of this method.</span></span>  
  
 `rSignatures`  
 <span data-ttu-id="5dcd8-108">[out] Tableau utilisé pour stocker les jetons de Signature.</span><span class="sxs-lookup"><span data-stu-id="5dcd8-108">[out] The array used to store the Signature tokens.</span></span>  
  
 `cMax`  
 <span data-ttu-id="5dcd8-109">[in] Taille maximale du tableau `rSignatures`.</span><span class="sxs-lookup"><span data-stu-id="5dcd8-109">[in] The maximum size of the `rSignatures` array.</span></span>  
  
 `pcSignatures`  
 <span data-ttu-id="5dcd8-110">[out] Le nombre de jetons Signature retournés dans `rSignatures`.</span><span class="sxs-lookup"><span data-stu-id="5dcd8-110">[out] The number of Signature tokens returned in `rSignatures`.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="5dcd8-111">Valeur de retour</span><span class="sxs-lookup"><span data-stu-id="5dcd8-111">Return Value</span></span>  
  
|<span data-ttu-id="5dcd8-112">HRESULT</span><span class="sxs-lookup"><span data-stu-id="5dcd8-112">HRESULT</span></span>|<span data-ttu-id="5dcd8-113">Description</span><span class="sxs-lookup"><span data-stu-id="5dcd8-113">Description</span></span>|  
|-------------|-----------------|  
|`S_OK`|<span data-ttu-id="5dcd8-114">`EnumSignatures` retourné avec succès.</span><span class="sxs-lookup"><span data-stu-id="5dcd8-114">`EnumSignatures` returned successfully.</span></span>|  
|`S_FALSE`|<span data-ttu-id="5dcd8-115">Il n’existe pas de jetons à énumérer.</span><span class="sxs-lookup"><span data-stu-id="5dcd8-115">There are no tokens to enumerate.</span></span> <span data-ttu-id="5dcd8-116">Dans ce cas, `pcSignatures` est égal à zéro.</span><span class="sxs-lookup"><span data-stu-id="5dcd8-116">In that case, `pcSignatures` is zero.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="5dcd8-117">Notes</span><span class="sxs-lookup"><span data-stu-id="5dcd8-117">Remarks</span></span>  
 <span data-ttu-id="5dcd8-118">Les jetons de Signature sont créés par le [IMetaDataEmit::GetTokenFromSig](../../../../docs/framework/unmanaged-api/metadata/imetadataemit-gettokenfromsig-method.md) (méthode).</span><span class="sxs-lookup"><span data-stu-id="5dcd8-118">The Signature tokens are created by the [IMetaDataEmit::GetTokenFromSig](../../../../docs/framework/unmanaged-api/metadata/imetadataemit-gettokenfromsig-method.md) method.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="5dcd8-119">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="5dcd8-119">Requirements</span></span>  
 <span data-ttu-id="5dcd8-120">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="5dcd8-120">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="5dcd8-121">**En-tête :** Cor.h</span><span class="sxs-lookup"><span data-stu-id="5dcd8-121">**Header:** Cor.h</span></span>  
  
 <span data-ttu-id="5dcd8-122">**Bibliothèque :** Inclus en tant que ressource dans MsCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="5dcd8-122">**Library:** Included as a resource in MsCorEE.dll</span></span>  
  
 <span data-ttu-id="5dcd8-123">**Versions du .NET Framework :** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="5dcd8-123">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="5dcd8-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="5dcd8-124">See also</span></span>

- [<span data-ttu-id="5dcd8-125">IMetaDataImport, interface</span><span class="sxs-lookup"><span data-stu-id="5dcd8-125">IMetaDataImport Interface</span></span>](../../../../docs/framework/unmanaged-api/metadata/imetadataimport-interface.md)
- [<span data-ttu-id="5dcd8-126">IMetaDataImport2, interface</span><span class="sxs-lookup"><span data-stu-id="5dcd8-126">IMetaDataImport2 Interface</span></span>](../../../../docs/framework/unmanaged-api/metadata/imetadataimport2-interface.md)
