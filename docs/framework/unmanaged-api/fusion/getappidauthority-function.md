---
title: GetAppIdAuthority, fonction
ms.date: 03/30/2017
api_name:
- GetAppIdAuthority
api_location:
- fusion.dll
- clr.dll
api_type:
- COM
f1_keywords:
- GetAppIdAuthority
helpviewer_keywords:
- GetAppIdAuthority function [.NET Framework fusion]
ms.assetid: 9f968dad-0d09-47fb-bebc-94c39a0d16ad
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 274b91793cd51348c42661bf12a4e4385e17f630
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61697769"
---
# <a name="getappidauthority-function"></a><span data-ttu-id="eb202-102">GetAppIdAuthority, fonction</span><span class="sxs-lookup"><span data-stu-id="eb202-102">GetAppIdAuthority Function</span></span>
<span data-ttu-id="eb202-103">Obtient un pointeur vers un [IAppIdAuthority](../../../../docs/framework/unmanaged-api/fusion/iappidauthority-interface.md) instance qui gère des clés pour les identités d’application et les références.</span><span class="sxs-lookup"><span data-stu-id="eb202-103">Gets a pointer to an [IAppIdAuthority](../../../../docs/framework/unmanaged-api/fusion/iappidauthority-interface.md) instance that manages keys for application identities and references.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="eb202-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="eb202-104">Syntax</span></span>  
  
```  
HRESULT GetAppIdAuthority (  
    [out] IAppIdAuthority **ppIAppIdAuthority  
 );  
```  
  
## <a name="parameters"></a><span data-ttu-id="eb202-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="eb202-105">Parameters</span></span>  
 `ppIAppIdAuthority`  
 <span data-ttu-id="eb202-106">[out] Retourné `IAppIdAuthority` pointeur.</span><span class="sxs-lookup"><span data-stu-id="eb202-106">[out] The returned `IAppIdAuthority` pointer.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="eb202-107">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="eb202-107">Requirements</span></span>  
 <span data-ttu-id="eb202-108">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="eb202-108">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="eb202-109">**En-tête :** Isolation.h</span><span class="sxs-lookup"><span data-stu-id="eb202-109">**Header:** Isolation.h</span></span>  
  
 <span data-ttu-id="eb202-110">**Versions du .NET Framework :** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="eb202-110">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="eb202-111">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="eb202-111">See also</span></span>

- [<span data-ttu-id="eb202-112">IAppIdAuthority, interface</span><span class="sxs-lookup"><span data-stu-id="eb202-112">IAppIdAuthority Interface</span></span>](../../../../docs/framework/unmanaged-api/fusion/iappidauthority-interface.md)
- [<span data-ttu-id="eb202-113">Fonctions statiques globales de fusion</span><span class="sxs-lookup"><span data-stu-id="eb202-113">Fusion Global Static Functions</span></span>](../../../../docs/framework/unmanaged-api/fusion/fusion-global-static-functions.md)
