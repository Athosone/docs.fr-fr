---
title: ICorDebugManagedCallback::BreakpointSetError, méthode
ms.date: 03/30/2017
api_name:
- ICorDebugManagedCallback.BreakpointSetError
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugManagedCallback::BreakpointSetError
helpviewer_keywords:
- BreakpointSetError method [.NET Framework debugging]
- ICorDebugManagedCallback::BreakpointSetError method [.NET Framework debugging]
ms.assetid: f2b773a4-c4d0-429c-9717-51d6e2ed86af
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 27d5b8e0127971cc3a46560590fd9d95f0ffd1f0
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61988323"
---
# <a name="icordebugmanagedcallbackbreakpointseterror-method"></a><span data-ttu-id="6712f-102">ICorDebugManagedCallback::BreakpointSetError, méthode</span><span class="sxs-lookup"><span data-stu-id="6712f-102">ICorDebugManagedCallback::BreakpointSetError Method</span></span>
<span data-ttu-id="6712f-103">Notifie le débogueur que le common language runtime n’a pas pu lier correctement un point d’arrêt a été défini avant une fonction compilée juste-à-temps (JIT).</span><span class="sxs-lookup"><span data-stu-id="6712f-103">Notifies the debugger that the common language runtime was unable to accurately bind a breakpoint that was set before a function was just-in-time (JIT) compiled.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="6712f-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="6712f-104">Syntax</span></span>  
  
```  
HRESULT BreakpointSetError (  
    [in] ICorDebugAppDomain  *pAppDomain,  
    [in] ICorDebugThread     *pThread,  
    [in] ICorDebugBreakpoint *pBreakpoint,  
    [in] DWORD                dwError  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="6712f-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="6712f-105">Parameters</span></span>  
 `pAppDomain`  
 <span data-ttu-id="6712f-106">[in] Pointeur vers un objet ICorDebugAppDomain qui représente le domaine d’application qui contient le point d’arrêt indépendant.</span><span class="sxs-lookup"><span data-stu-id="6712f-106">[in] A pointer to an ICorDebugAppDomain object that represents the application domain that contains the unbound breakpoint.</span></span>  
  
 `pThread`  
 <span data-ttu-id="6712f-107">[in] Pointeur vers un objet ICorDebugThread qui représente le thread qui contient le point d’arrêt indépendant.</span><span class="sxs-lookup"><span data-stu-id="6712f-107">[in] A pointer to an ICorDebugThread object that represents the thread that contains the unbound breakpoint.</span></span>  
  
 `pBreakpoint`  
 <span data-ttu-id="6712f-108">[in] Pointeur vers un objet ICorDebugBreakpoint qui représente le point d’arrêt indépendant.</span><span class="sxs-lookup"><span data-stu-id="6712f-108">[in] A pointer to an ICorDebugBreakpoint object that represents the unbound breakpoint.</span></span>  
  
 `dwError`  
 <span data-ttu-id="6712f-109">[in] Entier qui indique l’erreur.</span><span class="sxs-lookup"><span data-stu-id="6712f-109">[in] An integer that indicates the error.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="6712f-110">Notes</span><span class="sxs-lookup"><span data-stu-id="6712f-110">Remarks</span></span>  
 <span data-ttu-id="6712f-111">Le point d’arrêt donné ne sera jamais atteint.</span><span class="sxs-lookup"><span data-stu-id="6712f-111">The given breakpoint will never be hit.</span></span> <span data-ttu-id="6712f-112">Le débogueur doit désactiver et reconnectez-la.</span><span class="sxs-lookup"><span data-stu-id="6712f-112">The debugger should deactivate and rebind it.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="6712f-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="6712f-113">Requirements</span></span>  
 <span data-ttu-id="6712f-114">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="6712f-114">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="6712f-115">**En-tête :** CorDebug.idl, CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="6712f-115">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="6712f-116">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="6712f-116">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="6712f-117">**Versions du .NET Framework :** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="6712f-117">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="6712f-118">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="6712f-118">See also</span></span>

- [<span data-ttu-id="6712f-119">ICorDebugManagedCallback, interface</span><span class="sxs-lookup"><span data-stu-id="6712f-119">ICorDebugManagedCallback Interface</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugmanagedcallback-interface.md)
