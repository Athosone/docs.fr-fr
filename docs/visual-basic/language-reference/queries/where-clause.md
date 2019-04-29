---
title: Where, clause (Visual Basic)
ms.date: 07/20/2015
f1_keywords:
- vb.QueryWhere
helpviewer_keywords:
- Where statement [Visual Basic]
- queries [Visual Basic], Where
- Where clause [Visual Basic]
ms.assetid: 48b5c2c5-3181-429c-8545-894296798c89
ms.openlocfilehash: 5632e69039baebb3d1f1fd90c04586d9e50fe40f
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61945208"
---
# <a name="where-clause-visual-basic"></a><span data-ttu-id="6257a-102">Where, clause (Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="6257a-102">Where Clause (Visual Basic)</span></span>
<span data-ttu-id="6257a-103">Spécifie la condition de filtrage pour une requête.</span><span class="sxs-lookup"><span data-stu-id="6257a-103">Specifies the filtering condition for a query.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="6257a-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="6257a-104">Syntax</span></span>  
  
```  
Where condition  
```  
  
## <a name="parts"></a><span data-ttu-id="6257a-105">Composants</span><span class="sxs-lookup"><span data-stu-id="6257a-105">Parts</span></span>  
 `condition`  
 <span data-ttu-id="6257a-106">Obligatoire.</span><span class="sxs-lookup"><span data-stu-id="6257a-106">Required.</span></span> <span data-ttu-id="6257a-107">Une expression qui détermine si les valeurs de l’élément actuel dans la collection sont inclus dans la collection de sortie.</span><span class="sxs-lookup"><span data-stu-id="6257a-107">An expression that determines whether the values for the current item in the collection are included in the output collection.</span></span> <span data-ttu-id="6257a-108">L’expression doit correspondre à un `Boolean` valeur ou l’équivalent d’un `Boolean` valeur.</span><span class="sxs-lookup"><span data-stu-id="6257a-108">The expression must evaluate to a `Boolean` value or the equivalent of a `Boolean` value.</span></span> <span data-ttu-id="6257a-109">Si la condition prend la valeur `True`, l’élément est inclus dans le résultat de la requête ; sinon, l’élément est exclu des résultats de la requête.</span><span class="sxs-lookup"><span data-stu-id="6257a-109">If the condition evaluates to `True`, the element is included in the query result; otherwise, the element is excluded from the query result.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="6257a-110">Notes</span><span class="sxs-lookup"><span data-stu-id="6257a-110">Remarks</span></span>  
 <span data-ttu-id="6257a-111">Le `Where` clause vous permet de filtrer les données de requête en sélectionnant uniquement les éléments qui répondent à certains critères.</span><span class="sxs-lookup"><span data-stu-id="6257a-111">The `Where` clause enables you to filter query data by selecting only elements that meet certain criteria.</span></span> <span data-ttu-id="6257a-112">Les éléments dont les valeurs font la `Where` clause soit évaluée comme `True` sont inclus dans le résultat de la requête ; autres éléments sont exclus.</span><span class="sxs-lookup"><span data-stu-id="6257a-112">Elements whose values cause the `Where` clause to evaluate to `True` are included in the query result; other elements are excluded.</span></span> <span data-ttu-id="6257a-113">L’expression qui est utilisée dans un `Where` clause doit correspondre à un `Boolean` ou l’équivalent d’un `Boolean`, comme un entier qui prend la valeur `False` lorsque sa valeur est égale à zéro.</span><span class="sxs-lookup"><span data-stu-id="6257a-113">The expression that is used in a `Where` clause must evaluate to a `Boolean` or the equivalent of a `Boolean`, such as an Integer that evaluates to `False` when its value is zero.</span></span> <span data-ttu-id="6257a-114">Vous pouvez combiner plusieurs expressions dans un `Where` clause à l’aide des opérateurs logiques tels que `And`, `Or`, `AndAlso`, `OrElse`, `Is`, et `IsNot`.</span><span class="sxs-lookup"><span data-stu-id="6257a-114">You can combine multiple expressions in a `Where` clause by using logical operators such as `And`, `Or`, `AndAlso`, `OrElse`, `Is`, and `IsNot`.</span></span>  
  
 <span data-ttu-id="6257a-115">Par défaut, les expressions de requête ne sont pas évaluées jusqu'à ce qu’ils sont accessibles, par exemple, lorsqu’ils sont liés aux données ou itérées via dans un `For` boucle.</span><span class="sxs-lookup"><span data-stu-id="6257a-115">By default, query expressions are not evaluated until they are accessed—for example, when they are data-bound or iterated through in a `For` loop.</span></span> <span data-ttu-id="6257a-116">Par conséquent, le `Where` clause n’est pas évaluée jusqu'à ce que la requête est accessible.</span><span class="sxs-lookup"><span data-stu-id="6257a-116">As a result, the `Where` clause is not evaluated until the query is accessed.</span></span> <span data-ttu-id="6257a-117">Si des valeurs externes à la requête sont utilisées dans le `Where` clause, vérifiez que la valeur appropriée est utilisée dans le `Where` clause au moment de la requête est exécutée.</span><span class="sxs-lookup"><span data-stu-id="6257a-117">If you have values external to the query that are used in the `Where` clause, ensure that the appropriate value is used in the `Where` clause at the time the query is executed.</span></span> <span data-ttu-id="6257a-118">Pour plus d’informations sur l’exécution des requêtes, consultez [écrire votre première requête LINQ](../../../visual-basic/programming-guide/concepts/linq/writing-your-first-linq-query.md).</span><span class="sxs-lookup"><span data-stu-id="6257a-118">For more information about query execution, see [Writing Your First LINQ Query](../../../visual-basic/programming-guide/concepts/linq/writing-your-first-linq-query.md).</span></span>  
  
 <span data-ttu-id="6257a-119">Vous pouvez appeler des fonctions dans un `Where` clause pour effectuer un calcul ou une opération sur une valeur de l’élément actuel dans la collection.</span><span class="sxs-lookup"><span data-stu-id="6257a-119">You can call functions within a `Where` clause to perform a calculation or operation on a value from the current element in the collection.</span></span> <span data-ttu-id="6257a-120">Appel d’une fonction un `Where` clause peut entraîner la requête doit être exécutée immédiatement lorsqu’il est défini à la place de lorsqu’il est accessible.</span><span class="sxs-lookup"><span data-stu-id="6257a-120">Calling a function in a `Where` clause can cause the query to be executed immediately when it is defined instead of when it is accessed.</span></span> <span data-ttu-id="6257a-121">Pour plus d’informations sur l’exécution des requêtes, consultez [écrire votre première requête LINQ](../../../visual-basic/programming-guide/concepts/linq/writing-your-first-linq-query.md).</span><span class="sxs-lookup"><span data-stu-id="6257a-121">For more information about query execution, see [Writing Your First LINQ Query](../../../visual-basic/programming-guide/concepts/linq/writing-your-first-linq-query.md).</span></span>  
  
