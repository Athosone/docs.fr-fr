---
title: Suppression de DataRow
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
ms.assetid: c34f531d-4b9b-4071-b2d7-342c402aa586
ms.openlocfilehash: 57f51ada00bf24617ca3e295a010aae64f0aa849
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59196136"
---
# <a name="datarow-deletion"></a>Suppression de DataRow
Il existe deux méthodes que vous pouvez utiliser pour supprimer un <xref:System.Data.DataRow> à partir de l’objet une <xref:System.Data.DataTable> objet : le **supprimer** méthode de la <xref:System.Data.DataRowCollection> objet et le <xref:System.Data.DataRow.Delete%2A> méthode de la **DataRow**objet. Tandis que le <xref:System.Data.DataRowCollection.Remove%2A> supprime de la méthode un **DataRow** à partir de la **DataRowCollection**, le <xref:System.Data.DataRow.Delete%2A> méthode marque seulement la ligne pour suppression. La suppression réelle se produit lorsque l’application appelle le **AcceptChanges** (méthode). En utilisant <xref:System.Data.DataRow.Delete%2A>, vous pouvez vérifier par programme les lignes marquées pour suppression avant de les supprimer. Lorsqu'une ligne est marquée pour suppression, sa propriété <xref:System.Data.DataRow.RowState%2A> prend la valeur <xref:System.Data.DataRow.Delete%2A>.  
  
 Ni <xref:System.Data.DataRow.Delete%2A> ni <xref:System.Data.DataRowCollection.Remove%2A> ne doivent être appelées dans une boucle foreach lors de l'itération au sein d'un objet <xref:System.Data.DataRowCollection>. Ni <xref:System.Data.DataRow.Delete%2A> ni <xref:System.Data.DataRowCollection.Remove%2A> ne modifient l'état de la collection.  
  
 Lorsque vous utilisez un <xref:System.Data.DataSet> ou **DataTable** conjointement avec un **DataAdapter** et une source de données relationnelle, utilisez la **supprimer** méthode de la  **DataRow** pour supprimer la ligne. Le **supprimer** méthode marque la ligne comme étant **Deleted** dans le **DataSet** ou **DataTable** mais ne la supprime ne pas. Au lieu de cela, lorsque le **DataAdapter** rencontre une ligne marquée comme **Deleted**, il exécute son **DeleteCommand** méthode pour supprimer la ligne à la source de données. La ligne peut ensuite être définitivement supprimée à l’aide de la **AcceptChanges** (méthode). Si vous utilisez **supprimer** pour supprimer la ligne, la ligne est entièrement supprimée de la table, mais la **DataAdapter** ne supprimera pas la ligne à la source de données.  
  
 Le **supprimer** méthode de la **DataRowCollection** prend un **DataRow** en tant qu’argument et le supprime de la collection, comme illustré dans l’exemple suivant.  
  
```vb  
workTable.Rows.Remove(workRow)  
```  
  
```csharp  
workTable.Rows.Remove(workRow);  
```  
  
 En revanche, l’exemple suivant montre comment appeler le **supprimer** méthode sur un **DataRow** pour modifier son **RowState** à **Deleted** .  
  
```vb  
workRow.Delete  
```  
  
```csharp  
workRow.Delete();  
```  
  
 Si une ligne est marquée pour suppression et que vous appelez le **AcceptChanges** méthode de la **DataTable** de l’objet, la ligne est supprimée de la **DataTable**. En revanche, si vous appelez **RejectChanges**, le **RowState** de la ligne revient à qu’il avait avant d’être marqué en tant que **Deleted**.  
  
> [!NOTE]
>  Si le **RowState** d’un **DataRow** est **Added**, c'est-à-dire qu’elle vient d’être ajouté à la table, et il est alors marqué comme **Deleted**, il est supprimé de la table.  
  
## <a name="see-also"></a>Voir aussi

- <xref:System.Data.DataRow>
- <xref:System.Data.DataRowCollection>
- <xref:System.Data.DataTable>
- [Manipulation des données dans un DataTable](../../../../../docs/framework/data/adonet/dataset-datatable-dataview/manipulating-data-in-a-datatable.md)
- [Fournisseurs managés ADO.NET et centre de développement DataSet](https://go.microsoft.com/fwlink/?LinkId=217917)
