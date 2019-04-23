---
title: Styles et modèles GroupBox
ms.date: 03/30/2017
helpviewer_keywords:
- ControlTemplate [WPF], GroupBox
- parts [WPF], GroupBox
- GroupBox [WPF], styles and templates
- states [WPF], GroupBox
- styles [WPF], GroupBox
- templates [WPF], GroupBox
ms.assetid: 33df7037-0a1b-476f-b9d0-41566a777699
ms.openlocfilehash: 5ef8e4b44bc2b6072fa730f33c10191b64954f7c
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59078991"
---
# <a name="groupbox-styles-and-templates"></a><span data-ttu-id="1bfc9-102">Styles et modèles GroupBox</span><span class="sxs-lookup"><span data-stu-id="1bfc9-102">GroupBox Styles and Templates</span></span>
<a name="introduction"></a> <span data-ttu-id="1bfc9-103">Cette rubrique décrit les styles et modèles pour la <xref:System.Windows.Controls.GroupBox> contrôle.</span><span class="sxs-lookup"><span data-stu-id="1bfc9-103">This topic describes the styles and templates for the <xref:System.Windows.Controls.GroupBox> control.</span></span> <span data-ttu-id="1bfc9-104">Vous pouvez modifier la valeur par défaut <xref:System.Windows.Controls.ControlTemplate> pour donner le contrôle une apparence unique.</span><span class="sxs-lookup"><span data-stu-id="1bfc9-104">You can modify the default <xref:System.Windows.Controls.ControlTemplate> to give the control a unique appearance.</span></span> <span data-ttu-id="1bfc9-105">Pour plus d’informations, consultez [Personnalisation de l’apparence d’un contrôle existant en créant un ControlTemplate](customizing-the-appearance-of-an-existing-control.md).</span><span class="sxs-lookup"><span data-stu-id="1bfc9-105">For more information, see [Customizing the Appearance of an Existing Control by Creating a ControlTemplate](customizing-the-appearance-of-an-existing-control.md).</span></span>  
  
<a name="groupbox_parts"></a>   
## <a name="groupbox-parts"></a><span data-ttu-id="1bfc9-106">Parties de la zone de groupe</span><span class="sxs-lookup"><span data-stu-id="1bfc9-106">GroupBox Parts</span></span>  
 <span data-ttu-id="1bfc9-107">Le <xref:System.Windows.Controls.GroupBox> contrôle n’a pas de composants nommés.</span><span class="sxs-lookup"><span data-stu-id="1bfc9-107">The <xref:System.Windows.Controls.GroupBox> control does not have any named parts.</span></span>  
  
<a name="groupbox_states"></a>   
## <a name="groupbox-states"></a><span data-ttu-id="1bfc9-108">États de GroupBox</span><span class="sxs-lookup"><span data-stu-id="1bfc9-108">GroupBox States</span></span>  
 <span data-ttu-id="1bfc9-109">Le tableau suivant répertorie les états visuels pour le <xref:System.Windows.Controls.GroupBox> contrôle.</span><span class="sxs-lookup"><span data-stu-id="1bfc9-109">The following table lists the visual states for the <xref:System.Windows.Controls.GroupBox> control.</span></span>  
  
|<span data-ttu-id="1bfc9-110">Nom VisualState</span><span class="sxs-lookup"><span data-stu-id="1bfc9-110">VisualState Name</span></span>|<span data-ttu-id="1bfc9-111">Nom VisualStateGroup</span><span class="sxs-lookup"><span data-stu-id="1bfc9-111">VisualStateGroup Name</span></span>|<span data-ttu-id="1bfc9-112">Description</span><span class="sxs-lookup"><span data-stu-id="1bfc9-112">Description</span></span>|  
|-|-|-|  
|<span data-ttu-id="1bfc9-113">Valide</span><span class="sxs-lookup"><span data-stu-id="1bfc9-113">Valid</span></span>|<span data-ttu-id="1bfc9-114">ValidationStates</span><span class="sxs-lookup"><span data-stu-id="1bfc9-114">ValidationStates</span></span>|<span data-ttu-id="1bfc9-115">Le contrôle utilise le <xref:System.Windows.Controls.Validation> classe et le <xref:System.Windows.Controls.Validation.HasError%2A?displayProperty=nameWithType> propriété jointe est `false`.</span><span class="sxs-lookup"><span data-stu-id="1bfc9-115">The control uses the <xref:System.Windows.Controls.Validation> class and the <xref:System.Windows.Controls.Validation.HasError%2A?displayProperty=nameWithType> attached property is `false`.</span></span>|  
|<span data-ttu-id="1bfc9-116">InvalidFocused</span><span class="sxs-lookup"><span data-stu-id="1bfc9-116">InvalidFocused</span></span>|<span data-ttu-id="1bfc9-117">ValidationStates</span><span class="sxs-lookup"><span data-stu-id="1bfc9-117">ValidationStates</span></span>|<span data-ttu-id="1bfc9-118">Le <xref:System.Windows.Controls.Validation.HasError%2A?displayProperty=nameWithType> propriété jointe est `true` a le contrôle a le focus.</span><span class="sxs-lookup"><span data-stu-id="1bfc9-118">The <xref:System.Windows.Controls.Validation.HasError%2A?displayProperty=nameWithType> attached property is `true` has the control has focus.</span></span>|  
|<span data-ttu-id="1bfc9-119">InvalidUnfocused</span><span class="sxs-lookup"><span data-stu-id="1bfc9-119">InvalidUnfocused</span></span>|<span data-ttu-id="1bfc9-120">ValidationStates</span><span class="sxs-lookup"><span data-stu-id="1bfc9-120">ValidationStates</span></span>|<span data-ttu-id="1bfc9-121">Le <xref:System.Windows.Controls.Validation.HasError%2A?displayProperty=nameWithType> propriété jointe est `true` a le contrôle n’a pas le focus.</span><span class="sxs-lookup"><span data-stu-id="1bfc9-121">The <xref:System.Windows.Controls.Validation.HasError%2A?displayProperty=nameWithType> attached property is `true` has the control does not have focus.</span></span>|  
  
