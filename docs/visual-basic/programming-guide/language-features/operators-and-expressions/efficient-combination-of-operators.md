---
title: Association efficace d'opérateurs (Visual Basic)
ms.date: 07/20/2015
helpviewer_keywords:
- expressions [Visual Basic], parentheses
- operators [Visual Basic], associativity
- expressions [Visual Basic], operators
- operators [Visual Basic], precedence
- Visual Basic code, operators
- Visual Basic code, expressions
- operators [Visual Basic], complex expressions
- expressions [Visual Basic], complex
- parentheses [Visual Basic], complex expressions
- numeric expressions
ms.assetid: bd22340e-b5be-458b-8772-3916c02309a4
ms.openlocfilehash: 8f5dd6c56b3e4576b9d798e0e5e10b2996f558dc
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61864650"
---
# <a name="efficient-combination-of-operators-visual-basic"></a><span data-ttu-id="482f2-102">Association efficace d'opérateurs (Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="482f2-102">Efficient Combination of Operators (Visual Basic)</span></span>
<span data-ttu-id="482f2-103">Expressions complexes peuvent contenir plusieurs opérateurs distincts.</span><span class="sxs-lookup"><span data-stu-id="482f2-103">Complex expressions can contain many different operators.</span></span> <span data-ttu-id="482f2-104">L'exemple suivant illustre ce comportement.</span><span class="sxs-lookup"><span data-stu-id="482f2-104">The following example illustrates this.</span></span>  
  
 `x = (45 * (y + z)) ^ (2 / 85) * 5 + z`  
  
 <span data-ttu-id="482f2-105">Création d’expressions complexes tels que celui de l’exemple précédent nécessite une compréhension approfondie des règles de priorité des opérateurs.</span><span class="sxs-lookup"><span data-stu-id="482f2-105">Creating complex expressions such as the one in the preceding example requires a thorough understanding of the rules of operator precedence.</span></span> <span data-ttu-id="482f2-106">Pour plus d’informations, consultez [priorité des opérateurs en Visual Basic](../../../../visual-basic/language-reference/operators/operator-precedence.md).</span><span class="sxs-lookup"><span data-stu-id="482f2-106">For more information, see [Operator Precedence in Visual Basic](../../../../visual-basic/language-reference/operators/operator-precedence.md).</span></span>  
  
## <a name="parenthetical-expressions"></a><span data-ttu-id="482f2-107">Expressions entre parenthèses</span><span class="sxs-lookup"><span data-stu-id="482f2-107">Parenthetical Expressions</span></span>  
 <span data-ttu-id="482f2-108">Fréquence à laquelle vous souhaitez opérations dans un ordre différent de celui déterminé par la priorité des opérateurs.</span><span class="sxs-lookup"><span data-stu-id="482f2-108">Often you want operations to proceed in a different order from that determined by operator precedence.</span></span> <span data-ttu-id="482f2-109">Prenons l'exemple suivant.</span><span class="sxs-lookup"><span data-stu-id="482f2-109">Consider the following example.</span></span>  
  
 `x = z * y + 4`  
  
 <span data-ttu-id="482f2-110">L’exemple précédent multiplie `z` par `y`, puis ajoute le résultat à `4`.</span><span class="sxs-lookup"><span data-stu-id="482f2-110">The preceding example multiplies `z` by `y`, then adds the result to `4`.</span></span> <span data-ttu-id="482f2-111">Mais si vous souhaitez ajouter `y` et `4` avant de multiplier le résultat par `z`, vous pouvez substituer la priorité des opérateurs normale en utilisant des parenthèses.</span><span class="sxs-lookup"><span data-stu-id="482f2-111">But if you want to add `y` and `4` before multiplying the result by `z`, you can override normal operator precedence by using parentheses.</span></span> <span data-ttu-id="482f2-112">En plaçant une expression entre parenthèses, vous forcez cette expression soit évaluée en premier, quelle que soit la priorité des opérateurs.</span><span class="sxs-lookup"><span data-stu-id="482f2-112">By enclosing an expression in parentheses, you force that expression to be evaluated first, regardless of operator precedence.</span></span> <span data-ttu-id="482f2-113">Pour forcer l’exemple précédent pour effectuer l’ajout de tout d’abord, vous pouvez la réécrire dans l’exemple suivant.</span><span class="sxs-lookup"><span data-stu-id="482f2-113">To force the preceding example to do the addition first, you could rewrite it as in the following example.</span></span>  
  
 `x = z * (y + 4)`  
  
 <span data-ttu-id="482f2-114">L’exemple précédent ajoute `y` et `4`, puis multiplie cette somme par `z`.</span><span class="sxs-lookup"><span data-stu-id="482f2-114">The preceding example adds `y` and `4`, then multiplies that sum by `z`.</span></span>  
  
