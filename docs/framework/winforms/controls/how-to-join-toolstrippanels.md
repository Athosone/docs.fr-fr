---
title: 'Procédure : joindre des contrôles ToolStripPanel'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- toolbars [Windows Forms], joining together
- ToolStripPanel control [Windows Forms], joining together
ms.assetid: 4eadda6d-e3b8-4151-aaf2-a8d564fbe6b3
ms.openlocfilehash: f73c13c4aac1abef70a2ceb0a30c3e46d8664748
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61941100"
---
# <a name="how-to-join-toolstrippanels"></a><span data-ttu-id="6c3e9-102">Procédure : joindre des contrôles ToolStripPanel</span><span class="sxs-lookup"><span data-stu-id="6c3e9-102">How to: Join ToolStripPanels</span></span>
<span data-ttu-id="6c3e9-103">Vous pouvez joindre des contrôles <xref:System.Windows.Forms.ToolStrip> à un <xref:System.Windows.Forms.ToolStripPanel> au moment de l'exécution pour bénéficier de la souplesse des applications MDI (Multiple-Document Interface).</span><span class="sxs-lookup"><span data-stu-id="6c3e9-103">You can join <xref:System.Windows.Forms.ToolStrip> controls to a <xref:System.Windows.Forms.ToolStripPanel> at run time, which provides the flexibility of multiple-document interface (MDI) applications.</span></span>  
  
## <a name="example"></a><span data-ttu-id="6c3e9-104">Exemple</span><span class="sxs-lookup"><span data-stu-id="6c3e9-104">Example</span></span>  
 <span data-ttu-id="6c3e9-105">L'exemple de code suivant montre comment joindre des contrôles <xref:System.Windows.Forms.ToolStrip> à un <xref:System.Windows.Forms.ToolStripPanel>.</span><span class="sxs-lookup"><span data-stu-id="6c3e9-105">The following code example demonstrates how to join <xref:System.Windows.Forms.ToolStrip> controls to a <xref:System.Windows.Forms.ToolStripPanel>.</span></span>  
  
 [!code-csharp[System.Windows.Forms.ToolStrip.Misc#11](~/samples/snippets/csharp/VS_Snippets_Winforms/System.Windows.Forms.ToolStrip.Misc/CS/Program.cs#11)]
 [!code-vb[System.Windows.Forms.ToolStrip.Misc#11](~/samples/snippets/visualbasic/VS_Snippets_Winforms/System.Windows.Forms.ToolStrip.Misc/VB/Program.vb#11)]  
  
## <a name="compiling-the-code"></a><span data-ttu-id="6c3e9-106">Compilation du code</span><span class="sxs-lookup"><span data-stu-id="6c3e9-106">Compiling the Code</span></span>  
 <span data-ttu-id="6c3e9-107">Cet exemple nécessite :</span><span class="sxs-lookup"><span data-stu-id="6c3e9-107">This example requires:</span></span>  
  
- <span data-ttu-id="6c3e9-108">des références aux assemblys System.Design, System.Drawing et System.Windows.Forms.</span><span class="sxs-lookup"><span data-stu-id="6c3e9-108">References to the System.Design, System.Drawing, and System.Windows.Forms assemblies.</span></span>  
  
 <span data-ttu-id="6c3e9-109">Pour plus d’informations sur la création de cet exemple à partir de la ligne de commande pour Visual Basic ou Visual c#, consultez [génération à partir de la ligne de commande](../../../visual-basic/reference/command-line-compiler/building-from-the-command-line.md) ou [de ligne de commande avec csc.exe](../../../csharp/language-reference/compiler-options/command-line-building-with-csc-exe.md).</span><span class="sxs-lookup"><span data-stu-id="6c3e9-109">For information about building this example from the command line for Visual Basic or Visual C#, see [Building from the Command Line](../../../visual-basic/reference/command-line-compiler/building-from-the-command-line.md) or [Command-line Building With csc.exe](../../../csharp/language-reference/compiler-options/command-line-building-with-csc-exe.md).</span></span> <span data-ttu-id="6c3e9-110">Vous pouvez également créer cet exemple dans Visual Studio en collant le code dans un nouveau projet.</span><span class="sxs-lookup"><span data-stu-id="6c3e9-110">You can also build this example in Visual Studio by pasting the code into a new project.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="6c3e9-111">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="6c3e9-111">See also</span></span>

- <xref:System.Windows.Forms.ToolStrip>
- <xref:System.Windows.Forms.ToolStripPanel>
- [<span data-ttu-id="6c3e9-112">Guide pratique pour Utiliser des contrôles ToolStripPanel pour MDI</span><span class="sxs-lookup"><span data-stu-id="6c3e9-112">How to: Use ToolStripPanels for MDI</span></span>](how-to-use-toolstrippanels-for-mdi.md)
