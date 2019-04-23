---
title: 'Procédure : Gérer l’événement ScrollChanged'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- ScrollViewer control [WPF], raising ScrollChanged events
- ScrollChanged events [WPF]
ms.assetid: 42c695d8-ee28-49d4-80fd-fc71e9be7f29
ms.openlocfilehash: 54f20a4b8c6e6fcc190257fcf5de4374415d68b4
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/22/2019
ms.locfileid: "59974160"
---
# <a name="how-to-handle-the-scrollchanged-event"></a>Procédure : Gérer l’événement ScrollChanged
## <a name="example"></a>Exemple  
 Cet exemple montre comment gérer les <xref:System.Windows.Controls.ScrollViewer.ScrollChanged> événement d’un <xref:System.Windows.Controls.ScrollViewer>.  
  
 Un <xref:System.Windows.Documents.FlowDocument> élément avec <xref:System.Windows.Documents.Paragraph> parties est défini dans [!INCLUDE[TLA2#tla_xaml](../../../../includes/tla2sharptla-xaml-md.md)]. Lorsque le <xref:System.Windows.Controls.ScrollViewer.ScrollChanged> événement se produit en raison de l’interaction de l’utilisateur, un gestionnaire est appelé, et le texte est écrit pour un <xref:System.Windows.Controls.TextBlock> indiquant que l’événement s’est produite.  
  
 [!code-xaml[scrollchangedeventargsLayout#1](~/samples/snippets/csharp/VS_Snippets_Wpf/scrollchangedeventargsLayout/CSharp/Window1.xaml#1)]  
[!code-xaml[scrollchangedeventargsLayout#2](~/samples/snippets/csharp/VS_Snippets_Wpf/scrollchangedeventargsLayout/CSharp/Window1.xaml#2)]  
  
 [!code-csharp[scrollchangedeventargsLayout#3](~/samples/snippets/csharp/VS_Snippets_Wpf/scrollchangedeventargsLayout/CSharp/Window1.xaml.cs#3)]
 [!code-vb[scrollchangedeventargsLayout#3](~/samples/snippets/visualbasic/VS_Snippets_Wpf/scrollchangedeventargsLayout/VisualBasic/Window1.xaml.vb#3)]  
  
## <a name="see-also"></a>Voir aussi

- <xref:System.Windows.Controls.ScrollViewer>
- <xref:System.Windows.Controls.ScrollViewer.ScrollChanged>
- <xref:System.Windows.Controls.ScrollChangedEventHandler>
- <xref:System.Windows.Controls.ScrollChangedEventArgs>
