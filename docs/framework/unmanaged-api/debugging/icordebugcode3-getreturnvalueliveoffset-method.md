---
title: ICorDebugCode3::GetReturnValueLiveOffset, méthode
ms.date: 03/30/2017
dev_langs:
- cpp
api_name:
- ICorDebugCode3.GetReturnValueLiveOffset
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugCode3::GetReturnValueLiveOffset
helpviewer_keywords:
- ICorDebugCode3::GetReturnValueLiveOffset method [.NET Framework debugging]
- GetReturnValueLiveOffset method [.NET Framework debugging]
ms.assetid: 8c2ff5d8-8c04-4423-b1e1-e1c8764b36d3
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 03ee275336d3ae71f63d82add694fe1308efbe8b
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61750060"
---
# <a name="icordebugcode3getreturnvalueliveoffset-method"></a><span data-ttu-id="cb237-102">ICorDebugCode3::GetReturnValueLiveOffset, méthode</span><span class="sxs-lookup"><span data-stu-id="cb237-102">ICorDebugCode3::GetReturnValueLiveOffset Method</span></span>
<span data-ttu-id="cb237-103">Pour un offset IL spécifié, obtient les offsets natifs où un point d’arrêt doit être placé afin que le débogueur puisse obtenir la valeur de retour d’une fonction.</span><span class="sxs-lookup"><span data-stu-id="cb237-103">For a specified IL offset, gets the native offsets where a breakpoint should be placed so that the debugger can obtain the return value from a function.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="cb237-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="cb237-104">Syntax</span></span>  
  
