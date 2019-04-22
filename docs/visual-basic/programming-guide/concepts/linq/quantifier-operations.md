---
title: Opérations de quantificateur (Visual Basic)
ms.date: 07/20/2015
ms.assetid: ae1a2b73-503c-4f4b-a3fd-31b5adbee67c
ms.openlocfilehash: e871a77caf0b7cfe361f11462085180c17bf2057
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "58816042"
---
# <a name="quantifier-operations-visual-basic"></a><span data-ttu-id="e450a-102">Opérations de quantificateur (Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="e450a-102">Quantifier Operations (Visual Basic)</span></span>
<span data-ttu-id="e450a-103">Les opérations de quantificateur retournent une valeur <xref:System.Boolean> qui indique si certains ou tous les éléments d’une séquence remplissent une condition.</span><span class="sxs-lookup"><span data-stu-id="e450a-103">Quantifier operations return a <xref:System.Boolean> value that indicates whether some or all of the elements in a sequence satisfy a condition.</span></span>  
  
 <span data-ttu-id="e450a-104">L’illustration suivante représente deux opérations de quantificateur différentes sur deux séquences sources différentes.</span><span class="sxs-lookup"><span data-stu-id="e450a-104">The following illustration depicts two different quantifier operations on two different source sequences.</span></span> <span data-ttu-id="e450a-105">La première opération demande si un ou plusieurs des éléments sont le caractère 'A' et le résultat est `true`.</span><span class="sxs-lookup"><span data-stu-id="e450a-105">The first operation asks if one or more of the elements are the character 'A', and the result is `true`.</span></span> <span data-ttu-id="e450a-106">La deuxième opération demande si tous les éléments sont le caractère 'A' et le résultat est `true`.</span><span class="sxs-lookup"><span data-stu-id="e450a-106">The second operation asks if all the elements are the character 'A', and the result is `true`.</span></span>  
  
 ![Opérations de quantificateur LINQ](./media/quantifier-operations/linq-quantifier-operations.png)  
  
 <span data-ttu-id="e450a-108">Les méthodes d’opérateur de requête standard qui effectuent des opérations de quantificateur sont répertoriées dans la section suivante.</span><span class="sxs-lookup"><span data-stu-id="e450a-108">The standard query operator methods that perform quantifier operations are listed in the following section.</span></span>  
  
## <a name="methods"></a><span data-ttu-id="e450a-109">Méthodes</span><span class="sxs-lookup"><span data-stu-id="e450a-109">Methods</span></span>  
  
|<span data-ttu-id="e450a-110">Nom de la méthode</span><span class="sxs-lookup"><span data-stu-id="e450a-110">Method Name</span></span>|<span data-ttu-id="e450a-111">Description</span><span class="sxs-lookup"><span data-stu-id="e450a-111">Description</span></span>|<span data-ttu-id="e450a-112">Syntaxe d’Expression de requête de Visual Basic</span><span class="sxs-lookup"><span data-stu-id="e450a-112">Visual Basic Query Expression Syntax</span></span>|<span data-ttu-id="e450a-113">Informations complémentaires</span><span class="sxs-lookup"><span data-stu-id="e450a-113">More Information</span></span>|  
|-----------------|-----------------|------------------------------------------|----------------------|  
|<span data-ttu-id="e450a-114">Tous</span><span class="sxs-lookup"><span data-stu-id="e450a-114">All</span></span>|<span data-ttu-id="e450a-115">Détermine si tous les éléments d’une séquence remplissent une condition.</span><span class="sxs-lookup"><span data-stu-id="e450a-115">Determines whether all the elements in a sequence satisfy a condition.</span></span>|`Aggregate … In … Into All(…)`|<xref:System.Linq.Enumerable.All%2A?displayProperty=nameWithType><br /><br /> <xref:System.Linq.Queryable.All%2A?displayProperty=nameWithType>|  
|<span data-ttu-id="e450a-116">Any</span><span class="sxs-lookup"><span data-stu-id="e450a-116">Any</span></span>|<span data-ttu-id="e450a-117">Détermine si certains éléments d’une séquence remplissent une condition.</span><span class="sxs-lookup"><span data-stu-id="e450a-117">Determines whether any elements in a sequence satisfy a condition.</span></span>|`Aggregate … In … Into Any()`|<xref:System.Linq.Enumerable.Any%2A?displayProperty=nameWithType><br /><br /> <xref:System.Linq.Queryable.Any%2A?displayProperty=nameWithType>|  
|<span data-ttu-id="e450a-118">Contient</span><span class="sxs-lookup"><span data-stu-id="e450a-118">Contains</span></span>|<span data-ttu-id="e450a-119">Détermine si une séquence contient un élément spécifié.</span><span class="sxs-lookup"><span data-stu-id="e450a-119">Determines whether a sequence contains a specified element.</span></span>|<span data-ttu-id="e450a-120">Non applicable.</span><span class="sxs-lookup"><span data-stu-id="e450a-120">Not applicable.</span></span>|<xref:System.Linq.Enumerable.Contains%2A?displayProperty=nameWithType><br /><br /> <xref:System.Linq.Queryable.Contains%2A?displayProperty=nameWithType>|  
  
