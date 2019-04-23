---
title: <localIssuer>
ms.date: 03/30/2017
ms.assetid: 26bdd0df-0e7d-4b9e-bbeb-f28c53769385
ms.openlocfilehash: 9a51387cd75d57a6828ecde1dcd788b056f7e27a
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59122874"
---
# <a name="localissuer"></a>\<localIssuer>
Spécifie l'adresse et la liaison de l'émetteur local à utiliser pour obtenir un jeton de sécurité.  
  
 \<system.ServiceModel>  
\<behaviors>  
section d’endpointBehaviors  
\<behavior>  
\<clientCredentials>  
\<issuedToken>  
\<localIssuer>  
  
## <a name="syntax"></a>Syntaxe  
  
```xml  
<localIssuer address="String"
             binding="String"
             bindingConfiguration="String" />
```  
  
## <a name="attributes-and-elements"></a>Attributs et éléments  
 Les sections suivantes décrivent des attributs, des éléments enfants et des éléments parents.  
  
### <a name="attributes"></a>Attributs  
  
|Attribut|Description|  
|---------------|-----------------|  
|adresse|Chaîne requise. Spécifie l'URI de l'émetteur local.|  
|liaison|Chaîne facultative. Une des liaisons fournies par le système. Pour obtenir la liste, consultez [System-Provided Bindings](../../../../../docs/framework/wcf/system-provided-bindings.md).|  
|bindingConfiguration|Chaîne facultative. Spécifie une configuration de liaison recherchée dans le fichier de configuration.|  
  
### <a name="child-elements"></a>Éléments enfants  
  
|Élément|Description|  
|-------------|-----------------|  
|[\<identity>](../../../../../docs/framework/configure-apps/file-schema/wcf/identity.md)|Spécifie les informations d'identité de l'émetteur local.|  
|[\<headers>](../../../../../docs/framework/configure-apps/file-schema/wcf/headers-element.md)|Collection d'en-têtes d'adresse requis pour adresser correctement l'émetteur local. Vous pouvez utiliser le mot clé `add` pour ajouter un en-tête à cette collection.|  
  
### <a name="parent-elements"></a>Éléments parents  
  
|Élément|Description|  
|-------------|-----------------|  
|[\<issuedToken>](../../../../../docs/framework/configure-apps/file-schema/wcf/issuedtoken.md)|Spécifie un jeton personnalisé utilisé pour authentifier un client auprès d'un service.|  
  
## <a name="remarks"></a>Notes  
 Lors de l'obtention d'un jeton émis depuis un service d'émission de jeton de sécurité (STS), l'application cliente doit être configurée avec l'adresse et la liaison à utiliser pour pouvoir communiquer avec le STS. Lorsque le <xref:System.ServiceModel.WSFederationHttpBinding> ne fournit pas d’URL pour le service de jeton de sécurité, ou lorsque l’adresse de l’émetteur d’une liaison fédérée est `http://schemas.microsoft.com/2005/12/ServiceModel/Addressing/Anonymous` ou `null`, le canal de client Windows Communication Foundation (WCF) utilise les valeurs spécifiées par `address`et `binding` pour communiquer avec le STS pour obtenir le jeton émis. Pour plus d’informations sur la configuration d’un émetteur local, consultez [Comment : Configurer un émetteur Local](../../../../../docs/framework/wcf/feature-details/how-to-configure-a-local-issuer.md).  
  
## <a name="example"></a>Exemple  
 L'exemple suivant définit les attributs `address`, `binding` et `bindingConfiguration` d'un élément `localIssuer`.  
  
```xml  
<system.serviceModel>
  <behaviors>
    <endpointBehaviors>
      <behavior name="MyEndpointBehavior">
        <clientCredentials>
          <issuedToken cacheIssuedTokens="false"
                       defaultKeyEntropyMode="ClientEntropy">
            <localIssuer address="net.tcp://cohowinery/tokens"
                         binding="netTcpBinding"
                         bindingConfiguration="myTcpBindingConfig" />
          </issuedToken>
        </clientCredentials>
      </behavior>
    </endpointBehaviors>
  </behaviors>
</system.serviceModel>
```  
  
## <a name="see-also"></a>Voir aussi

- <xref:System.ServiceModel.Configuration.IssuedTokenClientElement.LocalIssuer%2A>
- <xref:System.ServiceModel.Configuration.IssuedTokenParametersEndpointAddressElement>
- <xref:System.ServiceModel.Security.IssuedTokenClientCredential>
- [Comportements de sécurité](../../../../../docs/framework/wcf/feature-details/security-behaviors-in-wcf.md)
- [Guide pratique pour Configurer un émetteur Local](../../../../../docs/framework/wcf/feature-details/how-to-configure-a-local-issuer.md)
- [Identité du service et authentification](../../../../../docs/framework/wcf/feature-details/service-identity-and-authentication.md)
- [Comportements de sécurité](../../../../../docs/framework/wcf/feature-details/security-behaviors-in-wcf.md)
- [Fédération et jetons émis](../../../../../docs/framework/wcf/feature-details/federation-and-issued-tokens.md)
- [Sécurisation des services et des clients](../../../../../docs/framework/wcf/feature-details/securing-services-and-clients.md)
- [Sécurisation des clients](../../../../../docs/framework/wcf/securing-clients.md)
- [Guide pratique pour Créer un Client fédéré](../../../../../docs/framework/wcf/feature-details/how-to-create-a-federated-client.md)
- [Fédération et jetons émis](../../../../../docs/framework/wcf/feature-details/federation-and-issued-tokens.md)
