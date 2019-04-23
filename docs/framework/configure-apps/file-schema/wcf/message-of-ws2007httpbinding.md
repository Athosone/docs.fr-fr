---
title: <message> de <ws2007HttpBinding>
ms.date: 03/30/2017
ms.assetid: 9ffd8db6-84a8-4b38-a9fe-2cb1a87a1c97
ms.openlocfilehash: bf0ed2de73505d5634d6c7d26881f9800a0bf1f2
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59166736"
---
# <a name="message-of-ws2007httpbinding"></a>\<message > de \<ws2007HttpBinding >
Définit les paramètres de sécurité au niveau du message de la [ \<ws2007HttpBinding >](../../../../../docs/framework/configure-apps/file-schema/wcf/ws2007httpbinding.md) élément.  
  
 \<system.ServiceModel>  
\<bindings>  
\<ws2007HttpBinding>  
\<binding>  
\<security>  
\<message>  
  
## <a name="syntax"></a>Syntaxe  
  
```xml  
<ws2007HttpBinding>
  <binding>
    <security>
      <message clientCredentialType="None/Windows/UserName/Certificate/IssuedToken"
               establishSecurityContext="Boolean"
               negotiateServiceCredential="Boolean"
               algorithmSuite="Enumeration. See algorithmSuite Attribute below."
               defaultProtectionLevel="None/Sign/EncryptionAndSign" />
    </security>
  </binding>
</ws2007HttpBinding>
```  
  
## <a name="type"></a>Type  
 <xref:System.ServiceModel.NonDualMessageSecurityOverHttp>  
  
## <a name="attributes-and-elements"></a>Attributs et éléments  
 Les sections suivantes décrivent des attributs, des éléments enfants et des éléments parents.  
  
### <a name="attributes"></a>Attributs  
  
|Attribut|Description|  
|---------------|-----------------|  
|`algorithmSuite`|Définit les algorithmes de chiffrement de message et de clé de type WRAP. Les algorithmes et les tailles de clé sont déterminés par la classe <xref:System.ServiceModel.Security.SecurityAlgorithmSuite>. Ces algorithmes se mappent à ceux définis dans la spécification Security Policy Language (WS-SecurityPolicy).<br /><br /> La valeur par défaut est Basic256.|  
|`clientCredentialType`|Optionnel. Spécifie le type d'informations d'identification à utiliser lorsque l'exécution de l'authentification du client à l'aide du mode de sécurité a la valeur `Message` ou `TransportWithMessageCredentials`. Consultez les valeurs d'énumération dans le tableau suivant. Le paramètre par défaut est Windows.<br /><br /> Cet attribut est de type <xref:System.ServiceModel.MessageCredentialType>.|  
|`establishSecurityContext`|Valeur indiquant si le canal de sécurité établit une session sécurisée. Une session sécurisée établit un jeton de contexte de sécurité (SCT) avant d'échanger les messages d'application. Lorsque le jeton SCT est établi, le canal de sécurité offre une interface <xref:System.ServiceModel.Channels.ISession> aux canaux supérieurs. Pour plus d’informations sur l’utilisation des sessions sécurisées, consultez [Comment : Créer une Session sécurisée](../../../../../docs/framework/wcf/feature-details/how-to-create-a-secure-session.md).<br /><br /> La valeur par défaut est `true`.|  
|`negotiateServiceCredential`|Optionnel. Valeur indiquant si les informations d'identification du service sont configurées auprès du client hors bande ou transférées du service au client via un processus de négociation. Ce type de négociation précède l'échange habituel de messages.<br /><br /> Si le `clientCredentialType` attribut a la valeur None, Username ou Certificate, cet attribut `false` implique que le certificat de service est disponible au niveau du client hors bande et que le client doit spécifier le certificat de service (à l’aide de la [ \<serviceCertificate >](../../../../../docs/framework/configure-apps/file-schema/wcf/servicecertificate-of-servicecredentials.md)) dans le [ \<serviceCredentials >](../../../../../docs/framework/configure-apps/file-schema/wcf/servicecredentials.md) comportement de service. Ce mode est interopérable avec les piles SOAP qui implémentent WS-Trust et WS-SecureConversation.<br /><br /> Si l'attribut `ClientCredentialType` a la valeur `Windows`, l'affectation de la valeur `false` à cet attribut spécifie l'authentification basée sur Kerberos. Cela signifie que le client et le service doivent faire partie du même domaine Kerberos. Ce mode est interopérable avec les piles SOAP qui implémentent le profil de jeton Kerberos (comme défini dans OASIS WSS TC) ainsi que WS-Trust et WS-SecureConversation.<br /><br /> Lorsque cet attribut a la valeur `true`, il entraîne une négociation SOAP .NET qui tunnelle l'échange <xref:System.ServiceModel.Security.Tokens.ServiceModelSecurityTokenTypes.Spnego%2A> par des messages SOAP.<br /><br /> La valeur par défaut est `true`.|  
  
## <a name="algorithmsuite-attribute"></a>Attribut algorithmSuite  
  
