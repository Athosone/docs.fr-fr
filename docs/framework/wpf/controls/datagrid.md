---
title: DataGrid
ms.date: 03/30/2017
helpviewer_keywords:
- DataGrid column types [WPF]
- DataGrid scenarios [WPF]
- DataGrid control [WPF]
- controls [WPF], DataGrid
- DataGrid [WPF], common tasks for
- DataGrid [WPF], customizing the appearance of
- DataGrid columns [WPF], using
ms.assetid: bf89ea63-79b6-422b-bc9f-0485ad803216
ms.openlocfilehash: dda712d58a4ff956de074ecd416402ba0aece5f4
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61912234"
---
# <a name="datagrid"></a>DataGrid
Le <xref:System.Windows.Controls.DataGrid> contrôle vous permet d’afficher et modifier des données à partir de nombreuses sources différentes, comme à partir d’une base de données SQL, requête LINQ ou toute autre source de données pouvant être liées. Pour plus d’informations, consultez [Vue d’ensemble de la liaison de ressources](../data/binding-sources-overview.md).  
  
 Colonnes peuvent afficher du texte, des contrôles, comme un <xref:System.Windows.Controls.ComboBox>, ou tout autre contenu WPF, tels que des images, des boutons ou n’importe quel contenu dans un modèle. Vous pouvez utiliser un <xref:System.Windows.Controls.DataGridTemplateColumn> pour afficher les données définies dans un modèle. Le tableau suivant répertorie les types de colonnes qui sont fournis par défaut.  
  
|Type de colonne générée|Type de données|  
|---------------------------|---------------|  
|<xref:System.Windows.Controls.DataGridTextColumn>|<xref:System.String>|  
|<xref:System.Windows.Controls.DataGridCheckBoxColumn>|<xref:System.Boolean>|  
|<xref:System.Windows.Controls.DataGridComboBoxColumn>|<xref:System.Enum>|  
|<xref:System.Windows.Controls.DataGridHyperlinkColumn>|<xref:System.Uri>|  
  
 <xref:System.Windows.Controls.DataGrid> peut être personnalisé en apparence, telles que la taille, la couleur et la police de la cellule. <xref:System.Windows.Controls.DataGrid> prend en charge toutes les fonctionnalités de styles et modèles d’autres contrôles WPF. <xref:System.Windows.Controls.DataGrid> inclut également des comportements par défaut et personnalisables pour modification, le tri et la validation.  
  
 Le tableau suivant répertorie certaines des tâches courantes pour <xref:System.Windows.Controls.DataGrid> et comment les accomplir. En affichant l’API associée, vous pouvez trouver plus d’informations et exemples de code.  
  
