---
title: 'Procédure : Créer un Expander avec un ScrollViewer'
ms.date: 03/30/2017
helpviewer_keywords:
- controls [WPF], Expander
- ScrollViewer control [WPF], with Expander control
- Expander control [WPF], creating
- controls [WPF], ScrollViewer
ms.assetid: 2ad124d2-2406-4157-aaf2-64e067298f01
ms.openlocfilehash: ef0bc5d344f7d465de9209708430d3e61d40d4f7
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61910791"
---
# <a name="how-to-create-an-expander-with-a-scrollviewer"></a>Procédure : Créer un Expander avec un ScrollViewer
Cet exemple montre comment créer un <xref:System.Windows.Controls.Expander> contrôle qui contient un contenu complexe, comme une image et le texte. L’exemple joint également le contenu de la <xref:System.Windows.Controls.Expander> dans un <xref:System.Windows.Controls.ScrollViewer> contrôle.  
  
## <a name="example"></a>Exemple  
 L’exemple suivant montre comment créer un <xref:System.Windows.Controls.Expander>. L’exemple utilise un <xref:System.Windows.Controls.Primitives.BulletDecorator> contrôle, qui contient une image et du texte, afin de définir le <xref:System.Windows.Controls.HeaderedContentControl.Header%2A>. Un <xref:System.Windows.Controls.ScrollViewer> contrôle fournit une méthode pour faire défiler le contenu développé.  
  
 Notez que l’exemple définit le <xref:System.Windows.FrameworkElement.Height%2A> propriété sur le <xref:System.Windows.Controls.ScrollViewer> au lieu de sur le contenu. Si le <xref:System.Windows.FrameworkElement.Height%2A> est défini sur le contenu, le <xref:System.Windows.Controls.ScrollViewer> n’autorise pas l’utilisateur à faire défiler le contenu. Le <xref:System.Windows.FrameworkElement.Width%2A> propriété est définie sur le <xref:System.Windows.Controls.Expander> contrôle et si ce paramètre s’applique à la <xref:System.Windows.Controls.HeaderedContentControl.Header%2A> et le contenu développé.  
  
 [!code-xaml[ExpanderRichContent#CreateExpander](~/samples/snippets/csharp/VS_Snippets_Wpf/ExpanderRichContent/CSharp/Window1.xaml#createexpander)]  
  
 [!code-csharp[ExpanderRichContent#CreateExpanderCode](~/samples/snippets/csharp/VS_Snippets_Wpf/ExpanderRichContent/CSharp/Window1.xaml.cs#createexpandercode)]  
  
## <a name="see-also"></a>Voir aussi

- <xref:System.Windows.Controls.Expander>
- [Vue d'ensemble de l'Expandeur](expander-overview.md)
- [Rubriques de guide pratique](expander-how-to-topics.md)
