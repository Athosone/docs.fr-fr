---
title: ICorDebugBlockingObjectEnum::Next, méthode
ms.date: 03/30/2017
api_name:
- ICorDebugBlockingObjectEnum.Next Method
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugBlockingObjectEnum::Next
helpviewer_keywords:
- Next method, ICorDebugBlockingObjectEnum interface [.NET Framework debugging]
- ICorDebugBlockingObjectEnum::Next method [.NET Framework debugging]
ms.assetid: 0121753f-ebea-48d0-aeb2-ed7fda76dc60
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 889c3bb2d5e0cd1feb9e592e667d47dedd4ede36
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59171143"
---
# <a name="icordebugblockingobjectenumnext-method"></a><span data-ttu-id="8832a-102">ICorDebugBlockingObjectEnum::Next, méthode</span><span class="sxs-lookup"><span data-stu-id="8832a-102">ICorDebugBlockingObjectEnum::Next Method</span></span>
<span data-ttu-id="8832a-103">Obtient le nombre spécifié de [CorDebugBlockingObject](../../../../docs/framework/unmanaged-api/debugging/cordebugblockingobject-structure.md) objets à partir de l’énumération, en commençant à la position actuelle.</span><span class="sxs-lookup"><span data-stu-id="8832a-103">Gets the specified number of [CorDebugBlockingObject](../../../../docs/framework/unmanaged-api/debugging/cordebugblockingobject-structure.md) objects from the enumeration, starting at the current position.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="8832a-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="8832a-104">Syntax</span></span>  
  
```  
HRESULT Next([in] ULONG  celt,  
             [out, size_is(celt), length_is(*pceltFetched)]  
                           CorDebugBlockingObject values[],  
             [out] ULONG *pceltFetched;  
```  
  
## <a name="parameters"></a><span data-ttu-id="8832a-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="8832a-105">Parameters</span></span>  
 `celt`  
 <span data-ttu-id="8832a-106">[in] Le nombre d’objets à récupérer.</span><span class="sxs-lookup"><span data-stu-id="8832a-106">[in] The number of objects to retrieve.</span></span>  
  
 `values`  
 <span data-ttu-id="8832a-107">[out] Un tableau de pointeurs vers [CorDebugBlockingObject](../../../../docs/framework/unmanaged-api/debugging/cordebugblockingobject-structure.md) objets.</span><span class="sxs-lookup"><span data-stu-id="8832a-107">[out] An array of pointers to [CorDebugBlockingObject](../../../../docs/framework/unmanaged-api/debugging/cordebugblockingobject-structure.md) objects.</span></span>  
  
 `pceltFetched`  
 <span data-ttu-id="8832a-108">[out] Pointeur vers le nombre d’objets qui ont été récupérées.</span><span class="sxs-lookup"><span data-stu-id="8832a-108">[out] A pointer to the number of objects that were retrieved.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="8832a-109">Valeur de retour</span><span class="sxs-lookup"><span data-stu-id="8832a-109">Return Value</span></span>  
 <span data-ttu-id="8832a-110">Cette méthode retourne les HRESULT spécifiques suivants.</span><span class="sxs-lookup"><span data-stu-id="8832a-110">This method returns the following specific HRESULTs.</span></span>  
  
