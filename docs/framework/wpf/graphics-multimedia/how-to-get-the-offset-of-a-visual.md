---
title: 'Procédure : Obtenir le décalage d’un visuel'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- getting offset values from visual objects [WPF]
- offset values [WPF], retrieving from visual objects [WPF]
- visual objects [WPF], retrieving offset values from
- retrieving offset values from visual objects [WPF]
ms.assetid: 889a1dd6-1b11-445a-b351-fbb04c53ee34
ms.openlocfilehash: 4787b771c7e59a8b033b9267079c068a5845a1e6
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61947488"
---
# <a name="how-to-get-the-offset-of-a-visual"></a>Procédure : Obtenir le décalage d’un visuel
Ces exemples montrent comment récupérer la valeur de décalage d’un objet visuel qui est relative à son parent, ou de n’importe quel ancêtre ou descendant.  
  
## <a name="example"></a>Exemple  
 L’exemple de balisage suivant montre un <xref:System.Windows.Controls.TextBlock> qui est défini avec <xref:System.Windows.FrameworkElement.Margin%2A> égale à 4.  
  
 [!code-xaml[VisualSnippets#VisualSnippet1](~/samples/snippets/csharp/VS_Snippets_Wpf/VisualSnippets/CSharp/Window1.xaml#visualsnippet1)]  
  
 L’exemple de code suivant montre comment utiliser le <xref:System.Windows.Media.VisualTreeHelper.GetOffset%2A> méthode pour récupérer le décalage de la <xref:System.Windows.Controls.TextBlock>. Les valeurs de décalage sont contenus dans le texte retourné <xref:System.Windows.Vector> valeur.  
  
 [!code-csharp[VisualSnippets#VisualSnippet2](~/samples/snippets/csharp/VS_Snippets_Wpf/VisualSnippets/CSharp/Window1.xaml.cs#visualsnippet2)]
 [!code-vb[VisualSnippets#VisualSnippet2](~/samples/snippets/visualbasic/VS_Snippets_Wpf/VisualSnippets/visualbasic/window1.xaml.vb#visualsnippet2)]  
  
 L’offset prend en compte la <xref:System.Windows.FrameworkElement.Margin%2A> valeur. Dans ce cas, <xref:System.Windows.Vector.X%2A> est 4, et <xref:System.Windows.Vector.Y%2A> est 4.  
  
 La valeur de décalage retournée est relatif au parent de la <xref:System.Windows.Media.Visual>. Si vous souhaitez retourner une valeur de décalage par rapport au parent de n’est pas un <xref:System.Windows.Media.Visual>, utilisez le <xref:System.Windows.Media.Visual.TransformToAncestor%2A> (méthode).  
  
## <a name="getting-the-offset-relative-to-an-ancestor"></a>Obtention de l’Offset relatif à un ancêtre  
 L’exemple de balisage suivant montre un <xref:System.Windows.Controls.TextBlock> qui est imbriqué dans deux <xref:System.Windows.Controls.StackPanel> objets.  
  
 [!code-xaml[VisualSnippets#VisualSnippet7](~/samples/snippets/csharp/VS_Snippets_Wpf/VisualSnippets/CSharp/Window2.xaml#visualsnippet7)]  
  
 L’illustration suivante montre les résultats du balisage.  
  
 ![Valeurs de décalage des objets](./media/visualoffset-01.png "VisualOffset_01")  
TextBlock imbriqué dans deux StackPanel  
  
 L’exemple de code suivant montre comment utiliser le <xref:System.Windows.Media.Visual.TransformToAncestor%2A> méthode pour récupérer le décalage de la <xref:System.Windows.Controls.TextBlock> par rapport à la contenant <xref:System.Windows.Window>. Les valeurs de décalage sont contenus dans le texte retourné <xref:System.Windows.Media.GeneralTransform> valeur.  
  
 [!code-csharp[VisualSnippets#VisualSnippet5](~/samples/snippets/csharp/VS_Snippets_Wpf/VisualSnippets/CSharp/Window1.xaml.cs#visualsnippet5)]
 [!code-vb[VisualSnippets#VisualSnippet5](~/samples/snippets/visualbasic/VS_Snippets_Wpf/VisualSnippets/visualbasic/window1.xaml.vb#visualsnippet5)]  
  
 L’offset prend en compte la <xref:System.Windows.FrameworkElement.Margin%2A> valeurs pour tous les objets dans le contenant <xref:System.Windows.Window>. Dans ce cas, <xref:System.Windows.Vector.X%2A> est 28 (16 + 8 + 4), et <xref:System.Windows.Vector.Y%2A> est 28.  
  
 La valeur de décalage retournée est par rapport à l’ancêtre de la <xref:System.Windows.Media.Visual>. Si vous souhaitez retourner une valeur de décalage est relative au descendant d’un <xref:System.Windows.Media.Visual>, utilisez le <xref:System.Windows.Media.Visual.TransformToDescendant%2A> (méthode).  
  
## <a name="getting-the-offset-relative-to-a-descendant"></a>Obtention de l’Offset par rapport à un Descendant  
 L’exemple de balisage suivant montre un <xref:System.Windows.Controls.TextBlock> qui est contenue dans un <xref:System.Windows.Controls.StackPanel> objet.  
  
 [!code-xaml[VisualSnippets#VisualSnippet4](~/samples/snippets/csharp/VS_Snippets_Wpf/VisualSnippets/CSharp/Window1.xaml#visualsnippet4)]  
  
 L’exemple de code suivant montre comment utiliser le <xref:System.Windows.Media.Visual.TransformToDescendant%2A> méthode pour récupérer le décalage de la <xref:System.Windows.Controls.StackPanel> par rapport à son enfant <xref:System.Windows.Controls.TextBlock>. Les valeurs de décalage sont contenus dans le texte retourné <xref:System.Windows.Media.GeneralTransform> valeur.  
  
 [!code-csharp[VisualSnippets#VisualSnippet9](~/samples/snippets/csharp/VS_Snippets_Wpf/VisualSnippets/CSharp/Window1.xaml.cs#visualsnippet9)]
 [!code-vb[VisualSnippets#VisualSnippet9](~/samples/snippets/visualbasic/VS_Snippets_Wpf/VisualSnippets/visualbasic/window1.xaml.vb#visualsnippet9)]  
  
 L’offset prend en compte la <xref:System.Windows.FrameworkElement.Margin%2A> valeurs pour tous les objets. Dans ce cas, <xref:System.Windows.Vector.X%2A> est -4, et <xref:System.Windows.Vector.Y%2A> est -4. Les valeurs de décalage sont des valeurs négatives, étant donné que l’objet parent est décalé vers par rapport à son objet enfant.  
  
## <a name="see-also"></a>Voir aussi

- <xref:System.Windows.Media.Visual>
- <xref:System.Windows.Media.VisualTreeHelper>
- [Vue d’ensemble du rendu graphique de WPF](wpf-graphics-rendering-overview.md)
