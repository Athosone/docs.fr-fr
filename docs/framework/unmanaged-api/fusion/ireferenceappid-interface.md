---
title: IReferenceAppId, interface
ms.date: 03/30/2017
api_name:
- IReferenceAppId
api_location:
- fusion.dll
api_type:
- COM
f1_keywords:
- IReferenceAppId
helpviewer_keywords:
- IReferenceAppId interface [.NET Framework fusion]
ms.assetid: 8eb9e565-f358-43ce-900e-a8f8a5aa6cfb
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 25733e459423500352595d6be0eee26ef75ca7e2
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59157194"
---
# <a name="ireferenceappid-interface"></a>IReferenceAppId, interface
Représente une référence à l’identificateur unique pour l’application dans la portée actuelle.  
  
## <a name="methods"></a>Méthodes  
  
|Méthode|Description|  
|------------|-----------------|  
|`IReferenceAppId::get_CodeBase`|Obtient un pointeur vers une représentation sous forme de chaîne de l’identificateur de code de l’application référencée par ce `IReferenceAppId`.|  
|`IReferenceAppId::put_CodeBase`|Définit l’identificateur de code de l’application référencée par ce `IReferenceAppId`.|  
|`IReferenceAppId::EnumAppPath`|Obtient un pointeur d’interface vers un `IEnumReferenceIdentity` instance contenant le `IReferenceIdentity` instances qui représentent les membres de ce `IReferenceAppId`.|  
|`IReferenceAppId::get_SubscriptionId`|Obtient un pointeur vers une représentation sous forme de chaîne de l’identificateur de jeton pour un abonnement à ce `IReferenceAppId`.|  
|`IReferenceAppId::put_SubscriptionId`|Définit l’identificateur de jeton pour un abonnement à ce `IReferenceAppId` à la valeur de chaîne spécifiée.|  
  
## <a name="requirements"></a>Configuration requise  
 **Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).  
  
 **En-tête :** Isolation.h  
  
 **Versions du .NET Framework :** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]  
  
## <a name="see-also"></a>Voir aussi

- [Interfaces de fusion](../../../../docs/framework/unmanaged-api/fusion/fusion-interfaces.md)
- [IEnumReferenceIdentity, interface](../../../../docs/framework/unmanaged-api/fusion/ienumreferenceidentity-interface.md)
- [IReferenceIdentity, interface](../../../../docs/framework/unmanaged-api/fusion/ireferenceidentity-interface.md)