|<span data-ttu-id="8832a-111">HRESULT</span><span class="sxs-lookup"><span data-stu-id="8832a-111">HRESULT</span></span>|<span data-ttu-id="8832a-112">Description</span><span class="sxs-lookup"><span data-stu-id="8832a-112">Description</span></span>|  
|-------------|-----------------|  
|<span data-ttu-id="8832a-113">S_OK</span><span class="sxs-lookup"><span data-stu-id="8832a-113">S_OK</span></span>|<span data-ttu-id="8832a-114">La commande s'est correctement terminée.</span><span class="sxs-lookup"><span data-stu-id="8832a-114">The method completed successfully.</span></span>|  
|<span data-ttu-id="8832a-115">S_FALSE</span><span class="sxs-lookup"><span data-stu-id="8832a-115">S_FALSE</span></span>|<span data-ttu-id="8832a-116">`pceltFetched` n’est pas égal à `celt`.</span><span class="sxs-lookup"><span data-stu-id="8832a-116">`pceltFetched` does not equal `celt`.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="8832a-117">Notes</span><span class="sxs-lookup"><span data-stu-id="8832a-117">Remarks</span></span>  
 <span data-ttu-id="8832a-118">Cette méthode fonctionne comme un énumérateur COM classique.</span><span class="sxs-lookup"><span data-stu-id="8832a-118">This method functions like a typical COM enumerator.</span></span>  
  
 <span data-ttu-id="8832a-119">Les valeurs du tableau d’entrée doivent être au moins de taille `celt`.</span><span class="sxs-lookup"><span data-stu-id="8832a-119">The input array values must be at least of size `celt`.</span></span> <span data-ttu-id="8832a-120">Le tableau est rempli avec une l’autre `celt` valeurs dans l’énumération ou avec toutes les valeurs restantes si moins de `celt` restent.</span><span class="sxs-lookup"><span data-stu-id="8832a-120">The array will be filled with either the next `celt` values in the enumeration or with all remaining values if fewer than `celt` remain.</span></span> <span data-ttu-id="8832a-121">Lorsque cette méthode est retournée, `pceltFetched` sera remplie avec le nombre de valeurs qui ont été récupérées.</span><span class="sxs-lookup"><span data-stu-id="8832a-121">When this method returns, `pceltFetched` will be filled with the number of values that were retrieved.</span></span> <span data-ttu-id="8832a-122">Si `values` contient des pointeurs non valides ou pointe vers une mémoire tampon qui est inférieure à `celt`, ou si `pceltFetched` est un pointeur non valide, le résultat est indéfini.</span><span class="sxs-lookup"><span data-stu-id="8832a-122">If `values` contains invalid pointers or points to a buffer that is smaller than `celt`, or if `pceltFetched` is an invalid pointer, the result is undefined.</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="8832a-123">Bien que le [CorDebugBlockingObject](../../../../docs/framework/unmanaged-api/debugging/cordebugblockingobject-structure.md) structure n’a pas besoin être libéré, l’interface « ICorDebugValue » qu’elle n’a besoin d’être publié.</span><span class="sxs-lookup"><span data-stu-id="8832a-123">Although the [CorDebugBlockingObject](../../../../docs/framework/unmanaged-api/debugging/cordebugblockingobject-structure.md) structure does not need to be released, the "ICorDebugValue" interface inside of it does need to be released.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="8832a-124">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="8832a-124">Requirements</span></span>  
 <span data-ttu-id="8832a-125">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="8832a-125">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="8832a-126">**En-tête :** CorDebug.idl, CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="8832a-126">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="8832a-127">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="8832a-127">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="8832a-128">**Versions du .NET Framework :** [!INCLUDE[net_current_v40plus](../../../../includes/net-current-v40plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="8832a-128">**.NET Framework Versions:** [!INCLUDE[net_current_v40plus](../../../../includes/net-current-v40plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="8832a-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="8832a-129">See also</span></span>

- [<span data-ttu-id="8832a-130">ICorDebugDataTarget, interface</span><span class="sxs-lookup"><span data-stu-id="8832a-130">ICorDebugDataTarget Interface</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugdatatarget-interface.md)
- [<span data-ttu-id="8832a-131">Interfaces de débogage</span><span class="sxs-lookup"><span data-stu-id="8832a-131">Debugging Interfaces</span></span>](../../../../docs/framework/unmanaged-api/debugging/debugging-interfaces.md)
- [<span data-ttu-id="8832a-132">Débogage</span><span class="sxs-lookup"><span data-stu-id="8832a-132">Debugging</span></span>](../../../../docs/framework/unmanaged-api/debugging/index.md)
