---
title: IXCLRDataProcess, interface
ms.date: 01/16/2019
api.name:
- IXCLRDataProcess Interface
api.location:
- mscordacwks.dll
api.type:
- COM
f1.keywords:
- IXCLRDataProcess Interface
helpviewer.keywords:
- IXCLRDataProcess Interface [.NET Framework debugging]
topic_type:
- apiref
author: cshung
ms.author: andrewau
ms.openlocfilehash: ff74a7acb5cc84c177f083c19402cd78977aeab5
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61775243"
---
# <a name="ixclrdataprocess-interface"></a><span data-ttu-id="8201d-102">IXCLRDataProcess, interface</span><span class="sxs-lookup"><span data-stu-id="8201d-102">IXCLRDataProcess Interface</span></span>

<span data-ttu-id="8201d-103">Fournit des méthodes pour obtenir des informations relatives à un processus.</span><span class="sxs-lookup"><span data-stu-id="8201d-103">Provides methods for querying information about a process.</span></span>

[!INCLUDE[debugging-api-recommended-note](../../../../includes/debugging-api-recommended-note.md)]

## <a name="methods"></a><span data-ttu-id="8201d-104">Méthodes</span><span class="sxs-lookup"><span data-stu-id="8201d-104">Methods</span></span>

| <span data-ttu-id="8201d-105">Méthode</span><span class="sxs-lookup"><span data-stu-id="8201d-105">Method</span></span>                                                                                                                                               | <span data-ttu-id="8201d-106">Description</span><span class="sxs-lookup"><span data-stu-id="8201d-106">Description</span></span>                                                                                     |
| ---------------------------------------------------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------- |
| [<span data-ttu-id="8201d-107">GetAppDomainByUniqueId</span><span class="sxs-lookup"><span data-stu-id="8201d-107">GetAppDomainByUniqueId</span></span>](../../../../docs/framework/unmanaged-api/debugging/ixclrdataprocess-getappdomainbyuniqueid-method.md)                       | <span data-ttu-id="8201d-108">Obtient un `AppDomain` dans un processus par son id unique.</span><span class="sxs-lookup"><span data-stu-id="8201d-108">Gets an `AppDomain` in a process by its unique id.</span></span>                                              |
| [<span data-ttu-id="8201d-109">StartEnumModules</span><span class="sxs-lookup"><span data-stu-id="8201d-109">StartEnumModules</span></span>](../../../../docs/framework/unmanaged-api/debugging/ixclrdataprocess-startenummodules-method.md)                                   | <span data-ttu-id="8201d-110">Fournit un handle pour énumérer les modules d’un processus.</span><span class="sxs-lookup"><span data-stu-id="8201d-110">Provides a handle to enumerate the modules of a process.</span></span>                                        |
| [<span data-ttu-id="8201d-111">EnumModule</span><span class="sxs-lookup"><span data-stu-id="8201d-111">EnumModule</span></span>](../../../../docs/framework/unmanaged-api/debugging/ixclrdataprocess-enummodule-method.md)                                               | <span data-ttu-id="8201d-112">Énumère les modules de ce processus.</span><span class="sxs-lookup"><span data-stu-id="8201d-112">Enumerates the modules of this process.</span></span>                                                         |
| [<span data-ttu-id="8201d-113">EndEnumModules</span><span class="sxs-lookup"><span data-stu-id="8201d-113">EndEnumModules</span></span>](../../../../docs/framework/unmanaged-api/debugging/ixclrdataprocess-endenummodules-method.md)                                       | <span data-ttu-id="8201d-114">Libère les ressources utilisées par les itérateurs internes utilisés pendant l’énumération de module.</span><span class="sxs-lookup"><span data-stu-id="8201d-114">Releases the resources used by internal iterators used during module enumeration.</span></span>               |
| [<span data-ttu-id="8201d-115">StartEnumMethodInstancesByAddress</span><span class="sxs-lookup"><span data-stu-id="8201d-115">StartEnumMethodInstancesByAddress</span></span>](../../../../docs/framework/unmanaged-api/debugging/ixclrdataprocess-startenummethodinstancesbyaddress-method.md) | <span data-ttu-id="8201d-116">Fournit un handle pour énumérer les instances de la méthode de `AppDomain` en commençant à une adresse donnée.</span><span class="sxs-lookup"><span data-stu-id="8201d-116">Provides a handle to enumerate the method instances of `AppDomain` starting at a given address.</span></span> |
| [<span data-ttu-id="8201d-117">EnumMethodInstanceByAddress</span><span class="sxs-lookup"><span data-stu-id="8201d-117">EnumMethodInstanceByAddress</span></span>](../../../../docs/framework/unmanaged-api/debugging/ixclrdataprocess-enummethodinstancebyaddress-method.md)             | <span data-ttu-id="8201d-118">Énumère les instances de la méthode de ce processus, en commençant à un offset d’adresse.</span><span class="sxs-lookup"><span data-stu-id="8201d-118">Enumerates the method instances of this process starting at an address offset.</span></span>                  |
| [<span data-ttu-id="8201d-119">EndEnumMethodInstancesByAddress</span><span class="sxs-lookup"><span data-stu-id="8201d-119">EndEnumMethodInstancesByAddress</span></span>](../../../../docs/framework/unmanaged-api/debugging/ixclrdataprocess-endenummethodinstancesbyaddress-method.md)     | <span data-ttu-id="8201d-120">Libère les ressources utilisées par les itérateurs internes utilisés pendant l’énumération de l’instance.</span><span class="sxs-lookup"><span data-stu-id="8201d-120">Releases the resources used by internal iterators used during instance enumeration.</span></span>             |

