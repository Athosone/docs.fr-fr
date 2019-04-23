---
title: <add> de <claimTypeRequirements>
ms.date: 03/30/2017
ms.assetid: c68e83c9-39e8-4264-b1ce-b6a9eb5b98aa
ms.openlocfilehash: 97d3ecca369aeffb7b2e8464f385eeae13bd470f
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59168842"
---
# <a name="add-of-claimtyperequirements"></a>\<add> of \<claimTypeRequirements>
Spécifie les types de revendications requis et facultatifs censés apparaître dans les informations d'identification fédérées. Par exemple, les services déclarent les exigences relatives aux informations d’identification entrantes devant posséder un certain jeu de types de revendications.  
  
 \<system.serviceModel>  
\<bindings>  
\<customBinding>  
\<binding>  
\<security>  
\<issuedTokenParameters>  
\<claimTypeRequirements>  
  
## <a name="syntax"></a>Syntaxe  
  
```xml  
<claimTypeRequirements>
  <add claimType="URI"
       isOptional="Boolean" />
</claimTypeRequirements>
```  
  
## <a name="attributes-and-elements"></a>Attributs et éléments  
 Les sections suivantes décrivent des attributs, des éléments enfants et des éléments parents.  
  
### <a name="attributes"></a>Attributs  
  
|Attribut|Description|  
|---------------|-----------------|  
|claimType|URI définissant le type d'une revendication. Par exemple, pour acheter un produit d'un site Web, l'utilisateur doit présenter une carte de crédit valide avec limite de crédit suffisante. Le type de revendication est l'URI de la carte de crédit.|  
|isOptional|Valeur booléenne indiquant si l'opération concerne une revendication facultative. Affectez à cet attribut la valeur `false` si c'est une revendication requise.<br /><br /> Vous pouvez utiliser cet attribut lorsque le service demande certaines informations sans pour autant les exiger. Par exemple, si vous décidez que l'utilisateur doit indiquer ses prénom, nom et adresse mais pas forcément son numéro de téléphone.|  
  
### <a name="child-elements"></a>Éléments enfants  
 Aucun.  
  
### <a name="parent-elements"></a>Éléments parents  
  
|Élément|Description|  
|-------------|-----------------|  
|[\<claimTypeRequirements>](../../../../../docs/framework/configure-apps/file-schema/wcf/claimtyperequirements-element.md)|Spécifie une collection de types de revendications requis.<br /><br /> Dans un scénario fédéré, les services déclarent les spécifications relatives aux informations d'identification entrantes. Par exemple, ces informations d'identification doivent posséder un jeu de types de revendications défini. Chaque élément de la collection indique les types de revendications requis et facultatifs censés apparaître dans les informations d'identification fédérées.|  
  
## <a name="remarks"></a>Notes  
 Dans un scénario fédéré, les services déclarent les spécifications relatives aux informations d'identification entrantes. Par exemple, ces informations d'identification doivent posséder un jeu de types de revendications défini. Cette exigence est explicitée dans une stratégie de sécurité. Lorsqu’un client requiert des informations d’identification à partir d’un service fédéré (CardSpace, par exemple), il indique ces exigences dans une demande de jeton (RequestSecurityToken) afin que le service fédéré puisse publier ces informations et répondre aux exigences.  
  
## <a name="example"></a>Exemple  
 La configuration suivante ajoute deux exigences de type de revendication à une liaison de sécurité.  
  
```xml  
<bindings>
  <wsFederationHttpBinding>
    <binding name="myFederatedBinding">
      <security mode="Message">
        <message issuedTokenType="urn:oasis:names:tc:SAML:1.0:assertion">
          <claimTypeRequirements>
            <add claimType="http://schemas.microsoft.com/ws/2005/05/identity/claims/EmailAddress" />
            <add claimType="http://schemas.microsoft.com/ws/2005/05/identity/claims/UserName"
                 optional="true" />
          </claimTypeRequirements>
        </message>
      </security>
    </binding>
  </wsFederationHttpBinding>
</bindings>
```  
  
## <a name="see-also"></a>Voir aussi

- <xref:System.ServiceModel.Security.Tokens.ClaimTypeRequirement>
- <xref:System.ServiceModel.Security.Tokens.IssuedSecurityTokenParameters.ClaimTypeRequirements%2A>
- <xref:System.ServiceModel.Configuration.IssuedTokenParametersElement.ClaimTypeRequirements%2A>
- <xref:System.ServiceModel.Configuration.ClaimTypeElementCollection>
- <xref:System.ServiceModel.Configuration.ClaimTypeElement>
- <xref:System.ServiceModel.Channels.CustomBinding>
- [\<claimTypeRequirements>](../../../../../docs/framework/configure-apps/file-schema/wcf/claimtyperequirements-element.md)
- [Liaisons](../../../../../docs/framework/wcf/bindings.md)
- [Extension de liaisons](../../../../../docs/framework/wcf/extending/extending-bindings.md)
- [Liaisons personnalisées](../../../../../docs/framework/wcf/extending/custom-bindings.md)
- [\<customBinding>](../../../../../docs/framework/configure-apps/file-schema/wcf/custombinding.md)
- [Guide pratique pour Créer une liaison personnalisée à l’aide de SecurityBindingElement](../../../../../docs/framework/wcf/feature-details/how-to-create-a-custom-binding-using-the-securitybindingelement.md)
- [Sécurité de liaison personnalisée](../../../../../docs/framework/wcf/samples/custom-binding-security.md)
