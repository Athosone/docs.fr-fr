---
title: 'Procédure : Créer une courbe de Bézier quadratique'
ms.date: 03/30/2017
helpviewer_keywords:
- Bezier curves [WPF], creating
- quadratic Bezier curves [WPF], creating
- graphics [WPF], quadratic Bezier curves
ms.assetid: cd8fca4a-504e-4fd8-92ea-2969065a6e02
ms.openlocfilehash: a0b2145b4a5bba11186419fe680f2eca41949d6a
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62054560"
---
# <a name="how-to-create-a-quadratic-bezier-curve"></a><span data-ttu-id="8caf9-102">Procédure : Créer une courbe de Bézier quadratique</span><span class="sxs-lookup"><span data-stu-id="8caf9-102">How to: Create a Quadratic Bezier Curve</span></span>
<span data-ttu-id="8caf9-103">Cet exemple montre comment créer une courbe de Bézier quadratique.</span><span class="sxs-lookup"><span data-stu-id="8caf9-103">This example shows how to create a quadratic Bezier curve.</span></span>  <span data-ttu-id="8caf9-104">Pour créer une courbe de Bézier quadratique, utilisez le <xref:System.Windows.Media.PathGeometry>, <xref:System.Windows.Media.PathFigure>, et <xref:System.Windows.Media.QuadraticBezierSegment> classes.</span><span class="sxs-lookup"><span data-stu-id="8caf9-104">To create a quadratic Bezier curve, use the <xref:System.Windows.Media.PathGeometry>, <xref:System.Windows.Media.PathFigure>, and <xref:System.Windows.Media.QuadraticBezierSegment> classes.</span></span>  
  
## <a name="example"></a><span data-ttu-id="8caf9-105">Exemple</span><span class="sxs-lookup"><span data-stu-id="8caf9-105">Example</span></span>  
 <span data-ttu-id="8caf9-106">Dans les exemples suivants, une courbe de Bézier quadratique est dessinée de (10,100) à (300,100).</span><span class="sxs-lookup"><span data-stu-id="8caf9-106">In the following examples, a quadratic Bezier curve is drawn from (10,100) to (300,100).</span></span> <span data-ttu-id="8caf9-107">La courbe a un point de contrôle de (200,200).</span><span class="sxs-lookup"><span data-stu-id="8caf9-107">The curve has a control point of (200,200).</span></span>  
  
 <span data-ttu-id="8caf9-108">[xaml]</span><span class="sxs-lookup"><span data-stu-id="8caf9-108">[xaml]</span></span>  
  
 <span data-ttu-id="8caf9-109">Dans [!INCLUDE[TLA#tla_xaml](../../../../includes/tlasharptla-xaml-md.md)], vous pouvez utiliser la syntaxe d’attribut pour décrire un chemin d’accès.</span><span class="sxs-lookup"><span data-stu-id="8caf9-109">In [!INCLUDE[TLA#tla_xaml](../../../../includes/tlasharptla-xaml-md.md)], you can use attribute syntax to describe a path.</span></span>  
  
 [!code-xaml[GeometrySample#54](~/samples/snippets/csharp/VS_Snippets_Wpf/GeometrySample/CS/geometryattributesyntaxexample.xaml#54)]  
  
 <span data-ttu-id="8caf9-110">[xaml]</span><span class="sxs-lookup"><span data-stu-id="8caf9-110">[xaml]</span></span>  
  
 <span data-ttu-id="8caf9-111">(Notez que cette syntaxe d’attribut crée en fait un <xref:System.Windows.Media.StreamGeometry>, une version légère d’une <xref:System.Windows.Media.PathGeometry>.</span><span class="sxs-lookup"><span data-stu-id="8caf9-111">(Note that this attribute syntax actually creates a <xref:System.Windows.Media.StreamGeometry>, a lighter-weight version of a <xref:System.Windows.Media.PathGeometry>.</span></span> <span data-ttu-id="8caf9-112">(Pour plus d’informations, consultez la page [Syntaxe XAML pour les tracés](path-markup-syntax.md).)</span><span class="sxs-lookup"><span data-stu-id="8caf9-112">For more information, see the [Path Markup Syntax](path-markup-syntax.md) page.)</span></span>  
  
 <span data-ttu-id="8caf9-113">Dans [!INCLUDE[TLA2#tla_xaml](../../../../includes/tla2sharptla-xaml-md.md)], vous pouvez également dessiner une courbe de Bézier quadratique à l’aide de la syntaxe d’élément objet.</span><span class="sxs-lookup"><span data-stu-id="8caf9-113">In [!INCLUDE[TLA2#tla_xaml](../../../../includes/tla2sharptla-xaml-md.md)], you may also draw a quadratic Bezier curve using object element syntax.</span></span> <span data-ttu-id="8caf9-114">L'exemple suivant est équivalent à l’exemple [!INCLUDE[TLA2#tla_xaml](../../../../includes/tla2sharptla-xaml-md.md)] précédent.</span><span class="sxs-lookup"><span data-stu-id="8caf9-114">The following is equivalent to the previous [!INCLUDE[TLA2#tla_xaml](../../../../includes/tla2sharptla-xaml-md.md)] example.</span></span>  
  
 [!code-xaml[GeometrySample#34](~/samples/snippets/csharp/VS_Snippets_Wpf/GeometrySample/CS/pathgeometryexample.xaml#34)]  
  
 <span data-ttu-id="8caf9-115">Cet exemple fait partie d’un exemple plus vaste ; pour l’exemple complet, consultez [Géométries, exemple](https://go.microsoft.com/fwlink/?LinkID=159989).</span><span class="sxs-lookup"><span data-stu-id="8caf9-115">This example is part of larger sample; for the complete sample, see the [Geometries Sample](https://go.microsoft.com/fwlink/?LinkID=159989).</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="8caf9-116">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="8caf9-116">See also</span></span>

- [<span data-ttu-id="8caf9-117">Créer un arc elliptique</span><span class="sxs-lookup"><span data-stu-id="8caf9-117">Create an Elliptical Arc</span></span>](how-to-create-an-elliptical-arc.md)
- [<span data-ttu-id="8caf9-118">Créer une courbe de Bézier cubique</span><span class="sxs-lookup"><span data-stu-id="8caf9-118">Create a Cubic Bezier Curve</span></span>](how-to-create-a-cubic-bezier-curve.md)
