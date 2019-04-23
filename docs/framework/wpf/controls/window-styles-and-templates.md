---
title: Styles et modèles Window
ms.date: 03/30/2017
helpviewer_keywords:
- parts [WPF], Window
- templates [WPF], Window
- styles [WPF], Window
- ControlTemplate [WPF], Window
- Window [WPF], styles and templates
- states [WPF], Window
ms.assetid: 2dfdf025-347b-4342-bf28-95206c273f35
ms.openlocfilehash: ebd21829591b8fefe87aeba0b86280f18eff4f06
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59203728"
---
# <a name="window-styles-and-templates"></a><span data-ttu-id="37aa8-102">Styles et modèles Window</span><span class="sxs-lookup"><span data-stu-id="37aa8-102">Window Styles and Templates</span></span>
<span data-ttu-id="37aa8-103">Cette rubrique décrit les styles et modèles pour la <xref:System.Windows.Window> contrôle.</span><span class="sxs-lookup"><span data-stu-id="37aa8-103">This topic describes the styles and templates for the <xref:System.Windows.Window> control.</span></span> <span data-ttu-id="37aa8-104">Vous pouvez modifier la valeur par défaut <xref:System.Windows.Controls.ControlTemplate> pour donner le contrôle une apparence unique.</span><span class="sxs-lookup"><span data-stu-id="37aa8-104">You can modify the default <xref:System.Windows.Controls.ControlTemplate> to give the control a unique appearance.</span></span> <span data-ttu-id="37aa8-105">Pour plus d’informations, consultez [Personnalisation de l’apparence d’un contrôle existant en créant un ControlTemplate](customizing-the-appearance-of-an-existing-control.md).</span><span class="sxs-lookup"><span data-stu-id="37aa8-105">For more information, see [Customizing the Appearance of an Existing Control by Creating a ControlTemplate](customizing-the-appearance-of-an-existing-control.md).</span></span>  
  
## <a name="window-parts"></a><span data-ttu-id="37aa8-106">Parties de la fenêtre</span><span class="sxs-lookup"><span data-stu-id="37aa8-106">Window Parts</span></span>  
 <span data-ttu-id="37aa8-107">Le <xref:System.Windows.Window> contrôle n’a pas de composants nommés.</span><span class="sxs-lookup"><span data-stu-id="37aa8-107">The <xref:System.Windows.Window> control does not have any named parts.</span></span>  
  
## <a name="window-states"></a><span data-ttu-id="37aa8-108">États de la fenêtre</span><span class="sxs-lookup"><span data-stu-id="37aa8-108">Window States</span></span>  
 <span data-ttu-id="37aa8-109">Le tableau suivant répertorie les états visuels pour le <xref:System.Windows.Window> contrôle.</span><span class="sxs-lookup"><span data-stu-id="37aa8-109">The following table lists the visual states for the <xref:System.Windows.Window> control.</span></span>  
  
|<span data-ttu-id="37aa8-110">Nom VisualState</span><span class="sxs-lookup"><span data-stu-id="37aa8-110">VisualState Name</span></span>|<span data-ttu-id="37aa8-111">Nom VisualStateGroup</span><span class="sxs-lookup"><span data-stu-id="37aa8-111">VisualStateGroup Name</span></span>|<span data-ttu-id="37aa8-112">Description</span><span class="sxs-lookup"><span data-stu-id="37aa8-112">Description</span></span>|  
|-|-|-|  
|<span data-ttu-id="37aa8-113">Valide</span><span class="sxs-lookup"><span data-stu-id="37aa8-113">Valid</span></span>|<span data-ttu-id="37aa8-114">ValidationStates</span><span class="sxs-lookup"><span data-stu-id="37aa8-114">ValidationStates</span></span>|<span data-ttu-id="37aa8-115">Le contrôle utilise le <xref:System.Windows.Controls.Validation> classe et le <xref:System.Windows.Controls.Validation.HasError%2A?displayProperty=nameWithType> propriété jointe est `false`.</span><span class="sxs-lookup"><span data-stu-id="37aa8-115">The control uses the <xref:System.Windows.Controls.Validation> class and the <xref:System.Windows.Controls.Validation.HasError%2A?displayProperty=nameWithType> attached property is `false`.</span></span>|  
|<span data-ttu-id="37aa8-116">InvalidFocused</span><span class="sxs-lookup"><span data-stu-id="37aa8-116">InvalidFocused</span></span>|<span data-ttu-id="37aa8-117">ValidationStates</span><span class="sxs-lookup"><span data-stu-id="37aa8-117">ValidationStates</span></span>|<span data-ttu-id="37aa8-118">Le <xref:System.Windows.Controls.Validation.HasError%2A?displayProperty=nameWithType> propriété jointe est `true` a le contrôle a le focus.</span><span class="sxs-lookup"><span data-stu-id="37aa8-118">The <xref:System.Windows.Controls.Validation.HasError%2A?displayProperty=nameWithType> attached property is `true` has the control has focus.</span></span>|  
|<span data-ttu-id="37aa8-119">InvalidUnfocused</span><span class="sxs-lookup"><span data-stu-id="37aa8-119">InvalidUnfocused</span></span>|<span data-ttu-id="37aa8-120">ValidationStates</span><span class="sxs-lookup"><span data-stu-id="37aa8-120">ValidationStates</span></span>|<span data-ttu-id="37aa8-121">Le <xref:System.Windows.Controls.Validation.HasError%2A?displayProperty=nameWithType> propriété jointe est `true` a le contrôle n’a pas le focus.</span><span class="sxs-lookup"><span data-stu-id="37aa8-121">The <xref:System.Windows.Controls.Validation.HasError%2A?displayProperty=nameWithType> attached property is `true` has the control does not have focus.</span></span>|  
  
