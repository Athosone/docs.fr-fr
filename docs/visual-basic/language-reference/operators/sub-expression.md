---
title: Sous-expression (Visual Basic)
ms.date: 07/20/2015
helpviewer_keywords:
- lambda expressions [Visual Basic], sub expression
- Sub Expression [Visual Basic]
- subroutines [Visual Basic], sub expressions
ms.assetid: 36b6bfd1-6539-4d8f-a5eb-6541a745ffde
ms.openlocfilehash: 5b26a091dc8eb7415702c3c2853a569324def7d5
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62013502"
---
# <a name="sub-expression-visual-basic"></a><span data-ttu-id="5c2d6-102">Sous-expression (Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="5c2d6-102">Sub Expression (Visual Basic)</span></span>
<span data-ttu-id="5c2d6-103">Déclare les paramètres et le code qui définissent une expression lambda de sous-routine.</span><span class="sxs-lookup"><span data-stu-id="5c2d6-103">Declares the parameters and code that define a subroutine lambda expression.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="5c2d6-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="5c2d6-104">Syntax</span></span>  
  
```  
Sub ( [ parameterlist ] ) statement  
- or -  
Sub ( [ parameterlist ] )  
  [ statements ]  
End Sub  
```  
  
## <a name="parts"></a><span data-ttu-id="5c2d6-105">Composants</span><span class="sxs-lookup"><span data-stu-id="5c2d6-105">Parts</span></span>  
  
|<span data-ttu-id="5c2d6-106">Terme</span><span class="sxs-lookup"><span data-stu-id="5c2d6-106">Term</span></span>|<span data-ttu-id="5c2d6-107">Définition</span><span class="sxs-lookup"><span data-stu-id="5c2d6-107">Definition</span></span>|  
|---|---|  
|`parameterlist`|<span data-ttu-id="5c2d6-108">Facultatif.</span><span class="sxs-lookup"><span data-stu-id="5c2d6-108">Optional.</span></span> <span data-ttu-id="5c2d6-109">Liste des noms de variables locales qui représentent les paramètres de la procédure.</span><span class="sxs-lookup"><span data-stu-id="5c2d6-109">A list of local variable names that represent the parameters of the procedure.</span></span> <span data-ttu-id="5c2d6-110">Les parenthèses doivent être présents même lorsque la liste est vide.</span><span class="sxs-lookup"><span data-stu-id="5c2d6-110">The parentheses must be present even when the list is empty.</span></span> <span data-ttu-id="5c2d6-111">Pour plus d'informations, consultez [Parameter List](../../../visual-basic/language-reference/statements/parameter-list.md).</span><span class="sxs-lookup"><span data-stu-id="5c2d6-111">For more information, see [Parameter List](../../../visual-basic/language-reference/statements/parameter-list.md).</span></span>|  
|`statement`|<span data-ttu-id="5c2d6-112">Obligatoire.</span><span class="sxs-lookup"><span data-stu-id="5c2d6-112">Required.</span></span> <span data-ttu-id="5c2d6-113">Une instruction unique.</span><span class="sxs-lookup"><span data-stu-id="5c2d6-113">A single statement.</span></span>|  
|`statements`|<span data-ttu-id="5c2d6-114">Obligatoire.</span><span class="sxs-lookup"><span data-stu-id="5c2d6-114">Required.</span></span> <span data-ttu-id="5c2d6-115">Une liste d’instructions.</span><span class="sxs-lookup"><span data-stu-id="5c2d6-115">A list of statements.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="5c2d6-116">Notes</span><span class="sxs-lookup"><span data-stu-id="5c2d6-116">Remarks</span></span>  
 <span data-ttu-id="5c2d6-117">Un *expression lambda* est une sous-routine qui n’a pas un nom et qui s’exécute une ou plusieurs instructions.</span><span class="sxs-lookup"><span data-stu-id="5c2d6-117">A *lambda expression* is a subroutine that does not have a name and that executes one or more statements.</span></span> <span data-ttu-id="5c2d6-118">Vous pouvez utiliser une expression lambda n’importe où que vous pouvez utiliser un type délégué, sauf en tant qu’argument à `RemoveHandler`.</span><span class="sxs-lookup"><span data-stu-id="5c2d6-118">You can use a lambda expression anywhere that you can use a delegate type, except as an argument to `RemoveHandler`.</span></span> <span data-ttu-id="5c2d6-119">Pour plus d’informations sur les délégués et l’utilisation d’expressions lambda avec les délégués, consultez [instruction Delegate](../../../visual-basic/language-reference/statements/delegate-statement.md) et [Conversion souple des délégués](../../../visual-basic/programming-guide/language-features/delegates/relaxed-delegate-conversion.md).</span><span class="sxs-lookup"><span data-stu-id="5c2d6-119">For more information about delegates, and the use of lambda expressions with delegates, see [Delegate Statement](../../../visual-basic/language-reference/statements/delegate-statement.md) and [Relaxed Delegate Conversion](../../../visual-basic/programming-guide/language-features/delegates/relaxed-delegate-conversion.md).</span></span>  
  
