---
title: 'Procédure : Dessiner un rectangle'
ms.date: 03/30/2017
helpviewer_keywords:
- drawing [WPF], rectangles
- graphics [WPF], rectangles
- rectangles [WPF], drawing
ms.assetid: beeb57ef-fab5-4446-a38a-1588f97b4c2f
ms.openlocfilehash: 261026b994b432565928b38ff1657115ff7cbe4e
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59217352"
---
# <a name="how-to-draw-a-rectangle"></a><span data-ttu-id="ddb46-102">Procédure : Dessiner un rectangle</span><span class="sxs-lookup"><span data-stu-id="ddb46-102">How to: Draw a Rectangle</span></span>
<span data-ttu-id="ddb46-103">Cet exemple montre comment dessiner un rectangle à l’aide de la <xref:System.Windows.Shapes.Rectangle> élément.</span><span class="sxs-lookup"><span data-stu-id="ddb46-103">This example shows how to draw a rectangle by using the <xref:System.Windows.Shapes.Rectangle> element.</span></span>  
  
 <span data-ttu-id="ddb46-104">Pour dessiner un rectangle, créez un <xref:System.Windows.Shapes.Rectangle> élément et spécifiez son <xref:System.Windows.FrameworkElement.Width%2A> et <xref:System.Windows.FrameworkElement.Height%2A>.</span><span class="sxs-lookup"><span data-stu-id="ddb46-104">To draw a rectangle, create a <xref:System.Windows.Shapes.Rectangle> element and specify its <xref:System.Windows.FrameworkElement.Width%2A> and <xref:System.Windows.FrameworkElement.Height%2A>.</span></span> <span data-ttu-id="ddb46-105">Pour peindre l’intérieur du rectangle, définissez son <xref:System.Windows.Shapes.Shape.Fill%2A>.</span><span class="sxs-lookup"><span data-stu-id="ddb46-105">To paint the inside of the rectangle, set its <xref:System.Windows.Shapes.Shape.Fill%2A>.</span></span> <span data-ttu-id="ddb46-106">Pour donner le rectangle à un plan, utilisez son <xref:System.Windows.Shapes.Shape.Stroke%2A> et <xref:System.Windows.Shapes.Shape.StrokeThickness%2A> propriétés.</span><span class="sxs-lookup"><span data-stu-id="ddb46-106">To give the rectangle an outline, use its <xref:System.Windows.Shapes.Shape.Stroke%2A> and <xref:System.Windows.Shapes.Shape.StrokeThickness%2A> properties.</span></span>  
  
 <span data-ttu-id="ddb46-107">Le rectangle de donner des angles arrondis, spécifiez le paramètre facultatif <xref:System.Windows.Shapes.Rectangle.RadiusX%2A> et <xref:System.Windows.Shapes.Rectangle.RadiusY%2A> propriétés.</span><span class="sxs-lookup"><span data-stu-id="ddb46-107">To give the rectangle rounded corners, specify the optional <xref:System.Windows.Shapes.Rectangle.RadiusX%2A> and <xref:System.Windows.Shapes.Rectangle.RadiusY%2A> properties.</span></span> <span data-ttu-id="ddb46-108">Le <xref:System.Windows.Shapes.Rectangle.RadiusX%2A> et <xref:System.Windows.Shapes.Rectangle.RadiusY%2A> propriétés définies les rayons des axes x et y de l’ellipse utilisée pour arrondir les angles du rectangle.</span><span class="sxs-lookup"><span data-stu-id="ddb46-108">The <xref:System.Windows.Shapes.Rectangle.RadiusX%2A> and <xref:System.Windows.Shapes.Rectangle.RadiusY%2A> properties set the x-axis and y-axis radii of the ellipse that is used to round the corners of the rectangle.</span></span>  
  
 <span data-ttu-id="ddb46-109">Dans l’exemple suivant, deux <xref:System.Windows.Shapes.Rectangle> éléments sont dessinés un <xref:System.Windows.Controls.Canvas>.</span><span class="sxs-lookup"><span data-stu-id="ddb46-109">In the following example, two <xref:System.Windows.Shapes.Rectangle> elements are drawn in a <xref:System.Windows.Controls.Canvas>.</span></span> <span data-ttu-id="ddb46-110">Le premier rectangle est un <xref:System.Windows.Media.Brushes.Blue%2A> intérieurs.</span><span class="sxs-lookup"><span data-stu-id="ddb46-110">The first rectangle has a <xref:System.Windows.Media.Brushes.Blue%2A> interior.</span></span> <span data-ttu-id="ddb46-111">Le deuxième rectangle a une <xref:System.Windows.Media.Brushes.Blue%2A> intérieurs, une <xref:System.Windows.Media.Brushes.Black%2A> contour et angles arrondis est utilisée.</span><span class="sxs-lookup"><span data-stu-id="ddb46-111">The second rectangle has a <xref:System.Windows.Media.Brushes.Blue%2A> interior, a <xref:System.Windows.Media.Brushes.Black%2A> outline, and rounded corners.</span></span>  
  
