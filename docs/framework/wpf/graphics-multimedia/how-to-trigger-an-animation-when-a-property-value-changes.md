---
title: 'Procédure : Déclencher une animation en cas de modification d’une valeur de propriété'
ms.date: 03/30/2017
helpviewer_keywords:
- animation [WPF], starting when property values change
- triggering animation [WPF]
- Storyboards [WPF], starting when property values change
ms.assetid: 12399c21-0300-4f4f-9e3a-d92d9907e5f5
ms.openlocfilehash: 7e3eecedf7d464eeb8e4f60f2f05fa06d2e23e09
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61769302"
---
# <a name="how-to-trigger-an-animation-when-a-property-value-changes"></a><span data-ttu-id="d8beb-102">Procédure : Déclencher une animation en cas de modification d’une valeur de propriété</span><span class="sxs-lookup"><span data-stu-id="d8beb-102">How to: Trigger an Animation When a Property Value Changes</span></span>
<span data-ttu-id="d8beb-103">Cet exemple montre comment utiliser un <xref:System.Windows.Trigger> pour démarrer un <xref:System.Windows.Media.Animation.Storyboard> quand une valeur de propriété change.</span><span class="sxs-lookup"><span data-stu-id="d8beb-103">This example shows how to use a <xref:System.Windows.Trigger> to start a <xref:System.Windows.Media.Animation.Storyboard> when a property value changes.</span></span> <span data-ttu-id="d8beb-104">Vous pouvez utiliser un <xref:System.Windows.Trigger> à l’intérieur d’un <xref:System.Windows.Style>, <xref:System.Windows.Controls.ControlTemplate>, ou <xref:System.Windows.DataTemplate>.</span><span class="sxs-lookup"><span data-stu-id="d8beb-104">You can use a <xref:System.Windows.Trigger> inside a <xref:System.Windows.Style>, <xref:System.Windows.Controls.ControlTemplate>, or <xref:System.Windows.DataTemplate>.</span></span>  
  
## <a name="example"></a><span data-ttu-id="d8beb-105">Exemple</span><span class="sxs-lookup"><span data-stu-id="d8beb-105">Example</span></span>  
 <span data-ttu-id="d8beb-106">L’exemple suivant utilise un <xref:System.Windows.Trigger> pour animer la <xref:System.Windows.UIElement.Opacity%2A> d’un <xref:System.Windows.Controls.Button> lors de son <xref:System.Windows.UIElement.IsMouseOver%2A> propriété devient `true`.</span><span class="sxs-lookup"><span data-stu-id="d8beb-106">The following example uses a <xref:System.Windows.Trigger> to animate the <xref:System.Windows.UIElement.Opacity%2A> of a <xref:System.Windows.Controls.Button> when its <xref:System.Windows.UIElement.IsMouseOver%2A> property becomes `true`.</span></span>  
  
 [!code-xaml[AnimatePropertyStoryboards#PropertyTriggerExample](~/samples/snippets/xaml/VS_Snippets_Wpf/AnimatePropertyStoryboards/XAML/PropertyTriggerExample.xaml#propertytriggerexample)]  
  
 <span data-ttu-id="d8beb-107">Les animations appliquées par la propriété <xref:System.Windows.Trigger> objets se comportent de façon plus complexe que <xref:System.Windows.EventTrigger> animations ou les animations démarrées à l’aide de <xref:System.Windows.Media.Animation.Storyboard> méthodes.</span><span class="sxs-lookup"><span data-stu-id="d8beb-107">Animations applied by property <xref:System.Windows.Trigger> objects behave in a more complex fashion than <xref:System.Windows.EventTrigger> animations or animations started using <xref:System.Windows.Media.Animation.Storyboard> methods.</span></span>  <span data-ttu-id="d8beb-108">Elles « effectuent un transfert » avec des animations défini par d’autres <xref:System.Windows.Trigger> objets, mais composent avec <xref:System.Windows.EventTrigger> et animations déclenchées à la méthode.</span><span class="sxs-lookup"><span data-stu-id="d8beb-108">They "handoff" with animations defined by other <xref:System.Windows.Trigger> objects, but compose with <xref:System.Windows.EventTrigger> and method-triggered animations.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="d8beb-109">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d8beb-109">See also</span></span>

- <xref:System.Windows.Trigger>
- [<span data-ttu-id="d8beb-110">Vue d’ensemble des techniques d’animation de propriétés</span><span class="sxs-lookup"><span data-stu-id="d8beb-110">Property Animation Techniques Overview</span></span>](property-animation-techniques-overview.md)
- [<span data-ttu-id="d8beb-111">Vue d'ensemble des plans conceptuels</span><span class="sxs-lookup"><span data-stu-id="d8beb-111">Storyboards Overview</span></span>](storyboards-overview.md)
