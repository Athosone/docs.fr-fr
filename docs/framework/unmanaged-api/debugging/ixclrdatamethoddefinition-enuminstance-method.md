---
title: IXCLRDataMethodDefinition::EnumInstance (méthode)
ms.date: 01/16/2019
api.name:
- IXCLRDataMethodDefinition::EnumInstance Method
api.location:
- mscordacwks.dll
api.type:
- COM
f1.keywords:
- IXCLRDataMethodDefinition::EnumInstance Method
helpviewer.keywords:
- IXCLRDataMethodDefinition::EnumInstance Method [.NET Framework debugging]
topic_type:
- apiref
author: cshung
ms.author: andrewau
ms.openlocfilehash: dacf76582916ad50f51ae7c8818b496f31f9553e
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61771928"
---
# <a name="ixclrdatamethoddefinitionenuminstance-method"></a><span data-ttu-id="b817b-102">IXCLRDataMethodDefinition::EnumInstance (méthode)</span><span class="sxs-lookup"><span data-stu-id="b817b-102">IXCLRDataMethodDefinition::EnumInstance Method</span></span>

<span data-ttu-id="b817b-103">Énumère les instances de cette définition de méthode.</span><span class="sxs-lookup"><span data-stu-id="b817b-103">Enumerates the instances of this method definition.</span></span>

[!INCLUDE[debugging-api-recommended-note](../../../../includes/debugging-api-recommended-note.md)]

## <a name="syntax"></a><span data-ttu-id="b817b-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="b817b-104">Syntax</span></span>

```
HRESULT EnumInstance(
    [in, out] CLRDATA_ENUM         *handle,
    [out] IXCLRDataMethodInstance **instance
);
```

## <a name="parameters"></a><span data-ttu-id="b817b-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="b817b-105">Parameters</span></span>

`handle`\
<span data-ttu-id="b817b-106">[in, out] Un handle pour énumérer les instances.</span><span class="sxs-lookup"><span data-stu-id="b817b-106">[in, out] A handle for enumerating the instances.</span></span>

`instance`\
<span data-ttu-id="b817b-107">[out] L’instance énumérée.</span><span class="sxs-lookup"><span data-stu-id="b817b-107">[out] The enumerated instance.</span></span>

## <a name="remarks"></a><span data-ttu-id="b817b-108">Notes</span><span class="sxs-lookup"><span data-stu-id="b817b-108">Remarks</span></span>

<span data-ttu-id="b817b-109">La méthode fournie fait partie de la `IXCLRDataMethodDefinition` interface et correspond à l’emplacement de quatrième de la table de la méthode virtuelle.</span><span class="sxs-lookup"><span data-stu-id="b817b-109">The provided method is part of the `IXCLRDataMethodDefinition` interface and corresponds to the fourth slot of the virtual method table.</span></span>

## <a name="requirements"></a><span data-ttu-id="b817b-110">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="b817b-110">Requirements</span></span>

<span data-ttu-id="b817b-111">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="b817b-111">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
<span data-ttu-id="b817b-112">**En-tête :** Aucun.</span><span class="sxs-lookup"><span data-stu-id="b817b-112">**Header:** None</span></span>  
<span data-ttu-id="b817b-113">**Bibliothèque :** Aucun.</span><span class="sxs-lookup"><span data-stu-id="b817b-113">**Library:** None</span></span>  
<span data-ttu-id="b817b-114">**Versions du .NET Framework :** [!INCLUDE[net_current_v47plus](../../../../includes/net-current-v47plus.md)]</span><span class="sxs-lookup"><span data-stu-id="b817b-114">**.NET Framework Versions:** [!INCLUDE[net_current_v47plus](../../../../includes/net-current-v47plus.md)]</span></span>  

## <a name="see-also"></a><span data-ttu-id="b817b-115">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b817b-115">See also</span></span>

- [<span data-ttu-id="b817b-116">Énumération de CLRDataSourceType</span><span class="sxs-lookup"><span data-stu-id="b817b-116">CLRDataSourceType Enumeration</span></span>](../../../../docs/framework/unmanaged-api/debugging/clrdatasourcetype-enumeration.md)
- [<span data-ttu-id="b817b-117">Débogage</span><span class="sxs-lookup"><span data-stu-id="b817b-117">Debugging</span></span>](../../../../docs/framework/unmanaged-api/debugging/index.md)
- [<span data-ttu-id="b817b-118">Interface de IXCLRDataMethodDefinition</span><span class="sxs-lookup"><span data-stu-id="b817b-118">IXCLRDataMethodDefinition Interface</span></span>](../../../../docs/framework/unmanaged-api/debugging/ixclrdatamethoddefinition-interface.md)
- [<span data-ttu-id="b817b-119">Interface de IXCLRDataMethodInstance</span><span class="sxs-lookup"><span data-stu-id="b817b-119">IXCLRDataMethodInstance Interface</span></span>](../../../../docs/framework/unmanaged-api/debugging/ixclrdatamethodinstance-interface.md)
