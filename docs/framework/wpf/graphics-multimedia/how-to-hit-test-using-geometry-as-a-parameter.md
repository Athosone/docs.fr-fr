---
title: 'Procédure : Effectuer un test de positionnement avec Geometry comme paramètre'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- hit tests [WPF], on visual objects using Geometry objects [WPF]
- visual objects [WPF], hit tests on
- Geometry objects [WPF], hit tests on visual objects [WPF]
ms.assetid: 6c8bdbf2-19e0-4fbb-bf89-c1252b2ebc61
ms.openlocfilehash: 73420d6ae1386676ed900e91b3951df9e0934db8
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59100962"
---
# <a name="how-to-hit-test-using-geometry-as-a-parameter"></a><span data-ttu-id="30464-102">Procédure : Effectuer un test de positionnement avec Geometry comme paramètre</span><span class="sxs-lookup"><span data-stu-id="30464-102">How to: Hit Test Using Geometry as a Parameter</span></span>
<span data-ttu-id="30464-103">Cet exemple montre comment effectuer un test de positionnement sur un objet visuel à l’aide un <xref:System.Windows.Media.Geometry> comme test d’atteinte paramètre.</span><span class="sxs-lookup"><span data-stu-id="30464-103">This example shows how to perform a hit test on a visual object using a <xref:System.Windows.Media.Geometry> as a hit test parameter.</span></span>  
  
