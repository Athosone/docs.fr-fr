---
title: Chiffrement de signatures numériques
ms.date: 03/30/2017
helpviewer_keywords:
- encryption of digital signatures [WCF]
- digital signatures [WCF], encryption
- digital signatures [WCF]
ms.assetid: 0868866d-40b4-4341-8e42-eee3b7f15b69
ms.openlocfilehash: ea53a575802f1e7903a66c2eda466c8937fb02f9
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59341593"
---
# <a name="encryption-of-digital-signatures"></a>Chiffrement de signatures numériques
Par défaut, un message est signé et chiffré et sa signature chiffrée numériquement. Vous pouvez contrôler ce paramètre en créant une liaison personnalisée à l’aide d’une instance de <xref:System.ServiceModel.Channels.AsymmetricSecurityBindingElement> ou de <xref:System.ServiceModel.Channels.SymmetricSecurityBindingElement>, puis en affectant à la propriété `MessageProtectionOrder` de l’une de ces deux classes une valeur d’énumération <xref:System.ServiceModel.Security.MessageProtectionOrder>. La valeur par défaut est <xref:System.ServiceModel.Security.MessageProtectionOrder.SignBeforeEncryptAndEncryptSignature>. Ce processus nécessite 10 à 40 pour cent plus de temps que lorsque les messages sont seulement signés et chiffrés. Toutefois, désactiver le chiffrement de la signature présente un risque en matière de sécurité, les intrus pouvant deviner en son absence le contenu des messages. En effet, l'élément de la signature contient le code de hachage du texte brut de chaque partie signée du message. Par exemple, même si le corps des messages est chiffré par défaut, la signature non chiffrée contient le code de hachage du corps des messages. Si le message est petit, un intrus risque de parvenir à déduire son contenu. Le chiffrement de la signature limite ou élimine complètement ce risque.  
  
 En conclusion, désactivez uniquement le chiffrement de la signature lorsque les messages ne contiennent pas d'informations à caractère sensible et lorsque cela peut permettre une amélioration significative des performances, par exemple lorsque vous envoyez des fichiers binaires de grande taille ne nécessitant pas de protection particulière.  
  
### <a name="to-disable-digital-signing"></a>Pour désactiver la signature numérique  
  
1. Créer un <xref:System.ServiceModel.Channels.CustomBinding>. Pour plus d'informations, voir [Procédure : Créer une liaison personnalisée à l’aide de SecurityBindingElement](../../../../docs/framework/wcf/feature-details/how-to-create-a-custom-binding-using-the-securitybindingelement.md).  
  
2. Ajoutez un élément <xref:System.ServiceModel.Channels.AsymmetricSecurityBindingElement> ou un élément <xref:System.ServiceModel.Channels.SymmetricSecurityBindingElement> à la collection de liaisons.  
  
3. Affectez à la propriété <xref:System.ServiceModel.Channels.AsymmetricSecurityBindingElement.MessageProtectionOrder%2A?displayProperty=nameWithType> la valeur <xref:System.ServiceModel.Security.MessageProtectionOrder.SignBeforeEncrypt> ou affectez à la propriété <xref:System.ServiceModel.Channels.SymmetricSecurityBindingElement.MessageProtectionOrder%2A?displayProperty=nameWithType> la valeur <xref:System.ServiceModel.Security.MessageProtectionOrder.SignBeforeEncrypt>.  
  
 Pour plus d’informations sur la création de liaisons personnalisées, consultez [Creating liaisons](../../../../docs/framework/wcf/extending/creating-user-defined-bindings.md). Pour plus d’informations sur la création d’une liaison personnalisée pour un mode d’authentification spécifiques, consultez [Comment : Créer un SecurityBindingElement pour un Mode d’authentification spécifié](../../../../docs/framework/wcf/feature-details/how-to-create-a-securitybindingelement-for-a-specified-authentication-mode.md).  
  
## <a name="see-also"></a>Voir aussi

- <xref:System.ServiceModel.Security.MessageProtectionOrder>
- <xref:System.ServiceModel.Channels.AsymmetricSecurityBindingElement>
- <xref:System.ServiceModel.Channels.SymmetricSecurityBindingElement>
- [Guide pratique pour Créer une liaison personnalisée à l’aide de SecurityBindingElement](../../../../docs/framework/wcf/feature-details/how-to-create-a-custom-binding-using-the-securitybindingelement.md)
- [Création de liaisons définies par l’utilisateur](../../../../docs/framework/wcf/extending/creating-user-defined-bindings.md)
- [Guide pratique pour Créer un SecurityBindingElement pour un Mode d’authentification spécifié](../../../../docs/framework/wcf/feature-details/how-to-create-a-securitybindingelement-for-a-specified-authentication-mode.md)
