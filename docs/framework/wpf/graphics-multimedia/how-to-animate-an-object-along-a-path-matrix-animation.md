---
title: 'Procédure : Animer un objet sur un tracé (animation de matrice)'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- animation [WPF], objects along paths (matrix animation)
- matrix animation [WPF]
ms.assetid: 7000e697-1414-468c-b915-cf66062fc49e
ms.openlocfilehash: ab15126680b7d8c6936246a7dae2f67c7541233b
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59190923"
---
# <a name="how-to-animate-an-object-along-a-path-matrix-animation"></a><span data-ttu-id="6de15-102">Procédure : Animer un objet sur un tracé (animation de matrice)</span><span class="sxs-lookup"><span data-stu-id="6de15-102">How to: Animate an Object Along a Path (Matrix Animation)</span></span>
<span data-ttu-id="6de15-103">Cet exemple montre comment utiliser le <xref:System.Windows.Media.Animation.MatrixAnimationUsingPath> classe pour animer un objet sur un tracé défini par un <xref:System.Windows.Media.PathGeometry>.</span><span class="sxs-lookup"><span data-stu-id="6de15-103">This example shows how to use the <xref:System.Windows.Media.Animation.MatrixAnimationUsingPath> class to animate an object along a path that is defined by a <xref:System.Windows.Media.PathGeometry>.</span></span>  
  
## <a name="example"></a><span data-ttu-id="6de15-104">Exemple</span><span class="sxs-lookup"><span data-stu-id="6de15-104">Example</span></span>  
 <span data-ttu-id="6de15-105">L’exemple suivant anime un objet sur un tracé de la manière suivante :</span><span class="sxs-lookup"><span data-stu-id="6de15-105">The following example animates an object along a path by doing the following:</span></span>  
  
-   <span data-ttu-id="6de15-106">Applique un <xref:System.Windows.Media.MatrixTransform> à l’objet afin de le déplacer.</span><span class="sxs-lookup"><span data-stu-id="6de15-106">Applies a <xref:System.Windows.Media.MatrixTransform> to the object in order to move it.</span></span>  
  
-   <span data-ttu-id="6de15-107">Définit le chemin d’accès en utilisant un <xref:System.Windows.Media.PathGeometry>.</span><span class="sxs-lookup"><span data-stu-id="6de15-107">Defines the path by using a <xref:System.Windows.Media.PathGeometry>.</span></span>  
  
-   <span data-ttu-id="6de15-108">Crée un <xref:System.Windows.Media.Animation.MatrixAnimationUsingPath> et l’utilise pour animer la <xref:System.Windows.Media.Matrix> propriété de la <xref:System.Windows.Media.MatrixTransform>.</span><span class="sxs-lookup"><span data-stu-id="6de15-108">Creates a <xref:System.Windows.Media.Animation.MatrixAnimationUsingPath> and uses it to animate the <xref:System.Windows.Media.Matrix> property of the <xref:System.Windows.Media.MatrixTransform>.</span></span> <span data-ttu-id="6de15-109">Le <xref:System.Windows.Media.Animation.MatrixAnimationUsingPath> prend le <xref:System.Windows.Media.PathGeometry> et l’utilise pour générer <xref:System.Windows.Media.Matrix> valeurs.</span><span class="sxs-lookup"><span data-stu-id="6de15-109">The <xref:System.Windows.Media.Animation.MatrixAnimationUsingPath> takes the <xref:System.Windows.Media.PathGeometry> and uses it to generate <xref:System.Windows.Media.Matrix> values.</span></span>  
  
 [!code-xaml[PathAnimationGallery_snippet#MatrixAnimationUsingPathWholePage](~/samples/snippets/csharp/VS_Snippets_Wpf/PathAnimationGallery_snippet/CS/matrixanimationusingpathexample.xaml#matrixanimationusingpathwholepage)]  
  
 [!code-csharp[PathAnimationGallery_procedural_snip#MatrixAnimationUsingPathWholePage](~/samples/snippets/csharp/VS_Snippets_Wpf/PathAnimationGallery_procedural_snip/CSharp/MatrixAnimationUsingPathExample.cs#matrixanimationusingpathwholepage)]
 [!code-vb[PathAnimationGallery_procedural_snip#MatrixAnimationUsingPathWholePage](~/samples/snippets/visualbasic/VS_Snippets_Wpf/PathAnimationGallery_procedural_snip/VisualBasic/MatrixAnimationUsingPathExample.vb#matrixanimationusingpathwholepage)]  
  
 <span data-ttu-id="6de15-110">Pour obtenir un exemple complet, consultez [Animation de tracés, exemple](https://go.microsoft.com/fwlink/?LinkID=160028).</span><span class="sxs-lookup"><span data-stu-id="6de15-110">For the complete sample, see [Path Animation Sample](https://go.microsoft.com/fwlink/?LinkID=160028).</span></span> <span data-ttu-id="6de15-111">Pour plus d’informations sur les tracés géométriques, consultez le [vue d’ensemble de Geometry](geometry-overview.md).</span><span class="sxs-lookup"><span data-stu-id="6de15-111">For more information about geometric paths, see the [Geometry Overview](geometry-overview.md).</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="6de15-112">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="6de15-112">See also</span></span>

- [<span data-ttu-id="6de15-113">Vue d’ensemble de l’animation</span><span class="sxs-lookup"><span data-stu-id="6de15-113">Animation Overview</span></span>](animation-overview.md)
- [<span data-ttu-id="6de15-114">Animation de tracés, exemple</span><span class="sxs-lookup"><span data-stu-id="6de15-114">Path Animation Sample</span></span>](https://go.microsoft.com/fwlink/?LinkID=160028)
- [<span data-ttu-id="6de15-115">Guides pratiques relatifs aux animations de tracés</span><span class="sxs-lookup"><span data-stu-id="6de15-115">Path Animation How-to Topics</span></span>](path-animation-how-to-topics.md)
