---
title: IMetaDataImport::GetNestedClassProps, méthode
ms.date: 03/30/2017
api_name:
- IMetaDataImport.GetNestedClassProps
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IMetaDataImport::GetNestedClassProps
helpviewer_keywords:
- GetNestedClassProps method [.NET Framework metadata]
- IMetaDataImport::GetNestedClassProps method [.NET Framework metadata]
ms.assetid: 704d19f1-bdef-4745-af8c-6476eb246fb3
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: eb5820087001a207af0c2552f91b4c17f5f78ff7
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61777648"
---
# <a name="imetadataimportgetnestedclassprops-method"></a><span data-ttu-id="730b4-102">IMetaDataImport::GetNestedClassProps, méthode</span><span class="sxs-lookup"><span data-stu-id="730b4-102">IMetaDataImport::GetNestedClassProps Method</span></span>
<span data-ttu-id="730b4-103">Obtient le jeton TypeDef pour le parent <xref:System.Type> du type imbriqué.</span><span class="sxs-lookup"><span data-stu-id="730b4-103">Gets the TypeDef token for the parent <xref:System.Type> of the specified nested type.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="730b4-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="730b4-104">Syntax</span></span>  
  
```  
HRESULT GetNestedClassProps (  
   [in]   mdTypeDef      tdNestedClass,  
   [out]  mdTypeDef      *ptdEnclosingClass  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="730b4-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="730b4-105">Parameters</span></span>  
 `tdNestedClass`  
 <span data-ttu-id="730b4-106">[in] Jeton TypeDef représentant le <xref:System.Type> pour renvoyer la classe parente jeton pour.</span><span class="sxs-lookup"><span data-stu-id="730b4-106">[in] A TypeDef token representing the <xref:System.Type> to return the parent class token for.</span></span>  
  
 `ptdEnclosingClass`  
 <span data-ttu-id="730b4-107">[out] Un pointeur vers le jeton TypeDef pour le <xref:System.Type> qui `tdNestedClass` est imbriqué dans.</span><span class="sxs-lookup"><span data-stu-id="730b4-107">[out] A pointer to the TypeDef token for the <xref:System.Type> that `tdNestedClass` is nested in.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="730b4-108">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="730b4-108">Requirements</span></span>  
 <span data-ttu-id="730b4-109">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="730b4-109">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="730b4-110">**En-tête :** Cor.h</span><span class="sxs-lookup"><span data-stu-id="730b4-110">**Header:** Cor.h</span></span>  
  
 <span data-ttu-id="730b4-111">**Bibliothèque :** Inclus en tant que ressource dans MsCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="730b4-111">**Library:** Included as a resource in MsCorEE.dll</span></span>  
  
 <span data-ttu-id="730b4-112">**Versions du .NET Framework :** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="730b4-112">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="730b4-113">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="730b4-113">See also</span></span>

- [<span data-ttu-id="730b4-114">IMetaDataImport, interface</span><span class="sxs-lookup"><span data-stu-id="730b4-114">IMetaDataImport Interface</span></span>](../../../../docs/framework/unmanaged-api/metadata/imetadataimport-interface.md)
- [<span data-ttu-id="730b4-115">IMetaDataImport2, interface</span><span class="sxs-lookup"><span data-stu-id="730b4-115">IMetaDataImport2 Interface</span></span>](../../../../docs/framework/unmanaged-api/metadata/imetadataimport2-interface.md)
