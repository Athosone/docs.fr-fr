---
title: ICorDebugThread4, interface
ms.date: 03/30/2017
api_name:
- ICorDebugThread4
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugThread4
helpviewer_keywords:
- ICorDebugThread4 interface [.NET Framework debugging]
ms.assetid: a8c7719a-322b-4133-8566-4c27218dc104
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: f213a35a12bfb5cc92558a76e122a1494d567f93
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59170792"
---
# <a name="icordebugthread4-interface"></a><span data-ttu-id="b8a25-102">ICorDebugThread4, interface</span><span class="sxs-lookup"><span data-stu-id="b8a25-102">ICorDebugThread4 Interface</span></span>
<span data-ttu-id="b8a25-103">Fournit des informations sur le blocage des threads.</span><span class="sxs-lookup"><span data-stu-id="b8a25-103">Provides thread blocking information.</span></span>  
  
## <a name="methods"></a><span data-ttu-id="b8a25-104">Méthodes</span><span class="sxs-lookup"><span data-stu-id="b8a25-104">Methods</span></span>  
  
|<span data-ttu-id="b8a25-105">Méthode</span><span class="sxs-lookup"><span data-stu-id="b8a25-105">Method</span></span>|<span data-ttu-id="b8a25-106">Description</span><span class="sxs-lookup"><span data-stu-id="b8a25-106">Description</span></span>|  
|------------|-----------------|  
|[<span data-ttu-id="b8a25-107">GetBlockingObjects, méthode</span><span class="sxs-lookup"><span data-stu-id="b8a25-107">GetBlockingObjects Method</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugthread4-getblockingobjects-method.md)|<span data-ttu-id="b8a25-108">Fournit une énumération ordonnée de [CorDebugBlockingObject](../../../../docs/framework/unmanaged-api/debugging/cordebugblockingobject-structure.md) structures qui fournissent des informations de blocage de thread.</span><span class="sxs-lookup"><span data-stu-id="b8a25-108">Provides an ordered enumeration of [CorDebugBlockingObject](../../../../docs/framework/unmanaged-api/debugging/cordebugblockingobject-structure.md) structures that provide thread blocking information.</span></span>|  
|[<span data-ttu-id="b8a25-109">HadUnhandledException, méthode</span><span class="sxs-lookup"><span data-stu-id="b8a25-109">HadUnhandledException Method</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugthread4-hadunhandledexception-method.md)|<span data-ttu-id="b8a25-110">Indique si le thread a déjà eu une exception non gérée.</span><span class="sxs-lookup"><span data-stu-id="b8a25-110">Indicates whether the thread has ever had an unhandled exception.</span></span>|  
|[<span data-ttu-id="b8a25-111">GetCurrentCustomDebuggerNotification, méthode</span><span class="sxs-lookup"><span data-stu-id="b8a25-111">GetCurrentCustomDebuggerNotification Method</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugthread4-getcurrentcustomdebuggernotification-method.md)|<span data-ttu-id="b8a25-112">Obtient les valeurs combinées [ICorDebugManagedCallback3::CustomNotification](../../../../docs/framework/unmanaged-api/debugging/icordebugmanagedcallback3-customnotification-method.md) objet sur le thread actuel.</span><span class="sxs-lookup"><span data-stu-id="b8a25-112">Gets the current [ICorDebugManagedCallback3::CustomNotification](../../../../docs/framework/unmanaged-api/debugging/icordebugmanagedcallback3-customnotification-method.md) object on the current thread.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="b8a25-113">Notes</span><span class="sxs-lookup"><span data-stu-id="b8a25-113">Remarks</span></span>  
 <span data-ttu-id="b8a25-114">Cette interface est une extension logique de ICorDebugThread, ICorDebugThread2, et [ICorDebugThread3](../../../../docs/framework/unmanaged-api/debugging/icordebugthread3-interface.md) interfaces.</span><span class="sxs-lookup"><span data-stu-id="b8a25-114">This interface is a logical extension of the ICorDebugThread, ICorDebugThread2, and [ICorDebugThread3](../../../../docs/framework/unmanaged-api/debugging/icordebugthread3-interface.md) interfaces.</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="b8a25-115">Cette interface ne prend pas en charge l'appel à distance, que ce soit entre ordinateurs ou entre processus.</span><span class="sxs-lookup"><span data-stu-id="b8a25-115">This interface does not support being called remotely, either cross-machine or cross-process.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="b8a25-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="b8a25-116">Requirements</span></span>  
 <span data-ttu-id="b8a25-117">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="b8a25-117">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="b8a25-118">**En-tête :** CorDebug.idl, CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="b8a25-118">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="b8a25-119">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="b8a25-119">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="b8a25-120">**Versions du .NET Framework :** [!INCLUDE[net_current_v40plus](../../../../includes/net-current-v40plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="b8a25-120">**.NET Framework Versions:** [!INCLUDE[net_current_v40plus](../../../../includes/net-current-v40plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="b8a25-121">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b8a25-121">See also</span></span>

- [<span data-ttu-id="b8a25-122">Interfaces de débogage</span><span class="sxs-lookup"><span data-stu-id="b8a25-122">Debugging Interfaces</span></span>](../../../../docs/framework/unmanaged-api/debugging/debugging-interfaces.md)
- [<span data-ttu-id="b8a25-123">Débogage</span><span class="sxs-lookup"><span data-stu-id="b8a25-123">Debugging</span></span>](../../../../docs/framework/unmanaged-api/debugging/index.md)
