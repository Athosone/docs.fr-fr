---
title: '\= Opérateur (Visual Basic)'
ms.date: 07/20/2015
f1_keywords:
- '\='
- vb.\=
helpviewer_keywords:
- '\= operator [Visual Basic]'
- assignment statements [Visual Basic], compound
- statements [Visual Basic], compound assignment
- operator \= [Visual Basic]
- compound assignment statements [Visual Basic]
ms.assetid: 6f39915d-e398-4045-afcc-da6885e57b9c
ms.openlocfilehash: 377a14a76f67e938f24c973b5946abd63f851bfd
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61768345"
---
# <a name="-operator"></a><span data-ttu-id="56889-102">\\=, Opérateur</span><span class="sxs-lookup"><span data-stu-id="56889-102">\\= Operator</span></span>
<span data-ttu-id="56889-103">Divise la valeur d’une variable ou une propriété par la valeur d’une expression et assigne le résultat de l’entier à la variable ou propriété.</span><span class="sxs-lookup"><span data-stu-id="56889-103">Divides the value of a variable or property by the value of an expression and assigns the integer result to the variable or property.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="56889-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="56889-104">Syntax</span></span>  
  
```  
variableorproperty \= expression  
```  
  
## <a name="parts"></a><span data-ttu-id="56889-105">Composants</span><span class="sxs-lookup"><span data-stu-id="56889-105">Parts</span></span>  
 `variableorproperty`  
 <span data-ttu-id="56889-106">Obligatoire.</span><span class="sxs-lookup"><span data-stu-id="56889-106">Required.</span></span> <span data-ttu-id="56889-107">Toute variable ou propriété numérique.</span><span class="sxs-lookup"><span data-stu-id="56889-107">Any numeric variable or property.</span></span>  
  
 `expression`  
 <span data-ttu-id="56889-108">Obligatoire.</span><span class="sxs-lookup"><span data-stu-id="56889-108">Required.</span></span> <span data-ttu-id="56889-109">Toute expression numérique.</span><span class="sxs-lookup"><span data-stu-id="56889-109">Any numeric expression.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="56889-110">Notes</span><span class="sxs-lookup"><span data-stu-id="56889-110">Remarks</span></span>  
 <span data-ttu-id="56889-111">L’élément sur le côté gauche de la `\=` opérateur peut être une simple variable scalaire, une propriété ou un élément d’un tableau.</span><span class="sxs-lookup"><span data-stu-id="56889-111">The element on the left side of the `\=` operator can be a simple scalar variable, a property, or an element of an array.</span></span> <span data-ttu-id="56889-112">La variable ou la propriété ne peut pas être [ReadOnly](../../../visual-basic/language-reference/modifiers/readonly.md).</span><span class="sxs-lookup"><span data-stu-id="56889-112">The variable or property cannot be [ReadOnly](../../../visual-basic/language-reference/modifiers/readonly.md).</span></span>  
  
 <span data-ttu-id="56889-113">Le `\=` opérateur divise la valeur d’une variable ou une propriété du côté gauche par la valeur situé à sa droite et assigne le résultat de l’entier à la variable ou propriété du côté gauche</span><span class="sxs-lookup"><span data-stu-id="56889-113">The `\=` operator divides the value of a variable or property on its left by the value on its right, and assigns the integer result to the variable or property on its left</span></span>  
  
 <span data-ttu-id="56889-114">Pour plus d’informations sur la division d’entier, consultez [\, opérateur (Visual Basic)](../../../visual-basic/language-reference/operators/integer-division-operator.md).</span><span class="sxs-lookup"><span data-stu-id="56889-114">For further information on integer division, see [\ Operator (Visual Basic)](../../../visual-basic/language-reference/operators/integer-division-operator.md).</span></span>  
  
