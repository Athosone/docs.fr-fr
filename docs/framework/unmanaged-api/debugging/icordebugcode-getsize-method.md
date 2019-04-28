---
title: ICorDebugCode::GetSize, méthode
ms.date: 03/30/2017
api_name:
- ICorDebugCode.GetSize
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugCode::GetSize
helpviewer_keywords:
- GetSize method, ICorDebugCode interface [.NET Framework debugging]
- ICorDebugCode::GetSize method [.NET Framework debugging]
ms.assetid: 115bc6de-f5e2-4e8e-bb38-c7cf54045434
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 678b7fbd595b1238b7025c22b0ed80b02ed4becd
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61750204"
---
# <a name="icordebugcodegetsize-method"></a><span data-ttu-id="254f3-102">ICorDebugCode::GetSize, méthode</span><span class="sxs-lookup"><span data-stu-id="254f3-102">ICorDebugCode::GetSize Method</span></span>
<span data-ttu-id="254f3-103">Obtient la taille, en octets, du code binaire représenté par « ICorDebugCode ».</span><span class="sxs-lookup"><span data-stu-id="254f3-103">Gets the size, in bytes, of the binary code represented by this "ICorDebugCode".</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="254f3-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="254f3-104">Syntax</span></span>  
  
```  
HRESULT GetSize (  
    [out] ULONG32    *pcBytes  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="254f3-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="254f3-105">Parameters</span></span>  
 `pcBytes`  
 <span data-ttu-id="254f3-106">[out] Un pointeur vers la taille, en octets, du fichier binaire de code que ce `ICorDebugCode` représente l’objet.</span><span class="sxs-lookup"><span data-stu-id="254f3-106">[out] A pointer to the size, in bytes, of the binary code that this `ICorDebugCode` object represents.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="254f3-107">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="254f3-107">Requirements</span></span>  
 <span data-ttu-id="254f3-108">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="254f3-108">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="254f3-109">**En-tête :** CorDebug.idl, CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="254f3-109">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="254f3-110">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="254f3-110">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="254f3-111">**Versions du .NET Framework :** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="254f3-111">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="254f3-112">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="254f3-112">See also</span></span>
