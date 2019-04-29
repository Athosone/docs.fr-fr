---
title: 'Procédure : supprimer ou masquer des colonnes dans le contrôle DataGrid Windows Forms'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- data grids [Windows Forms], deleting columns
- DataGrid control [Windows Forms], deleting columns
- data grids [Windows Forms], hiding columns
- columns [Windows Forms], hiding
- columns [Windows Forms], deleting in data grids
- DataGrid control [Windows Forms], hiding columns
ms.assetid: bcd0dd96-6687-4c48-b0e1-d5287b93ac91
ms.openlocfilehash: d3f1f013cbb5e41c997014f556602b01bab62914
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61757389"
---
# <a name="how-to-delete-or-hide-columns-in-the-windows-forms-datagrid-control"></a>Procédure : supprimer ou masquer des colonnes dans le contrôle DataGrid Windows Forms
> [!NOTE]
>  Le contrôle <xref:System.Windows.Forms.DataGridView> remplace le contrôle <xref:System.Windows.Forms.DataGrid> et lui ajoute des fonctionnalités ; toutefois, le contrôle <xref:System.Windows.Forms.DataGrid> est conservé pour la compatibilité descendante et l'utilisation future si tel est votre choix. Pour plus d’informations, consultez [Différences entre les contrôles DataGridView et DataGrid Windows Forms](differences-between-the-windows-forms-datagridview-and-datagrid-controls.md).  
  
 Vous pouvez par programmation supprimer ou masquer des colonnes dans les formulaires Windows <xref:System.Windows.Forms.DataGrid> contrôle à l’aide des propriétés et méthodes de la <xref:System.Windows.Forms.GridColumnStylesCollection> et <xref:System.Windows.Forms.DataGridColumnStyle> objets (qui sont membres de la <xref:System.Windows.Forms.DataGridTableStyle> classe).  
  
 Les colonnes supprimées ou masquées existent toujours dans la source de données est lié à la grille et accessible par programme. Ils sont simplement n’est plus visibles dans la grille de données.  
  
> [!NOTE]
>  Si votre application n’accède pas à certaines colonnes de données, et que vous ne souhaitez pas les afficher dans la grille de données, il n’est probablement pas nécessaire pour les inclure dans la source de données en premier lieu.  
  
### <a name="to-delete-a-column-from-the-datagrid-programmatically"></a>Pour supprimer une colonne à partir de la grille de données par programmation  
  
1. Dans la zone de déclarations de votre formulaire, déclarez une nouvelle instance de la <xref:System.Windows.Forms.DataGridTableStyle> classe.  
  
2. Définir le <xref:System.Windows.Forms.DataGridTableStyle.MappingName%2A?displayProperty=nameWithType> propriété à la table dans votre source de données que vous souhaitez appliquer le style. L’exemple suivant utilise le <xref:System.Windows.Forms.DataGrid.DataMember%2A?displayProperty=nameWithType> propriété, qu’il considère est déjà défini.  
  
3. Ajoutez la nouvelle <xref:System.Windows.Forms.DataGridTableStyle> objet à la collection de styles de table de la grille de données.  
  
4. Appelez le <xref:System.Windows.Forms.GridColumnStylesCollection.RemoveAt%2A> méthode de la <xref:System.Windows.Forms.DataGrid>de <xref:System.Windows.Forms.DataGridTableStyle.GridColumnStyles%2A> collection, en spécifiant l’index de colonne de la colonne à supprimer.  
  
    ```vb  
    ' Declare a new DataGridTableStyle in the  
    ' declarations area of your form.  
    Dim ts As DataGridTableStyle = New DataGridTableStyle()  
  
    Sub DeleteColumn()  
       ' Set the DataGridTableStyle.MappingName property  
       ' to the table in the data source to map to.  
       ts.MappingName = DataGrid1.DataMember  
  
       ' Add it to the datagrid's TableStyles collection  
       DataGrid1.TableStyles.Add(ts)  
  
       ' Delete the first column (index 0)  
       DataGrid1.TableStyles(0).GridColumnStyles.RemoveAt(0)  
    End Sub  
    ```  
  
    ```csharp  
    // Declare a new DataGridTableStyle in the  
    // declarations area of your form.  
    DataGridTableStyle ts = new DataGridTableStyle();  
  
    private void deleteColumn()  
    {  
       // Set the DataGridTableStyle.MappingName property  
       // to the table in the data source to map to.  
       ts.MappingName = dataGrid1.DataMember;  
  
       // Add it to the datagrid's TableStyles collection  
       dataGrid1.TableStyles.Add(ts);  
  
       // Delete the first column (index 0)  
       dataGrid1.TableStyles[0].GridColumnStyles.RemoveAt(0);  
    }  
    ```  
  
### <a name="to-hide-a-column-in-the-datagrid-programmatically"></a>Pour masquer une colonne dans la grille de données par programmation  
  
1. Dans la zone de déclarations de votre formulaire, déclarez une nouvelle instance de la <xref:System.Windows.Forms.DataGridTableStyle> classe.  
  
2. Définir le <xref:System.Windows.Forms.DataGridTableStyle.MappingName%2A> propriété de la <xref:System.Windows.Forms.DataGridTableStyle> à la table dans votre source de données que vous souhaitez appliquer le style. Le code suivant exemple utilise le <xref:System.Windows.Forms.DataGrid.DataMember%2A?displayProperty=nameWithType> propriété, qu’il considère est déjà défini.  
  
3. Ajoutez la nouvelle <xref:System.Windows.Forms.DataGridTableStyle> objet à la collection de styles de table de la grille de données.  
  
4. Masquer la colonne en définissant son `Width` propriété sur 0, qui spécifie l’index de colonne de la colonne à masquer.  
  
    ```vb  
    ' Declare a new DataGridTableStyle in the  
    ' declarations area of your form.  
    Dim ts As DataGridTableStyle = New DataGridTableStyle()  
  
    Sub HideColumn()  
       ' Set the DataGridTableStyle.MappingName property  
       ' to the table in the data source to map to.  
       ts.MappingName = DataGrid1.DataMember  
  
       ' Add it to the datagrid's TableStyles collection  
       DataGrid1.TableStyles.Add(ts)  
  
       ' Hide the first column (index 0)  
       DataGrid1.TableStyles(0).GridColumnStyles(0).Width = 0  
    End Sub  
    ```  
  
    ```csharp  
    // Declare a new DataGridTableStyle in the  
    // declarations area of your form.  
    DataGridTableStyle ts = new DataGridTableStyle();  
  
    private void hideColumn()  
    {  
       // Set the DataGridTableStyle.MappingName property  
       // to the table in the data source to map to.  
       ts.MappingName = dataGrid1.DataMember;  
  
       // Add it to the datagrid's TableStyles collection  
       dataGrid1.TableStyles.Add(ts);  
  
       // Hide the first column (index 0)  
       dataGrid1.TableStyles[0].GridColumnStyles[0].Width = 0;  
    }  
    ```  
  
## <a name="see-also"></a>Voir aussi

- [Guide pratique pour Modification des données affichées au moment de l’exécution dans le contrôle DataGrid Windows Forms](change-displayed-data-at-run-time-wf-datagrid-control.md)
- [Guide pratique pour Ajouter des Tables et des colonnes au contrôle DataGrid Windows Forms](how-to-add-tables-and-columns-to-the-windows-forms-datagrid-control.md)
