---
title: 'Procédure : Animer un EllipseGeometry'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- animation [WPF], EllipseGeometry objects [WPF]
- EllipseGeometry objects [WPF], animating
- graphics [WPF], animation
ms.assetid: 767b9b6e-9cb7-482e-b6c2-fee7750c3995
ms.openlocfilehash: 0f8174a2144435c9ad65904ee587355e8b38e935
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59126007"
---
# <a name="how-to-animate-an-ellipsegeometry"></a><span data-ttu-id="8ada5-102">Procédure : Animer un EllipseGeometry</span><span class="sxs-lookup"><span data-stu-id="8ada5-102">How to: Animate an EllipseGeometry</span></span>
<span data-ttu-id="8ada5-103">Cet exemple montre comment animer un <xref:System.Windows.Media.Geometry> au sein d’un <xref:System.Windows.Shapes.Path> élément.</span><span class="sxs-lookup"><span data-stu-id="8ada5-103">This example shows how to animate a <xref:System.Windows.Media.Geometry> within a <xref:System.Windows.Shapes.Path> element.</span></span> <span data-ttu-id="8ada5-104">Dans l’exemple suivant, un <xref:System.Windows.Media.Animation.PointAnimation> est utilisé pour animer la <xref:System.Windows.Media.EllipseGeometry.Center%2A> d’un <xref:System.Windows.Media.EllipseGeometry>.</span><span class="sxs-lookup"><span data-stu-id="8ada5-104">In the following example, a <xref:System.Windows.Media.Animation.PointAnimation> is used to animate the <xref:System.Windows.Media.EllipseGeometry.Center%2A> of an <xref:System.Windows.Media.EllipseGeometry>.</span></span>  
  
## <a name="example"></a><span data-ttu-id="8ada5-105">Exemple</span><span class="sxs-lookup"><span data-stu-id="8ada5-105">Example</span></span>  
 [!code-xaml[animatepath_snip_XAML#1](~/samples/snippets/csharp/VS_Snippets_Wpf/animatepath_snip_XAML/CS/EllipseGeometryExample.xaml#1)]  
  
 [!code-csharp[animatepath_snip#101](~/samples/snippets/csharp/VS_Snippets_Wpf/animatepath_snip/CSharp/EllipseGeometryExample.cs#101)]  
  
 [!code-vb[animatepath_snip#201](~/samples/snippets/visualbasic/VS_Snippets_Wpf/animatepath_snip/VisualBasic/EllipseGeometryExample.vb#201)]  
  
## <a name="see-also"></a><span data-ttu-id="8ada5-106">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="8ada5-106">See also</span></span>

- [<span data-ttu-id="8ada5-107">Vue d’ensemble de l’animation</span><span class="sxs-lookup"><span data-stu-id="8ada5-107">Animation Overview</span></span>](animation-overview.md)
- [<span data-ttu-id="8ada5-108">Vue d’ensemble de Geometry</span><span class="sxs-lookup"><span data-stu-id="8ada5-108">Geometry Overview</span></span>](geometry-overview.md)
