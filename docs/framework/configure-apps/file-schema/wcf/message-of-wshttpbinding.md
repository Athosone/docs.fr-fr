---
title: <message> de <wsHttpBinding>
ms.date: 03/30/2017
ms.assetid: 621abbde-590b-454d-90ac-68dc3c69c720
ms.openlocfilehash: 4d9b46b6c148f9280f6504b9bccdf644ab451c00
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61768894"
---
# <a name="message-of-wshttpbinding"></a>\<message > de \<wsHttpBinding >
Définit les paramètres de sécurité au niveau du message de la [ \<wsHttpBinding >](../../../../../docs/framework/configure-apps/file-schema/wcf/wshttpbinding.md).  
  
 \<system.ServiceModel>  
\<bindings>  
\<wsHttpBinding>  
\<binding>  
\<security>  
\<message>  
  
## <a name="syntax"></a>Syntaxe  
  
```xml  
<message algorithmSuite="Basic128/Basic192/Basic256/Basic128Rsa15/Basic256Rsa15/TripleDes/TripleDesRsa15/Basic128Sha256/Basic192Sha256/TripleDesSha256/Basic128Sha256Rsa15/Basic192Sha256Rsa15/Basic256Sha256Rsa15/TripleDesSha256Rsa15"
         clientCredentialType="Certificate/IssuedToken/None/UserName/Windows"
         establishSecurityContext="Boolean"
         negotiateServiceCredential="Boolean" />
```  
  
## <a name="type"></a>Type  
 <xref:System.ServiceModel.NonDualMessageSecurityOverHttp>  
  
## <a name="attributes-and-elements"></a>Attributs et éléments  
 Les sections suivantes décrivent des attributs, des éléments enfants et des éléments parents.  
  
### <a name="attributes"></a>Attributs  
  
|Attribut|Description|  
|---------------|-----------------|  
|algorithmSuite|Définit les algorithmes de chiffrement de message et de clé de type WRAP. Les algorithmes et les tailles de clé sont déterminés par la classe <xref:System.ServiceModel.Security.SecurityAlgorithmSuite>. Ces algorithmes se mappent à ceux définis dans la spécification Security Policy Language (WS-SecurityPolicy).<br /><br /> La valeur par défaut est `Basic256`.|  
|clientCredentialType|Facultatif. Spécifie le type d'information d'identification à utiliser lorsque l'exécution de l'authentification du client à l'aide du mode de sécurité est `Message` ou `TransportWithMessageCredentials`. Consultez les valeurs d'énumération ci-dessous. La valeur par défaut est `Windows`.<br /><br /> Cet attribut est de type <xref:System.ServiceModel.MessageCredentialType>.|  
|establishSecurityContext|Valeur booléenne qui détermine si le canal de sécurité établit une session sécurisée. Une session sécurisée établit un jeton de contexte de sécurité (SCT) avant d'échanger les messages d'application. Lorsque le jeton SCT est établi, le canal de sécurité offre une interface <xref:System.ServiceModel.Channels.ISession> aux canaux supérieurs. Pour plus d’informations sur l’utilisation des sessions sécurisées, consultez [Comment : Créer une Session sécurisée](../../../../../docs/framework/wcf/feature-details/how-to-create-a-secure-session.md).<br /><br /> La valeur par défaut est `true`.|  
|negotiateServiceCredential|Optionnel. Valeur booléenne qui spécifie si les informations d'identification du service sont configurées auprès du client hors bande ou transférées du service au client via un processus de négociation. Ce type de négociation précède l'échange habituel de messages.<br /><br /> Si le `clientCredentialType` attribut a la valeur None, Username ou Certificate, cet attribut `false` implique que le certificat de service est disponible au niveau du client hors bande et que le client doit spécifier le certificat de service (à l’aide de la [ \<serviceCertificate >](../../../../../docs/framework/configure-apps/file-schema/wcf/servicecertificate-of-servicecredentials.md)) dans le [ \<serviceCredentials >](../../../../../docs/framework/configure-apps/file-schema/wcf/servicecredentials.md) comportement de service. Ce mode est interopérable avec les piles SOAP qui implémentent WS-Trust et WS-SecureConversation.<br /><br /> Si l'attribut `ClientCredentialType` a la valeur `Windows`, l'affectation de la valeur `false` à cet attribut spécifie l'authentification basée sur Kerberos. Cela signifie que le client et le service doivent faire partie du même domaine Kerberos. Ce mode est interopérable avec les piles SOAP qui implémentent le profil de jeton Kerberos (comme défini dans OASIS WSS TC) ainsi que WS-Trust et WS-SecureConversation.<br /><br /> Lorsque cet attribut a la valeur `true`, il entraîne une négociation .NET SOAP qui tunnelle l'échange SPNego par des messages SOAP.<br /><br /> La valeur par défaut est `true`.|  
  
## <a name="algorithmsuite-attribute"></a>Attribut algorithmSuite  
  
