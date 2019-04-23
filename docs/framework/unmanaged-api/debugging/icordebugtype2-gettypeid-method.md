---
title: ICorDebugType2::GetTypeID (méthode)
ms.date: 03/30/2017
api_name:
- ICorDebugType2.GetTypeID
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugType::GetTypeID
helpviewer_keywords:
- GetTypeID method, ICorDebugType2 interface [.NET Framework debugging]
- ICorDebugType2.GetTypeID method [.NET Framework debugging]
ms.assetid: 0b933686-226e-4373-92b7-fac579ee7b1a
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 2b19efdedc21f66e4692ce1850eb3947f856e436
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59083749"
---
# <a name="icordebugtype2gettypeid-method"></a><span data-ttu-id="31d7d-102">ICorDebugType2::GetTypeID (méthode)</span><span class="sxs-lookup"><span data-stu-id="31d7d-102">ICorDebugType2::GetTypeID Method</span></span>
<span data-ttu-id="31d7d-103">Obtient un [COR_TYPEID](../../../../docs/framework/unmanaged-api/debugging/cor-typeid-structure.md) pour ce type.</span><span class="sxs-lookup"><span data-stu-id="31d7d-103">Gets a [COR_TYPEID](../../../../docs/framework/unmanaged-api/debugging/cor-typeid-structure.md) for this type.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="31d7d-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="31d7d-104">Syntax</span></span>  
  
```  
HRESULT GetTypeID(  
    ([out] COR_TYPEID *id  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="31d7d-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="31d7d-105">Parameters</span></span>  
 `id`  
 <span data-ttu-id="31d7d-106">[out] Un pointeur vers le [COR_TYPEID](../../../../docs/framework/unmanaged-api/debugging/cor-typeid-structure.md) pour ICorDebugType.</span><span class="sxs-lookup"><span data-stu-id="31d7d-106">[out] A pointer to the [COR_TYPEID](../../../../docs/framework/unmanaged-api/debugging/cor-typeid-structure.md) for this ICorDebugType.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="31d7d-107">Valeur de retour</span><span class="sxs-lookup"><span data-stu-id="31d7d-107">Return Value</span></span>  
 <span data-ttu-id="31d7d-108">La valeur de retour est `S_OK` en cas de réussite ou un code d'échec `HRESULT` en cas d'échec.</span><span class="sxs-lookup"><span data-stu-id="31d7d-108">The return value is `S_OK` on success, or a failure `HRESULT` code on failure.</span></span> <span data-ttu-id="31d7d-109">Le `HRESULT` codes incluent les éléments suivants :</span><span class="sxs-lookup"><span data-stu-id="31d7d-109">The `HRESULT` codes include the following:</span></span>  
  
|<span data-ttu-id="31d7d-110">Code de retour</span><span class="sxs-lookup"><span data-stu-id="31d7d-110">Return code</span></span>|<span data-ttu-id="31d7d-111">Description</span><span class="sxs-lookup"><span data-stu-id="31d7d-111">Description</span></span>|  
|-----------------|-----------------|  
|`S_OK`|<span data-ttu-id="31d7d-112">La méthode a réussi.</span><span class="sxs-lookup"><span data-stu-id="31d7d-112">Method succeeded.</span></span> <span data-ttu-id="31d7d-113">La méthode a récupéré valide [COR_TYPEID](../../../../docs/framework/unmanaged-api/debugging/cor-typeid-structure.md).</span><span class="sxs-lookup"><span data-stu-id="31d7d-113">The method has retrieved a valid [COR_TYPEID](../../../../docs/framework/unmanaged-api/debugging/cor-typeid-structure.md).</span></span>|  
|`CORDBG_E_CLASS_NOT_LOADED`|<span data-ttu-id="31d7d-114">Le type n’a pas été chargé.</span><span class="sxs-lookup"><span data-stu-id="31d7d-114">The type has not been loaded.</span></span>|  
|`CORDBG_E_UNSUPPORTED`|<span data-ttu-id="31d7d-115">Le type n’est pas pris en charge.</span><span class="sxs-lookup"><span data-stu-id="31d7d-115">The type is not supported.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="31d7d-116">Notes</span><span class="sxs-lookup"><span data-stu-id="31d7d-116">Remarks</span></span>  
 <span data-ttu-id="31d7d-117">Cette méthode fournit un mappage de ICorDebugType, qui représente un type qui peut ou ont ne peut-être pas été chargé dans l’exécution, à un [COR_TYPEID](../../../../docs/framework/unmanaged-api/debugging/cor-typeid-structure.md), qui sert un opaque gérer qui identifie un type chargé dans le runtime.</span><span class="sxs-lookup"><span data-stu-id="31d7d-117">This method provides a mapping from the ICorDebugType, which represents a type that may or may not have been loaded into the runtime, to a [COR_TYPEID](../../../../docs/framework/unmanaged-api/debugging/cor-typeid-structure.md), which serves as an opaque handle that identifies a type loaded into the runtime.</span></span>  
  
 <span data-ttu-id="31d7d-118">Lorsque le type qui représente le ICorDebugType n’a pas encore été chargé, cette méthode retourne `CORDBG_E_CLASS_NOT_LOADED`.</span><span class="sxs-lookup"><span data-stu-id="31d7d-118">When the type that the ICorDebugType represents has not yet been loaded, this method returns `CORDBG_E_CLASS_NOT_LOADED`.</span></span>  <span data-ttu-id="31d7d-119">Si le type n’est pas pris en charge, elle retourne `CORDBG_E_UNSUPPORTED`.</span><span class="sxs-lookup"><span data-stu-id="31d7d-119">If the type is not supported, it returns `CORDBG_E_UNSUPPORTED`.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="31d7d-120">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="31d7d-120">Requirements</span></span>  
 <span data-ttu-id="31d7d-121">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="31d7d-121">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="31d7d-122">**En-tête :** CorDebug.idl, CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="31d7d-122">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="31d7d-123">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="31d7d-123">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="31d7d-124">**Versions du .NET Framework :** [!INCLUDE[net_current_v462plus](../../../../includes/net-current-v462plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="31d7d-124">**.NET Framework Versions:** [!INCLUDE[net_current_v462plus](../../../../includes/net-current-v462plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="31d7d-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="31d7d-125">See also</span></span>

- [<span data-ttu-id="31d7d-126">ICorDebugType2, interface</span><span class="sxs-lookup"><span data-stu-id="31d7d-126">ICorDebugType2 Interface</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugtype2-interface.md)
