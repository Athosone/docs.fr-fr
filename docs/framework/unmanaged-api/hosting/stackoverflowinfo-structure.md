---
title: StackOverflowInfo, structure
ms.date: 03/30/2017
api_name:
- StackOverflowInfo
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- StackOverflowInfo
helpviewer_keywords:
- StackOverflowInfo structure [.NET Framework hosting]
ms.assetid: 519389f2-0217-436c-99d4-93a76ebce5b5
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: ac0f5d522a24394369583692f8c564254529bf13
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61796035"
---
# <a name="stackoverflowinfo-structure"></a><span data-ttu-id="abde3-102">StackOverflowInfo, structure</span><span class="sxs-lookup"><span data-stu-id="abde3-102">StackOverflowInfo Structure</span></span>
<span data-ttu-id="abde3-103">Stocke le type de dépassement de capacité s’est produite et des informations sur l’exception qui a été levée en raison du dépassement de capacité.</span><span class="sxs-lookup"><span data-stu-id="abde3-103">Stores the type of overflow that occurred and information on the exception that was thrown due to the overflow.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="abde3-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="abde3-104">Syntax</span></span>  
  
```  
typedef struct _StackOverflowInfo {  
    StackOverflowType   soType;  
    EXCEPTION_POINTERS  *pExceptionInfo;  
} StackOverflowInfo;  
```  
  
## <a name="members"></a><span data-ttu-id="abde3-105">Membres</span><span class="sxs-lookup"><span data-stu-id="abde3-105">Members</span></span>  
  
|<span data-ttu-id="abde3-106">Membre</span><span class="sxs-lookup"><span data-stu-id="abde3-106">Member</span></span>|<span data-ttu-id="abde3-107">Description</span><span class="sxs-lookup"><span data-stu-id="abde3-107">Description</span></span>|  
|------------|-----------------|  
|`soType`|<span data-ttu-id="abde3-108">Une valeur de la [StackOverflowType](../../../../docs/framework/unmanaged-api/hosting/stackoverflowtype-enumeration.md) énumération qui spécifie le type de dépassement de capacité.</span><span class="sxs-lookup"><span data-stu-id="abde3-108">A value of the [StackOverflowType](../../../../docs/framework/unmanaged-api/hosting/stackoverflowtype-enumeration.md) enumeration that specifies the type of overflow.</span></span>|  
|`pExceptionInfo`|<span data-ttu-id="abde3-109">Un pointeur vers un Win32 `EXCEPTION_POINTERS` objet qui contient un enregistrement d’exception avec une description indépendante de l’ordinateur d’une exception et un enregistrement de contexte avec une description dépendantes de l’ordinateur du contexte du processeur au moment de l’exception.</span><span class="sxs-lookup"><span data-stu-id="abde3-109">A pointer to a Win32 `EXCEPTION_POINTERS` object, which contains an exception record with a machine-independent description of an exception and a context record with a machine-dependent description of the processor context at the time of the exception.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="abde3-110">Notes</span><span class="sxs-lookup"><span data-stu-id="abde3-110">Remarks</span></span>  
 <span data-ttu-id="abde3-111">Un `StackOverflowInfo` objet est passé à la [IActionOnCLREvent::OnEvent](../../../../docs/framework/unmanaged-api/hosting/iactiononclrevent-onevent-method.md) méthode pour `Event_StackOverflow` événements.</span><span class="sxs-lookup"><span data-stu-id="abde3-111">A `StackOverflowInfo` object is passed to the [IActionOnCLREvent::OnEvent](../../../../docs/framework/unmanaged-api/hosting/iactiononclrevent-onevent-method.md) method for `Event_StackOverflow` events.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="abde3-112">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="abde3-112">Requirements</span></span>  
 <span data-ttu-id="abde3-113">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="abde3-113">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="abde3-114">**En-tête :** MSCorEE.idl</span><span class="sxs-lookup"><span data-stu-id="abde3-114">**Header:** MSCorEE.idl</span></span>  
  
 <span data-ttu-id="abde3-115">**Bibliothèque :** Inclus en tant que ressource dans MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="abde3-115">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="abde3-116">**Versions du .NET Framework :** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="abde3-116">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="abde3-117">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="abde3-117">See also</span></span>

- [<span data-ttu-id="abde3-118">Structures d’hébergement</span><span class="sxs-lookup"><span data-stu-id="abde3-118">Hosting Structures</span></span>](../../../../docs/framework/unmanaged-api/hosting/hosting-structures.md)