### <a name="nested-parenthetical-expressions"></a><span data-ttu-id="482f2-115">Expressions entre parenthèses imbriquées</span><span class="sxs-lookup"><span data-stu-id="482f2-115">Nested Parenthetical Expressions</span></span>  
 <span data-ttu-id="482f2-116">Vous pouvez imbriquer des expressions dans plusieurs niveaux de parenthèses pour substituer davantage la priorité.</span><span class="sxs-lookup"><span data-stu-id="482f2-116">You can nest expressions in multiple levels of parentheses to override precedence even further.</span></span> <span data-ttu-id="482f2-117">Les expressions plus imbriquées dans les parenthèses sont évaluées en premier, suivie de la prochaine plus profondément imbriquée, et ainsi de suite pour le moins profondément imbriquées et enfin les expressions en dehors des parenthèses.</span><span class="sxs-lookup"><span data-stu-id="482f2-117">The expressions most deeply nested in parentheses are evaluated first, followed by the next most deeply nested, and so on to the least deeply nested, and finally the expressions outside parentheses.</span></span> <span data-ttu-id="482f2-118">L'exemple suivant illustre ce comportement.</span><span class="sxs-lookup"><span data-stu-id="482f2-118">The following example illustrates this.</span></span>  
  
 `x = (z * 4) ^ (y * (z + 2))`  
  
 <span data-ttu-id="482f2-119">Dans l’exemple précédent, `z + 2` est évalué en premier, puis les autres expressions entre parenthèses.</span><span class="sxs-lookup"><span data-stu-id="482f2-119">In the preceding example, `z + 2` is evaluated first, then the other parenthetical expressions.</span></span> <span data-ttu-id="482f2-120">Élévation à la puissance, qui normalement prioritaire par rapport à l’addition ou multiplication, est évaluée en dernier dans cet exemple, car les autres expressions entre parenthèses.</span><span class="sxs-lookup"><span data-stu-id="482f2-120">Exponentiation, which normally has higher precedence than addition or multiplication, is evaluated last in this example because the other expressions are enclosed in parentheses.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="482f2-121">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="482f2-121">See also</span></span>

- [<span data-ttu-id="482f2-122">Opérateurs arithmétiques en Visual Basic</span><span class="sxs-lookup"><span data-stu-id="482f2-122">Arithmetic Operators in Visual Basic</span></span>](../../../../visual-basic/programming-guide/language-features/operators-and-expressions/arithmetic-operators.md)
- [<span data-ttu-id="482f2-123">Opérateurs de comparaison en Visual Basic</span><span class="sxs-lookup"><span data-stu-id="482f2-123">Comparison Operators in Visual Basic</span></span>](../../../../visual-basic/programming-guide/language-features/operators-and-expressions/comparison-operators.md)
- [<span data-ttu-id="482f2-124">Opérateurs logiques et au niveau du bit en Visual Basic</span><span class="sxs-lookup"><span data-stu-id="482f2-124">Logical and Bitwise Operators in Visual Basic</span></span>](../../../../visual-basic/programming-guide/language-features/operators-and-expressions/logical-and-bitwise-operators.md)
- [<span data-ttu-id="482f2-125">Opérateurs logiques/de bits (Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="482f2-125">Logical/Bitwise Operators (Visual Basic)</span></span>](../../../../visual-basic/language-reference/operators/logical-bitwise-operators.md)
- [<span data-ttu-id="482f2-126">Expressions booléennes</span><span class="sxs-lookup"><span data-stu-id="482f2-126">Boolean Expressions</span></span>](../../../../visual-basic/programming-guide/language-features/operators-and-expressions/boolean-expressions.md)
- [<span data-ttu-id="482f2-127">Comparaisons de valeurs</span><span class="sxs-lookup"><span data-stu-id="482f2-127">Value Comparisons</span></span>](../../../../visual-basic/programming-guide/language-features/operators-and-expressions/value-comparisons.md)
- [<span data-ttu-id="482f2-128">Guide pratique pour Calculer des valeurs numériques</span><span class="sxs-lookup"><span data-stu-id="482f2-128">How to: Calculate Numeric Values</span></span>](../../../../visual-basic/programming-guide/language-features/operators-and-expressions/how-to-calculate-numeric-values.md)
- [<span data-ttu-id="482f2-129">Priorité des opérateurs en Visual Basic</span><span class="sxs-lookup"><span data-stu-id="482f2-129">Operator Precedence in Visual Basic</span></span>](../../../../visual-basic/language-reference/operators/operator-precedence.md)
