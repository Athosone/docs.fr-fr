---
title: Take While, clause (Visual Basic)
ms.date: 07/20/2015
f1_keywords:
- vb.QueryTakeWhile
helpviewer_keywords:
- queries [Visual Basic], Take While
- Take While clause [Visual Basic]
- Take While statement [Visual Basic]
ms.assetid: db8f9f2f-fc9f-4a6c-b0b8-1bf048147e11
ms.openlocfilehash: 080a106fc1deeb54165511ed03d7c7c5d2060f21
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "58818747"
---
# <a name="take-while-clause-visual-basic"></a><span data-ttu-id="15161-102">Take While, clause (Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="15161-102">Take While Clause (Visual Basic)</span></span>
<span data-ttu-id="15161-103">Inclut les éléments d’une collection tant qu’une condition spécifiée a la valeur `true` et ignore les éléments restants.</span><span class="sxs-lookup"><span data-stu-id="15161-103">Includes elements in a collection as long as a specified condition is `true` and bypasses the remaining elements.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="15161-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="15161-104">Syntax</span></span>  
  
```  
Take While expression  
```  
  
## <a name="parts"></a><span data-ttu-id="15161-105">Composants</span><span class="sxs-lookup"><span data-stu-id="15161-105">Parts</span></span>  
  
|<span data-ttu-id="15161-106">Terme</span><span class="sxs-lookup"><span data-stu-id="15161-106">Term</span></span>|<span data-ttu-id="15161-107">Définition</span><span class="sxs-lookup"><span data-stu-id="15161-107">Definition</span></span>|  
|---|---|  
|`expression`|<span data-ttu-id="15161-108">Obligatoire.</span><span class="sxs-lookup"><span data-stu-id="15161-108">Required.</span></span> <span data-ttu-id="15161-109">Une expression qui représente une condition pour tester des éléments.</span><span class="sxs-lookup"><span data-stu-id="15161-109">An expression that represents a condition to test elements for.</span></span> <span data-ttu-id="15161-110">L’expression doit retourner un `Boolean` valeur ou un équivalent fonctionnel, comme un `Integer` soit évaluée comme un `Boolean`.</span><span class="sxs-lookup"><span data-stu-id="15161-110">The expression must return a `Boolean` value or a functional equivalent, such as an `Integer` to be evaluated as a `Boolean`.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="15161-111">Notes</span><span class="sxs-lookup"><span data-stu-id="15161-111">Remarks</span></span>  
 <span data-ttu-id="15161-112">Le `Take While` clause inclut des éléments à partir du début d’un résultat de requête jusqu'à fourni `expression` retourne `false`.</span><span class="sxs-lookup"><span data-stu-id="15161-112">The `Take While` clause includes elements from the start of a query result until the supplied `expression` returns `false`.</span></span> <span data-ttu-id="15161-113">Après le `expression` retourne `false`, la requête ignore tous les éléments restants.</span><span class="sxs-lookup"><span data-stu-id="15161-113">After the `expression` returns `false`, the query will bypass all remaining elements.</span></span> <span data-ttu-id="15161-114">Le `expression` est ignoré pour les autres résultats.</span><span class="sxs-lookup"><span data-stu-id="15161-114">The `expression` is ignored for the remaining results.</span></span>  
  
 <span data-ttu-id="15161-115">Le `Take While` diffère de la clause le `Where` clause dans qui le `Where` clause peut être utilisée pour inclure tous les éléments à partir d’une requête qui remplissent une condition particulière.</span><span class="sxs-lookup"><span data-stu-id="15161-115">The `Take While` clause differs from the `Where` clause in that the `Where` clause can be used to include all elements from a query that meet a particular condition.</span></span> <span data-ttu-id="15161-116">Le `Take While` clause inclut des éléments uniquement jusqu'à la première fois que la condition n’est pas satisfaite.</span><span class="sxs-lookup"><span data-stu-id="15161-116">The `Take While` clause includes elements only until the first time that the condition is not satisfied.</span></span> <span data-ttu-id="15161-117">Le `Take While` clause est particulièrement utile lorsque vous travaillez avec un résultat de requête ordonnée.</span><span class="sxs-lookup"><span data-stu-id="15161-117">The `Take While` clause is most useful when you are working with an ordered query result.</span></span>  
  
## <a name="example"></a><span data-ttu-id="15161-118">Exemple</span><span class="sxs-lookup"><span data-stu-id="15161-118">Example</span></span>  
 <span data-ttu-id="15161-119">Le code suivant exemple utilise le `Take While` clause pour récupérer les résultats jusqu'à ce que le premier client sans commande est trouvé.</span><span class="sxs-lookup"><span data-stu-id="15161-119">The following code example uses the `Take While` clause to retrieve results until the first customer without any orders is found.</span></span>  
  
 [!code-vb[VbSimpleQuerySamples#2](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbSimpleQuerySamples/VB/QuerySamples1.vb#2)]  
  
## <a name="see-also"></a><span data-ttu-id="15161-120">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="15161-120">See also</span></span>

- [<span data-ttu-id="15161-121">Introduction à LINQ en Visual Basic</span><span class="sxs-lookup"><span data-stu-id="15161-121">Introduction to LINQ in Visual Basic</span></span>](../../../visual-basic/programming-guide/language-features/linq/introduction-to-linq.md)
- [<span data-ttu-id="15161-122">Requêtes</span><span class="sxs-lookup"><span data-stu-id="15161-122">Queries</span></span>](../../../visual-basic/language-reference/queries/index.md)
- [<span data-ttu-id="15161-123">Select (clause)</span><span class="sxs-lookup"><span data-stu-id="15161-123">Select Clause</span></span>](../../../visual-basic/language-reference/queries/select-clause.md)
- [<span data-ttu-id="15161-124">From (clause)</span><span class="sxs-lookup"><span data-stu-id="15161-124">From Clause</span></span>](../../../visual-basic/language-reference/queries/from-clause.md)
- [<span data-ttu-id="15161-125">Take (clause)</span><span class="sxs-lookup"><span data-stu-id="15161-125">Take Clause</span></span>](../../../visual-basic/language-reference/queries/take-clause.md)
- [<span data-ttu-id="15161-126">Skip While (clause)</span><span class="sxs-lookup"><span data-stu-id="15161-126">Skip While Clause</span></span>](../../../visual-basic/language-reference/queries/skip-while-clause.md)
- [<span data-ttu-id="15161-127">Where (clause)</span><span class="sxs-lookup"><span data-stu-id="15161-127">Where Clause</span></span>](../../../visual-basic/language-reference/queries/where-clause.md)
