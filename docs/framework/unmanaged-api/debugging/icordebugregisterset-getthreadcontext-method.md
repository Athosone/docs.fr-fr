---
title: ICorDebugRegisterSet::GetThreadContext, méthode
ms.date: 03/30/2017
api_name:
- ICorDebugRegisterSet.GetThreadContext
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugRegisterSet::GetThreadContext
helpviewer_keywords:
- GetThreadContext method, ICorDebugRegisterSet interface [.NET Framework debugging]
- ICorDebugRegisterSet::GetThreadContext method [.NET Framework debugging]
ms.assetid: 0f63400b-dc1c-48d6-b51a-75c3f7f28e03
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: fecbcff0fd124b94aeeecf82e23d9875c34ebb9b
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61782895"
---
# <a name="icordebugregistersetgetthreadcontext-method"></a><span data-ttu-id="58508-102">ICorDebugRegisterSet::GetThreadContext, méthode</span><span class="sxs-lookup"><span data-stu-id="58508-102">ICorDebugRegisterSet::GetThreadContext Method</span></span>
<span data-ttu-id="58508-103">Obtient le contexte du thread actuel.</span><span class="sxs-lookup"><span data-stu-id="58508-103">Gets the context of the current thread.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="58508-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="58508-104">Syntax</span></span>  
  
```  
HRESULT GetThreadContext(  
    [in] ULONG32 contextSize,  
    [in, out, length_is(contextSize),  
        size_is(contextSize)] BYTE context[]  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="58508-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="58508-105">Parameters</span></span>  
 `contextSize`  
 <span data-ttu-id="58508-106">[in] La taille, en octets, de la `context` tableau.</span><span class="sxs-lookup"><span data-stu-id="58508-106">[in] The size, in bytes, of the `context` array.</span></span>  
  
 `context`  
 <span data-ttu-id="58508-107">[in, out] Un tableau d’octets qui composent le Win32 `CONTEXT` structure pour la plateforme actuelle.</span><span class="sxs-lookup"><span data-stu-id="58508-107">[in, out] An array of bytes that compose the Win32 `CONTEXT` structure for the current platform.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="58508-108">Notes</span><span class="sxs-lookup"><span data-stu-id="58508-108">Remarks</span></span>  
 <span data-ttu-id="58508-109">Le débogueur doit appeler cette fonction au lieu de Win32 `GetThreadContext` fonctionner, car le thread peut être dans un état « infiltré » où son contexte a été changé temporairement.</span><span class="sxs-lookup"><span data-stu-id="58508-109">The debugger should call this function instead of the Win32 `GetThreadContext` function, because the thread may be in a "hijacked" state where its context has been temporarily changed.</span></span> <span data-ttu-id="58508-110">Les données retournées sont un Win32 `CONTEXT` structure pour la plateforme actuelle.</span><span class="sxs-lookup"><span data-stu-id="58508-110">The data returned is a Win32 `CONTEXT` structure for the current platform.</span></span>  
  
 <span data-ttu-id="58508-111">Pour les frames, les clients doivent vérifier les registres qui sont valides à l’aide de [ICorDebugRegisterSet::GetRegistersAvailable](../../../../docs/framework/unmanaged-api/debugging/icordebugregisterset-getregistersavailable-method.md).</span><span class="sxs-lookup"><span data-stu-id="58508-111">For non-leaf frames, clients should check which registers are valid by using [ICorDebugRegisterSet::GetRegistersAvailable](../../../../docs/framework/unmanaged-api/debugging/icordebugregisterset-getregistersavailable-method.md).</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="58508-112">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="58508-112">Requirements</span></span>  
 <span data-ttu-id="58508-113">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="58508-113">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="58508-114">**En-tête :** CorDebug.idl, CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="58508-114">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="58508-115">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="58508-115">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="58508-116">**Versions du .NET Framework :** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="58508-116">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="58508-117">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="58508-117">See also</span></span>

- [<span data-ttu-id="58508-118">ICorDebugRegisterSet, interface</span><span class="sxs-lookup"><span data-stu-id="58508-118">ICorDebugRegisterSet Interface</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugregisterset-interface.md)
- [<span data-ttu-id="58508-119">ICorDebugRegisterSet2, interface</span><span class="sxs-lookup"><span data-stu-id="58508-119">ICorDebugRegisterSet2 Interface</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugregisterset2-interface.md)
