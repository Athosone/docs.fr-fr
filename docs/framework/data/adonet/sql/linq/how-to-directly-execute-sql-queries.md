---
title: 'Procédure : Exécuter directement des requêtes SQL'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
ms.assetid: e491b9bf-741a-4296-9f51-76c25ddf6a82
ms.openlocfilehash: 6423959ed5036cc8ab2a88bb7273ef7aa95c8958
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62037763"
---
# <a name="how-to-directly-execute-sql-queries"></a><span data-ttu-id="2ba10-102">Procédure : Exécuter directement des requêtes SQL</span><span class="sxs-lookup"><span data-stu-id="2ba10-102">How to: Directly Execute SQL Queries</span></span>
[!INCLUDE[vbtecdlinq](../../../../../../includes/vbtecdlinq-md.md)] <span data-ttu-id="2ba10-103">traduit les requêtes que vous écrivez dans les requêtes SQL paramétrées (sous forme textuelle) et les envoie au serveur SQL pour traitement.</span><span class="sxs-lookup"><span data-stu-id="2ba10-103">translates the queries you write into parameterized SQL queries (in text form) and sends them to the SQL server for processing.</span></span>  
  
 <span data-ttu-id="2ba10-104">SQL ne peut pas exécuter les diverses méthodes qui peuvent être localement disponibles pour votre application.</span><span class="sxs-lookup"><span data-stu-id="2ba10-104">SQL cannot execute the variety of methods that might be locally available to your application.</span></span> [!INCLUDE[vbtecdlinq](../../../../../../includes/vbtecdlinq-md.md)] <span data-ttu-id="2ba10-105">essaie de convertir ces méthodes locales en opérations et fonctions équivalentes qui sont disponibles à l'intérieur de l'environnement SQL.</span><span class="sxs-lookup"><span data-stu-id="2ba10-105">tries to convert these local methods to equivalent operations and functions that are available inside the SQL environment.</span></span> <span data-ttu-id="2ba10-106">La plupart des méthodes et opérateurs sur les types intégrés [!INCLUDE[dnprdnshort](../../../../../../includes/dnprdnshort-md.md)] ont des traductions directes en commandes SQL.</span><span class="sxs-lookup"><span data-stu-id="2ba10-106">Most methods and operators on [!INCLUDE[dnprdnshort](../../../../../../includes/dnprdnshort-md.md)] built-in types have direct translations to SQL commands.</span></span> <span data-ttu-id="2ba10-107">Certains peuvent être produits à partir des fonctions disponibles.</span><span class="sxs-lookup"><span data-stu-id="2ba10-107">Some can be produced from the functions that are available.</span></span> <span data-ttu-id="2ba10-108">Ceux qui ne peuvent pas être produits génèrent des exceptions runtime.</span><span class="sxs-lookup"><span data-stu-id="2ba10-108">Those that cannot be produced generate run-time exceptions.</span></span> <span data-ttu-id="2ba10-109">Pour plus d’informations, consultez [le mappage de Type SQL-CLR](../../../../../../docs/framework/data/adonet/sql/linq/sql-clr-type-mapping.md).</span><span class="sxs-lookup"><span data-stu-id="2ba10-109">For more information, see [SQL-CLR Type Mapping](../../../../../../docs/framework/data/adonet/sql/linq/sql-clr-type-mapping.md).</span></span>  
  
 <span data-ttu-id="2ba10-110">Dans les cas où une requête [!INCLUDE[vbtecdlinq](../../../../../../includes/vbtecdlinq-md.md)] est insuffisante pour une tâche spécialisée, vous pouvez utiliser la méthode <xref:System.Data.Linq.DataContext.ExecuteQuery%2A> pour exécuter une requête SQL, puis convertir directement le résultat de votre requête en objets.</span><span class="sxs-lookup"><span data-stu-id="2ba10-110">In cases where a [!INCLUDE[vbtecdlinq](../../../../../../includes/vbtecdlinq-md.md)] query is insufficient for a specialized task, you can use the <xref:System.Data.Linq.DataContext.ExecuteQuery%2A> method to execute a SQL query, and then convert the result of your query directly into objects.</span></span>  
  
