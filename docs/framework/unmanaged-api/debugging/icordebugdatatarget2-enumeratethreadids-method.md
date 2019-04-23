---
title: ICorDebugDataTarget2::EnumerateThreadIDs, méthode
ms.date: 03/30/2017
ms.assetid: af02460f-2a45-496e-bc4e-a1ac4f80fe11
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 70b3b57b51faed51aa7d5a70a3b785e0f719321b
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59215838"
---
# <a name="icordebugdatatarget2enumeratethreadids-method"></a><span data-ttu-id="ca755-102">ICorDebugDataTarget2::EnumerateThreadIDs, méthode</span><span class="sxs-lookup"><span data-stu-id="ca755-102">ICorDebugDataTarget2::EnumerateThreadIDs Method</span></span>
<span data-ttu-id="ca755-103">Retourne une liste des ID de threads actifs.</span><span class="sxs-lookup"><span data-stu-id="ca755-103">Returns a list of active thread IDs.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="ca755-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="ca755-104">Syntax</span></span>  
  
```  
HRESULT EnumerateThreadIDs(  
    [in] ULONG32 cThreadIds,   
    [out] ULONG32 *pcThreadIds,   
    [out, size_is(cThreadIds), length_is(*pcThreadIds)] ULONG32 pThreadIds[]  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="ca755-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="ca755-105">Parameters</span></span>  
 <span data-ttu-id="ca755-106">cThreadIDs</span><span class="sxs-lookup"><span data-stu-id="ca755-106">cThreadIDs</span></span>  
 <span data-ttu-id="ca755-107">[in] Nombre maximal de threads dont les ID peuvent être retournés.</span><span class="sxs-lookup"><span data-stu-id="ca755-107">[in] The maximum number of threads whose IDs can be returned.</span></span>  
  
 <span data-ttu-id="ca755-108">pcThreadIds</span><span class="sxs-lookup"><span data-stu-id="ca755-108">pcThreadIds</span></span>  
 <span data-ttu-id="ca755-109">[out] Pointeur vers un `ULONG32` qui indique le nombre réel d'ID de threads ayant été écrits dans le tableau `pThreadIds`.</span><span class="sxs-lookup"><span data-stu-id="ca755-109">[out] A pointer to a `ULONG32` that indicates the actual number of thread IDs written to the `pThreadIds` array.</span></span>  
  
 <span data-ttu-id="ca755-110">pThreadIDs</span><span class="sxs-lookup"><span data-stu-id="ca755-110">pThreadIDs</span></span>  
 <span data-ttu-id="ca755-111">Tableau d'identificateurs de threads.</span><span class="sxs-lookup"><span data-stu-id="ca755-111">An array of thread identifiers.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="ca755-112">Notes</span><span class="sxs-lookup"><span data-stu-id="ca755-112">Remarks</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="ca755-113">Cette méthode est uniquement disponible avec .NET Native.</span><span class="sxs-lookup"><span data-stu-id="ca755-113">This method is available with .NET Native only.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="ca755-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="ca755-114">Requirements</span></span>  
 <span data-ttu-id="ca755-115">**Plateformes :** Consultez [requise](../../../../docs/framework/get-started/system-requirements.md). **En-tête :** CorDebug.idl, CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="ca755-115">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="ca755-116">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="ca755-116">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="ca755-117">**Versions du .NET Framework :** [!INCLUDE[net_46_native](../../../../includes/net-46-native-md.md)]</span><span class="sxs-lookup"><span data-stu-id="ca755-117">**.NET Framework Versions:** [!INCLUDE[net_46_native](../../../../includes/net-46-native-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="ca755-118">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ca755-118">See also</span></span>

- [<span data-ttu-id="ca755-119">ICorDebugDataTarget2, interface</span><span class="sxs-lookup"><span data-stu-id="ca755-119">ICorDebugDataTarget2 Interface</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugdatatarget2-interface.md)
- [<span data-ttu-id="ca755-120">Interfaces de débogage</span><span class="sxs-lookup"><span data-stu-id="ca755-120">Debugging Interfaces</span></span>](../../../../docs/framework/unmanaged-api/debugging/debugging-interfaces.md)
