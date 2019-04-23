---
title: ICorDebug::DebugActiveProcess, méthode
ms.date: 03/30/2017
api_name:
- ICorDebug.DebugActiveProcess
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebug::DebugActiveProcess
helpviewer_keywords:
- DebugActiveProcess method [.NET Framework debugging]
- ICorDebug::DebugActiveProcess method [.NET Framework debugging]
ms.assetid: fdab0ade-7f56-4fa2-b3ef-f7a1d2852bba
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: b880358ed0d7bce4896217bc07c6ef6268d62962
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59076274"
---
# <a name="icordebugdebugactiveprocess-method"></a><span data-ttu-id="5d224-102">ICorDebug::DebugActiveProcess, méthode</span><span class="sxs-lookup"><span data-stu-id="5d224-102">ICorDebug::DebugActiveProcess Method</span></span>
<span data-ttu-id="5d224-103">Attache le débogueur à un processus existant.</span><span class="sxs-lookup"><span data-stu-id="5d224-103">Attaches the debugger to an existing process.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="5d224-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="5d224-104">Syntax</span></span>  
  
```  
HRESULT DebugActiveProcess (  
    [in]  DWORD               id,  
    [in]  BOOL                win32Attach,  
    [out] ICorDebugProcess    **ppProcess  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="5d224-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="5d224-105">Parameters</span></span>  
 `id`  
 <span data-ttu-id="5d224-106">[in] ID du processus auquel le débogueur doit être attaché.</span><span class="sxs-lookup"><span data-stu-id="5d224-106">[in] The ID of the process to which the debugger is to be attached.</span></span>  
  
 `win32Attach`  
 <span data-ttu-id="5d224-107">[in] Valeur booléenne qui est défini sur `true` si le débogueur doit se comporter comme le débogueur Win32 pour le processus et distribuer les rappels non managés ; sinon, `false`.</span><span class="sxs-lookup"><span data-stu-id="5d224-107">[in] Boolean value that is set to `true` if the debugger should behave as the Win32 debugger for the process and dispatch the unmanaged callbacks; otherwise, `false`.</span></span>  
  
 `ppProcess`  
 <span data-ttu-id="5d224-108">[out] Pointeur vers l’adresse d’un objet « ICorDebugProcess » qui représente le processus auquel le débogueur est attaché.</span><span class="sxs-lookup"><span data-stu-id="5d224-108">[out] A pointer to the address of an "ICorDebugProcess" object that represents the process to which the debugger has been attached.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="5d224-109">Notes</span><span class="sxs-lookup"><span data-stu-id="5d224-109">Remarks</span></span>  
 <span data-ttu-id="5d224-110">Débogage d’interopérabilité n’est pas pris en charge sur les plateformes Win9x et non x86, telles que les plateformes basés sur IA-64 et AMD64.</span><span class="sxs-lookup"><span data-stu-id="5d224-110">Interop debugging is not supported on Win9x and non-x86 platforms, such as IA-64-based and AMD64-based platforms.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="5d224-111">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="5d224-111">Requirements</span></span>  
 <span data-ttu-id="5d224-112">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="5d224-112">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="5d224-113">**En-tête :** CorDebug.idl, CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="5d224-113">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="5d224-114">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="5d224-114">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="5d224-115">**Versions du .NET Framework :** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="5d224-115">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="5d224-116">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="5d224-116">See also</span></span>

- [<span data-ttu-id="5d224-117">ICorDebug, interface</span><span class="sxs-lookup"><span data-stu-id="5d224-117">ICorDebug Interface</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebug-interface.md)
