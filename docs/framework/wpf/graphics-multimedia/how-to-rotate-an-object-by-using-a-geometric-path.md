---
title: 'Procédure : Faire pivoter un objet à l’aide d’un tracé géométrique'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- geometric paths [WPF], rotating objects by
- rotating objects by geometric paths [WPF]
ms.assetid: cb31ca4d-f05a-4c6b-9a18-4b6faaf38d45
ms.openlocfilehash: 3e35169da7297ec62e0114ab21f4ba81c0a656ea
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61651244"
---
# <a name="how-to-rotate-an-object-by-using-a-geometric-path"></a><span data-ttu-id="b10cf-102">Procédure : Faire pivoter un objet à l’aide d’un tracé géométrique</span><span class="sxs-lookup"><span data-stu-id="b10cf-102">How to: Rotate an Object by Using a Geometric Path</span></span>
<span data-ttu-id="b10cf-103">Cet exemple montre comment faire tourner (pivoter) un objet sur un tracé géométrique défini par un <xref:System.Windows.Media.PathGeometry> objet.</span><span class="sxs-lookup"><span data-stu-id="b10cf-103">This example shows how to rotate (pivot) an object along a geometric path that is defined by a <xref:System.Windows.Media.PathGeometry> object.</span></span>  
  
## <a name="example"></a><span data-ttu-id="b10cf-104">Exemple</span><span class="sxs-lookup"><span data-stu-id="b10cf-104">Example</span></span>  
 <span data-ttu-id="b10cf-105">L’exemple suivant utilise trois <xref:System.Windows.Media.Animation.DoubleAnimationUsingPath> objets pour déplacer un rectangle sur un tracé géométrique.</span><span class="sxs-lookup"><span data-stu-id="b10cf-105">The following example uses three <xref:System.Windows.Media.Animation.DoubleAnimationUsingPath> objects to move a rectangle along a geometric path.</span></span>  
  
- <span data-ttu-id="b10cf-106">La première <xref:System.Windows.Media.Animation.DoubleAnimationUsingPath> anime un <xref:System.Windows.Media.RotateTransform> qui est appliqué au rectangle.</span><span class="sxs-lookup"><span data-stu-id="b10cf-106">The first <xref:System.Windows.Media.Animation.DoubleAnimationUsingPath> animates a <xref:System.Windows.Media.RotateTransform> that is applied to the rectangle.</span></span> <span data-ttu-id="b10cf-107">L’animation génère des valeurs d’angle.</span><span class="sxs-lookup"><span data-stu-id="b10cf-107">The animation generates angle values.</span></span> <span data-ttu-id="b10cf-108">Le rectangle tourne (pivote) ainsi sur les contours du tracé.</span><span class="sxs-lookup"><span data-stu-id="b10cf-108">It makes the rectangle rotate (pivot) along the contours of the path.</span></span>  
  
- <span data-ttu-id="b10cf-109">Les deux autres objets animent les <xref:System.Windows.Media.TranslateTransform.X%2A> et <xref:System.Windows.Media.TranslateTransform.Y%2A> valeurs d’un <xref:System.Windows.Media.TranslateTransform> qui est appliqué au rectangle.</span><span class="sxs-lookup"><span data-stu-id="b10cf-109">The other two objects animate the <xref:System.Windows.Media.TranslateTransform.X%2A> and <xref:System.Windows.Media.TranslateTransform.Y%2A> values of a <xref:System.Windows.Media.TranslateTransform> that is applied to the rectangle.</span></span> <span data-ttu-id="b10cf-110">Le rectangle se déplace alors horizontalement et verticalement sur le tracé.</span><span class="sxs-lookup"><span data-stu-id="b10cf-110">They make the rectangle move horizontally and vertically along the path.</span></span>  
  
 [!code-xaml[PathAnimationGallery_snippet#RotateAnimationUsingPathWholePage](~/samples/snippets/csharp/VS_Snippets_Wpf/PathAnimationGallery_snippet/CS/rotateanimationusingpathexample.xaml#rotateanimationusingpathwholepage)]  
  
 [!code-csharp[PathAnimationGallery_procedural_snip#RotateAnimationUsingPathWholePage](~/samples/snippets/csharp/VS_Snippets_Wpf/PathAnimationGallery_procedural_snip/CSharp/RotateAnimationUsingPathExample.cs#rotateanimationusingpathwholepage)]
 [!code-vb[PathAnimationGallery_procedural_snip#RotateAnimationUsingPathWholePage](~/samples/snippets/visualbasic/VS_Snippets_Wpf/PathAnimationGallery_procedural_snip/VisualBasic/RotateAnimationUsingPathExample.vb#rotateanimationusingpathwholepage)]  
  
 <span data-ttu-id="b10cf-111">Une autre façon de faire pivoter un objet à l’aide d’un tracé géométrique consiste à utiliser un <xref:System.Windows.Media.Animation.MatrixAnimationUsingPath> de l’objet et définissez son <xref:System.Windows.Media.Animation.MatrixAnimationUsingPath.DoesRotateWithTangent%2A> propriété `true`.</span><span class="sxs-lookup"><span data-stu-id="b10cf-111">Another way to rotate an object by using a geometric path is to use a <xref:System.Windows.Media.Animation.MatrixAnimationUsingPath> object and set its <xref:System.Windows.Media.Animation.MatrixAnimationUsingPath.DoesRotateWithTangent%2A> property to `true`.</span></span> <span data-ttu-id="b10cf-112">Pour plus d’informations et un exemple, consultez [faire pivoter un objet à l’aide d’un tracé géométrique (Animation de matrice)](how-to-rotate-an-object-by-using-a-geometric-path-matrix-animation.md).</span><span class="sxs-lookup"><span data-stu-id="b10cf-112">For more information and an example, see [Rotate an Object by Using a Geometric Path (Matrix Animation)](how-to-rotate-an-object-by-using-a-geometric-path-matrix-animation.md).</span></span>  
  
 <span data-ttu-id="b10cf-113">Pour obtenir un exemple complet, consultez [Animation de tracés, exemple](https://go.microsoft.com/fwlink/?LinkID=160028).</span><span class="sxs-lookup"><span data-stu-id="b10cf-113">For the complete sample, see [Path Animation Sample](https://go.microsoft.com/fwlink/?LinkID=160028).</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="b10cf-114">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b10cf-114">See also</span></span>

- [<span data-ttu-id="b10cf-115">Vue d’ensemble de l’animation</span><span class="sxs-lookup"><span data-stu-id="b10cf-115">Animation Overview</span></span>](animation-overview.md)
- [<span data-ttu-id="b10cf-116">Animation de tracés, exemple</span><span class="sxs-lookup"><span data-stu-id="b10cf-116">Path Animation Sample</span></span>](https://go.microsoft.com/fwlink/?LinkID=160028)
- [<span data-ttu-id="b10cf-117">Guides pratiques relatifs aux animations de tracés</span><span class="sxs-lookup"><span data-stu-id="b10cf-117">Path Animation How-to Topics</span></span>](path-animation-how-to-topics.md)