## <a name="example"></a><span data-ttu-id="30464-104">Exemple</span><span class="sxs-lookup"><span data-stu-id="30464-104">Example</span></span>  
 <span data-ttu-id="30464-105">L’exemple suivant montre comment configurer un test de positionnement à l’aide <xref:System.Windows.Media.GeometryHitTestParameters> pour le <xref:System.Windows.Media.VisualTreeHelper.HitTest%2A> (méthode).</span><span class="sxs-lookup"><span data-stu-id="30464-105">The following example shows how to set up a hit test using <xref:System.Windows.Media.GeometryHitTestParameters> for the <xref:System.Windows.Media.VisualTreeHelper.HitTest%2A> method.</span></span> <span data-ttu-id="30464-106">Le <xref:System.Windows.Point> valeur qui est passée à la `OnMouseDown` méthode est utilisée pour créer un <xref:System.Windows.Media.Geometry> objet afin d’étendre la plage du test d’atteinte.</span><span class="sxs-lookup"><span data-stu-id="30464-106">The <xref:System.Windows.Point> value that is passed to the `OnMouseDown` method is used to create a <xref:System.Windows.Media.Geometry> object in order to expand the range of the hit test.</span></span>  
  
 [!code-csharp[HitTestingOverview#HitTestingOverviewSnippet10](~/samples/snippets/csharp/VS_Snippets_Wpf/HitTestingOverview/CSharp/GeometryHitTest.cs#hittestingoverviewsnippet10)]
 [!code-vb[HitTestingOverview#HitTestingOverviewSnippet10](~/samples/snippets/visualbasic/VS_Snippets_Wpf/HitTestingOverview/visualbasic/geometryhittest.vb#hittestingoverviewsnippet10)]  
  
 <span data-ttu-id="30464-107">Le <xref:System.Windows.Media.GeometryHitTestResult.IntersectionDetail%2A> propriété du <xref:System.Windows.Media.GeometryHitTestResult> fournit des informations sur les résultats d’un test d’atteinte qui utilise un <xref:System.Windows.Media.Geometry> comme test d’atteinte paramètre.</span><span class="sxs-lookup"><span data-stu-id="30464-107">The <xref:System.Windows.Media.GeometryHitTestResult.IntersectionDetail%2A> property of <xref:System.Windows.Media.GeometryHitTestResult> provides information about the results of a hit test that uses a <xref:System.Windows.Media.Geometry> as a hit test parameter.</span></span> <span data-ttu-id="30464-108">L’illustration suivante montre la relation entre la géométrie du test de positionnement (le cercle bleu) et le contenu restitué de l’objet visuel cible (le carré rouge).</span><span class="sxs-lookup"><span data-stu-id="30464-108">The following illustration shows the relationship between the hit test geometry (the blue circle) and the rendered content of the target visual object (the red square).</span></span>  
  
 ![Diagramme illustrant IntersectionDetail utilisé dans le test de positionnement.](./media/how-to-hit-test-using-geometry-as-a-parameter/intersectiondetail-hit-test.png)  
  
 <span data-ttu-id="30464-110">L’exemple suivant montre comment implémenter un rappel de test de positionnement lorsqu’un <xref:System.Windows.Media.Geometry> est utilisé comme un paramètre de test de positionnement.</span><span class="sxs-lookup"><span data-stu-id="30464-110">The following example shows how to implement a hit test callback when a <xref:System.Windows.Media.Geometry> is used as a hit test parameter.</span></span> <span data-ttu-id="30464-111">Le `result` paramètre est casté en un <xref:System.Windows.Media.GeometryHitTestResult> afin de récupérer la valeur de la <xref:System.Windows.Media.GeometryHitTestResult.IntersectionDetail%2A> propriété.</span><span class="sxs-lookup"><span data-stu-id="30464-111">The `result` parameter is cast to a <xref:System.Windows.Media.GeometryHitTestResult> in order to retrieve the value of the <xref:System.Windows.Media.GeometryHitTestResult.IntersectionDetail%2A> property.</span></span> <span data-ttu-id="30464-112">La valeur de propriété vous permet de déterminer si le <xref:System.Windows.Media.Geometry> paramètre de test de positionnement est entièrement ou partiellement contenu dans le contenu restitué de la cible du test d’atteinte.</span><span class="sxs-lookup"><span data-stu-id="30464-112">The property value allows you to determine if the <xref:System.Windows.Media.Geometry> hit test parameter is fully or partially contained within the rendered content of the hit test target.</span></span> <span data-ttu-id="30464-113">Dans ce cas, l’exemple de code ajoute à la liste les résultats du test de positionnement uniquement pour les objets visuels qui sont entièrement contenus dans les limites de la cible.</span><span class="sxs-lookup"><span data-stu-id="30464-113">In this case, the sample code is only adding hit test results to the list for visuals that are fully contained within the target boundary.</span></span>  
  
 [!code-csharp[HitTestingOverview#HitTestingOverviewSnippet11](~/samples/snippets/csharp/VS_Snippets_Wpf/HitTestingOverview/CSharp/GeometryHitTest.cs#hittestingoverviewsnippet11)]
 [!code-vb[HitTestingOverview#HitTestingOverviewSnippet11](~/samples/snippets/visualbasic/VS_Snippets_Wpf/HitTestingOverview/visualbasic/geometryhittest.vb#hittestingoverviewsnippet11)]  
  
> [!NOTE]
>  <span data-ttu-id="30464-114">Le <xref:System.Windows.Media.HitTestResult> rappel ne doit pas être appelé lorsque le détail de l’intersection est <xref:System.Windows.Media.IntersectionDetail.Empty>.</span><span class="sxs-lookup"><span data-stu-id="30464-114">The <xref:System.Windows.Media.HitTestResult> callback should not be called when the intersection detail is <xref:System.Windows.Media.IntersectionDetail.Empty>.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="30464-115">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="30464-115">See also</span></span>

- [<span data-ttu-id="30464-116">Test de positionnement dans la couche visuelle</span><span class="sxs-lookup"><span data-stu-id="30464-116">Hit Testing in the Visual Layer</span></span>](hit-testing-in-the-visual-layer.md)
- [<span data-ttu-id="30464-117">Effectuer un test de positionnement avec Geometry dans un Visual</span><span class="sxs-lookup"><span data-stu-id="30464-117">Hit Test Geometry in a Visual</span></span>](how-to-hit-test-geometry-in-a-visual.md)
