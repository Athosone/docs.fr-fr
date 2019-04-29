---
title: Courbes ouvertes et fermées dans GDI+
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- curves [Windows Forms], filling
- GDI+, curves
- curves [Windows Forms], drawing
- curves
ms.assetid: 08d2cc9a-dc9d-4eed-bcbb-2c8e2ca5d3ae
ms.openlocfilehash: 33a8954296a7e63637ad5e210fb30fba1a3fdd53
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61641467"
---
# <a name="open-and-closed-curves-in-gdi"></a><span data-ttu-id="7c6c0-102">Courbes ouvertes et fermées dans GDI+</span><span class="sxs-lookup"><span data-stu-id="7c6c0-102">Open and Closed Curves in GDI+</span></span>
<span data-ttu-id="7c6c0-103">L’illustration suivante montre deux courbes : un seul est ouvert et l’autre fermée.</span><span class="sxs-lookup"><span data-stu-id="7c6c0-103">The following illustration shows two curves: one open and one closed.</span></span>  
  
 <span data-ttu-id="7c6c0-104">![Courbes ouvertes et fermées](./media/aboutgdip02-art24.gif "Aboutgdip02_art24")</span><span class="sxs-lookup"><span data-stu-id="7c6c0-104">![Open & Closed curves](./media/aboutgdip02-art24.gif "Aboutgdip02_art24")</span></span>  
  
