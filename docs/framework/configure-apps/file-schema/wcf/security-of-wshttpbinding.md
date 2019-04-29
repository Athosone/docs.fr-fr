---
title: <security> de <wsHttpBinding>
ms.date: 03/30/2017
ms.assetid: 8658b162-2ddf-4162-a869-aa517a42288a
ms.openlocfilehash: 68d3aa4da793e0338c2b0b704335bafce7cc3e31
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61670393"
---
# <a name="security-of-wshttpbinding"></a>\<sécurité > de \<wsHttpBinding >
Représente les fonctionnalités de sécurité de la [ \<wsHttpBinding >](../../../../../docs/framework/configure-apps/file-schema/wcf/wshttpbinding.md).  
  
 \<system.ServiceModel>  
\<bindings>  
\<wsHttpBinding>  
\<binding>  
\<security>  
  
## <a name="syntax"></a>Syntaxe  
  
```xml  
<security mode="Message/None/Transport/TransportWithMessageCredential">
  <transport clientCredentialType="Basic/Certificate/Digest/None/Ntlm/Windows"
             proxyCredentialType="Basic/Digest/None/Ntlm/Windows"
             realm="String"
             defaultClientCredentialType="Basic/Certificate/Digest/None/Ntlm/Windows"
             defaultProxyCredentialType="Basic/Digest/None/Ntlm/Windows"
             defaultRealm="String" />
  <message clientCredentialType="Certificate/IssuedToken/None/UserName/Windows"
           algorithmSuite="Basic128/Basic192/Basic256/Basic128Rsa15/Basic256Rsa15/TripleDes/TripleDesRsa15/Basic128Sha256/Basic192Sha256/TripleDesSha256/Basic128Sha256Rsa15/Basic192Sha256Rsa15/Basic256Sha256Rsa15/TripleDesSha256Rsa15"
           establishSecurityContext="Boolean"
           negotiateServiceCredential="Boolean" />
</security>
```  
  
## <a name="attributes-and-elements"></a>Attributs et éléments  
 Les sections suivantes décrivent des attributs, des éléments enfants et des éléments parents.  
  
### <a name="attributes"></a>Attributs  
  
|Attribut|Description|  
|---------------|-----------------|  
|mode|-Facultatif. Spécifie le type de sécurité appliqué. La valeur par défaut est `Message`.<br />-Cet attribut est de type <xref:System.ServiceModel.SecurityMode>.|  
  
## <a name="mode-attribute"></a>Mode, attribut  
  
|Value|Description|  
|-----------|-----------------|  
|Aucun.|La sécurité est désactivée.|  
|Transport|La sécurité est fournie à l'aide de HTTPS. Le service doit être configuré avec les certificats SSL. Le message est entièrement sécurisé grâce à HTTPS et est authentifié par le client à l’aide du certificat SSL du service. L'authentification du client est contrôlée à l'aide de l'attribut `ClientCredentials`. de la [ \<transport >](../../../../../docs/framework/configure-apps/file-schema/wcf/transport-of-wshttpbinding.md).|  
|Message|La sécurité est fournie à l'aide de la sécurité des messages SOAP. Par défaut, le corps SOAP est chiffré et signé. Ce mode offre diverses fonctionnalités, telles que, si les informations d’identification du service sont disponibles au client hors bande, la suite algorithmique à utiliser et quel niveau de protection à appliquer au corps du message grâce à la propriété Security.Message. L'authentification du client est exécutée une fois par session et les résultats d'authentification sont mis en cache pour la durée de la session.|  
|TransportWithMessageCredential|Dans ce mode, le protocole HTTPS garantit l'intégrité, la confidentialité et l'authentification du serveur, et la sécurité des messages SOAP garantit l'authentification du client. Par défaut, l'authentification du client est exécutée une fois par session et les résultats d'authentification sont mis en cache pour la durée de la session.|  
  
### <a name="child-elements"></a>Éléments enfants  
  
|Élément|Description|  
|-------------|-----------------|  
|[\<transport>](../../../../../docs/framework/configure-apps/file-schema/wcf/transport-of-wshttpbinding.md)|Définit les paramètres de sécurité de transport. Cet élément correspond au type <xref:System.ServiceModel.Configuration.HttpTransportSecurityElement>.|  
|[\<message>](../../../../../docs/framework/configure-apps/file-schema/wcf/message-of-wshttpbinding.md)|Définit les paramètres de sécurité pour le message. Cet élément correspond au type <xref:System.ServiceModel.Configuration.MessageSecurityOverHttpElement>.|  
  
### <a name="parent-elements"></a>Éléments parents  
  
|Élément|Description|  
|-------------|-----------------|  
|[\<wsHttpBinding>](../../../../../docs/framework/configure-apps/file-schema/wcf/wshttpbinding.md)|Liaison sécurisée pour les applications de transport HTTP.|  
  
## <a name="remarks"></a>Notes  
 La classe WSHttpBinding est conçue pour interagir avec les services qui implémentent les spécifications WS-*. La sécurité de transport de cette liaison correspond à Secure Sockets Layer (SSL) sur HTTP, c'est-à-dire à HTTPS.  
  
## <a name="see-also"></a>Voir aussi

- <xref:System.ServiceModel.WSHttpSecurity>
- <xref:System.ServiceModel.WSHttpBinding.Security%2A>
- <xref:System.ServiceModel.Configuration.WSHttpBindingElement.Security%2A>
- <xref:System.ServiceModel.Configuration.WSHttpSecurityElement>
- [Sécurisation des services et des clients](../../../../../docs/framework/wcf/feature-details/securing-services-and-clients.md)
- [Liaisons](../../../../../docs/framework/wcf/bindings.md)
- [Configuration des liaisons fournies par le système](../../../../../docs/framework/wcf/feature-details/configuring-system-provided-bindings.md)
- [Utilisation de liaisons pour configurer des services et des clients](../../../../../docs/framework/wcf/using-bindings-to-configure-services-and-clients.md)
- [\<binding>](../../../../../docs/framework/misc/binding.md)