## <a name="example"></a><span data-ttu-id="6257a-122">Exemple</span><span class="sxs-lookup"><span data-stu-id="6257a-122">Example</span></span>  
 <span data-ttu-id="6257a-123">La requête suivante expression utilise un `From` clause pour déclarer une variable de portée `cust` pour chaque `Customer` de l’objet dans le `customers` collection.</span><span class="sxs-lookup"><span data-stu-id="6257a-123">The following query expression uses a `From` clause to declare a range variable `cust` for each `Customer` object in the `customers` collection.</span></span> <span data-ttu-id="6257a-124">Le `Where` clause utilise la variable de portée pour restreindre la sortie aux clients à partir de la région spécifiée.</span><span class="sxs-lookup"><span data-stu-id="6257a-124">The `Where` clause uses the range variable to restrict the output to customers from the specified region.</span></span> <span data-ttu-id="6257a-125">Le `For Each` boucle affiche le nom de société pour chaque client dans le résultat de la requête.</span><span class="sxs-lookup"><span data-stu-id="6257a-125">The `For Each` loop displays the company name for each customer in the query result.</span></span>  
  
 [!code-vb[VbSimpleQuerySamples#23](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbSimpleQuerySamples/VB/QuerySamples1.vb#23)]  
  
## <a name="example"></a><span data-ttu-id="6257a-126">Exemple</span><span class="sxs-lookup"><span data-stu-id="6257a-126">Example</span></span>  
 <span data-ttu-id="6257a-127">L’exemple suivant utilise `And` et `Or` des opérateurs logiques dans le `Where` clause.</span><span class="sxs-lookup"><span data-stu-id="6257a-127">The following example uses `And` and `Or` logical operators in the `Where` clause.</span></span>  
  
 [!code-vb[VbSimpleQuerySamples#31](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbSimpleQuerySamples/VB/QuerySamples1.vb#31)]  
  
## <a name="see-also"></a><span data-ttu-id="6257a-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="6257a-128">See also</span></span>

- [<span data-ttu-id="6257a-129">Introduction à LINQ en Visual Basic</span><span class="sxs-lookup"><span data-stu-id="6257a-129">Introduction to LINQ in Visual Basic</span></span>](../../../visual-basic/programming-guide/language-features/linq/introduction-to-linq.md)
- [<span data-ttu-id="6257a-130">Requêtes</span><span class="sxs-lookup"><span data-stu-id="6257a-130">Queries</span></span>](../../../visual-basic/language-reference/queries/index.md)
- [<span data-ttu-id="6257a-131">From (clause)</span><span class="sxs-lookup"><span data-stu-id="6257a-131">From Clause</span></span>](../../../visual-basic/language-reference/queries/from-clause.md)
- [<span data-ttu-id="6257a-132">Select (clause)</span><span class="sxs-lookup"><span data-stu-id="6257a-132">Select Clause</span></span>](../../../visual-basic/language-reference/queries/select-clause.md)
- [<span data-ttu-id="6257a-133">For Each...Next (instruction)</span><span class="sxs-lookup"><span data-stu-id="6257a-133">For Each...Next Statement</span></span>](../../../visual-basic/language-reference/statements/for-each-next-statement.md)
