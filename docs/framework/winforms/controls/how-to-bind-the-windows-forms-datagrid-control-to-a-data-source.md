---
title: 'Procédure : lier le contrôle DataGrid Windows Forms à une source de données'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
- cpp
helpviewer_keywords:
- datasets [Windows Forms], binding to DataGrid control
- data binding [Windows Forms], DataGrid control
- DataGrid control [Windows Forms], data binding
- bound controls [Windows Forms], DataGrid control
- Windows Forms controls, data binding
- bound controls [Windows Forms]
- data-bound controls [Windows Forms], DataGrid
ms.assetid: 128cdb07-dfd3-4d60-9d6a-902847667c36
ms.openlocfilehash: 920a93894cc126f85bc6b618efbe6e9cedea4881
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59332571"
---
# <a name="how-to-bind-the-windows-forms-datagrid-control-to-a-data-source"></a>Procédure : lier le contrôle DataGrid Windows Forms à une source de données
> [!NOTE]
>  Le contrôle <xref:System.Windows.Forms.DataGridView> remplace le contrôle <xref:System.Windows.Forms.DataGrid> et lui ajoute des fonctionnalités ; toutefois, le contrôle <xref:System.Windows.Forms.DataGrid> est conservé pour la compatibilité descendante et l'utilisation future si tel est votre choix. Pour plus d’informations, consultez [Différences entre les contrôles DataGridView et DataGrid Windows Forms](differences-between-the-windows-forms-datagridview-and-datagrid-controls.md).  
  
 Les formulaires Windows <xref:System.Windows.Forms.DataGrid> contrôle est spécifiquement conçu pour afficher des informations à partir d’une source de données. Vous liez le contrôle au moment de l’exécution en appelant le <xref:System.Windows.Forms.DataGrid.SetDataBinding%2A> (méthode). Bien que vous pouvez afficher des données à partir de diverses sources de données, les sources les plus courantes sont les vues de données et des jeux de données.  
  
### <a name="to-data-bind-the-datagrid-control-programmatically"></a>Lier aux données du contrôle DataGrid par programme  
  
1. Écrire du code pour remplir le dataset.  
  
     Si la source de données est un jeu de données ou une vue de données basée sur une table de dataset, ajoutez le code au formulaire pour remplir le dataset.  
  
     Le code exact que vous utilisez dépend où le jeu de données est l’obtention de données. Si le jeu de données est rempli directement à partir d’une base de données, vous appelez généralement la `Fill` méthode d’un adaptateur de données, comme dans l’exemple suivant, qui remplit un dataset nommé `DsCategories1`:  
  
    ```vb  
    sqlDataAdapter1.Fill(DsCategories1)  
    ```  
  
    ```csharp  
    sqlDataAdapter1.Fill(DsCategories1);  
    ```  
  
    ```cpp  
    sqlDataAdapter1->Fill(dsCategories1);  
    ```  
  
     Si le jeu de données est remplie à partir d’un service Web XML, vous en général, créez une instance du service dans votre code, puis appelez une de ses méthodes pour retourner un jeu de données. Vous permet ensuite de fusionner le jeu de données à partir du service Web XML dans votre jeu de données local. L’exemple suivant montre comment vous pouvez créer une instance d’un service Web XML appelé `CategoriesService`, appelez sa `GetCategories` (méthode) et fusion, le jeu de données résultant dans un jeu de données local appelé `DsCategories1`:  
  
    ```vb  
    Dim ws As New MyProject.localhost.CategoriesService()  
    ws.Credentials = System.Net.CredentialCache.DefaultCredentials  
    DsCategories1.Merge(ws.GetCategories())  
    ```  
  
    ```csharp  
    MyProject.localhost.CategoriesService ws = new MyProject.localhost.CategoriesService();  
    ws.Credentials = System.Net.CredentialCache.DefaultCredentials;  
    DsCategories1.Merge(ws.GetCategories());  
    ```  
  
    ```cpp  
    MyProject::localhost::CategoriesService^ ws =   
       new MyProject::localhost::CategoriesService();  
    ws->Credentials = System::Net::CredentialCache::DefaultCredentials;  
    dsCategories1->Merge(ws->GetCategories());  
    ```  
  
2. Appelez le <xref:System.Windows.Forms.DataGrid> du contrôle <xref:System.Windows.Forms.DataGrid.SetDataBinding%2A> méthode, en lui passant la source de données et un membre de données. Si vous n’avez pas besoin de transmettre explicitement un membre de données, passez une chaîne vide.  
  
    > [!NOTE]
    >  Si vous liez la grille pour la première fois, vous pouvez définir le contrôle <xref:System.Windows.Forms.DataGrid.DataSource%2A> et <xref:System.Windows.Forms.DataGrid.DataMember%2A> propriétés. Toutefois, vous ne pouvez pas réinitialiser ces propriétés une fois qu’elles ont été définies. Par conséquent, il est recommandé de toujours utiliser le <xref:System.Windows.Forms.DataGrid.SetDataBinding%2A> (méthode).  
  
     L’exemple suivant montre comment vous pouvez lier par programmation à la table Customers dans un dataset nommé `DsCustomers1`:  
  
    ```vb  
    DataGrid1.SetDataBinding(DsCustomers1, "Customers")  
    ```  
  
    ```csharp  
    DataGrid1.SetDataBinding(DsCustomers1, "Customers");  
    ```  
  
    ```cpp  
    dataGrid1->SetDataBinding(dsCustomers1, "Customers");  
    ```  
  
     Si la table Customers est la seule table dans le jeu de données, vous pourriez également lier à la grille de cette façon :  
  
    ```vb  
    DataGrid1.SetDataBinding(DsCustomers1, "")  
    ```  
  
    ```csharp  
    DataGrid1.SetDataBinding(DsCustomers1, "");  
    ```  
  
    ```cpp  
    dataGrid1->SetDataBinding(dsCustomers1, "");  
    ```  
  
3. (Facultatif) Ajouter les styles de table approprié et les styles de colonne à la grille. S’il n’y a aucun style de tableau, vous verrez la table, mais avec la mise en forme minimale et toutes les colonnes visibles.  
  
## <a name="see-also"></a>Voir aussi

- [Vue d’ensemble du contrôle DataGrid](datagrid-control-overview-windows-forms.md)
- [Guide pratique pour Ajouter des Tables et des colonnes au contrôle DataGrid Windows Forms](how-to-add-tables-and-columns-to-the-windows-forms-datagrid-control.md)
- [DataGrid, contrôle](datagrid-control-windows-forms.md)
- [Liaison de données Windows Forms](../windows-forms-data-binding.md)
