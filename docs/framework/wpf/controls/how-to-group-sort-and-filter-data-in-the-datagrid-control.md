---
title: 'Procédure : Regrouper, trier et filtrer les données dans le contrôle DataGrid'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- DataGrid [WPF], sort
- DataGrid [WPF], group
- DataGrid [WPF], filter
ms.assetid: 03345e85-89e3-4aec-9ed0-3b80759df770
ms.openlocfilehash: 81fdb0a6d5602f612c55d7e790ca9a0fe56c144e
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61771099"
---
# <a name="how-to-group-sort-and-filter-data-in-the-datagrid-control"></a>Procédure : Regrouper, trier et filtrer les données dans le contrôle DataGrid

Il est souvent utile d’afficher des données dans un <xref:System.Windows.Controls.DataGrid> de différentes façons par regroupement, le tri et filtrage des données. Pour regrouper, trier et filtrer les données dans un <xref:System.Windows.Controls.DataGrid>, liez-le à une <xref:System.Windows.Data.CollectionView> qui prend en charge ces fonctions. Vous pouvez ensuite travailler avec les données dans le <xref:System.Windows.Data.CollectionView> sans affecter les données sous-jacentes de la source. Les modifications dans la vue de collection sont répercutées dans le <xref:System.Windows.Controls.DataGrid> l’interface utilisateur (IU).

Le <xref:System.Windows.Data.CollectionView> classe fournit le regroupement et tri des fonctionnalités pour une source de données qui implémente le <xref:System.Collections.IEnumerable> interface. Le <xref:System.Windows.Data.CollectionViewSource> classe vous permet de définir les propriétés d’un <xref:System.Windows.Data.CollectionView> à partir de XAML.

Dans cet exemple, une collection de `Task` objets est lié à un <xref:System.Windows.Data.CollectionViewSource>. Le <xref:System.Windows.Data.CollectionViewSource> est utilisé comme le <xref:System.Windows.Controls.ItemsControl.ItemsSource%2A> pour le <xref:System.Windows.Controls.DataGrid>. Regroupement, le tri et filtrage sont effectuées sur le <xref:System.Windows.Data.CollectionViewSource> et s’affichent dans le <xref:System.Windows.Controls.DataGrid> l’interface utilisateur.

![Données groupées dans un DataGrid](././media/wpf-datagridgroups.png "WPF_DataGridGroups") des données groupées dans un contrôle DataGrid

## <a name="using-a-collectionviewsource-as-an-itemssource"></a>À l’aide d’un élément CollectionViewSource comme un ItemsSource

Pour grouper, trier et filtrer des données dans un <xref:System.Windows.Controls.DataGrid> contrôle, vous liez le <xref:System.Windows.Controls.DataGrid> à un <xref:System.Windows.Data.CollectionView> qui prend en charge ces fonctions. Dans cet exemple, le <xref:System.Windows.Controls.DataGrid> est lié à un <xref:System.Windows.Data.CollectionViewSource> qui fournit ces fonctions pour un <xref:System.Collections.Generic.List%601> de `Task` objets.

### <a name="to-bind-a-datagrid-to-a-collectionviewsource"></a>Pour lier un contrôle DataGrid à un élément CollectionViewSource

