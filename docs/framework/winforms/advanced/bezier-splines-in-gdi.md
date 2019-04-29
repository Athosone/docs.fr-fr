---
title: B&#233;Bézier cardinales dans GDI +
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- Bezier splines
- splines [Windows Forms], Bezier
- GDI+, Bezier splines
ms.assetid: 5774ce1e-87d4-4bc7-88c4-4862052781b8
ms.openlocfilehash: ff4e9eb18610b70c88e057d3d44020321bbb9f4f
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61779247"
---
# <a name="b233zier-splines-in-gdi"></a><span data-ttu-id="ecad3-102">B&#233;Bézier cardinales dans GDI +</span><span class="sxs-lookup"><span data-stu-id="ecad3-102">B&#233;zier Splines in GDI+</span></span>
<span data-ttu-id="ecad3-103">Une spline de Bézier est une courbe spécifiée par quatre points : deux points de terminaison (p1 et p2) et deux points de contrôle (c1 et c2).</span><span class="sxs-lookup"><span data-stu-id="ecad3-103">A Bézier spline is a curve specified by four points: two end points (p1 and p2) and two control points (c1 and c2).</span></span> <span data-ttu-id="ecad3-104">La courbe commence en p1 et p2 se termine.</span><span class="sxs-lookup"><span data-stu-id="ecad3-104">The curve begins at p1 and ends at p2.</span></span> <span data-ttu-id="ecad3-105">La courbe ne passe pas par les points de contrôle, mais les points de contrôle agissent comme des aimants qui la courbe dans certaines directions et influencent la courbure de la courbe.</span><span class="sxs-lookup"><span data-stu-id="ecad3-105">The curve does not pass through the control points, but the control points act as magnets, pulling the curve in certain directions and influencing the way the curve bends.</span></span> <span data-ttu-id="ecad3-106">L’illustration suivante montre une courbe de Bézier, ainsi que ses points de terminaison et les points de contrôle.</span><span class="sxs-lookup"><span data-stu-id="ecad3-106">The following illustration shows a Bézier curve along with its endpoints and control points.</span></span>  
  
 <span data-ttu-id="ecad3-107">![Splines de Bézier](./media/aboutgdip02-art11a.gif "Aboutgdip02_art11a")</span><span class="sxs-lookup"><span data-stu-id="ecad3-107">![Bezier Splines](./media/aboutgdip02-art11a.gif "Aboutgdip02_art11a")</span></span>  
  
 <span data-ttu-id="ecad3-108">La courbe commence à p1 et se déplace vers le point de contrôle c1.</span><span class="sxs-lookup"><span data-stu-id="ecad3-108">The curve starts at p1 and moves toward the control point c1.</span></span> <span data-ttu-id="ecad3-109">La tangente de la courbe en p1 est la ligne dessinée de p1 à c1.</span><span class="sxs-lookup"><span data-stu-id="ecad3-109">The tangent line to the curve at p1 is the line drawn from p1 to c1.</span></span> <span data-ttu-id="ecad3-110">La tangente en p2 est la ligne dessinée de c2 à p2.</span><span class="sxs-lookup"><span data-stu-id="ecad3-110">The tangent line at the endpoint p2 is the line drawn from c2 to p2.</span></span>  
  
