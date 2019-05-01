---
title: IMetaDataTables::GetBlob, méthode
ms.date: 03/30/2017
api_name:
- IMetaDataTables.GetBlob
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IMetaDataTables::GetBlob
helpviewer_keywords:
- GetBlob method [.NET Framework metadata]
- IMetaDataTables::GetBlob method [.NET Framework metadata]
ms.assetid: 94667c1c-6d58-4aa7-b74e-530b11e2a276
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: babe098b16729cfcd41b48075a49b9ae9be7dfdc
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62049802"
---
# <a name="imetadatatablesgetblob-method"></a><span data-ttu-id="4379c-102">IMetaDataTables::GetBlob, méthode</span><span class="sxs-lookup"><span data-stu-id="4379c-102">IMetaDataTables::GetBlob Method</span></span>
<span data-ttu-id="4379c-103">Obtient un pointeur vers l’objet binaire volumineux (BLOB) à l’index de colonne spécifiée.</span><span class="sxs-lookup"><span data-stu-id="4379c-103">Gets a pointer to the binary large object (BLOB) at the specified column index.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="4379c-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="4379c-104">Syntax</span></span>  
  
```  
HRESULT GetBlob (  
    [in]  ULONG          ixBlob,  
    [out] ULONG          *pcbData,  
    [out] const void     **ppData  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="4379c-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="4379c-105">Parameters</span></span>  
 `ixBlob`  
 <span data-ttu-id="4379c-106">[in] L’adresse mémoire à partir duquel obtenir `ppData`.</span><span class="sxs-lookup"><span data-stu-id="4379c-106">[in] The memory address from which to get `ppData`.</span></span>  
  
 `pcbData`  
 <span data-ttu-id="4379c-107">[out] Un pointeur vers la taille, en octets, de `ppData`.</span><span class="sxs-lookup"><span data-stu-id="4379c-107">[out] A pointer to the size, in bytes, of `ppData`.</span></span>  
  
 `ppData`  
 <span data-ttu-id="4379c-108">[out] Un pointeur vers un pointeur vers les données binaires récupérées.</span><span class="sxs-lookup"><span data-stu-id="4379c-108">[out] A pointer to a pointer to the binary data retrieved.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="4379c-109">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="4379c-109">Requirements</span></span>  
 <span data-ttu-id="4379c-110">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="4379c-110">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="4379c-111">**En-tête :** Cor.h</span><span class="sxs-lookup"><span data-stu-id="4379c-111">**Header:** Cor.h</span></span>  
  
 <span data-ttu-id="4379c-112">**Bibliothèque :** Utilisé en tant que ressource dans MsCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="4379c-112">**Library:** Used as a resource in MsCorEE.dll</span></span>  
  
 <span data-ttu-id="4379c-113">**Versions du .NET Framework :** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="4379c-113">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="4379c-114">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="4379c-114">See also</span></span>

- [<span data-ttu-id="4379c-115">IMetaDataTables, interface</span><span class="sxs-lookup"><span data-stu-id="4379c-115">IMetaDataTables Interface</span></span>](../../../../docs/framework/unmanaged-api/metadata/imetadatatables-interface.md)
- [<span data-ttu-id="4379c-116">IMetaDataTables2, interface</span><span class="sxs-lookup"><span data-stu-id="4379c-116">IMetaDataTables2 Interface</span></span>](../../../../docs/framework/unmanaged-api/metadata/imetadatatables2-interface.md)
