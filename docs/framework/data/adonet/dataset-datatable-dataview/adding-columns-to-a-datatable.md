---
title: Ajout de colonnes à un DataTable
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
ms.assetid: e85c4a0e-4f3f-458c-b58b-0ddbc06bf974
ms.openlocfilehash: 2e7008f6693d7d76520a7ff6ae9172e28e4990c2
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59207004"
---
# <a name="adding-columns-to-a-datatable"></a>Ajout de colonnes à un DataTable
Un <xref:System.Data.DataTable> contient une collection de <xref:System.Data.DataColumn> objets référencés par le **colonnes** propriété de la table. Cette collection de colonnes, ainsi que toute contrainte, définit le schéma, ou structure, de la table.  
  
 Vous créez **DataColumn** objets au sein d’une table en utilisant le **DataColumn** constructeur, ou en appelant le **ajouter** méthode de la **colonnes**propriété de la table, qui est un <xref:System.Data.DataColumnCollection>. Le **ajouter** méthode accepte facultatif **ColumnName**, **DataType**, et **Expression** arguments et crée un nouveau  **DataColumn** en tant que membre de la collection. Il accepte également un existant **DataColumn** de l’objet et l’ajoute à la collection et retourne une référence à l’ajout **DataColumn** si nécessaire. Étant donné que **DataTable** objets ne sont pas spécifiques à n’importe quelle source de données, les types .NET Framework sont utilisées lorsque vous spécifiez le type de données d’un **DataColumn**.  
  
 L’exemple suivant ajoute quatre colonnes à un **DataTable**.  
  
```vb  
Dim workTable As DataTable = New DataTable("Customers")  
  
Dim workCol As DataColumn = workTable.Columns.Add( _  
    "CustID", Type.GetType("System.Int32"))  
workCol.AllowDBNull = false  
workCol.Unique = true  
  
workTable.Columns.Add("CustLName", Type.GetType("System.String"))  
workTable.Columns.Add("CustFName", Type.GetType("System.String"))  
workTable.Columns.Add("Purchases", Type.GetType("System.Double"))  
```  
  
```csharp  
DataTable workTable = new DataTable("Customers");  
  
DataColumn workCol = workTable.Columns.Add("CustID", typeof(Int32));  
workCol.AllowDBNull = false;  
workCol.Unique = true;  
  
workTable.Columns.Add("CustLName", typeof(String));  
workTable.Columns.Add("CustFName", typeof(String));  
workTable.Columns.Add("Purchases", typeof(Double));  
```  
  
 Dans l’exemple, notez que les propriétés de la **CustID** colonne sont définies pour ne pas autoriser **DBNull** valeurs et pour limiter les valeurs uniques. Toutefois, si vous définissez la **CustID** colonne comme colonne clé primaire de la table, le **AllowDBNull** propriété définira automatiquement **false** et le **Unique** propriété définira automatiquement **true**. Pour plus d’informations, consultez [définition des clés primaires](../../../../../docs/framework/data/adonet/dataset-datatable-dataview/defining-primary-keys.md).  
  
> [!CAUTION]
>  Si un nom de colonne n’est pas fourni pour une colonne, la colonne reçoit un nom incrémentiel par défaut de la colonne*N,* à partir de « Column1 », lorsqu’il est ajouté à la **DataColumnCollection**. Nous vous recommandons d’éviter la convention d’affectation de noms de « colonne*N*» lorsque vous fournissez un nom de colonne, étant donné que le nom fourni peut entrer en conflit avec un nom de colonne par défaut existant dans le **DataColumnCollection**. Si le nom fourni existe déjà, une exception est levée.  
  
 Si vous utilisez <xref:System.Xml.Linq.XElement> en tant que <xref:System.Data.DataColumn.DataType%2A> d'un <xref:System.Data.DataColumn> dans <xref:System.Data.DataTable>, la sérialisation XML ne fonctionnera pas lors de la lecture dans les données. Par exemple, si vous écrivez un <xref:System.Xml.XmlDocument> à l'aide de la méthode `DataTable.WriteXml`, lors de la sérialisation vers XML, un nœud parent supplémentaire est ajouté dans le <xref:System.Xml.Linq.XElement>. Pour contourner ce problème, utilisez le type <xref:System.Data.SqlTypes.SqlXml> à la place de <xref:System.Xml.Linq.XElement>. `ReadXml` et `WriteXml` fonctionnent correctement avec <xref:System.Data.SqlTypes.SqlXml>.  
  
## <a name="see-also"></a>Voir aussi

- <xref:System.Data.DataColumn>
- <xref:System.Data.DataColumnCollection>
- <xref:System.Data.DataTable>
- [Définition de schéma de DataTable](../../../../../docs/framework/data/adonet/dataset-datatable-dataview/datatable-schema-definition.md)
- [DataTables](../../../../../docs/framework/data/adonet/dataset-datatable-dataview/datatables.md)
- [Fournisseurs managés ADO.NET et centre de développement DataSet](https://go.microsoft.com/fwlink/?LinkId=217917)
