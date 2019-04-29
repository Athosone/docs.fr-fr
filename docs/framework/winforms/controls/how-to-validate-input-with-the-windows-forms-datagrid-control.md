---
title: 'Procédure : valider l’entrée avec le contrôle DataGrid Windows Forms'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- DataGrid control [Windows Forms], examples
- user input [Windows Forms], validating
- examples [Windows Forms], DataGrid control
- DataGrid control [Windows Forms], validating input
- validation [Windows Forms], user input
ms.assetid: f1e9c3a0-d0a1-4893-a615-b4b0db046c63
ms.openlocfilehash: dc8c8f157e6673c1bddc68bfb511683e6d2b99be
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61796472"
---
# <a name="how-to-validate-input-with-the-windows-forms-datagrid-control"></a>Procédure : valider l’entrée avec le contrôle DataGrid Windows Forms

> [!NOTE]
> Le contrôle <xref:System.Windows.Forms.DataGridView> remplace le contrôle <xref:System.Windows.Forms.DataGrid> et lui ajoute des fonctionnalités ; toutefois, le contrôle <xref:System.Windows.Forms.DataGrid> est conservé pour la compatibilité descendante et l'utilisation future si tel est votre choix. Pour plus d’informations, consultez [Différences entre les contrôles DataGridView et DataGrid Windows Forms](differences-between-the-windows-forms-datagridview-and-datagrid-controls.md).

Il existe deux types de validation d’entrée disponibles pour les formulaires Windows <xref:System.Windows.Forms.DataGrid> contrôle. Si l’utilisateur tente d’entrer une valeur qui est d’un type de données inacceptable pour la cellule, par exemple une chaîne en entier, la nouvelle valeur non valide est remplacée par l’ancienne valeur. Ce type de validation d’entrée est effectué automatiquement et ne peuvent pas être personnalisé.

L’autre type de validation d’entrée peut être utilisé pour refuser des données inacceptables, par exemple une valeur 0 dans un champ qui doit être supérieure ou égale à 1, ou une chaîne inappropriée. Cela est effectué dans le jeu de données en écrivant un gestionnaire d’événements pour le <xref:System.Data.DataTable.ColumnChanging> ou <xref:System.Data.DataTable.RowChanging> événement. L’exemple ci-dessous utilise la <xref:System.Data.DataTable.ColumnChanging> événement, car la valeur inacceptable n’est pas autorisée pour la colonne « Product » en particulier. Vous pouvez utiliser le <xref:System.Data.DataTable.RowChanging> événements pour vérifier que la valeur d’une colonne « End Date » est postérieure à la colonne « Date de début » dans la même ligne.

## <a name="to-validate-user-input"></a>Pour valider l’entrée utilisateur

1. Écrire du code pour gérer le <xref:System.Data.DataTable.ColumnChanging> événement pour la table appropriée. Lors de l’entrée incorrecte est détectée, appelez le <xref:System.Data.DataRow.SetColumnError%2A> méthode de la <xref:System.Data.DataRow> objet.

    ```vb
    Private Sub Customers_ColumnChanging(ByVal sender As Object, _
    ByVal e As System.Data.DataColumnChangeEventArgs)
       ' Only check for errors in the Product column
       If (e.Column.ColumnName.Equals("Product")) Then
          ' Do not allow "Automobile" as a product.
          If CType(e.ProposedValue, String) = "Automobile" Then
             Dim badValue As Object = e.ProposedValue
             e.ProposedValue = "Bad Data"
             e.Row.RowError = "The Product column contains an error"
             e.Row.SetColumnError(e.Column, "Product cannot be " & _
             CType(badValue, String))
          End If
       End If
    End Sub
    ```

    ```csharp
    //Handle column changing events on the Customers table
    private void Customers_ColumnChanging(object sender, System.Data.DataColumnChangeEventArgs e) {

       //Only check for errors in the Product column
       if (e.Column.ColumnName.Equals("Product")) {

          //Do not allow "Automobile" as a product
          if (e.ProposedValue.Equals("Automobile")) {
             object badValue = e.ProposedValue;
             e.ProposedValue = "Bad Data";
             e.Row.RowError = "The Product column contains an error";
             e.Row.SetColumnError(e.Column, "Product cannot be " + badValue);
          }
       }
    }
    ```

2. Connecter le Gestionnaire d’événements à l’événement.

    Placez le code suivant dans une du formulaire <xref:System.Windows.Forms.Form.Load> événement ou son constructeur.

    ```vb
    ' Assumes the grid is bound to a dataset called customersDataSet1
    ' with a table called Customers.
    ' Put this code in the form's Load event or its constructor.
    AddHandler customersDataSet1.Tables("Customers").ColumnChanging, AddressOf Customers_ColumnChanging
    ```

    ```csharp
    // Assumes the grid is bound to a dataset called customersDataSet1
    // with a table called Customers.
    // Put this code in the form's Load event or its constructor.
    customersDataSet1.Tables["Customers"].ColumnChanging += new DataColumnChangeEventHandler(this.Customers_ColumnChanging);
    ```

## <a name="see-also"></a>Voir aussi

- <xref:System.Windows.Forms.DataGrid>
- <xref:System.Data.DataTable.ColumnChanging>
- <xref:System.Data.DataRow.SetColumnError%2A>
- [DataGrid, contrôle](datagrid-control-windows-forms.md)
