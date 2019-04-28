---
title: 'Procédure : ajouter des détails de ligne à un contrôle DataGrid'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- DataTemplate [WPF], DataGrid
- row details [WPF], DataGrid
- DataGrid [WPF], row details
ms.assetid: 0bdc6f50-9b4c-483f-9df6-a47a1fde998b
ms.openlocfilehash: d5b6539f3d379088528b9654861267988b6fc69b
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61911385"
---
# <a name="how-to-add-row-details-to-a-datagrid-control"></a>Procédure : ajouter des détails de ligne à un contrôle DataGrid
Lorsque vous utilisez le <xref:System.Windows.Controls.DataGrid> contrôle, vous pouvez personnaliser la présentation des données en ajoutant une section de détails de ligne. Ajout d’une section de détails de ligne vous permet de regrouper des données dans un modèle qui est éventuellement visible ou réduit. Par exemple, vous pouvez ajouter des détails de la ligne à un <xref:System.Windows.Controls.DataGrid> qui présente uniquement un résumé des données pour chaque ligne dans le <xref:System.Windows.Controls.DataGrid>, mais présente davantage de champs de données lorsque l’utilisateur sélectionne une ligne. Vous définissez le modèle pour la section de détails de ligne dans le <xref:System.Windows.Controls.DataGrid.RowDetailsTemplate%2A> propriété. L’illustration suivante montre un exemple d’une section de détails de ligne.  
  
 ![DataGrid affiché avec détails des lignes](./media/ndp-rowdetails.png "NDP_RowDetails")  
  
 Vous définissez le modèle de détails de ligne comme XAML inline ou comme une ressource. Les deux approches sont présentées dans les procédures suivantes. Un modèle de données qui est ajouté en tant que ressource peut être utilisé dans le projet sans recréer le modèle. Un modèle de données qui est ajouté en tant qu’inline XAML est uniquement accessible à partir du contrôle où il est défini.  
  
### <a name="to-display-row-details-by-using-inline-xaml"></a>Pour afficher les détails de la ligne à l’aide en ligne XAML  
  
1. Créer un <xref:System.Windows.Controls.DataGrid> qui affiche les données d’une source de données.  
  
2. Dans l'élément <xref:System.Windows.Controls.DataGrid>, ajoutez un élément <xref:System.Windows.Controls.DataGrid.RowDetailsTemplate%2A>.  
  
3. Créer un <xref:System.Windows.DataTemplate> qui définit l’apparence de la section de détails de ligne.  
  
     Le XAML suivant le <xref:System.Windows.Controls.DataGrid> et comment définir le <xref:System.Windows.Controls.DataGrid.RowDetailsTemplate%2A> inline. Le <xref:System.Windows.Controls.DataGrid> affiche trois valeurs dans chaque ligne et trois valeurs plus lorsque la ligne est sélectionnée.  
  
     [!code-xaml[DataGrid_RowDetails#1](~/samples/snippets/csharp/VS_Snippets_Wpf/datagrid_rowdetails/cs/mainwindow.xaml#1)]  
  
     Le code suivant montre la requête qui est utilisée pour sélectionner les données qui s’affiche dans le <xref:System.Windows.Controls.DataGrid>. Dans cet exemple, la requête sélectionne les données à partir d’une entité qui contient des informations sur le client.  
  
     [!code-csharp[DataGrid_RowDetails#2](~/samples/snippets/csharp/VS_Snippets_Wpf/datagrid_rowdetails/cs/mainwindow.xaml.cs#2)]
     [!code-vb[DataGrid_RowDetails#2](~/samples/snippets/visualbasic/VS_Snippets_Wpf/datagrid_rowdetails/vb/mainwindow.xaml.vb#2)]  
  
### <a name="to-display-row-details-by-using-a-resource"></a>Pour afficher les détails de la ligne à l’aide d’une ressource  
  
1. Créer un <xref:System.Windows.Controls.DataGrid> qui affiche les données d’une source de données.  
  
2. Ajouter un <xref:System.Windows.FrameworkElement.Resources%2A> élément à l’élément racine, comme un <xref:System.Windows.Window> contrôle ou un <xref:System.Windows.Controls.Page> contrôler ou ajouter un <xref:System.Windows.Application.Resources%2A> élément à la <xref:System.Windows.Application> classe dans le fichier App.xaml (ou Application.xaml).  
  
3. Dans l’élément de ressources, créez un <xref:System.Windows.DataTemplate> qui définit l’apparence de la section de détails de ligne.  
  
     Le XAML suivant le <xref:System.Windows.Controls.DataGrid.RowDetailsTemplate%2A> définies dans le <xref:System.Windows.Application> classe.  
  
     [!code-xaml[DataGrid_RowDetails#3](~/samples/snippets/csharp/VS_Snippets_Wpf/datagrid_rowdetails/cs/app.xaml#3)]  
  
4. Sur le <xref:System.Windows.DataTemplate>, définissez le [Directive x : Key](../../xaml-services/x-key-directive.md) à une valeur qui identifie de façon unique le modèle de données.  
  
5. Dans le <xref:System.Windows.Controls.DataGrid> élément, définissez le <xref:System.Windows.Controls.DataGrid.RowDetailsTemplate%2A> propriété à la ressource définie dans les étapes précédentes. Affectez à la ressource comme une ressource statique.  
  
     Le XAML suivant le <xref:System.Windows.Controls.DataGrid.RowDetailsTemplate%2A> propriété définie sur la ressource à partir de l’exemple précédent.  
  
     [!code-xaml[DataGrid_RowDetails#4](~/samples/snippets/csharp/VS_Snippets_Wpf/datagrid_rowdetails/cs/window2.xaml#4)]  
  
### <a name="to-set-visibility-and-prevent-horizontal-scrolling-for-row-details"></a>Pour définir la visibilité et empêcher le défilement horizontal pour les détails de la ligne  
  
1. Si nécessaire, définissez la <xref:System.Windows.Controls.DataGrid.RowDetailsVisibilityMode%2A> propriété un <xref:System.Windows.Controls.DataGridRowDetailsVisibilityMode> valeur.  
  
     Par défaut, la valeur est définie <xref:System.Windows.Controls.DataGridRowDetailsVisibilityMode.VisibleWhenSelected>. Vous pouvez le définir sur <xref:System.Windows.Controls.DataGridRowDetailsVisibilityMode.Visible> pour afficher les détails pour toutes les lignes ou <xref:System.Windows.Controls.DataGridRowDetailsVisibilityMode.Collapsed> pour masquer les détails de toutes les lignes.  
  
2. Si nécessaire, définissez la <xref:System.Windows.Controls.DataGrid.AreRowDetailsFrozen%2A> propriété `true` pour empêcher la ligne décrit en détail la section de faire défiler horizontalement.
