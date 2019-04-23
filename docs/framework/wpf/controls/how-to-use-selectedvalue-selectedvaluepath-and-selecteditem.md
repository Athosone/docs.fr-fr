---
title: 'Procédure : Utiliser SelectedValue, SelectedValuePath et SelectedItem'
ms.date: 03/30/2017
helpviewer_keywords:
- TreeView control [WPF], SelectedValue properties
- Control class [WPF], SelectedItem properties
- Control class [WPF], TreeView properties
- Control class [WPF], SelectedValue properties
- TreeView control [WPF], SelectedItem properties
- SelectedValue [WPF], SelectedValuePath properties
- TreeView control [WPF], SelectedValuePath properties
- Control class [WPF], SelectedValuePath properties
- SelectedValue [WPF], SelectedItem properties
ms.assetid: 2fc92ad4-f02c-4f89-bbe9-d4978a7af0db
ms.openlocfilehash: d9f7a8f04f53b7d38a49dfef2c947dfa1c2d263d
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59169700"
---
# <a name="how-to-use-selectedvalue-selectedvaluepath-and-selecteditem"></a>Procédure : Utiliser SelectedValue, SelectedValuePath et SelectedItem
Cet exemple montre comment utiliser le <xref:System.Windows.Controls.TreeView.SelectedValue%2A> et <xref:System.Windows.Controls.TreeView.SelectedValuePath%2A> propriétés pour spécifier une valeur pour le <xref:System.Windows.Controls.TreeView.SelectedItem%2A> d’un <xref:System.Windows.Controls.TreeView>.  
  
## <a name="example"></a>Exemple  
 Le <xref:System.Windows.Controls.TreeView.SelectedValuePath%2A> propriété offre un moyen de spécifier un <xref:System.Windows.Controls.TreeView.SelectedValue%2A> pour le <xref:System.Windows.Controls.TreeView.SelectedItem%2A> dans un <xref:System.Windows.Controls.TreeView>. Le <xref:System.Windows.Controls.TreeView.SelectedItem%2A> représente un objet dans le <xref:System.Windows.Controls.ItemsControl.Items%2A> collection et le <xref:System.Windows.Controls.TreeView> affiche la valeur d’une propriété unique de l’élément sélectionné. Le <xref:System.Windows.Controls.TreeView.SelectedValuePath%2A> propriété spécifie le chemin d’accès à la propriété qui est utilisée pour déterminer la valeur de la <xref:System.Windows.Controls.TreeView.SelectedValue%2A> propriété. Les exemples de cette rubrique illustrent ce concept.  
  
 L’exemple suivant montre un <xref:System.Windows.Data.XmlDataProvider> qui contient des informations sur les employés.  
  
 [!code-xaml[TreeViewSelectedValue#XMLDataProvider](~/samples/snippets/csharp/VS_Snippets_Wpf/TreeViewSelectedValue/CS/Window1.xaml#xmldataprovider)]  
  
 L’exemple suivant définit un <xref:System.Windows.HierarchicalDataTemplate> qui affiche le `EmployeeName` et `EmployeeWorkDay` de la `Employee`. Notez que le <xref:System.Windows.HierarchicalDataTemplate> ne spécifie pas le `EmployeeNumber` en tant que partie du modèle.  
  
 [!code-xaml[TreeViewSelectedValue#HierarchicalDataTemplate](~/samples/snippets/csharp/VS_Snippets_Wpf/TreeViewSelectedValue/CS/Window1.xaml#hierarchicaldatatemplate)]  
  
 L’exemple suivant montre un <xref:System.Windows.Controls.TreeView> qui utilise défini précédemment <xref:System.Windows.HierarchicalDataTemplate> et qui définit le <xref:System.Windows.Controls.TreeView.SelectedValue%2A> propriété le `EmployeeNumber`. Lorsque vous sélectionnez un `EmployeeName` dans le <xref:System.Windows.Controls.TreeView>, le <xref:System.Windows.Controls.TreeView.SelectedItem%2A> propriété retourne le `EmployeeInfo` élément de données correspondant au `EmployeeName`. Toutefois, étant donné que le <xref:System.Windows.Controls.TreeView.SelectedValuePath%2A> de ce <xref:System.Windows.Controls.TreeView> a la valeur `EmployeeNumber`, le <xref:System.Windows.Controls.TreeView.SelectedValue%2A> est défini sur le `EmployeeNumber`.  
  
 [!code-xaml[TreeViewSelectedValue#SelectedValuePath](~/samples/snippets/csharp/VS_Snippets_Wpf/TreeViewSelectedValue/CS/Window1.xaml#selectedvaluepath)]  
  
## <a name="see-also"></a>Voir aussi

- <xref:System.Windows.Controls.TreeView>
- <xref:System.Windows.Controls.TreeViewItem>
- [Vue d'ensemble de TreeView](treeview-overview.md)
- [Rubriques de guide pratique](treeview-how-to-topics.md)
