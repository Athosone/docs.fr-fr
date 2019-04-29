---
title: 'Procédure : Modifier la propriété TextWrapping par programmation'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- documents [WPF], changing TextWrapping property programmatically
- TextWrapping property [WPF], changing programmatically
ms.assetid: 30d25554-4c82-4df9-a8d6-35683a4a13bb
ms.openlocfilehash: 21ca31d24121492fe6927cd533d5b3c0785b5a28
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61776660"
---
# <a name="how-to-change-the-textwrapping-property-programmatically"></a>Procédure : Modifier la propriété TextWrapping par programmation
## <a name="example"></a>Exemple  
 L’exemple de code suivant montre comment modifier la valeur de la <xref:System.Windows.Controls.TextBlock.TextWrapping%2A> propriété par programmation.  
  
 Trois <xref:System.Windows.Controls.Button> éléments sont placés dans un <xref:System.Windows.Controls.StackPanel> élément [!INCLUDE[TLA2#tla_xaml](../../../../includes/tla2sharptla-xaml-md.md)]. Chaque <xref:System.Windows.Controls.Primitives.ButtonBase.Click> événement pour un <xref:System.Windows.Controls.Button> correspond à un gestionnaire d’événements dans le code. Les gestionnaires d’événements utilisent le même nom que le <xref:System.Windows.Controls.TextBlock.TextWrapping%2A> valeur elles s’appliquent à `txt2` lorsque le bouton est activé. En outre, le texte dans `txt1` (un <xref:System.Windows.Controls.TextBlock> ne pas indiqué dans le [!INCLUDE[TLA2#tla_xaml](../../../../includes/tla2sharptla-xaml-md.md)]) est mis à jour pour refléter les modifications de la propriété.  
  
 [!code-xaml[TextWrapProperty#1](~/samples/snippets/visualbasic/VS_Snippets_Wpf/TextWrapProperty/VisualBasic/Pane1.xaml#1)]  
  
 [!code-csharp[TextWrapProperty#2](~/samples/snippets/csharp/VS_Snippets_Wpf/TextWrapProperty/CSharp/Window1.xaml.cs#2)]
 [!code-vb[TextWrapProperty#2](~/samples/snippets/visualbasic/VS_Snippets_Wpf/TextWrapProperty/VisualBasic/Pane1.xaml.vb#2)]  
  
## <a name="see-also"></a>Voir aussi

- <xref:System.Windows.Controls.TextBlock.TextWrapping%2A>
- <xref:System.Windows.TextWrapping>