## <a name="window-controltemplate-example"></a><span data-ttu-id="37aa8-122">Exemple de ControlTemplate de fenêtre</span><span class="sxs-lookup"><span data-stu-id="37aa8-122">Window ControlTemplate Example</span></span>  
 <span data-ttu-id="37aa8-123">L’exemple suivant montre comment définir un <xref:System.Windows.Controls.ControlTemplate> pour la <xref:System.Windows.Window> contrôle.</span><span class="sxs-lookup"><span data-stu-id="37aa8-123">The following example shows how to define a <xref:System.Windows.Controls.ControlTemplate> for the <xref:System.Windows.Window> control.</span></span>  
  
 [!code-xaml[ControlTemplateExamples#Window](~/samples/snippets/csharp/VS_Snippets_Wpf/ControlTemplateExamples/CS/resources/window.xaml#window)]  
  
 <span data-ttu-id="37aa8-124">Le <xref:System.Windows.Controls.ControlTemplate> utilise un ou plusieurs des ressources suivantes.</span><span class="sxs-lookup"><span data-stu-id="37aa8-124">The <xref:System.Windows.Controls.ControlTemplate> uses one or more of the following resources.</span></span>  
  
 [!code-xaml[ControlTemplateExamples#ResizeGrip](~/samples/snippets/csharp/VS_Snippets_Wpf/ControlTemplateExamples/CS/resources/resizegrip.xaml#resizegrip)]  
[!code-xaml[ControlTemplateExamples#Resources](~/samples/snippets/csharp/VS_Snippets_Wpf/ControlTemplateExamples/CS/resources/shared.xaml#resources)]  
  
 <span data-ttu-id="37aa8-125">Pour voir l’exemple complet, consultez [Styling with ControlTemplates Sample](https://github.com/Microsoft/WPF-Samples/tree/master/Styles%20&%20Templates/IntroToStylingAndTemplating) (Exemple de style avec ControlTemplates).</span><span class="sxs-lookup"><span data-stu-id="37aa8-125">For the complete sample, see [Styling with ControlTemplates Sample](https://github.com/Microsoft/WPF-Samples/tree/master/Styles%20&%20Templates/IntroToStylingAndTemplating).</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="37aa8-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="37aa8-126">See also</span></span>

- <xref:System.Windows.FrameworkElement.Style%2A>
- <xref:System.Windows.Controls.ControlTemplate>
- [<span data-ttu-id="37aa8-127">Styles et modèles Control</span><span class="sxs-lookup"><span data-stu-id="37aa8-127">Control Styles and Templates</span></span>](control-styles-and-templates.md)
- [<span data-ttu-id="37aa8-128">Personnalisation des contrôles</span><span class="sxs-lookup"><span data-stu-id="37aa8-128">Control Customization</span></span>](control-customization.md)
- [<span data-ttu-id="37aa8-129">Application d’un style et création de modèles</span><span class="sxs-lookup"><span data-stu-id="37aa8-129">Styling and Templating</span></span>](styling-and-templating.md)
- [<span data-ttu-id="37aa8-130">Personnalisation de l’apparence d’un contrôle existant en créant un ControlTemplate</span><span class="sxs-lookup"><span data-stu-id="37aa8-130">Customizing the Appearance of an Existing Control by Creating a ControlTemplate</span></span>](customizing-the-appearance-of-an-existing-control.md)
