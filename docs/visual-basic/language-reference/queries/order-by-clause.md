---
title: Order By, clause (Visual Basic)
ms.date: 07/20/2015
f1_keywords:
- vb.QueryOrderBy
- vb.QueryAscending
- vb.QueryDescending
helpviewer_keywords:
- queries [Visual Basic], Order By
- Order By clause [Visual Basic]
- Order By statement [Visual Basic]
ms.assetid: fa911282-6b81-44c7-acfa-46b5bb93df75
ms.openlocfilehash: 1c84a4cdb4a149154d459ca4d9c290ed360d1772
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "58835009"
---
# <a name="order-by-clause-visual-basic"></a><span data-ttu-id="a5d77-102">Order By, clause (Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="a5d77-102">Order By Clause (Visual Basic)</span></span>
<span data-ttu-id="a5d77-103">Spécifie l’ordre de tri pour un résultat de requête.</span><span class="sxs-lookup"><span data-stu-id="a5d77-103">Specifies the sort order for a query result.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="a5d77-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="a5d77-104">Syntax</span></span>  
  
```  
Order By orderExp1 [ Ascending | Descending ] [, orderExp2 [...] ]  
```  
  
## <a name="parts"></a><span data-ttu-id="a5d77-105">Composants</span><span class="sxs-lookup"><span data-stu-id="a5d77-105">Parts</span></span>  
 `orderExp1`  
 <span data-ttu-id="a5d77-106">Obligatoire.</span><span class="sxs-lookup"><span data-stu-id="a5d77-106">Required.</span></span> <span data-ttu-id="a5d77-107">Un ou plusieurs champs à partir du résultat de requête en cours qui identifient de manière de classer les valeurs retournées.</span><span class="sxs-lookup"><span data-stu-id="a5d77-107">One or more fields from the current query result that identify how to order the returned values.</span></span> <span data-ttu-id="a5d77-108">Les noms de champs doivent être séparés par des virgules (,).</span><span class="sxs-lookup"><span data-stu-id="a5d77-108">The field names must be separated by commas (,).</span></span> <span data-ttu-id="a5d77-109">Vous pouvez identifier chaque champ comme étant trié dans l’ordre croissant ou décroissant à l’aide de la `Ascending` ou `Descending` mots clés.</span><span class="sxs-lookup"><span data-stu-id="a5d77-109">You can identify each field as sorted in ascending or descending order by using the `Ascending` or `Descending` keywords.</span></span> <span data-ttu-id="a5d77-110">Si aucun `Ascending` ou `Descending` mot clé est spécifié, l’ordre de tri par défaut est croissant.</span><span class="sxs-lookup"><span data-stu-id="a5d77-110">If no `Ascending` or `Descending` keyword is specified, the default sort order is ascending.</span></span> <span data-ttu-id="a5d77-111">Les champs d’ordre de tri prévalent de gauche à droite.</span><span class="sxs-lookup"><span data-stu-id="a5d77-111">The sort order fields are given precedence from left to right.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="a5d77-112">Notes</span><span class="sxs-lookup"><span data-stu-id="a5d77-112">Remarks</span></span>  
 <span data-ttu-id="a5d77-113">Vous pouvez utiliser le `Order By` clause pour trier les résultats d’une requête.</span><span class="sxs-lookup"><span data-stu-id="a5d77-113">You can use the `Order By` clause to sort the results of a query.</span></span> <span data-ttu-id="a5d77-114">Le `Order By` clause peut trier seulement un résultat basé sur la variable de portée pour la portée actuelle.</span><span class="sxs-lookup"><span data-stu-id="a5d77-114">The `Order By` clause can only sort a result based on the range variable for the current scope.</span></span> <span data-ttu-id="a5d77-115">Par exemple, le `Select` clause introduit une nouvelle étendue dans une expression de requête avec de nouvelles variables d’itération pour cette portée.</span><span class="sxs-lookup"><span data-stu-id="a5d77-115">For example, the `Select` clause introduces a new scope in a query expression with new iteration variables for that scope.</span></span> <span data-ttu-id="a5d77-116">Plage des variables définies avant une `Select` clause dans une requête ne sont pas disponibles après la `Select` clause.</span><span class="sxs-lookup"><span data-stu-id="a5d77-116">Range variables defined before a `Select` clause in a query are not available after the `Select` clause.</span></span> <span data-ttu-id="a5d77-117">Par conséquent, si vous souhaitez classer vos résultats par un champ qui n’est pas disponible dans le `Select` clause, vous devez placer le `Order By` clause avant le `Select` clause.</span><span class="sxs-lookup"><span data-stu-id="a5d77-117">Therefore, if you want to order your results by a field that is not available in the `Select` clause, you must put the `Order By` clause before the `Select` clause.</span></span> <span data-ttu-id="a5d77-118">Un exemple de lorsque vous seriez obligé de le faire est lorsque vous souhaitez trier votre requête par champs qui ne sont pas retournées dans le cadre du résultat.</span><span class="sxs-lookup"><span data-stu-id="a5d77-118">One example of when you would have to do this is when you want to sort your query by fields that are not returned as part of the result.</span></span>  
  
 <span data-ttu-id="a5d77-119">Ordre croissant ou décroissant pour un champ est déterminé par l’implémentation de la <xref:System.IComparable> interface pour le type de données du champ.</span><span class="sxs-lookup"><span data-stu-id="a5d77-119">Ascending and descending order for a field is determined by the implementation of the <xref:System.IComparable> interface for the data type of the field.</span></span> <span data-ttu-id="a5d77-120">Si le type de données n’implémente pas le <xref:System.IComparable> interface, l’ordre de tri est ignoré.</span><span class="sxs-lookup"><span data-stu-id="a5d77-120">If the data type does not implement the <xref:System.IComparable> interface, the sort order is ignored.</span></span>  
  
