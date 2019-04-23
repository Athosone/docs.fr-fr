---
title: IReferenceIdentity, interface
ms.date: 03/30/2017
api_name:
- IReferenceIdentity
api_location:
- fusion.dll
api_type:
- COM
f1_keywords:
- IReferenceIdentity
helpviewer_keywords:
- IReferenceIdentity interface [.NET Framework fusion]
ms.assetid: 9180ac5a-7019-4716-9f83-8a91d157239a
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: dd46ea26532074c9ea42da4d07a38ed583aad076
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59220160"
---
# <a name="ireferenceidentity-interface"></a><span data-ttu-id="346c9-102">IReferenceIdentity, interface</span><span class="sxs-lookup"><span data-stu-id="346c9-102">IReferenceIdentity Interface</span></span>
<span data-ttu-id="346c9-103">Représente une référence à la signature unique d’un objet de code.</span><span class="sxs-lookup"><span data-stu-id="346c9-103">Represents a reference to the unique signature of a code object.</span></span>  
  
## <a name="methods"></a><span data-ttu-id="346c9-104">Méthodes</span><span class="sxs-lookup"><span data-stu-id="346c9-104">Methods</span></span>  
  
|<span data-ttu-id="346c9-105">Méthode</span><span class="sxs-lookup"><span data-stu-id="346c9-105">Method</span></span>|<span data-ttu-id="346c9-106">Description</span><span class="sxs-lookup"><span data-stu-id="346c9-106">Description</span></span>|  
|------------|-----------------|  
|`IReferenceIdentity::Clone`|<span data-ttu-id="346c9-107">Obtient un pointeur d’interface vers un nouveau `IReferenceIdentity` instance qui est identique à ce `IReferenceIdentity`, sauf pour les modifications de l’attribut spécifié.</span><span class="sxs-lookup"><span data-stu-id="346c9-107">Gets an interface pointer to a new `IReferenceIdentity` instance that is identical to this `IReferenceIdentity`, except for the specified attribute changes.</span></span>|  
|`IReferenceIdentity::EnumAttributes`|<span data-ttu-id="346c9-108">Obtient un pointeur d’interface vers un `IEnumIDENTITY_ATTRIBUTE` instance qui contient les attributs associés à ce `IReferenceIdentity`.</span><span class="sxs-lookup"><span data-stu-id="346c9-108">Gets an interface pointer to an `IEnumIDENTITY_ATTRIBUTE` instance that contains the attributes associated with this `IReferenceIdentity`.</span></span>|  
|`IReferenceIdentity::GetAttribute`|<span data-ttu-id="346c9-109">Obtient la valeur de l’attribut dans l’espace de noms spécifié, avec le nom spécifié.</span><span class="sxs-lookup"><span data-stu-id="346c9-109">Gets the value of the attribute in the specified namespace, with the specified name.</span></span>|  
|`IReferenceIdentity::SetAttribute`|<span data-ttu-id="346c9-110">Définit l’attribut qui a l’espace de noms spécifié et le nom spécifié à la valeur spécifiée.</span><span class="sxs-lookup"><span data-stu-id="346c9-110">Sets the attribute that has the specified namespace and the specified name to the specified value.</span></span>|  
  
## <a name="requirements"></a><span data-ttu-id="346c9-111">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="346c9-111">Requirements</span></span>  
 <span data-ttu-id="346c9-112">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="346c9-112">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="346c9-113">**En-tête :** Isolation.h</span><span class="sxs-lookup"><span data-stu-id="346c9-113">**Header:** Isolation.h</span></span>  
  
 <span data-ttu-id="346c9-114">**Versions du .NET Framework :** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="346c9-114">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="346c9-115">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="346c9-115">See also</span></span>

- [<span data-ttu-id="346c9-116">Interfaces de fusion</span><span class="sxs-lookup"><span data-stu-id="346c9-116">Fusion Interfaces</span></span>](../../../../docs/framework/unmanaged-api/fusion/fusion-interfaces.md)
- [<span data-ttu-id="346c9-117">IEnumIDENTITY_ATTRIBUTE, interface</span><span class="sxs-lookup"><span data-stu-id="346c9-117">IEnumIDENTITY_ATTRIBUTE Interface</span></span>](../../../../docs/framework/unmanaged-api/fusion/ienumidentity-attribute-interface.md)
