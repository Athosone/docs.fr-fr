---
title: IMetaDataImport2::GetGenericParamProps, méthode
ms.date: 03/30/2017
api_name:
- IMetaDataImport2.GetGenericParamProps
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IMetaDataImport2::GetGenericParamProps
helpviewer_keywords:
- IMetaDataImport2::GetGenericParamProps method [.NET Framework metadata]
- GetGenericParamProps method [.NET Framework metadata]
ms.assetid: dbb21e67-712b-49e7-a27c-a1e73ffd46c5
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: 55a765fe3942cbf71a8460187e829dc7f3ca877e
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59082332"
---
# <a name="imetadataimport2getgenericparamprops-method"></a><span data-ttu-id="ba94a-102">IMetaDataImport2::GetGenericParamProps, méthode</span><span class="sxs-lookup"><span data-stu-id="ba94a-102">IMetaDataImport2::GetGenericParamProps Method</span></span>
<span data-ttu-id="ba94a-103">Obtient les métadonnées associées au paramètre générique représenté par le jeton spécifié.</span><span class="sxs-lookup"><span data-stu-id="ba94a-103">Gets the metadata associated with the generic parameter represented by the specified token.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="ba94a-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="ba94a-104">Syntax</span></span>  
  
```  
HRESULT GetGenericParamProps (  
   [in]  mdGenericParam  gp,  
   [out] ULONG           *pulParamSeq,  
   [out] DWORD           *pdwParamFlags,  
   [out] mdToken         *ptOwner,  
   [out] DWORD           *reserved,  
   [out] LPWSTR          wzName,  
   [in]  ULONG           cchName,  
   [out] ULONG           *pchName  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="ba94a-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="ba94a-105">Parameters</span></span>  
 `gp`  
 <span data-ttu-id="ba94a-106">[in] Le jeton qui représente le paramètre générique pour lequel retourner les métadonnées.</span><span class="sxs-lookup"><span data-stu-id="ba94a-106">[in] The token that represents the generic parameter for which to return metadata.</span></span>  
  
 `pulParamSeq`  
 <span data-ttu-id="ba94a-107">[out] La position ordinale de la `Type` paramètre dans le constructeur parent ou la méthode.</span><span class="sxs-lookup"><span data-stu-id="ba94a-107">[out] The ordinal position of the `Type` parameter in the parent constructor or method.</span></span>  
  
 `pdwParamFlags`  
 <span data-ttu-id="ba94a-108">[out] Une valeur de la [CorGenericParamAttr](../../../../docs/framework/unmanaged-api/metadata/corgenericparamattr-enumeration.md) énumération qui décrit le `Type` pour le paramètre générique.</span><span class="sxs-lookup"><span data-stu-id="ba94a-108">[out] A value of the [CorGenericParamAttr](../../../../docs/framework/unmanaged-api/metadata/corgenericparamattr-enumeration.md) enumeration that describes the `Type` for the generic parameter.</span></span>  
  
 `ptOwner`  
 <span data-ttu-id="ba94a-109">[out] Jeton TypeDef ou MethodDef qui représente le propriétaire du paramètre.</span><span class="sxs-lookup"><span data-stu-id="ba94a-109">[out] A TypeDef or MethodDef token that represents the owner of the parameter.</span></span>  
  
 `reserved`  
 <span data-ttu-id="ba94a-110">[out] Réservé pour une extensibilité future.</span><span class="sxs-lookup"><span data-stu-id="ba94a-110">[out] Reserved for future extensibility.</span></span>  
  
 `wzName`  
 <span data-ttu-id="ba94a-111">[out] Le nom du paramètre générique.</span><span class="sxs-lookup"><span data-stu-id="ba94a-111">[out] The name of the generic parameter.</span></span>  
  
 `cchName`  
 <span data-ttu-id="ba94a-112">[in] La taille de la `wzName` mémoire tampon.</span><span class="sxs-lookup"><span data-stu-id="ba94a-112">[in] The size of the `wzName` buffer.</span></span>  
  
 `pchName`  
 <span data-ttu-id="ba94a-113">[out] La taille retournée du nom, en caractères larges.</span><span class="sxs-lookup"><span data-stu-id="ba94a-113">[out] The returned size of the name, in wide characters.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="ba94a-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="ba94a-114">Requirements</span></span>  
 <span data-ttu-id="ba94a-115">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="ba94a-115">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="ba94a-116">**En-tête :** Cor.h</span><span class="sxs-lookup"><span data-stu-id="ba94a-116">**Header:** Cor.h</span></span>  
  
 <span data-ttu-id="ba94a-117">**Bibliothèque :** Utilisé en tant que ressource dans MsCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="ba94a-117">**Library:** Used as a resource in MsCorEE.dll</span></span>  
  
 <span data-ttu-id="ba94a-118">**Versions du .NET Framework :** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="ba94a-118">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="ba94a-119">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ba94a-119">See also</span></span>

- [<span data-ttu-id="ba94a-120">IMetaDataImport2, interface</span><span class="sxs-lookup"><span data-stu-id="ba94a-120">IMetaDataImport2 Interface</span></span>](../../../../docs/framework/unmanaged-api/metadata/imetadataimport2-interface.md)
- [<span data-ttu-id="ba94a-121">IMetaDataImport, interface</span><span class="sxs-lookup"><span data-stu-id="ba94a-121">IMetaDataImport Interface</span></span>](../../../../docs/framework/unmanaged-api/metadata/imetadataimport-interface.md)
