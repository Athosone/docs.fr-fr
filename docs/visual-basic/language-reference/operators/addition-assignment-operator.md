---
title: += (opérateur Visual Basic)
ms.date: 07/20/2015
f1_keywords:
- vb.+=
helpviewer_keywords:
- += operator [Visual Basic]
- assignment statements [Visual Basic], compound
- statements [Visual Basic], compound assignment
- += operator [Visual Basic], appending strings
- compound assignment statements [Visual Basic]
ms.assetid: d3e959f4-85d4-4e47-87c4-77b62335a5b3
ms.openlocfilehash: 4b8f36397d0f52866ebe9fa188d6b163364aeffc
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61608331"
---
# <a name="-operator-visual-basic"></a><span data-ttu-id="01bf5-102">+= (opérateur Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="01bf5-102">+= Operator (Visual Basic)</span></span>
<span data-ttu-id="01bf5-103">Ajoute la valeur d’une expression numérique à la valeur d’une propriété ou une variable numérique et assigne le résultat à la variable ou propriété.</span><span class="sxs-lookup"><span data-stu-id="01bf5-103">Adds the value of a numeric expression to the value of a numeric variable or property and assigns the result to the variable or property.</span></span> <span data-ttu-id="01bf5-104">Peut également être utilisé pour concaténer une `String` expression à une `String` variable ou propriété et assigner le résultat à la variable ou propriété.</span><span class="sxs-lookup"><span data-stu-id="01bf5-104">Can also be used to concatenate a `String` expression to a `String` variable or property and assign the result to the variable or property.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="01bf5-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="01bf5-105">Syntax</span></span>  
  
```  
variableorproperty += expression  
```  
  
