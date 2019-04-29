---
title: 'Exemples de syntaxe d’expression de requête : Opérateurs de jointure'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
ms.assetid: 343e8dda-70b2-409d-9334-ce9a880c3cea
ms.openlocfilehash: da583ed207a8c4fc9e061d517895ca0f2fea2f5e
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61613532"
---
# <a name="query-expression-syntax-examples-join-operators"></a><span data-ttu-id="c3e17-102">Exemples de syntaxe d’expression de requête : Opérateurs de jointure</span><span class="sxs-lookup"><span data-stu-id="c3e17-102">Query Expression Syntax Examples: Join Operators</span></span>
<span data-ttu-id="c3e17-103">La jointure est une opération importante dans les requêtes qui ciblent des sources de données qui n'ont pas de relations explorables les unes avec les autres, comme les tables de base de données relationnelles.</span><span class="sxs-lookup"><span data-stu-id="c3e17-103">Joining is an important operation in queries that target data sources that have no navigable relationships to each other, such as relational database tables.</span></span> <span data-ttu-id="c3e17-104">Une jointure de deux sources de données est l'association d'objets dans une source de données avec des objets qui partagent un attribut commun dans l'autre source de données.</span><span class="sxs-lookup"><span data-stu-id="c3e17-104">A join of two data sources is the association of objects in one data source with objects that share a common attribute in the other data source.</span></span> <span data-ttu-id="c3e17-105">Pour plus d’informations, consultez [vue d’ensemble des opérateurs de requête Standard](https://docs.microsoft.com/previous-versions/visualstudio/visual-studio-2013/bb397896(v=vs.120)).</span><span class="sxs-lookup"><span data-stu-id="c3e17-105">For more information, see [Standard Query Operators Overview](https://docs.microsoft.com/previous-versions/visualstudio/visual-studio-2013/bb397896(v=vs.120)).</span></span>  
  
 <span data-ttu-id="c3e17-106">Les exemples de cette rubrique montrent comment utiliser le <xref:System.Linq.Enumerable.GroupJoin%2A> et <xref:System.Linq.Enumerable.Join%2A> méthodes permettant d’interroger la [AdventureWorks Sales Model](https://archive.codeplex.com/?p=msftdbprodsamples) à l’aide de la syntaxe d’expression de requête.</span><span class="sxs-lookup"><span data-stu-id="c3e17-106">The examples in this topic demonstrate how to use the <xref:System.Linq.Enumerable.GroupJoin%2A> and <xref:System.Linq.Enumerable.Join%2A> methods to query the [AdventureWorks Sales Model](https://archive.codeplex.com/?p=msftdbprodsamples) using query expression syntax.</span></span> <span data-ttu-id="c3e17-107">Le modèle de vente AdventureWorks Sales Model utilisé dans ces exemples est construit à partir des tables Contact, Address, Product, SalesOrderHeader et SalesOrderDetail de l'exemple de base de données AdventureWorks.</span><span class="sxs-lookup"><span data-stu-id="c3e17-107">The AdventureWorks Sales Model used in these examples is built from the Contact, Address, Product, SalesOrderHeader, and SalesOrderDetail tables in the AdventureWorks sample database.</span></span>  
  
 <span data-ttu-id="c3e17-108">Les exemples de cette rubrique utilisent les éléments suivants `using` / `Imports` instructions :</span><span class="sxs-lookup"><span data-stu-id="c3e17-108">The examples in this topic use the following `using`/`Imports` statements:</span></span>  
  
 [!code-csharp[DP L2E Examples#ImportsUsing](../../../../../../samples/snippets/csharp/VS_Snippets_Data/DP L2E Examples/CS/Program.cs#importsusing)]
 [!code-vb[DP L2E Examples#ImportsUsing](../../../../../../samples/snippets/visualbasic/VS_Snippets_Data/DP L2E Examples/VB/Module1.vb#importsusing)]  
  
## <a name="groupjoin"></a><span data-ttu-id="c3e17-109">GroupJoin</span><span class="sxs-lookup"><span data-stu-id="c3e17-109">GroupJoin</span></span>  
  
### <a name="example"></a><span data-ttu-id="c3e17-110">Exemple</span><span class="sxs-lookup"><span data-stu-id="c3e17-110">Example</span></span>  
 <span data-ttu-id="c3e17-111">L'exemple ci-dessous effectue une jointure <xref:System.Linq.Enumerable.GroupJoin%2A> sur les tables SalesOrderHeader et SalesOrderDetail pour trouver le nombre de commandes par client.</span><span class="sxs-lookup"><span data-stu-id="c3e17-111">The following example performs a <xref:System.Linq.Enumerable.GroupJoin%2A> over the SalesOrderHeader and SalesOrderDetail tables to find the number of orders per customer.</span></span> <span data-ttu-id="c3e17-112">Une jointure de groupe est l'équivalent d'une jointure externe gauche qui retourne chaque élément de la première source de données (gauche), même s'il n'y a pas d'éléments corrélés dans l'autre source de données.</span><span class="sxs-lookup"><span data-stu-id="c3e17-112">A group join is the equivalent of a left outer join, which returns each element of the first (left) data source, even if no correlated elements are in the other data source.</span></span>  
  
 [!code-csharp[DP L2E Examples#GroupJoin2](../../../../../../samples/snippets/csharp/VS_Snippets_Data/DP L2E Examples/CS/Program.cs#groupjoin2)]
 [!code-vb[DP L2E Examples#GroupJoin2](../../../../../../samples/snippets/visualbasic/VS_Snippets_Data/DP L2E Examples/VB/Module1.vb#groupjoin2)]  
  
### <a name="example"></a><span data-ttu-id="c3e17-113">Exemple</span><span class="sxs-lookup"><span data-stu-id="c3e17-113">Example</span></span>  
 <span data-ttu-id="c3e17-114">L'exemple ci-dessous effectue une jointure <xref:System.Linq.Enumerable.GroupJoin%2A> sur les tables Contact et SalesOrderHeader pour trouver le nombre de commandes par contact.</span><span class="sxs-lookup"><span data-stu-id="c3e17-114">The following example performs a <xref:System.Linq.Enumerable.GroupJoin%2A> over the Contact and SalesOrderHeader tables to find the number of orders per contact.</span></span> <span data-ttu-id="c3e17-115">Le nombre de commandes et les ID de chaque contact sont affichés.</span><span class="sxs-lookup"><span data-stu-id="c3e17-115">The order count and IDs for each contact are displayed.</span></span>  
  
 [!code-csharp[DP L2E Examples#GroupJoin](../../../../../../samples/snippets/csharp/VS_Snippets_Data/DP L2E Examples/CS/Program.cs#groupjoin)]
 [!code-vb[DP L2E Examples#GroupJoin](../../../../../../samples/snippets/visualbasic/VS_Snippets_Data/DP L2E Examples/VB/Module1.vb#groupjoin)]  
  
## <a name="join"></a><span data-ttu-id="c3e17-116">Join</span><span class="sxs-lookup"><span data-stu-id="c3e17-116">Join</span></span>  
  
### <a name="example"></a><span data-ttu-id="c3e17-117">Exemple</span><span class="sxs-lookup"><span data-stu-id="c3e17-117">Example</span></span>  
 <span data-ttu-id="c3e17-118">L'exemple ci-dessous effectue une jointure sur les tables SalesOrderHeader et SalesOrderDetail pour obtenir les commandes en ligne du mois d'août.</span><span class="sxs-lookup"><span data-stu-id="c3e17-118">The following example performs a join over the SalesOrderHeader and SalesOrderDetail tables to get online orders from the month of August.</span></span>  
  
 [!code-csharp[DP L2E Examples#Join](../../../../../../samples/snippets/csharp/VS_Snippets_Data/DP L2E Examples/CS/Program.cs#join)]
 [!code-vb[DP L2E Examples#Join](../../../../../../samples/snippets/visualbasic/VS_Snippets_Data/DP L2E Examples/VB/Module1.vb#join)]  
  
## <a name="see-also"></a><span data-ttu-id="c3e17-119">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c3e17-119">See also</span></span>

- [<span data-ttu-id="c3e17-120">Requêtes dans LINQ to Entities</span><span class="sxs-lookup"><span data-stu-id="c3e17-120">Queries in LINQ to Entities</span></span>](../../../../../../docs/framework/data/adonet/ef/language-reference/queries-in-linq-to-entities.md)
