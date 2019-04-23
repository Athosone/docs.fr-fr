---
title: 'Procédure : Définir le texte d’un contrôle TextBox'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- text content [WPF], setting
- TextBox control [WPF], setting text content
ms.assetid: bcd25fc7-a52f-4453-b802-2c8d2b335ab8
ms.openlocfilehash: da91e27b804d649f5b8010bc9d7c074425be26f6
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59212191"
---
# <a name="how-to-set-the-text-content-of-a-textbox-control"></a><span data-ttu-id="f95d9-102">Procédure : Définir le texte d’un contrôle TextBox</span><span class="sxs-lookup"><span data-stu-id="f95d9-102">How to: Set the Text Content of a TextBox Control</span></span>
<span data-ttu-id="f95d9-103">Cet exemple montre comment utiliser le <xref:System.Windows.Controls.TextBox.Text%2A> propriété pour définir le texte initial d’un <xref:System.Windows.Controls.TextBox> contrôle.</span><span class="sxs-lookup"><span data-stu-id="f95d9-103">This example shows how to use the <xref:System.Windows.Controls.TextBox.Text%2A> property to set the initial text contents of a <xref:System.Windows.Controls.TextBox> control.</span></span>  
  
 <span data-ttu-id="f95d9-104">**Remarque** bien que le [!INCLUDE[TLA#tla_xaml](../../../../includes/tlasharptla-xaml-md.md)] version de l’exemple peut utiliser le `<TextBox.Text>` balises autour du texte de chaque bouton <xref:System.Windows.Controls.TextBox> contenu, il n’est pas nécessaire, car le <xref:System.Windows.Controls.TextBox> s’applique le <xref:System.Windows.Markup.ContentPropertyAttribute> attribut le <xref:System.Windows.Controls.TextBox.Text%2A> propriété.</span><span class="sxs-lookup"><span data-stu-id="f95d9-104">**Note** Although the [!INCLUDE[TLA#tla_xaml](../../../../includes/tlasharptla-xaml-md.md)] version of the example could use the `<TextBox.Text>` tags around the text of each button's <xref:System.Windows.Controls.TextBox> content, it is not necessary because the <xref:System.Windows.Controls.TextBox> applies the <xref:System.Windows.Markup.ContentPropertyAttribute> attribute to the <xref:System.Windows.Controls.TextBox.Text%2A> property.</span></span> <span data-ttu-id="f95d9-105">Pour plus d’informations, consultez [vue d’ensemble de XAML (WPF)](../advanced/xaml-overview-wpf.md).</span><span class="sxs-lookup"><span data-stu-id="f95d9-105">For more information, see [XAML Overview (WPF)](../advanced/xaml-overview-wpf.md).</span></span>  
  
## <a name="example"></a><span data-ttu-id="f95d9-106">Exemple</span><span class="sxs-lookup"><span data-stu-id="f95d9-106">Example</span></span>  
 [!code-xaml[TextBox_MiscCode#_TextBoxSetTextXAML](~/samples/snippets/csharp/VS_Snippets_Wpf/TextBox_MiscCode/CSharp/Window1.xaml#_textboxsettextxaml)]  
  
## <a name="example"></a><span data-ttu-id="f95d9-107">Exemple</span><span class="sxs-lookup"><span data-stu-id="f95d9-107">Example</span></span>  
 [!code-csharp[TextBox_MiscCode#_TextBoxSetText](~/samples/snippets/csharp/VS_Snippets_Wpf/TextBox_MiscCode/CSharp/Window1.xaml.cs#_textboxsettext)]
 [!code-vb[TextBox_MiscCode#_TextBoxSetText](~/samples/snippets/visualbasic/VS_Snippets_Wpf/TextBox_MiscCode/VisualBasic/Window1.xaml.vb#_textboxsettext)]  
  
## <a name="see-also"></a><span data-ttu-id="f95d9-108">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f95d9-108">See also</span></span>

- [<span data-ttu-id="f95d9-109">Vue d’ensemble de TextBox</span><span class="sxs-lookup"><span data-stu-id="f95d9-109">TextBox Overview</span></span>](textbox-overview.md)
- [<span data-ttu-id="f95d9-110">Vue d’ensemble de RichTextBox</span><span class="sxs-lookup"><span data-stu-id="f95d9-110">RichTextBox Overview</span></span>](richtextbox-overview.md)