## <a name="parts"></a><span data-ttu-id="01bf5-106">Composants</span><span class="sxs-lookup"><span data-stu-id="01bf5-106">Parts</span></span>  
 `variableorproperty`  
 <span data-ttu-id="01bf5-107">Obligatoire.</span><span class="sxs-lookup"><span data-stu-id="01bf5-107">Required.</span></span> <span data-ttu-id="01bf5-108">Toute numérique ou `String` variable ou propriété.</span><span class="sxs-lookup"><span data-stu-id="01bf5-108">Any numeric or `String` variable or property.</span></span>  
  
 `expression`  
 <span data-ttu-id="01bf5-109">Obligatoire.</span><span class="sxs-lookup"><span data-stu-id="01bf5-109">Required.</span></span> <span data-ttu-id="01bf5-110">Toute numérique ou `String` expression.</span><span class="sxs-lookup"><span data-stu-id="01bf5-110">Any numeric or `String` expression.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="01bf5-111">Notes</span><span class="sxs-lookup"><span data-stu-id="01bf5-111">Remarks</span></span>  
 <span data-ttu-id="01bf5-112">L’élément sur le côté gauche de la `+=` opérateur peut être une simple variable scalaire, une propriété ou un élément d’un tableau.</span><span class="sxs-lookup"><span data-stu-id="01bf5-112">The element on the left side of the `+=` operator can be a simple scalar variable, a property, or an element of an array.</span></span> <span data-ttu-id="01bf5-113">La variable ou la propriété ne peut pas être [ReadOnly](../../../visual-basic/language-reference/modifiers/readonly.md).</span><span class="sxs-lookup"><span data-stu-id="01bf5-113">The variable or property cannot be [ReadOnly](../../../visual-basic/language-reference/modifiers/readonly.md).</span></span>  
  
 <span data-ttu-id="01bf5-114">Le `+=` opérateur ajoute la valeur située à droite vers la variable ou propriété du côté gauche et assigne le résultat à la variable ou la propriété situé à sa gauche.</span><span class="sxs-lookup"><span data-stu-id="01bf5-114">The `+=` operator adds the value on its right to the variable or property on its left, and assigns the result to the variable or property on its left.</span></span> <span data-ttu-id="01bf5-115">Le `+=` opérateur peut également être utilisé pour concaténer les `String` expression située à droite vers le `String` variable ou une propriété sur la gauche et assigner le résultat à la variable ou propriété du côté gauche.</span><span class="sxs-lookup"><span data-stu-id="01bf5-115">The `+=` operator can also be used to concatenate the `String` expression on its right to the `String` variable or property on its left, and assign the result to the variable or property on its left.</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="01bf5-116">Lorsque vous utilisez le `+=` opérateur, vous ne pourrez pas être en mesure de déterminer si la concaténation d’addition ou la chaîne aura lieu.</span><span class="sxs-lookup"><span data-stu-id="01bf5-116">When you use the `+=` operator, you might not be able to determine whether addition or string concatenation will occur.</span></span> <span data-ttu-id="01bf5-117">Utilisez le `&=` opérateur de concaténation pour éliminer toute ambiguïté et pour fournir le code auto-documenté.</span><span class="sxs-lookup"><span data-stu-id="01bf5-117">Use the `&=` operator for concatenation to eliminate ambiguity and to provide self-documenting code.</span></span>  
  
 <span data-ttu-id="01bf5-118">Cet opérateur d’assignation effectue implicitement étendues, mais ne pas les conversions restrictives si l’environnement de compilation applique une sémantique stricte.</span><span class="sxs-lookup"><span data-stu-id="01bf5-118">This assignment operator implicitly performs widening but not narrowing conversions if the compilation environment enforces strict semantics.</span></span> <span data-ttu-id="01bf5-119">Pour plus d’informations sur ces conversions, consultez [Widening and Narrowing Conversions](../../../visual-basic/programming-guide/language-features/data-types/widening-and-narrowing-conversions.md).</span><span class="sxs-lookup"><span data-stu-id="01bf5-119">For more information on these conversions, see [Widening and Narrowing Conversions](../../../visual-basic/programming-guide/language-features/data-types/widening-and-narrowing-conversions.md).</span></span> <span data-ttu-id="01bf5-120">Pour plus d’informations sur les sémantiques strictes et permissives, consultez [Option Strict, instruction](../../../visual-basic/language-reference/statements/option-strict-statement.md).</span><span class="sxs-lookup"><span data-stu-id="01bf5-120">For more information on strict and permissive semantics, see [Option Strict Statement](../../../visual-basic/language-reference/statements/option-strict-statement.md).</span></span>  
  
 <span data-ttu-id="01bf5-121">Si la sémantique permissive est autorisée, le `+=` opérateur exécute implicitement un ensemble de conversions de chaîne et numériques identiques à ceux effectués par le `+` opérateur.</span><span class="sxs-lookup"><span data-stu-id="01bf5-121">If permissive semantics are allowed, the `+=` operator implicitly performs a variety of string and numeric conversions identical to those performed by the `+` operator.</span></span> <span data-ttu-id="01bf5-122">Pour plus d’informations sur ces conversions, consultez [opérateur +](../../../visual-basic/language-reference/operators/addition-operator.md).</span><span class="sxs-lookup"><span data-stu-id="01bf5-122">For details on these conversions, see [+ Operator](../../../visual-basic/language-reference/operators/addition-operator.md).</span></span>  
  
## <a name="overloading"></a><span data-ttu-id="01bf5-123">Surcharge</span><span class="sxs-lookup"><span data-stu-id="01bf5-123">Overloading</span></span>  
 <span data-ttu-id="01bf5-124">Le `+` opérateur peut être *surchargé*, ce qui signifie qu’une classe ou structure peut redéfinir son comportement lorsqu’un opérande a le type de cette classe ou structure.</span><span class="sxs-lookup"><span data-stu-id="01bf5-124">The `+` operator can be *overloaded*, which means that a class or structure can redefine its behavior when an operand has the type of that class or structure.</span></span> <span data-ttu-id="01bf5-125">La surcharge la `+` opérateur affecte le comportement de la `+=` opérateur.</span><span class="sxs-lookup"><span data-stu-id="01bf5-125">Overloading the `+` operator affects the behavior of the `+=` operator.</span></span> <span data-ttu-id="01bf5-126">Si votre code utilise `+=` sur une classe ou structure qui surcharge `+`, assurez-vous que vous comprenez son comportement redéfini.</span><span class="sxs-lookup"><span data-stu-id="01bf5-126">If your code uses `+=` on a class or structure that overloads `+`, be sure you understand its redefined behavior.</span></span> <span data-ttu-id="01bf5-127">Pour plus d'informations, consultez [Operator Procedures](../../../visual-basic/programming-guide/language-features/procedures/operator-procedures.md).</span><span class="sxs-lookup"><span data-stu-id="01bf5-127">For more information, see [Operator Procedures](../../../visual-basic/programming-guide/language-features/procedures/operator-procedures.md).</span></span>  
  