1. Créer une collection de données qui implémente le <xref:System.Collections.IEnumerable> interface.

    Si vous utilisez <xref:System.Collections.Generic.List%601> pour créer votre collection, vous devez créer une nouvelle classe qui hérite de <xref:System.Collections.Generic.List%601> au lieu d’instancier une instance de <xref:System.Collections.Generic.List%601>. Cela vous permet de lier les données à la collection dans XAML.

    > [!NOTE]
    > Les objets dans la collection doivent implémenter le <xref:System.ComponentModel.INotifyPropertyChanged> interface modifiée et le <xref:System.ComponentModel.IEditableObject> interface afin que le <xref:System.Windows.Controls.DataGrid> pour répondre correctement aux modifications apportées aux propriétés et les modifications. Pour plus d’informations, consultez [Implémenter la notification des modifications de propriétés](../data/how-to-implement-property-change-notification.md).

    [!code-csharp[DataGrid_GroupSortFilter#101](~/samples/snippets/csharp/VS_Snippets_Wpf/DataGrid_GroupSortFilter/CS/MainWindow.xaml.cs#101)]
    [!code-vb[DataGrid_GroupSortFilter#101](~/samples/snippets/visualbasic/VS_Snippets_Wpf/DataGrid_GroupSortFilter/VB/MainWindow.xaml.vb#101)]

2. Dans XAML, créez une instance de la classe de collection et définissez la [Directive x : Key](../../xaml-services/x-key-directive.md).

3. Dans XAML, créez une instance de la <xref:System.Windows.Data.CollectionViewSource> classe, définissez la [Directive x : Key](../../xaml-services/x-key-directive.md)et définir l’instance de votre classe de collection en tant que le <xref:System.Windows.Data.CollectionViewSource.Source%2A>.

    [!code-xaml[DataGrid_GroupSortFilter#201](~/samples/snippets/csharp/VS_Snippets_Wpf/DataGrid_GroupSortFilter/CS/WindowSnips1.xaml#201)]

4. Créez une instance de la <xref:System.Windows.Controls.DataGrid> , puis définissez le <xref:System.Windows.Controls.ItemsControl.ItemsSource%2A> propriété le <xref:System.Windows.Data.CollectionViewSource>.

    [!code-xaml[DataGrid_GroupSortFilter#002](~/samples/snippets/csharp/VS_Snippets_Wpf/DataGrid_GroupSortFilter/CS/MainWindow.xaml#002)]

5. Pour accéder à la <xref:System.Windows.Data.CollectionViewSource> à partir de votre code, utilisez le <xref:System.Windows.Data.CollectionViewSource.GetDefaultView%2A> méthode pour obtenir une référence à la <xref:System.Windows.Data.CollectionViewSource>.

    [!code-csharp[DataGrid_GroupSortFilter#102](~/samples/snippets/csharp/VS_Snippets_Wpf/DataGrid_GroupSortFilter/CS/MainWindow.xaml.cs#102)]
    [!code-vb[DataGrid_GroupSortFilter#102](~/samples/snippets/visualbasic/VS_Snippets_Wpf/DataGrid_GroupSortFilter/VB/MainWindow.xaml.vb#102)]

## <a name="grouping-items-in-a-datagrid"></a>Regrouper des éléments dans un contrôle DataGrid

Pour spécifier la façon dont les éléments sont regroupés dans un <xref:System.Windows.Controls.DataGrid>, vous utilisez le <xref:System.Windows.Data.PropertyGroupDescription> type pour regrouper les éléments dans la vue de source.

### <a name="to-group-items-in-a-datagrid-using-xaml"></a>Pour regrouper des éléments dans une grille de données à l’aide de XAML

1. Créer un <xref:System.Windows.Data.PropertyGroupDescription> qui spécifie la propriété à group by. Vous pouvez spécifier la propriété dans XAML ou dans le code.

   1. Dans XAML, définissez le <xref:System.Windows.Data.PropertyGroupDescription.PropertyName%2A> au nom de la propriété à grouper par.

   2. Dans le code, passez le nom de la propriété au groupe par le constructeur.

2. Ajouter le <xref:System.Windows.Data.PropertyGroupDescription> à la <xref:System.Windows.Data.CollectionViewSource.GroupDescriptions%2A?displayProperty=nameWithType> collection.

3. Ajouter des instances supplémentaires de <xref:System.Windows.Data.PropertyGroupDescription> à la <xref:System.Windows.Data.CollectionViewSource.GroupDescriptions%2A> collection à ajouter davantage de niveaux de regroupement.

    [!code-xaml[DataGrid_GroupSortFilter#012](~/samples/snippets/csharp/VS_Snippets_Wpf/DataGrid_GroupSortFilter/CS/MainWindow.xaml#012)]
    [!code-csharp[DataGrid_GroupSortFilter#112](~/samples/snippets/csharp/VS_Snippets_Wpf/DataGrid_GroupSortFilter/CS/MainWindow.xaml.cs#112)]
    [!code-vb[DataGrid_GroupSortFilter#112](~/samples/snippets/visualbasic/VS_Snippets_Wpf/DataGrid_GroupSortFilter/VB/MainWindow.xaml.vb#112)]

4. Pour supprimer un groupe, supprimez le <xref:System.Windows.Data.PropertyGroupDescription> à partir de la <xref:System.Windows.Data.CollectionViewSource.GroupDescriptions%2A> collection.

5. Pour supprimer tous les groupes, appelez le <xref:System.Collections.ObjectModel.Collection%601.Clear%2A> méthode de la <xref:System.Windows.Data.CollectionViewSource.GroupDescriptions%2A> collection.

    [!code-csharp[DataGrid_GroupSortFilter#114](~/samples/snippets/csharp/VS_Snippets_Wpf/DataGrid_GroupSortFilter/CS/MainWindow.xaml.cs#114)]
    [!code-vb[DataGrid_GroupSortFilter#114](~/samples/snippets/visualbasic/VS_Snippets_Wpf/DataGrid_GroupSortFilter/VB/MainWindow.xaml.vb#114)]

Lorsque les éléments sont regroupés dans le <xref:System.Windows.Controls.DataGrid>, vous pouvez définir un <xref:System.Windows.Controls.GroupStyle> qui spécifie l’apparence de chaque groupe. Vous appliquez le <xref:System.Windows.Controls.GroupStyle> en l’ajoutant à la <xref:System.Windows.Controls.ItemsControl.GroupStyle%2A> collection du contrôle DataGrid. Si vous avez plusieurs niveaux de regroupement, vous pouvez appliquer des styles différents à chaque niveau de groupe. Styles sont appliqués dans l’ordre dans lequel ils sont définis. Par exemple, si vous définissez deux styles, la première sera appliquée aux groupes de ligne de niveau supérieur. Le deuxième style sera appliqué à tous les groupes de lignes au deuxième niveau et versions antérieures. Le <xref:System.Windows.FrameworkElement.DataContext%2A> de la <xref:System.Windows.Controls.GroupStyle> est le <xref:System.Windows.Data.CollectionViewGroup> qui représente le groupe.

### <a name="to-change-the-appearance-of-row-group-headers"></a>Pour modifier l’apparence des en-têtes de groupe de lignes

1. Créer un <xref:System.Windows.Controls.GroupStyle> qui définit l’apparence du groupe de lignes.

2. Placez le <xref:System.Windows.Controls.GroupStyle> à l’intérieur de la `<DataGrid.GroupStyle>` balises.

    [!code-xaml[DataGrid_GroupSortFilter#003](~/samples/snippets/csharp/VS_Snippets_Wpf/DataGrid_GroupSortFilter/CS/MainWindow.xaml#003)]

## <a name="sorting-items-in-a-datagrid"></a>Tri des éléments dans un contrôle DataGrid

Pour spécifier la façon dont les éléments sont triés dans un <xref:System.Windows.Controls.DataGrid>, vous utilisez le <xref:System.ComponentModel.SortDescription> type pour trier les éléments dans la vue de source.

### <a name="to-sort-items-in-a-datagrid"></a>Pour trier les éléments dans un contrôle DataGrid

1. Créer un <xref:System.ComponentModel.SortDescription> qui spécifie la propriété par laquelle trier. Vous pouvez spécifier la propriété dans XAML ou dans le code.

    1. Dans XAML, définissez le <xref:System.ComponentModel.SortDescription.PropertyName%2A> sur le nom de la propriété par laquelle trier.

    2. Dans le code, passez le nom de la propriété par laquelle trier et le <xref:System.ComponentModel.ListSortDirection> au constructeur.

2. Ajouter le <xref:System.ComponentModel.SortDescription> à la <xref:System.Windows.Data.CollectionViewSource.SortDescriptions%2A?displayProperty=nameWithType> collection.

3. Ajouter des instances supplémentaires de <xref:System.ComponentModel.SortDescription> à la <xref:System.Windows.Data.CollectionViewSource.SortDescriptions%2A> collection pour trier en fonction des propriétés supplémentaires.

    [!code-xaml[DataGrid_GroupSortFilter#011](~/samples/snippets/csharp/VS_Snippets_Wpf/DataGrid_GroupSortFilter/CS/MainWindow.xaml#011)]
    [!code-csharp[DataGrid_GroupSortFilter#211](~/samples/snippets/csharp/VS_Snippets_Wpf/DataGrid_GroupSortFilter/CS/WindowSnips1.xaml.cs#211)]
    [!code-vb[DataGrid_GroupSortFilter#211](~/samples/snippets/visualbasic/VS_Snippets_Wpf/DataGrid_GroupSortFilter/VB/MainWindow.xaml.vb#211)]

## <a name="filtering-items-in-a-datagrid"></a>Filtrage des éléments dans un contrôle DataGrid

Pour filtrer les éléments dans un <xref:System.Windows.Controls.DataGrid> à l’aide un <xref:System.Windows.Data.CollectionViewSource>, vous fournissez la logique de filtrage dans le gestionnaire pour le <xref:System.Windows.Data.CollectionViewSource.Filter?displayProperty=nameWithType> événement.

### <a name="to-filter-items-in-a-datagrid"></a>Pour filtrer des éléments dans un contrôle DataGrid

1. Ajoutez un gestionnaire pour le <xref:System.Windows.Data.CollectionViewSource.Filter?displayProperty=nameWithType> événement.

2. Dans le <xref:System.Windows.Data.CollectionViewSource.Filter> Gestionnaire d’événements, définir la logique de filtrage.

    Le filtre sera appliqué chaque fois que la vue soit actualisée.

    [!code-xaml[DataGrid_GroupSortFilter#013](~/samples/snippets/csharp/VS_Snippets_Wpf/DataGrid_GroupSortFilter/CS/MainWindow.xaml#013)]
    [!code-csharp[DataGrid_GroupSortFilter#113](~/samples/snippets/csharp/VS_Snippets_Wpf/DataGrid_GroupSortFilter/CS/MainWindow.xaml.cs#113)]
    [!code-vb[DataGrid_GroupSortFilter#113](~/samples/snippets/visualbasic/VS_Snippets_Wpf/DataGrid_GroupSortFilter/VB/MainWindow.xaml.vb#113)]

Ou bien, vous pouvez filtrer les éléments dans un <xref:System.Windows.Controls.DataGrid> en créant une méthode qui fournit la logique et le paramètre de filtrage le <xref:System.Windows.Data.CollectionView.Filter%2A?displayProperty=nameWithType> propriété pour appliquer le filtre. Pour voir un exemple de cette méthode, consultez [filtrer des données dans une vue](../data/how-to-filter-data-in-a-view.md).

## <a name="example"></a>Exemple

L’exemple suivant montre le regroupement, le tri et filtrage `Task` les données dans un <xref:System.Windows.Data.CollectionViewSource> et l’affichage groupés, triée et filtrée `Task` les données dans un <xref:System.Windows.Controls.DataGrid>. Le <xref:System.Windows.Data.CollectionViewSource> est utilisé comme le <xref:System.Windows.Controls.ItemsControl.ItemsSource%2A> pour le <xref:System.Windows.Controls.DataGrid>. Regroupement, le tri et filtrage sont effectuées sur le <xref:System.Windows.Data.CollectionViewSource> et s’affichent dans le <xref:System.Windows.Controls.DataGrid> l’interface utilisateur.

Pour tester cet exemple, vous devrez ajuster le nom DGGroupSortFilterExample pour faire correspondre le nom de votre projet. Si vous utilisez Visual Basic, vous devez modifier le nom de classe pour <xref:System.Windows.Window> à ce qui suit.

`<Window x:Class="MainWindow"`

[!code-xaml[DataGrid_GroupSortFilter#000](~/samples/snippets/csharp/VS_Snippets_Wpf/DataGrid_GroupSortFilter/CS/MainWindow.xaml#000)]
[!code-csharp[DataGrid_GroupSortFilter#100](~/samples/snippets/csharp/VS_Snippets_Wpf/DataGrid_GroupSortFilter/CS/MainWindow.xaml.cs#100)]
[!code-vb[DataGrid_GroupSortFilter#100](~/samples/snippets/visualbasic/VS_Snippets_Wpf/DataGrid_GroupSortFilter/VB/MainWindow.xaml.vb#100)]

## <a name="see-also"></a>Voir aussi

- [Vue d’ensemble de la liaison de données](../data/data-binding-overview.md)
- [Créer et effectuer une liaison à un ObservableCollection](../data/how-to-create-and-bind-to-an-observablecollection.md)
- [Filtrer les données d’une vue](../data/how-to-filter-data-in-a-view.md)
- [Trier des données dans une vue](../data/how-to-sort-data-in-a-view.md)
- [Trier et grouper des données à l'aide d'une vue en XAML](../data/how-to-sort-and-group-data-using-a-view-in-xaml.md)
