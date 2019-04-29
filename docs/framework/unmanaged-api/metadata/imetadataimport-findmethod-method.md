---
title: IMetaDataImport::FindMethod, méthode
ms.date: 03/30/2017
api_name:
- IMetaDataImport.FindMethod
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IMetaDataImport::FindMethod
helpviewer_keywords:
- FindMethod method [.NET Framework metadata]
- IMetaDataImport::FindMethod method [.NET Framework metadata]
ms.assetid: 0f9bde1d-e306-438d-941b-d0925b322304
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: 28aa8313e7ba0c071187d0f1f6d78431b16fc005
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61777869"
---
# <a name="imetadataimportfindmethod-method"></a><span data-ttu-id="5d2a8-102">IMetaDataImport::FindMethod, méthode</span><span class="sxs-lookup"><span data-stu-id="5d2a8-102">IMetaDataImport::FindMethod Method</span></span>
<span data-ttu-id="5d2a8-103">Obtient un pointeur vers le MethodDef jeton pour la méthode qui est comprise par le <xref:System.Type> et qui a la signature de nom et de métadonnées spécifiée.</span><span class="sxs-lookup"><span data-stu-id="5d2a8-103">Gets a pointer to the MethodDef token for the method that is enclosed by the specified <xref:System.Type> and that has the specified name and metadata signature.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="5d2a8-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="5d2a8-104">Syntax</span></span>  
  
```  
HRESULT FindMethod (  
   [in]  mdTypeDef          td,  
   [in]  LPCWSTR            szName,   
   [in]  PCCOR_SIGNATURE    pvSigBlob,   
   [in]  ULONG              cbSigBlob,   
   [out] mdMethodDef        *pmb  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="5d2a8-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="5d2a8-105">Parameters</span></span>  
 `td`  
 <span data-ttu-id="5d2a8-106">[in] Le `mdTypeDef` jeton pour le type (classe ou interface) qui encadre le membre à rechercher.</span><span class="sxs-lookup"><span data-stu-id="5d2a8-106">[in] The `mdTypeDef` token for the type (a class or interface) that encloses the member to search for.</span></span> <span data-ttu-id="5d2a8-107">Si cette valeur est `mdTokenNil`, puis la recherche est effectuée pour une fonction globale.</span><span class="sxs-lookup"><span data-stu-id="5d2a8-107">If this value is `mdTokenNil`, then the lookup is done for a global function.</span></span>  
  
 `szName`  
 <span data-ttu-id="5d2a8-108">[in] Le nom de la méthode à rechercher.</span><span class="sxs-lookup"><span data-stu-id="5d2a8-108">[in] The name of the method to search for.</span></span>  
  
 `pvSigBlob`  
 <span data-ttu-id="5d2a8-109">[in] Pointeur vers la signature de métadonnées binaires de la méthode.</span><span class="sxs-lookup"><span data-stu-id="5d2a8-109">[in] A pointer to the binary metadata signature of the method.</span></span>  
  
 `cbSigBlob`  
 <span data-ttu-id="5d2a8-110">[in] La taille en octets de `pvSigBlob`.</span><span class="sxs-lookup"><span data-stu-id="5d2a8-110">[in] The size in bytes of `pvSigBlob`.</span></span>  
  
 `pmb`  
 <span data-ttu-id="5d2a8-111">[out] Pointeur vers le jeton MethodDef correspondant.</span><span class="sxs-lookup"><span data-stu-id="5d2a8-111">[out] A pointer to the matching MethodDef token.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="5d2a8-112">Notes</span><span class="sxs-lookup"><span data-stu-id="5d2a8-112">Remarks</span></span>  
 <span data-ttu-id="5d2a8-113">Vous spécifiez la méthode à l’aide de son interface ou la classe englobante (`td`), son nom (`szName`) et éventuellement sa signature (`pvSigBlob`).</span><span class="sxs-lookup"><span data-stu-id="5d2a8-113">You specify the method using its enclosing class or interface (`td`), its name (`szName`), and optionally its signature (`pvSigBlob`).</span></span> <span data-ttu-id="5d2a8-114">Il existe peut-être plusieurs méthodes portant le même nom dans une classe ou interface.</span><span class="sxs-lookup"><span data-stu-id="5d2a8-114">There might be multiple methods with the same name in a class or interface.</span></span> <span data-ttu-id="5d2a8-115">Dans ce cas, passez signature de la méthode pour rechercher la correspondance unique.</span><span class="sxs-lookup"><span data-stu-id="5d2a8-115">In that case, pass the method's signature to find the unique match.</span></span>  
  
 <span data-ttu-id="5d2a8-116">La signature est passé à `FindMethod` doit avoir été générée dans la portée actuelle, car les signatures sont liées à une étendue spécifique.</span><span class="sxs-lookup"><span data-stu-id="5d2a8-116">The signature passed to `FindMethod` must have been generated in the current scope, because signatures are bound to a particular scope.</span></span> <span data-ttu-id="5d2a8-117">Une signature peut incorporer un jeton qui identifie le type de valeur ou de la classe englobant.</span><span class="sxs-lookup"><span data-stu-id="5d2a8-117">A signature can embed a token that identifies the enclosing class or value type.</span></span> <span data-ttu-id="5d2a8-118">Le jeton est un index dans la table TypeDef local.</span><span class="sxs-lookup"><span data-stu-id="5d2a8-118">The token is an index into the local TypeDef table.</span></span> <span data-ttu-id="5d2a8-119">Vous ne pouvez pas générer une signature d’exécution en dehors du contexte de la portée actuelle et utiliser cette signature comme entrée `FindMethod`.</span><span class="sxs-lookup"><span data-stu-id="5d2a8-119">You cannot build a run-time signature outside the context of the current scope and use that signature as input to input to `FindMethod`.</span></span>  
  
 <span data-ttu-id="5d2a8-120">`FindMethod` recherche uniquement les méthodes qui ont été définis directement dans la classe ou interface ; Il ne trouve pas de méthodes héritées.</span><span class="sxs-lookup"><span data-stu-id="5d2a8-120">`FindMethod` finds only methods that were defined directly in the class or interface; it does not find inherited methods.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="5d2a8-121">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="5d2a8-121">Requirements</span></span>  
 <span data-ttu-id="5d2a8-122">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="5d2a8-122">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="5d2a8-123">**En-tête :** Cor.h</span><span class="sxs-lookup"><span data-stu-id="5d2a8-123">**Header:** Cor.h</span></span>  
  
 <span data-ttu-id="5d2a8-124">**Bibliothèque :** Inclus en tant que ressource dans MsCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="5d2a8-124">**Library:** Included as a resource in MsCorEE.dll</span></span>  
  
 <span data-ttu-id="5d2a8-125">**Versions du .NET Framework :** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="5d2a8-125">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="5d2a8-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="5d2a8-126">See also</span></span>

- <xref:System.Reflection.MethodInfo>
- [<span data-ttu-id="5d2a8-127">IMetaDataImport, interface</span><span class="sxs-lookup"><span data-stu-id="5d2a8-127">IMetaDataImport Interface</span></span>](../../../../docs/framework/unmanaged-api/metadata/imetadataimport-interface.md)
- [<span data-ttu-id="5d2a8-128">IMetaDataImport2, interface</span><span class="sxs-lookup"><span data-stu-id="5d2a8-128">IMetaDataImport2 Interface</span></span>](../../../../docs/framework/unmanaged-api/metadata/imetadataimport2-interface.md)
