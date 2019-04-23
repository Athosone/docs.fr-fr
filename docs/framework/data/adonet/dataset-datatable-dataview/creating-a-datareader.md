---
title: Création d'un DataReader
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
ms.assetid: 49d4422a-7464-4ab8-8ec7-90185fde3ecf
ms.openlocfilehash: 8932f393af58f2014f643c5b6ebd6dc7a127b7eb
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59122003"
---
# <a name="creating-a-datareader"></a>Création d'un DataReader
Les classes <xref:System.Data.DataTable> et <xref:System.Data.DataSet> ont une méthode <xref:System.Data.DataTable.CreateDataReader%2A> qui retourne le contenu de la collection <xref:System.Data.DataTable> de l'objet <xref:System.Data.DataSet> ou de l'objet <xref:System.Data.DataSet.Tables%2A> sous la forme d'un ou plusieurs jeux de résultats en lecture seule et en avant uniquement.  
  
## <a name="example"></a>Exemple  
 L'application console suivante crée une instance de l'objet <xref:System.Data.DataTable>. Cet exemple passe ensuite le plein <xref:System.Data.DataTable> à une procédure qui appelle le <xref:System.Data.DataTable.CreateDataReader%2A> (méthode), qui effectue une itération dans les résultats contenus dans le <xref:System.Data.DataTableReader>.  
  
 [!code-csharp[DataWorks DataTable.CreateDataReader#1](../../../../../samples/snippets/csharp/VS_Snippets_ADO.NET/DataWorks DataTable.CreateDataReader/CS/source.cs#1)]
 [!code-vb[DataWorks DataTable.CreateDataReader#1](../../../../../samples/snippets/visualbasic/VS_Snippets_ADO.NET/DataWorks DataTable.CreateDataReader/VB/source.vb#1)]  
  
 L'exemple affiche la sortie suivante dans la fenêtre de console :  
  
```  
1 Mary  
2 Andy  
3 Peter  
4 Russ  
```  
  
## <a name="see-also"></a>Voir aussi

- <xref:System.Data.DataTable.CreateDataReader%2A>
- <xref:System.Data.DataSet.CreateDataReader%2A>
- [DataTableReaders](../../../../../docs/framework/data/adonet/dataset-datatable-dataview/datatablereaders.md)
- [Fournisseurs managés ADO.NET et centre de développement DataSet](https://go.microsoft.com/fwlink/?LinkId=217917)
