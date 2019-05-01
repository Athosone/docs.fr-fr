---
title: ICorPublishProcess::GetProcessID, méthode
ms.date: 03/30/2017
api_name:
- ICorPublishProcess.GetProcessID
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorPublishProcess::GetProcessID
helpviewer_keywords:
- ICorPublishProcess::GetProcessID method [.NET Framework debugging]
- GetProcessID method [.NET Framework debugging]
ms.assetid: f31185e0-f01d-463a-b392-42163e39bfe9
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 6f3948e45b991e667ea90c7846ee0d6fd630c0db
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61986580"
---
# <a name="icorpublishprocessgetprocessid-method"></a><span data-ttu-id="7ca75-102">ICorPublishProcess::GetProcessID, méthode</span><span class="sxs-lookup"><span data-stu-id="7ca75-102">ICorPublishProcess::GetProcessID Method</span></span>
<span data-ttu-id="7ca75-103">Obtient l’identificateur de système d’exploitation de ce processus.</span><span class="sxs-lookup"><span data-stu-id="7ca75-103">Gets the operating system identifier for this process.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="7ca75-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="7ca75-104">Syntax</span></span>  
  
```  
HRESULT GetProcessID (  
    [out] unsigned   *pid  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="7ca75-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="7ca75-105">Parameters</span></span>  
 `pid`  
 <span data-ttu-id="7ca75-106">[out] Un pointeur vers l’identificateur du processus représenté par cet [ICorPublishProcess](../../../../docs/framework/unmanaged-api/debugging/icorpublishprocess-interface.md) objet.</span><span class="sxs-lookup"><span data-stu-id="7ca75-106">[out] A pointer to the identifier of the process represented by this [ICorPublishProcess](../../../../docs/framework/unmanaged-api/debugging/icorpublishprocess-interface.md) object.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="7ca75-107">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="7ca75-107">Requirements</span></span>  
 <span data-ttu-id="7ca75-108">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="7ca75-108">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="7ca75-109">**En-tête :** CorPub.idl, CorPub.h</span><span class="sxs-lookup"><span data-stu-id="7ca75-109">**Header:** CorPub.idl, CorPub.h</span></span>  
  
 <span data-ttu-id="7ca75-110">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="7ca75-110">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="7ca75-111">**Versions du .NET Framework :** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="7ca75-111">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="7ca75-112">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="7ca75-112">See also</span></span>

- [<span data-ttu-id="7ca75-113">ICorPublishProcess, interface</span><span class="sxs-lookup"><span data-stu-id="7ca75-113">ICorPublishProcess Interface</span></span>](../../../../docs/framework/unmanaged-api/debugging/icorpublishprocess-interface.md)
