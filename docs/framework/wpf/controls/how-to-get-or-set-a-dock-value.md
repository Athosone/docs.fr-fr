---
title: 'Procédure : Obtenir ou définir une valeur Dock'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- Dock values [WPF], setting
- Dock values [WPF], getting
ms.assetid: fcf4ab8a-c7cd-4835-8d04-de1c999ab4a8
ms.openlocfilehash: fb6c8a7d62aa09a6e1d82cb4079d1425a7f39f8c
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59160731"
---
# <a name="how-to-get-or-set-a-dock-value"></a>Procédure : Obtenir ou définir une valeur Dock
L’exemple suivant montre comment affecter un <xref:System.Windows.Controls.Dock> valeur pour un objet. L’exemple utilise le <xref:System.Windows.Controls.DockPanel.GetDock%2A> et <xref:System.Windows.Controls.DockPanel.SetDock%2A> méthodes de <xref:System.Windows.Controls.DockPanel>.  
  
## <a name="example"></a>Exemple  
 L’exemple crée une instance de la <xref:System.Windows.Controls.TextBlock> élément, `txt1`et attribue un <xref:System.Windows.Controls.Dock> valeur `Top` à l’aide de la <xref:System.Windows.Controls.DockPanel.SetDock%2A> méthode de <xref:System.Windows.Controls.DockPanel>. Il ajoute ensuite la valeur de la <xref:System.Windows.Controls.Dock> propriété le <xref:System.Windows.Controls.TextBlock.Text%2A> de la <xref:System.Windows.Controls.TextBlock> élément à l’aide de la <xref:System.Windows.Controls.DockPanel.GetDock%2A> (méthode). Enfin, l’exemple ajoute le <xref:System.Windows.Controls.TextBlock> élément au parent <xref:System.Windows.Controls.DockPanel>, `dp1`.  
  
 [!code-csharp[DockPanelSetDock#1](~/samples/snippets/csharp/VS_Snippets_Wpf/DockPanelSetDock/CSharp/DockPanel_SetDock.cs#1)]
 [!code-vb[DockPanelSetDock#1](~/samples/snippets/visualbasic/VS_Snippets_Wpf/DockPanelSetDock/VisualBasic/DockPanel_SetDock.vb#1)]  
  
## <a name="see-also"></a>Voir aussi

- <xref:System.Windows.Controls.DockPanel>
- <xref:System.Windows.Controls.DockPanel.GetDock%2A>
- <xref:System.Windows.Controls.DockPanel.SetDock%2A>
- [Vue d’ensemble de Panel](panels-overview.md)