|Scénario|Approche|  
|--------------|--------------|  
|Couleurs d’arrière-plan en alternance|Définir le <xref:System.Windows.Controls.ItemsControl.AlternationIndex%2A> propriété sur 2 ou plus, puis attribuez un <xref:System.Windows.Media.Brush> à la <xref:System.Windows.Controls.DataGrid.RowBackground%2A> et <xref:System.Windows.Controls.DataGrid.AlternatingRowBackground%2A> propriétés.|  
|Définir le comportement de sélection de cellule et de ligne|Définissez les propriétés <xref:System.Windows.Controls.DataGrid.SelectionMode%2A> et <xref:System.Windows.Controls.DataGrid.SelectionUnit%2A>.|  
|Personnaliser l’apparence visuelle des en-têtes, des cellules et des lignes|Appliquer un nouveau <xref:System.Windows.Style> à la <xref:System.Windows.Controls.DataGrid.ColumnHeaderStyle%2A>, <xref:System.Windows.Controls.DataGrid.RowHeaderStyle%2A>, <xref:System.Windows.Controls.DataGrid.CellStyle%2A>, ou <xref:System.Windows.Controls.DataGrid.RowStyle%2A> propriétés.|  
|Définir les options de dimensionnement|Définir le <xref:System.Windows.FrameworkElement.Height%2A>, <xref:System.Windows.FrameworkElement.MaxHeight%2A>, <xref:System.Windows.FrameworkElement.MinHeight%2A>, <xref:System.Windows.FrameworkElement.Width%2A>, <xref:System.Windows.FrameworkElement.MaxWidth%2A>, ou <xref:System.Windows.FrameworkElement.MinWidth%2A> propriétés. Pour plus d’informations, consultez [les Options de dimensionnement dans le contrôle DataGrid](sizing-options-in-the-datagrid-control.md).|  
|Accéder aux éléments sélectionné|Vérifier le <xref:System.Windows.Controls.DataGrid.SelectedCells%2A> propriété à obtenir les cellules sélectionnées et le <xref:System.Windows.Controls.Primitives.MultiSelector.SelectedItems%2A> propriété à obtenir les lignes sélectionnées. Pour plus d'informations, consultez <xref:System.Windows.Controls.DataGrid.SelectedCells%2A>.|  
|Personnaliser les interactions de l’utilisateur final|Définir le <xref:System.Windows.Controls.DataGrid.CanUserAddRows%2A>, <xref:System.Windows.Controls.DataGrid.CanUserDeleteRows%2A>, <xref:System.Windows.Controls.DataGrid.CanUserReorderColumns%2A>, <xref:System.Windows.Controls.DataGrid.CanUserResizeColumns%2A>, <xref:System.Windows.Controls.DataGrid.CanUserResizeRows%2A>, et <xref:System.Windows.Controls.DataGrid.CanUserSortColumns%2A> propriétés.|  
|Annuler ou modifier des colonnes générées automatiquement|Gérer le <xref:System.Windows.Controls.DataGrid.AutoGeneratingColumn> événement.|  
|Figer une colonne|Définir le <xref:System.Windows.Controls.DataGrid.FrozenColumnCount%2A> propriété 1 et placez la colonne à la position la plus à gauche en définissant le <xref:System.Windows.Controls.DataGridColumn.DisplayIndex%2A> 0 à la propriété.|  
|Utiliser des données XML comme source de données|Lier le <xref:System.Windows.Controls.ItemsControl.ItemsSource%2A> sur la <xref:System.Windows.Controls.DataGrid> à la requête XPath qui représente la collection d’éléments. Créez chaque colonne dans la <xref:System.Windows.Controls.DataGrid>. Lier chaque colonne en définissant le XPath de la liaison à la requête qui obtient la propriété sur la source d’élément. Pour obtenir un exemple, consultez <xref:System.Windows.Controls.DataGridTextColumn>.|  
  
## <a name="related-topics"></a>Rubriques connexes  
  
|Titre|Description|  
|-----------|-----------------|  
|[Procédure pas à pas : Afficher des données à partir d’une base de données SQL Server dans un contrôle DataGrid](walkthrough-display-data-from-a-sql-server-database-in-a-datagrid-control.md)|Décrit comment configurer un projet WPF, ajouter un élément Entity Framework, définissez la source et afficher les données dans un <xref:System.Windows.Controls.DataGrid>.|  
|[Guide pratique pour Ajouter des détails de la ligne à un contrôle DataGrid](how-to-add-row-details-to-a-datagrid-control.md)|Décrit comment créer des détails de la ligne pour un <xref:System.Windows.Controls.DataGrid>.|  
|[Guide pratique pour Implémenter la Validation avec le contrôle DataGrid](how-to-implement-validation-with-the-datagrid-control.md)|Décrit comment valider des valeurs dans <xref:System.Windows.Controls.DataGrid> cellules et des lignes et des commentaires de validation complet.|  
|[Comportement par défaut du clavier et de la souris dans le contrôle DataGrid](default-keyboard-and-mouse-behavior-in-the-datagrid-control.md)|Décrit comment interagir avec le <xref:System.Windows.Controls.DataGrid> contrôle à l’aide du clavier et la souris.|  
|[Guide pratique pour Regrouper, trier et filtrer les données dans le contrôle DataGrid](how-to-group-sort-and-filter-data-in-the-datagrid-control.md)|Décrit comment afficher des données dans un <xref:System.Windows.Controls.DataGrid> de différentes façons par regroupement, le tri et filtrage des données.|  
|[Options de dimensionnement dans le contrôle DataGrid](sizing-options-in-the-datagrid-control.md)|Décrit comment contrôler le dimensionnement absolu et automatique dans le <xref:System.Windows.Controls.DataGrid>.|  
  
## <a name="see-also"></a>Voir aussi

- <xref:System.Windows.Controls.DataGrid>
- [Application d’un style et création de modèles](styling-and-templating.md)
- [Vue d’ensemble de la liaison de données](../data/data-binding-overview.md)
- [Vue d’ensemble des modèles de données](../data/data-templating-overview.md)
- [Contrôles](index.md)
- [Modèle de contenu WPF](wpf-content-model.md)
