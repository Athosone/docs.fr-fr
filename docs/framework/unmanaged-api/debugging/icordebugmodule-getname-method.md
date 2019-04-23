---
title: ICorDebugModule::GetName, méthode
ms.date: 03/30/2017
api_name:
- ICorDebugModule.GetName
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugModule::GetName
helpviewer_keywords:
- ICorDebugModule::GetName method [.NET Framework debugging]
- GetName method, ICorDebugModule interface [.NET Framework debugging]
ms.assetid: db499637-7ba9-421e-b8b1-35856995e80b
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: b39467c067e50f2d553b35a41b0f783e0fc82156
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59176642"
---
# <a name="icordebugmodulegetname-method"></a><span data-ttu-id="7dfc4-102">ICorDebugModule::GetName, méthode</span><span class="sxs-lookup"><span data-stu-id="7dfc4-102">ICorDebugModule::GetName Method</span></span>
<span data-ttu-id="7dfc4-103">Obtient le nom de fichier du module.</span><span class="sxs-lookup"><span data-stu-id="7dfc4-103">Gets the file name of the module.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="7dfc4-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="7dfc4-104">Syntax</span></span>  
  
```  
HRESULT GetName(  
    [in] ULONG32 cchName,  
    [out] ULONG32 *pcchName,  
    [out, size_is(cchName), length_is(*pcchName)] WCHAR szName[]  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="7dfc4-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="7dfc4-105">Parameters</span></span>  
 `cchname`  
 <span data-ttu-id="7dfc4-106">[in] Taille du tableau `szName`.</span><span class="sxs-lookup"><span data-stu-id="7dfc4-106">[in] The size of the `szName` array.</span></span>  
  
 `pcchName`  
 <span data-ttu-id="7dfc4-107">[in] Pointeur vers la longueur du nom retourné.</span><span class="sxs-lookup"><span data-stu-id="7dfc4-107">[in] A pointer to the length of the returned name.</span></span>  
  
 `szName`  
 <span data-ttu-id="7dfc4-108">[out] Tableau qui stocke le nom retourné.</span><span class="sxs-lookup"><span data-stu-id="7dfc4-108">[out] An array that stores the returned name.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="7dfc4-109">Notes</span><span class="sxs-lookup"><span data-stu-id="7dfc4-109">Remarks</span></span>  
 <span data-ttu-id="7dfc4-110">Le `GetName` méthode retourne une valeur S_OK HRESULT si le nom de fichier du module correspond au nom sur le disque.</span><span class="sxs-lookup"><span data-stu-id="7dfc4-110">The `GetName` method returns an S_OK HRESULT if the module's file name matches the name on disk.</span></span> <span data-ttu-id="7dfc4-111">`GetName` Retourne une valeur HRESULT S_FALSE si le nom est créé, comme pour un module dynamique ou en mémoire.</span><span class="sxs-lookup"><span data-stu-id="7dfc4-111">`GetName` returns an S_FALSE HRESULT if the name is fabricated, such as for a dynamic or in-memory module.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="7dfc4-112">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="7dfc4-112">Requirements</span></span>  
 <span data-ttu-id="7dfc4-113">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="7dfc4-113">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="7dfc4-114">**En-tête :** CorDebug.idl, CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="7dfc4-114">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="7dfc4-115">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="7dfc4-115">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="7dfc4-116">**Versions du .NET Framework :** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="7dfc4-116">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="7dfc4-117">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="7dfc4-117">See also</span></span>
