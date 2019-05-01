---
title: 'Procédure : Définir un rectangle à l’aide d’un RectangleGeometry'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- graphics [WPF], rectangles
- rectangles [WPF], creating with RectangleGeometry class
ms.assetid: e40b8a8e-54b8-416b-a9f2-be6dca9fdf0b
ms.openlocfilehash: 146ca7017ee38ad5c1065e59662ac441e7bfbfe2
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61965410"
---
# <a name="how-to-define-a-rectangle-using-a-rectanglegeometry"></a><span data-ttu-id="ad4f9-102">Procédure : Définir un rectangle à l’aide d’un RectangleGeometry</span><span class="sxs-lookup"><span data-stu-id="ad4f9-102">How to: Define a Rectangle Using a RectangleGeometry</span></span>
<span data-ttu-id="ad4f9-103">Cet exemple explique comment utiliser le <xref:System.Windows.Media.RectangleGeometry> classe pour décrire un rectangle.</span><span class="sxs-lookup"><span data-stu-id="ad4f9-103">This example describes how to use the <xref:System.Windows.Media.RectangleGeometry> class to describe a rectangle.</span></span>  
  
## <a name="example"></a><span data-ttu-id="ad4f9-104">Exemple</span><span class="sxs-lookup"><span data-stu-id="ad4f9-104">Example</span></span>  
 <span data-ttu-id="ad4f9-105">L’exemple suivant montre comment créer et afficher un <xref:System.Windows.Media.RectangleGeometry>.</span><span class="sxs-lookup"><span data-stu-id="ad4f9-105">The following example shows how to create and render a <xref:System.Windows.Media.RectangleGeometry>.</span></span>  <span data-ttu-id="ad4f9-106">La position relative et les dimensions du rectangle sont définies par un <xref:System.Windows.Rect> structure.</span><span class="sxs-lookup"><span data-stu-id="ad4f9-106">The relative position and the dimensions of the rectangle are defined by a <xref:System.Windows.Rect> structure.</span></span> <span data-ttu-id="ad4f9-107">La position relative est `50,50` et la hauteur et la largeur sont toutes deux `25` création d’un carré.</span><span class="sxs-lookup"><span data-stu-id="ad4f9-107">The relative position is `50,50` and the height and the width are both `25` creating a square.</span></span> <span data-ttu-id="ad4f9-108">L’intérieur du rectangle est peint avec un <xref:System.Windows.Media.Brushes.LemonChiffon%2A> pinceau et son contour est peint avec un <xref:System.Windows.Media.Brushes.Black%2A> trait avec une épaisseur de `1`.</span><span class="sxs-lookup"><span data-stu-id="ad4f9-108">The rectangle's interior is painted with a <xref:System.Windows.Media.Brushes.LemonChiffon%2A> brush and its outline is painted with a <xref:System.Windows.Media.Brushes.Black%2A> stroke with a thickness of `1`.</span></span>  
  
 [!code-xaml[GeometryOverviewSamples_snip#GraphicsMMRectangleGeometryExample](~/samples/snippets/csharp/VS_Snippets_Wpf/GeometryOverviewSamples_snip/CS/GeometryExamples.xaml#graphicsmmrectanglegeometryexample)]  
  
 [!code-csharp[GeometryOverviewSamples_procedural_snip#GraphicsMMRectangleGeometryExample](~/samples/snippets/csharp/VS_Snippets_Wpf/GeometryOverviewSamples_procedural_snip/CSharp/GeometryExamples.cs#graphicsmmrectanglegeometryexample)]
 [!code-vb[GeometryOverviewSamples_procedural_snip#GraphicsMMRectangleGeometryExample](~/samples/snippets/visualbasic/VS_Snippets_Wpf/GeometryOverviewSamples_procedural_snip/visualbasic/geometryexamples.vb#graphicsmmrectanglegeometryexample)]  
  
 <span data-ttu-id="ad4f9-109">![A RectangleGeometry](./media/graphicsmm-rectangle.gif "graphicsmm_rectangle")</span><span class="sxs-lookup"><span data-stu-id="ad4f9-109">![A RectangleGeometry](./media/graphicsmm-rectangle.gif "graphicsmm_rectangle")</span></span>  
<span data-ttu-id="ad4f9-110">RectangleGeometry</span><span class="sxs-lookup"><span data-stu-id="ad4f9-110">RectangleGeometry</span></span>  
  
 <span data-ttu-id="ad4f9-111">Bien que cet exemple utilise un <xref:System.Windows.Shapes.Path> élément à restituer le <xref:System.Windows.Media.RectangleGeometry>, il existe d’autres façons d’utiliser <xref:System.Windows.Media.RectangleGeometry> objets.</span><span class="sxs-lookup"><span data-stu-id="ad4f9-111">Although this example used a <xref:System.Windows.Shapes.Path> element to render the <xref:System.Windows.Media.RectangleGeometry>, there are many other ways to use <xref:System.Windows.Media.RectangleGeometry> objects.</span></span> <span data-ttu-id="ad4f9-112">Par exemple, un <xref:System.Windows.Media.RectangleGeometry> peut être utilisé pour spécifier le <xref:System.Windows.UIElement.Clip%2A> d’un <xref:System.Windows.UIElement> ou le <xref:System.Windows.Media.GeometryDrawing.Geometry%2A> d’un <xref:System.Windows.Media.GeometryDrawing>.</span><span class="sxs-lookup"><span data-stu-id="ad4f9-112">For example, a <xref:System.Windows.Media.RectangleGeometry> can be used to specify the <xref:System.Windows.UIElement.Clip%2A> of a <xref:System.Windows.UIElement> or the <xref:System.Windows.Media.GeometryDrawing.Geometry%2A> of a <xref:System.Windows.Media.GeometryDrawing>.</span></span>  
  
 <span data-ttu-id="ad4f9-113">Autres classes de géométrie simple incluent <xref:System.Windows.Media.LineGeometry> et <xref:System.Windows.Media.EllipseGeometry>.</span><span class="sxs-lookup"><span data-stu-id="ad4f9-113">Other simple geometry classes include <xref:System.Windows.Media.LineGeometry> and <xref:System.Windows.Media.EllipseGeometry>.</span></span> <span data-ttu-id="ad4f9-114">Ces géométries, ainsi que celles qui sont plus complexes, peut également être créés à l’aide un <xref:System.Windows.Media.PathGeometry> ou <xref:System.Windows.Media.StreamGeometry>.</span><span class="sxs-lookup"><span data-stu-id="ad4f9-114">These geometries, as well as more complex ones, can also be created using a <xref:System.Windows.Media.PathGeometry> or <xref:System.Windows.Media.StreamGeometry>.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="ad4f9-115">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ad4f9-115">See also</span></span>

- [<span data-ttu-id="ad4f9-116">Vue d’ensemble de Geometry</span><span class="sxs-lookup"><span data-stu-id="ad4f9-116">Geometry Overview</span></span>](geometry-overview.md)
- [<span data-ttu-id="ad4f9-117">Créer une forme composite</span><span class="sxs-lookup"><span data-stu-id="ad4f9-117">Create a Composite Shape</span></span>](how-to-create-a-composite-shape.md)
- [<span data-ttu-id="ad4f9-118">Créer une forme à l’aide d’un PathGeometry</span><span class="sxs-lookup"><span data-stu-id="ad4f9-118">Create a Shape by Using a PathGeometry</span></span>](how-to-create-a-shape-by-using-a-pathgeometry.md)
