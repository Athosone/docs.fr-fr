---
title: 'Exemples de syntaxe de requête fondée sur une méthode : Regroupement'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
ms.assetid: cb23c25c-1075-4cc3-a8ff-4db72e536c0d
ms.openlocfilehash: 8f09983aa90be666cc13ae4eba018db2ae706daa
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59219224"
---
# <a name="method-based-query-syntax-examples-grouping"></a><span data-ttu-id="9700c-102">Exemples de syntaxe de requête fondée sur une méthode : Regroupement</span><span class="sxs-lookup"><span data-stu-id="9700c-102">Method-Based Query Syntax Examples: Grouping</span></span>
<span data-ttu-id="9700c-103">Les exemples de cette rubrique vous montrent comment utiliser le `GroupBy` méthode pour interroger le [AdventureWorks Sales Model](https://archive.codeplex.com/?p=msftdbprodsamples) à l’aide de la syntaxe de requête fondée sur une méthode.</span><span class="sxs-lookup"><span data-stu-id="9700c-103">The examples in this topic show you how to use the `GroupBy` method to query the [AdventureWorks Sales Model](https://archive.codeplex.com/?p=msftdbprodsamples) using method-based query syntax.</span></span> <span data-ttu-id="9700c-104">Le modèle de vente AdventureWorks Sales Model utilisé dans ces exemples est construit à partir des tables Contact, Address, Product, SalesOrderHeader et SalesOrderDetail de l'exemple de base de données AdventureWorks.</span><span class="sxs-lookup"><span data-stu-id="9700c-104">The AdventureWorks Sales Model that is used in these examples is built from the Contact, Address, Product, SalesOrderHeader, and SalesOrderDetail tables in the AdventureWorks sample database.</span></span>  
  
 <span data-ttu-id="9700c-105">Les exemples de cette rubrique utilisent les éléments suivants `using` / `Imports` instructions :</span><span class="sxs-lookup"><span data-stu-id="9700c-105">The examples in this topic use the following `using`/`Imports` statements:</span></span>  
  
 [!code-csharp[DP L2E Examples#ImportsUsing](../../../../../../samples/snippets/csharp/VS_Snippets_Data/DP L2E Examples/CS/Program.cs#importsusing)]
 [!code-vb[DP L2E Examples#ImportsUsing](../../../../../../samples/snippets/visualbasic/VS_Snippets_Data/DP L2E Examples/VB/Module1.vb#importsusing)]  
  
## <a name="example"></a><span data-ttu-id="9700c-106">Exemple</span><span class="sxs-lookup"><span data-stu-id="9700c-106">Example</span></span>  
 <span data-ttu-id="9700c-107">L'exemple suivant utilise la méthode `GroupBy` pour retourner les objets `Address` qui sont regroupés par code postal.</span><span class="sxs-lookup"><span data-stu-id="9700c-107">The following example uses the `GroupBy` method to return `Address` objects that are grouped by postal code.</span></span> <span data-ttu-id="9700c-108">Les résultats sont projetés dans un type anonyme.</span><span class="sxs-lookup"><span data-stu-id="9700c-108">The results are projected into an anonymous type.</span></span>  
  
 [!code-csharp[DP L2E Examples#GroupBySimple3_MQ](../../../../../../samples/snippets/csharp/VS_Snippets_Data/DP L2E Examples/CS/Program.cs#groupbysimple3_mq)]
 [!code-vb[DP L2E Examples#GroupBySimple3_MQ](../../../../../../samples/snippets/visualbasic/VS_Snippets_Data/DP L2E Examples/VB/Module1.vb#groupbysimple3_mq)]  
  
## <a name="example"></a><span data-ttu-id="9700c-109">Exemple</span><span class="sxs-lookup"><span data-stu-id="9700c-109">Example</span></span>  
 <span data-ttu-id="9700c-110">L'exemple suivant utilise la méthode `GroupBy` pour retourner les objets `Contact` qui sont regroupés en fonction de la première lettre du nom de famille des contacts.</span><span class="sxs-lookup"><span data-stu-id="9700c-110">The following example uses the `GroupBy` method to return `Contact` objects that are grouped by the first letter of the contact's last name.</span></span> <span data-ttu-id="9700c-111">Les résultats sont également triés selon la première lettre du nom de famille et projetés dans un type anonyme.</span><span class="sxs-lookup"><span data-stu-id="9700c-111">The results are also sorted by the first letter of the last name and projected into an anonymous type.</span></span>  
  
 [!code-csharp[DP L2E Examples#GroupBySimple2_MQ](../../../../../../samples/snippets/csharp/VS_Snippets_Data/DP L2E Examples/CS/Program.cs#groupbysimple2_mq)]
 [!code-vb[DP L2E Examples#GroupBySimple2_MQ](../../../../../../samples/snippets/visualbasic/VS_Snippets_Data/DP L2E Examples/VB/Module1.vb#groupbysimple2_mq)]  
  
## <a name="example"></a><span data-ttu-id="9700c-112">Exemple</span><span class="sxs-lookup"><span data-stu-id="9700c-112">Example</span></span>  
 <span data-ttu-id="9700c-113">L'exemple suivant utilise la méthode `GroupBy` pour retourner les objets `SalesOrderHeader` qui sont regroupés par code client (Customer ID).</span><span class="sxs-lookup"><span data-stu-id="9700c-113">The following example uses the `GroupBy` method to return `SalesOrderHeader` objects that are grouped by customer ID.</span></span> <span data-ttu-id="9700c-114">Le nombre de ventes réalisées pour chaque client est également retourné.</span><span class="sxs-lookup"><span data-stu-id="9700c-114">The number of sales for each customer is also returned.</span></span>  
  
 [!code-csharp[DP L2E Examples#GroupByCount_MQ](../../../../../../samples/snippets/csharp/VS_Snippets_Data/DP L2E Examples/CS/Program.cs#groupbycount_mq)]
 [!code-vb[DP L2E Examples#GroupByCount_MQ](../../../../../../samples/snippets/visualbasic/VS_Snippets_Data/DP L2E Examples/VB/Module1.vb#groupbycount_mq)]  
  
## <a name="see-also"></a><span data-ttu-id="9700c-115">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="9700c-115">See also</span></span>

- [<span data-ttu-id="9700c-116">Requêtes dans LINQ to Entities</span><span class="sxs-lookup"><span data-stu-id="9700c-116">Queries in LINQ to Entities</span></span>](../../../../../../docs/framework/data/adonet/ef/language-reference/queries-in-linq-to-entities.md)
