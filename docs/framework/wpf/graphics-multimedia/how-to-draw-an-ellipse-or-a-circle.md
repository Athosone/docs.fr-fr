---
title: 'Procédure : Dessiner une ellipse ou un cercle'
ms.date: 03/30/2017
helpviewer_keywords:
- ellipses [WPF], drawing
- circles [WPF], drawing
- drawing circles [WPF]
- drawing ellipses [WPF]
- graphics [WPF], drawing circles
- graphics [WPF], drawing ellipses
ms.assetid: 99763b8c-bfc8-44be-8231-8a70daf5481a
ms.openlocfilehash: 1393e158c1787dc7d4e44e5e1c90ed2e65666dc3
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59146742"
---
# <a name="how-to-draw-an-ellipse-or-a-circle"></a>Procédure : Dessiner une ellipse ou un cercle
Cet exemple montre comment dessiner des ellipses et des cercles à l’aide de la <xref:System.Windows.Shapes.Ellipse> élément. Pour dessiner une ellipse, créez un <xref:System.Windows.Shapes.Ellipse> élément et spécifiez son <xref:System.Windows.FrameworkElement.Width%2A> et <xref:System.Windows.FrameworkElement.Height%2A>. Utilisez ses <xref:System.Windows.Shapes.Shape.Fill%2A> propriété pour spécifier le <xref:System.Windows.Media.Brush> qui est utilisé pour peindre l’intérieur de l’ellipse. Utilisez ses <xref:System.Windows.Shapes.Shape.Stroke%2A> propriété pour spécifier le <xref:System.Windows.Media.Brush> qui est utilisé pour peindre le contour de l’ellipse. Le <xref:System.Windows.Shapes.Shape.StrokeThickness%2A> propriété spécifie l’épaisseur du contour de l’ellipse.  
  
 Pour dessiner un cercle, effectuez la <xref:System.Windows.FrameworkElement.Width%2A> et <xref:System.Windows.FrameworkElement.Height%2A> de la <xref:System.Windows.Shapes.Ellipse> élément égal à l’autre.  
  
 L’exemple suivant dessine quatre <xref:System.Windows.Shapes.Ellipse> éléments au sein d’un <xref:System.Windows.Controls.Canvas>.  
  
## <a name="example"></a>Exemple  
 [!code-xaml[drawingwithshapeelements#EllipseExample1](~/samples/snippets/csharp/VS_Snippets_Wpf/DrawingWithShapeElements/CS/ellipseexample.xaml#ellipseexample1)]  
  
 Bien que cet exemple utilise un <xref:System.Windows.Controls.Canvas> pour contenir les points de suspension, vous pouvez utiliser des éléments de l’ellipse (et tous les autres éléments de la forme) avec n’importe quel <xref:System.Windows.Controls.Panel> ou <xref:System.Windows.Controls.Control> qui prend en charge le contenu non textuel.  
  
 Cet exemple fait partie d’un exemple plus complet ; Pour obtenir un exemple complet, consultez [exemples d’éléments de forme](https://go.microsoft.com/fwlink/?LinkID=160037).  
  
## <a name="see-also"></a>Voir aussi

- <xref:System.Windows.Shapes.Ellipse>
- <xref:System.Windows.Shapes.Shape>
- [Exemples d’éléments de forme](https://go.microsoft.com/fwlink/?LinkID=160037)
