---
title: Création d'un DataSet
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
ms.assetid: 57629d8f-393e-4677-8b83-29ffde27f5fc
ms.openlocfilehash: d2d17056e6dcd29ef9b5c5e8c3024a32fce32bd5
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61879877"
---
# <a name="creating-a-dataset"></a>Création d'un DataSet
Pour créer une instance d'un objet <xref:System.Data.DataSet>, appelez le constructeur de l'objet <xref:System.Data.DataSet>. Vous pouvez également spécifier un argument de nom. Si vous ne spécifiez pas de nom pour l'objet <xref:System.Data.DataSet>, le nom est défini sur « NewDataSet ».  
  
 Vous pouvez également créer un objet <xref:System.Data.DataSet> à partir d'un objet <xref:System.Data.DataSet> existant. Le nouvel objet <xref:System.Data.DataSet> peut être : une copie exacte de l'objet <xref:System.Data.DataSet> existant ; un clône de l'objet <xref:System.Data.DataSet> qui copie la structure relationnelle ou le schéma, mais sans aucune des données de l'objet <xref:System.Data.DataSet> existant ; un sous-ensemble de l'objet <xref:System.Data.DataSet>, qui ne contient que les lignes modifiées de l'objet <xref:System.Data.DataSet> existant, à l'aide de la méthode <xref:System.Data.DataSet.GetChanges%2A>. Pour plus d’informations, consultez [contenu d’un DataSet copie](../../../../../docs/framework/data/adonet/dataset-datatable-dataview/copying-dataset-contents.md).  
  
 L'exemple de code suivant montre comment construire une instance d'un objet <xref:System.Data.DataSet>.  
  
```vb  
Dim customerOrders As DataSet = New DataSet("CustomerOrders")  
```  
  
```csharp  
DataSet customerOrders = new DataSet("CustomerOrders");  
```  
  
## <a name="see-also"></a>Voir aussi

- [Remplissage d’un DataSet à partir d’un DataAdapter](../../../../../docs/framework/data/adonet/populating-a-dataset-from-a-dataadapter.md)
- [DataSets, DataTables et DataViews](../../../../../docs/framework/data/adonet/dataset-datatable-dataview/index.md)
- [Fournisseurs managés ADO.NET et centre de développement DataSet](https://go.microsoft.com/fwlink/?LinkId=217917)