## <a name="remarks"></a><span data-ttu-id="8201d-121">Notes</span><span class="sxs-lookup"><span data-stu-id="8201d-121">Remarks</span></span>

<span data-ttu-id="8201d-122">Cette interface réside dans le runtime et n’est pas exposée par le biais d’en-têtes ou les fichiers de bibliothèque.</span><span class="sxs-lookup"><span data-stu-id="8201d-122">This interface lives inside the runtime and is not exposed through any headers or library files.</span></span> <span data-ttu-id="8201d-123">Toutefois, il est une interface COM qui dérive de `IUnknown` avec le GUID `5c552ab6-fc09-4cb3-8e36-22fa03c798b7` qui peuvent être obtenues via les mécanismes COM habituels.</span><span class="sxs-lookup"><span data-stu-id="8201d-123">However, it's a COM interface that derives from `IUnknown` with GUID `5c552ab6-fc09-4cb3-8e36-22fa03c798b7` that can be obtained through the usual COM mechanisms.</span></span>

## <a name="requirements"></a><span data-ttu-id="8201d-124">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="8201d-124">Requirements</span></span>

<span data-ttu-id="8201d-125">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="8201d-125">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>   
<span data-ttu-id="8201d-126">**En-tête :** Aucun.</span><span class="sxs-lookup"><span data-stu-id="8201d-126">**Header:** None</span></span>  
<span data-ttu-id="8201d-127">**Bibliothèque :** Aucun.</span><span class="sxs-lookup"><span data-stu-id="8201d-127">**Library:** None</span></span>  
<span data-ttu-id="8201d-128">**Versions du .NET Framework :** [!INCLUDE[net_current_v47plus](../../../../includes/net-current-v47plus.md)]</span><span class="sxs-lookup"><span data-stu-id="8201d-128">**.NET Framework Versions:** [!INCLUDE[net_current_v47plus](../../../../includes/net-current-v47plus.md)]</span></span>  

## <a name="see-also"></a><span data-ttu-id="8201d-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="8201d-129">See also</span></span>

- [<span data-ttu-id="8201d-130">Débogage</span><span class="sxs-lookup"><span data-stu-id="8201d-130">Debugging</span></span>](../../../../docs/framework/unmanaged-api/debugging/index.md)
- [<span data-ttu-id="8201d-131">Interfaces de débogage</span><span class="sxs-lookup"><span data-stu-id="8201d-131">Debugging Interfaces</span></span>](../../../../docs/framework/unmanaged-api/debugging/debugging-interfaces.md)
