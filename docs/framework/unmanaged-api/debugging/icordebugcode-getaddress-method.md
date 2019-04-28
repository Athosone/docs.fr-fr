---
title: ICorDebugCode::GetAddress, méthode
ms.date: 03/30/2017
api_name:
- ICorDebugCode.GetAddress
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugCode::GetAddress
helpviewer_keywords:
- GetAddress method, ICorDebugCode interface [.NET Framework debugging]
- ICorDebugCode::GetAddress method [.NET Framework debugging]
ms.assetid: cc507cb0-df2e-49c2-b32e-0c3271a8df9a
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 11ced90b88f083eb69b06d197d64a8ef4252f9d5
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61750421"
---
# <a name="icordebugcodegetaddress-method"></a><span data-ttu-id="2c4ac-102">ICorDebugCode::GetAddress, méthode</span><span class="sxs-lookup"><span data-stu-id="2c4ac-102">ICorDebugCode::GetAddress Method</span></span>
<span data-ttu-id="2c4ac-103">Obtient l’adresse virtuelle relative (RVA) du segment de code qui représente cette interface « ICorDebugCode ».</span><span class="sxs-lookup"><span data-stu-id="2c4ac-103">Gets the relative virtual address (RVA) of the code segment that this "ICorDebugCode" interface represents.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="2c4ac-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="2c4ac-104">Syntax</span></span>  
  
```  
HRESULT GetAddress (  
    [out] CORDB_ADDRESS *pStart  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="2c4ac-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="2c4ac-105">Parameters</span></span>  
 `pStart`  
 <span data-ttu-id="2c4ac-106">[out] Pointeur vers l’adresse RVA du segment de code.</span><span class="sxs-lookup"><span data-stu-id="2c4ac-106">[out] A pointer to the RVA of the code segment.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="2c4ac-107">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="2c4ac-107">Requirements</span></span>  
 <span data-ttu-id="2c4ac-108">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="2c4ac-108">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="2c4ac-109">**En-tête :** CorDebug.idl, CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="2c4ac-109">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="2c4ac-110">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="2c4ac-110">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="2c4ac-111">**Versions du .NET Framework :** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="2c4ac-111">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="2c4ac-112">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="2c4ac-112">See also</span></span>