## <a name="query-expression-syntax-examples"></a><span data-ttu-id="e450a-121">Exemples de syntaxe d'expression de requête</span><span class="sxs-lookup"><span data-stu-id="e450a-121">Query Expression Syntax Examples</span></span>  
 <span data-ttu-id="e450a-122">Ces exemples utilisent la `Aggregate` clause en Visual Basic en tant que partie de la condition de filtrage dans une requête LINQ.</span><span class="sxs-lookup"><span data-stu-id="e450a-122">These examples use the `Aggregate` clause in Visual Basic as part of the filtering condition in a LINQ query.</span></span>  
  
 <span data-ttu-id="e450a-123">L’exemple suivant utilise le `Aggregate` clause et la <xref:System.Linq.Enumerable.All%2A> méthode d’extension pour retourner à partir d’une collection de ces personnes dont les animaux domestiques sont tous dépassés un âge spécifié.</span><span class="sxs-lookup"><span data-stu-id="e450a-123">The following example uses the `Aggregate` clause and the <xref:System.Linq.Enumerable.All%2A> extension method to return from a collection those people whose pets are all older than a specified age.</span></span>  
  
 [!code-vb[CsLINQAnyAll#1](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/CsLINQAnyAll/VB/AnyAll.vb#1)]  
  
 <span data-ttu-id="e450a-124">L’exemple suivant utilise le `Aggregate` clause et la <xref:System.Linq.Enumerable.Any%2A> méthode d’extension pour retourner à partir d’une collection, les personnes qui ont au moins un animal domestique qui a dépassé un âge spécifié.</span><span class="sxs-lookup"><span data-stu-id="e450a-124">The next example uses the `Aggregate` clause and the <xref:System.Linq.Enumerable.Any%2A> extension method to return from a collection those people who have at least one pet that is older than a specified age.</span></span>  
  
 [!code-vb[CsLINQAnyAll#2](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/CsLINQAnyAll/VB/AnyAll.vb#2)]  
  
## <a name="see-also"></a><span data-ttu-id="e450a-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e450a-125">See also</span></span>

- <xref:System.Linq>
- [<span data-ttu-id="e450a-126">Vue d’ensemble des opérateurs de requête standard (Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="e450a-126">Standard Query Operators Overview (Visual Basic)</span></span>](../../../../visual-basic/programming-guide/concepts/linq/standard-query-operators-overview.md)
- [<span data-ttu-id="e450a-127">Aggregate (clause)</span><span class="sxs-lookup"><span data-stu-id="e450a-127">Aggregate Clause</span></span>](../../../../visual-basic/language-reference/queries/aggregate-clause.md)
- [<span data-ttu-id="e450a-128">Guide pratique pour Rechercher des phrases qui contiennent un ensemble spécifié de mots (LINQ) (Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="e450a-128">How to: Query for Sentences that Contain a Specified Set of Words (LINQ) (Visual Basic)</span></span>](../../../../visual-basic/programming-guide/concepts/linq/how-to-query-for-sentences-that-contain-a-specified-set-of-words.md)
