---
title: ICorDebugValue, interface
ms.date: 03/30/2017
api_name:
- ICorDebugValue
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugValue
helpviewer_keywords:
- ICorDebugValue interface [.NET Framework debugging]
ms.assetid: b2f7007f-c446-4b18-aed1-a25cff8aee31
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: bdc889dd6b2854654bfe43b24afbe4cc19863c80
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59227819"
---
# <a name="icordebugvalue-interface"></a><span data-ttu-id="ef4f6-102">ICorDebugValue, interface</span><span class="sxs-lookup"><span data-stu-id="ef4f6-102">ICorDebugValue Interface</span></span>
<span data-ttu-id="ef4f6-103">Représente une valeur dans le processus en cours de débogage.</span><span class="sxs-lookup"><span data-stu-id="ef4f6-103">Represents a value in the process being debugged.</span></span> <span data-ttu-id="ef4f6-104">La valeur peut être une lecture ou une valeur de l’écriture.</span><span class="sxs-lookup"><span data-stu-id="ef4f6-104">The value can be a read or a write value.</span></span>  
  
## <a name="methods"></a><span data-ttu-id="ef4f6-105">Méthodes</span><span class="sxs-lookup"><span data-stu-id="ef4f6-105">Methods</span></span>  
  
|<span data-ttu-id="ef4f6-106">Méthode</span><span class="sxs-lookup"><span data-stu-id="ef4f6-106">Method</span></span>|<span data-ttu-id="ef4f6-107">Description</span><span class="sxs-lookup"><span data-stu-id="ef4f6-107">Description</span></span>|  
|------------|-----------------|  
|[<span data-ttu-id="ef4f6-108">CreateBreakpoint, méthode</span><span class="sxs-lookup"><span data-stu-id="ef4f6-108">CreateBreakpoint Method</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugvalue-createbreakpoint-method.md)|<span data-ttu-id="ef4f6-109">Cette méthode n’est pas implémentée actuellement.</span><span class="sxs-lookup"><span data-stu-id="ef4f6-109">This method is not currently implemented.</span></span>|  
|[<span data-ttu-id="ef4f6-110">GetAddress, méthode</span><span class="sxs-lookup"><span data-stu-id="ef4f6-110">GetAddress Method</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugvalue-getaddress-method.md)|<span data-ttu-id="ef4f6-111">Obtient l’adresse de ce `ICorDebugValue` objet, qui est en cours de débogage.</span><span class="sxs-lookup"><span data-stu-id="ef4f6-111">Gets the address of this `ICorDebugValue` object, which is in the process of being debugged.</span></span>|  
|[<span data-ttu-id="ef4f6-112">GetSize, méthode</span><span class="sxs-lookup"><span data-stu-id="ef4f6-112">GetSize Method</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugvalue-getsize-method.md)|<span data-ttu-id="ef4f6-113">Obtient la taille, en octets, de ce `ICorDebugValue` objet.</span><span class="sxs-lookup"><span data-stu-id="ef4f6-113">Gets the size, in bytes, of this `ICorDebugValue` object.</span></span>|  
|[<span data-ttu-id="ef4f6-114">GetType, méthode</span><span class="sxs-lookup"><span data-stu-id="ef4f6-114">GetType Method</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugvalue-gettype-method.md)|<span data-ttu-id="ef4f6-115">Obtient le type primitif de cet `ICorDebugValue` objet.</span><span class="sxs-lookup"><span data-stu-id="ef4f6-115">Gets the primitive type of this `ICorDebugValue` object.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="ef4f6-116">Notes</span><span class="sxs-lookup"><span data-stu-id="ef4f6-116">Remarks</span></span>  
 <span data-ttu-id="ef4f6-117">En règle générale, la propriété d’un objet de valeur est passée lorsqu’elle est retournée.</span><span class="sxs-lookup"><span data-stu-id="ef4f6-117">In general, ownership of a value object is passed when it is returned.</span></span> <span data-ttu-id="ef4f6-118">Le destinataire est responsable de la suppression d’une référence à partir de l’objet lorsqu’il est terminé avec l’objet.</span><span class="sxs-lookup"><span data-stu-id="ef4f6-118">The recipient is responsible for removing a reference from the object when it is finished with the object.</span></span>  
  
 <span data-ttu-id="ef4f6-119">Selon où la valeur a été récupérée à partir de, la valeur restera ne peut-être pas valide une fois que le processus se poursuit.</span><span class="sxs-lookup"><span data-stu-id="ef4f6-119">Depending on where the value was retrieved from, the value may not remain valid after the process is resumed.</span></span> <span data-ttu-id="ef4f6-120">Par conséquent, en règle générale, la valeur ne doit pas être maintenue à travers un appel de la [ICorDebugController::Continue](../../../../docs/framework/unmanaged-api/debugging/icordebugcontroller-continue-method.md) (méthode).</span><span class="sxs-lookup"><span data-stu-id="ef4f6-120">So, in general, the value shouldn't be held across a call of the [ICorDebugController::Continue](../../../../docs/framework/unmanaged-api/debugging/icordebugcontroller-continue-method.md) method.</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="ef4f6-121">Cette interface ne prend pas en charge l'appel à distance, que ce soit entre ordinateurs ou entre processus.</span><span class="sxs-lookup"><span data-stu-id="ef4f6-121">This interface does not support being called remotely, either cross-machine or cross-process.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="ef4f6-122">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="ef4f6-122">Requirements</span></span>  
 <span data-ttu-id="ef4f6-123">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="ef4f6-123">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="ef4f6-124">**En-tête :** CorDebug.idl, CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="ef4f6-124">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="ef4f6-125">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="ef4f6-125">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="ef4f6-126">**Versions du .NET Framework :** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="ef4f6-126">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="ef4f6-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ef4f6-127">See also</span></span>

- [<span data-ttu-id="ef4f6-128">ICorDebugValue3, interface</span><span class="sxs-lookup"><span data-stu-id="ef4f6-128">ICorDebugValue3 Interface</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugvalue3-interface.md)
- [<span data-ttu-id="ef4f6-129">Interfaces de débogage</span><span class="sxs-lookup"><span data-stu-id="ef4f6-129">Debugging Interfaces</span></span>](../../../../docs/framework/unmanaged-api/debugging/debugging-interfaces.md)
