---
title: ICorDebugILFrame2, interface
ms.date: 03/30/2017
api_name:
- ICorDebugILFrame2
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugILFrame2
helpviewer_keywords:
- ICorDebugILFrame2 interface [.NET Framework debugging]
ms.assetid: f94b9d53-d8f8-4424-a95e-53a1bfd26e4a
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: a4f57f27ec92e7977b46ebfa5967b0590674d2a1
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59113436"
---
# <a name="icordebugilframe2-interface"></a><span data-ttu-id="d973a-102">ICorDebugILFrame2, interface</span><span class="sxs-lookup"><span data-stu-id="d973a-102">ICorDebugILFrame2 Interface</span></span>

<span data-ttu-id="d973a-103">Une extension logique de l’interface ICorDebugILFrame.</span><span class="sxs-lookup"><span data-stu-id="d973a-103">A logical extension of the ICorDebugILFrame interface.</span></span>  
  
## <a name="methods"></a><span data-ttu-id="d973a-104">Méthodes</span><span class="sxs-lookup"><span data-stu-id="d973a-104">Methods</span></span>  
  
|<span data-ttu-id="d973a-105">Méthode</span><span class="sxs-lookup"><span data-stu-id="d973a-105">Method</span></span>|<span data-ttu-id="d973a-106">Description</span><span class="sxs-lookup"><span data-stu-id="d973a-106">Description</span></span>|  
|------------|-----------------|  
|[<span data-ttu-id="d973a-107">EnumerateTypeParameters, méthode</span><span class="sxs-lookup"><span data-stu-id="d973a-107">EnumerateTypeParameters Method</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugilframe2-enumeratetypeparameters-method.md)|<span data-ttu-id="d973a-108">Obtient un objet ICorDebugTypeEnum qui contienne le <xref:System.Type> paramètres dans ce frame.</span><span class="sxs-lookup"><span data-stu-id="d973a-108">Gets an ICorDebugTypeEnum object that contains the <xref:System.Type> parameters in this frame.</span></span>|  
|[<span data-ttu-id="d973a-109">RemapFunction, méthode</span><span class="sxs-lookup"><span data-stu-id="d973a-109">RemapFunction Method</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugilframe2-remapfunction-method.md)|<span data-ttu-id="d973a-110">Remappe une fonction modifiée en spécifiant le nouveau décalage MSIL.</span><span class="sxs-lookup"><span data-stu-id="d973a-110">Remaps an edited function by specifying the new MSIL offset.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="d973a-111">Notes</span><span class="sxs-lookup"><span data-stu-id="d973a-111">Remarks</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="d973a-112">Cette interface ne prend pas en charge l'appel à distance, que ce soit entre ordinateurs ou entre processus.</span><span class="sxs-lookup"><span data-stu-id="d973a-112">This interface does not support being called remotely, either cross-machine or cross-process.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="d973a-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="d973a-113">Requirements</span></span>  
 <span data-ttu-id="d973a-114">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="d973a-114">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="d973a-115">**En-tête :** CorDebug.idl, CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="d973a-115">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="d973a-116">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="d973a-116">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="d973a-117">**Versions du .NET Framework :** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="d973a-117">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="d973a-118">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d973a-118">See also</span></span>

- [<span data-ttu-id="d973a-119">Interfaces de débogage</span><span class="sxs-lookup"><span data-stu-id="d973a-119">Debugging Interfaces</span></span>](../../../../docs/framework/unmanaged-api/debugging/debugging-interfaces.md)
