---
title: ITypeName::GetTypeArguments, méthode
ms.date: 03/30/2017
api_name:
- ITypeName.GetTypeArguments
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- GetTypeArguments
helpviewer_keywords:
- ITypeName::GetTypeArguments method [.NET Framework hosting]
- GetTypeArguments method [.NET Framework hosting]
ms.assetid: 638d77df-ff9c-40d9-88ee-930f5f87ada1
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: e4cd4fa8f4ba2bea5a2a853544eae6239bfaaeba
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59132273"
---
# <a name="itypenamegettypearguments-method"></a><span data-ttu-id="99df8-102">ITypeName::GetTypeArguments, méthode</span><span class="sxs-lookup"><span data-stu-id="99df8-102">ITypeName::GetTypeArguments Method</span></span>
<span data-ttu-id="99df8-103">Cette m&#233;thode prend en charge l'infrastructure .NET Framework et n'est pas destin&#233;e &#224; &#234;tre utilis&#233;e directement &#224; partir de votre code.</span><span class="sxs-lookup"><span data-stu-id="99df8-103">This method supports the .NET Framework infrastructure and is not intended to be used directly from your code.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="99df8-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="99df8-104">Syntax</span></span>  
  
```  
HRESULT GetTypeArguments (  
    [in] DWORD           count,  
    [out] ITypeName**    rgpArguments,  
    [out, retval] DWORD* pCount  
);  
```  
  
## <a name="requirements"></a><span data-ttu-id="99df8-105">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="99df8-105">Requirements</span></span>  
 <span data-ttu-id="99df8-106">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="99df8-106">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="99df8-107">**En-tête :** MSCorEE.h</span><span class="sxs-lookup"><span data-stu-id="99df8-107">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="99df8-108">**Bibliothèque :** Inclus en tant que ressource dans MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="99df8-108">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="99df8-109">**Versions du .NET Framework :** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="99df8-109">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="99df8-110">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="99df8-110">See also</span></span>

- [<span data-ttu-id="99df8-111">Interfaces d’hébergement</span><span class="sxs-lookup"><span data-stu-id="99df8-111">Hosting Interfaces</span></span>](../../../../docs/framework/unmanaged-api/hosting/hosting-interfaces.md)
