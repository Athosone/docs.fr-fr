---
title: IInstallReferenceEnum, interface
ms.date: 03/30/2017
api_name:
- IInstallReferenceEnum
api_location:
- fusion.dll
api_type:
- COM
f1_keywords:
- IInstallReferenceEnum
helpviewer_keywords:
- IInstallReferenceEnum interface [.NET Framework fusion]
ms.assetid: 2863b33b-a541-462c-bbe8-702a2832898e
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 35faeb69e864a428dc40394ad89a7d50b95bbcab
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59103323"
---
# <a name="iinstallreferenceenum-interface"></a><span data-ttu-id="86d04-102">IInstallReferenceEnum, interface</span><span class="sxs-lookup"><span data-stu-id="86d04-102">IInstallReferenceEnum Interface</span></span>
<span data-ttu-id="86d04-103">Représente un énumérateur pour les assemblys référencés installés dans le global assembly cache.</span><span class="sxs-lookup"><span data-stu-id="86d04-103">Represents an enumerator for the referenced assemblies installed in the global assembly cache.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="86d04-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="86d04-104">Syntax</span></span>  
  
```  
interface IInstallReferenceEnum : IUnknown {  
    HRESULT GetNextInstallReferenceItem (  
        [out] IInstallReferenceItem **ppRefItem,  
        [in]  DWORD dwFlags,  
        [in]  LPVOID pvReserved  
    );  
};  
```  
  
## <a name="methods"></a><span data-ttu-id="86d04-105">Méthodes</span><span class="sxs-lookup"><span data-stu-id="86d04-105">Methods</span></span>  
  
|<span data-ttu-id="86d04-106">Méthode</span><span class="sxs-lookup"><span data-stu-id="86d04-106">Method</span></span>|<span data-ttu-id="86d04-107">Description</span><span class="sxs-lookup"><span data-stu-id="86d04-107">Description</span></span>|  
|------------|-----------------|  
|[<span data-ttu-id="86d04-108">GetNextInstallReferenceItem, méthode</span><span class="sxs-lookup"><span data-stu-id="86d04-108">GetNextInstallReferenceItem Method</span></span>](../../../../docs/framework/unmanaged-api/fusion/iinstallreferenceenum-getnextinstallreferenceitem-method.md)|<span data-ttu-id="86d04-109">Obtient un pointeur vers la prochaine `IInstallReferenceItem` contenues dans cette `IInstallReferenceEnum`.</span><span class="sxs-lookup"><span data-stu-id="86d04-109">Gets a pointer to the next `IInstallReferenceItem` contained in this `IInstallReferenceEnum`.</span></span>|  
  
## <a name="requirements"></a><span data-ttu-id="86d04-110">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="86d04-110">Requirements</span></span>  
 <span data-ttu-id="86d04-111">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="86d04-111">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="86d04-112">**En-tête :** Fusion.h</span><span class="sxs-lookup"><span data-stu-id="86d04-112">**Header:** Fusion.h</span></span>  
  
 <span data-ttu-id="86d04-113">**Versions du .NET Framework :** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="86d04-113">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="86d04-114">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="86d04-114">See also</span></span>

- [<span data-ttu-id="86d04-115">Interfaces de fusion</span><span class="sxs-lookup"><span data-stu-id="86d04-115">Fusion Interfaces</span></span>](../../../../docs/framework/unmanaged-api/fusion/fusion-interfaces.md)
- [<span data-ttu-id="86d04-116">IInstallReferenceItem, interface</span><span class="sxs-lookup"><span data-stu-id="86d04-116">IInstallReferenceItem Interface</span></span>](../../../../docs/framework/unmanaged-api/fusion/iinstallreferenceitem-interface.md)
