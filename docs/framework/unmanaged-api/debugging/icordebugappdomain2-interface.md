---
title: ICorDebugAppDomain2, interface
ms.date: 03/30/2017
api_name:
- ICorDebugAppDomain2
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugAppDomain2
helpviewer_keywords:
- ICorDebugAppDomain2 interface [.NET Framework debugging]
ms.assetid: 314d29f3-feb0-4a92-9530-b569c280cc31
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 5c6ef901f43cd6568f17657ed8e58bc2cc2cc0a1
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59186054"
---
# <a name="icordebugappdomain2-interface"></a><span data-ttu-id="72d7d-102">ICorDebugAppDomain2, interface</span><span class="sxs-lookup"><span data-stu-id="72d7d-102">ICorDebugAppDomain2 Interface</span></span>

<span data-ttu-id="72d7d-103">Fournit des méthodes pour travailler avec des tableaux, les pointeurs, les pointeurs de fonction et les types référence.</span><span class="sxs-lookup"><span data-stu-id="72d7d-103">Provides methods to work with arrays, pointers, function pointers, and reference types.</span></span> <span data-ttu-id="72d7d-104">Cette interface est une extension de l’interface ICorDebugAppDomain.</span><span class="sxs-lookup"><span data-stu-id="72d7d-104">This interface is an extension of the ICorDebugAppDomain interface.</span></span>  
  
## <a name="methods"></a><span data-ttu-id="72d7d-105">Méthodes</span><span class="sxs-lookup"><span data-stu-id="72d7d-105">Methods</span></span>  
  
|<span data-ttu-id="72d7d-106">Méthode</span><span class="sxs-lookup"><span data-stu-id="72d7d-106">Method</span></span>|<span data-ttu-id="72d7d-107">Description</span><span class="sxs-lookup"><span data-stu-id="72d7d-107">Description</span></span>|  
|------------|-----------------|  
|[<span data-ttu-id="72d7d-108">GetArrayOrPointerType, méthode</span><span class="sxs-lookup"><span data-stu-id="72d7d-108">GetArrayOrPointerType Method</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugappdomain2-getarrayorpointertype-method.md)|<span data-ttu-id="72d7d-109">Obtient un tableau du type spécifié, ou un pointeur ou une référence vers le type spécifié.</span><span class="sxs-lookup"><span data-stu-id="72d7d-109">Gets an array of the specified type, or a pointer or reference to the specified type.</span></span>|  
|[<span data-ttu-id="72d7d-110">GetFunctionPointerType</span><span class="sxs-lookup"><span data-stu-id="72d7d-110">GetFunctionPointerType</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugappdomain2-getfunctionpointertype-method.md)|<span data-ttu-id="72d7d-111">Obtient un pointeur vers une fonction qui a une signature donnée.</span><span class="sxs-lookup"><span data-stu-id="72d7d-111">Gets a pointer to a function that has a given signature.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="72d7d-112">Notes</span><span class="sxs-lookup"><span data-stu-id="72d7d-112">Remarks</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="72d7d-113">Cette interface ne prend pas en charge l'appel à distance, que ce soit entre ordinateurs ou entre processus.</span><span class="sxs-lookup"><span data-stu-id="72d7d-113">This interface does not support being called remotely, either cross-machine or cross-process.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="72d7d-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="72d7d-114">Requirements</span></span>  
 <span data-ttu-id="72d7d-115">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="72d7d-115">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="72d7d-116">**En-tête :** CorDebug.idl, CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="72d7d-116">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="72d7d-117">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="72d7d-117">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="72d7d-118">**Versions du .NET Framework :** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="72d7d-118">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="72d7d-119">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="72d7d-119">See also</span></span>

- [<span data-ttu-id="72d7d-120">Interfaces de débogage</span><span class="sxs-lookup"><span data-stu-id="72d7d-120">Debugging Interfaces</span></span>](../../../../docs/framework/unmanaged-api/debugging/debugging-interfaces.md)
