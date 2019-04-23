---
title: Élément <CompatSortNLSVersion>
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- <CompatSortNLSVersion> element
- CompatSortNLSVersion element
ms.assetid: 782cc82e-83f7-404a-80b7-6d3061a8b6e3
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: dfd241056947fbf1daf48b84ff41e3f74ff7b8de
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59195772"
---
# <a name="compatsortnlsversion-element"></a>\<CompatSortNLSVersion > élément
Spécifie que le runtime doit utiliser des ordres de tri hérités lors de l'exécution de comparaisons de chaînes.  
  
 \<configuration>  
\<runtime>  
\<CompatSortNLSVersion > élément  
  
## <a name="syntax"></a>Syntaxe  
  
```xml  
<CompatSortNLSVersion    
   enabled="4096"/>  
```  
  
## <a name="attributes-and-elements"></a>Attributs et éléments  
 Les sections suivantes décrivent des attributs, des éléments enfants et des éléments parents.  
  
### <a name="attributes"></a>Attributs  
  
|Attribut|Description|  
|---------------|-----------------|  
|`enabled`|Attribut requis.<br /><br /> Spécifie l'ID de paramètres régionaux dont l'ordre de tri doit être utilisé.|  
  
## <a name="enabled-attribute"></a>Attribut enabled  
  
|Value|Description|  
|-----------|-----------------|  
|4096|ID de paramètres régionaux qui représente un ordre de tri secondaire. Dans ce cas, 4096 représente l'ordre de tri de [!INCLUDE[net_v35_short](../../../../../includes/net-v35-short-md.md)] et versions antérieures.|  
  
### <a name="child-elements"></a>Éléments enfants  
 Aucun.  
  
### <a name="parent-elements"></a>Éléments parents  
  
|Élément|Description|  
|-------------|-----------------|  
|`configuration`|Élément racine de chaque fichier de configuration utilisé par le Common Language Runtime et les applications .NET Framework.|  
|`runtime`|Contient des informations sur les options d'initialisation du runtime.|  
  
## <a name="remarks"></a>Notes  
 Étant donné que la comparaison de chaînes, le tri et les opérations de casse effectuaient par le <xref:System.Globalization.CompareInfo?displayProperty=nameWithType> classe dans le [!INCLUDE[net_v40_short](../../../../../includes/net-v40-short-md.md)] est conforme à la norme Unicode 5.1, les résultats de méthodes de comparaison de chaînes telles que <xref:System.String.Compare%28System.String%2CSystem.String%29?displayProperty=nameWithType> et <xref:System.String.LastIndexOf%28System.String%29?displayProperty=nameWithType> peut différer de versions précédentes du .NET Framework. Si votre application dépend d'un comportement hérité, vous pouvez restaurer la comparaison de chaînes et les règles de tri utilisées dans [!INCLUDE[net_v35_short](../../../../../includes/net-v35-short-md.md)] et versions antérieures en incluant l'élément `<CompatSortNLSVersion>` dans le fichier de configuration de l'application.  
  
> [!IMPORTANT]
>  La restauration de la comparaison de chaînes héritées et des règles de tri requiert également que la bibliothèque de liens dynamiques sort00001000.dll soit disponible sur le système local.  
  
 Vous pouvez également utiliser des règles de tri et de comparaison de chaîne héritées dans un domaine d'application spécifique en passant la chaîne « NetFx40_Legacy20SortingBehavior » à la méthode <xref:System.AppDomainSetup.SetCompatibilitySwitches%2A> lorsque vous créez le domaine d'application.  
  
## <a name="example"></a>Exemple  
 L'exemple suivant instancie deux objets <xref:System.String> et appelle la méthode <xref:System.String.Compare%28System.String%2CSystem.String%2CSystem.StringComparison%29?displayProperty=nameWithType> pour les comparer en utilisant les conventions de la culture actuelle.  
  
 [!code-csharp[String.BreakingChanges#1](../../../../../samples/snippets/csharp/VS_Snippets_CLR/string.breakingchanges/cs/example1.cs#1)]
 [!code-vb[String.BreakingChanges#1](../../../../../samples/snippets/visualbasic/VS_Snippets_CLR/string.breakingchanges/vb/example1.vb#1)]  
  
 Lorsque vous exécutez l'exemple sur [!INCLUDE[net_v40_short](../../../../../includes/net-v40-short-md.md)], la sortie suivante s'affiche.  
  
```  
sta follows a in the sort order.  
```  
  
 Cela est complètement différent de la sortie qui s'affiche lorsque vous exécutez l'exemple sur [!INCLUDE[net_v35_short](../../../../../includes/net-v35-short-md.md)].  
  
```  
sta equals a in the sort order.  
```  
  
 Toutefois, si vous ajoutez le fichier de configuration suivant au répertoire de l'exemple, puis exécutez l'exemple sur [!INCLUDE[net_v40_short](../../../../../includes/net-v40-short-md.md)], la sortie est identique à celle produite par l'exemple lorsqu'il est exécuté sur [!INCLUDE[net_v35_short](../../../../../includes/net-v35-short-md.md)].  
  
```xml  
<?xml version ="1.0"?>  
<configuration>  
   <runtime>  
      <CompatSortNLSVersion enabled="4096"/>  
   </runtime>  
</configuration>  
```  
  
## <a name="see-also"></a>Voir aussi

- [Schéma des paramètres d’exécution](../../../../../docs/framework/configure-apps/file-schema/runtime/index.md)
- [Schéma des fichiers de configuration](../../../../../docs/framework/configure-apps/file-schema/index.md)
