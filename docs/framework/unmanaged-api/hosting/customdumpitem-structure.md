---
title: CustomDumpItem, structure
ms.date: 03/30/2017
api_name:
- CustomDumpItem
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- CustomDumpItem
helpviewer_keywords:
- CustomDumpItem structure [.NET Framework hosting]
ms.assetid: fd9085ff-7beb-4c38-97f0-037cd8ba4f65
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 9000f35e9a8f7ecc6c40cf0ef9c220fc9f4f9c10
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59185924"
---
# <a name="customdumpitem-structure"></a><span data-ttu-id="0ac96-102">CustomDumpItem, structure</span><span class="sxs-lookup"><span data-stu-id="0ac96-102">CustomDumpItem Structure</span></span>
<span data-ttu-id="0ac96-103">Décrit un élément à ajouter à une image personnalisée dans le rapport d’erreurs.</span><span class="sxs-lookup"><span data-stu-id="0ac96-103">Describes an item to be added to a custom dump in error reporting.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="0ac96-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="0ac96-104">Syntax</span></span>  
  
```  
struct {  
    ECustomDumpItemKind itemKind;   
    union {  
        UINT_PTR pReserved;  
    }  
} CustomDumpItem;  
```  
  
## <a name="members"></a><span data-ttu-id="0ac96-105">Membres</span><span class="sxs-lookup"><span data-stu-id="0ac96-105">Members</span></span>  
  
|<span data-ttu-id="0ac96-106">Membre</span><span class="sxs-lookup"><span data-stu-id="0ac96-106">Member</span></span>|<span data-ttu-id="0ac96-107">Description</span><span class="sxs-lookup"><span data-stu-id="0ac96-107">Description</span></span>|  
|------------|-----------------|  
|`itemKind`|<span data-ttu-id="0ac96-108">Un [ECustomDumpItemKind](../../../../docs/framework/unmanaged-api/hosting/ecustomdumpitemkind-enumeration.md) valeur qui indique le type d’élément à ajouter.</span><span class="sxs-lookup"><span data-stu-id="0ac96-108">An [ECustomDumpItemKind](../../../../docs/framework/unmanaged-api/hosting/ecustomdumpitemkind-enumeration.md) value that indicates the kind of item to be added.</span></span>|  
|`pReserved`|<span data-ttu-id="0ac96-109">Actuellement non utilisé.</span><span class="sxs-lookup"><span data-stu-id="0ac96-109">Not currently used.</span></span> <span data-ttu-id="0ac96-110">Les éléments ajoutés à l’union doivent être ne dépassant pas la taille du pointeur.</span><span class="sxs-lookup"><span data-stu-id="0ac96-110">Any items added to the union must be no larger than pointer size.</span></span> <span data-ttu-id="0ac96-111">Si un `struct` est nécessaire, vous devez allouer séparément et pointer dessus.</span><span class="sxs-lookup"><span data-stu-id="0ac96-111">If a `struct` is required, you must allocate it separately and point to it.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="0ac96-112">Notes</span><span class="sxs-lookup"><span data-stu-id="0ac96-112">Remarks</span></span>  
 <span data-ttu-id="0ac96-113">[ICLRErrorReportingManager::BeginCustomDump](../../../../docs/framework/unmanaged-api/hosting/iclrerrorreportingmanager-begincustomdump-method.md) prend un paramètre de type `CustomDumpItem`.</span><span class="sxs-lookup"><span data-stu-id="0ac96-113">[ICLRErrorReportingManager::BeginCustomDump](../../../../docs/framework/unmanaged-api/hosting/iclrerrorreportingmanager-begincustomdump-method.md) takes a parameter of type `CustomDumpItem`.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="0ac96-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="0ac96-114">Requirements</span></span>  
 <span data-ttu-id="0ac96-115">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="0ac96-115">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="0ac96-116">**En-tête :** MSCorEE.idl</span><span class="sxs-lookup"><span data-stu-id="0ac96-116">**Header:** MSCorEE.idl</span></span>  
  
 <span data-ttu-id="0ac96-117">**Bibliothèque :** Inclus en tant que ressource dans MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="0ac96-117">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="0ac96-118">**Versions du .NET Framework :** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="0ac96-118">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="0ac96-119">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0ac96-119">See also</span></span>

- [<span data-ttu-id="0ac96-120">Structures d’hébergement</span><span class="sxs-lookup"><span data-stu-id="0ac96-120">Hosting Structures</span></span>](../../../../docs/framework/unmanaged-api/hosting/hosting-structures.md)
