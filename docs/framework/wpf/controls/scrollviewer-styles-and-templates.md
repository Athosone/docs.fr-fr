---
title: Styles et modèles ScrollViewer
ms.date: 03/30/2017
helpviewer_keywords:
- parts [WPF], ScrollViewer
- states [WPF], ScrollViewer
- styles [WPF], ScrollViewer
- templates [WPF], ScrollViewer
- ControlTemplate [WPF], ScrollViewer
- ScrollViewer [WPF], styles and templates
ms.assetid: dffdd822-ae69-4946-abaf-710860cd65b2
ms.openlocfilehash: 9c0edfd7ab4772eb9a1f5ecdd3db611fa36bf8d3
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61971026"
---
# <a name="scrollviewer-styles-and-templates"></a>Styles et modèles ScrollViewer
Cette rubrique décrit les styles et modèles pour la <xref:System.Windows.Controls.ScrollViewer> contrôle. Vous pouvez modifier la valeur par défaut <xref:System.Windows.Controls.ControlTemplate> pour donner le contrôle une apparence unique. Pour plus d’informations, consultez [Personnalisation de l’apparence d’un contrôle existant en créant un ControlTemplate](customizing-the-appearance-of-an-existing-control.md).  
  
## <a name="scrollviewer-parts"></a>Composants de ScrollViewer  
 Le tableau suivant répertorie les composants nommés pour le <xref:System.Windows.Controls.ScrollViewer> contrôle.  
  
|Élément|Type|Description|  
|-|-|-|  
|PART_ScrollContentPresenter|<xref:System.Windows.Controls.ScrollContentPresenter>|L’espace réservé pour le contenu dans le <xref:System.Windows.Controls.ScrollViewer>.|  
|PART_HorizontalScrollBar|<xref:System.Windows.Controls.Primitives.ScrollBar>|Le <xref:System.Windows.Controls.Primitives.ScrollBar> utilisé pour faire défiler le contenu horizontalement.|  
|PART_VerticalScrollBar|<xref:System.Windows.Controls.Primitives.ScrollBar>|Le <xref:System.Windows.Controls.Primitives.ScrollBar> utilisé pour faire défiler le contenu verticalement.|  
  
## <a name="scrollviewer-states"></a>États de ScrollViewer  
 Le tableau suivant répertorie les états visuels pour le <xref:System.Windows.Controls.ScrollViewer> contrôle.  
  
|Nom VisualState|Nom VisualStateGroup|Description|  
|-|-|-|  
|Valide|ValidationStates|Le contrôle utilise le <xref:System.Windows.Controls.Validation> classe et le <xref:System.Windows.Controls.Validation.HasError%2A?displayProperty=nameWithType> propriété jointe est `false`.|  
|InvalidFocused|ValidationStates|Le <xref:System.Windows.Controls.Validation.HasError%2A?displayProperty=nameWithType> propriété jointe est `true` a le contrôle a le focus.|  
|InvalidUnfocused|ValidationStates|Le <xref:System.Windows.Controls.Validation.HasError%2A?displayProperty=nameWithType> propriété jointe est `true` a le contrôle n’a pas le focus.|  
  
## <a name="scrollviewer-controltemplate-example"></a>Exemple de ControlTemplate de ScrollViewer  
 L’exemple suivant montre comment définir un <xref:System.Windows.Controls.ControlTemplate> pour la <xref:System.Windows.Controls.ScrollViewer> contrôle.  
  
 [!code-xaml[ControlTemplateExamples#ScrollViewer](~/samples/snippets/csharp/VS_Snippets_Wpf/ControlTemplateExamples/CS/resources/scrollviewer.xaml#scrollviewer)]  
  
 L’exemple précédent utilise une ou plusieurs des ressources suivantes.  
  
 [!code-xaml[ControlTemplateExamples#Resources](~/samples/snippets/csharp/VS_Snippets_Wpf/ControlTemplateExamples/CS/resources/shared.xaml#resources)]  
  
 Pour voir l’exemple complet, consultez [Styling with ControlTemplates Sample](https://github.com/Microsoft/WPF-Samples/tree/master/Styles%20&%20Templates/IntroToStylingAndTemplating) (Exemple de style avec ControlTemplates).  
  
## <a name="see-also"></a>Voir aussi

- <xref:System.Windows.FrameworkElement.Style%2A>
- <xref:System.Windows.Controls.ControlTemplate>
- [Styles et modèles Control](control-styles-and-templates.md)
- [Personnalisation des contrôles](control-customization.md)
- [Application d’un style et création de modèles](styling-and-templating.md)
- [Personnalisation de l’apparence d’un contrôle existant en créant un ControlTemplate](customizing-the-appearance-of-an-existing-control.md)
