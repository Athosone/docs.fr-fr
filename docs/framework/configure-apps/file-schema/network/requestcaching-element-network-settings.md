---
title: <requestCaching>, élément (paramètres réseau)
ms.date: 03/30/2017
f1_keywords:
- http://schemas.microsoft.com/.NetConfiguration/v2.0#requestCaching
- http://schemas.microsoft.com/.NetConfiguration/v2.0#configuration/system.net/requestCaching
helpviewer_keywords:
- requestCaching element
- <requestCaching> element
ms.assetid: 9962a2fe-cbda-41a6-9377-571811eaea84
ms.openlocfilehash: af290e4b9258a08425a15e297ff538502edea916
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61674426"
---
# <a name="requestcaching-element-network-settings"></a>\<requestCaching>, élément (paramètres réseau)
Contrôle le mécanisme de mise en cache pour les demandes réseau.  
  
 \<configuration>  
\<system.net>  
\<requestCaching>  
  
## <a name="syntax"></a>Syntaxe  
  
```xml  
<requestCaching  
  isPrivateCache ="true|false"  
  disableAllCaching="true|false"  
  defaultPolicyLevel="BypassCache|Default|CacheOnly|CacheIfAvailable|Revalidate|Reload|NoCacheNoStore|Revalidate"  
  unspecifiedMaximumAge= "d.hh.mm.ss">  
    <defaultHttpCachePolicy>...</defaultHttpCachePolicy>  
    <defaultFtpCachePolicy>...</defaultFtpCachePolicy>  
</requestCaching>
```  
  
## <a name="attributes-and-elements"></a>Attributs et éléments  
 Les sections suivantes décrivent des attributs, des éléments enfants et des éléments parents.  
  
### <a name="attributes"></a>Attributs  
  
|Attribut|Description|  
|---------------|-----------------|  
|`isPrivateCache`|Spécifie si le cache fournit une isolation entre les informations d’utilisateurs différents. La valeur par défaut est `true`. Cette valeur doit être `false` pour les applications de couche intermédiaire.|  
|`disableAllCaching`|Spécifie que la mise en cache est désactivée pour toutes les réponses Web et ne peut pas être substituée par programmation.|  
|`defaultPolicyLevel`|Une des valeurs dans l’énumération <xref:System.Net.Cache.RequestCacheLevel>. La valeur par défaut est `BypassCache`.|  
|`unspecifiedMaximumAge`|Spécifie la durée par défaut après lequel le contenu est marqué comme ayant expiré.|  
  
## <a name="policylevel-attribute"></a>policyLevel attribut  
  
|Value|Description|  
|-----------|-----------------|  
|`Default`|Retourne la ressource mise en cache si la ressource est actualisée, la longueur du contenu est précise, et l’expiration, la modification et attributs de la longueur du contenu sont présents.|  
|`BypassCache`|Retourne la ressource à partir du serveur.|  
|`CacheOnly`|Retourne la ressource mise en cache si la longueur du contenu est présente et qu’il correspond à la taille d’entrée.|  
|`CacheIfAvailable`|Retourne la ressource mise en cache si la longueur du contenu est fournie et correspond à la taille d’entrée ; Sinon, la ressource est téléchargée à partir du serveur et est retournée à l’appelant.|  
|`Revalidate`|Retourne la ressource mise en cache si l’horodatage de la ressource mise en cache est identique à l’horodatage de la ressource sur le serveur ; Sinon, la ressource est téléchargée à partir du serveur, stocké dans le cache et est retournée à l’appelant.|  
|`Reload`|Télécharge la ressource à partir du serveur, il stocke dans le cache et retourne la ressource à l’appelant.|  
|`NoCacheNoStore`|Si une ressource mise en cache existe, elle est supprimée. La ressource est téléchargée à partir du serveur et est retournée à l’appelant.|  
|`Revalidate`|Satisfait une demande à l’aide de la copie mise en cache de la ressource si l’horodatage est le même que l’horodatage de la ressource sur le serveur ; Sinon, la ressource est téléchargée à partir du serveur, présenté à l’appelant et est stockée dans le cache,|  
  
### <a name="child-elements"></a>Éléments enfants  
  
|Élément|Description|  
|-------------|-----------------|  
|[defaultHttpCachePolicy](../../../../../docs/framework/configure-apps/file-schema/network/defaulthttpcachepolicy-element-network-settings.md)|Élément facultatif.<br /><br /> Décrit si la mise en cache HTTP est active et décrit la valeur par défaut, la mise en cache de stratégie.|  
|[\<defaultFtpCachePolicy >, élément (paramètres réseau)](../../../../../docs/framework/configure-apps/file-schema/network/defaultftpcachepolicy-element-network-settings.md)|Élément facultatif.<br /><br /> Décrit si la mise en cache FTP est active et décrit la valeur par défaut, la mise en cache de stratégie.|  
  
### <a name="parent-elements"></a>Éléments parents  
  
|Élément|Description|  
|-------------|-----------------|  
|[system.net](../../../../../docs/framework/configure-apps/file-schema/network/system-net-element-network-settings.md)|Contient des paramètres qui spécifient la manière dont .NET Framework se connecte au réseau.|  
  
## <a name="example"></a>Exemple  
 L’exemple suivant montre comment désactiver toute mise en cache.  
  
```xml  
<configuration>  
  <system.net>  
    <requestCaching  
      disableAllCaching="true"  
    />  
  </system.net>  
</configuration>  
```  
  
## <a name="see-also"></a>Voir aussi

- <xref:System.Net.Cache?displayProperty=nameWithType>
- [Schéma des paramètres réseau](../../../../../docs/framework/configure-apps/file-schema/network/index.md)