## <a name="example"></a><span data-ttu-id="2ba10-111">Exemple</span><span class="sxs-lookup"><span data-stu-id="2ba10-111">Example</span></span>  
 <span data-ttu-id="2ba10-112">Dans l'exemple suivant, supposons que les données de la classe `Customer` sont réparties sur deux tables (customer1 et customer2).</span><span class="sxs-lookup"><span data-stu-id="2ba10-112">In the following example, assume that the data for the `Customer` class is spread over two tables (customer1 and customer2).</span></span> <span data-ttu-id="2ba10-113">La requête retourne une séquence d'objets `Customer`.</span><span class="sxs-lookup"><span data-stu-id="2ba10-113">The query returns a sequence of `Customer` objects.</span></span>  
  
 [!code-csharp[DLinqQuerying#4](../../../../../../samples/snippets/csharp/VS_Snippets_Data/DLinqQuerying/cs/Program.cs#4)]
 [!code-vb[DLinqQuerying#4](../../../../../../samples/snippets/visualbasic/VS_Snippets_Data/DLinqQuerying/vb/Module1.vb#4)]  
  
 <span data-ttu-id="2ba10-114">Tant que les noms de colonne dans les résultats sous forme de tableau correspondent aux propriétés des colonnes de votre classe d’entité, [!INCLUDE[vbtecdlinq](../../../../../../includes/vbtecdlinq-md.md)] crée vos objets à partir de n’importe quelle requête SQL.</span><span class="sxs-lookup"><span data-stu-id="2ba10-114">As long as the column names in the tabular results match column properties of your entity class, [!INCLUDE[vbtecdlinq](../../../../../../includes/vbtecdlinq-md.md)] creates your objects out of any SQL query.</span></span>  
  
## <a name="example"></a><span data-ttu-id="2ba10-115">Exemple</span><span class="sxs-lookup"><span data-stu-id="2ba10-115">Example</span></span>  
 <span data-ttu-id="2ba10-116">La méthode <xref:System.Data.Linq.DataContext.ExecuteQuery%2A> autorise également les paramètres.</span><span class="sxs-lookup"><span data-stu-id="2ba10-116">The <xref:System.Data.Linq.DataContext.ExecuteQuery%2A> method also allows for parameters.</span></span> <span data-ttu-id="2ba10-117">Utilisez un code similaire à l'exemple de code suivant pour exécuter une requête paramétrée.</span><span class="sxs-lookup"><span data-stu-id="2ba10-117">Use code such as the following to execute a parameterized query.</span></span>  
  
 [!code-csharp[DLinqQuerying#5](../../../../../../samples/snippets/csharp/VS_Snippets_Data/DLinqQuerying/cs/Program.cs#5)]
 [!code-vb[DLinqQuerying#5](../../../../../../samples/snippets/visualbasic/VS_Snippets_Data/DLinqQuerying/vb/Module1.vb#5)]  
  
 <span data-ttu-id="2ba10-118">Les paramètres sont exprimés dans le texte de requête en utilisant la même notation avec accolades utilisée par `Console.WriteLine()` et `String.Format()`.</span><span class="sxs-lookup"><span data-stu-id="2ba10-118">The parameters are expressed in the query text by using the same curly notation used by `Console.WriteLine()` and `String.Format()`.</span></span> <span data-ttu-id="2ba10-119">En fait, `String.Format()` est réellement appelé sur la chaîne de requête que vous fournissez, en remplaçant les paramètres entre accolades avec générés tels que les noms de paramètres @p0, @p1 ..., @p(n).</span><span class="sxs-lookup"><span data-stu-id="2ba10-119">In fact, `String.Format()` is actually called on the query string you provide, substituting the curly braced parameters with generated parameter names such as @p0, @p1 …, @p(n).</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="2ba10-120">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="2ba10-120">See also</span></span>

- [<span data-ttu-id="2ba10-121">Informations générales</span><span class="sxs-lookup"><span data-stu-id="2ba10-121">Background Information</span></span>](../../../../../../docs/framework/data/adonet/sql/linq/background-information.md)
- [<span data-ttu-id="2ba10-122">Interrogation de la base de données</span><span class="sxs-lookup"><span data-stu-id="2ba10-122">Querying the Database</span></span>](../../../../../../docs/framework/data/adonet/sql/linq/querying-the-database.md)
