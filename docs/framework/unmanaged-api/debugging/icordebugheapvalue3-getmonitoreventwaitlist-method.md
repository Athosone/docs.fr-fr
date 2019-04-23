---
title: ICorDebugHeapValue3::GetMonitorEventWaitList, méthode
ms.date: 03/30/2017
api_name:
- ICorDebugHeapValue3.GetMonitorEventWaitList
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugHeapValue3::GetMonitorEventWaitList
helpviewer_keywords:
- ICorDebugHeapValue3::GetMonitorEventWaitList method [.NET Framework debugging]
- GetMonitorEventWaitList method [.NET Framework debugging]
ms.assetid: 035a9035-ac66-4953-b48a-99652b42b7fe
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: db331d75244d59aacf2207a6b83a3f337a64b989
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59102789"
---
# <a name="icordebugheapvalue3getmonitoreventwaitlist-method"></a><span data-ttu-id="9c739-102">ICorDebugHeapValue3::GetMonitorEventWaitList, méthode</span><span class="sxs-lookup"><span data-stu-id="9c739-102">ICorDebugHeapValue3::GetMonitorEventWaitList Method</span></span>
<span data-ttu-id="9c739-103">Fournit une liste ordonnée de threads qui sont en attente sur l’événement qui est associé à un verrou du moniteur.</span><span class="sxs-lookup"><span data-stu-id="9c739-103">Provides an ordered list of threads that are queued on the event that is associated with a monitor lock.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="9c739-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="9c739-104">Syntax</span></span>  
  
```  
HRESULT GetMonitorEventWaitList (  
    [out] ICorDebugThreadEnum **ppThreadEnum  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="9c739-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="9c739-105">Parameters</span></span>  
 `ppThreadEnum`  
 <span data-ttu-id="9c739-106">[out] L’énumérateur ICorDebugThreadEnum qui fournit la liste ordonnée des threads.</span><span class="sxs-lookup"><span data-stu-id="9c739-106">[out] The ICorDebugThreadEnum enumerator that provides the ordered list of threads.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="9c739-107">Valeur de retour</span><span class="sxs-lookup"><span data-stu-id="9c739-107">Return Value</span></span>  
 <span data-ttu-id="9c739-108">Cette méthode retourne les HRESULT spécifiques suivants ainsi que les erreurs HRESULT indiquant l'échec de la méthode.</span><span class="sxs-lookup"><span data-stu-id="9c739-108">This method returns the following specific HRESULTs as well as HRESULT errors that indicate method failure.</span></span>  
  
|<span data-ttu-id="9c739-109">HRESULT</span><span class="sxs-lookup"><span data-stu-id="9c739-109">HRESULT</span></span>|<span data-ttu-id="9c739-110">Description</span><span class="sxs-lookup"><span data-stu-id="9c739-110">Description</span></span>|  
|-------------|-----------------|  
|<span data-ttu-id="9c739-111">S_OK</span><span class="sxs-lookup"><span data-stu-id="9c739-111">S_OK</span></span>|<span data-ttu-id="9c739-112">The list is not empty.</span><span class="sxs-lookup"><span data-stu-id="9c739-112">The list is not empty.</span></span>|  
|<span data-ttu-id="9c739-113">S_FALSE</span><span class="sxs-lookup"><span data-stu-id="9c739-113">S_FALSE</span></span>|<span data-ttu-id="9c739-114">La liste est vide.</span><span class="sxs-lookup"><span data-stu-id="9c739-114">The list is empty.</span></span>|  
  
## <a name="exceptions"></a><span data-ttu-id="9c739-115">Exceptions</span><span class="sxs-lookup"><span data-stu-id="9c739-115">Exceptions</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="9c739-116">Notes</span><span class="sxs-lookup"><span data-stu-id="9c739-116">Remarks</span></span>  
 <span data-ttu-id="9c739-117">Le premier thread dans la liste est le premier thread est libéré par l’appel suivant à <xref:System.Threading.Monitor.Pulse%28System.Object%29?displayProperty=nameWithType>.</span><span class="sxs-lookup"><span data-stu-id="9c739-117">The first thread in the list is the first thread that is released by the next call to <xref:System.Threading.Monitor.Pulse%28System.Object%29?displayProperty=nameWithType>.</span></span> <span data-ttu-id="9c739-118">Le thread suivant dans la liste est publié sur l’appel suivant et ainsi de suite.</span><span class="sxs-lookup"><span data-stu-id="9c739-118">The next thread in the list is released on the following call, and so on.</span></span>  
  
 <span data-ttu-id="9c739-119">Si la liste n’est pas vide, cette méthode retourne S_OK.</span><span class="sxs-lookup"><span data-stu-id="9c739-119">If the list is not empty, this method returns S_OK.</span></span> <span data-ttu-id="9c739-120">Si la liste est vide, la méthode retourne S_FALSE ; Dans ce cas, l’énumération est toujours valide, bien qu’il soit vide.</span><span class="sxs-lookup"><span data-stu-id="9c739-120">If the list is empty, the method returns S_FALSE; in this case, the enumeration is still valid, although it is empty.</span></span>  
  
 <span data-ttu-id="9c739-121">Dans les deux cas, l’interface d’énumération est utilisable uniquement pour la durée de l’état synchronisé actuel.</span><span class="sxs-lookup"><span data-stu-id="9c739-121">In either case, the enumeration interface is usable only for the duration of the current synchronized state.</span></span> <span data-ttu-id="9c739-122">Toutefois, les interfaces du thread distribuées à partir de celui-ci sont valides jusqu'à ce que le thread se termine.</span><span class="sxs-lookup"><span data-stu-id="9c739-122">However, the thread's interfaces dispensed from it are valid until the thread exits.</span></span>  
  
 <span data-ttu-id="9c739-123">Si `ppThreadEnum` n’est pas un pointeur valide, le résultat est indéfini.</span><span class="sxs-lookup"><span data-stu-id="9c739-123">If `ppThreadEnum` is not a valid pointer, the result is undefined.</span></span>  
  
 <span data-ttu-id="9c739-124">Si une erreur se produit et il est impossible de déterminer qui, le cas échéant, les threads sont en attente pour l’analyse, la méthode retourne un HRESULT qui indique un échec.</span><span class="sxs-lookup"><span data-stu-id="9c739-124">If an error occurs such that it cannot be determined which, if any, threads are waiting for the monitor, the method returns an HRESULT that indicates failure.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="9c739-125">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="9c739-125">Requirements</span></span>  
 <span data-ttu-id="9c739-126">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="9c739-126">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="9c739-127">**En-tête :** CorDebug.idl, CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="9c739-127">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="9c739-128">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="9c739-128">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="9c739-129">**Versions du .NET Framework :** [!INCLUDE[net_current_v40plus](../../../../includes/net-current-v40plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="9c739-129">**.NET Framework Versions:** [!INCLUDE[net_current_v40plus](../../../../includes/net-current-v40plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="9c739-130">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="9c739-130">See also</span></span>

- [<span data-ttu-id="9c739-131">Interfaces de débogage</span><span class="sxs-lookup"><span data-stu-id="9c739-131">Debugging Interfaces</span></span>](../../../../docs/framework/unmanaged-api/debugging/debugging-interfaces.md)
- [<span data-ttu-id="9c739-132">Débogage</span><span class="sxs-lookup"><span data-stu-id="9c739-132">Debugging</span></span>](../../../../docs/framework/unmanaged-api/debugging/index.md)
