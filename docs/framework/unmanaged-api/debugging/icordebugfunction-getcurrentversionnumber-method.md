---
title: ICorDebugFunction::GetCurrentVersionNumber, méthode
ms.date: 03/30/2017
api_name:
- ICorDebugFunction.GetCurrentVersionNumber
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugFunction::GetCurrentVersionNumber
helpviewer_keywords:
- GetCurrentVersionNumber method [.NET Framework debugging]
- ICorDebugFunction::GetCurrentVersionNumber method [.NET Framework debugging]
ms.assetid: c3af1575-cbe6-457a-bc08-c53460edcbc8
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: ea615eacb30fd4e7a0fd7d730094c2ab4f9dc285
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61988726"
---
# <a name="icordebugfunctiongetcurrentversionnumber-method"></a><span data-ttu-id="e282f-102">ICorDebugFunction::GetCurrentVersionNumber, méthode</span><span class="sxs-lookup"><span data-stu-id="e282f-102">ICorDebugFunction::GetCurrentVersionNumber Method</span></span>
<span data-ttu-id="e282f-103">Obtient le numéro de version de la dernière modification apportée à la fonction représentée par cet objet ICorDebugFunction.</span><span class="sxs-lookup"><span data-stu-id="e282f-103">Gets the version number of the latest edit made to the function represented by this ICorDebugFunction object.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="e282f-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="e282f-104">Syntax</span></span>  
  
```  
HRESULT GetCurrentVersionNumber (  
    [out] ULONG32 *pnCurrentVersion  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="e282f-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="e282f-105">Parameters</span></span>  
 `pnCurrentVersion`  
 <span data-ttu-id="e282f-106">[out] Pointeur vers une valeur entière qui est le numéro de version de la dernière modification apportée à cette fonction.</span><span class="sxs-lookup"><span data-stu-id="e282f-106">[out] A pointer to an integer value that is the version number of the latest edit made to this function.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="e282f-107">Notes</span><span class="sxs-lookup"><span data-stu-id="e282f-107">Remarks</span></span>  
 <span data-ttu-id="e282f-108">Le numéro de version de la dernière modification apportée à cette fonction peut être supérieur au numéro de version de la fonction elle-même.</span><span class="sxs-lookup"><span data-stu-id="e282f-108">The version number of the latest edit made to this function may be greater than the version number of the function itself.</span></span> <span data-ttu-id="e282f-109">Utilisez le [ICorDebugFunction2::GetVersionNumber](../../../../docs/framework/unmanaged-api/debugging/icordebugfunction2-getversionnumber-method.md) méthode ou le [ICorDebugCode::GetVersionNumber](../../../../docs/framework/unmanaged-api/debugging/icordebugcode-getversionnumber-method.md) méthode pour récupérer le numéro de version de la fonction.</span><span class="sxs-lookup"><span data-stu-id="e282f-109">Use either the [ICorDebugFunction2::GetVersionNumber](../../../../docs/framework/unmanaged-api/debugging/icordebugfunction2-getversionnumber-method.md) method or the [ICorDebugCode::GetVersionNumber](../../../../docs/framework/unmanaged-api/debugging/icordebugcode-getversionnumber-method.md) method to retrieve the version number of the function.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="e282f-110">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="e282f-110">Requirements</span></span>  
 <span data-ttu-id="e282f-111">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="e282f-111">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="e282f-112">**En-tête :** CorDebug.idl, CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="e282f-112">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="e282f-113">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="e282f-113">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="e282f-114">**Versions du .NET Framework :** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="e282f-114">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>
