---
title: Styles et modèles PasswordBox
ms.date: 03/30/2017
helpviewer_keywords:
- styles [WPF], PasswordBox
- templates [WPF], PasswordBox
- ControlTemplate [WPF], PasswordBox
- states [WPF], PasswordBox
- PasswordBox [WPF], styles and templates
- parts [WPF], PasswordBox
ms.assetid: deb52107-959f-4a60-b303-d21a0a933060
ms.openlocfilehash: 7783330dd56ec5b2759e783a6935761eb3587978
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61770641"
---
# <a name="passwordbox-styles-and-templates"></a>Styles et modèles PasswordBox

Cette rubrique décrit les styles et modèles pour la <xref:System.Windows.Controls.PasswordBox> contrôle. Vous pouvez modifier la valeur par défaut <xref:System.Windows.Controls.ControlTemplate> pour donner le contrôle une apparence unique. Pour plus d’informations, consultez [Personnalisation de l’apparence d’un contrôle existant en créant un ControlTemplate](customizing-the-appearance-of-an-existing-control.md).

## <a name="passwordbox-parts"></a>Composants de PasswordBox

Le tableau suivant répertorie les composants nommés pour le <xref:System.Windows.Controls.PasswordBox> contrôle.

|Élément|Type|Description|
|-|-|-|
|PART_ContentHost|<xref:System.Windows.FrameworkElement>|Un élément visuel qui peut contenir un <xref:System.Windows.FrameworkElement>. Le texte de la <xref:System.Windows.Controls.PasswordBox> s’affiche dans cet élément.|

## <a name="passwordbox-states"></a>États de PasswordBox

Le tableau suivant répertorie les états visuels pour le <xref:System.Windows.Controls.PasswordBox> contrôle.

|Nom VisualState|Nom VisualStateGroup|Description|
|-|-|-|
|Normale|CommonStates|État par défaut.|
|MouseOver|CommonStates|Le pointeur de souris est positionné sur le contrôle.|
|Désactivé|CommonStates|Le contrôle est désactivé.|
|Avec focus|FocusStates|Le contrôle a le focus.|
|Sans focus|FocusStates|Le contrôle n’a pas le focus.|
|Valide|ValidationStates|Le contrôle utilise le <xref:System.Windows.Controls.Validation> classe et le <xref:System.Windows.Controls.Validation.HasError%2A?displayProperty=nameWithType> propriété jointe est `false`.|
|InvalidFocused|ValidationStates|Le <xref:System.Windows.Controls.Validation.HasError%2A?displayProperty=nameWithType> propriété jointe est `true` a le contrôle a le focus.|
|InvalidUnfocused|ValidationStates|Le <xref:System.Windows.Controls.Validation.HasError%2A?displayProperty=nameWithType> propriété jointe est `true` a le contrôle n’a pas le focus.|

## <a name="passwordbox-controltemplate-example"></a>Exemple de ControlTemplate PasswordBox

L’exemple suivant montre comment définir un <xref:System.Windows.Controls.ControlTemplate> pour la <xref:System.Windows.Controls.PasswordBox> contrôle.

[!code-xaml[ControlTemplateExamples#PasswordBox](~/samples/snippets/csharp/VS_Snippets_Wpf/ControlTemplateExamples/CS/resources/textbox.xaml#passwordbox)]

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
