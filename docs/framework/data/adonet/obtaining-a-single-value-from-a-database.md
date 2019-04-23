---
title: Obtention d'une valeur unique à partir d'une base de données
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
ms.assetid: b38526cd-a62a-48cb-822a-e91dfa68e02d
ms.openlocfilehash: 5eb81fd2a64f06f1252f71e251e58df568e7407c
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59120677"
---
# <a name="obtaining-a-single-value-from-a-database"></a><span data-ttu-id="d11b9-102">Obtention d'une valeur unique à partir d'une base de données</span><span class="sxs-lookup"><span data-stu-id="d11b9-102">Obtaining a Single Value from a Database</span></span>
<span data-ttu-id="d11b9-103">Vous aurez peut-être besoin de retourner des informations de base de données qui sont simplement une valeur unique plutôt qu'une table ou un flux de données.</span><span class="sxs-lookup"><span data-stu-id="d11b9-103">You may need to return database information that is simply a single value rather than in the form of a table or data stream.</span></span> <span data-ttu-id="d11b9-104">Par exemple, vous souhaitez retourner le résultat d’une fonction d’agrégation telles que COUNT (\*), SUM (price) ou AVG (Quantity).</span><span class="sxs-lookup"><span data-stu-id="d11b9-104">For example, you may want to return the result of an aggregate function such as COUNT(\*), SUM(Price), or AVG(Quantity).</span></span> <span data-ttu-id="d11b9-105">Le **commande** objet offre la possibilité de retourner des valeurs uniques à l’aide de la **ExecuteScalar** (méthode).</span><span class="sxs-lookup"><span data-stu-id="d11b9-105">The **Command** object provides the capability to return single values using the **ExecuteScalar** method.</span></span> <span data-ttu-id="d11b9-106">Le **ExecuteScalar** méthode est retournée, comme une valeur scalaire, la valeur de la première colonne de la première ligne du jeu de résultats.</span><span class="sxs-lookup"><span data-stu-id="d11b9-106">The **ExecuteScalar** method returns, as a scalar value, the value of the first column of the first row of the result set.</span></span>  
  
 <span data-ttu-id="d11b9-107">L'exemple de code suivant insère une nouvelle valeur dans la base de données en utilisant un objet <xref:System.Data.SqlClient.SqlCommand>.</span><span class="sxs-lookup"><span data-stu-id="d11b9-107">The following code example inserts a new value in the database using a <xref:System.Data.SqlClient.SqlCommand>.</span></span> <span data-ttu-id="d11b9-108">La méthode <xref:System.Data.SqlClient.SqlCommand.ExecuteScalar%2A> est utilisée pour retourner la valeur de la colonne d'identité de l'enregistrement inséré.</span><span class="sxs-lookup"><span data-stu-id="d11b9-108">The <xref:System.Data.SqlClient.SqlCommand.ExecuteScalar%2A> method is used to return the identity column value for the inserted record.</span></span>  
  
 [!code-csharp[DataWorks SqlCommand.ExecuteScalar#1](../../../../samples/snippets/csharp/VS_Snippets_ADO.NET/DataWorks SqlCommand.ExecuteScalar/CS/source.cs#1)]
 [!code-vb[DataWorks SqlCommand.ExecuteScalar#1](../../../../samples/snippets/visualbasic/VS_Snippets_ADO.NET/DataWorks SqlCommand.ExecuteScalar/VB/source.vb#1)]  
  
## <a name="see-also"></a><span data-ttu-id="d11b9-109">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d11b9-109">See also</span></span>

- [<span data-ttu-id="d11b9-110">Commandes et paramètres</span><span class="sxs-lookup"><span data-stu-id="d11b9-110">Commands and Parameters</span></span>](../../../../docs/framework/data/adonet/commands-and-parameters.md)
- [<span data-ttu-id="d11b9-111">Exécution d’une commande</span><span class="sxs-lookup"><span data-stu-id="d11b9-111">Executing a Command</span></span>](../../../../docs/framework/data/adonet/executing-a-command.md)
- [<span data-ttu-id="d11b9-112">DbConnection, DbCommand et DbException</span><span class="sxs-lookup"><span data-stu-id="d11b9-112">DbConnection, DbCommand and DbException</span></span>](../../../../docs/framework/data/adonet/dbconnection-dbcommand-and-dbexception.md)
- [<span data-ttu-id="d11b9-113">Fournisseurs managés ADO.NET et centre de développement DataSet</span><span class="sxs-lookup"><span data-stu-id="d11b9-113">ADO.NET Managed Providers and DataSet Developer Center</span></span>](https://go.microsoft.com/fwlink/?LinkId=217917)
