---
title: 'Procédure : Dessiner une polyligne à l’aide de l’élément Polyline'
ms.date: 03/30/2017
helpviewer_keywords:
- connected lines [WPF]
- polylines [WPF], drawing
- graphics [WPF], polylines
- lines [WPF], connected (see polylines)
- drawing [WPF], polylines
ms.assetid: 65db8935-d047-4295-87c4-b427ff3ad293
ms.openlocfilehash: 4f55ecc206be0ef4947923047e796c36131c70ec
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62003208"
---
# <a name="how-to-draw-a-polyline-by-using-the-polyline-element"></a><span data-ttu-id="2446f-102">Procédure : Dessiner une polyligne à l’aide de l’élément Polyline</span><span class="sxs-lookup"><span data-stu-id="2446f-102">How to: Draw a Polyline by Using the Polyline Element</span></span>
<span data-ttu-id="2446f-103">Cet exemple montre comment dessiner une polyligne, c'est-à-dire une série de lignes connectées, à l’aide de la <xref:System.Windows.Shapes.Polyline> élément.</span><span class="sxs-lookup"><span data-stu-id="2446f-103">This example shows how to draw a polyline, which is a series of connected lines, by using the <xref:System.Windows.Shapes.Polyline> element.</span></span>  
  
 <span data-ttu-id="2446f-104">Pour dessiner une polyligne, créez un <xref:System.Windows.Shapes.Polyline> élément et utiliser ses <xref:System.Windows.Shapes.Polyline.Points%2A> propriété pour spécifier les sommets de la forme.</span><span class="sxs-lookup"><span data-stu-id="2446f-104">To draw a polyline, create a <xref:System.Windows.Shapes.Polyline> element and use its <xref:System.Windows.Shapes.Polyline.Points%2A> property to specify the shape vertices.</span></span> <span data-ttu-id="2446f-105">Enfin, utilisez la <xref:System.Windows.Shapes.Shape.Stroke%2A> et <xref:System.Windows.Shapes.Shape.StrokeThickness%2A> hiérarchique de propriétés pour décrire la polyligne car une ligne sans trait est invisible.</span><span class="sxs-lookup"><span data-stu-id="2446f-105">Finally, use the <xref:System.Windows.Shapes.Shape.Stroke%2A> and <xref:System.Windows.Shapes.Shape.StrokeThickness%2A> properties to describe the polyline outline because a line without a stroke is invisible.</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="2446f-106">Étant donné que le <xref:System.Windows.Shapes.Polyline> élément n’est pas une forme fermée, le <xref:System.Windows.Shapes.Shape.Fill%2A> propriété n’a aucun effet, même si vous fermez délibérément le contour de la forme.</span><span class="sxs-lookup"><span data-stu-id="2446f-106">Because the <xref:System.Windows.Shapes.Polyline> element is not a closed shape, the <xref:System.Windows.Shapes.Shape.Fill%2A> property has no effect, even if you deliberately close the shape outline.</span></span> <span data-ttu-id="2446f-107">Pour créer une forme fermée avec un <xref:System.Windows.Shapes.Shape.Fill%2A>, utilisez un <xref:System.Windows.Shapes.Polygon> élément.</span><span class="sxs-lookup"><span data-stu-id="2446f-107">To create a closed shape with a <xref:System.Windows.Shapes.Shape.Fill%2A>, use a <xref:System.Windows.Shapes.Polygon> element.</span></span>  
  
 <span data-ttu-id="2446f-108">L’exemple suivant dessine deux <xref:System.Windows.Shapes.Polyline> éléments à l’intérieur d’un <xref:System.Windows.Controls.Canvas>.</span><span class="sxs-lookup"><span data-stu-id="2446f-108">The following example draws two <xref:System.Windows.Shapes.Polyline> elements inside a <xref:System.Windows.Controls.Canvas>.</span></span>  
  
## <a name="example"></a><span data-ttu-id="2446f-109">Exemple</span><span class="sxs-lookup"><span data-stu-id="2446f-109">Example</span></span>  
 <span data-ttu-id="2446f-110">Dans [!INCLUDE[TLA#tla_xaml](../../../../includes/tlasharptla-xaml-md.md)], une syntaxe valide pour les points est une liste délimitée par des paires de séparées par des virgules coordonnées x et y.</span><span class="sxs-lookup"><span data-stu-id="2446f-110">In [!INCLUDE[TLA#tla_xaml](../../../../includes/tlasharptla-xaml-md.md)], valid syntax for points is a space-delimited list of comma-separated x- and y-coordinate pairs.</span></span>  
  
 [!code-xaml[drawingwithshapeelements#PolylineExample1](~/samples/snippets/csharp/VS_Snippets_Wpf/DrawingWithShapeElements/CS/polylineexample.xaml#polylineexample1)]  
  
 <span data-ttu-id="2446f-111">Bien que cet exemple utilise un <xref:System.Windows.Controls.Canvas> pour contenir les polylignes, vous pouvez utiliser des éléments polyline (et tous les autres éléments de la forme) avec n’importe quel <xref:System.Windows.Controls.Panel> ou <xref:System.Windows.Controls.Control> qui prend en charge le contenu non textuel.</span><span class="sxs-lookup"><span data-stu-id="2446f-111">Although this example uses a <xref:System.Windows.Controls.Canvas> to contain the polylines, you can use polyline elements (and all the other shape elements) with any <xref:System.Windows.Controls.Panel> or <xref:System.Windows.Controls.Control> that supports non-text content.</span></span>  
  
 <span data-ttu-id="2446f-112">Cet exemple fait partie d’un exemple plus complet ; Pour obtenir un exemple complet, consultez [exemples d’éléments de forme](https://go.microsoft.com/fwlink/?LinkID=160037).</span><span class="sxs-lookup"><span data-stu-id="2446f-112">This example is part of a larger sample; for the complete sample, see [Shape Elements Sample](https://go.microsoft.com/fwlink/?LinkID=160037).</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="2446f-113">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="2446f-113">See also</span></span>

- <xref:System.Windows.Shapes.Polyline>
- <xref:System.Windows.Shapes.Polygon>
- <xref:System.Windows.Shapes.Shape>
- [<span data-ttu-id="2446f-114">Exemples d’éléments de forme</span><span class="sxs-lookup"><span data-stu-id="2446f-114">Shape Elements Sample</span></span>](https://go.microsoft.com/fwlink/?LinkID=160037)
- [<span data-ttu-id="2446f-115">Vue d’ensemble des formes et dessins de base dans WPF</span><span class="sxs-lookup"><span data-stu-id="2446f-115">Shapes and Basic Drawing in WPF Overview</span></span>](shapes-and-basic-drawing-in-wpf-overview.md)
