---
title: 'Procédure : créer des figures à partir de lignes, courbes et formes'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- figures [Windows Forms], creating from shapes
- figures [Windows Forms], creating from lines
ms.assetid: 82fd56c7-b443-4765-9b7c-62ce030656ec
ms.openlocfilehash: eeaf478375e08734b20d83b6f3c8030732495013
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59224908"
---
# <a name="how-to-create-figures-from-lines-curves-and-shapes"></a><span data-ttu-id="f56c0-102">Procédure : créer des figures à partir de lignes, courbes et formes</span><span class="sxs-lookup"><span data-stu-id="f56c0-102">How to: Create Figures from Lines, Curves, and Shapes</span></span>
<span data-ttu-id="f56c0-103">Pour créer une figure, construisez un <xref:System.Drawing.Drawing2D.GraphicsPath>, puis appeler les méthodes, telles que <xref:System.Drawing.Drawing2D.GraphicsPath.AddLine%2A> et <xref:System.Drawing.Drawing2D.GraphicsPath.AddCurve%2A>, pour ajouter des primitives pour le chemin d’accès.</span><span class="sxs-lookup"><span data-stu-id="f56c0-103">To create a figure, construct a <xref:System.Drawing.Drawing2D.GraphicsPath>, and then call methods, such as <xref:System.Drawing.Drawing2D.GraphicsPath.AddLine%2A> and <xref:System.Drawing.Drawing2D.GraphicsPath.AddCurve%2A>, to add primitives to the path.</span></span>  
  
## <a name="example"></a><span data-ttu-id="f56c0-104">Exemple</span><span class="sxs-lookup"><span data-stu-id="f56c0-104">Example</span></span>  
 <span data-ttu-id="f56c0-105">Les exemples de code suivants créent des chemins d’accès qui comportent des figures :</span><span class="sxs-lookup"><span data-stu-id="f56c0-105">The following code examples create paths that have figures:</span></span>  
  
-   <span data-ttu-id="f56c0-106">Le premier exemple crée un chemin d’accès qui a une seule figure.</span><span class="sxs-lookup"><span data-stu-id="f56c0-106">The first example creates a path that has a single figure.</span></span> <span data-ttu-id="f56c0-107">La figure se compose d’un arc unique. L’arc a un angle de balayage de-180 degrés, ce qui est dans le sens inverse dans le système de coordonnées par défaut.</span><span class="sxs-lookup"><span data-stu-id="f56c0-107">The figure consists of a single arc. The arc has a sweep angle of –180 degrees, which is counterclockwise in the default coordinate system.</span></span>  
  
-   <span data-ttu-id="f56c0-108">Le deuxième exemple crée un chemin d’accès qui a deux chiffres.</span><span class="sxs-lookup"><span data-stu-id="f56c0-108">The second example creates a path that has two figures.</span></span> <span data-ttu-id="f56c0-109">La première représente un arc suivi d’une ligne.</span><span class="sxs-lookup"><span data-stu-id="f56c0-109">The first figure is an arc followed by a line.</span></span> <span data-ttu-id="f56c0-110">La deuxième figure est une ligne suivie d’une courbe de suivi d’une ligne.</span><span class="sxs-lookup"><span data-stu-id="f56c0-110">The second figure is a line followed by a curve followed by a line.</span></span> <span data-ttu-id="f56c0-111">La première figure est laissée ouverte, et la deuxième figure est fermée.</span><span class="sxs-lookup"><span data-stu-id="f56c0-111">The first figure is left open, and the second figure is closed.</span></span>  
  
 [!code-csharp[System.Drawing.ConstructingDrawingPaths#21](~/samples/snippets/csharp/VS_Snippets_Winforms/System.Drawing.ConstructingDrawingPaths/CS/Class1.cs#21)]
 [!code-vb[System.Drawing.ConstructingDrawingPaths#21](~/samples/snippets/visualbasic/VS_Snippets_Winforms/System.Drawing.ConstructingDrawingPaths/VB/Class1.vb#21)]  
  
 [!code-csharp[System.Drawing.ConstructingDrawingPaths#22](~/samples/snippets/csharp/VS_Snippets_Winforms/System.Drawing.ConstructingDrawingPaths/CS/Class1.cs#22)]
 [!code-vb[System.Drawing.ConstructingDrawingPaths#22](~/samples/snippets/visualbasic/VS_Snippets_Winforms/System.Drawing.ConstructingDrawingPaths/VB/Class1.vb#22)]  
  
## <a name="compiling-the-code"></a><span data-ttu-id="f56c0-112">Compilation du code</span><span class="sxs-lookup"><span data-stu-id="f56c0-112">Compiling the Code</span></span>  
 <span data-ttu-id="f56c0-113">Les exemples précédents sont conçus pour une utilisation avec Windows Forms, et ils nécessitent <xref:System.Windows.Forms.PaintEventArgs> `e`, qui est un paramètre de la <xref:System.Windows.Forms.Control.Paint> Gestionnaire d’événements.</span><span class="sxs-lookup"><span data-stu-id="f56c0-113">The previous examples are designed for use with Windows Forms, and they require <xref:System.Windows.Forms.PaintEventArgs> `e`, which is a parameter of the <xref:System.Windows.Forms.Control.Paint> event handler.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="f56c0-114">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f56c0-114">See also</span></span>

- <xref:System.Drawing.Drawing2D.GraphicsPath>
- [<span data-ttu-id="f56c0-115">Génération et dessin de tracés</span><span class="sxs-lookup"><span data-stu-id="f56c0-115">Constructing and Drawing Paths</span></span>](constructing-and-drawing-paths.md)
- [<span data-ttu-id="f56c0-116">Utilisation d'un stylet pour dessiner des lignes et des formes</span><span class="sxs-lookup"><span data-stu-id="f56c0-116">Using a Pen to Draw Lines and Shapes</span></span>](using-a-pen-to-draw-lines-and-shapes.md)
