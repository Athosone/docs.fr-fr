---
title: <client>
ms.date: 03/30/2017
f1_keywords:
- http://schemas.microsoft.com/.NetConfiguration/v2.0#configuration/system.ServiceModel/client
- http://schemas.microsoft.com/.NetConfiguration/v2.0#client
ms.assetid: bf0f7031-76c8-4e7e-a6c6-9ad9119134be
ms.openlocfilehash: 2e0352efdd5b709984338fe4484b120bddb7d545
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61704295"
---
# <a name="client"></a>\<client>
L'élément `client` définit une liste de points de terminaison auxquels un client peut se connecter.  
  
 \<system.ServiceModel>  
\<client>  
  
## <a name="syntax"></a>Syntaxe  
  
```xml  
<system.serviceModel>
  <client>
    <endpoint>
    </endpoint>
    <metadata>
    </metadata>
  </client>
</system.serviceModel>
```  
  
## <a name="attributes-and-elements"></a>Attributs et éléments  
 Les sections suivantes décrivent des attributs, des éléments enfants et des éléments parents.  
  
### <a name="attributes"></a>Attributs  
 Aucun.  
  
### <a name="child-elements"></a>Éléments enfants  
  
|Élément|Description|  
|-------------|-----------------|  
|[\<endpoint>](../../../../../docs/framework/configure-apps/file-schema/wcf/endpoint-of-client.md)|Contient une collection d'éléments de point de terminaison qui spécifient les points de terminaison auxquels ce client peut se connecter.|  
|[\<metadata>](../../../../../docs/framework/configure-apps/file-schema/wcf/metadata.md)|Contient des paramètres pour le traitement de métadonnées.|  
  
### <a name="parent-elements"></a>Éléments parents  
  
|Élément|Description|  
|-------------|-----------------|  
|[\<system.serviceModel>](../../../../../docs/framework/configure-apps/file-schema/wcf/system-servicemodel.md)|Élément racine de tous les éléments de configuration Windows Communication Foundation (WCF).|  
  
## <a name="remarks"></a>Notes  
 La section `client` définit une liste de points de terminaison auxquels un client peut se connecter. Chaque point de terminaison répertorié dans la section client définit ses propres liaison, comportement et contrat. Il est identifié uniquement par la combinaison des attributs `name` et `contract`. Le code client spécifie le `name` permettant de se connecter à un point de terminaison pour le service que le client implémente. Si l'attribut `name` est omis, le point de terminaison agit comme point de terminaison par défaut pour le contrat qu'il implémente.  
  
 De plus, cette section spécifie également des paramètres pour le traitement des métadonnées.  
  
## <a name="example"></a>Exemple  
  
```xml  
<client>
  <endpoint address="/HelloWorld/"
            bindingConfiguration="usingDefaults"
            name="MyBinding"
            binding="customBinding"
            contract="HelloWorld">
    <addressProperties actingAs="http://www.microsoft.com/TestActor"
                       identityData="BasicReadWrite"
                       identityType="Spn"
                       isAddressPrivate="false">
  </endpoint>
</client>
```  
  
## <a name="see-also"></a>Voir aussi

- <xref:System.ServiceModel.Configuration.ClientSection>
- <xref:System.ServiceModel.Configuration.MetadataElement>
- [Configuration du client WCF](../../../../../docs/framework/wcf/feature-details/client-configuration.md)
- [Clients](../../../../../docs/framework/wcf/feature-details/clients.md)
