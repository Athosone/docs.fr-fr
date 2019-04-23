---
title: 'Procédure : Appliquer des propriétés Stretch au contenu d’un Viewbox'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- StretchDirection properties [WPF]
- Stretch properties [WPF]
- controls [WPF], Viewbox
- Viewbox control [WPF]
ms.assetid: b9c22ef4-bce4-4300-9e0c-8260b7db83cc
ms.openlocfilehash: 08358ea07e0c41e3b7cdf52251a3ed4296035e2d
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59209877"
---
# <a name="how-to-apply-stretch-properties-to-the-contents-of-a-viewbox"></a>Procédure : Appliquer des propriétés Stretch au contenu d’un Viewbox
## <a name="example"></a>Exemple  
 Cet exemple montre comment modifier la valeur de la <xref:System.Windows.Controls.Viewbox.StretchDirection%2A> et <xref:System.Windows.Controls.Viewbox.Stretch%2A> propriétés d’un <xref:System.Windows.Controls.Viewbox>.  
  
 Le premier exemple utilise [!INCLUDE[TLA#tla_xaml](../../../../includes/tlasharptla-xaml-md.md)] pour définir un <xref:System.Windows.Controls.Viewbox> élément. Il assigne un <xref:System.Windows.FrameworkElement.MaxWidth%2A> et <xref:System.Windows.FrameworkElement.MaxHeight%2A> de 400. L’exemple imbrique un <xref:System.Windows.Controls.Image> élément dans le <xref:System.Windows.Controls.Viewbox>. <xref:System.Windows.Controls.Button> éléments qui correspondent aux valeurs de propriété de la <xref:System.Windows.Controls.Viewbox.Stretch%2A> et <xref:System.Windows.Controls.StretchDirection> énumérations manipulent le comportement d’étirement de la commande imbriquée <xref:System.Windows.Controls.Image>.  
  
 [!code-xaml[viewboxStretchLayoutSamp#1](~/samples/snippets/csharp/VS_Snippets_Wpf/viewboxStretchLayoutSamp/CSharp/Window1.xaml#1)]  
  
 Les descripteurs de fichiers code-behind suivant le <xref:System.Windows.Controls.Button> <xref:System.Windows.Controls.Primitives.ButtonBase.Click> événements que le précédent [!INCLUDE[TLA2#tla_xaml](../../../../includes/tla2sharptla-xaml-md.md)] exemple définit.  
  
 [!code-csharp[viewboxStretchLayoutSamp#2](~/samples/snippets/csharp/VS_Snippets_Wpf/viewboxStretchLayoutSamp/CSharp/Window1.xaml.cs#2)]
 [!code-vb[viewboxStretchLayoutSamp#2](~/samples/snippets/visualbasic/VS_Snippets_Wpf/viewboxStretchLayoutSamp/VisualBasic/Window1.xaml.vb#2)]  
  
## <a name="see-also"></a>Voir aussi

- <xref:System.Windows.Controls.Viewbox>
- <xref:System.Windows.Media.Stretch>
- <xref:System.Windows.Controls.StretchDirection>
