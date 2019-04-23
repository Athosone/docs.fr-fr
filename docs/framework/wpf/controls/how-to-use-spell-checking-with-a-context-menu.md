---
title: 'Procédure : Utiliser la vérification de l’orthographe avec un menu contextuel'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- enabling spell checking in a text box [WPF]
- reenabling spell checking in a text box [WPF]
- spell checking with a context menu [WPF]
ms.assetid: 61f69a20-2ff3-4056-9060-e32f4483ec5e
ms.openlocfilehash: 72b24c386eb99140c9c2729688994b81f92e1a6f
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59192977"
---
# <a name="how-to-use-spell-checking-with-a-context-menu"></a>Procédure : Utiliser la vérification de l’orthographe avec un menu contextuel
Par défaut, lorsque vous activez la vérification orthographique dans un contrôle d’édition telles que <xref:System.Windows.Controls.TextBox> ou <xref:System.Windows.Controls.RichTextBox>, vous obtenez les options de vérification orthographique dans le menu contextuel. Par exemple, les utilisateurs le droit d’un mot mal orthographié, ils obtiennent un ensemble de suggestions orthographiques ou l’option **ignorer tout**. Toutefois, lorsque vous substituez le menu contextuel par défaut avec votre propre menu contextuel personnalisé, cette fonctionnalité est perdue, et vous devez écrire du code pour réactiver la fonctionnalité de vérification orthographique dans le menu contextuel. L’exemple suivant montre comment activer cette fonctionnalité sur un <xref:System.Windows.Controls.TextBox>.  
  
## <a name="example"></a>Exemple  
 L’exemple suivant montre le [!INCLUDE[TLA#tla_xaml](../../../../includes/tlasharptla-xaml-md.md)] qui crée un <xref:System.Windows.Controls.TextBox> avec des événements qui sont utilisées pour implémenter le menu contextuel.  
  
 [!code-xaml[TextBoxMiscSnippets_snip#SpellerCustomContextMenuExampleWholePage](~/samples/snippets/csharp/VS_Snippets_Wpf/TextBoxMiscSnippets_snip/csharp/speller_custom_context_menu.xaml#spellercustomcontextmenuexamplewholepage)]  
  
## <a name="example"></a>Exemple  
 L’exemple suivant montre le code qui implémente le menu contextuel.  
  
 [!code-csharp[TextBoxMiscSnippets_snip#SpellerCustomContextMenuCodeExampleWholePage](~/samples/snippets/csharp/VS_Snippets_Wpf/TextBoxMiscSnippets_snip/csharp/speller_custom_context_menu.xaml.cs#spellercustomcontextmenucodeexamplewholepage)]
 [!code-vb[TextBoxMiscSnippets_snip#SpellerCustomContextMenuCodeExampleWholePage](~/samples/snippets/visualbasic/VS_Snippets_Wpf/TextBoxMiscSnippets_snip/visualbasic/speller_custom_context_menu.xaml.vb#spellercustomcontextmenucodeexamplewholepage)]  
  
 Le code utilisé pour y parvenir avec un <xref:System.Windows.Controls.RichTextBox> est similaire. La différence principale réside dans le paramètre passé à la `GetSpellingError` (méthode). Pour un <xref:System.Windows.Controls.TextBox>, passez à l’index d’entier de la position du signe insertion :  
  
 `spellingError = myTextBox.GetSpellingError(caretIndex);`  
  
 Pour un <xref:System.Windows.Controls.RichTextBox>, transmettez le <xref:System.Windows.Documents.TextPointer> qui spécifie la position du signe insertion :  
  
 `spellingError = myRichTextBox.GetSpellingError(myRichTextBox.CaretPosition);`  
  
## <a name="see-also"></a>Voir aussi

- [Vue d’ensemble de TextBox](textbox-overview.md)
- [Vue d’ensemble de RichTextBox](richtextbox-overview.md)
- [Activer la vérification de l'orthographe dans un contrôle d'édition de texte](how-to-enable-spell-checking-in-a-text-editing-control.md)
- [Utiliser un menu contextuel personnalisé avec un TextBox](how-to-use-a-custom-context-menu-with-a-textbox.md)
