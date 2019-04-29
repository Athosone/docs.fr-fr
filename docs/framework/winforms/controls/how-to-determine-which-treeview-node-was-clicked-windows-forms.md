---
title: 'Procédure : Déterminer le nœud de TreeView cliqué (Windows Forms)'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
- cpp
f1_keywords:
- TreeNode
helpviewer_keywords:
- examples [Windows Forms], TreeView control
- tree nodes in TreeView control [Windows Forms], determining node clicked
- TreeView control [Windows Forms], determining node clicked
ms.assetid: 06a4a191-d918-42af-9f49-956c93eff261
ms.openlocfilehash: 71f13c7b160822c92475d4d03e923b40d4f0454d
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61771044"
---
# <a name="how-to-determine-which-treeview-node-was-clicked-windows-forms"></a><span data-ttu-id="ee989-102">Procédure : Déterminer le nœud de TreeView cliqué (Windows Forms)</span><span class="sxs-lookup"><span data-stu-id="ee989-102">How to: Determine Which TreeView Node Was Clicked (Windows Forms)</span></span>
<span data-ttu-id="ee989-103">Lorsque vous travaillez avec les formulaires Windows <xref:System.Windows.Forms.TreeView> contrôle, une tâche courante consiste à déterminer le nœud sur lequel l’utilisateur a cliqué et réagir de façon appropriée.</span><span class="sxs-lookup"><span data-stu-id="ee989-103">When working with the Windows Forms <xref:System.Windows.Forms.TreeView> control, a common task is to determine which node was clicked, and respond appropriately.</span></span>  
  
### <a name="to-determine-which-treeview-node-was-clicked"></a><span data-ttu-id="ee989-104">Pour déterminer l’utilisateur a cliqué sur le nœud de TreeView</span><span class="sxs-lookup"><span data-stu-id="ee989-104">To determine which TreeView node was clicked</span></span>  
  
1. <span data-ttu-id="ee989-105">Utilisez le <xref:System.EventArgs> objet pour retourner une référence à l’objet de nœud cliqué.</span><span class="sxs-lookup"><span data-stu-id="ee989-105">Use the <xref:System.EventArgs> object to return a reference to the clicked node object.</span></span>  
  
2. <span data-ttu-id="ee989-106">Déterminer le nœud sur lequel l’utilisateur a cliqué en vérifiant la <xref:System.Windows.Forms.TreeViewEventArgs> classe, qui contient les données associées à l’événement.</span><span class="sxs-lookup"><span data-stu-id="ee989-106">Determine which node was clicked by checking the <xref:System.Windows.Forms.TreeViewEventArgs> class, which contains data related to the event.</span></span>  
  
    ```vb  
    Private Sub TreeView1_AfterSelect(ByVal sender As System.Object, _  
    ByVal e As System.Windows.Forms.TreeViewEventArgs) Handles TreeView1.AfterSelect  
       ' Determine by checking the Node property of the TreeViewEventArgs.  
       MessageBox.Show(e.Node.Text)  
    End Sub  
    ```  
  
    ```csharp  
    protected void treeView1_AfterSelect (object sender,   
    System.Windows.Forms.TreeViewEventArgs e)  
    {  
       // Determine by checking the Text property.  
       MessageBox.Show(e.Node.Text);  
    }  
    ```  
  
    ```cpp  
    private:  
       void treeView1_AfterSelect(System::Object ^  sender,  
          System::Windows::Forms::TreeViewEventArgs ^  e)  
       {  
          // Determine by checking the Text property.  
          MessageBox::Show(e->Node->Text);  
       }  
    ```  
  
    > [!NOTE]
    >  <span data-ttu-id="ee989-107">Comme alternative, vous pouvez utiliser la <xref:System.Windows.Forms.MouseEventArgs> de la <xref:System.Windows.Forms.Control.MouseDown> ou <xref:System.Windows.Forms.Control.MouseUp> événement pour obtenir le <xref:System.Drawing.Point.X%2A> et <xref:System.Drawing.Point.Y%2A> coordonner les valeurs de la <xref:System.Drawing.Point> où le clic s’est produite.</span><span class="sxs-lookup"><span data-stu-id="ee989-107">As an alternative, you can use the <xref:System.Windows.Forms.MouseEventArgs> of the <xref:System.Windows.Forms.Control.MouseDown> or <xref:System.Windows.Forms.Control.MouseUp> event to get the <xref:System.Drawing.Point.X%2A> and <xref:System.Drawing.Point.Y%2A> coordinate values of the <xref:System.Drawing.Point> where the click occurred.</span></span> <span data-ttu-id="ee989-108">Ensuite, utilisez le <xref:System.Windows.Forms.TreeView> du contrôle <xref:System.Windows.Forms.TreeView.GetNodeAt%2A> méthode pour déterminer le nœud sur lequel l’utilisateur a cliqué.</span><span class="sxs-lookup"><span data-stu-id="ee989-108">Then, use the <xref:System.Windows.Forms.TreeView> control's <xref:System.Windows.Forms.TreeView.GetNodeAt%2A> method to determine which node was clicked.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="ee989-109">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ee989-109">See also</span></span>

- [<span data-ttu-id="ee989-110">TreeView, contrôle</span><span class="sxs-lookup"><span data-stu-id="ee989-110">TreeView Control</span></span>](treeview-control-windows-forms.md)
