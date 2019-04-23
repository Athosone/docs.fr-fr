---
title: Jetons SAML et revendications
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- WCF, federation
- federation
- issued tokens
- SAML token
ms.assetid: 930b6e34-9eab-4e95-826c-4e06659bb977
ms.openlocfilehash: 04517e5089f55c2d2b08a492439026d33ed9069d
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59339838"
---
# <a name="saml-tokens-and-claims"></a>Jetons SAML et revendications
Security Assertions Markup Language (SAML) *jetons* sont des représentations XML de revendications. Par défaut, les jetons SAML Windows Communication Foundation (WCF) utilise dans les scénarios de sécurité fédérée sont *jetons émis*.  
  
 Les jetons SAML comportent des instructions qui sont des ensembles de revendications générées par une entité au sujet d'une autre entité. Par exemple, dans des scénarios de sécurité fédérée, les instructions sont générées par un service de jeton de sécurité au sujet d'un utilisateur dans le système. Le service de jeton de sécurité signe le jeton SAML pour indiquer la véracité des instructions incluses dans le jeton. De plus, le jeton SAML est associé à du matériel de clé de chiffrement dont l'utilisateur du jeton SAML prouve la connaissance. Cette preuve satisfait la partie de confiance que le jeton SAML a été émis, en fait, pour cet utilisateur. Par exemple, dans un scénario classique :  
  
1. Un client demande un jeton SAML à un service de jeton de sécurité en s'authentifiant auprès de ce service à l'aide des informations d'identification Windows.  
  
2. Le service de jeton de sécurité émet un jeton SAML pour le client. Le jeton SAML est signé avec un certificat associé au service de jeton de sécurité et contient une clé de vérification chiffrée pour le service cible.  
  
3. Le client reçoit également une copie de la *clé de vérification*. Le client présente alors le jeton SAML au service d’application (le *confiance*) et signe le message avec cette clé de vérification.  
  
4. La signature sur le jeton SAML indique à la partie de confiance que le service de jeton de sécurité a émis le jeton. La signature de message créée avec la clé de vérification indique à la partie de confiance que le jeton a été émis pour le client.  
  
## <a name="from-claims-to-samlattributes"></a>Des revendications aux éléments SamlAttributes  
 Dans WCF, les instructions dans les jetons SAML sont modélisées en tant que <xref:System.IdentityModel.Tokens.SamlAttribute> objets qui peuvent être remplis directement à partir de <xref:System.IdentityModel.Claims.Claim> objets, fournis le <xref:System.IdentityModel.Claims.Claim> objet a un <xref:System.IdentityModel.Claims.Claim.Right%2A> propriété de <xref:System.IdentityModel.Claims.Rights.PossessProperty%2A> et le <xref:System.IdentityModel.Claims.Claim.Resource%2A> propriété est de type <xref:System.String>. Exemple :  
  
 [!code-csharp[c_CreateSTS#8](../../../../samples/snippets/csharp/VS_Snippets_CFX/c_creatests/cs/source.cs#8)]
 [!code-vb[c_CreateSTS#8](../../../../samples/snippets/visualbasic/VS_Snippets_CFX/c_creatests/vb/source.vb#8)]  
  
> [!NOTE]
>  Lorsque des jetons SAML sont sérialisés dans des messages, lorsqu'ils sont émis par un service de jeton de sécurité ou lorsqu'ils sont présentés par des clients à des services dans le cadre de l'authentification, le quota de taille maximale de message doit être suffisamment important pour prendre en charge le jeton SAML et les autres parties du message. Dans un cas normal, les quotas de taille de message par défaut sont suffisants. Toutefois, dans le cas où un jeton SAML est de grande taille parce qu'il contient des centaines de revendications, vous pouvez avoir besoin d'augmenter les quotas pour prendre en charge le jeton sérialisé. Pour plus d’informations, consultez [considérations de sécurité pour les données](../../../../docs/framework/wcf/feature-details/security-considerations-for-data.md).  
  
## <a name="from-samlattributes-to-claims"></a>Des éléments SamlAttributes aux revendications  
 Lorsque des jetons SAML sont reçus dans des messages, les différentes instructions incluses dans le jeton SAML sont transformées en objets <xref:System.IdentityModel.Policy.IAuthorizationPolicy> qui sont placés dans <xref:System.IdentityModel.Policy.AuthorizationContext>. Les revendications provenant de chaque instruction SAML sont retournées par la propriété <xref:System.IdentityModel.Policy.AuthorizationContext.ClaimSets%2A> de <xref:System.IdentityModel.Policy.AuthorizationContext> et peuvent être examinées pour déterminer s'il convient d'authentifier et d'autoriser l'utilisateur.  
  
## <a name="see-also"></a>Voir aussi

- <xref:System.IdentityModel.Policy.AuthorizationContext>
- <xref:System.IdentityModel.Policy.IAuthorizationPolicy>
- <xref:System.IdentityModel.Claims.ClaimSet>
- [Fédération](../../../../docs/framework/wcf/feature-details/federation.md)
- [Guide pratique pour Créer un Client fédéré](../../../../docs/framework/wcf/feature-details/how-to-create-a-federated-client.md)
- [Guide pratique pour Configurer les informations d’identification sur un Service de fédération](../../../../docs/framework/wcf/feature-details/how-to-configure-credentials-on-a-federation-service.md)
- [Gestion des revendications et autorisation avec le modèle d’identité](../../../../docs/framework/wcf/feature-details/managing-claims-and-authorization-with-the-identity-model.md)
- [Revendications et jetons](../../../../docs/framework/wcf/feature-details/claims-and-tokens.md)
- [Création de revendications et valeurs de ressource](../../../../docs/framework/wcf/feature-details/claim-creation-and-resource-values.md)
- [Guide pratique pour Créer une revendication personnalisée](../../../../docs/framework/wcf/extending/how-to-create-a-custom-claim.md)