|Value|Description|  
|-----------|-----------------|  
|Basic128|Utilisez le chiffrement Basic128, Sha1 pour le condensat du message et Rsa-oaep-mgf1p pour la clé de type WRAP.|  
|Basic192|Utilisez le chiffrement Basic192, Sha1 pour le condensat du message et Rsa-oaep-mgf1p pour la clé de type WRAP.|  
|Basic256|Utilisez le chiffrement Basic256, Sha1 pour le condensat du message et Rsa-oaep-mgf1p pour la clé de type WRAP.|  
|Basic256Rsa15|Utilisez Basic256 pour le chiffrement du message, Sha1 pour le condensat du message et Rsa15 pour la clé de type WRAP.|  
|Basic192Rsa15|Utilisez Basic192 pour le chiffrement du message, Sha1 pour le condensat du message et Rsa15 pour la clé de type WRAP.|  
|TripleDes|Utilisez le chiffrement TripleDes, Sha1 pour le condensat du message et Rsa-oaep-mgf1p pour la clé de type WRAP.|  
|Basic128Rsa15|Utilisez Basic128 pour le chiffrement du message, Sha1 pour le résumé du message et Rsa15 pour la clé de type WRAP.|  
|TripleDesRsa15|Utilisez le chiffrement TripleDes, Sha1 pour le condensat du message et Rsa15 pour la clé de type WRAP.|  
|Basic128Sha256|Utilisez Basic256 pour le chiffrement du message, Sha256 pour le condensat du message et Rsa-oaep-mgf1p pour la clé de type WRAP.|  
|Basic192Sha256|Utilisez Basic192 pour le chiffrement du message, Sha256 pour le résumé du message et Rsa-oaep-mgf1p pour la clé de type WRAP.|  
|Basic256Sha256|Utilisez Basic256 pour le chiffrement du message, Sha256 pour le condensat du message et Rsa-oaep-mgf1p pour la clé de type WRAP.|  
|TripleDesSha256|Utilisez TripleDes pour le chiffrement du message, Sha256 pour le résumé du message et Rsa-oaep-mgf1p pour la clé de type WRAP.|  
|Basic128Sha256Rsa15|Utilisez Basic128 pour le chiffrement du message, Sha256 pour le condensat du message et Rsa15 pour la clé de type WRAP.|  
|Basic192Sha256Rsa15|Utilisez Basic192 pour le chiffrement du message, Sha256 pour le condensat du message et Rsa15 pour la clé de type WRAP.|  
|Basic256Sha256Rsa15|Utilisez Basic256 pour le chiffrement du message, Sha256 pour le condensat du message et Rsa15 pour la clé de type WRAP.|  
|TripleDesSha256Rsa15|Utilisez TripleDes pour le chiffrement du message, Sha256 pour le condensat du message et Rsa15 pour la clé de type WRAP.|  
  
## <a name="clientcredentialtype-attribute"></a>Attribut clientCredentialType  
  
|Value|Description|  
|-----------|-----------------|  
|Aucun.|Permet au service d'interagir avec les clients anonymes. Du côté du service, cela indique que le service ne requiert pas d'informations d'identification du client. Au niveau du client, indique que ce dernier ne fournit pas d'informations d'identification du client.|  
|Certificat|Autorise le service à exiger une authentification du client via un certificat. Si le mode de sécurité du message est utilisé et que l'attribut `negotiateServiceCredential` est définit à `false`, le client doit être configuré avec le certificat de service.|  
|IssuedToken|Spécifie un jeton personnalisé, habituellement publié par un service d'émission de jeton de sécurité.|  
|UserName|Autorise le service à imposer que le client soit authentifié à l'aide d'une information d'identification UserName. WCF ne prend pas en charge l’envoi d’un mot de passe digest ou de dérivation de clés à l’aide du mot de passe et à l’aide de ces clés pour la sécurité de message. Par conséquent, WCF met en œuvre que le transport est sécurisé lors de l’utilisation des informations d’identification UserName. Ce mode d'informations d'identification a pour résultat soit un échange interopérable, soit une négociation non interopérable basée sur l'attribut `negotiateServiceCredential`.|  
|Windows|Permet aux échanges SOAP d'être placés dans le contexte authentifié d'informations d'identification Windows. Si l'attribut `negotiateServiceCredential` a la valeur `true`, cela exécute une négociation SSPI ou Kerberos (norme interopérable).|  
  
### <a name="child-elements"></a>Éléments enfants  
 Aucun.  
  
### <a name="parent-elements"></a>Éléments parents  
  
|Élément|Description|  
|-------------|-----------------|  
|[\<security>](../../../../../docs/framework/configure-apps/file-schema/wcf/security-of-wshttpbinding.md)|Définit les paramètres de sécurité pour un [ \<wsHttpBinding >](../../../../../docs/framework/configure-apps/file-schema/wcf/wshttpbinding.md).|  
  
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
