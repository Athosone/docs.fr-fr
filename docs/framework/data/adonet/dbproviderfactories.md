---
title: DbProviderFactories
ms.date: 03/30/2017
ms.assetid: 2a8e2640-3a49-42a1-a3a9-b43026907ae1
ms.openlocfilehash: 2376cf39228cb5e8208112333ba06bb80070de84
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59208811"
---
# <a name="dbproviderfactories"></a>DbProviderFactories
L'espace de noms <xref:System.Data.Common> fournit des classes permettant de créer des instances <xref:System.Data.Common.DbProviderFactory> afin d'utiliser des sources de données spécifiques. Lorsque vous créez une instance <xref:System.Data.Common.DbProviderFactory> et que vous lui passez des informations sur le fournisseur de données, `DbProviderFactory` peut déterminer l'objet de connexion fortement typé correct à retourner en fonction des informations qui lui ont été fournies.  
  
 Depuis .NET Framework version 4, les fournisseurs de données tels que <xref:System.Data.Odbc>, <xref:System.Data.OleDb>, <xref:System.Data.SqlClient> et <xref:System.Data.OracleClient> ne sont plus répertoriés dans le fichier machine.config, contrairement aux fournisseurs personnalisés qui continueront à y figurer.  
  
## <a name="in-this-section"></a>Dans cette section  
 [Vue d’ensemble du modèle Factory](../../../../docs/framework/data/adonet/factory-model-overview.md)  
 Fournit une vue d'ensemble du modèle de design factory et de l'interface de programmation.  
  
 [Obtention d’un DbProviderFactory](../../../../docs/framework/data/adonet/obtaining-a-dbproviderfactory.md)  
 Montre comment répertorier les fournisseurs de données installés et créer <xref:System.Data.Common.DbConnection> à partir de `DbProviderFactory`.  
  
 [DbConnection, DbCommand et DbException](../../../../docs/framework/data/adonet/dbconnection-dbcommand-and-dbexception.md)  
 Montre comment créer <xref:System.Data.Common.DbCommand> et <xref:System.Data.Common.DbDataReader> et comment gérer des erreurs de données à l'aide de <xref:System.Data.Common.DbException>.  
  
 [Modification des données avec un DbDataAdapter](../../../../docs/framework/data/adonet/modifying-data-with-a-dbdataadapter.md)  
 Montre comment utiliser <xref:System.Data.Common.DbCommandBuilder> avec <xref:System.Data.Common.DbDataAdapter> pour récupérer et modifier des données.  
  
## <a name="see-also"></a>Voir aussi

- [Extraction et modification de données dans ADO.NET](../../../../docs/framework/data/adonet/retrieving-and-modifying-data.md)
- [Fournisseurs managés ADO.NET et centre de développement DataSet](https://go.microsoft.com/fwlink/?LinkId=217917)
