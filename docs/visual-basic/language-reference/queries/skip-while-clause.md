---
title: Skip While, clause (Visual Basic)
ms.date: 07/20/2015
f1_keywords:
- vb.QuerySkipWhile
helpviewer_keywords:
- Skip While statement [Visual Basic]
- Skip While clause [Visual Basic]
- queries [Visual Basic], Skip While
ms.assetid: 5dee8350-7520-4f1a-b00d-590cacd572d6
ms.openlocfilehash: 3d6caeb1938e8e53e8ec2575f740cd5e49496f62
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62054417"
---
# <a name="skip-while-clause-visual-basic"></a><span data-ttu-id="c7a9a-102">Skip While, clause (Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="c7a9a-102">Skip While Clause (Visual Basic)</span></span>
<span data-ttu-id="c7a9a-103">Ignore les éléments d’une collection tant qu’une condition spécifiée a la valeur `true`, puis retourne les éléments restants.</span><span class="sxs-lookup"><span data-stu-id="c7a9a-103">Bypasses elements in a collection as long as a specified condition is `true` and then returns the remaining elements.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="c7a9a-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="c7a9a-104">Syntax</span></span>  
  
```  
Skip While expression  
```  
  
## <a name="parts"></a><span data-ttu-id="c7a9a-105">Composants</span><span class="sxs-lookup"><span data-stu-id="c7a9a-105">Parts</span></span>  
  
|<span data-ttu-id="c7a9a-106">Terme</span><span class="sxs-lookup"><span data-stu-id="c7a9a-106">Term</span></span>|<span data-ttu-id="c7a9a-107">Définition</span><span class="sxs-lookup"><span data-stu-id="c7a9a-107">Definition</span></span>|  
|---|---|  
|`expression`|<span data-ttu-id="c7a9a-108">Obligatoire.</span><span class="sxs-lookup"><span data-stu-id="c7a9a-108">Required.</span></span> <span data-ttu-id="c7a9a-109">Une expression qui représente une condition pour tester des éléments.</span><span class="sxs-lookup"><span data-stu-id="c7a9a-109">An expression that represents a condition to test elements for.</span></span> <span data-ttu-id="c7a9a-110">L’expression doit retourner un `Boolean` valeur ou un équivalent fonctionnel, comme un `Integer` soit évaluée comme un `Boolean`.</span><span class="sxs-lookup"><span data-stu-id="c7a9a-110">The expression must return a `Boolean` value or a functional equivalent, such as an `Integer` to be evaluated as a `Boolean`.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="c7a9a-111">Notes</span><span class="sxs-lookup"><span data-stu-id="c7a9a-111">Remarks</span></span>  
 <span data-ttu-id="c7a9a-112">Le `Skip While` clause ignore des éléments à partir du début d’un résultat de requête jusqu'à ce que le texte fourni `expression` retourne `false`.</span><span class="sxs-lookup"><span data-stu-id="c7a9a-112">The `Skip While` clause bypasses elements from the beginning of a query result until the supplied `expression` returns `false`.</span></span> <span data-ttu-id="c7a9a-113">Après avoir `expression` retourne `false`, la requête retourne tous les éléments restants.</span><span class="sxs-lookup"><span data-stu-id="c7a9a-113">After `expression` returns `false`, the query returns all the remaining elements.</span></span> <span data-ttu-id="c7a9a-114">Le `expression` est ignoré pour les autres résultats.</span><span class="sxs-lookup"><span data-stu-id="c7a9a-114">The `expression` is ignored for the remaining results.</span></span>  
  
 <span data-ttu-id="c7a9a-115">Le `Skip While` clause diffère la `Where` clause dans qui le `Where` clause peut être utilisée pour exclure tous les éléments à partir d’une requête qui ne répondent pas à une condition particulière.</span><span class="sxs-lookup"><span data-stu-id="c7a9a-115">The `Skip While` clause differs from the `Where` clause in that the `Where` clause can be used to exclude all elements from a query that do not meet a particular condition.</span></span> <span data-ttu-id="c7a9a-116">Le `Skip While` clause exclut des éléments uniquement jusqu'à la première fois que la condition n’est pas satisfaite.</span><span class="sxs-lookup"><span data-stu-id="c7a9a-116">The `Skip While` clause excludes elements only until the first time that the condition is not satisfied.</span></span> <span data-ttu-id="c7a9a-117">Le `Skip While` clause est particulièrement utile lorsque vous travaillez avec un résultat de requête ordonnée.</span><span class="sxs-lookup"><span data-stu-id="c7a9a-117">The `Skip While` clause is most useful when you are working with an ordered query result.</span></span>  
  
 <span data-ttu-id="c7a9a-118">Vous pouvez ignorer un nombre spécifique de résultats à partir du début d’un résultat de requête à l’aide de la `Skip` clause.</span><span class="sxs-lookup"><span data-stu-id="c7a9a-118">You can bypass a specific number of results from the beginning of a query result by using the `Skip` clause.</span></span>  
  
## <a name="example"></a><span data-ttu-id="c7a9a-119">Exemple</span><span class="sxs-lookup"><span data-stu-id="c7a9a-119">Example</span></span>  
 <span data-ttu-id="c7a9a-120">Le code suivant exemple utilise le `Skip While` clause d’ignorer les résultats jusqu'à ce que le premier client à partir des États-Unis est trouvé.</span><span class="sxs-lookup"><span data-stu-id="c7a9a-120">The following code example uses the `Skip While` clause to bypass results until the first customer from the United States is found.</span></span>  
  
 [!code-vb[VbSimpleQuerySamples#3](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbSimpleQuerySamples/VB/QuerySamples1.vb#3)]  
  
## <a name="see-also"></a><span data-ttu-id="c7a9a-121">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c7a9a-121">See also</span></span>

- [<span data-ttu-id="c7a9a-122">Introduction à LINQ en Visual Basic</span><span class="sxs-lookup"><span data-stu-id="c7a9a-122">Introduction to LINQ in Visual Basic</span></span>](../../../visual-basic/programming-guide/language-features/linq/introduction-to-linq.md)
- [<span data-ttu-id="c7a9a-123">Requêtes</span><span class="sxs-lookup"><span data-stu-id="c7a9a-123">Queries</span></span>](../../../visual-basic/language-reference/queries/index.md)
- [<span data-ttu-id="c7a9a-124">Select (clause)</span><span class="sxs-lookup"><span data-stu-id="c7a9a-124">Select Clause</span></span>](../../../visual-basic/language-reference/queries/select-clause.md)
- [<span data-ttu-id="c7a9a-125">From (clause)</span><span class="sxs-lookup"><span data-stu-id="c7a9a-125">From Clause</span></span>](../../../visual-basic/language-reference/queries/from-clause.md)
- [<span data-ttu-id="c7a9a-126">Skip (clause)</span><span class="sxs-lookup"><span data-stu-id="c7a9a-126">Skip Clause</span></span>](../../../visual-basic/language-reference/queries/skip-clause.md)
- [<span data-ttu-id="c7a9a-127">Take While (clause)</span><span class="sxs-lookup"><span data-stu-id="c7a9a-127">Take While Clause</span></span>](../../../visual-basic/language-reference/queries/take-while-clause.md)
- [<span data-ttu-id="c7a9a-128">Where (clause)</span><span class="sxs-lookup"><span data-stu-id="c7a9a-128">Where Clause</span></span>](../../../visual-basic/language-reference/queries/where-clause.md)
