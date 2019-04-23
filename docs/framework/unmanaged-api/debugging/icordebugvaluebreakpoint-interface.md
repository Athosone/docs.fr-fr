---
title: ICorDebugValueBreakpoint, interface
ms.date: 03/30/2017
api_name:
- ICorDebugValueBreakpoint
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugValueBreakpoint
helpviewer_keywords:
- ICorDebugValueBreakpoint interface [.NET Framework debugging]
ms.assetid: c02338fe-da6c-467f-9567-70ebb387e901
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 778359a7d26b6e2f19984a1f7ff06a527f2449f0
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59167744"
---
# <a name="icordebugvaluebreakpoint-interface"></a><span data-ttu-id="9ba37-102">ICorDebugValueBreakpoint, interface</span><span class="sxs-lookup"><span data-stu-id="9ba37-102">ICorDebugValueBreakpoint Interface</span></span>
<span data-ttu-id="9ba37-103">Étend l’interface ICorDebugBreakpoint pour fournir l’accès à des valeurs spécifiques.</span><span class="sxs-lookup"><span data-stu-id="9ba37-103">Extends the ICorDebugBreakpoint interface to provide access to specific values.</span></span>  
  
## <a name="methods"></a><span data-ttu-id="9ba37-104">Méthodes</span><span class="sxs-lookup"><span data-stu-id="9ba37-104">Methods</span></span>  
  
|<span data-ttu-id="9ba37-105">Méthode</span><span class="sxs-lookup"><span data-stu-id="9ba37-105">Method</span></span>|<span data-ttu-id="9ba37-106">Description</span><span class="sxs-lookup"><span data-stu-id="9ba37-106">Description</span></span>|  
|------------|-----------------|  
|[<span data-ttu-id="9ba37-107">GetValue, méthode</span><span class="sxs-lookup"><span data-stu-id="9ba37-107">GetValue Method</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugvaluebreakpoint-getvalue-method.md)|<span data-ttu-id="9ba37-108">Obtient un pointeur d’interface vers un objet ICorDebugValue qui représente la valeur de l’objet sur lequel le point d’arrêt est défini.</span><span class="sxs-lookup"><span data-stu-id="9ba37-108">Gets an interface pointer to an ICorDebugValue object that represents the value of the object upon which the breakpoint is set.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="9ba37-109">Notes</span><span class="sxs-lookup"><span data-stu-id="9ba37-109">Remarks</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="9ba37-110">Cette interface ne prend pas en charge l'appel à distance, que ce soit entre ordinateurs ou entre processus.</span><span class="sxs-lookup"><span data-stu-id="9ba37-110">This interface does not support being called remotely, either cross-machine or cross-process.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="9ba37-111">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="9ba37-111">Requirements</span></span>  
 <span data-ttu-id="9ba37-112">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="9ba37-112">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="9ba37-113">**En-tête :** CorDebug.idl, CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="9ba37-113">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="9ba37-114">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="9ba37-114">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="9ba37-115">**Versions du .NET Framework :** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="9ba37-115">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="9ba37-116">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="9ba37-116">See also</span></span>

- [<span data-ttu-id="9ba37-117">Interfaces de débogage</span><span class="sxs-lookup"><span data-stu-id="9ba37-117">Debugging Interfaces</span></span>](../../../../docs/framework/unmanaged-api/debugging/debugging-interfaces.md)