## <a name="managed-interface-for-curves"></a><span data-ttu-id="7c6c0-105">Interface managée pour les courbes</span><span class="sxs-lookup"><span data-stu-id="7c6c0-105">Managed Interface for Curves</span></span>  
 <span data-ttu-id="7c6c0-106">Courbes fermées ont un intérieur et qui peuvent être remplis avec un pinceau.</span><span class="sxs-lookup"><span data-stu-id="7c6c0-106">Closed curves have an interior and therefore can be filled with a brush.</span></span> <span data-ttu-id="7c6c0-107">Le <xref:System.Drawing.Graphics> classe [!INCLUDE[ndptecgdiplus](../../../../includes/ndptecgdiplus-md.md)] fournit les méthodes suivantes pour remplir des formes fermées et courbes : <xref:System.Drawing.Graphics.FillRectangle%2A>, <xref:System.Drawing.Graphics.FillEllipse%2A>, <xref:System.Drawing.Graphics.FillPie%2A>, <xref:System.Drawing.Graphics.FillPolygon%2A>, <xref:System.Drawing.Graphics.FillClosedCurve%2A>, <xref:System.Drawing.Graphics.FillPath%2A>, et <xref:System.Drawing.Graphics.FillRegion%2A>.</span><span class="sxs-lookup"><span data-stu-id="7c6c0-107">The <xref:System.Drawing.Graphics> class in [!INCLUDE[ndptecgdiplus](../../../../includes/ndptecgdiplus-md.md)] provides the following methods for filling closed shapes and curves: <xref:System.Drawing.Graphics.FillRectangle%2A>, <xref:System.Drawing.Graphics.FillEllipse%2A>, <xref:System.Drawing.Graphics.FillPie%2A>, <xref:System.Drawing.Graphics.FillPolygon%2A>, <xref:System.Drawing.Graphics.FillClosedCurve%2A>, <xref:System.Drawing.Graphics.FillPath%2A>, and <xref:System.Drawing.Graphics.FillRegion%2A>.</span></span> <span data-ttu-id="7c6c0-108">Chaque fois que vous appelez une de ces méthodes, vous devez passer un des types de pinceau spécifique (<xref:System.Drawing.SolidBrush>, <xref:System.Drawing.Drawing2D.HatchBrush>, <xref:System.Drawing.TextureBrush>, <xref:System.Drawing.Drawing2D.LinearGradientBrush>, ou <xref:System.Drawing.Drawing2D.PathGradientBrush>) en tant qu’argument.</span><span class="sxs-lookup"><span data-stu-id="7c6c0-108">Whenever you call one of these methods, you must pass one of the specific brush types (<xref:System.Drawing.SolidBrush>, <xref:System.Drawing.Drawing2D.HatchBrush>, <xref:System.Drawing.TextureBrush>, <xref:System.Drawing.Drawing2D.LinearGradientBrush>, or <xref:System.Drawing.Drawing2D.PathGradientBrush>) as an argument.</span></span>  
  
 <span data-ttu-id="7c6c0-109">Le <xref:System.Drawing.Graphics.FillPie%2A> méthode est un complément de la <xref:System.Drawing.Graphics.DrawArc%2A> (méthode).</span><span class="sxs-lookup"><span data-stu-id="7c6c0-109">The <xref:System.Drawing.Graphics.FillPie%2A> method is a companion to the <xref:System.Drawing.Graphics.DrawArc%2A> method.</span></span> <span data-ttu-id="7c6c0-110">Tout comme le <xref:System.Drawing.Graphics.DrawArc%2A> méthode dessine une partie du contour d’une ellipse, le <xref:System.Drawing.Graphics.FillPie%2A> méthode remplit une portion de l’intérieur d’une ellipse.</span><span class="sxs-lookup"><span data-stu-id="7c6c0-110">Just as the <xref:System.Drawing.Graphics.DrawArc%2A> method draws a portion of the outline of an ellipse, the <xref:System.Drawing.Graphics.FillPie%2A> method fills a portion of the interior of an ellipse.</span></span> <span data-ttu-id="7c6c0-111">L’exemple suivant dessine un arc et remplit la partie correspondante de l’intérieur de l’ellipse :</span><span class="sxs-lookup"><span data-stu-id="7c6c0-111">The following example draws an arc and fills the corresponding portion of the interior of the ellipse:</span></span>  
  
 [!code-csharp[LinesCurvesAndShapes#21](~/samples/snippets/csharp/VS_Snippets_Winforms/LinesCurvesAndShapes/CS/Class1.cs#21)]
 [!code-vb[LinesCurvesAndShapes#21](~/samples/snippets/visualbasic/VS_Snippets_Winforms/LinesCurvesAndShapes/VB/Class1.vb#21)]  
  
 <span data-ttu-id="7c6c0-112">L’illustration suivante montre l’arc et le secteur rempli.</span><span class="sxs-lookup"><span data-stu-id="7c6c0-112">The following illustration shows the arc and the filled pie.</span></span>  
  
 <span data-ttu-id="7c6c0-113">![Courbes ouvertes et fermées](./media/aboutgdip02-art25.gif "Aboutgdip02_art25")</span><span class="sxs-lookup"><span data-stu-id="7c6c0-113">![Open & Closed curves](./media/aboutgdip02-art25.gif "Aboutgdip02_art25")</span></span>  
  
 <span data-ttu-id="7c6c0-114">Le <xref:System.Drawing.Graphics.FillClosedCurve%2A> méthode est un complément de la <xref:System.Drawing.Graphics.DrawClosedCurve%2A> (méthode).</span><span class="sxs-lookup"><span data-stu-id="7c6c0-114">The <xref:System.Drawing.Graphics.FillClosedCurve%2A> method is a companion to the <xref:System.Drawing.Graphics.DrawClosedCurve%2A> method.</span></span> <span data-ttu-id="7c6c0-115">Les deux méthodes ferment automatiquement la courbe en connectant le point de fin au point de départ.</span><span class="sxs-lookup"><span data-stu-id="7c6c0-115">Both methods automatically close the curve by connecting the ending point to the starting point.</span></span> <span data-ttu-id="7c6c0-116">L’exemple suivant dessine une courbe qui traverse (0, 0), (60, 20) et (40, 50).</span><span class="sxs-lookup"><span data-stu-id="7c6c0-116">The following example draws a curve that passes through (0, 0), (60, 20), and (40, 50).</span></span> <span data-ttu-id="7c6c0-117">Ensuite, la courbe est fermée automatiquement en vous connectant (40, 50) au point de départ (0, 0), et l’intérieur est rempli avec une couleur unie.</span><span class="sxs-lookup"><span data-stu-id="7c6c0-117">Then, the curve is automatically closed by connecting (40, 50) to the starting point (0, 0), and the interior is filled with a solid color.</span></span>  
  
 [!code-csharp[LinesCurvesAndShapes#22](~/samples/snippets/csharp/VS_Snippets_Winforms/LinesCurvesAndShapes/CS/Class1.cs#22)]
 [!code-vb[LinesCurvesAndShapes#22](~/samples/snippets/visualbasic/VS_Snippets_Winforms/LinesCurvesAndShapes/VB/Class1.vb#22)]  
  
 <span data-ttu-id="7c6c0-118">Le <xref:System.Drawing.Graphics.FillPath%2A> méthode remplit l’intérieur des différents éléments d’un chemin d’accès.</span><span class="sxs-lookup"><span data-stu-id="7c6c0-118">The <xref:System.Drawing.Graphics.FillPath%2A> method fills the interiors of the separate pieces of a path.</span></span> <span data-ttu-id="7c6c0-119">Si une partie d’un chemin d’accès ne forme pas une courbe fermée ou une forme, le <xref:System.Drawing.Graphics.FillPath%2A> méthode ferme automatiquement cet élément et le chemin d’accès avant de le remplir.</span><span class="sxs-lookup"><span data-stu-id="7c6c0-119">If a piece of a path doesn't form a closed curve or shape, the <xref:System.Drawing.Graphics.FillPath%2A> method automatically closes that piece of the path before filling it.</span></span> <span data-ttu-id="7c6c0-120">L’exemple suivant dessine et remplit un chemin d’accès qui se compose d’un arc, une spline cardinale, une chaîne et un graphique en secteurs :</span><span class="sxs-lookup"><span data-stu-id="7c6c0-120">The following example draws and fills a path that consists of an arc, a cardinal spline, a string, and a pie:</span></span>  
  
 [!code-csharp[LinesCurvesAndShapes#23](~/samples/snippets/csharp/VS_Snippets_Winforms/LinesCurvesAndShapes/CS/Class1.cs#23)]
 [!code-vb[LinesCurvesAndShapes#23](~/samples/snippets/visualbasic/VS_Snippets_Winforms/LinesCurvesAndShapes/VB/Class1.vb#23)]  
  
 <span data-ttu-id="7c6c0-121">L’illustration suivante montre le chemin d’accès avec et sans le remplissage uni.</span><span class="sxs-lookup"><span data-stu-id="7c6c0-121">The following illustration shows the path with and without the solid fill.</span></span> <span data-ttu-id="7c6c0-122">Notez que le texte dans la chaîne est indiqué, mais ne remplit pas par le <xref:System.Drawing.Graphics.DrawPath%2A> (méthode).</span><span class="sxs-lookup"><span data-stu-id="7c6c0-122">Note that the text in the string is outlined, but not filled, by the <xref:System.Drawing.Graphics.DrawPath%2A> method.</span></span> <span data-ttu-id="7c6c0-123">Il s’agit du <xref:System.Drawing.Graphics.FillPath%2A> (méthode) qui peint l’intérieur des caractères dans la chaîne.</span><span class="sxs-lookup"><span data-stu-id="7c6c0-123">It is the <xref:System.Drawing.Graphics.FillPath%2A> method that paints the interiors of the characters in the string.</span></span>  
  
 <span data-ttu-id="7c6c0-124">![Chaîne dans un chemin d’accès](./media/aboutgdip02-art26.gif "Aboutgdip02_art26")</span><span class="sxs-lookup"><span data-stu-id="7c6c0-124">![String in a path](./media/aboutgdip02-art26.gif "Aboutgdip02_art26")</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="7c6c0-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="7c6c0-125">See also</span></span>

- <xref:System.Drawing.Drawing2D.GraphicsPath?displayProperty=nameWithType>
- <xref:System.Drawing.Pen?displayProperty=nameWithType>
- <xref:System.Drawing.Point?displayProperty=nameWithType>
- [<span data-ttu-id="7c6c0-126">Lignes, courbes et formes</span><span class="sxs-lookup"><span data-stu-id="7c6c0-126">Lines, Curves, and Shapes</span></span>](lines-curves-and-shapes.md)
- [<span data-ttu-id="7c6c0-127">Guide pratique pour Créer des objets graphiques pour le dessin</span><span class="sxs-lookup"><span data-stu-id="7c6c0-127">How to: Create Graphics Objects for Drawing</span></span>](how-to-create-graphics-objects-for-drawing.md)
- [<span data-ttu-id="7c6c0-128">Génération et dessin de tracés</span><span class="sxs-lookup"><span data-stu-id="7c6c0-128">Constructing and Drawing Paths</span></span>](constructing-and-drawing-paths.md)
