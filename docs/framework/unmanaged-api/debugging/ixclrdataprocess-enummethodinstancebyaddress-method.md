---
title: IXCLRDataProcess::EnumMethodInstanceByAddress (méthode)
ms.date: 01/16/2019
api.name:
- IXCLRDataProcess::EnumMethodInstanceByAddress Method
api.location:
- mscordacwks.dll
api.type:
- COM
f1.keywords:
- IXCLRDataProcess::EnumMethodInstanceByAddress Method
helpviewer.keywords:
- IXCLRDataProcess::EnumMethodInstanceByAddress Method [.NET Framework debugging]
topic_type:
- apiref
author: cshung
ms.author: andrewau
ms.openlocfilehash: a51c709b0b331127b74d98c4dc42e2772fd7f2db
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59166437"
---
# <a name="ixclrdataprocessenummethodinstancebyaddress-method"></a><span data-ttu-id="4e5a7-102">IXCLRDataProcess::EnumMethodInstanceByAddress (méthode)</span><span class="sxs-lookup"><span data-stu-id="4e5a7-102">IXCLRDataProcess::EnumMethodInstanceByAddress Method</span></span>

<span data-ttu-id="4e5a7-103">Énumère les instances de la méthode de ce processus, en commençant à un offset d’adresse.</span><span class="sxs-lookup"><span data-stu-id="4e5a7-103">Enumerates the method instances of this process starting at an address offset.</span></span>

[!INCLUDE[debugging-api-recommended-note](../../../../includes/debugging-api-recommended-note.md)]

## <a name="syntax"></a><span data-ttu-id="4e5a7-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="4e5a7-104">Syntax</span></span>

```
HRESULT EnumMethodInstanceByAddress(
    [in] CLRDATA_ENUM              *handle,
    [out] IXCLRDataMethodInstance **method
);
```

## <a name="parameters"></a><span data-ttu-id="4e5a7-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="4e5a7-105">Parameters</span></span>

`handle`\
<span data-ttu-id="4e5a7-106">[in] Un handle pour énumérer les instances de la méthode.</span><span class="sxs-lookup"><span data-stu-id="4e5a7-106">[in] A handle for enumerating the method instances.</span></span>

`mod`\
<span data-ttu-id="4e5a7-107">[out] L’instance de la méthode énumérée.</span><span class="sxs-lookup"><span data-stu-id="4e5a7-107">[out] The enumerated method instance.</span></span>

## <a name="remarks"></a><span data-ttu-id="4e5a7-108">Notes</span><span class="sxs-lookup"><span data-stu-id="4e5a7-108">Remarks</span></span>

<span data-ttu-id="4e5a7-109">La méthode fournie fait partie de la `IXCLRDataProcess` interface et correspond à l’emplacement de la table de la méthode virtuelle de 28.</span><span class="sxs-lookup"><span data-stu-id="4e5a7-109">The provided method is part of the `IXCLRDataProcess` interface and corresponds to the 28th slot of the virtual method table.</span></span>

## <a name="requirements"></a><span data-ttu-id="4e5a7-110">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="4e5a7-110">Requirements</span></span>

<span data-ttu-id="4e5a7-111">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="4e5a7-111">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>   
<span data-ttu-id="4e5a7-112">**En-tête :** Aucun.</span><span class="sxs-lookup"><span data-stu-id="4e5a7-112">**Header:** None</span></span>   
<span data-ttu-id="4e5a7-113">**Bibliothèque :** Aucun.</span><span class="sxs-lookup"><span data-stu-id="4e5a7-113">**Library:** None</span></span>   
<span data-ttu-id="4e5a7-114">**Versions du .NET Framework :** [!INCLUDE[net_current_v47plus](../../../../includes/net-current-v47plus.md)]</span><span class="sxs-lookup"><span data-stu-id="4e5a7-114">**.NET Framework Versions:** [!INCLUDE[net_current_v47plus](../../../../includes/net-current-v47plus.md)]</span></span>   
 
## <a name="see-also"></a><span data-ttu-id="4e5a7-115">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="4e5a7-115">See also</span></span>

- [<span data-ttu-id="4e5a7-116">Énumération de CLRDataSourceType</span><span class="sxs-lookup"><span data-stu-id="4e5a7-116">CLRDataSourceType Enumeration</span></span>](clrdatasourcetype-enumeration.md)
- [<span data-ttu-id="4e5a7-117">Débogage</span><span class="sxs-lookup"><span data-stu-id="4e5a7-117">Debugging</span></span>](index.md)
- [<span data-ttu-id="4e5a7-118">Interface de IXCLRDataProcess</span><span class="sxs-lookup"><span data-stu-id="4e5a7-118">IXCLRDataProcess Interface</span></span>](ixclrdataprocess-interface.md)
