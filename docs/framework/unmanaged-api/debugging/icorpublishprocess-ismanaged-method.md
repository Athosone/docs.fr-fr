---
title: ICorPublishProcess::IsManaged, méthode
ms.date: 03/30/2017
api_name:
- ICorPublishProcess.IsManaged
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorPublishProcess::IsManaged
helpviewer_keywords:
- IsManaged method, ICorPublishProcess interface [.NET Framework debugging]
- ICorPublishProcess::IsManaged method [.NET Framework debugging]
ms.assetid: 06b1f7cc-acdf-47a6-9d53-d9dec2424152
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 29c5f96bab374d6e2d43424370bff2a4a2ab6df3
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59218288"
---
# <a name="icorpublishprocessismanaged-method"></a><span data-ttu-id="34d2e-102">ICorPublishProcess::IsManaged, méthode</span><span class="sxs-lookup"><span data-stu-id="34d2e-102">ICorPublishProcess::IsManaged Method</span></span>
<span data-ttu-id="34d2e-103">Obtient une valeur qui indique si le processus référencé par ce [ICorPublishProcess](../../../../docs/framework/unmanaged-api/debugging/icorpublishprocess-interface.md) ne connaît ont du code managé.</span><span class="sxs-lookup"><span data-stu-id="34d2e-103">Gets a value that indicates whether the process referenced by this [ICorPublishProcess](../../../../docs/framework/unmanaged-api/debugging/icorpublishprocess-interface.md) is known to have managed code.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="34d2e-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="34d2e-104">Syntax</span></span>  
  
```  
HRESULT IsManaged (  
    [out] BOOL   *pbManaged  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="34d2e-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="34d2e-105">Parameters</span></span>  
 `pbManaged`  
 <span data-ttu-id="34d2e-106">[out] Pointeur vers une valeur booléenne qui indique si le processus a du code managé.</span><span class="sxs-lookup"><span data-stu-id="34d2e-106">[out] A pointer to a Boolean value that indicates whether the process has managed code.</span></span> <span data-ttu-id="34d2e-107">La valeur est `true` si le processus a du code managé ; sinon, `false`.</span><span class="sxs-lookup"><span data-stu-id="34d2e-107">The value is `true` if the process has managed code; otherwise, `false`.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="34d2e-108">Notes</span><span class="sxs-lookup"><span data-stu-id="34d2e-108">Remarks</span></span>  
 <span data-ttu-id="34d2e-109">Depuis la version actuelle de `ICorPublishProcess` autorise l’accès uniquement aux processus qui ont du code managé, `IsManaged` retourne toujours `true`.</span><span class="sxs-lookup"><span data-stu-id="34d2e-109">Since the current version of `ICorPublishProcess` allows access only to processes that have managed code, `IsManaged` always returns `true`.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="34d2e-110">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="34d2e-110">Requirements</span></span>  
 <span data-ttu-id="34d2e-111">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="34d2e-111">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="34d2e-112">**En-tête :** CorPub.idl, CorPub.h</span><span class="sxs-lookup"><span data-stu-id="34d2e-112">**Header:** CorPub.idl, CorPub.h</span></span>  
  
 <span data-ttu-id="34d2e-113">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="34d2e-113">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="34d2e-114">**Versions du .NET Framework :** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="34d2e-114">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="34d2e-115">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="34d2e-115">See also</span></span>

- [<span data-ttu-id="34d2e-116">ICorPublishProcess, interface</span><span class="sxs-lookup"><span data-stu-id="34d2e-116">ICorPublishProcess Interface</span></span>](../../../../docs/framework/unmanaged-api/debugging/icorpublishprocess-interface.md)
