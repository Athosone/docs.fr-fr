---
title: IXCLRDataProcess::GetAppDomainByUniqueId Method
ms.date: 01/16/2019
api.name:
- IXCLRDataProcess::GetAppDomainByUniqueId Method
api.location:
- mscordacwks.dll
api.type:
- COM
f1.keywords:
- IXCLRDataProcess::GetAppDomainByUniqueId Method
helpviewer.keywords:
- IXCLRDataProcess::GetAppDomainByUniqueId Method [.NET Framework debugging]
topic_type:
- apiref
author: cshung
ms.author: andrewau
ms.openlocfilehash: 8b468d40ef8eb523ba8881627fae15cf9b7c7b80
ms.sourcegitcommit: 438919211260bb415fc8f96ca3eabc33cf2d681d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/16/2019
ms.locfileid: "59614020"
---
# <a name="ixclrdataprocessgetappdomainbyuniqueid-method"></a><span data-ttu-id="2d263-102">IXCLRDataProcess::GetAppDomainByUniqueId Method</span><span class="sxs-lookup"><span data-stu-id="2d263-102">IXCLRDataProcess::GetAppDomainByUniqueId Method</span></span>

<span data-ttu-id="2d263-103">Obtient un `AppDomain` dans un processus en fonction de son identificateur unique.</span><span class="sxs-lookup"><span data-stu-id="2d263-103">Gets an `AppDomain` in a process based on its unique identifier.</span></span>

[!INCLUDE[debugging-api-recommended-note](../../../../includes/debugging-api-recommended-note.md)]

## <a name="syntax"></a><span data-ttu-id="2d263-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="2d263-104">Syntax</span></span>

```cpp
HRESULT GetAppDomainByUniqueID(
    [in] ULONG64               id,
    [out] IXCLRDataAppDomain **appDomain
);
```

## <a name="parameters"></a><span data-ttu-id="2d263-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="2d263-105">Parameters</span></span>

`id`\
<span data-ttu-id="2d263-106">[in] L’identificateur unique du domaine d’application</span><span class="sxs-lookup"><span data-stu-id="2d263-106">[in] The unique identifier of the AppDomain</span></span>

`appDomain`\
<span data-ttu-id="2d263-107">[out] Le domaine d’application</span><span class="sxs-lookup"><span data-stu-id="2d263-107">[out] The AppDomain</span></span>

## <a name="remarks"></a><span data-ttu-id="2d263-108">Notes</span><span class="sxs-lookup"><span data-stu-id="2d263-108">Remarks</span></span>

<span data-ttu-id="2d263-109">La méthode fournie fait partie de la `IXCLRDataProcess` interface et correspond à l’emplacement de la table de la méthode virtuelle de 20.</span><span class="sxs-lookup"><span data-stu-id="2d263-109">The provided method is part of the `IXCLRDataProcess` interface and corresponds to the 20th slot of the virtual method table.</span></span> <span data-ttu-id="2d263-110">Le `IXCLRDataAppDomain*` retourné est utilisé pour l’interaction avec d’autres API.</span><span class="sxs-lookup"><span data-stu-id="2d263-110">The `IXCLRDataAppDomain*` returned is used for interaction with other APIs.</span></span>

## <a name="requirements"></a><span data-ttu-id="2d263-111">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="2d263-111">Requirements</span></span>

<span data-ttu-id="2d263-112">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="2d263-112">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>
<span data-ttu-id="2d263-113">**En-tête :** Aucun **bibliothèque :** Aucun **Versions du .NET Framework :** [!INCLUDE[net_current_v47plus](../../../../includes/net-current-v47plus.md)]</span><span class="sxs-lookup"><span data-stu-id="2d263-113">**Header:** None **Library:** None **.NET Framework Versions:** [!INCLUDE[net_current_v47plus](../../../../includes/net-current-v47plus.md)]</span></span>

## <a name="see-also"></a><span data-ttu-id="2d263-114">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="2d263-114">See also</span></span>

- [<span data-ttu-id="2d263-115">Débogage</span><span class="sxs-lookup"><span data-stu-id="2d263-115">Debugging</span></span>](index.md)
- [<span data-ttu-id="2d263-116">Interface de IXCLRDataProcess</span><span class="sxs-lookup"><span data-stu-id="2d263-116">IXCLRDataProcess Interface</span></span>](ixclrdataprocess-interface.md)
