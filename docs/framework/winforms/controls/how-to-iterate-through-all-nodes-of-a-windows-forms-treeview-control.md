---
title: 'Procédure : itérer au sein de tous les nœuds d’un contrôle TreeView Windows Forms'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
- cpp
helpviewer_keywords:
- examples [Windows Forms], TreeView control
- TreeView control [Windows Forms], iterating through nodes
- tree nodes in TreeView control [Windows Forms], iterating through
ms.assetid: 427f8928-ebcf-4beb-887f-695b905d5134
ms.openlocfilehash: 4b287cecddd63ec6535feb70118c3466c8960531
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59314228"
---
# <a name="how-to-iterate-through-all-nodes-of-a-windows-forms-treeview-control"></a>Procédure : itérer au sein de tous les nœuds d’un contrôle TreeView Windows Forms
Il est parfois utile d’examiner chaque nœud dans un formulaire Windows <xref:System.Windows.Forms.TreeView> contrôle afin d’effectuer des calculs sur les valeurs de nœud. Cette opération peut être effectuée à l’aide d’une procédure récursive (méthode récursive en C# et C++) qui procède à une itération au sein de chaque nœud dans chaque collection de l’arborescence.  
  
 Chaque <xref:System.Windows.Forms.TreeNode> objet dans une vue d’arborescence a des propriétés que vous pouvez utiliser pour naviguer l’arborescence : <xref:System.Windows.Forms.TreeNode.FirstNode%2A>, <xref:System.Windows.Forms.TreeNode.LastNode%2A>, <xref:System.Windows.Forms.TreeNode.NextNode%2A>, <xref:System.Windows.Forms.TreeNode.PrevNode%2A>, et <xref:System.Windows.Forms.TreeNode.Parent%2A>. La valeur de la <xref:System.Windows.Forms.TreeNode.Parent%2A> propriété est le nœud parent du nœud actuel. Les nœuds enfants du nœud actuel, le cas échéant, sont répertoriés dans son <xref:System.Windows.Forms.TreeNode.Nodes%2A> propriété. Le <xref:System.Windows.Forms.TreeView> contrôle lui-même a le <xref:System.Windows.Forms.TreeView.TopNode%2A> propriété, qui est le nœud racine de la vue d’ensemble de l’arborescence.  
  
### <a name="to-iterate-through-all-nodes-of-the-treeview-control"></a>Pour procéder à une itération au sein de tous les nœuds d’un contrôle TreeView  
  
1. Créez une procédure récursive (méthode récursive en C# et C++) pour tester chaque nœud.  
  
2. Appelez la procédure.  
  
     L’exemple suivant montre comment imprimer chaque <xref:System.Windows.Forms.TreeNode> l’objet <xref:System.Windows.Forms.TreeNode.Text%2A> propriété :  
  
    ```vb  
    Private Sub PrintRecursive(ByVal n As TreeNode)  
       System.Diagnostics.Debug.WriteLine(n.Text)  
       MessageBox.Show(n.Text)  
       Dim aNode As TreeNode  
       For Each aNode In n.Nodes  
          PrintRecursive(aNode)  
       Next  
    End Sub  
  
    ' Call the procedure using the top nodes of the treeview.  
    Private Sub CallRecursive(ByVal aTreeView As TreeView)  
       Dim n As TreeNode  
       For Each n In aTreeView.Nodes  
          PrintRecursive(n)  
       Next  
    End Sub  
    ```  
  
    ```csharp  
    private void PrintRecursive(TreeNode treeNode)  
    {  
       // Print the node.  
       System.Diagnostics.Debug.WriteLine(treeNode.Text);  
       MessageBox.Show(treeNode.Text);  
       // Print each node recursively.  
       foreach (TreeNode tn in treeNode.Nodes)  
       {  
          PrintRecursive(tn);  
       }  
    }  
  
    // Call the procedure using the TreeView.  
    private void CallRecursive(TreeView treeView)  
    {  
       // Print each node recursively.  
       TreeNodeCollection nodes = treeView.Nodes;  
       foreach (TreeNode n in nodes)  
       {  
          PrintRecursive(n);  
       }  
    }  
    ```  
  
    ```cpp  
    private:  
       void PrintRecursive( TreeNode^ treeNode )  
       {  
          // Print the node.  
          System::Diagnostics::Debug::WriteLine( treeNode->Text );  
          MessageBox::Show( treeNode->Text );  
  
          // Print each node recursively.  
          System::Collections::IEnumerator^ myNodes = (safe_cast<System::Collections::IEnumerable^>(treeNode->Nodes))->GetEnumerator();  
          try  
          {  
             while ( myNodes->MoveNext() )  
             {  
                TreeNode^ tn = safe_cast<TreeNode^>(myNodes->Current);  
                PrintRecursive( tn );  
             }  
          }  
          finally  
          {  
             IDisposable^ disposable = dynamic_cast<System::IDisposable^>(myNodes);  
             if ( disposable != nullptr )  
                      disposable->Dispose();  
          }  
       }  
  
       // Call the procedure using the TreeView.  
       void CallRecursive( TreeView^ treeView )  
       {  
          // Print each node recursively.  
          TreeNodeCollection^ nodes = treeView->Nodes;  
          System::Collections::IEnumerator^ myNodes = (safe_cast<System::Collections::IEnumerable^>(nodes))->GetEnumerator();  
          try  
          {  
             while ( myNodes->MoveNext() )  
             {  
                TreeNode^ n = safe_cast<TreeNode^>(myNodes->Current);  
                PrintRecursive( n );  
             }  
          }  
          finally  
          {  
             IDisposable^ disposable = dynamic_cast<System::IDisposable^>(myNodes);  
             if ( disposable != nullptr )  
                      disposable->Dispose();  
          }  
       }  
    ```  
  
## <a name="see-also"></a>Voir aussi

- [TreeView, contrôle](treeview-control-windows-forms.md)
- [Procédures récursives](~/docs/visual-basic/programming-guide/language-features/procedures/recursive-procedures.md)