|Value|Description|  
|-----------|-----------------|  
|Basic128|Utilisez le chiffrement Aes128, Sha1 pour le résumé du message et Rsa-oaep-mgf1p pour la clé de type WRAP.|  
|Basic192|Utilisez le chiffrement Aes192, Sha1 pour le résumé du message et Rsa-oaep-mgf1p pour la clé de type WRAP.|  
|Basic256|Utilisez le chiffrement Aes256, Sha1 pour le condensat du message et Rsa-oaep-mgf1p pour la clé de type WRAP.|  
|Basic256Rsa15|Utilisez Aes256 pour le chiffrement du message, Sha1 pour le condensat du message et Rsa15 pour la clé de type WRAP.|  
|Basic192Rsa15|Utilisez Aes192 pour le chiffrement du message, Sha1 pour le condensat du message et Rsa15 pour la clé de type WRAP.|  
|TripleDes|Utilisez le chiffrement TripleDes, Sha1 pour le condensat du message et Rsa-oaep-mgf1p pour la clé de type WRAP.|  
|Basic128Rsa15|Utilisez Aes128 pour le chiffrement du message, Sha1 pour le condensat du message et Rsa15 pour la clé de type WRAP.|  
|TripleDesRsa15|Utilisez le chiffrement TripleDes, Sha1 pour le condensat du message et Rsa15 pour la clé de type WRAP.|  
|Basic128Sha256|Utilisez Aes256 pour le chiffrement du message, Sha256 pour le résumé du message et Rsa-oaep-mgf1p pour la clé de type WRAP.|  
|Basic192Sha256|Utilisez Aes192 pour le chiffrement du message, Sha256 pour le condensat du message et Rsa-oaep-mgf1p pour la clé de type WRAP.|  
|Basic256Sha256|Utilisez Aes256 pour le chiffrement du message, Sha256 pour le résumé du message et Rsa-oaep-mgf1p pour la clé de type WRAP.|  
|TripleDesSha256|Utilisez TripleDes pour le chiffrement du message, Sha256 pour le résumé du message et Rsa-oaep-mgf1p pour la clé de type WRAP.|  
|Basic128Sha256Rsa15|Utilisez Aes128 pour le chiffrement du message, Sha256 pour le condensat du message et Rsa15 pour la clé de type WRAP.|  
|Basic192Sha256Rsa15|Utilisez Aes192 pour le chiffrement du message, Sha256 pour le condensat du message et Rsa15 pour la clé de type WRAP.|  
|Basic256Sha256Rsa15|Utilisez Aes256 pour le chiffrement du message, Sha256 pour le condensat du message et Rsa15 pour la clé de type WRAP.|  
|TripleDesSha256Rsa15|Utilisez TripleDes pour le chiffrement du message, Sha256 pour le condensat du message et Rsa15 pour la clé de type WRAP.|  
  
## <a name="clientcredentialtype-attribute"></a>Attribut clientCredentialType  
  
|Value|Description|  
|-----------|-----------------|  
|`None`|Permet au service d'interagir avec les clients anonymes. Au niveau du service, indique que ce dernier ne requiert pas d'informations d'identification du client. Au niveau du client, indique que ce dernier ne fournit pas d'informations d'identification du client.|  
|`Certificate`|Autorise le service à exiger une authentification du client via un certificat. Si le mode de sécurité `message` est utilisé et si l'attribut `negotiateServiceCredential` a la valeur `false`, le client doit disposer du certificat de service.|  
|`IssuedToken`|Spécifie un jeton personnalisé, généralement émis par un service de jeton de sécurité (STS).|  
|`UserName`|Autorise le service à exiger une authentification du client via un certificat `UserName`. WCF ne prend pas en charge l’envoi d’un mot de passe digest ou de dérivation de clés à l’aide du mot de passe et à l’aide de ces clés pour la sécurité de message. Par conséquent, WCF impose que le transport est sécurisé lors de l’utilisation `UserName` informations d’identification. Ce mode d'informations d'identification a pour résultat soit un échange interopérable, soit une négociation non interopérable basée sur l'attribut `negotiateServiceCredential`.|  
|`Windows`|Permet aux échanges SOAP d'être placés dans le contexte authentifié d'informations d'identification `Windows`. Si l'attribut `negotiateServiceCredential` a la valeur `true`, une négociation SSPI ou Kerberos (norme interopérable) est exécutée.|  
  
### <a name="child-elements"></a>Éléments enfants  
 Aucun.  
  
### <a name="parent-elements"></a>Éléments parents  
  
|Élément|Description|  
|-------------|-----------------|  
|[\<security>](../../../../../docs/framework/configure-apps/file-schema/wcf/security-of-ws2007httpbinding.md)|Définit les paramètres de sécurité pour un [ \<ws2007HttpBinding >](../../../../../docs/framework/configure-apps/file-schema/wcf/ws2007httpbinding.md).|  
  
## <a name="see-also"></a>Voir aussi

- <xref:System.ServiceModel.NonDualMessageSecurityOverHttp>
- <xref:System.ServiceModel.Configuration.WSHttpSecurityElement.Message%2A>
- <xref:System.ServiceModel.WSHttpSecurity.Message%2A>
- <xref:System.ServiceModel.Configuration.NonDualMessageSecurityOverHttpElement>
- [Sécurisation des services et des clients](../../../../../docs/framework/wcf/feature-details/securing-services-and-clients.md)
- [Liaisons](../../../../../docs/framework/wcf/bindings.md)
- [Configuration des liaisons fournies par le système](../../../../../docs/framework/wcf/feature-details/configuring-system-provided-bindings.md)
- [Utilisation de liaisons pour configurer des services et des clients](../../../../../docs/framework/wcf/using-bindings-to-configure-services-and-clients.md)
- [\<binding>](../../../../../docs/framework/misc/binding.md)