## <a name="overloading"></a><span data-ttu-id="56889-115">Surcharge</span><span class="sxs-lookup"><span data-stu-id="56889-115">Overloading</span></span>  
 <span data-ttu-id="56889-116">Le `\` opérateur peut être *surchargé*, ce qui signifie qu’une classe ou structure peut redéfinir son comportement lorsqu’un opérande a le type de cette classe ou structure.</span><span class="sxs-lookup"><span data-stu-id="56889-116">The `\` operator can be *overloaded*, which means that a class or structure can redefine its behavior when an operand has the type of that class or structure.</span></span> <span data-ttu-id="56889-117">La surcharge la `\` opérateur affecte le comportement de la `\=` opérateur.</span><span class="sxs-lookup"><span data-stu-id="56889-117">Overloading the `\` operator affects the behavior of the `\=` operator.</span></span> <span data-ttu-id="56889-118">Si votre code utilise `\=` sur une classe ou structure qui surcharge `\`, assurez-vous que vous comprenez son comportement redéfini.</span><span class="sxs-lookup"><span data-stu-id="56889-118">If your code uses `\=` on a class or structure that overloads `\`, be sure you understand its redefined behavior.</span></span> <span data-ttu-id="56889-119">Pour plus d'informations, consultez [Operator Procedures](../../../visual-basic/programming-guide/language-features/procedures/operator-procedures.md).</span><span class="sxs-lookup"><span data-stu-id="56889-119">For more information, see [Operator Procedures](../../../visual-basic/programming-guide/language-features/procedures/operator-procedures.md).</span></span>  
  
## <a name="example"></a><span data-ttu-id="56889-120">Exemple</span><span class="sxs-lookup"><span data-stu-id="56889-120">Example</span></span>  
 <span data-ttu-id="56889-121">L’exemple suivant utilise le `\=` opérateur pour diviser une `Integer` variable par une autre et assigner de résultat de l’entier à la première variable.</span><span class="sxs-lookup"><span data-stu-id="56889-121">The following example uses the `\=` operator to divide one `Integer` variable by a second and assign the integer result to the first variable.</span></span>  
  
 [!code-vb[VbVbalrOperators#19](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbalrOperators/VB/Class1.vb#19)]  
  
## <a name="see-also"></a><span data-ttu-id="56889-122">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="56889-122">See also</span></span>

- [<span data-ttu-id="56889-123">\, Opérateur (Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="56889-123">\ Operator (Visual Basic)</span></span>](../../../visual-basic/language-reference/operators/integer-division-operator.md)
- [<span data-ttu-id="56889-124">/ =, Opérateur (Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="56889-124">/= Operator (Visual Basic)</span></span>](../../../visual-basic/language-reference/operators/floating-point-division-assignment-operator.md)
- [<span data-ttu-id="56889-125">Opérateurs d’assignation</span><span class="sxs-lookup"><span data-stu-id="56889-125">Assignment Operators</span></span>](../../../visual-basic/language-reference/operators/assignment-operators.md)
- [<span data-ttu-id="56889-126">Opérateurs arithmétiques</span><span class="sxs-lookup"><span data-stu-id="56889-126">Arithmetic Operators</span></span>](../../../visual-basic/language-reference/operators/arithmetic-operators.md)
- [<span data-ttu-id="56889-127">Priorité des opérateurs en Visual Basic</span><span class="sxs-lookup"><span data-stu-id="56889-127">Operator Precedence in Visual Basic</span></span>](../../../visual-basic/language-reference/operators/operator-precedence.md)
- [<span data-ttu-id="56889-128">Opérateurs répertoriés par fonctionnalité</span><span class="sxs-lookup"><span data-stu-id="56889-128">Operators Listed by Functionality</span></span>](../../../visual-basic/language-reference/operators/operators-listed-by-functionality.md)
- [<span data-ttu-id="56889-129">Instructions</span><span class="sxs-lookup"><span data-stu-id="56889-129">Statements</span></span>](../../../visual-basic/programming-guide/language-features/statements.md)