<a name="groupbox_controltemplate_example"></a>   
## <a name="groupbox-controltemplate-example"></a><span data-ttu-id="1bfc9-122">Exemple de ControlTemplate GroupBox</span><span class="sxs-lookup"><span data-stu-id="1bfc9-122">GroupBox ControlTemplate Example</span></span>  
 <span data-ttu-id="1bfc9-123">L’exemple suivant montre comment définir un <xref:System.Windows.Controls.ControlTemplate> pour la <xref:System.Windows.Controls.GroupBox> contrôle.</span><span class="sxs-lookup"><span data-stu-id="1bfc9-123">The following example shows how to define a <xref:System.Windows.Controls.ControlTemplate> for the <xref:System.Windows.Controls.GroupBox> control.</span></span>  
  
 [!code-xaml[ControlTemplateExamples#GroupBox](~/samples/snippets/csharp/VS_Snippets_Wpf/ControlTemplateExamples/CS/resources/groupbox.xaml#groupbox)]  
  
 <span data-ttu-id="1bfc9-124">Le <xref:System.Windows.Controls.ControlTemplate> utilise un ou plusieurs des ressources suivantes.</span><span class="sxs-lookup"><span data-stu-id="1bfc9-124">The <xref:System.Windows.Controls.ControlTemplate> uses one or more of the following resources.</span></span>  
  
 [!code-xaml[ControlTemplateExamples#Resources](~/samples/snippets/csharp/VS_Snippets_Wpf/ControlTemplateExamples/CS/resources/shared.xaml#resources)]  
  
 <span data-ttu-id="1bfc9-125">Pour voir l’exemple complet, consultez [Styling with ControlTemplates Sample](https://github.com/Microsoft/WPF-Samples/tree/master/Styles%20&%20Templates/IntroToStylingAndTemplating) (Exemple de style avec ControlTemplates).</span><span class="sxs-lookup"><span data-stu-id="1bfc9-125">For the complete sample, see [Styling with ControlTemplates Sample](https://github.com/Microsoft/WPF-Samples/tree/master/Styles%20&%20Templates/IntroToStylingAndTemplating).</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="1bfc9-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1bfc9-126">See also</span></span>

- <xref:System.Windows.FrameworkElement.Style%2A>
- <xref:System.Windows.Controls.ControlTemplate>
- [<span data-ttu-id="1bfc9-127">Styles et modèles Control</span><span class="sxs-lookup"><span data-stu-id="1bfc9-127">Control Styles and Templates</span></span>](control-styles-and-templates.md)
- [<span data-ttu-id="1bfc9-128">Personnalisation des contrôles</span><span class="sxs-lookup"><span data-stu-id="1bfc9-128">Control Customization</span></span>](control-customization.md)
- [<span data-ttu-id="1bfc9-129">Application d’un style et création de modèles</span><span class="sxs-lookup"><span data-stu-id="1bfc9-129">Styling and Templating</span></span>](styling-and-templating.md)
- [<span data-ttu-id="1bfc9-130">Personnalisation de l’apparence d’un contrôle existant en créant un ControlTemplate</span><span class="sxs-lookup"><span data-stu-id="1bfc9-130">Customizing the Appearance of an Existing Control by Creating a ControlTemplate</span></span>](customizing-the-appearance-of-an-existing-control.md)
