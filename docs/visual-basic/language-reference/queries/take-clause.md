---
title: Take, clause (Visual Basic)
ms.date: 07/20/2015
f1_keywords:
- vb.QueryTake
helpviewer_keywords:
- Take statement [Visual Basic]
- queries [Visual Basic], Take
- Take clause [Visual Basic]
ms.assetid: 77bf87b2-1476-4456-957f-fee922fbad8c
ms.openlocfilehash: cb109eaf43fee19b77ac690492b85919c9d78301
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62054391"
---
# <a name="take-clause-visual-basic"></a><span data-ttu-id="24f81-102">Take, clause (Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="24f81-102">Take Clause (Visual Basic)</span></span>
<span data-ttu-id="24f81-103">Retourne un nombre spécifié d'éléments contigus à partir du début d'une collection.</span><span class="sxs-lookup"><span data-stu-id="24f81-103">Returns a specified number of contiguous elements from the start of a collection.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="24f81-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="24f81-104">Syntax</span></span>  
  
```  
Take count  
```  
  
## <a name="parts"></a><span data-ttu-id="24f81-105">Composants</span><span class="sxs-lookup"><span data-stu-id="24f81-105">Parts</span></span>  
 `count`  
 <span data-ttu-id="24f81-106">Obligatoire.</span><span class="sxs-lookup"><span data-stu-id="24f81-106">Required.</span></span> <span data-ttu-id="24f81-107">Une valeur ou une expression qui correspond au nombre d’éléments de la séquence à retourner.</span><span class="sxs-lookup"><span data-stu-id="24f81-107">A value or an expression that evaluates to the number of elements of the sequence to return.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="24f81-108">Notes</span><span class="sxs-lookup"><span data-stu-id="24f81-108">Remarks</span></span>  
 <span data-ttu-id="24f81-109">Le `Take` clause entraîne une requête inclure un nombre spécifié d’éléments contigus à partir du début d’une liste de résultats.</span><span class="sxs-lookup"><span data-stu-id="24f81-109">The `Take` clause causes a query to include a specified number of contiguous elements from the start of a results list.</span></span> <span data-ttu-id="24f81-110">Le nombre d’éléments à inclure est spécifié par le `count` paramètre.</span><span class="sxs-lookup"><span data-stu-id="24f81-110">The number of elements to include is specified by the `count` parameter.</span></span>  
  
 <span data-ttu-id="24f81-111">Vous pouvez utiliser la `Take` clause avec le `Skip` clause pour retourner une plage de données à partir de n’importe quel segment d’une requête.</span><span class="sxs-lookup"><span data-stu-id="24f81-111">You can use the `Take` clause with the `Skip` clause to return a range of data from any segment of a query.</span></span> <span data-ttu-id="24f81-112">Pour ce faire, passez à l’index du premier élément de la plage à la `Skip` clause et la taille de la plage à la `Take` clause.</span><span class="sxs-lookup"><span data-stu-id="24f81-112">To do this, pass the index of the first element of the range to the `Skip` clause and the size of the range to the `Take` clause.</span></span> <span data-ttu-id="24f81-113">Dans ce cas, le `Take` clause doit être spécifiée après le `Skip` clause.</span><span class="sxs-lookup"><span data-stu-id="24f81-113">In this case, the `Take` clause must be specified after the `Skip` clause.</span></span>  
  
 <span data-ttu-id="24f81-114">Lorsque vous utilisez le `Take` clause dans une requête, vous devez également vous assurer que les résultats sont retournés dans un ordre qui permettra la `Take` clause pour inclure les résultats prévus.</span><span class="sxs-lookup"><span data-stu-id="24f81-114">When you use the `Take` clause in a query, you may also need to ensure that the results are returned in an order that will enable the `Take` clause to include the intended results.</span></span> <span data-ttu-id="24f81-115">Pour plus d’informations sur le classement des résultats de la requête, consultez [Clause Order By](../../../visual-basic/language-reference/queries/order-by-clause.md).</span><span class="sxs-lookup"><span data-stu-id="24f81-115">For more information about ordering query results, see [Order By Clause](../../../visual-basic/language-reference/queries/order-by-clause.md).</span></span>  
  
 <span data-ttu-id="24f81-116">Vous pouvez utiliser le `TakeWhile` clause pour spécifier que seuls certains éléments soient retournés, selon une condition fournie.</span><span class="sxs-lookup"><span data-stu-id="24f81-116">You can use the `TakeWhile` clause to specify that only certain elements be returned, depending on a supplied condition.</span></span>  
  
## <a name="example"></a><span data-ttu-id="24f81-117">Exemple</span><span class="sxs-lookup"><span data-stu-id="24f81-117">Example</span></span>  
 <span data-ttu-id="24f81-118">Le code suivant exemple utilise le `Take` clause conjointement avec le `Skip` clause pour retourner des données à partir d’une requête dans les pages.</span><span class="sxs-lookup"><span data-stu-id="24f81-118">The following code example uses the `Take` clause together with the `Skip` clause to return data from a query in pages.</span></span> <span data-ttu-id="24f81-119">La fonction GetCustomers utilise le `Skip` clause pour ignorer les clients dans la liste jusqu'à ce que le départ fournie valeur d’index et utilise le `Take` clause pour retourner une page de clients à partir de cette valeur d’index.</span><span class="sxs-lookup"><span data-stu-id="24f81-119">The GetCustomers function uses the `Skip` clause to bypass the customers in the list until the supplied starting index value, and uses the `Take` clause to return a page of customers starting from that index value.</span></span>  
  
 [!code-vb[VbSimpleQuerySamples#1](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbSimpleQuerySamples/VB/QuerySamples1.vb#1)]  
  
## <a name="see-also"></a><span data-ttu-id="24f81-120">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="24f81-120">See also</span></span>

- [<span data-ttu-id="24f81-121">Introduction à LINQ en Visual Basic</span><span class="sxs-lookup"><span data-stu-id="24f81-121">Introduction to LINQ in Visual Basic</span></span>](../../../visual-basic/programming-guide/language-features/linq/introduction-to-linq.md)
- [<span data-ttu-id="24f81-122">Requêtes</span><span class="sxs-lookup"><span data-stu-id="24f81-122">Queries</span></span>](../../../visual-basic/language-reference/queries/index.md)
- [<span data-ttu-id="24f81-123">Select (clause)</span><span class="sxs-lookup"><span data-stu-id="24f81-123">Select Clause</span></span>](../../../visual-basic/language-reference/queries/select-clause.md)
- [<span data-ttu-id="24f81-124">From (clause)</span><span class="sxs-lookup"><span data-stu-id="24f81-124">From Clause</span></span>](../../../visual-basic/language-reference/queries/from-clause.md)
- [<span data-ttu-id="24f81-125">Order By (clause)</span><span class="sxs-lookup"><span data-stu-id="24f81-125">Order By Clause</span></span>](../../../visual-basic/language-reference/queries/order-by-clause.md)
- [<span data-ttu-id="24f81-126">Take While (clause)</span><span class="sxs-lookup"><span data-stu-id="24f81-126">Take While Clause</span></span>](../../../visual-basic/language-reference/queries/take-while-clause.md)
- [<span data-ttu-id="24f81-127">Skip (clause)</span><span class="sxs-lookup"><span data-stu-id="24f81-127">Skip Clause</span></span>](../../../visual-basic/language-reference/queries/skip-clause.md)
