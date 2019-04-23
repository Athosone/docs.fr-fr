---
title: ICorDebugSymbolProvider::GetMethodParameterSymbols, méthode
ms.date: 03/30/2017
ms.assetid: 58b7c0b9-f6ad-4b49-b92d-0e421cfd0ec6
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 98efd1446c88c3a6c004b5a3254c9db835a43804
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59197371"
---
# <a name="icordebugsymbolprovidergetmethodparametersymbols-method"></a><span data-ttu-id="6e957-102">ICorDebugSymbolProvider::GetMethodParameterSymbols, méthode</span><span class="sxs-lookup"><span data-stu-id="6e957-102">ICorDebugSymbolProvider::GetMethodParameterSymbols Method</span></span>
<span data-ttu-id="6e957-103">Obtient les symboles de paramètre d'une méthode en fonction de l'adresse virtuelle relative (RVA) de cette méthode.</span><span class="sxs-lookup"><span data-stu-id="6e957-103">Gets a method's parameter symbols given the relative virtual address (RVA) of that method.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="6e957-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="6e957-104">Syntax</span></span>  
  
```  
HRESULT GetMethodParameterSymbols(  
   [in] ULONG32 nativeRVA,  
   [in] ULONG32 cRequestedSymbols,  
   [out] ULONG32 *pcFetchedSymbols,  
   [out, size_is(cRequestedSymbols), length_is(*pcFetchedSymbols)] ICorDebugVariableSymbol *pSymbols[]  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="6e957-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="6e957-105">Parameters</span></span>  
 `nativeRVA`  
 <span data-ttu-id="6e957-106">[in] Adresse virtuelle relative native de la méthode.</span><span class="sxs-lookup"><span data-stu-id="6e957-106">[in] The native relative virtual address of the method.</span></span>  
  
 `cRequestedSymbols`  
 <span data-ttu-id="6e957-107">[in] Nombre de symboles locaux demandés.</span><span class="sxs-lookup"><span data-stu-id="6e957-107">[in] The number of local symbols requested.</span></span>  
  
 `pcFetchedSymbols`  
 <span data-ttu-id="6e957-108">[out] Pointeur vers le nombre de symboles récupérés par la méthode.</span><span class="sxs-lookup"><span data-stu-id="6e957-108">[out] A pointer to the number of symbols retrieved by the method.</span></span>  
  
 `pcFetchedSymbols`  
 <span data-ttu-id="6e957-109">[out] Un pointeur vers un [ICorDebugVariableSymbol](../../../../docs/framework/unmanaged-api/debugging/icordebugvariablesymbol-interface.md) tableau qui contient les symboles locaux de la méthode.</span><span class="sxs-lookup"><span data-stu-id="6e957-109">[out] A pointer to an [ICorDebugVariableSymbol](../../../../docs/framework/unmanaged-api/debugging/icordebugvariablesymbol-interface.md) array that contains the method's local symbols.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="6e957-110">Notes</span><span class="sxs-lookup"><span data-stu-id="6e957-110">Remarks</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="6e957-111">Cette méthode est uniquement disponible avec .NET Native.</span><span class="sxs-lookup"><span data-stu-id="6e957-111">This method is available with .NET Native only.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="6e957-112">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="6e957-112">Requirements</span></span>  
 <span data-ttu-id="6e957-113">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="6e957-113">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="6e957-114">**En-tête :** CorDebug.idl, CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="6e957-114">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="6e957-115">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="6e957-115">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="6e957-116">**Versions du .NET Framework :** [!INCLUDE[net_46_native](../../../../includes/net-46-native-md.md)]</span><span class="sxs-lookup"><span data-stu-id="6e957-116">**.NET Framework Versions:** [!INCLUDE[net_46_native](../../../../includes/net-46-native-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="6e957-117">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="6e957-117">See also</span></span>

- [<span data-ttu-id="6e957-118">GetMethodLocalSymbols, méthode</span><span class="sxs-lookup"><span data-stu-id="6e957-118">GetMethodLocalSymbols Method</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugsymbolprovider-getmethodlocalsymbols-method.md)
- [<span data-ttu-id="6e957-119">ICorDebugSymbolProvider, interface</span><span class="sxs-lookup"><span data-stu-id="6e957-119">ICorDebugSymbolProvider Interface</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugsymbolprovider-interface.md)
- [<span data-ttu-id="6e957-120">Interfaces de débogage</span><span class="sxs-lookup"><span data-stu-id="6e957-120">Debugging Interfaces</span></span>](../../../../docs/framework/unmanaged-api/debugging/debugging-interfaces.md)
