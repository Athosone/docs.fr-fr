---
title: Commandes et paramètres
ms.date: 03/30/2017
ms.assetid: b623f810-d871-49a5-b0f5-078cc3c34db6
ms.openlocfilehash: a769e8cbd5138e78136df018abe058ac6c568951
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59198125"
---
# <a name="commands-and-parameters"></a>Commandes et paramètres
Après avoir établi une connexion à une source de données, vous pouvez exécuter des commandes et retourner les résultats de la source de données à l'aide d'un objet <xref:System.Data.Common.DbCommand>. Vous pouvez créer une commande en utilisant l'un des constructeurs de commande du fournisseur de données .NET Framework avec lequel vous travaillez. Les constructeurs acceptent des arguments optionnels, comme une instruction SQL à exécuter au niveau de la source de données, un objet <xref:System.Data.Common.DbConnection> ou un objet <xref:System.Data.Common.DbTransaction>. Vous pouvez également configurer ces objets en tant que propriétés de la commande. Vous pouvez aussi créer une commande pour une connexion particulière à l'aide de la méthode <xref:System.Data.Common.DbConnection.CreateCommand%2A> d'un objet `DbConnection`. L'instruction SQL en cours d'exécution par la commande peut être configurée à l'aide de la propriété <xref:System.Data.Common.DbCommand.CommandText%2A>.  
  
 Chaque fournisseur de données .NET Framework inclus dans le .NET Framework possède un objet `Command`. Le fournisseur de données .NET Framework pour OLE DB inclut un objet <xref:System.Data.OleDb.OleDbCommand>, le fournisseur de données .NET Framework pour SQL Server inclut un objet <xref:System.Data.SqlClient.SqlCommand>, le fournisseur de données .NET Framework pour ODBC inclut un objet <xref:System.Data.Odbc.OdbcCommand> et le fournisseur de données .NET Framework pour Oracle inclut un objet <xref:System.Data.OracleClient.OracleCommand>.  
  
## <a name="in-this-section"></a>Dans cette section  
 [Exécution d’une commande](../../../../docs/framework/data/adonet/executing-a-command.md)  
 Décrit l'objet `Command` et son utilisation pour exécuter des requêtes et des commandes sur une source de données.  
  
 [Configuration des paramètres et des types de données des paramètres](../../../../docs/framework/data/adonet/configuring-parameters-and-parameter-data-types.md)  
 Décrit l'utilisation des paramètres `Command`, y compris la direction, les types de données et la syntaxe des paramètres.  
  
 [Génération de commandes avec CommandBuilders](../../../../docs/framework/data/adonet/generating-commands-with-commandbuilders.md)  
 Décrit l'utilisation de générateurs de commande pour générer automatiquement les commandes INSERT, UPDATE et DELETE pour un `DataAdapter` ayant une commande SELECT d'analyse unique.  
  
 [Obtention d’une valeur unique à partir d’une base de données](../../../../docs/framework/data/adonet/obtaining-a-single-value-from-a-database.md)  
 Décrit comment utiliser la méthode `ExecuteScalar` d'un objet `Command` pour retourner une valeur unique à partir d'une requête de base de données.  
  
 [Utilisation des commandes pour modifier les données](../../../../docs/framework/data/adonet/using-commands-to-modify-data.md)  
 Explique comment utiliser un fournisseur de données pour exécuter des procédures stockées ou des instructions DDL (Data Definition Language).  
  
## <a name="see-also"></a>Voir aussi

- [DataAdapters et DataReaders](../../../../docs/framework/data/adonet/dataadapters-and-datareaders.md)
- [DataSets, DataTables et DataViews](../../../../docs/framework/data/adonet/dataset-datatable-dataview/index.md)
- [Connexion à une source de données](../../../../docs/framework/data/adonet/connecting-to-a-data-source.md)
- [Fournisseurs managés ADO.NET et centre de développement DataSet](https://go.microsoft.com/fwlink/?LinkId=217917)
