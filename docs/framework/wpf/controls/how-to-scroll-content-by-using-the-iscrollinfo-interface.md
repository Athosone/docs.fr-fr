---
title: 'Procédure : Faire défiler le contenu à l’aide de l’interface IScrollInfo'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- ScrollViewer control [WPF], scrolling content
- scrolling content [WPF]
- IScrollInfo interface [WPF]
ms.assetid: d8700bef-a3f8-4c12-9de2-fc3b79f32cd3
ms.openlocfilehash: 6ebd8268e1358b45709885c07e6b096d5f806ebb
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62051245"
---
# <a name="how-to-scroll-content-by-using-the-iscrollinfo-interface"></a>Procédure : Faire défiler le contenu à l’aide de l’interface IScrollInfo
Cet exemple montre comment faire défiler le contenu à l’aide de la <xref:System.Windows.Controls.Primitives.IScrollInfo> interface.  
  
## <a name="example"></a>Exemple  
 L’exemple suivant illustre les fonctionnalités de la <xref:System.Windows.Controls.Primitives.IScrollInfo> interface. L’exemple crée un <xref:System.Windows.Controls.StackPanel> élément [!INCLUDE[TLA#tla_xaml](../../../../includes/tlasharptla-xaml-md.md)] qui est imbriqué dans un parent <xref:System.Windows.Controls.ScrollViewer>. Les éléments enfants de la <xref:System.Windows.Controls.StackPanel> peut défiler logiquement à l’aide des méthodes définies par le <xref:System.Windows.Controls.Primitives.IScrollInfo> interface et cast à l’instance de <xref:System.Windows.Controls.StackPanel> (`sp1`) dans le code.  
  
 [!code-xaml[IScrollInfoMethods#2](~/samples/snippets/csharp/VS_Snippets_Wpf/IScrollInfoMethods/CSharp/Window1.xaml#2)]  
  
 Chaque <xref:System.Windows.Controls.Button> dans le [!INCLUDE[TLA2#tla_xaml](../../../../includes/tla2sharptla-xaml-md.md)] fichier déclenche une méthode personnalisée associée qui contrôle le comportement de défilement dans <xref:System.Windows.Controls.StackPanel>. L’exemple suivant montre comment utiliser le <xref:System.Windows.Controls.Primitives.IScrollInfo.LineUp%2A> et <xref:System.Windows.Controls.Primitives.IScrollInfo.LineDown%2A> méthodes ; il indique également générique comment utiliser toutes les méthodes de positionnement qui le <xref:System.Windows.Controls.Primitives.IScrollInfo> classe définit.  
  
 [!code-csharp[IScrollInfoMethods#3](~/samples/snippets/csharp/VS_Snippets_Wpf/IScrollInfoMethods/CSharp/Window1.xaml.cs#3)]
 [!code-vb[IScrollInfoMethods#3](~/samples/snippets/visualbasic/VS_Snippets_Wpf/IScrollInfoMethods/VisualBasic/Window1.xaml.vb#3)]  
  
## <a name="see-also"></a>Voir aussi

- <xref:System.Windows.Controls.ScrollViewer>
- <xref:System.Windows.Controls.Primitives.IScrollInfo>
- <xref:System.Windows.Controls.StackPanel>
- [Vue d’ensemble de ScrollViewer](scrollviewer-overview.md)
- [Rubriques de guide pratique](scrollviewer-how-to-topics.md)
- [Vue d’ensemble de Panel](panels-overview.md)
