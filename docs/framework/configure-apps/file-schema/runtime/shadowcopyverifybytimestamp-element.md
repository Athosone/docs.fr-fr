---
title: Élément <shadowCopyVerifyByTimestamp>
ms.date: 03/30/2017
helpviewer_keywords:
- <shadowCopyTimeStampVerification> element
- shadowCopyTimeStampVerification element
ms.assetid: 2f1648e5-997b-435e-a4f9-d236c574c66c
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 4ad61b3824b8155cf3f68f61865891c023b4cf32
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59216412"
---
# <a name="shadowcopyverifybytimestamp-element"></a>\<shadowCopyVerifyByTimestamp> Element
Indique si les clichés instantanés utilisent le comportement de démarrage par défaut introduit dans le [!INCLUDE[net_v40_long](../../../../../includes/net-v40-long-md.md)], ou reviennent au comportement de démarrage des versions précédentes du .NET Framework.  
  
 \<configuration > élément  
\<runtime > élément  
\<shadowCopyVerifyByTimestamp> Element  
  
## <a name="syntax"></a>Syntaxe  
  
```xml  
<shadowCopyVerifyByTimestamp enabled="true|false" />  
```  
  
## <a name="attributes-and-elements"></a>Attributs et éléments  
 Les sections suivantes décrivent des attributs, des éléments enfants et des éléments parents.  
  
### <a name="attributes"></a>Attributs  
  
|Attribut|Description|  
|---------------|-----------------|  
|enabled|Attribut requis.<br /><br /> Spécifie si les domaines d’application qui utilisent les clichés instantanés comparer les horodatages d’assembly au démarrage, afin de déterminer si un assembly a été mis à jour avant de l’assembly les clichés instantanés.|  
  
## <a name="enabled-attribute"></a>Attribut enabled  
  
|Value|Description|  
|-----------|-----------------|  
|true|Au démarrage, copie uniquement les assemblys qui ont été mis à jour dans la mesure où ils ont été dernière copiés dans le répertoire des clichés instantanés. Il s’agit par défaut pour le [!INCLUDE[net_v40_short](../../../../../includes/net-v40-short-md.md)].|  
|False|Rétablit le comportement de démarrage des versions antérieures du .NET Framework, qui consiste à copier tous les fichiers au démarrage.|  
  
### <a name="child-elements"></a>Éléments enfants  
 Aucun.  
  
### <a name="parent-elements"></a>Éléments parents  
  
|Élément|Description|  
|-------------|-----------------|  
|`configuration`|Élément racine de chaque fichier de configuration utilisé par le Common Language Runtime et les applications .NET Framework.|  
|`runtime`|Contient des informations sur les liaisons d’assembly et l’opération garbage collection.|  
  
## <a name="remarks"></a>Notes  
 En commençant par le [!INCLUDE[net_v40_short](../../../../../includes/net-v40-short-md.md)], les assemblys sont des clichés instantanés uniquement si leurs horodatages indiquent qu’ils ont été modifiés depuis leur dernière copie dans le répertoire des clichés instantanés. Cela améliore les temps de démarrage pour de nombreuses applications qui utilisent les clichés instantanés, comme décrit dans [clichés instantanés d’assemblys](../../../../../docs/framework/app-domains/shadow-copy-assemblies.md). Les applications qui ont un pourcentage élevé et la fréquence des mises à jour de l’assembly ne sera peut-être pas avantageux à partir de ce changement de comportement. Dans ce cas, vous pouvez utiliser cet élément pour restaurer le comportement des versions antérieures du .NET Framework.  
  
## <a name="example"></a>Exemple  
 L’exemple suivant montre comment désactiver le comportement de démarrage par défaut des clichés instantanés dans le [!INCLUDE[net_v40_short](../../../../../includes/net-v40-short-md.md)]et rétablir le comportement de démarrage des versions antérieures du .NET Framework.  
  
```xml  
<configuration>  
   <runtime>  
      <shadowCopyVerifyByTimestamp enabled="false" />  
   </runtime>  
</configuration>  
```  
  
## <a name="see-also"></a>Voir aussi

- [Schéma des paramètres d’exécution](../../../../../docs/framework/configure-apps/file-schema/runtime/index.md)
- [Schéma des fichiers de configuration](../../../../../docs/framework/configure-apps/file-schema/index.md)
- [Clichés instantanés d'assemblys](../../../../../docs/framework/app-domains/shadow-copy-assemblies.md)
