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
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61988017"
---
# <a name="icordebugmodulegetname-method"></a><span data-ttu-id="81ac8-102">ICorDebugModule::GetName, méthode</span><span class="sxs-lookup"><span data-stu-id="81ac8-102">ICorDebugModule::GetName Method</span></span>
<span data-ttu-id="81ac8-103">Obtient le nom de fichier du module.</span><span class="sxs-lookup"><span data-stu-id="81ac8-103">Gets the file name of the module.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="81ac8-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="81ac8-104">Syntax</span></span>  
  
```  
HRESULT GetName(  
    [in] ULONG32 cchName,  
    [out] ULONG32 *pcchName,  
    [out, size_is(cchName), length_is(*pcchName)] WCHAR szName[]  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="81ac8-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="81ac8-105">Parameters</span></span>  
 `cchname`  
 <span data-ttu-id="81ac8-106">[in] Taille du tableau `szName`.</span><span class="sxs-lookup"><span data-stu-id="81ac8-106">[in] The size of the `szName` array.</span></span>  
  
 `pcchName`  
 <span data-ttu-id="81ac8-107">[in] Pointeur vers la longueur du nom retourné.</span><span class="sxs-lookup"><span data-stu-id="81ac8-107">[in] A pointer to the length of the returned name.</span></span>  
  
 `szName`  
 <span data-ttu-id="81ac8-108">[out] Tableau qui stocke le nom retourné.</span><span class="sxs-lookup"><span data-stu-id="81ac8-108">[out] An array that stores the returned name.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="81ac8-109">Notes</span><span class="sxs-lookup"><span data-stu-id="81ac8-109">Remarks</span></span>  
 <span data-ttu-id="81ac8-110">Le `GetName` méthode retourne une valeur S_OK HRESULT si le nom de fichier du module correspond au nom sur le disque.</span><span class="sxs-lookup"><span data-stu-id="81ac8-110">The `GetName` method returns an S_OK HRESULT if the module's file name matches the name on disk.</span></span> <span data-ttu-id="81ac8-111">`GetName` Retourne une valeur HRESULT S_FALSE si le nom est créé, comme pour un module dynamique ou en mémoire.</span><span class="sxs-lookup"><span data-stu-id="81ac8-111">`GetName` returns an S_FALSE HRESULT if the name is fabricated, such as for a dynamic or in-memory module.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="81ac8-112">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="81ac8-112">Requirements</span></span>  
 <span data-ttu-id="81ac8-113">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="81ac8-113">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="81ac8-114">**En-tête :** CorDebug.idl, CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="81ac8-114">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="81ac8-115">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="81ac8-115">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="81ac8-116">**Versions du .NET Framework :** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="81ac8-116">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="81ac8-117">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="81ac8-117">See also</span></span>