## <a name="example"></a><span data-ttu-id="01bf5-128">Exemple</span><span class="sxs-lookup"><span data-stu-id="01bf5-128">Example</span></span>  
 <span data-ttu-id="01bf5-129">L’exemple suivant utilise le `+=` opérateur pour combiner la valeur d’une variable avec un autre.</span><span class="sxs-lookup"><span data-stu-id="01bf5-129">The following example uses the `+=` operator to combine the value of one variable with another.</span></span> <span data-ttu-id="01bf5-130">La première partie utilise `+=` avec des variables numériques pour ajouter une valeur à un autre.</span><span class="sxs-lookup"><span data-stu-id="01bf5-130">The first part uses `+=` with numeric variables to add one value to another.</span></span> <span data-ttu-id="01bf5-131">La deuxième partie utilise `+=` avec `String` variables pour concaténer une valeur avec un autre.</span><span class="sxs-lookup"><span data-stu-id="01bf5-131">The second part uses `+=` with `String` variables to concatenate one value with another.</span></span> <span data-ttu-id="01bf5-132">Dans les deux cas, le résultat est assigné à la première variable.</span><span class="sxs-lookup"><span data-stu-id="01bf5-132">In both cases, the result is assigned to the first variable.</span></span>  
  
 [!code-vb[VbVbalrOperators#7](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbalrOperators/VB/Class1.vb#7)]  
  
 [!code-vb[VbVbalrOperators#8](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbalrOperators/VB/Class1.vb#8)]  
  
 <span data-ttu-id="01bf5-133">La valeur de `num1` est maintenant 13 et la valeur de `str1` est désormais « 103 ».</span><span class="sxs-lookup"><span data-stu-id="01bf5-133">The value of `num1` is now 13, and the value of `str1` is now "103".</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="01bf5-134">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="01bf5-134">See also</span></span>

- [<span data-ttu-id="01bf5-135">+, opérateur</span><span class="sxs-lookup"><span data-stu-id="01bf5-135">+ Operator</span></span>](../../../visual-basic/language-reference/operators/addition-operator.md)
- [<span data-ttu-id="01bf5-136">Opérateurs d’assignation</span><span class="sxs-lookup"><span data-stu-id="01bf5-136">Assignment Operators</span></span>](../../../visual-basic/language-reference/operators/assignment-operators.md)
- [<span data-ttu-id="01bf5-137">Opérateurs arithmétiques</span><span class="sxs-lookup"><span data-stu-id="01bf5-137">Arithmetic Operators</span></span>](../../../visual-basic/language-reference/operators/arithmetic-operators.md)
- [<span data-ttu-id="01bf5-138">opérateur de concaténation</span><span class="sxs-lookup"><span data-stu-id="01bf5-138">Concatenation Operators</span></span>](../../../visual-basic/language-reference/operators/concatenation-operators.md)
- [<span data-ttu-id="01bf5-139">Priorité des opérateurs en Visual Basic</span><span class="sxs-lookup"><span data-stu-id="01bf5-139">Operator Precedence in Visual Basic</span></span>](../../../visual-basic/language-reference/operators/operator-precedence.md)
- [<span data-ttu-id="01bf5-140">Opérateurs répertoriés par fonctionnalité</span><span class="sxs-lookup"><span data-stu-id="01bf5-140">Operators Listed by Functionality</span></span>](../../../visual-basic/language-reference/operators/operators-listed-by-functionality.md)
- [<span data-ttu-id="01bf5-141">Instructions</span><span class="sxs-lookup"><span data-stu-id="01bf5-141">Statements</span></span>](../../../visual-basic/programming-guide/language-features/statements.md)