## <a name="example"></a><span data-ttu-id="a5d77-121">Exemple</span><span class="sxs-lookup"><span data-stu-id="a5d77-121">Example</span></span>  
 <span data-ttu-id="a5d77-122">La requête suivante expression utilise un `From` clause pour déclarer une variable de portée `book` pour le `books` collection.</span><span class="sxs-lookup"><span data-stu-id="a5d77-122">The following query expression uses a `From` clause to declare a range variable `book` for the `books` collection.</span></span> <span data-ttu-id="a5d77-123">Le `Order By` clause trie les résultats de la requête par prix croissant (valeur par défaut).</span><span class="sxs-lookup"><span data-stu-id="a5d77-123">The `Order By` clause sorts the query result by price in ascending order (the default).</span></span> <span data-ttu-id="a5d77-124">La documentation avec le même prix est triée par titre dans l’ordre croissant.</span><span class="sxs-lookup"><span data-stu-id="a5d77-124">Books with the same price are sorted by title in ascending order.</span></span> <span data-ttu-id="a5d77-125">Le `Select` clause sélectionne le `Title` et `Price` propriétés que les valeurs retournées par la requête.</span><span class="sxs-lookup"><span data-stu-id="a5d77-125">The `Select` clause selects the `Title` and `Price` properties as the values returned by the query.</span></span>  
  
 [!code-vb[VbSimpleQuerySamples#24](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbSimpleQuerySamples/VB/QuerySamples1.vb#24)]  
  
## <a name="example"></a><span data-ttu-id="a5d77-126">Exemple</span><span class="sxs-lookup"><span data-stu-id="a5d77-126">Example</span></span>  
 <span data-ttu-id="a5d77-127">La requête suivante expression utilise le `Order By` clause pour trier le résultat de la requête par prix dans l’ordre décroissant.</span><span class="sxs-lookup"><span data-stu-id="a5d77-127">The following query expression uses the `Order By` clause to sort the query result by price in descending order.</span></span> <span data-ttu-id="a5d77-128">La documentation avec le même prix est triée par titre dans l’ordre croissant.</span><span class="sxs-lookup"><span data-stu-id="a5d77-128">Books with the same price are sorted by title in ascending order.</span></span>  
  
 [!code-vb[VbSimpleQuerySamples#25](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbSimpleQuerySamples/VB/QuerySamples1.vb#25)]  
  
## <a name="example"></a><span data-ttu-id="a5d77-129">Exemple</span><span class="sxs-lookup"><span data-stu-id="a5d77-129">Example</span></span>  
 <span data-ttu-id="a5d77-130">La requête suivante expression utilise un `Select` clause pour sélectionner le titre du livre, prix, date de publication et l’auteur.</span><span class="sxs-lookup"><span data-stu-id="a5d77-130">The following query expression uses a `Select` clause to select the book title, price, publish date, and author.</span></span> <span data-ttu-id="a5d77-131">Il remplit ensuite le `Title`, `Price`, `PublishDate`, et `Author` champs de la variable de portée de la nouvelle étendue.</span><span class="sxs-lookup"><span data-stu-id="a5d77-131">It then populates the `Title`, `Price`, `PublishDate`, and `Author` fields of the range variable for the new scope.</span></span> <span data-ttu-id="a5d77-132">Le `Order By` clause trie la nouvelle variable de portée de nom de l’auteur, titre de livre et ensuite le prix.</span><span class="sxs-lookup"><span data-stu-id="a5d77-132">The `Order By` clause orders the new range variable by author name, book title, and then price.</span></span> <span data-ttu-id="a5d77-133">Chaque colonne est triée dans l’ordre par défaut (croissant).</span><span class="sxs-lookup"><span data-stu-id="a5d77-133">Each column is sorted in the default order (ascending).</span></span>  
  
 [!code-vb[VbSimpleQuerySamples#26](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbSimpleQuerySamples/VB/QuerySamples1.vb#26)]  
  
## <a name="see-also"></a><span data-ttu-id="a5d77-134">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a5d77-134">See also</span></span>

- [<span data-ttu-id="a5d77-135">Introduction à LINQ en Visual Basic</span><span class="sxs-lookup"><span data-stu-id="a5d77-135">Introduction to LINQ in Visual Basic</span></span>](../../../visual-basic/programming-guide/language-features/linq/introduction-to-linq.md)
- [<span data-ttu-id="a5d77-136">Requêtes</span><span class="sxs-lookup"><span data-stu-id="a5d77-136">Queries</span></span>](../../../visual-basic/language-reference/queries/index.md)
- [<span data-ttu-id="a5d77-137">Select (clause)</span><span class="sxs-lookup"><span data-stu-id="a5d77-137">Select Clause</span></span>](../../../visual-basic/language-reference/queries/select-clause.md)
- [<span data-ttu-id="a5d77-138">From (clause)</span><span class="sxs-lookup"><span data-stu-id="a5d77-138">From Clause</span></span>](../../../visual-basic/language-reference/queries/from-clause.md)
