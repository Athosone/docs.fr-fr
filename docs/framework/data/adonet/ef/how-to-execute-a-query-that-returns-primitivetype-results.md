---
title: 'Procédure : Exécuter une requête qui retourne des résultats PrimitiveType'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
ms.assetid: 7139d585-4034-4dfa-916f-2120a8b72792
ms.openlocfilehash: 78d6c9287c5c69c41bd2f50abd8d57dcd1cb4e06
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61605805"
---
# <a name="how-to-execute-a-query-that-returns-primitivetype-results"></a><span data-ttu-id="6e169-102">Procédure : Exécuter une requête qui retourne des résultats PrimitiveType</span><span class="sxs-lookup"><span data-stu-id="6e169-102">How to: Execute a Query that Returns PrimitiveType Results</span></span>
<span data-ttu-id="6e169-103">Cette rubrique montre comment exécuter une commande par rapport à un modèle conceptuel en utilisant un objet <xref:System.Data.EntityClient.EntityCommand> et comment récupérer les résultats <xref:System.Data.Metadata.Edm.PrimitiveType> en utilisant un objet <xref:System.Data.EntityClient.EntityDataReader>.</span><span class="sxs-lookup"><span data-stu-id="6e169-103">This topic shows how to execute a command against a conceptual model by using an <xref:System.Data.EntityClient.EntityCommand>, and how to retrieve the <xref:System.Data.Metadata.Edm.PrimitiveType> results by using an <xref:System.Data.EntityClient.EntityDataReader>.</span></span>  
  
### <a name="to-run-the-code-in-this-example"></a><span data-ttu-id="6e169-104">Pour exécuter le code de cet exemple</span><span class="sxs-lookup"><span data-stu-id="6e169-104">To run the code in this example</span></span>  
  
1. <span data-ttu-id="6e169-105">Ajouter le [AdventureWorks Sales Model](https://github.com/Microsoft/sql-server-samples/releases/tag/adventureworks) à votre projet et configurez votre projet pour utiliser le [!INCLUDE[adonet_ef](../../../../../includes/adonet-ef-md.md)].</span><span class="sxs-lookup"><span data-stu-id="6e169-105">Add the [AdventureWorks Sales Model](https://github.com/Microsoft/sql-server-samples/releases/tag/adventureworks) to your project and configure your project to use the [!INCLUDE[adonet_ef](../../../../../includes/adonet-ef-md.md)].</span></span> <span data-ttu-id="6e169-106">Pour plus d'informations, voir [Procédure : Utilisez l’Assistant Entity Data Model](https://docs.microsoft.com/previous-versions/dotnet/netframework-4.0/bb738677(v=vs.100)).</span><span class="sxs-lookup"><span data-stu-id="6e169-106">For more information, see [How to: Use the Entity Data Model Wizard](https://docs.microsoft.com/previous-versions/dotnet/netframework-4.0/bb738677(v=vs.100)).</span></span>  
  
2. <span data-ttu-id="6e169-107">Dans la page de codes de votre application, ajoutez les instructions `using` (`Imports` en Visual Basic) suivantes :</span><span class="sxs-lookup"><span data-stu-id="6e169-107">In the code page for your application, add the following `using` statements (`Imports` in Visual Basic):</span></span>  
  
     [!code-csharp[DP EntityServices Concepts#Namespaces](../../../../../samples/snippets/csharp/VS_Snippets_Data/dp entityservices concepts/cs/source.cs#namespaces)]
     [!code-vb[DP EntityServices Concepts#Namespaces](../../../../../samples/snippets/visualbasic/VS_Snippets_Data/dp entityservices concepts/vb/source.vb#namespaces)]  
  
## <a name="example"></a><span data-ttu-id="6e169-108">Exemple</span><span class="sxs-lookup"><span data-stu-id="6e169-108">Example</span></span>  
 <span data-ttu-id="6e169-109">Cet exemple exécute une requête qui retourne des résultats <xref:System.Data.Metadata.Edm.PrimitiveType>.</span><span class="sxs-lookup"><span data-stu-id="6e169-109">This example executes a query that returns a <xref:System.Data.Metadata.Edm.PrimitiveType> result.</span></span> <span data-ttu-id="6e169-110">Si vous transmettez la requête suivante en tant qu’argument à la fonction `ExecutePrimitiveTypeQuery`, celle-ci affiche le tarif moyen de tous les produits (`Products`) :</span><span class="sxs-lookup"><span data-stu-id="6e169-110">If you pass the following query as an argument to the `ExecutePrimitiveTypeQuery` function, the function displays the average list price of all `Products`:</span></span>  
  
 [!code-csharp[DP EntityServices Concepts 2#EDM_AVG](../../../../../samples/snippets/csharp/VS_Snippets_Data/dp entityservices concepts 2/cs/entitysql.cs#edm_avg)]  
  
 <span data-ttu-id="6e169-111">Si vous transmettez une requête paramétrable, telle que la suivante, ajoutez les objets <xref:System.Data.EntityClient.EntityParameter> à la propriété <xref:System.Data.EntityClient.EntityCommand.Parameters%2A> sur l'objet <xref:System.Data.EntityClient.EntityCommand>.</span><span class="sxs-lookup"><span data-stu-id="6e169-111">If you pass a parameterized query, like the following, <xref:System.Data.EntityClient.EntityParameter> objects to the <xref:System.Data.EntityClient.EntityCommand.Parameters%2A> property on the <xref:System.Data.EntityClient.EntityCommand> object.</span></span>  
  
 [!code-csharp[DP EntityServices Concepts 2#CASE_WHEN_THEN_ELSE](../../../../../samples/snippets/csharp/VS_Snippets_Data/dp entityservices concepts 2/cs/entitysql.cs#case_when_then_else)]  
  
 [!code-csharp[DP EntityServices Concepts#eSQLPrimitiveTypes](../../../../../samples/snippets/csharp/VS_Snippets_Data/dp entityservices concepts/cs/source.cs#esqlprimitivetypes)]
 [!code-vb[DP EntityServices Concepts#eSQLPrimitiveTypes](../../../../../samples/snippets/visualbasic/VS_Snippets_Data/dp entityservices concepts/vb/source.vb#esqlprimitivetypes)]  
  
## <a name="see-also"></a><span data-ttu-id="6e169-112">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="6e169-112">See also</span></span>

- [<span data-ttu-id="6e169-113">Référence Entity SQL</span><span class="sxs-lookup"><span data-stu-id="6e169-113">Entity SQL Reference</span></span>](../../../../../docs/framework/data/adonet/ef/language-reference/entity-sql-reference.md)
- [<span data-ttu-id="6e169-114">Fournisseur EntityClient pour Entity Framework</span><span class="sxs-lookup"><span data-stu-id="6e169-114">EntityClient Provider for the Entity Framework</span></span>](../../../../../docs/framework/data/adonet/ef/entityclient-provider-for-the-entity-framework.md)
