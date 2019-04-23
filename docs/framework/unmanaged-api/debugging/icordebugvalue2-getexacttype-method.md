---
title: ICorDebugValue2::GetExactType, méthode
ms.date: 03/30/2017
api_name:
- ICorDebugValue2.GetExactType
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugValue2::GetExactType
helpviewer_keywords:
- ICorDebugValue2::GetExactType method [.NET Framework debugging]
- GetExactType method [.NET Framework debugging]
ms.assetid: 8e9aae1b-d1b7-4b6e-b577-6faf36dcec85
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 002e53d380140a63297a90baa270b5a6f1e5e328
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59192262"
---
# <a name="icordebugvalue2getexacttype-method"></a><span data-ttu-id="68016-102">ICorDebugValue2::GetExactType, méthode</span><span class="sxs-lookup"><span data-stu-id="68016-102">ICorDebugValue2::GetExactType Method</span></span>
<span data-ttu-id="68016-103">Obtient un pointeur d’interface vers un objet « ICorDebugType » qui représente le <xref:System.Type> de cette valeur.</span><span class="sxs-lookup"><span data-stu-id="68016-103">Gets an interface pointer to an "ICorDebugType" object that represents the <xref:System.Type> of this value.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="68016-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="68016-104">Syntax</span></span>  
  
```  
HRESULT GetExactType (  
    [out] ICorDebugType   **ppType  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="68016-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="68016-105">Parameters</span></span>  
 `ppType`  
 <span data-ttu-id="68016-106">[out] Un pointeur vers l’adresse d’un `ICorDebugType` objet qui représente le <xref:System.Type> de la valeur représentée par cet objet « ICorDebugValue2 ».</span><span class="sxs-lookup"><span data-stu-id="68016-106">[out] A pointer to the address of an `ICorDebugType` object that represents the <xref:System.Type> of the value represented by this "ICorDebugValue2" object.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="68016-107">Notes</span><span class="sxs-lookup"><span data-stu-id="68016-107">Remarks</span></span>  
 <span data-ttu-id="68016-108">Les génériques prenant en charge les `GetExactType` méthode remplace à la fois le [ICorDebugObjectValue::GetClass](../../../../docs/framework/unmanaged-api/debugging/icordebugobjectvalue-getclass-method.md) et le [ICorDebugValue::GetType](../../../../docs/framework/unmanaged-api/debugging/icordebugvalue-gettype-method.md) méthodes, chacune retournant des informations sur le type d’une valeur .</span><span class="sxs-lookup"><span data-stu-id="68016-108">The generics-aware `GetExactType` method supersedes both the [ICorDebugObjectValue::GetClass](../../../../docs/framework/unmanaged-api/debugging/icordebugobjectvalue-getclass-method.md) and the [ICorDebugValue::GetType](../../../../docs/framework/unmanaged-api/debugging/icordebugvalue-gettype-method.md) methods, each of which return information about the type of a value.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="68016-109">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="68016-109">Requirements</span></span>  
 <span data-ttu-id="68016-110">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="68016-110">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="68016-111">**En-tête :** CorDebug.idl, CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="68016-111">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="68016-112">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="68016-112">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="68016-113">**Versions du .NET Framework :** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="68016-113">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="68016-114">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="68016-114">See also</span></span>
