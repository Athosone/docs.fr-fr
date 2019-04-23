---
title: ICorDebugManagedCallback::NameChange, méthode
ms.date: 03/30/2017
api_name:
- ICorDebugManagedCallback.NameChange
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugManagedCallback::NameChange
helpviewer_keywords:
- ICorDebugManagedCallback::NameChange method [.NET Framework debugging]
- NameChange method [.NET Framework debugging]
ms.assetid: a7018a0e-880e-4b68-b52a-1cd22c7aad62
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 975353403a82956912fa41047253bb0dbf138502
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59124122"
---
# <a name="icordebugmanagedcallbacknamechange-method"></a><span data-ttu-id="5283f-102">ICorDebugManagedCallback::NameChange, méthode</span><span class="sxs-lookup"><span data-stu-id="5283f-102">ICorDebugManagedCallback::NameChange Method</span></span>
<span data-ttu-id="5283f-103">Notifie le débogueur que le nom d’un domaine d’application ou d’un thread a changé.</span><span class="sxs-lookup"><span data-stu-id="5283f-103">Notifies the debugger that the name of either an application domain or a thread has changed.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="5283f-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="5283f-104">Syntax</span></span>  
  
```  
HRESULT NameChange (  
    [in] ICorDebugAppDomain *pAppDomain,  
    [in] ICorDebugThread    *pThread  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="5283f-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="5283f-105">Parameters</span></span>  
 `pAppDomain`  
 <span data-ttu-id="5283f-106">[in] Un pointeur vers un objet ICorDebugAppDomain qui représente le domaine d’application qui avait un changement de nom ou qui contient le thread qui avait un changement de nom.</span><span class="sxs-lookup"><span data-stu-id="5283f-106">[in] A pointer to an ICorDebugAppDomain object that represents the application domain that either had a name change or that contains the thread that had a name change.</span></span>  
  
 `pThread`  
 <span data-ttu-id="5283f-107">[in] Pointeur vers un objet ICorDebugThread qui représente le thread qui avait un changement de nom.</span><span class="sxs-lookup"><span data-stu-id="5283f-107">[in] A pointer to an ICorDebugThread object that represents the thread that had a name change.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="5283f-108">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="5283f-108">Requirements</span></span>  
 <span data-ttu-id="5283f-109">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="5283f-109">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="5283f-110">**En-tête :** CorDebug.idl, CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="5283f-110">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="5283f-111">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="5283f-111">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="5283f-112">**Versions du .NET Framework :** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="5283f-112">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="5283f-113">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="5283f-113">See also</span></span>

- [<span data-ttu-id="5283f-114">ICorDebugManagedCallback, interface</span><span class="sxs-lookup"><span data-stu-id="5283f-114">ICorDebugManagedCallback Interface</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugmanagedcallback-interface.md)
