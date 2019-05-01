---
title: IMetaDataImport2::GetGenericParamConstraintProps, méthode
ms.date: 03/30/2017
api_name:
- IMetaDataImport2.GetGenericParamConstraintProps
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IMetaDataImport2::GetGenericParamConstraintProps
helpviewer_keywords:
- IMetaDataImport2::GetGenericParamConstraintProps method [.NET Framework metadata]
- GetGenericParamConstraintProps method [.NET Framework metadata]
ms.assetid: c5fee4a0-b132-4e5e-8730-e586ce314b9a
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: e0503c5bd924793df8143c89e358618fb8844c6c
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62049867"
---
# <a name="imetadataimport2getgenericparamconstraintprops-method"></a><span data-ttu-id="ae4c7-102">IMetaDataImport2::GetGenericParamConstraintProps, méthode</span><span class="sxs-lookup"><span data-stu-id="ae4c7-102">IMetaDataImport2::GetGenericParamConstraintProps Method</span></span>
<span data-ttu-id="ae4c7-103">Obtient les métadonnées associées à la contrainte de paramètre générique représentée par le jeton de la contrainte spécifiée.</span><span class="sxs-lookup"><span data-stu-id="ae4c7-103">Gets the metadata associated with the generic parameter constraint represented by the specified constraint token.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="ae4c7-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="ae4c7-104">Syntax</span></span>  
  
```  
HRESULT GetGenericParamConstraintProps (  
   [in]  mdGenericParamConstraint  gpc,  
   [out] mdGenericParam            *ptGenericParam,  
   [out] mdToken                   *ptkConstraintType  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="ae4c7-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="ae4c7-105">Parameters</span></span>  
 `gpc`  
 <span data-ttu-id="ae4c7-106">[in] Le jeton à la contrainte de paramètre générique pour lequel retourner les métadonnées.</span><span class="sxs-lookup"><span data-stu-id="ae4c7-106">[in] The token to the generic parameter constraint for which to return the metadata.</span></span>  
  
 `ptGenericParam`  
 <span data-ttu-id="ae4c7-107">[out] Pointeur vers le jeton qui représente le paramètre générique est contraint.</span><span class="sxs-lookup"><span data-stu-id="ae4c7-107">[out] A pointer to the token that represents the generic parameter that is constrained.</span></span>  
  
 `ptkConstraintType`  
 <span data-ttu-id="ae4c7-108">[out] Un pointeur vers un jeton TypeDef, TypeRef ou TypeSpec qui représente une contrainte sur `ptGenericParam`.</span><span class="sxs-lookup"><span data-stu-id="ae4c7-108">[out] A pointer to a TypeDef, TypeRef, or TypeSpec token that represents a constraint on `ptGenericParam`.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="ae4c7-109">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="ae4c7-109">Requirements</span></span>  
 <span data-ttu-id="ae4c7-110">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="ae4c7-110">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="ae4c7-111">**En-tête :** Cor.h</span><span class="sxs-lookup"><span data-stu-id="ae4c7-111">**Header:** Cor.h</span></span>  
  
 <span data-ttu-id="ae4c7-112">**Bibliothèque :** Utilisé en tant que ressource dans MsCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="ae4c7-112">**Library:** Used as a resource in MsCorEE.dll</span></span>  
  
 <span data-ttu-id="ae4c7-113">**Versions du .NET Framework :** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="ae4c7-113">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="ae4c7-114">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ae4c7-114">See also</span></span>

- [<span data-ttu-id="ae4c7-115">IMetaDataImport2, interface</span><span class="sxs-lookup"><span data-stu-id="ae4c7-115">IMetaDataImport2 Interface</span></span>](../../../../docs/framework/unmanaged-api/metadata/imetadataimport2-interface.md)
- [<span data-ttu-id="ae4c7-116">IMetaDataImport, interface</span><span class="sxs-lookup"><span data-stu-id="ae4c7-116">IMetaDataImport Interface</span></span>](../../../../docs/framework/unmanaged-api/metadata/imetadataimport-interface.md)
