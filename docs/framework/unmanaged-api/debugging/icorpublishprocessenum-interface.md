---
title: ICorPublishProcessEnum, interface
ms.date: 03/30/2017
api_name:
- ICorPublishProcessEnum
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorPublishProcessEnum
helpviewer_keywords:
- ICorPublishProcessEnum interface [.NET Framework debugging]
ms.assetid: aac8fcf9-ac09-437c-bd5c-2fda14ae1007
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 5186df61eb82b29fcfa9776408498b748068e122
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59173652"
---
# <a name="icorpublishprocessenum-interface"></a><span data-ttu-id="fe6be-102">ICorPublishProcessEnum, interface</span><span class="sxs-lookup"><span data-stu-id="fe6be-102">ICorPublishProcessEnum Interface</span></span>
<span data-ttu-id="fe6be-103">Une sous-classe de la [ICorPublishEnum](../../../../docs/framework/unmanaged-api/debugging/icorpublishenum-interface.md) interface qui fournit des méthodes pour parcourir une collection de [ICorPublishProcess](../../../../docs/framework/unmanaged-api/debugging/icorpublishprocess-interface.md) objets.</span><span class="sxs-lookup"><span data-stu-id="fe6be-103">A subclass of the [ICorPublishEnum](../../../../docs/framework/unmanaged-api/debugging/icorpublishenum-interface.md) interface that provides methods to traverse a collection of [ICorPublishProcess](../../../../docs/framework/unmanaged-api/debugging/icorpublishprocess-interface.md) objects.</span></span>  
  
## <a name="methods"></a><span data-ttu-id="fe6be-104">Méthodes</span><span class="sxs-lookup"><span data-stu-id="fe6be-104">Methods</span></span>  
  
|<span data-ttu-id="fe6be-105">Méthode</span><span class="sxs-lookup"><span data-stu-id="fe6be-105">Method</span></span>|<span data-ttu-id="fe6be-106">Description</span><span class="sxs-lookup"><span data-stu-id="fe6be-106">Description</span></span>|  
|------------|-----------------|  
|[<span data-ttu-id="fe6be-107">Next, méthode</span><span class="sxs-lookup"><span data-stu-id="fe6be-107">Next Method</span></span>](../../../../docs/framework/unmanaged-api/debugging/icorpublishprocessenum-next-method.md)|<span data-ttu-id="fe6be-108">Obtient le nombre spécifié de `ICorPublishProcess` instances à partir de la collection, en commençant à la position actuelle.</span><span class="sxs-lookup"><span data-stu-id="fe6be-108">Gets the specified number of `ICorPublishProcess` instances from the collection, starting at the current position.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="fe6be-109">Notes</span><span class="sxs-lookup"><span data-stu-id="fe6be-109">Remarks</span></span>  
 <span data-ttu-id="fe6be-110">Le `ICorPublishProcessEnum` interface implémente les méthodes de l’interface abstraite, [ICorPublishEnum](../../../../docs/framework/unmanaged-api/debugging/icorpublishenum-interface.md).</span><span class="sxs-lookup"><span data-stu-id="fe6be-110">The `ICorPublishProcessEnum` interface implements the methods of the abstract interface, [ICorPublishEnum](../../../../docs/framework/unmanaged-api/debugging/icorpublishenum-interface.md).</span></span>  
  
 <span data-ttu-id="fe6be-111">Un `ICorPublishProcessEnum` instance est créée par le [ICorPublish::EnumProcesses](../../../../docs/framework/unmanaged-api/debugging/icorpublish-enumprocesses-method.md) (méthode).</span><span class="sxs-lookup"><span data-stu-id="fe6be-111">An `ICorPublishProcessEnum` instance is created by the [ICorPublish::EnumProcesses](../../../../docs/framework/unmanaged-api/debugging/icorpublish-enumprocesses-method.md) method.</span></span> <span data-ttu-id="fe6be-112">Le parcours de la collection de `ICorPublishProcess` objets est basée sur les critères de filtre fournis au moment où le `ICorPublishProcessEnum` instance a été créée.</span><span class="sxs-lookup"><span data-stu-id="fe6be-112">The traversal of the collection of `ICorPublishProcess` objects is based on the filter criteria given at the time the `ICorPublishProcessEnum` instance was created.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="fe6be-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="fe6be-113">Requirements</span></span>  
 <span data-ttu-id="fe6be-114">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="fe6be-114">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="fe6be-115">**En-tête :** CorPub.idl, CorPub.h</span><span class="sxs-lookup"><span data-stu-id="fe6be-115">**Header:** CorPub.idl, CorPub.h</span></span>  
  
 <span data-ttu-id="fe6be-116">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="fe6be-116">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="fe6be-117">**Versions du .NET Framework :** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="fe6be-117">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="fe6be-118">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="fe6be-118">See also</span></span>

- [<span data-ttu-id="fe6be-119">Interfaces de débogage</span><span class="sxs-lookup"><span data-stu-id="fe6be-119">Debugging Interfaces</span></span>](../../../../docs/framework/unmanaged-api/debugging/debugging-interfaces.md)
- [<span data-ttu-id="fe6be-120">CorpubPublish, coclasse</span><span class="sxs-lookup"><span data-stu-id="fe6be-120">CorpubPublish Coclass</span></span>](../../../../docs/framework/unmanaged-api/debugging/corpubpublish-coclass.md)
