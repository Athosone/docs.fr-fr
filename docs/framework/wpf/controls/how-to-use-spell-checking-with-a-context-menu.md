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
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61699147"
---
# <a name="how-to-use-spell-checking-with-a-context-menu"></a><span data-ttu-id="cad8f-102">Procédure : Utiliser la vérification de l’orthographe avec un menu contextuel</span><span class="sxs-lookup"><span data-stu-id="cad8f-102">How to: Use Spell Checking with a Context Menu</span></span>
<span data-ttu-id="cad8f-103">Par défaut, lorsque vous activez la vérification orthographique dans un contrôle d’édition telles que <xref:System.Windows.Controls.TextBox> ou <xref:System.Windows.Controls.RichTextBox>, vous obtenez les options de vérification orthographique dans le menu contextuel.</span><span class="sxs-lookup"><span data-stu-id="cad8f-103">By default, when you enable spell checking in an editing control like <xref:System.Windows.Controls.TextBox> or <xref:System.Windows.Controls.RichTextBox>, you get spell-checking choices in the context menu.</span></span> <span data-ttu-id="cad8f-104">Par exemple, les utilisateurs le droit d’un mot mal orthographié, ils obtiennent un ensemble de suggestions orthographiques ou l’option **ignorer tout**.</span><span class="sxs-lookup"><span data-stu-id="cad8f-104">For example, when users right-click a misspelled word, they get a set of spelling suggestions or the option to **Ignore All**.</span></span> <span data-ttu-id="cad8f-105">Toutefois, lorsque vous substituez le menu contextuel par défaut avec votre propre menu contextuel personnalisé, cette fonctionnalité est perdue, et vous devez écrire du code pour réactiver la fonctionnalité de vérification orthographique dans le menu contextuel.</span><span class="sxs-lookup"><span data-stu-id="cad8f-105">However, when you override the default context menu with your own custom context menu, this functionality is lost, and you need to write code to reenable the spell-checking feature in the context menu.</span></span> <span data-ttu-id="cad8f-106">L’exemple suivant montre comment activer cette fonctionnalité sur un <xref:System.Windows.Controls.TextBox>.</span><span class="sxs-lookup"><span data-stu-id="cad8f-106">The following example shows how to enable this on a <xref:System.Windows.Controls.TextBox>.</span></span>  
  
## <a name="example"></a><span data-ttu-id="cad8f-107">Exemple</span><span class="sxs-lookup"><span data-stu-id="cad8f-107">Example</span></span>  
 <span data-ttu-id="cad8f-108">L’exemple suivant montre le [!INCLUDE[TLA#tla_xaml](../../../../includes/tlasharptla-xaml-md.md)] qui crée un <xref:System.Windows.Controls.TextBox> avec des événements qui sont utilisées pour implémenter le menu contextuel.</span><span class="sxs-lookup"><span data-stu-id="cad8f-108">The following example shows the [!INCLUDE[TLA#tla_xaml](../../../../includes/tlasharptla-xaml-md.md)] that creates a <xref:System.Windows.Controls.TextBox> with some events that are used to implement the context menu.</span></span>  
  
 [!code-xaml[TextBoxMiscSnippets_snip#SpellerCustomContextMenuExampleWholePage](~/samples/snippets/csharp/VS_Snippets_Wpf/TextBoxMiscSnippets_snip/csharp/speller_custom_context_menu.xaml#spellercustomcontextmenuexamplewholepage)]  
  
## <a name="example"></a><span data-ttu-id="cad8f-109">Exemple</span><span class="sxs-lookup"><span data-stu-id="cad8f-109">Example</span></span>  
 <span data-ttu-id="cad8f-110">L’exemple suivant montre le code qui implémente le menu contextuel.</span><span class="sxs-lookup"><span data-stu-id="cad8f-110">The following example shows the code that implements the context menu.</span></span>  
  
 [!code-csharp[TextBoxMiscSnippets_snip#SpellerCustomContextMenuCodeExampleWholePage](~/samples/snippets/csharp/VS_Snippets_Wpf/TextBoxMiscSnippets_snip/csharp/speller_custom_context_menu.xaml.cs#spellercustomcontextmenucodeexamplewholepage)]
 [!code-vb[TextBoxMiscSnippets_snip#SpellerCustomContextMenuCodeExampleWholePage](~/samples/snippets/visualbasic/VS_Snippets_Wpf/TextBoxMiscSnippets_snip/visualbasic/speller_custom_context_menu.xaml.vb#spellercustomcontextmenucodeexamplewholepage)]  
  
 <span data-ttu-id="cad8f-111">Le code utilisé pour y parvenir avec un <xref:System.Windows.Controls.RichTextBox> est similaire.</span><span class="sxs-lookup"><span data-stu-id="cad8f-111">The code used for doing this with a <xref:System.Windows.Controls.RichTextBox> is similar.</span></span> <span data-ttu-id="cad8f-112">La différence principale réside dans le paramètre passé à la `GetSpellingError` (méthode).</span><span class="sxs-lookup"><span data-stu-id="cad8f-112">The main difference is in the parameter passed to the `GetSpellingError` method.</span></span> <span data-ttu-id="cad8f-113">Pour un <xref:System.Windows.Controls.TextBox>, passez à l’index d’entier de la position du signe insertion :</span><span class="sxs-lookup"><span data-stu-id="cad8f-113">For a <xref:System.Windows.Controls.TextBox>, pass the integer index of the caret position:</span></span>  
  
 `spellingError = myTextBox.GetSpellingError(caretIndex);`  
  
 <span data-ttu-id="cad8f-114">Pour un <xref:System.Windows.Controls.RichTextBox>, transmettez le <xref:System.Windows.Documents.TextPointer> qui spécifie la position du signe insertion :</span><span class="sxs-lookup"><span data-stu-id="cad8f-114">For a <xref:System.Windows.Controls.RichTextBox>, pass the <xref:System.Windows.Documents.TextPointer> that specifies the caret position:</span></span>  
  
 `spellingError = myRichTextBox.GetSpellingError(myRichTextBox.CaretPosition);`  
  
## <a name="see-also"></a><span data-ttu-id="cad8f-115">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="cad8f-115">See also</span></span>

- [<span data-ttu-id="cad8f-116">Vue d’ensemble de TextBox</span><span class="sxs-lookup"><span data-stu-id="cad8f-116">TextBox Overview</span></span>](textbox-overview.md)
- [<span data-ttu-id="cad8f-117">Vue d’ensemble de RichTextBox</span><span class="sxs-lookup"><span data-stu-id="cad8f-117">RichTextBox Overview</span></span>](richtextbox-overview.md)
- [<span data-ttu-id="cad8f-118">Activer la vérification de l'orthographe dans un contrôle d'édition de texte</span><span class="sxs-lookup"><span data-stu-id="cad8f-118">Enable Spell Checking in a Text Editing Control</span></span>](how-to-enable-spell-checking-in-a-text-editing-control.md)
- [<span data-ttu-id="cad8f-119">Utiliser un menu contextuel personnalisé avec un TextBox</span><span class="sxs-lookup"><span data-stu-id="cad8f-119">Use a Custom Context Menu with a TextBox</span></span>](how-to-use-a-custom-context-menu-with-a-textbox.md)
