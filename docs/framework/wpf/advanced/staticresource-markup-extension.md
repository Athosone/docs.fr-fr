---
title: StaticResource, extension de balisage
ms.date: 03/30/2017
f1_keywords:
- StaticResource
- StaticResourceExtension
helpviewer_keywords:
- XAML [WPF], StaticResource markup extension
- StaticResource markup extensions [WPF]
ms.assetid: 97af044c-71f1-4617-9a94-9064b68185d2
ms.openlocfilehash: 8319e451268152e95326c02027157db72df631b8
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61981901"
---
# <a name="staticresource-markup-extension"></a>StaticResource, extension de balisage
Fournit une valeur pour tout [!INCLUDE[TLA2#tla_xaml](../../../../includes/tla2sharptla-xaml-md.md)] attribut de propriété en recherchant une référence à une ressource déjà définie. Comportement de recherche pour cette ressource est analogue à la recherche au moment du chargement, ce qui va rechercher les ressources qui ont été précédemment chargées à partir du balisage de l’actuel [!INCLUDE[TLA2#tla_xaml](../../../../includes/tla2sharptla-xaml-md.md)] page ainsi que d’autres sources d’application et générera cette valeur de ressource en tant que le valeur de propriété dans les objets d’exécution.  
  
## <a name="xaml-attribute-usage"></a>Utilisation d'attributs XAML  
  
```xml  
<object property="{StaticResource key}" .../>  
```  
  
## <a name="xaml-object-element-usage"></a>Utilisation d'éléments objet XAML  
  
```xml  
<object>  
  <object.property>  
<StaticResource ResourceKey="key" .../>  
  </object.property>  
</object>  
```  
  
## <a name="xaml-values"></a>Valeurs XAML  
  
|||  
|-|-|  
|`key`|Clé pour la ressource demandée. Cette clé a été initialement affectée par le [Directive x : Key](../../xaml-services/x-key-directive.md) si une ressource a été créée dans le balisage ou a été fournie comme le `key` paramètre lors de l’appel <xref:System.Windows.ResourceDictionary.Add%2A?displayProperty=nameWithType> si la ressource a été créée dans le code.|  
  
## <a name="remarks"></a>Notes  
  
> [!IMPORTANT]
>  Un `StaticResource` ne devez pas tenter de créer une référence vers l’avant à une ressource qui est définie lexical dans le [!INCLUDE[TLA2#tla_xaml](../../../../includes/tla2sharptla-xaml-md.md)] fichier. Toute tentative n’est pas pris en charge, et même si une telle référence n’échoue pas, une tentative de référence vers l’avant entraînera une altération des performances charge temps lorsque les tables de hachage interne représentant un <xref:System.Windows.ResourceDictionary> sont recherchés. Pour de meilleurs résultats, ajustez la composition de vos dictionnaires de ressources de manière à éviter les références vers l’avant. Si vous ne pouvez pas éviter une référence vers l’avant, utilisez [Extension de balisage DynamicResource](dynamicresource-markup-extension.md) à la place.  
  
 Spécifié <xref:System.Windows.StaticResourceExtension.ResourceKey%2A> doit correspondre à une ressource existante, identifiée par un [Directive x : Key](../../xaml-services/x-key-directive.md) à un certain niveau dans votre page, application, thèmes de contrôle disponibles et ressources externes ou ressources système. La recherche de ressource se produit dans cet ordre. Pour plus d’informations sur le comportement de recherche de ressources pour les ressources statiques et dynamiques, consultez [XAML ressources](xaml-resources.md).  
  
 Une clé de ressource peut être n’importe quelle chaîne définie dans le [XamlName, grammaire](../../xaml-services/xamlname-grammar.md). Une clé de ressource peut être également les autres types d’objets, comme un <xref:System.Type>. Un <xref:System.Type> clé est essentielle à la façon dont styles peuvent leur être par des thèmes, via une clé de style implicite. Pour plus d’informations, consultez [Vue d’ensemble de la création de contrôles](../controls/control-authoring-overview.md).  
  
 L’autre moyen déclaratif de référencement d’une ressource est comme un [Extension de balisage DynamicResource](dynamicresource-markup-extension.md).  
  
 La syntaxe d’attribut est la syntaxe la plus couramment utilisée avec cette extension de balisage. Le jeton de chaîne fourni après la chaîne d’identificateur `StaticResource` est assigné en tant que valeur <xref:System.Windows.StaticResourceExtension.ResourceKey%2A> de la classe d’extension <xref:System.Windows.StaticResourceExtension> sous-jacente.  
  
 `StaticResource` peut être utilisé dans la syntaxe d’élément objet. Dans ce cas, en spécifiant la valeur de la <xref:System.Windows.StaticResourceExtension.ResourceKey%2A> propriété est requise.  
  
 `StaticResource` peut également être utilisé dans une utilisation d'attributs en clair qui spécifie la propriété <xref:System.Windows.StaticResourceExtension.ResourceKey%2A> en tant que paire propriété=valeur :  
  
```xml  
<object property="{StaticResource ResourceKey=key}" .../>  
```  
  
 L'utilisation en clair est souvent utile pour les extensions qui comportent plusieurs propriétés définissables ou si certaines propriétés sont facultatives. `StaticResource` ne comportant qu'une seule propriété définissable (obligatoire), cette utilisation en clair n'est pas classique.  
  
 Dans le [!INCLUDE[TLA2#tla_winclient](../../../../includes/tla2sharptla-winclient-md.md)] [!INCLUDE[TLA2#tla_xaml](../../../../includes/tla2sharptla-xaml-md.md)] implémentation du processeur, la gestion de cette extension de balisage est définie par le <xref:System.Windows.StaticResourceExtension> classe.  
  
 `StaticResource` est une extension de balisage. Les extensions de balisage sont généralement implémentées pour éviter que les valeurs d’attribut ne soient autre chose que des valeurs littérales ou des noms de gestionnaire et lorsque l’exigence dépasse le cadre de la définition de convertisseurs de type sur certains types ou propriétés. Toutes les extensions de balisage [!INCLUDE[TLA2#tla_xaml](../../../../includes/tla2sharptla-xaml-md.md)] utilisent les caractères { et } dans leur syntaxe d’attribut, convention selon laquelle un processeur [!INCLUDE[TLA2#tla_xaml](../../../../includes/tla2sharptla-xaml-md.md)] reconnaît qu’une extension de balisage doit traiter l’attribut. Pour plus d’informations, consultez [Extensions de balisage et XAML WPF](markup-extensions-and-wpf-xaml.md).  
  
## <a name="see-also"></a>Voir aussi

- [Application d’un style et création de modèles](../controls/styling-and-templating.md)
- [Vue d’ensemble du langage XAML (WPF)](xaml-overview-wpf.md)
- [Extensions de balisage et XAML WPF](markup-extensions-and-wpf-xaml.md)
- [Ressources XAML](xaml-resources.md)
- [Ressources et code](resources-and-code.md)
