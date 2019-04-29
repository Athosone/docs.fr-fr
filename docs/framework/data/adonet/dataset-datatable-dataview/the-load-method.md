---
title: Méthode Load
ms.date: 03/30/2017
dev_langs:
- vb
ms.assetid: e22e5812-89c6-41f0-9302-bb899a46dbff
ms.openlocfilehash: 82f840ab7dd26a4888ebf024d696f2c70701eb18
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61607230"
---
# <a name="the-load-method"></a>Méthode Load
Vous pouvez utiliser la méthode <xref:System.Data.DataTable.Load%2A> pour charger un objet <xref:System.Data.DataTable> de lignes d'une source de données. Il s’agit d’une méthode surchargée qui, dans sa forme la plus simple, accepte un seul paramètre, un **DataReader**. Dans cet écran, elle charge simplement la **DataTable** avec des lignes. Si vous le souhaitez, vous pouvez spécifier le **LoadOption** paramètre pour contrôler la façon dont les données sont ajoutées à la **DataTable**.  
  
 Le **LoadOption** paramètre est particulièrement utile dans les cas où le **DataTable** déjà contient des lignes de données, car il décrit les données entrantes à partir de la source de données seront combinées avec les données dans la table. Par exemple, **PreserveCurrentValues** (la valeur par défaut) Spécifie que dans les cas où une ligne est marquée en tant que **Added** dans le **DataTable**, le **Original** valeur ou chaque colonne est définie pour le contenu de la ligne correspondante à partir de la source de données. Le **actuel** valeur conserve les valeurs affectées lors de la ligne a été ajoutée et le **RowState** de la ligne aura la valeur **Changed**.  
  
 Le tableau suivant donne une brève description des valeurs d'énumération <xref:System.Data.LoadOption>.  
  
|Valeur LoadOption|Description|  
|----------------------|-----------------|  
|**OverwriteRow**|Si des lignes entrantes ont la même **PrimaryKey** valeur sous la forme d’une ligne figurant déjà dans le **DataTable**, le **d’origine** et **actuel** les valeurs de chacun d’eux colonne sont remplacées par les valeurs dans la ligne entrante et la **RowState** propriété est définie sur **Unchanged**.<br /><br /> Lignes de la source de données qui n’existent pas déjà dans le **DataTable** sont ajoutés avec un **RowState** valeur **Unchanged**.<br /><br /> Cette option actualise le contenu de la **DataTable** afin qu’il correspond au contenu de la source de données.|  
|**PreserveCurrentValues (par défaut)**|Si des lignes entrantes ont la même **PrimaryKey** valeur sous la forme d’une ligne figurant déjà dans le **DataTable**, le **d’origine** a la valeur pour le contenu de la ligne entrante et la **Actuel** valeur n’est pas modifiée.<br /><br /> Si le **RowState** est **Added** ou **Modified**, il est défini sur **Modified**.<br /><br /> Si le **RowState** a été **Deleted**, il reste **Deleted**.<br /><br /> Lignes de la source de données qui n’existent pas déjà dans le **DataTable** sont ajoutés et le **RowState** a la valeur **Unchanged**.|  
|**UpdateCurrentValues**|Si des lignes entrantes ont la même **PrimaryKey** valeur en tant que ligne figurant déjà dans le **DataTable**, le **actuel** valeur est copiée dans le **Original**valeur et le **actuel** valeur est ensuite définie sur le contenu de la ligne entrante.<br /><br /> Si le **RowState** dans le **DataTable** a été **Added**, le **RowState** reste **Added**. Pour les lignes marquées comme **Modified** ou **Deleted**, le **RowState** est **Modified**.<br /><br /> Lignes de la source de données qui n’existent pas déjà dans le **DataTable** sont ajoutés et le **RowState** a la valeur **Added**.|  
  
 L’exemple suivant utilise le **charge** méthode pour afficher une liste d’anniversaires des employés dans la **Northwind** base de données.  
  
```vb  
Private Sub LoadBirthdays(ByVal connectionString As String)  
    ' Assumes that connectionString is a valid connection string  
    ' to the Northwind database on SQL Server.  
    Dim queryString As String = _  
    "SELECT LastName, FirstName, BirthDate " & _  
      " FROM dbo.Employees " & _  
      "ORDER BY BirthDate, LastName, FirstName"  
  
    ' Open and fill a DataSet.   
    Dim adapter As SqlDataAdapter = New SqlDataAdapter( _  
        queryString, connectionString)  
    Dim employees As New DataSet  
    adapter.Fill(employees, "Employees")  
  
    ' Create a SqlDataReader for use with the Load Method.  
    Dim reader As DataTableReader = employees.GetDataReader()  
  
    ' Create an instance of DataTable and assign the first  
    ' DataTable in the DataSet.Tables collection to it.  
    Dim dataTableEmp As DataTable = employees.Tables(0)  
  
    ' Fill the DataTable with data by calling Load and  
    ' passing the SqlDataReader.  
    dataTableEmp.Load(reader, LoadOption.OverwriteRow)  
  
    ' Loop through the rows collection and display the values  
    ' in the console window.  
    Dim employeeRow As DataRow  
    For Each employeeRow In dataTableEmp.Rows  
        Console.WriteLine("{0:MM\\dd\\yyyy}" & ControlChars.Tab & _  
          "{1}, {2}", _  
          employeeRow("BirthDate"), _  
          employeeRow("LastName"), _  
          employeeRow("FirstName"))  
    Next employeeRow  
  
    ' Keep the window opened to view the contents.  
    Console.ReadLine()  
End Sub  
```  
  
## <a name="see-also"></a>Voir aussi

- [Manipulation des données dans un DataTable](../../../../../docs/framework/data/adonet/dataset-datatable-dataview/manipulating-data-in-a-datatable.md)
- [Fournisseurs managés ADO.NET et centre de développement DataSet](https://go.microsoft.com/fwlink/?LinkId=217917)
