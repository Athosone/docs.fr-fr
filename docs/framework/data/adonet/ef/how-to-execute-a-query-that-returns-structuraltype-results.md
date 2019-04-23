---
title: 'Procédure : Exécuter une requête qui retourne des résultats StructuralType'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
ms.assetid: 2314f2a2-b1c3-40c4-95bb-cdf9b21a7b53
ms.openlocfilehash: b306eaace09eda2c9bb3b88b793c48a6961b93e2
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59304729"
---
# <a name="how-to-execute-a-query-that-returns-structuraltype-results"></a>Procédure : Exécuter une requête qui retourne des résultats StructuralType
Cette rubrique montre comment exécuter une commande par rapport à un modèle conceptuel en utilisant un objet <xref:System.Data.EntityClient.EntityCommand> et comment récupérer les résultats de <xref:System.Data.Metadata.Edm.StructuralType> en utilisant un objet <xref:System.Data.EntityClient.EntityDataReader>. Les classes <xref:System.Data.Metadata.Edm.EntityType>, <xref:System.Data.Metadata.Edm.RowType> et <xref:System.Data.Metadata.Edm.ComplexType> sont dérivées de la classe <xref:System.Data.Metadata.Edm.StructuralType>.  
  
### <a name="to-run-the-code-in-this-example"></a>Pour exécuter le code de cet exemple  
  
1. Ajouter le [AdventureWorks Sales Model](https://github.com/Microsoft/sql-server-samples/releases/tag/adventureworks) à votre projet et configurez votre projet pour utiliser le [!INCLUDE[adonet_ef](../../../../../includes/adonet-ef-md.md)]. Pour plus d'informations, voir [Procédure : Utilisez l’Assistant Entity Data Model](https://docs.microsoft.com/previous-versions/dotnet/netframework-4.0/bb738677(v=vs.100)).  
  
2. Dans la page de codes de votre application, ajoutez les instructions `using` (`Imports` en Visual Basic) suivantes :  
  
     [!code-csharp[DP EntityServices Concepts#Namespaces](../../../../../samples/snippets/csharp/VS_Snippets_Data/dp entityservices concepts/cs/source.cs#namespaces)]
     [!code-vb[DP EntityServices Concepts#Namespaces](../../../../../samples/snippets/visualbasic/VS_Snippets_Data/dp entityservices concepts/vb/source.vb#namespaces)]  
  
## <a name="example"></a>Exemple  
 Cet exemple exécute une requête qui retourne des résultats <xref:System.Data.Metadata.Edm.EntityType>. Si vous transmettez la requête suivante en tant qu’argument à la fonction `ExecuteStructuralTypeQuery`, celle-ci affiche des détails sur l’objet `Products` :  
  
 [!code-csharp[DP EntityServices Concepts 2#SelectProduct](../../../../../samples/snippets/csharp/VS_Snippets_Data/dp entityservices concepts 2/cs/entitysql.cs#selectproduct)]  
  
 Si vous transmettez une requête paramétrable, telle que la suivante, ajoutez les objets <xref:System.Data.EntityClient.EntityParameter> à la propriété <xref:System.Data.EntityClient.EntityCommand.Parameters%2A> sur l'objet <xref:System.Data.EntityClient.EntityCommand>.  
  
 [!code-csharp[DP EntityServices Concepts 2#GREATER_OR_EQUALS](../../../../../samples/snippets/csharp/VS_Snippets_Data/dp entityservices concepts 2/cs/entitysql.cs#greater_or_equals)]  
  
 [!code-csharp[DP EntityServices Concepts#eSQLStructuralTypes](../../../../../samples/snippets/csharp/VS_Snippets_Data/dp entityservices concepts/cs/source.cs#esqlstructuraltypes)]
 [!code-vb[DP EntityServices Concepts#eSQLStructuralTypes](../../../../../samples/snippets/visualbasic/VS_Snippets_Data/dp entityservices concepts/vb/source.vb#esqlstructuraltypes)]  
  
## <a name="see-also"></a>Voir aussi

- [Référence Entity SQL](../../../../../docs/framework/data/adonet/ef/language-reference/entity-sql-reference.md)
- [Fournisseur EntityClient pour Entity Framework](../../../../../docs/framework/data/adonet/ef/entityclient-provider-for-the-entity-framework.md)
