---
title: <bypasslist>, élément (paramètres réseau)
ms.date: 03/30/2017
f1_keywords:
- http://schemas.microsoft.com/.NetConfiguration/v2.0#bypasslist
- http://schemas.microsoft.com/.NetConfiguration/v2.0#configuration/system.net/defaultProxy/bypasslist
helpviewer_keywords:
- bypasslist element
- <bypasslist> element
ms.assetid: 124446b7-abb1-4e5e-a492-b64398f268f1
ms.openlocfilehash: d3d986dae478f49504dae21b9f39574b7887b4d2
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61674621"
---
# <a name="bypasslist-element-network-settings"></a>\<BypassList >, élément (paramètres réseau)
Fournit un ensemble d’expressions régulières décrivant les adresses qui n’utilisent pas un proxy.  
  
 \<configuration>  
\<system.net>  
\<defaultProxy>  
\<bypasslist>  
  
## <a name="syntax"></a>Syntaxe  
  
```xml  
<bypasslist>   
</bypasslist>  
```  
  
## <a name="attributes-and-elements"></a>Attributs et éléments  
 Les sections suivantes décrivent des attributs, des éléments enfants et des éléments parents.  
  
### <a name="attributes"></a>Attributs  
 Aucun.  
  
### <a name="child-elements"></a>Éléments enfants  
  
|**Élément**|**Description**|  
|-----------------|---------------------|  
|[add](../../../../../docs/framework/configure-apps/file-schema/network/add-element-for-bypasslist-network-settings.md)|Ajoute une adresse IP ou le nom DNS à la liste de contournement proxy.|  
|[clear](../../../../../docs/framework/configure-apps/file-schema/network/clear-element-for-bypasslist-network-settings.md)|Efface la liste de contournement.|  
|[remove](../../../../../docs/framework/configure-apps/file-schema/network/remove-element-for-bypasslist-network-settings.md)|Supprime une adresse IP ou le nom DNS de la liste de contournement proxy.|  
  
### <a name="parent-elements"></a>Éléments parents  
  
|**Élément**|**Description**|  
|-----------------|---------------------|  
|[defaultProxy](../../../../../docs/framework/configure-apps/file-schema/network/defaultproxy-element-network-settings.md)|Configure le serveur proxy HTTP (Hypertext Transfer Protocol).|  
  
## <a name="remarks"></a>Notes  
 La liste de contournement contient des expressions régulières qui décrivent les URI qui <xref:System.Net.WebRequest> instances accéder directement au lieu de via le serveur proxy.  
  
 Soyez prudent lorsque vous spécifiez une expression régulière pour cet élément. L’expression régulière « [a-z] +\\.contoso\\.com » correspond à tout hôte dans le domaine contoso.com, mais il correspond également à n’importe quel hôte dans le domaine contoso.com.cpandl.com. Pour faire correspondre uniquement sur un ordinateur hôte dans le domaine contoso.com, utilisez une ancre (« $») : « [a-z] +\\.contoso\\.com$ ».  
  
 Pour plus d’informations sur les expressions régulières, consultez. [Expressions régulières .NET framework](../../../../../docs/standard/base-types/regular-expressions.md).  
  
## <a name="configuration-files"></a>Fichiers de configuration  
 Cet élément peut être défini dans le fichier de configuration de l'application ou dans le fichier de configuration de l'ordinateur (Machine.config).  
  
## <a name="example"></a>Exemple  
 L’exemple suivant ajoute deux adresses à la liste de contournement. La première contourne le proxy pour tous les serveurs dans le domaine contoso.com ; la deuxième contourne le proxy pour tous les serveurs dont les adresses IP commencent par 192.168.  
  
```xml  
<configuration>  
  <system.net>  
    <defaultProxy>  
      <bypasslist>  
        <add address="[a-z]+\.contoso\.com$" />  
        <add address="192\.168\.\d{1,3}\.\d{1,3}" />  
      </bypasslist>  
    </defaultProxy>  
  </system.net>  
</configuration>  
```  
  
## <a name="see-also"></a>Voir aussi

- <xref:System.Net.WebProxy?displayProperty=nameWithType>
- [Schéma des paramètres réseau](../../../../../docs/framework/configure-apps/file-schema/network/index.md)
