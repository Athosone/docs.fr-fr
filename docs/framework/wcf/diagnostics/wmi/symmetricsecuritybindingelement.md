---
title: SymmetricSecurityBindingElement
ms.date: 03/30/2017
ms.assetid: b2e182b6-c041-4d80-a926-6058068d9f79
ms.openlocfilehash: f6effd533a205d0e8fd1421119e325f06b340dd1
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61956713"
---
# <a name="symmetricsecuritybindingelement"></a>SymmetricSecurityBindingElement
SymmetricSecurityBindingElement  
  
## <a name="syntax"></a>Syntaxe  
  
```csharp
class SymmetricSecurityBindingElement : SecurityBindingElement  
{  
  string MessageProtectionOrder;  
  boolean RequireSignatureConfirmation;  
};  
```  
  
## <a name="methods"></a>Méthodes  
 La classe SymmetricSecurityBindingElement ne définit pas de méthodes.  
  
## <a name="properties"></a>Properties  
 La classe SymmetricSecurityBindingElement a les propriétés suivantes :  
  
### <a name="messageprotectionorder"></a>MessageProtectionOrder  
 Type de données : chaîne  
  
 Type d’accès : Propriétés en lecture seule  
  
 Ordre de chiffrement et de signature des messages de cette liaison.  
  
### <a name="requiresignatureconfirmation"></a>RequireSignatureConfirmation  
 Type de données : booléen  
  
 Type d’accès : Propriétés en lecture seule  
  
 Si la liaison requiert la confirmation de signature.  
  
## <a name="requirements"></a>Configuration requise  
  
|MOF|Déclaré dans Servicemodel.mof.|  
|---------|-----------------------------------|  
|Espace de noms|Défini dans root\ServiceModel|  
  
## <a name="see-also"></a>Voir aussi

- <xref:System.ServiceModel.Channels.SymmetricSecurityBindingElement>
