---
title: 'Procédure : Animer un objet sur un tracé (animation de point)'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- animation [WPF], objects along paths (point animation)
- point animation [WPF]
ms.assetid: 1fa3f817-35bc-41a1-b366-f5a20b70da0c
ms.openlocfilehash: 4ef28118975d02500916676ca50e0f9622c7a3e2
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61651452"
---
# <a name="how-to-animate-an-object-along-a-path-point-animation"></a><span data-ttu-id="b0339-102">Procédure : Animer un objet sur un tracé (animation de point)</span><span class="sxs-lookup"><span data-stu-id="b0339-102">How to: Animate an Object Along a Path (Point Animation)</span></span>
<span data-ttu-id="b0339-103">Cet exemple montre comment utiliser un <xref:System.Windows.Media.Animation.PointAnimationUsingPath> objet à animer un <xref:System.Windows.Point> sur un tracé courbé.</span><span class="sxs-lookup"><span data-stu-id="b0339-103">This example shows how to use a <xref:System.Windows.Media.Animation.PointAnimationUsingPath> object to animate a <xref:System.Windows.Point> along a curved path.</span></span>  
  
## <a name="example"></a><span data-ttu-id="b0339-104">Exemple</span><span class="sxs-lookup"><span data-stu-id="b0339-104">Example</span></span>  
 <span data-ttu-id="b0339-105">L’exemple suivant déplace un <xref:System.Windows.Media.EllipseGeometry> sur un tracé défini par un <xref:System.Windows.Media.PathGeometry>.</span><span class="sxs-lookup"><span data-stu-id="b0339-105">The following example moves an <xref:System.Windows.Media.EllipseGeometry> along a path defined by a <xref:System.Windows.Media.PathGeometry>.</span></span> <span data-ttu-id="b0339-106">La géométrie d’ellipse <xref:System.Windows.Media.EllipseGeometry.Center%2A> propriété, qui prend un <xref:System.Windows.Point> valeur, spécifie sa position ; pour déplacer la géométrie d’ellipse, vous animer sa <xref:System.Windows.Media.EllipseGeometry.Center%2A> propriété.</span><span class="sxs-lookup"><span data-stu-id="b0339-106">The ellipse geometry's <xref:System.Windows.Media.EllipseGeometry.Center%2A> property, which takes a <xref:System.Windows.Point> value, specifies its position; to move the ellipse geometry, you animate its <xref:System.Windows.Media.EllipseGeometry.Center%2A> property.</span></span> <span data-ttu-id="b0339-107">L’exemple utilise un <xref:System.Windows.Media.Animation.PointAnimationUsingPath> pour animer la <xref:System.Windows.Media.EllipseGeometry> l’objet <xref:System.Windows.Media.EllipseGeometry.Center%2A> propriété.</span><span class="sxs-lookup"><span data-stu-id="b0339-107">The example uses a <xref:System.Windows.Media.Animation.PointAnimationUsingPath> to animate the <xref:System.Windows.Media.EllipseGeometry> object's <xref:System.Windows.Media.EllipseGeometry.Center%2A> property.</span></span>  
  
 [!code-xaml[PathAnimationGallery_snippet#PointAnimationUsingPathWholePage](~/samples/snippets/csharp/VS_Snippets_Wpf/PathAnimationGallery_snippet/CS/pointanimationusingpathexample.xaml#pointanimationusingpathwholepage)]  
  
 [!code-csharp[PathAnimationGallery_procedural_snip#PointAnimationUsingPathWholePage](~/samples/snippets/csharp/VS_Snippets_Wpf/PathAnimationGallery_procedural_snip/CSharp/PointAnimationUsingPathExample.cs#pointanimationusingpathwholepage)]
 [!code-vb[PathAnimationGallery_procedural_snip#PointAnimationUsingPathWholePage](~/samples/snippets/visualbasic/VS_Snippets_Wpf/PathAnimationGallery_procedural_snip/VisualBasic/PointAnimationUsingPathExample.vb#pointanimationusingpathwholepage)]  
  
 <span data-ttu-id="b0339-108">Pour obtenir un exemple complet, consultez [Animation de tracés, exemple](https://go.microsoft.com/fwlink/?LinkID=160028).</span><span class="sxs-lookup"><span data-stu-id="b0339-108">For the complete sample, see [Path Animation Sample](https://go.microsoft.com/fwlink/?LinkID=160028).</span></span>  
  
 <span data-ttu-id="b0339-109">La version du code de l’exemple précédent utilisé un <xref:System.Windows.Media.Animation.Storyboard> pour animer la <xref:System.Windows.Media.EllipseGeometry>, bien qu’une seule animation ait été appliquée.</span><span class="sxs-lookup"><span data-stu-id="b0339-109">The code version of the preceding sample used a <xref:System.Windows.Media.Animation.Storyboard> to animate the <xref:System.Windows.Media.EllipseGeometry>, even though only one animation was applied.</span></span> <span data-ttu-id="b0339-110">Un <xref:System.Windows.Media.Animation.Storyboard> est souvent le moyen le plus simple d’appliquer plusieurs animations, car ces animations peuvent être contrôlées par le même <xref:System.Windows.Media.Animation.Storyboard>.</span><span class="sxs-lookup"><span data-stu-id="b0339-110">A <xref:System.Windows.Media.Animation.Storyboard> is often the easiest way to apply multiple animations because these animations can be controlled by the same <xref:System.Windows.Media.Animation.Storyboard>.</span></span> <span data-ttu-id="b0339-111">Toutefois, un moyen plus simple pour appliquer une seule animation à une propriété lors de l’utilisation de code consiste à utiliser le <xref:System.Windows.Media.Animation.Animatable.BeginAnimation%2A> (méthode).</span><span class="sxs-lookup"><span data-stu-id="b0339-111">However, an easier way to apply a single animation to a property when using code is to use the <xref:System.Windows.Media.Animation.Animatable.BeginAnimation%2A> method.</span></span> <span data-ttu-id="b0339-112">Si vous voulez voir un exemple, consultez l’article [Comment : animer une propriété sans utiliser de storyboard](how-to-animate-a-property-without-using-a-storyboard.md).</span><span class="sxs-lookup"><span data-stu-id="b0339-112">For an example, see [Animate a Property Without Using a Storyboard](how-to-animate-a-property-without-using-a-storyboard.md).</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="b0339-113">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b0339-113">See also</span></span>

- [<span data-ttu-id="b0339-114">Animation de tracés, exemple</span><span class="sxs-lookup"><span data-stu-id="b0339-114">Path Animation Sample</span></span>](https://go.microsoft.com/fwlink/?LinkID=160028)
- [<span data-ttu-id="b0339-115">Vue d’ensemble de l’animation</span><span class="sxs-lookup"><span data-stu-id="b0339-115">Animation Overview</span></span>](animation-overview.md)
- [<span data-ttu-id="b0339-116">Guides pratiques relatifs aux animations de tracés</span><span class="sxs-lookup"><span data-stu-id="b0339-116">Path Animation How-to Topics</span></span>](path-animation-how-to-topics.md)
