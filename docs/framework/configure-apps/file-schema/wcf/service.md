---
title: <service>
ms.date: 03/30/2017
ms.assetid: 13123dd6-c4a9-4a04-a984-df184b851788
ms.openlocfilehash: 68bddc01b02d9885b3f0fc4c2cbc5c3249de03f4
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59197956"
---
# <a name="service"></a>\<service>
L'élément `service` contient les paramètres d'un service Windows Communication Foundation (WCF). Il contient également les points de terminaison qui exposent le service.  
  
 \<system.ServiceModel>  
\<services>  
\<service>  
  
## <a name="syntax"></a>Syntaxe  
  
```xml  
<service behaviorConfiguration="String"
         name="String">
</service>
```  
  
## <a name="attributes-and-elements"></a>Attributs et éléments  
 Les sections suivantes décrivent des attributs, des éléments enfants et des éléments parents.  
  
### <a name="attributes"></a>Attributs  
  
|Attribut|Description|  
|---------------|-----------------|  
|behaviorConfiguration|Chaîne qui contient le nom du comportement à utiliser pour instancier le service. Le nom du comportement doit être dans la portée, au niveau où le service est défini. La valeur par défaut est une chaîne vide.|  
|name|Attribut de chaîne requis indiquant le type de service à instancier. Ce paramètre doit correspondre à un type valide. Le format doit être `Namespace.Class.`|  
  
### <a name="child-elements"></a>Éléments enfants  
  
|Élément|Description|  
|-------------|-----------------|  
|[\<endpoint>](../../../../../docs/framework/configure-apps/file-schema/wcf/endpoint-element.md)|Collection d’éléments `endpoint` qui exposent ce service.|  
|[\<host>](../../../../../docs/framework/configure-apps/file-schema/wcf/host.md)|Spécifie l'hôte de cette instance de service. Cet élément est de type <xref:System.ServiceModel.Configuration.HostElement>.|  
  
### <a name="parent-elements"></a>Éléments parents  
  
|Élément|Description|  
|-------------|-----------------|  
|[\<services>](../../../../../docs/framework/configure-apps/file-schema/wcf/services.md)|Élément racine de tous les éléments de configuration WCF.|  
  
## <a name="remarks"></a>Notes  
 Les services sont définis dans la section `services` du fichier de configuration. Un assembly peut contenir n'importe quel nombre de services. Chacun dispose de sa propre section de configuration de `service`. Cette section et son contenu définissent le contrat de service, le comportement et les points de terminaison de ce service en particulier.  
  
 L'élément `behaviorConfiguration` est également facultatif. Il identifie le comportement que le service adopte. Le comportement spécifié dans cet attribut doit créer une liaison avec un comportement dans la portée du même fichier de configuration.  
  
 Chaque service expose un ou plusieurs points de terminaison, qui ont leurs propres adresse et liaison. Toutes les liaisons utilisées dans le fichier de configuration doivent être définies dans l'étendue du fichier. La liaison est liée aux points de terminaison grâce à la combinaison des attributs `name` et `bindingConfiguration`. L'attribut `name` décrit la section dans laquelle la liaison est définie. L'attribut `bindingConfiguration` définit quelle configuration de la section de liaison est utilisée. Une section de liaison peut définir plusieurs configurations.  
  
## <a name="example"></a>Exemple  
 Il s'agit d'un exemple de configuration de service.  
  
```xml  
<service behaviorConfiguration="testChannelBehavior"
         name="HelloWorld">
  <endpoint address="/HelloWorld2/"
            name="test"
            bindingNamespace="http://www.cohowinery.com/"
            binding="basicHttpBinding"
            contract="IHelloWorld" />
</service>
```  
  
## <a name="see-also"></a>Voir aussi

- <xref:System.ServiceModel.Configuration.ServiceElement>
- [Configuration des services](../../../../../docs/framework/wcf/configuring-services.md)
