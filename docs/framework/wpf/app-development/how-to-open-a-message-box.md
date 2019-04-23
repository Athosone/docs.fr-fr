---
title: 'Procédure : Ouvrir une boîte de message'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- message boxes [WPF], opening
- opening message boxes [WPF]
ms.assetid: acaad17f-af43-4eca-a004-f1c9e7c6f292
ms.openlocfilehash: cf7534cdee5e17d53e95294573023d660135e395
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59101105"
---
# <a name="how-to-open-a-message-box"></a><span data-ttu-id="bac93-102">Procédure : Ouvrir une boîte de message</span><span class="sxs-lookup"><span data-stu-id="bac93-102">How to: Open a Message Box</span></span>
<span data-ttu-id="bac93-103">Cet exemple montre comment ouvrir une boîte de message.</span><span class="sxs-lookup"><span data-stu-id="bac93-103">This example shows how to open a message box.</span></span>  
  
## <a name="example"></a><span data-ttu-id="bac93-104">Exemple</span><span class="sxs-lookup"><span data-stu-id="bac93-104">Example</span></span>  
 <span data-ttu-id="bac93-105">Une boîte de message est une boîte de dialogue modale préfabriquée pour afficher des informations pour les utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="bac93-105">A message box is a prefabricated modal dialog box for displaying information to users.</span></span> <span data-ttu-id="bac93-106">Une boîte de message est ouverte en appelant la méthode statique <xref:System.Windows.MessageBox.Show%2A> méthode de la <xref:System.Windows.MessageBox> classe.</span><span class="sxs-lookup"><span data-stu-id="bac93-106">A message box is opened by calling the static <xref:System.Windows.MessageBox.Show%2A> method of the <xref:System.Windows.MessageBox> class.</span></span> <span data-ttu-id="bac93-107">Lorsque <xref:System.Windows.MessageBox.Show%2A> est appelée, le message est passé à l’aide d’un paramètre de chaîne.</span><span class="sxs-lookup"><span data-stu-id="bac93-107">When <xref:System.Windows.MessageBox.Show%2A> is called, the message is passed using a string parameter.</span></span> <span data-ttu-id="bac93-108">Plusieurs surcharges de <xref:System.Windows.MessageBox.Show%2A> vous permettent de configurer l’apparence d’une boîte de message (voir <xref:System.Windows.MessageBox>).</span><span class="sxs-lookup"><span data-stu-id="bac93-108">Several overloads of <xref:System.Windows.MessageBox.Show%2A> allow you to configure how a message box will appear (see <xref:System.Windows.MessageBox>).</span></span>  
  
 [!code-csharp[MessageBoxSnippets#MessageBoxShow1CODE](~/samples/snippets/csharp/VS_Snippets_Wpf/MessageBoxSnippets/CSharp/Show1Window.xaml.cs#messageboxshow1code)]
 [!code-vb[MessageBoxSnippets#MessageBoxShow1CODE](~/samples/snippets/visualbasic/VS_Snippets_Wpf/MessageBoxSnippets/visualbasic/show1window.xaml.vb#messageboxshow1code)]  
  
## <a name="see-also"></a><span data-ttu-id="bac93-109">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="bac93-109">See also</span></span>

- [<span data-ttu-id="bac93-110">MessageBox, exemple</span><span class="sxs-lookup"><span data-stu-id="bac93-110">MessageBox Sample</span></span>](https://go.microsoft.com/fwlink/?LinkID=160023)
