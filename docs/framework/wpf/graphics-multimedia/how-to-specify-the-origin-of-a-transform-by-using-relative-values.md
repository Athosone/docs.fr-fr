---
title: 'Procédure : Spécifier l’origine d’une transformation à l’aide de valeurs relatives'
ms.date: 03/30/2017
helpviewer_keywords:
- origins of Transforms [WPF]
- Transforms [WPF], origins of
- graphics [WPF], origins of Transforms
ms.assetid: f4dbc29d-93c7-41cd-96d8-5cfd8624b470
ms.openlocfilehash: 48b3b0df8dab8516873495a996074eae57ffe00f
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61651126"
---
# <a name="how-to-specify-the-origin-of-a-transform-by-using-relative-values"></a><span data-ttu-id="ba8ae-102">Procédure : Spécifier l’origine d’une transformation à l’aide de valeurs relatives</span><span class="sxs-lookup"><span data-stu-id="ba8ae-102">How to: Specify the Origin of a Transform by Using Relative Values</span></span>
<span data-ttu-id="ba8ae-103">Cet exemple montre comment utiliser des valeurs relatives pour spécifier l’origine d’un <xref:System.Windows.UIElement.RenderTransform%2A> qui est appliqué à un <xref:System.Windows.FrameworkElement>.</span><span class="sxs-lookup"><span data-stu-id="ba8ae-103">This example shows how to use relative values to specify the origin of a <xref:System.Windows.UIElement.RenderTransform%2A> that is applied to a <xref:System.Windows.FrameworkElement>.</span></span>  
  
 <span data-ttu-id="ba8ae-104">Lorsque vous faites pivoter, mettre à l’échelle ou incliner un <xref:System.Windows.FrameworkElement> à l’aide de la <xref:System.Windows.UIElement.RenderTransform%2A> propriété, le paramètre par défaut applique la transformation à l’angle supérieur gauche de l’élément.</span><span class="sxs-lookup"><span data-stu-id="ba8ae-104">When you rotate, scale, or skew a <xref:System.Windows.FrameworkElement> by using the <xref:System.Windows.UIElement.RenderTransform%2A> property, the default setting applies the transform to the upper-left corner of the element.</span></span> <span data-ttu-id="ba8ae-105">Si vous souhaitez effectuer un pivotement, une mise à l’échelle ou une inclinaison à partir du centre de l’élément, vous pouvez compenser en définissant le centre de la transformation sur le centre de l’élément.</span><span class="sxs-lookup"><span data-stu-id="ba8ae-105">If you want to rotate, scale, or skew from the center of the element, you can compensate by setting the center of the transform to the center of the element.</span></span> <span data-ttu-id="ba8ae-106">Cette solution suppose toutefois de connaître la taille de l’élément.</span><span class="sxs-lookup"><span data-stu-id="ba8ae-106">However, that solution requires that you know the size of the element.</span></span> <span data-ttu-id="ba8ae-107">Un moyen plus simple d’appliquer une transformation au centre d’un élément consiste à définir son <xref:System.Windows.UIElement.RenderTransformOrigin%2A> propriété à (0,5, 0,5), au lieu de définir une valeur de centre sur la transformation elle-même.</span><span class="sxs-lookup"><span data-stu-id="ba8ae-107">An easier way of applying a transform to the center of an element is to set its <xref:System.Windows.UIElement.RenderTransformOrigin%2A> property to (0.5, 0.5), instead of setting a center value on the transform itself.</span></span>  
  
## <a name="example"></a><span data-ttu-id="ba8ae-108">Exemple</span><span class="sxs-lookup"><span data-stu-id="ba8ae-108">Example</span></span>  
 <span data-ttu-id="ba8ae-109">L’exemple suivant utilise un <xref:System.Windows.Media.RotateTransform> pour faire pivoter un <xref:System.Windows.Controls.Button> 45 degrés dans le sens horaire.</span><span class="sxs-lookup"><span data-stu-id="ba8ae-109">The following example uses a <xref:System.Windows.Media.RotateTransform> to rotate a <xref:System.Windows.Controls.Button> 45 degrees clockwise.</span></span> <span data-ttu-id="ba8ae-110">L’exemple ne spécifie pas de centre, donc le bouton pivote autour du point (0, 0), qui se trouve dans le coin supérieur gauche.</span><span class="sxs-lookup"><span data-stu-id="ba8ae-110">Because the example does not specify a center, the button rotates about the point (0, 0), which is its upper-left corner.</span></span> <span data-ttu-id="ba8ae-111">Le <xref:System.Windows.Media.RotateTransform> est appliqué à la <xref:System.Windows.UIElement.RenderTransform%2A> propriété.</span><span class="sxs-lookup"><span data-stu-id="ba8ae-111">The <xref:System.Windows.Media.RotateTransform> is applied to the <xref:System.Windows.UIElement.RenderTransform%2A> property.</span></span>  
  
 <span data-ttu-id="ba8ae-112">L’illustration suivante montre le résultat de la transformation pour l’exemple qui suit.</span><span class="sxs-lookup"><span data-stu-id="ba8ae-112">The following illustration shows the transformation result for the example that follows.</span></span>  
  
 <span data-ttu-id="ba8ae-113">![Bouton transformé à l’aide de RenderTransform](./media/graphicsmm-rendertransformwithdefaultcenter.png "graphicsmm_RenderTransformWithDefaultCenter")</span><span class="sxs-lookup"><span data-stu-id="ba8ae-113">![A button transformed using RenderTransform](./media/graphicsmm-rendertransformwithdefaultcenter.png "graphicsmm_RenderTransformWithDefaultCenter")</span></span>  
