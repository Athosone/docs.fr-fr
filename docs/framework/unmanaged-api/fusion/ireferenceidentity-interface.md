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
# <a name="ireferenceidentity-interface"></a>IReferenceIdentity, interface
Représente une référence à la signature unique d’un objet de code.  
  
## <a name="methods"></a>Méthodes  
  
|Méthode|Description|  
|------------|-----------------|  
|`IReferenceIdentity::Clone`|Obtient un pointeur d’interface vers un nouveau `IReferenceIdentity` instance qui est identique à ce `IReferenceIdentity`, sauf pour les modifications de l’attribut spécifié.|  
|`IReferenceIdentity::EnumAttributes`|Obtient un pointeur d’interface vers un `IEnumIDENTITY_ATTRIBUTE` instance qui contient les attributs associés à ce `IReferenceIdentity`.|  
|`IReferenceIdentity::GetAttribute`|Obtient la valeur de l’attribut dans l’espace de noms spécifié, avec le nom spécifié.|  
|`IReferenceIdentity::SetAttribute`|Définit l’attribut qui a l’espace de noms spécifié et le nom spécifié à la valeur spécifiée.|  
  
## <a name="requirements"></a>Configuration requise  
 **Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).  
  
 **En-tête :** Isolation.h  
  
 **Versions du .NET Framework :** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]  
  
## <a name="see-also"></a>Voir aussi

- [Interfaces de fusion](../../../../docs/framework/unmanaged-api/fusion/fusion-interfaces.md)
- [IEnumIDENTITY_ATTRIBUTE, interface](../../../../docs/framework/unmanaged-api/fusion/ienumidentity-attribute-interface.md)