## <a name="lambda-expression-syntax"></a><span data-ttu-id="5c2d6-120">Syntaxe d’expression lambda</span><span class="sxs-lookup"><span data-stu-id="5c2d6-120">Lambda Expression Syntax</span></span>  
 <span data-ttu-id="5c2d6-121">La syntaxe d’une expression lambda ressemble à celle d’une sous-routine standard.</span><span class="sxs-lookup"><span data-stu-id="5c2d6-121">The syntax of a lambda expression resembles that of a standard subroutine.</span></span> <span data-ttu-id="5c2d6-122">Les différences sont les suivantes :</span><span class="sxs-lookup"><span data-stu-id="5c2d6-122">The differences are as follows:</span></span>  
  
- <span data-ttu-id="5c2d6-123">Une expression lambda n’a pas un nom.</span><span class="sxs-lookup"><span data-stu-id="5c2d6-123">A lambda expression does not have a name.</span></span>  
  
- <span data-ttu-id="5c2d6-124">Une expression lambda ne peut pas avoir un modificateur, tel que `Overloads` ou `Overrides`.</span><span class="sxs-lookup"><span data-stu-id="5c2d6-124">A lambda expression cannot have a modifier, such as `Overloads` or `Overrides`.</span></span>  
  
- <span data-ttu-id="5c2d6-125">Le corps d’une expression lambda sur une ligne doit être une instruction, pas une expression.</span><span class="sxs-lookup"><span data-stu-id="5c2d6-125">The body of a single-line lambda expression must be a statement, not an expression.</span></span> <span data-ttu-id="5c2d6-126">Le corps peut se composer d’un appel à une procédure sub, mais pas un appel à une procédure de fonction.</span><span class="sxs-lookup"><span data-stu-id="5c2d6-126">The body can consist of a call to a sub procedure, but not a call to a function procedure.</span></span>  
  
- <span data-ttu-id="5c2d6-127">Dans une expression lambda, soit tous les paramètres doivent avoir spécifié tous les paramètres ou types de données doivent être déduits.</span><span class="sxs-lookup"><span data-stu-id="5c2d6-127">In a lambda expression, either all parameters must have specified data types or all parameters must be inferred.</span></span>  
  
- <span data-ttu-id="5c2d6-128">Facultatif et `ParamArray` paramètres ne sont pas autorisés dans les expressions lambda.</span><span class="sxs-lookup"><span data-stu-id="5c2d6-128">Optional and `ParamArray` parameters are not permitted in lambda expressions.</span></span>  
  
- <span data-ttu-id="5c2d6-129">Paramètres génériques ne sont pas autorisées dans les expressions lambda.</span><span class="sxs-lookup"><span data-stu-id="5c2d6-129">Generic parameters are not permitted in lambda expressions.</span></span>  
  
## <a name="example"></a><span data-ttu-id="5c2d6-130">Exemple</span><span class="sxs-lookup"><span data-stu-id="5c2d6-130">Example</span></span>  
 <span data-ttu-id="5c2d6-131">Voici un exemple d’une expression lambda qui écrit une valeur dans la console.</span><span class="sxs-lookup"><span data-stu-id="5c2d6-131">Following is an example of a lambda expression that writes a value to the console.</span></span> <span data-ttu-id="5c2d6-132">L’exemple montre les deux la syntaxe d’expression lambda multiligne ou plusieurs lignes d’une sous-routine.</span><span class="sxs-lookup"><span data-stu-id="5c2d6-132">The example shows both the single-line and multiline lambda expression syntax for a subroutine.</span></span> <span data-ttu-id="5c2d6-133">Pour plus d’exemples, consultez [Expressions Lambda](../../../visual-basic/programming-guide/language-features/procedures/lambda-expressions.md).</span><span class="sxs-lookup"><span data-stu-id="5c2d6-133">For more examples, see [Lambda Expressions](../../../visual-basic/programming-guide/language-features/procedures/lambda-expressions.md).</span></span>  
  
 [!code-vb[VbVbalrLambdas#15](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbalrLambdas/VB/Class1.vb#15)]  
  
## <a name="see-also"></a><span data-ttu-id="5c2d6-134">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="5c2d6-134">See also</span></span>

- [<span data-ttu-id="5c2d6-135">Sub (instruction)</span><span class="sxs-lookup"><span data-stu-id="5c2d6-135">Sub Statement</span></span>](../../../visual-basic/language-reference/statements/sub-statement.md)
- [<span data-ttu-id="5c2d6-136">Expressions lambda</span><span class="sxs-lookup"><span data-stu-id="5c2d6-136">Lambda Expressions</span></span>](../../../visual-basic/programming-guide/language-features/procedures/lambda-expressions.md)
- [<span data-ttu-id="5c2d6-137">Opérateurs et expressions</span><span class="sxs-lookup"><span data-stu-id="5c2d6-137">Operators and Expressions</span></span>](../../../visual-basic/programming-guide/language-features/operators-and-expressions/index.md)
- [<span data-ttu-id="5c2d6-138">Instructions</span><span class="sxs-lookup"><span data-stu-id="5c2d6-138">Statements</span></span>](../../../visual-basic/programming-guide/language-features/statements.md)
- [<span data-ttu-id="5c2d6-139">Conversion simplifiée des délégués</span><span class="sxs-lookup"><span data-stu-id="5c2d6-139">Relaxed Delegate Conversion</span></span>](../../../visual-basic/programming-guide/language-features/delegates/relaxed-delegate-conversion.md)