<span data-ttu-id="ba8ae-114">Rotation de 45 degrés dans le sens des aiguilles d’une montre à l’aide de la propriété RenderTransform</span><span class="sxs-lookup"><span data-stu-id="ba8ae-114">A 45 degree clockwise rotation by using the RenderTransform property</span></span>  
  
 [!code-xaml[Transforms_snip#GraphicsMMRotateButtonExample1](~/samples/snippets/csharp/VS_Snippets_Wpf/Transforms_snip/CS/ButtonRotateTransformExample.xaml#graphicsmmrotatebuttonexample1)]  
  
 <span data-ttu-id="ba8ae-115">L’exemple suivant utilise également un <xref:System.Windows.Media.RotateTransform> pour faire pivoter un <xref:System.Windows.Controls.Button> 45 degrés dans le sens horaire ; Toutefois, cet exemple définit le <xref:System.Windows.UIElement.RenderTransformOrigin%2A> du bouton à (0,5, 0,5).</span><span class="sxs-lookup"><span data-stu-id="ba8ae-115">The following example also uses a <xref:System.Windows.Media.RotateTransform> to rotate a <xref:System.Windows.Controls.Button> 45 degrees clockwise; however, this example sets the <xref:System.Windows.UIElement.RenderTransformOrigin%2A> of the button to (0.5, 0.5).</span></span> <span data-ttu-id="ba8ae-116">Par conséquent, la rotation est appliquée au centre du bouton et non sur son coin supérieur gauche.</span><span class="sxs-lookup"><span data-stu-id="ba8ae-116">As a result, the rotation is applied to the center of the button instead of to the upper-left corner.</span></span>  
  
 <span data-ttu-id="ba8ae-117">L’illustration suivante montre le résultat de la transformation pour l’exemple qui suit.</span><span class="sxs-lookup"><span data-stu-id="ba8ae-117">The following illustration shows the transformation result for the example that follows.</span></span>  
  
 <span data-ttu-id="ba8ae-118">![Bouton transformé autour de son centre](./media/graphicsmm-rendertransformrelativecenter.png "graphicsmm_RenderTransformRelativeCenter")</span><span class="sxs-lookup"><span data-stu-id="ba8ae-118">![A button transformed about its center](./media/graphicsmm-rendertransformrelativecenter.png "graphicsmm_RenderTransformRelativeCenter")</span></span>  
<span data-ttu-id="ba8ae-119">Rotation de 45 degrés à l’aide de la propriété RenderTransform avec un RenderTransformOrigin de (0,5, 0,5)</span><span class="sxs-lookup"><span data-stu-id="ba8ae-119">A 45 degree rotation by using the RenderTransform property with a RenderTransformOrigin of (0.5, 0.5)</span></span>  
  
 [!code-xaml[Transforms_snip#GraphicsMMRotateButtonExample2](~/samples/snippets/csharp/VS_Snippets_Wpf/Transforms_snip/CS/ButtonRotateTransformExample.xaml#graphicsmmrotatebuttonexample2)]  
  
 <span data-ttu-id="ba8ae-120">Pour plus d’informations sur la transformation <xref:System.Windows.FrameworkElement> , voir la [transforme la vue d’ensemble](transforms-overview.md).</span><span class="sxs-lookup"><span data-stu-id="ba8ae-120">For more information about transforming <xref:System.Windows.FrameworkElement> objects, see the [Transforms Overview](transforms-overview.md).</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="ba8ae-121">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ba8ae-121">See also</span></span>

- <xref:System.Windows.Media.Transform>
- [<span data-ttu-id="ba8ae-122">Vue d’ensemble des transformations</span><span class="sxs-lookup"><span data-stu-id="ba8ae-122">Transforms Overview</span></span>](transforms-overview.md)
- [<span data-ttu-id="ba8ae-123">Rubriques de guide pratique</span><span class="sxs-lookup"><span data-stu-id="ba8ae-123">How-to Topics</span></span>](transformations-how-to-topics.md)
