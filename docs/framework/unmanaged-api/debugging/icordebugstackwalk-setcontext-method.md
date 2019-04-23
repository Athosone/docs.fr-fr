---
title: ICorDebugStackWalk::SetContext, méthode
ms.date: 03/30/2017
api_name:
- ICorDebugStackWalk.SetContext Method
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugStackWalk::SetContext
helpviewer_keywords:
- SetContext method [.NET Framework debugging]
- ICorDebugStackWalk::SetContext method [.NET Framework debugging]
ms.assetid: bac0b156-31a3-4e7f-be4d-ab21789c81f1
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 7306ee61d750ae256c93c049819a23d3d61f7297
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59116465"
---
# <a name="icordebugstackwalksetcontext-method"></a><span data-ttu-id="ec6cf-102">ICorDebugStackWalk::SetContext, méthode</span><span class="sxs-lookup"><span data-stu-id="ec6cf-102">ICorDebugStackWalk::SetContext Method</span></span>
<span data-ttu-id="ec6cf-103">Définit le [ICorDebugStackWalk](../../../../docs/framework/unmanaged-api/debugging/icordebugstackwalk-interface.md) contexte actuel de l’objet à un contexte valid pour le thread.</span><span class="sxs-lookup"><span data-stu-id="ec6cf-103">Sets the [ICorDebugStackWalk](../../../../docs/framework/unmanaged-api/debugging/icordebugstackwalk-interface.md) object’s current context to a valid context for the thread.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="ec6cf-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="ec6cf-104">Syntax</span></span>  
  
```  
HRESULT SetContext([in] CorDebugSetContextFlag flag,  
                   [in] ULONG32 contextSize,  
                   [in, size_is(contextSize)] BYTE context[]);  
```  
  
## <a name="parameters"></a><span data-ttu-id="ec6cf-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="ec6cf-105">Parameters</span></span>  
 `flag`  
 <span data-ttu-id="ec6cf-106">[in] Un [CorDebugSetContextFlag](../../../../docs/framework/unmanaged-api/debugging/cordebugsetcontextflag-enumeration.md) indicateur qui indique si le contexte provient du frame actif sur la pile, ou un contexte obtenu par le déroulement de la pile.</span><span class="sxs-lookup"><span data-stu-id="ec6cf-106">[in] A [CorDebugSetContextFlag](../../../../docs/framework/unmanaged-api/debugging/cordebugsetcontextflag-enumeration.md) flag that indicates whether the context is from the active frame on the stack, or a context obtained by unwinding the stack.</span></span>  
  
 `contextSize`  
 <span data-ttu-id="ec6cf-107">[in] La taille allouée de la `CONTEXT` mémoire tampon.</span><span class="sxs-lookup"><span data-stu-id="ec6cf-107">[in] The allocated size of the `CONTEXT` buffer.</span></span>  
  
 `context`  
 <span data-ttu-id="ec6cf-108">[in] Le `CONTEXT` mémoire tampon.</span><span class="sxs-lookup"><span data-stu-id="ec6cf-108">[in] The `CONTEXT` buffer.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="ec6cf-109">Valeur de retour</span><span class="sxs-lookup"><span data-stu-id="ec6cf-109">Return Value</span></span>  
 <span data-ttu-id="ec6cf-110">Cette méthode retourne les HRESULT spécifiques suivants ainsi que les erreurs HRESULT indiquant l'échec de la méthode.</span><span class="sxs-lookup"><span data-stu-id="ec6cf-110">This method returns the following specific HRESULTs as well as HRESULT errors that indicate method failure.</span></span>  
  