```cpp
HRESULT GetReturnValueLiveOffset(  
    [in] ULONG32 ILoffset,  
    [in] ULONG32 bufferSize,   
    [out] ULONG32 *pFetched,   
    [out, size_is(buffersize), length_is(*pFetched)] ULong32 pOffsets[]  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="cb237-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="cb237-105">Parameters</span></span>  
 `ILoffset`  
 <span data-ttu-id="cb237-106">Offset IL.</span><span class="sxs-lookup"><span data-stu-id="cb237-106">The IL offset.</span></span> <span data-ttu-id="cb237-107">Il doit être un site d’appel de fonction ou l’appel de fonction échoue.</span><span class="sxs-lookup"><span data-stu-id="cb237-107">It must be a function call site or the function call will fail.</span></span>  
  
 `bufferSize`  
 <span data-ttu-id="cb237-108">Le nombre d’octets pour stocker `pOffsets`.</span><span class="sxs-lookup"><span data-stu-id="cb237-108">The number of bytes available to store `pOffsets`.</span></span>  
  
 `pFetched`  
 <span data-ttu-id="cb237-109">Pointeur vers le nombre de décalages réellement retournés.</span><span class="sxs-lookup"><span data-stu-id="cb237-109">A pointer to the number of offsets actually returned.</span></span> <span data-ttu-id="cb237-110">En règle générale, sa valeur est 1, mais une seule instruction IL peut mapper à plusieurs `CALL` instructions assembleur.</span><span class="sxs-lookup"><span data-stu-id="cb237-110">Usually, its value is 1, but a single IL instruction can map to multiple `CALL` assembly instructions.</span></span>  
  
 `pOffsets`  
 <span data-ttu-id="cb237-111">Tableau d’offsets natifs.</span><span class="sxs-lookup"><span data-stu-id="cb237-111">An array of native offsets.</span></span> <span data-ttu-id="cb237-112">En règle générale, `pOffsets` contient un offset unique, bien qu’une seule instruction IL peut mapper à plusieurs cartes à plusieurs `CALL` instructions assembleur.</span><span class="sxs-lookup"><span data-stu-id="cb237-112">Typically, `pOffsets` contains a single offset, although a single IL instruction can map to multiple map to multiple `CALL` assembly instructions.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="cb237-113">Notes</span><span class="sxs-lookup"><span data-stu-id="cb237-113">Remarks</span></span>  
 <span data-ttu-id="cb237-114">Cette méthode est utilisée avec la [ICorDebugILFrame3::GetReturnValueForILOffset](../../../../docs/framework/unmanaged-api/debugging/icordebugilframe3-getreturnvalueforiloffset-method.md) méthode pour obtenir la valeur de retour d’une méthode qui retourne un type référence.</span><span class="sxs-lookup"><span data-stu-id="cb237-114">This method is used along with the [ICorDebugILFrame3::GetReturnValueForILOffset](../../../../docs/framework/unmanaged-api/debugging/icordebugilframe3-getreturnvalueforiloffset-method.md) method to get the return value of a method that returns a reference type.</span></span> <span data-ttu-id="cb237-115">En passant un offset IL à un site d’appel de fonction à cette méthode retourne un ou plusieurs offsets natifs.</span><span class="sxs-lookup"><span data-stu-id="cb237-115">Passing an IL offset to a function call site to this method returns one or more native offsets.</span></span> <span data-ttu-id="cb237-116">Le débogueur peut ensuite définir des points d’arrêt sur ces offsets natifs dans la fonction.</span><span class="sxs-lookup"><span data-stu-id="cb237-116">The debugger can then set breakpoints on these native offsets in the function.</span></span> <span data-ttu-id="cb237-117">Lorsque le débogueur atteint un des points d’arrêt, vous pouvez ensuite passer le même offset IL que vous avez passé à cette méthode pour le [ICorDebugILFrame3::GetReturnValueForILOffset](../../../../docs/framework/unmanaged-api/debugging/icordebugilframe3-getreturnvalueforiloffset-method.md) méthode pour obtenir la valeur de retour.</span><span class="sxs-lookup"><span data-stu-id="cb237-117">When the debugger hits one of the breakpoints, you can then pass the same IL offset that you passed to this method to the [ICorDebugILFrame3::GetReturnValueForILOffset](../../../../docs/framework/unmanaged-api/debugging/icordebugilframe3-getreturnvalueforiloffset-method.md) method to get the return value.</span></span> <span data-ttu-id="cb237-118">Le débogueur doit ensuite effacer tous les points d’arrêt qu’il a définis.</span><span class="sxs-lookup"><span data-stu-id="cb237-118">The debugger should then clear all the breakpoints that it set.</span></span>  
  
> [!WARNING]
>  <span data-ttu-id="cb237-119">Le `ICorDebugCode3::GetReturnValueLiveOffset` et [ICorDebugILFrame3::GetReturnValueForILOffset](../../../../docs/framework/unmanaged-api/debugging/icordebugilframe3-getreturnvalueforiloffset-method.md) méthodes permettent d’obtenir des informations de valeur de retour pour les types de référence uniquement.</span><span class="sxs-lookup"><span data-stu-id="cb237-119">The `ICorDebugCode3::GetReturnValueLiveOffset` and [ICorDebugILFrame3::GetReturnValueForILOffset](../../../../docs/framework/unmanaged-api/debugging/icordebugilframe3-getreturnvalueforiloffset-method.md) methods allow you to get return value information for reference types only.</span></span> <span data-ttu-id="cb237-120">Récupération des informations de valeur de retour dans les types valeur (autrement dit, tous les types qui dérivent <xref:System.ValueType>) n’est pas pris en charge.</span><span class="sxs-lookup"><span data-stu-id="cb237-120">Retrieving return value information from value types (that is, all types that derive from <xref:System.ValueType>) is not supported.</span></span>  
  
 <span data-ttu-id="cb237-121">La fonction retourne le `HRESULT` valeurs indiquées dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="cb237-121">The function returns the `HRESULT` values shown in the following table.</span></span>  
  
|<span data-ttu-id="cb237-122">Valeur`HRESULT` </span><span class="sxs-lookup"><span data-stu-id="cb237-122">`HRESULT` value</span></span>|<span data-ttu-id="cb237-123">Description</span><span class="sxs-lookup"><span data-stu-id="cb237-123">Description</span></span>|  
|---------------------|-----------------|  
|`S_OK`|<span data-ttu-id="cb237-124">Opération réussie.</span><span class="sxs-lookup"><span data-stu-id="cb237-124">Success.</span></span>|  
|`CORDBG_E_INVALID_OPCODE`|<span data-ttu-id="cb237-125">Le site offset IL donné n’est pas une instruction d’appel, ou la fonction retourne `void`.</span><span class="sxs-lookup"><span data-stu-id="cb237-125">The given IL offset site is not a call instruction, or the function returns `void`.</span></span>|  
|`CORDBG_E_UNSUPPORTED`|<span data-ttu-id="cb237-126">L’offset IL donné est un appel approprié, mais le type de retour non pris en charge pour l’obtention d’une valeur de retour.</span><span class="sxs-lookup"><span data-stu-id="cb237-126">The given IL offset is a proper call, but the return type is unsupported for getting a return value.</span></span>|  
  
 <span data-ttu-id="cb237-127">Le `ICorDebugCode3::GetReturnValueLiveOffset` méthode n’est disponible uniquement sur x86 et les systèmes AMD64.</span><span class="sxs-lookup"><span data-stu-id="cb237-127">The `ICorDebugCode3::GetReturnValueLiveOffset` method is available only on x86-based and AMD64 systems.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="cb237-128">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="cb237-128">Requirements</span></span>  
 <span data-ttu-id="cb237-129">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="cb237-129">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="cb237-130">**En-tête :** CorDebug.idl, CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="cb237-130">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="cb237-131">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="cb237-131">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="cb237-132">**Versions du .NET Framework :** [!INCLUDE[net_current_v451plus](../../../../includes/net-current-v451plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="cb237-132">**.NET Framework Versions:** [!INCLUDE[net_current_v451plus](../../../../includes/net-current-v451plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="cb237-133">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="cb237-133">See also</span></span>

- [<span data-ttu-id="cb237-134">GetReturnValueForILOffset, méthode</span><span class="sxs-lookup"><span data-stu-id="cb237-134">GetReturnValueForILOffset Method</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugilframe3-getreturnvalueforiloffset-method.md)
- [<span data-ttu-id="cb237-135">ICorDebugCode3, interface</span><span class="sxs-lookup"><span data-stu-id="cb237-135">ICorDebugCode3 Interface</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugcode3-interface.md)
