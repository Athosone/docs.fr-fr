---
title: 'Procédure : Dessiner une forme fermée à l’aide de l’élément Polygon'
ms.date: 03/30/2017
helpviewer_keywords:
- graphics [WPF], Polygon elements
- closed shapes [WPF], drawing with Polygon elements
- Polygon elements [WPF]
- drawing [WPF], closed shapes with Polygon elements
ms.assetid: 4b0ca008-29ce-48dd-8bc3-f3a20ffca6a6
ms.openlocfilehash: 533c341e2fae528ec896bf38bafa13974af1d127
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62003234"
---
# <a name="how-to-draw-a-closed-shape-by-using-the-polygon-element"></a>Procédure : Dessiner une forme fermée à l’aide de l’élément Polygon
Cet exemple montre comment dessiner une forme fermée à l’aide de la <xref:System.Windows.Shapes.Polygon> élément. Pour dessiner une forme fermée, créez un <xref:System.Windows.Shapes.Polygon> élément et utiliser ses <xref:System.Windows.Shapes.Polygon.Points%2A> propriété pour spécifier les vertex d’une forme. Une ligne est dessinée automatiquement qui se connecte le premier et dernier point. Enfin, spécifiez un <xref:System.Windows.Shapes.Shape.Fill%2A>, un <xref:System.Windows.Shapes.Shape.Stroke%2A>, ou les deux.  
  
## <a name="example"></a>Exemple  
 Dans [!INCLUDE[TLA#tla_xaml](../../../../includes/tlasharptla-xaml-md.md)], une syntaxe valide pour les points est une liste délimitée par des paires de séparées par des virgules coordonnées x et y.  
  
 [!code-xaml[drawingwithshapeelements#PolygonExample1](~/samples/snippets/csharp/VS_Snippets_Wpf/DrawingWithShapeElements/CS/polygonexample.xaml#polygonexample1)]  
  
 Bien que l’exemple utilise un <xref:System.Windows.Controls.Canvas> pour contenir les polygones, vous pouvez utiliser des éléments de polygone (et tous les autres éléments de la forme) avec n’importe quel <xref:System.Windows.Controls.Panel> ou <xref:System.Windows.Controls.Control> qui prend en charge le contenu non textuel.  
  
 Cet exemple fait partie d’un exemple plus complet ; Pour obtenir un exemple complet, consultez [exemples d’éléments de forme](https://go.microsoft.com/fwlink/?LinkID=160037).
