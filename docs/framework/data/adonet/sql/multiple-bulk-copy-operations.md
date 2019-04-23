---
title: Plusieurs opérations de copie en bloc
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
ms.assetid: 5ad12f94-7459-4a93-a421-4160d1a90715
ms.openlocfilehash: 405a82c625853d242ca68088ffdf81b6bcd7c518
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59209760"
---
# <a name="multiple-bulk-copy-operations"></a>Plusieurs opérations de copie en bloc
Vous pouvez effectuer des opérations de copie multiples en bloc à l'aide d'une seule instance d'une classe <xref:System.Data.SqlClient.SqlBulkCopy>. Si les paramètres d’opération changent entre les copies (par exemple, le nom de la table de destination), vous devez les mettre à jour avant tous les appels suivants à un de le **WriteToServer** méthodes, comme illustré dans l’exemple suivant. Sauf modification explicite, toutes les valeurs de propriété sont identiques à ce qu'elles étaient lors de l'opération de copie en bloc précédente pour une instance donnée.  
  
> [!NOTE]
>  L'exécution d'opérations de copie en bloc multiples à l'aide de la même instance de <xref:System.Data.SqlClient.SqlBulkCopy> est généralement plus efficace que l'utilisation d'une instance séparée pour chaque opération.  
  
 Si vous effectuez plusieurs opérations de copie en bloc à l'aide du même objet <xref:System.Data.SqlClient.SqlBulkCopy>, aucune restriction ne s'applique selon que les informations source ou cible sont identiques ou différentes dans chaque opération. Toutefois, vous devez veiller à ce que les informations d'association de colonne soient correctement définies chaque fois que vous écrivez sur le serveur.  
  
> [!IMPORTANT]
>  Cet exemple ne s’exécutera pas, sauf si vous avez créé les tables de travail comme décrit dans [exemple de configuration de copie en bloc](../../../../../docs/framework/data/adonet/sql/bulk-copy-example-setup.md). Ce code est fourni pour illustrer la syntaxe pour l’utilisation de **SqlBulkCopy** uniquement. Si les tables sources et de destination se trouvent dans la même instance SQL Server, il est plus facile et plus rapide d'utiliser une instruction Transact-SQL `INSERT … SELECT` pour copier les données.  
  
 [!code-csharp[DataWorks SqlBulkCopy.ColumnMappingOrdersDetails#1](../../../../../samples/snippets/csharp/VS_Snippets_ADO.NET/DataWorks SqlBulkCopy.ColumnMappingOrdersDetails/CS/source.cs#1)]
 [!code-vb[DataWorks SqlBulkCopy.ColumnMappingOrdersDetails#1](../../../../../samples/snippets/visualbasic/VS_Snippets_ADO.NET/DataWorks SqlBulkCopy.ColumnMappingOrdersDetails/VB/source.vb#1)]  
  
## <a name="see-also"></a>Voir aussi

- [Opérations de copie en bloc dans SQL Server](../../../../../docs/framework/data/adonet/sql/bulk-copy-operations-in-sql-server.md)
- [Fournisseurs managés ADO.NET et centre de développement DataSet](https://go.microsoft.com/fwlink/?LinkId=217917)