## <a name="drawing-bzier-splines"></a><span data-ttu-id="ecad3-111">Dessiner des Splines de Bézier</span><span class="sxs-lookup"><span data-stu-id="ecad3-111">Drawing Bézier Splines</span></span>  
 <span data-ttu-id="ecad3-112">Pour dessiner une spline de Bézier, vous avez besoin d’une instance de la <xref:System.Drawing.Graphics> classe et un <xref:System.Drawing.Pen>.</span><span class="sxs-lookup"><span data-stu-id="ecad3-112">To draw a Bézier spline, you need an instance of the <xref:System.Drawing.Graphics> class and a <xref:System.Drawing.Pen>.</span></span> <span data-ttu-id="ecad3-113">L’instance de la <xref:System.Drawing.Graphics> classe fournit le <xref:System.Drawing.Graphics.DrawBezier%2A> (méthode) et le <xref:System.Drawing.Pen> stocke les attributs, tels que la largeur et la couleur, de la ligne utilisée pour représenter la courbe.</span><span class="sxs-lookup"><span data-stu-id="ecad3-113">The instance of the <xref:System.Drawing.Graphics> class provides the <xref:System.Drawing.Graphics.DrawBezier%2A> method, and the <xref:System.Drawing.Pen> stores attributes, such as width and color, of the line used to render the curve.</span></span> <span data-ttu-id="ecad3-114">Le <xref:System.Drawing.Pen> est passé en tant qu’arguments à la <xref:System.Drawing.Graphics.DrawBezier%2A> (méthode).</span><span class="sxs-lookup"><span data-stu-id="ecad3-114">The <xref:System.Drawing.Pen> is passed as one of the arguments to the <xref:System.Drawing.Graphics.DrawBezier%2A> method.</span></span> <span data-ttu-id="ecad3-115">Les autres arguments passés à la <xref:System.Drawing.Graphics.DrawBezier%2A> méthode sont les points de terminaison et les points de contrôle.</span><span class="sxs-lookup"><span data-stu-id="ecad3-115">The remaining arguments passed to the <xref:System.Drawing.Graphics.DrawBezier%2A> method are the endpoints and the control points.</span></span> <span data-ttu-id="ecad3-116">L’exemple suivant dessine une spline de Bézier avec le point de départ (0, 0), contrôler les points (40, 20) et (80, 150) et se terminant par le point (100, 10) :</span><span class="sxs-lookup"><span data-stu-id="ecad3-116">The following example draws a Bézier spline with starting point (0, 0), control points (40, 20) and (80, 150), and ending point (100, 10):</span></span>  
  
 [!code-csharp[LinesCurvesAndShapes#71](~/samples/snippets/csharp/VS_Snippets_Winforms/LinesCurvesAndShapes/CS/Class1.cs#71)]
 [!code-vb[LinesCurvesAndShapes#71](~/samples/snippets/visualbasic/VS_Snippets_Winforms/LinesCurvesAndShapes/VB/Class1.vb#71)]  
  
 <span data-ttu-id="ecad3-117">L’illustration suivante montre la courbe, les points de contrôle et deux lignes tangents.</span><span class="sxs-lookup"><span data-stu-id="ecad3-117">The following illustration shows the curve, the control points, and two tangent lines.</span></span>  
  
 <span data-ttu-id="ecad3-118">![Splines de Bézier](./media/aboutgdip02-art12.gif "Aboutgdip02_art12")</span><span class="sxs-lookup"><span data-stu-id="ecad3-118">![Bezier Splines](./media/aboutgdip02-art12.gif "Aboutgdip02_art12")</span></span>  
  
 <span data-ttu-id="ecad3-119">Splines de Bézier ont été initialement développés par Pierre Bézier pour la conception de l’industrie automobile.</span><span class="sxs-lookup"><span data-stu-id="ecad3-119">Bézier splines were originally developed by Pierre Bézier for design in the automotive industry.</span></span> <span data-ttu-id="ecad3-120">Ils ont fait leurs preuves pour être utile dans de nombreux types de conception assistée par ordinateur et sont également utilisées pour définir les contours des polices.</span><span class="sxs-lookup"><span data-stu-id="ecad3-120">They have since proven to be useful in many types of computer-aided design and are also used to define the outlines of fonts.</span></span> <span data-ttu-id="ecad3-121">Splines de Bézier peuvent produire une grande variété de formes, certains d'entre eux sont affichés dans l’illustration suivante.</span><span class="sxs-lookup"><span data-stu-id="ecad3-121">Bézier splines can yield a wide variety of shapes, some of which are shown in the following illustration.</span></span>  
  
 <span data-ttu-id="ecad3-122">![Paths](./media/aboutgdip02-art13.gif "Aboutgdip02_art13")</span><span class="sxs-lookup"><span data-stu-id="ecad3-122">![Paths](./media/aboutgdip02-art13.gif "Aboutgdip02_art13")</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="ecad3-123">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ecad3-123">See also</span></span>

- <xref:System.Drawing.Graphics?displayProperty=nameWithType>
- <xref:System.Drawing.Pen?displayProperty=nameWithType>
- [<span data-ttu-id="ecad3-124">Lignes, courbes et formes</span><span class="sxs-lookup"><span data-stu-id="ecad3-124">Lines, Curves, and Shapes</span></span>](lines-curves-and-shapes.md)
- [<span data-ttu-id="ecad3-125">Génération et dessin de courbes</span><span class="sxs-lookup"><span data-stu-id="ecad3-125">Constructing and Drawing Curves</span></span>](constructing-and-drawing-curves.md)
- [<span data-ttu-id="ecad3-126">Guide pratique pour Créer des objets graphiques pour le dessin</span><span class="sxs-lookup"><span data-stu-id="ecad3-126">How to: Create Graphics Objects for Drawing</span></span>](how-to-create-graphics-objects-for-drawing.md)
- [<span data-ttu-id="ecad3-127">Guide pratique pour Créer un stylet</span><span class="sxs-lookup"><span data-stu-id="ecad3-127">How to: Create a Pen</span></span>](how-to-create-a-pen.md)