## <a name="example"></a><span data-ttu-id="ddb46-112">Exemple</span><span class="sxs-lookup"><span data-stu-id="ddb46-112">Example</span></span>  
 [!code-xaml[drawingwithshapeelements#Rectangle1](~/samples/snippets/csharp/VS_Snippets_Wpf/DrawingWithShapeElements/CS/rectangleexample.xaml#rectangle1)]  
  
 <span data-ttu-id="ddb46-113">Bien que cet exemple utilise un <xref:System.Windows.Controls.Canvas> pour contenir les rectangles, vous pouvez utiliser des éléments rectangle (et toutes les autres formes) avec n’importe quel <xref:System.Windows.Controls.Panel> ou <xref:System.Windows.Controls.Control> qui prend en charge le contenu non textuel.</span><span class="sxs-lookup"><span data-stu-id="ddb46-113">Although this example uses a <xref:System.Windows.Controls.Canvas> to contain the rectangles, you can use rectangle elements (and all the other shape elements) with any <xref:System.Windows.Controls.Panel> or <xref:System.Windows.Controls.Control> that supports non-text content.</span></span> <span data-ttu-id="ddb46-114">En fait, les rectangles sont particulièrement utiles pour fournir des arrière-plans pour certaines parties de <xref:System.Windows.Controls.Grid> panneaux.</span><span class="sxs-lookup"><span data-stu-id="ddb46-114">In fact, rectangles are particularly useful for providing backgrounds for portions of <xref:System.Windows.Controls.Grid> panels.</span></span> <span data-ttu-id="ddb46-115">Pour obtenir un exemple, consultez le [vue d’ensemble de la Table](../advanced/table-overview.md).</span><span class="sxs-lookup"><span data-stu-id="ddb46-115">For an example, see the [Table Overview](../advanced/table-overview.md).</span></span>  
  
 <span data-ttu-id="ddb46-116">Cet exemple fait partie d’un exemple plus complet ; Pour obtenir un exemple complet, consultez [exemples d’éléments de forme](https://go.microsoft.com/fwlink/?LinkID=160037).</span><span class="sxs-lookup"><span data-stu-id="ddb46-116">This example is part of a larger sample; for the complete sample, see [Shape Elements Sample](https://go.microsoft.com/fwlink/?LinkID=160037).</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="ddb46-117">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ddb46-117">See also</span></span>

- <xref:System.Windows.Shapes.Rectangle>
- [<span data-ttu-id="ddb46-118">Exemples d’éléments de forme</span><span class="sxs-lookup"><span data-stu-id="ddb46-118">Shape Elements Sample</span></span>](https://go.microsoft.com/fwlink/?LinkID=160037)
- [<span data-ttu-id="ddb46-119">Vue d’ensemble des formes et dessins de base dans WPF</span><span class="sxs-lookup"><span data-stu-id="ddb46-119">Shapes and Basic Drawing in WPF Overview</span></span>](shapes-and-basic-drawing-in-wpf-overview.md)
- [<span data-ttu-id="ddb46-120">Vue d’ensemble de Table</span><span class="sxs-lookup"><span data-stu-id="ddb46-120">Table Overview</span></span>](../advanced/table-overview.md)
