---
title: Polygones dans GDI+
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- polygons
- drawing [Windows Forms], polygons
- GDI+, polygons
ms.assetid: a72213d2-d69a-4c2b-a75c-be7b20390c13
ms.openlocfilehash: 2b1e3d387e4d056d9187c54dcef560544206c370
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61641291"
---
# <a name="polygons-in-gdi"></a><span data-ttu-id="27f67-102">Polygones dans GDI+</span><span class="sxs-lookup"><span data-stu-id="27f67-102">Polygons in GDI+</span></span>
<span data-ttu-id="27f67-103">Un polygone est une forme fermée avec trois ou quatre côtés.</span><span class="sxs-lookup"><span data-stu-id="27f67-103">A polygon is a closed shape with three or more straight sides.</span></span> <span data-ttu-id="27f67-104">Par exemple, un triangle est un polygone à trois côtés, un rectangle est un polygone avec les quatre côtés et un pentagone est un polygone à cinq côtés.</span><span class="sxs-lookup"><span data-stu-id="27f67-104">For example, a triangle is a polygon with three sides, a rectangle is a polygon with four sides, and a pentagon is a polygon with five sides.</span></span> <span data-ttu-id="27f67-105">L’illustration suivante montre plusieurs polygones.</span><span class="sxs-lookup"><span data-stu-id="27f67-105">The following illustration shows several polygons.</span></span>  
  
 <span data-ttu-id="27f67-106">![Polygons](./media/aboutgdip02-art07.gif "Aboutgdip02_art07")</span><span class="sxs-lookup"><span data-stu-id="27f67-106">![Polygons](./media/aboutgdip02-art07.gif "Aboutgdip02_art07")</span></span>  
  
## <a name="drawing-a-polygon"></a><span data-ttu-id="27f67-107">Dessin d’un polygone</span><span class="sxs-lookup"><span data-stu-id="27f67-107">Drawing a Polygon</span></span>  
 <span data-ttu-id="27f67-108">Pour dessiner un polygone, vous devez un <xref:System.Drawing.Graphics> objet, un <xref:System.Drawing.Pen> objet et un tableau de <xref:System.Drawing.Point> (ou <xref:System.Drawing.PointF>) objets.</span><span class="sxs-lookup"><span data-stu-id="27f67-108">To draw a polygon, you need a <xref:System.Drawing.Graphics> object, a <xref:System.Drawing.Pen> object, and an array of <xref:System.Drawing.Point> (or <xref:System.Drawing.PointF>) objects.</span></span> <span data-ttu-id="27f67-109">Le <xref:System.Drawing.Graphics> objet fournit le <xref:System.Drawing.Graphics.DrawPolygon%2A> (méthode).</span><span class="sxs-lookup"><span data-stu-id="27f67-109">The <xref:System.Drawing.Graphics> object provides the <xref:System.Drawing.Graphics.DrawPolygon%2A> method.</span></span> <span data-ttu-id="27f67-110">Le <xref:System.Drawing.Pen> objet stocke les attributs, tels que la largeur et la couleur, de la ligne utilisée pour restituer le polygone et le tableau de <xref:System.Drawing.Point> objets stocke les points à relier par des lignes droites.</span><span class="sxs-lookup"><span data-stu-id="27f67-110">The <xref:System.Drawing.Pen> object stores attributes, such as width and color, of the line used to render the polygon, and the array of <xref:System.Drawing.Point> objects stores the points to be connected by straight lines.</span></span> <span data-ttu-id="27f67-111">Le <xref:System.Drawing.Pen> objet et le tableau de <xref:System.Drawing.Point> objets sont passés comme arguments pour le <xref:System.Drawing.Graphics.DrawPolygon%2A> (méthode).</span><span class="sxs-lookup"><span data-stu-id="27f67-111">The <xref:System.Drawing.Pen> object and the array of <xref:System.Drawing.Point> objects are passed as arguments to the <xref:System.Drawing.Graphics.DrawPolygon%2A> method.</span></span> <span data-ttu-id="27f67-112">L’exemple suivant dessine un polygone à trois côtés.</span><span class="sxs-lookup"><span data-stu-id="27f67-112">The following example draws a three-sided polygon.</span></span> <span data-ttu-id="27f67-113">Notez qu’il n’y a uniquement trois points dans `myPointArray`: (0, 0), (50, 30) et (30, 60).</span><span class="sxs-lookup"><span data-stu-id="27f67-113">Note that there are only three points in `myPointArray`: (0, 0), (50, 30), and (30, 60).</span></span> <span data-ttu-id="27f67-114">Le <xref:System.Drawing.Graphics.DrawPolygon%2A> méthode ferme automatiquement le polygone en dessinant une ligne à partir de (30, 60) par le point de départ (0, 0).</span><span class="sxs-lookup"><span data-stu-id="27f67-114">The <xref:System.Drawing.Graphics.DrawPolygon%2A> method automatically closes the polygon by drawing a line from (30, 60) back to the starting point (0, 0).</span></span>  
  
 [!code-csharp[LinesCurvesAndShapes#111](~/samples/snippets/csharp/VS_Snippets_Winforms/LinesCurvesAndShapes/CS/Class1.cs#111)]
 [!code-vb[LinesCurvesAndShapes#111](~/samples/snippets/visualbasic/VS_Snippets_Winforms/LinesCurvesAndShapes/VB/Class1.vb#111)]  
  
 <span data-ttu-id="27f67-115">L’illustration suivante montre le polygone.</span><span class="sxs-lookup"><span data-stu-id="27f67-115">The following illustration shows the polygon.</span></span>  
  
 <span data-ttu-id="27f67-116">![Polygon](./media/aboutgdip02-art08.gif "Aboutgdip02_art08")</span><span class="sxs-lookup"><span data-stu-id="27f67-116">![Polygon](./media/aboutgdip02-art08.gif "Aboutgdip02_art08")</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="27f67-117">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="27f67-117">See also</span></span>

- <xref:System.Drawing.Graphics?displayProperty=nameWithType>
- <xref:System.Drawing.Pen?displayProperty=nameWithType>
- [<span data-ttu-id="27f67-118">Lignes, courbes et formes</span><span class="sxs-lookup"><span data-stu-id="27f67-118">Lines, Curves, and Shapes</span></span>](lines-curves-and-shapes.md)
- [<span data-ttu-id="27f67-119">Guide pratique pour Créer un stylet</span><span class="sxs-lookup"><span data-stu-id="27f67-119">How to: Create a Pen</span></span>](how-to-create-a-pen.md)
