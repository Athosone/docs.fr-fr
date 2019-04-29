---
title: IMetaDataImport::GetClassLayout, méthode
ms.date: 03/30/2017
api_name:
- IMetaDataImport.GetClassLayout
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IMetaDataImport::GetClassLayout
helpviewer_keywords:
- IMetaDataImport::GetClassLayout method [.NET Framework metadata]
- GetClassLayout method, IMetaDataImport interface [.NET Framework metadata]
ms.assetid: 8f35414d-f40b-4b99-8768-9adb675c622a
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: 11748d3ad99c4050045cce3786eec5604c02ac0f
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61777830"
---
# <a name="imetadataimportgetclasslayout-method"></a><span data-ttu-id="e74c4-102">IMetaDataImport::GetClassLayout, méthode</span><span class="sxs-lookup"><span data-stu-id="e74c4-102">IMetaDataImport::GetClassLayout Method</span></span>
<span data-ttu-id="e74c4-103">Obtient les informations de disposition pour la classe référencée par le jeton TypeDef spécifié.</span><span class="sxs-lookup"><span data-stu-id="e74c4-103">Gets layout information for the class referenced by the specified TypeDef token.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="e74c4-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="e74c4-104">Syntax</span></span>  
  
```  
HRESULT GetClassLayout  (   
   [in]  mdTypeDef          td,   
   [out] DWORD              *pdwPackSize,  
   [out] COR_FIELD_OFFSET   rFieldOffset[],  
   [in]  ULONG              cMax,  
   [out] ULONG              *pcFieldOffset,  
   [out] ULONG              *pulClassSize  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="e74c4-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="e74c4-105">Parameters</span></span>  
 `td`  
 <span data-ttu-id="e74c4-106">[in] Le jeton TypeDef pour la classe avec la mise en page à retourner.</span><span class="sxs-lookup"><span data-stu-id="e74c4-106">[in] The TypeDef token for the class with the layout to return.</span></span>  
  
 `pdwPackSize`  
 <span data-ttu-id="e74c4-107">[out] Une des valeurs 1, 2, 4, 8 ou 16, qui représente la taille de pack de la classe.</span><span class="sxs-lookup"><span data-stu-id="e74c4-107">[out] One of the values 1, 2, 4, 8, or 16, representing the pack size of the class.</span></span>  
  
 `rFieldOffset`  
 <span data-ttu-id="e74c4-108">[out] Un tableau de [COR_FIELD_OFFSET](../../../../docs/framework/unmanaged-api/metadata/cor-field-offset-structure.md) valeurs.</span><span class="sxs-lookup"><span data-stu-id="e74c4-108">[out] An array of [COR_FIELD_OFFSET](../../../../docs/framework/unmanaged-api/metadata/cor-field-offset-structure.md) values.</span></span>  
  
 `cMax`  
 <span data-ttu-id="e74c4-109">[in] Taille maximale du tableau `rFieldOffset`.</span><span class="sxs-lookup"><span data-stu-id="e74c4-109">[in] The maximum size of the `rFieldOffset` array.</span></span>  
  
 `pcFieldOffset`  
 <span data-ttu-id="e74c4-110">[out] Le nombre d’éléments retournés dans `rFieldOffset`.</span><span class="sxs-lookup"><span data-stu-id="e74c4-110">[out] The number of elements returned in `rFieldOffset`.</span></span>  
  
 `pulClassSize`  
 <span data-ttu-id="e74c4-111">[out] La taille en octets de la classe représentée par `td`.</span><span class="sxs-lookup"><span data-stu-id="e74c4-111">[out] The size in bytes of the class represented by `td`.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="e74c4-112">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="e74c4-112">Requirements</span></span>  
 <span data-ttu-id="e74c4-113">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="e74c4-113">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="e74c4-114">**En-tête :** Cor.h</span><span class="sxs-lookup"><span data-stu-id="e74c4-114">**Header:** Cor.h</span></span>  
  
 <span data-ttu-id="e74c4-115">**Bibliothèque :** Inclus en tant que ressource dans MsCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="e74c4-115">**Library:** Included as a resource in MsCorEE.dll</span></span>  
  
 <span data-ttu-id="e74c4-116">**Versions du .NET Framework :** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="e74c4-116">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="e74c4-117">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e74c4-117">See also</span></span>

- [<span data-ttu-id="e74c4-118">IMetaDataImport, interface</span><span class="sxs-lookup"><span data-stu-id="e74c4-118">IMetaDataImport Interface</span></span>](../../../../docs/framework/unmanaged-api/metadata/imetadataimport-interface.md)
- [<span data-ttu-id="e74c4-119">IMetaDataImport2, interface</span><span class="sxs-lookup"><span data-stu-id="e74c4-119">IMetaDataImport2 Interface</span></span>](../../../../docs/framework/unmanaged-api/metadata/imetadataimport2-interface.md)