|<span data-ttu-id="ec6cf-111">HRESULT</span><span class="sxs-lookup"><span data-stu-id="ec6cf-111">HRESULT</span></span>|<span data-ttu-id="ec6cf-112">Description</span><span class="sxs-lookup"><span data-stu-id="ec6cf-112">Description</span></span>|  
|-------------|-----------------|  
|<span data-ttu-id="ec6cf-113">S_OK</span><span class="sxs-lookup"><span data-stu-id="ec6cf-113">S_OK</span></span>|<span data-ttu-id="ec6cf-114">Le `ICorDebugStackWalk` contexte de l’objet a été défini correctement.</span><span class="sxs-lookup"><span data-stu-id="ec6cf-114">The `ICorDebugStackWalk` object's context was successfully set.</span></span>|  
|<span data-ttu-id="ec6cf-115">E_FAIL</span><span class="sxs-lookup"><span data-stu-id="ec6cf-115">E_FAIL</span></span>|<span data-ttu-id="ec6cf-116">Le `ICorDebugStackWalk` contexte de l’objet n’a pas été défini.</span><span class="sxs-lookup"><span data-stu-id="ec6cf-116">The `ICorDebugStackWalk` object's context was not set.</span></span>|  
|<span data-ttu-id="ec6cf-117">E_INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="ec6cf-117">E_INVALIDARG</span></span>|<span data-ttu-id="ec6cf-118">Le contexte est null.</span><span class="sxs-lookup"><span data-stu-id="ec6cf-118">The context is null.</span></span>|  
|<span data-ttu-id="ec6cf-119">HRESULT_FROM_WIN32(ERROR_INSUFFICIENT_BUFFER)</span><span class="sxs-lookup"><span data-stu-id="ec6cf-119">HRESULT_FROM_WIN32(ERROR_INSUFFICIENT_BUFFER)</span></span>|<span data-ttu-id="ec6cf-120">Mémoire tampon de contexte est trop petite.</span><span class="sxs-lookup"><span data-stu-id="ec6cf-120">The context buffer is too small.</span></span>|  
  
## <a name="exceptions"></a><span data-ttu-id="ec6cf-121">Exceptions</span><span class="sxs-lookup"><span data-stu-id="ec6cf-121">Exceptions</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="ec6cf-122">Notes</span><span class="sxs-lookup"><span data-stu-id="ec6cf-122">Remarks</span></span>  
 <span data-ttu-id="ec6cf-123">Cette méthode ne modifie pas le contexte actuel du thread.</span><span class="sxs-lookup"><span data-stu-id="ec6cf-123">This method does not alter the current context of the thread.</span></span>  
  
 <span data-ttu-id="ec6cf-124">Définition du contexte actuel à un contexte non valide peut provoquer des résultats imprévisibles à partir de l’Explorateur de pile.</span><span class="sxs-lookup"><span data-stu-id="ec6cf-124">Setting the current context to an invalid context may cause unpredictable results from the stack walker.</span></span>  
  
 <span data-ttu-id="ec6cf-125">Vous pouvez récupérer une copie au niveau du bit exacte de ce contexte en appelant immédiatement la [ICorDebugStackWalk::GetContext](../../../../docs/framework/unmanaged-api/debugging/icordebugstackwalk-getcontext-method.md) (méthode).</span><span class="sxs-lookup"><span data-stu-id="ec6cf-125">You can retrieve an exact bitwise copy of this context by immediately calling the [ICorDebugStackWalk::GetContext](../../../../docs/framework/unmanaged-api/debugging/icordebugstackwalk-getcontext-method.md) method.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="ec6cf-126">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="ec6cf-126">Requirements</span></span>  
 <span data-ttu-id="ec6cf-127">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="ec6cf-127">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="ec6cf-128">**En-tête :** CorDebug.idl, CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="ec6cf-128">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="ec6cf-129">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="ec6cf-129">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="ec6cf-130">**Versions du .NET Framework :** [!INCLUDE[net_current_v40plus](../../../../includes/net-current-v40plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="ec6cf-130">**.NET Framework Versions:** [!INCLUDE[net_current_v40plus](../../../../includes/net-current-v40plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="ec6cf-131">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ec6cf-131">See also</span></span>

- [<span data-ttu-id="ec6cf-132">Interfaces de débogage</span><span class="sxs-lookup"><span data-stu-id="ec6cf-132">Debugging Interfaces</span></span>](../../../../docs/framework/unmanaged-api/debugging/debugging-interfaces.md)
- [<span data-ttu-id="ec6cf-133">Débogage</span><span class="sxs-lookup"><span data-stu-id="ec6cf-133">Debugging</span></span>](../../../../docs/framework/unmanaged-api/debugging/index.md)
