---
title: <security> de <peerTransport>
ms.date: 03/30/2017
ms.assetid: f73634ed-f896-4968-bf74-5e5ac52d3b6b
ms.openlocfilehash: 1aff79bf5867a3a1ebe05e3f812475dac4b413e9
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61670493"
---
# <a name="security-of-peertransport"></a>\<sécurité > de \<peerTransport >
Contient les paramètres de sécurité associés à un canal homologue, y compris le type d'authentification utilisé et la sécurité utilisée pour le transport de messages.  
  
 \<system.serviceModel>  
\<bindings>  
\<customBinding>  
\<binding>  
\<peerTransport>  
\<security>  
  
## <a name="syntax"></a>Syntaxe  
  
```xml  
<security mode="None/Transport/Message/TransportWithMessageCredential">
  <transport clientCredentialType="None/Windows/UserName/Certificate/CardSpace" />
</security
```  
  
## <a name="attributes-and-elements"></a>Attributs et éléments  
 Les sections suivantes décrivent des attributs, des éléments enfants et des éléments parents.  
  
### <a name="attributes"></a>Attributs  
  
|Attribut|Description|  
|---------------|-----------------|  
|`mode`|Spécifie le type de sécurité à appliquer. La valeur par défaut est Message. Cet attribut est de type <xref:System.ServiceModel.SecurityMode>.|  
  
## <a name="mode-attribute"></a>Attribut Mode  
  
|Value|Description|  
|-----------|-----------------|  
|`None`|La sécurité est désactivée.|  
|`Transport`|La sécurité est fournie à l'aide de HTTPS.|  
|`Message`|La sécurité SOAP assure l'authentification, l'intégrité et la confidentialité.|  
|`TransportWithMessageCredential`|Le protocole HTTPS assure l'authentification et la confidentialité. Les messages SOAP fournissent des types d'informations d'identification enrichies.|  
  
### <a name="child-elements"></a>Éléments enfants  
  
|Élément|Description|  
|-------------|-----------------|  
|[\<transport>](../../../../../docs/framework/configure-apps/file-schema/wcf/transport-of-peertransport.md)|Définit un transport d’homologue pour une liaison personnalisée. Cet élément dispose d'un attribut `clientCredentialType` qui spécifie les informations d'identification à utiliser lors de l'interaction avec un service. Cet attribut est de type <xref:System.ServiceModel.PeerTransportCredentialType>.<br /><br /> Cet élément est de type <xref:System.ServiceModel.Configuration.PeerTransportSecurityElement>.|  
  
### <a name="parent-elements"></a>Éléments parents  
  
|Élément|Description|  
|-------------|-----------------|  
|[\<peerTransport>](../../../../../docs/framework/configure-apps/file-schema/wcf/peertransport.md)|Définit un transport d’homologue pour une liaison personnalisée.|  
  
## <a name="see-also"></a>Voir aussi

- <xref:System.ServiceModel.Configuration.PeerSecurityElement>
- <xref:System.ServiceModel.PeerSecuritySettings>
- <xref:System.ServiceModel.Channels.CustomBinding>
- [Sécurité de transport](../../../../../docs/framework/wcf/feature-details/transport-security.md)
- [Transports](../../../../../docs/framework/wcf/feature-details/transports.md)
- [Choix d’un transport](../../../../../docs/framework/wcf/feature-details/choosing-a-transport.md)
- [Liaisons](../../../../../docs/framework/wcf/bindings.md)
- [Extension de liaisons](../../../../../docs/framework/wcf/extending/extending-bindings.md)
- [Liaisons personnalisées](../../../../../docs/framework/wcf/extending/custom-bindings.md)
- [\<customBinding>](../../../../../docs/framework/configure-apps/file-schema/wcf/custombinding.md)
