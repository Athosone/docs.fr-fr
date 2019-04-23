---
title: ICorDebugClass, interface
ms.date: 03/30/2017
api_name:
- ICorDebugClass
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugClass
helpviewer_keywords:
- ICorDebugClass interface [.NET Framework debugging]
ms.assetid: 03a6facb-f12f-49be-9839-e73b9c791cd5
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 7e1ad830e728fbe764085a5808a48e4cacedc595
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59133625"
---
# <a name="icordebugclass-interface"></a><span data-ttu-id="90c4d-102">ICorDebugClass, interface</span><span class="sxs-lookup"><span data-stu-id="90c4d-102">ICorDebugClass Interface</span></span>

<span data-ttu-id="90c4d-103">Représente un type, qui peut être de base ou complexe (c'est-à-dire défini par l'utilisateur).</span><span class="sxs-lookup"><span data-stu-id="90c4d-103">Represents a type, which can be either basic or complex (that is, user-defined).</span></span> <span data-ttu-id="90c4d-104">Si le type est générique, `ICorDebugClass` représente le type générique non instancié.</span><span class="sxs-lookup"><span data-stu-id="90c4d-104">If the type is generic, `ICorDebugClass` represents the uninstantiated generic type.</span></span>  
  
## <a name="methods"></a><span data-ttu-id="90c4d-105">Méthodes</span><span class="sxs-lookup"><span data-stu-id="90c4d-105">Methods</span></span>  
  
|<span data-ttu-id="90c4d-106">Méthode</span><span class="sxs-lookup"><span data-stu-id="90c4d-106">Method</span></span>|<span data-ttu-id="90c4d-107">Description</span><span class="sxs-lookup"><span data-stu-id="90c4d-107">Description</span></span>|  
|------------|-----------------|  
|[<span data-ttu-id="90c4d-108">GetModule, méthode</span><span class="sxs-lookup"><span data-stu-id="90c4d-108">GetModule Method</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugclass-getmodule-method.md)|<span data-ttu-id="90c4d-109">Obtient le module qui définit cette classe.</span><span class="sxs-lookup"><span data-stu-id="90c4d-109">Gets the module that defines this class.</span></span>|  
|[<span data-ttu-id="90c4d-110">GetStaticFieldValue, méthode</span><span class="sxs-lookup"><span data-stu-id="90c4d-110">GetStaticFieldValue Method</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugclass-getstaticfieldvalue-method.md)|<span data-ttu-id="90c4d-111">Obtient la valeur du champ statique spécifié.</span><span class="sxs-lookup"><span data-stu-id="90c4d-111">Gets the value of the specified static field.</span></span>|  
|[<span data-ttu-id="90c4d-112">GetToken, méthode</span><span class="sxs-lookup"><span data-stu-id="90c4d-112">GetToken Method</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugclass-gettoken-method.md)|<span data-ttu-id="90c4d-113">Obtient le `TypeDef` jeton de métadonnées pour cette classe.</span><span class="sxs-lookup"><span data-stu-id="90c4d-113">Gets the `TypeDef` metadata token for this class.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="90c4d-114">Notes</span><span class="sxs-lookup"><span data-stu-id="90c4d-114">Remarks</span></span>  
 <span data-ttu-id="90c4d-115">Le `ICorDebugClass` interface représente un type générique non instancié.</span><span class="sxs-lookup"><span data-stu-id="90c4d-115">The `ICorDebugClass` interface represents an uninstantiated generic type.</span></span> <span data-ttu-id="90c4d-116">L’interface de ICorDebugType représente un type générique instancié.</span><span class="sxs-lookup"><span data-stu-id="90c4d-116">The ICorDebugType interface represents an instantiated generic type.</span></span> <span data-ttu-id="90c4d-117">Par exemple, `Hashtable<K, V>` serait représenté par `ICorDebugClass`, tandis que `Hashtable<Int32, String>` serait représenté par `ICorDebugType`.</span><span class="sxs-lookup"><span data-stu-id="90c4d-117">For example, `Hashtable<K, V>` would be represented by `ICorDebugClass`, whereas `Hashtable<Int32, String>` would be represented by `ICorDebugType`.</span></span>  
  
 <span data-ttu-id="90c4d-118">Les types non génériques sont représentés par les deux `ICorDebugClass` et `ICorDebugType`.</span><span class="sxs-lookup"><span data-stu-id="90c4d-118">Non-generic types are represented by both `ICorDebugClass` and `ICorDebugType`.</span></span> <span data-ttu-id="90c4d-119">L’interface de ce dernier a été introduite dans le .NET Framework version 2.0 pour gérer l’instanciation de type.</span><span class="sxs-lookup"><span data-stu-id="90c4d-119">The latter interface was introduced in the .NET Framework version 2.0 to deal with type instantiation.</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="90c4d-120">Cette interface ne prend pas en charge l'appel à distance, que ce soit entre ordinateurs ou entre processus.</span><span class="sxs-lookup"><span data-stu-id="90c4d-120">This interface does not support being called remotely, either cross-machine or cross-process.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="90c4d-121">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="90c4d-121">Requirements</span></span>  
 <span data-ttu-id="90c4d-122">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="90c4d-122">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="90c4d-123">**En-tête :** CorDebug.idl, CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="90c4d-123">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="90c4d-124">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="90c4d-124">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="90c4d-125">**Versions du .NET Framework :** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="90c4d-125">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="90c4d-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="90c4d-126">See also</span></span>

- [<span data-ttu-id="90c4d-127">Interfaces de débogage</span><span class="sxs-lookup"><span data-stu-id="90c4d-127">Debugging Interfaces</span></span>](../../../../docs/framework/unmanaged-api/debugging/debugging-interfaces.md)
