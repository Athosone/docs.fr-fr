---
title: IMetaDataTables::GetTableInfo, méthode
ms.date: 03/30/2017
api_name:
- IMetaDataTables.GetTableInfo
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IMetaDataTables::GetTableInfo
helpviewer_keywords:
- IMetaDataTables::GetTableInfo method [.NET Framework metadata]
- GetTableInfo method [.NET Framework metadata]
ms.assetid: 50cbe557-2322-41aa-8e0d-f967602eaa0f
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: 82c88c75d5799134d8c683c91e28f956743b84ba
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61992223"
---
# <a name="imetadatatablesgettableinfo-method"></a><span data-ttu-id="031ac-102">IMetaDataTables::GetTableInfo, méthode</span><span class="sxs-lookup"><span data-stu-id="031ac-102">IMetaDataTables::GetTableInfo Method</span></span>
<span data-ttu-id="031ac-103">Obtient le nom, la taille de ligne, le nombre de lignes, le nombre de colonnes et index de colonne clé de la table spécifiée.</span><span class="sxs-lookup"><span data-stu-id="031ac-103">Gets the name, row size, number of rows, number of columns, and key column index of the specified table.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="031ac-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="031ac-104">Syntax</span></span>  
  
```  
HRESULT GetTableInfo (  
    [in]  ULONG       ixTbl,  
    [out] ULONG       *pcbRow,  
    [out] ULONG       *pcRows,  
    [out] ULONG       *pcCols,  
    [out] ULONG       *piKey,  
    [out] const char  **ppName  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="031ac-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="031ac-105">Parameters</span></span>  
 `ixTbl`  
 <span data-ttu-id="031ac-106">[in] L’identificateur de la table dont les propriétés à retourner.</span><span class="sxs-lookup"><span data-stu-id="031ac-106">[in] The identifier of the table whose properties to return.</span></span>  
  
 `pcbRow`  
 <span data-ttu-id="031ac-107">[out] Pointeur vers la taille, en octets, d’une ligne de table.</span><span class="sxs-lookup"><span data-stu-id="031ac-107">[out] A pointer to the size, in bytes, of a table row.</span></span>  
  
 `pcRows`  
 <span data-ttu-id="031ac-108">[out] Pointeur vers le nombre de lignes dans la table.</span><span class="sxs-lookup"><span data-stu-id="031ac-108">[out] A pointer to the number of rows in the table.</span></span>  
  
 `pcCols`  
 <span data-ttu-id="031ac-109">[out] Pointeur vers le nombre de colonnes dans la table.</span><span class="sxs-lookup"><span data-stu-id="031ac-109">[out] A pointer to the number of columns in the table.</span></span>  
  
 `piKey`  
 <span data-ttu-id="031ac-110">[out] Pointeur vers l’index de la colonne clé, ou -1 si la table ne comporte aucune colonne clé.</span><span class="sxs-lookup"><span data-stu-id="031ac-110">[out] A pointer to the index of the key column, or -1 if the table has no key column.</span></span>  
  
 `ppName`  
 <span data-ttu-id="031ac-111">[out] Pointeur vers un pointeur vers le nom de table.</span><span class="sxs-lookup"><span data-stu-id="031ac-111">[out] A pointer to a pointer to the table name.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="031ac-112">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="031ac-112">Requirements</span></span>  
 <span data-ttu-id="031ac-113">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="031ac-113">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="031ac-114">**En-tête :** Cor.h</span><span class="sxs-lookup"><span data-stu-id="031ac-114">**Header:** Cor.h</span></span>  
  
 <span data-ttu-id="031ac-115">**Bibliothèque :** Utilisé en tant que ressource dans MsCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="031ac-115">**Library:** Used as a resource in MsCorEE.dll</span></span>  
  
 <span data-ttu-id="031ac-116">**Versions du .NET Framework :** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="031ac-116">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="031ac-117">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="031ac-117">See also</span></span>

- [<span data-ttu-id="031ac-118">IMetaDataTables, interface</span><span class="sxs-lookup"><span data-stu-id="031ac-118">IMetaDataTables Interface</span></span>](../../../../docs/framework/unmanaged-api/metadata/imetadatatables-interface.md)
- [<span data-ttu-id="031ac-119">IMetaDataTables2, interface</span><span class="sxs-lookup"><span data-stu-id="031ac-119">IMetaDataTables2 Interface</span></span>](../../../../docs/framework/unmanaged-api/metadata/imetadatatables2-interface.md)
