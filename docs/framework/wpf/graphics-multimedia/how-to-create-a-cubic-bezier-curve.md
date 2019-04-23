---
title: 'Procédure : Créer une courbe de Bézier cubique'
ms.date: 03/30/2017
helpviewer_keywords:
- curves [WPF], cubic Bezier
- Bezier curves [WPF], cubic
- graphics [WPF], cubic Bezier curves
- cubic Bezier curves [WPF]
ms.assetid: 450a3a77-7c57-48b0-a008-0f6051add980
ms.openlocfilehash: 36544abc774b7fe82c2ff47483cfedd6fb13e344
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59115568"
---
# <a name="how-to-create-a-cubic-bezier-curve"></a>Procédure : Créer une courbe de Bézier cubique
Cet exemple montre comment créer une courbe de Bézier cubique. Pour créer une courbe de Bézier cubique, utilisez le <xref:System.Windows.Media.PathGeometry>, <xref:System.Windows.Media.PathFigure>, et <xref:System.Windows.Media.BezierSegment> classes.  Pour afficher la géométrie résultante, utilisez un <xref:System.Windows.Shapes.Path> élément, ou l’utiliser avec un <xref:System.Windows.Media.GeometryDrawing> ou un <xref:System.Windows.Media.DrawingContext>. Dans les exemples suivants, une courbe de Bézier cubique est tracée de (10, 100) à (300, 100). La courbe a des points de contrôle de (100, 0) et (200, 200).  
  
## <a name="example"></a>Exemple  
 [xaml]  
  
 Dans [!INCLUDE[TLA#tla_xaml](../../../../includes/tlasharptla-xaml-md.md)], vous pouvez utiliser la syntaxe de balise abrégée pour décrire un chemin d’accès.  
  
 [!code-xaml[GeometrySample#53](~/samples/snippets/csharp/VS_Snippets_Wpf/GeometrySample/CS/geometryattributesyntaxexample.xaml#53)]  
  
 [xaml]  
  
 Dans [!INCLUDE[TLA2#tla_xaml](../../../../includes/tla2sharptla-xaml-md.md)], vous pouvez également dessiner une courbe de Bézier cubique à l’aide de balises d’objet. L'exemple suivant est équivalent à l’exemple [!INCLUDE[TLA2#tla_xaml](../../../../includes/tla2sharptla-xaml-md.md)] précédent.  
  
 [!code-xaml[GeometrySample#33](~/samples/snippets/csharp/VS_Snippets_Wpf/GeometrySample/CS/pathgeometryexample.xaml#33)]  
  
 Cet exemple fait partie d’un exemple plus vaste ; pour l’exemple complet, consultez [Géométries, exemple](https://go.microsoft.com/fwlink/?LinkID=159989).  
  
## <a name="see-also"></a>Voir aussi

- [Créer un arc elliptique](how-to-create-an-elliptical-arc.md)
- [Créer un LineSegment dans une PathGeometry](how-to-create-a-linesegment-in-a-pathgeometry.md)
- [Créer une courbe de Bézier cubique](how-to-create-a-cubic-bezier-curve.md)
- [Créer une courbe de Bézier quadratique](how-to-create-a-quadratic-bezier-curve.md)
