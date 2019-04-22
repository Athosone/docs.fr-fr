---
title: While...End While, instruction (Visual Basic)
ms.date: 07/20/2015
f1_keywords:
- vb.While
- vb.While...EndWhile
helpviewer_keywords:
- While statement [Visual Basic], While...End While
- While statement [Visual Basic]
- While...End While statements [Visual Basic]
ms.assetid: b931d1ce-e8ed-44d8-a13d-92a4f5458a1e
ms.openlocfilehash: 00ca0ad24231128b25a988921386d6bd3265e9a0
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "58843706"
---
# <a name="whileend-while-statement-visual-basic"></a><span data-ttu-id="15bd8-102">While...End While, instruction (Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="15bd8-102">While...End While Statement (Visual Basic)</span></span>
<span data-ttu-id="15bd8-103">Exécute une série d’instructions tant qu’une condition donnée est `True`.</span><span class="sxs-lookup"><span data-stu-id="15bd8-103">Runs a series of statements as long as a given condition is `True`.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="15bd8-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="15bd8-104">Syntax</span></span>  
  
```  
While condition  
    [ statements ]  
    [ Continue While ]  
    [ statements ]  
    [ Exit While ]  
    [ statements ]  
End While  
```  
  
## <a name="parts"></a><span data-ttu-id="15bd8-105">Composants</span><span class="sxs-lookup"><span data-stu-id="15bd8-105">Parts</span></span>  
  
|<span data-ttu-id="15bd8-106">Terme</span><span class="sxs-lookup"><span data-stu-id="15bd8-106">Term</span></span>|<span data-ttu-id="15bd8-107">Définition</span><span class="sxs-lookup"><span data-stu-id="15bd8-107">Definition</span></span>|  
|---|---|  
|`condition`|<span data-ttu-id="15bd8-108">Obligatoire.</span><span class="sxs-lookup"><span data-stu-id="15bd8-108">Required.</span></span> <span data-ttu-id="15bd8-109">`Boolean` expression.</span><span class="sxs-lookup"><span data-stu-id="15bd8-109">`Boolean` expression.</span></span> <span data-ttu-id="15bd8-110">Si `condition` est `Nothing`, Visual Basic traite en tant que `False`.</span><span class="sxs-lookup"><span data-stu-id="15bd8-110">If `condition` is `Nothing`, Visual Basic treats it as `False`.</span></span>|  
|`statements`|<span data-ttu-id="15bd8-111">Optionnel.</span><span class="sxs-lookup"><span data-stu-id="15bd8-111">Optional.</span></span> <span data-ttu-id="15bd8-112">Une ou plusieurs instructions qui suivent `While`, qui exécutera chaque fois `condition` est `True`.</span><span class="sxs-lookup"><span data-stu-id="15bd8-112">One or more statements following `While`, which run every time `condition` is `True`.</span></span>|  
|`Continue While`|<span data-ttu-id="15bd8-113">Optionnel.</span><span class="sxs-lookup"><span data-stu-id="15bd8-113">Optional.</span></span> <span data-ttu-id="15bd8-114">Transfère le contrôle à l’itération suivante de la `While` bloc.</span><span class="sxs-lookup"><span data-stu-id="15bd8-114">Transfers control to the next iteration of the `While` block.</span></span>|  
|`Exit While`|<span data-ttu-id="15bd8-115">Optionnel.</span><span class="sxs-lookup"><span data-stu-id="15bd8-115">Optional.</span></span> <span data-ttu-id="15bd8-116">Transfère le contrôle de la `While` bloc.</span><span class="sxs-lookup"><span data-stu-id="15bd8-116">Transfers control out of the `While` block.</span></span>|  
|`End While`|<span data-ttu-id="15bd8-117">Obligatoire.</span><span class="sxs-lookup"><span data-stu-id="15bd8-117">Required.</span></span> <span data-ttu-id="15bd8-118">Met fin à la définition du bloc `While`.</span><span class="sxs-lookup"><span data-stu-id="15bd8-118">Terminates the definition of the `While` block.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="15bd8-119">Notes</span><span class="sxs-lookup"><span data-stu-id="15bd8-119">Remarks</span></span>  
 <span data-ttu-id="15bd8-120">Utilisez un `While...End While` structure lorsque vous souhaitez répéter un ensemble d’instructions un nombre indéfini de fois, tant qu’une condition reste `True`.</span><span class="sxs-lookup"><span data-stu-id="15bd8-120">Use a `While...End While` structure when you want to repeat a set of statements an indefinite number of times, as long as a condition remains `True`.</span></span> <span data-ttu-id="15bd8-121">Si vous souhaitez davantage de flexibilité avec où vous testez la condition ou du résultat vous tester cela, vous préférerez peut-être la [faire... Instruction de boucle](../../../visual-basic/language-reference/statements/do-loop-statement.md).</span><span class="sxs-lookup"><span data-stu-id="15bd8-121">If you want more flexibility with where you test the condition or what result you test it for, you might prefer the [Do...Loop Statement](../../../visual-basic/language-reference/statements/do-loop-statement.md).</span></span> <span data-ttu-id="15bd8-122">Si vous souhaitez répéter les instructions un nombre défini de fois, le [pour... L’instruction suivante](../../../visual-basic/language-reference/statements/for-next-statement.md) constitue généralement un meilleur choix.</span><span class="sxs-lookup"><span data-stu-id="15bd8-122">If you want to repeat the statements a set number of times, the [For...Next Statement](../../../visual-basic/language-reference/statements/for-next-statement.md) is usually a better choice.</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="15bd8-123">Le `While` clé est également utilisé dans le [faire... Instruction de boucle](../../../visual-basic/language-reference/statements/do-loop-statement.md), le [Skip While, Clause](../../../visual-basic/language-reference/queries/skip-while-clause.md) et [Take While, Clause](../../../visual-basic/language-reference/queries/take-while-clause.md).</span><span class="sxs-lookup"><span data-stu-id="15bd8-123">The `While` keyword is also used in the [Do...Loop Statement](../../../visual-basic/language-reference/statements/do-loop-statement.md), the [Skip While Clause](../../../visual-basic/language-reference/queries/skip-while-clause.md) and the [Take While Clause](../../../visual-basic/language-reference/queries/take-while-clause.md).</span></span>  
  
 <span data-ttu-id="15bd8-124">Si `condition` est `True`, tous les de la `statements` exécution jusqu'à ce que le `End While` est rencontrée.</span><span class="sxs-lookup"><span data-stu-id="15bd8-124">If `condition` is `True`, all of the `statements` run until the `End While` statement is encountered.</span></span> <span data-ttu-id="15bd8-125">Contrôle puis le retourne à la `While` instruction, et `condition` est à nouveau vérifié.</span><span class="sxs-lookup"><span data-stu-id="15bd8-125">Control then returns to the `While` statement, and `condition` is again checked.</span></span> <span data-ttu-id="15bd8-126">Si `condition` est toujours `True`, le processus est répété.</span><span class="sxs-lookup"><span data-stu-id="15bd8-126">If `condition` is still `True`, the process is repeated.</span></span> <span data-ttu-id="15bd8-127">S’il a `False`, le contrôle passe à l’instruction qui suit la `End While` instruction.</span><span class="sxs-lookup"><span data-stu-id="15bd8-127">If it’s `False`, control passes to the statement that follows the `End While` statement.</span></span>  
  
 <span data-ttu-id="15bd8-128">La `While` instruction toujours vérifie la condition avant le début de la boucle.</span><span class="sxs-lookup"><span data-stu-id="15bd8-128">The `While` statement always checks the condition before it starts the loop.</span></span> <span data-ttu-id="15bd8-129">La boucle continue tant que la condition est `True`.</span><span class="sxs-lookup"><span data-stu-id="15bd8-129">Looping continues while the condition remains `True`.</span></span> <span data-ttu-id="15bd8-130">Si `condition` est `False` lorsque vous entrez tout d’abord la boucle, il ne s’exécute même une seule fois.</span><span class="sxs-lookup"><span data-stu-id="15bd8-130">If `condition` is `False` when you first enter the loop, it doesn’t run even once.</span></span>  
  
 <span data-ttu-id="15bd8-131">Le `condition` généralement les résultats à partir d’une comparaison de deux valeurs, mais elle peuvent être toute expression qui prend la valeur un [Type de données booléen](../../../visual-basic/language-reference/data-types/boolean-data-type.md) valeur (`True` ou `False`).</span><span class="sxs-lookup"><span data-stu-id="15bd8-131">The `condition` usually results from a comparison of two values, but it can be any expression that evaluates to a [Boolean Data Type](../../../visual-basic/language-reference/data-types/boolean-data-type.md) value (`True` or `False`).</span></span> <span data-ttu-id="15bd8-132">Cette expression peut inclure une valeur d’un autre type de données, comme un type numérique, ce qui a été converti en `Boolean`.</span><span class="sxs-lookup"><span data-stu-id="15bd8-132">This expression can include a value of another data type, such as a numeric type, that has been converted to `Boolean`.</span></span>  
  
 <span data-ttu-id="15bd8-133">Vous pouvez imbriquer `While` boucles en plaçant une boucle dans une autre.</span><span class="sxs-lookup"><span data-stu-id="15bd8-133">You can nest `While` loops by placing one loop within another.</span></span> <span data-ttu-id="15bd8-134">Vous pouvez également imbriquer des différents types de structures de contrôle dans l’autre.</span><span class="sxs-lookup"><span data-stu-id="15bd8-134">You can also nest different kinds of control structures within one another.</span></span> <span data-ttu-id="15bd8-135">Pour plus d’informations, consultez [Structures de contrôle imbriquées](../../../visual-basic/programming-guide/language-features/control-flow/nested-control-structures.md).</span><span class="sxs-lookup"><span data-stu-id="15bd8-135">For more information, see [Nested Control Structures](../../../visual-basic/programming-guide/language-features/control-flow/nested-control-structures.md).</span></span>  
  
## <a name="exit-while"></a><span data-ttu-id="15bd8-136">Sortie lors de la</span><span class="sxs-lookup"><span data-stu-id="15bd8-136">Exit While</span></span>  
 <span data-ttu-id="15bd8-137">Le [quitter tandis que](../../../visual-basic/language-reference/statements/exit-statement.md) instruction peut fournir une autre façon de quitter un `While` boucle.</span><span class="sxs-lookup"><span data-stu-id="15bd8-137">The [Exit While](../../../visual-basic/language-reference/statements/exit-statement.md) statement can provide another way to exit a `While` loop.</span></span> <span data-ttu-id="15bd8-138">`Exit While` transfère le contrôle à l’instruction qui suit immédiatement la `End While` instruction.</span><span class="sxs-lookup"><span data-stu-id="15bd8-138">`Exit While` immediately transfers control to the statement that follows the `End While` statement.</span></span>  
  
 <span data-ttu-id="15bd8-139">Vous utilisez généralement `Exit While` après une condition est évaluée (par exemple, dans un `If...Then...Else` structure).</span><span class="sxs-lookup"><span data-stu-id="15bd8-139">You typically use `Exit While` after some condition is evaluated (for example, in an `If...Then...Else` structure).</span></span> <span data-ttu-id="15bd8-140">Vous souhaiterez peut-être quitter une boucle si vous détectez une condition qui rend inutile ou impossible pour poursuivre l’itération, comme une valeur erronée ou une demande d’arrêt.</span><span class="sxs-lookup"><span data-stu-id="15bd8-140">You might want to exit a loop if you detect a condition that makes it unnecessary or impossible to continue iterating, such as an erroneous value or a termination request.</span></span> <span data-ttu-id="15bd8-141">Vous pouvez utiliser `Exit While` lorsque vous testez une condition qui peut entraîner un *boucle sans fin*, qui est une boucle qui pourrait s’exécuter très volumineux ou même infini de fois.</span><span class="sxs-lookup"><span data-stu-id="15bd8-141">You can use `Exit While` when you test for a condition that could cause an *endless loop*, which is a loop that could run an extremely large or even infinite number of times.</span></span> <span data-ttu-id="15bd8-142">Vous pouvez ensuite utiliser `Exit While` pour abandonner la boucle.</span><span class="sxs-lookup"><span data-stu-id="15bd8-142">You can then use `Exit While` to escape the loop.</span></span>  
  
 <span data-ttu-id="15bd8-143">Vous pouvez placer un nombre quelconque de `Exit While` instructions n’importe où dans le `While` boucle.</span><span class="sxs-lookup"><span data-stu-id="15bd8-143">You can place any number of `Exit While` statements anywhere in the `While` loop.</span></span>  
  
 <span data-ttu-id="15bd8-144">Lorsqu’il est utilisé dans imbriqués `While` boucles, `Exit While` transfère le contrôle en dehors de la boucle la plus profonde et dans le niveau d’imbrication supérieur suivant.</span><span class="sxs-lookup"><span data-stu-id="15bd8-144">When used within nested `While` loops, `Exit While` transfers control out of the innermost loop and into the next higher level of nesting.</span></span>  
  
 <span data-ttu-id="15bd8-145">La `Continue While` instruction transfère le contrôle immédiatement à l’itération suivante de la boucle.</span><span class="sxs-lookup"><span data-stu-id="15bd8-145">The `Continue While` statement immediately transfers control to the next iteration of the loop.</span></span> <span data-ttu-id="15bd8-146">Pour plus d’informations, consultez [instruction Continue](../../../visual-basic/language-reference/statements/continue-statement.md).</span><span class="sxs-lookup"><span data-stu-id="15bd8-146">For more information, see [Continue Statement](../../../visual-basic/language-reference/statements/continue-statement.md).</span></span>  
  
## <a name="example"></a><span data-ttu-id="15bd8-147">Exemple</span><span class="sxs-lookup"><span data-stu-id="15bd8-147">Example</span></span>  
 <span data-ttu-id="15bd8-148">Dans l’exemple suivant, les instructions dans la boucle continuent à s’exécuter jusqu'à ce que le `index` variable est supérieure à 10.</span><span class="sxs-lookup"><span data-stu-id="15bd8-148">In the following example, the statements in the loop continue to run until the `index` variable is greater than 10.</span></span>  
  
 [!code-vb[VbVbalrStatements#171](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbalrStatements/VB/class14.vb#171)]  
  
## <a name="example"></a><span data-ttu-id="15bd8-149">Exemple</span><span class="sxs-lookup"><span data-stu-id="15bd8-149">Example</span></span>  
 <span data-ttu-id="15bd8-150">L’exemple suivant illustre l’utilisation de la `Continue While` et `Exit While` instructions.</span><span class="sxs-lookup"><span data-stu-id="15bd8-150">The following example illustrates the use of the `Continue While` and `Exit While` statements.</span></span>  
  
 [!code-vb[VbVbalrStatements#172](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbalrStatements/VB/class14.vb#172)]  
  
## <a name="example"></a><span data-ttu-id="15bd8-151">Exemple</span><span class="sxs-lookup"><span data-stu-id="15bd8-151">Example</span></span>  
 <span data-ttu-id="15bd8-152">L’exemple suivant lit toutes les lignes dans un fichier texte.</span><span class="sxs-lookup"><span data-stu-id="15bd8-152">The following example reads all lines in a text file.</span></span> <span data-ttu-id="15bd8-153">Le <xref:System.IO.File.OpenText%2A> méthode ouvre le fichier et retourne un <xref:System.IO.StreamReader> qui lit les caractères.</span><span class="sxs-lookup"><span data-stu-id="15bd8-153">The <xref:System.IO.File.OpenText%2A> method opens the file and returns a <xref:System.IO.StreamReader> that reads the characters.</span></span> <span data-ttu-id="15bd8-154">Dans le `While` condition, le <xref:System.IO.StreamReader.Peek%2A> méthode de la `StreamReader` détermine si le fichier contient des caractères supplémentaires.</span><span class="sxs-lookup"><span data-stu-id="15bd8-154">In the `While` condition, the <xref:System.IO.StreamReader.Peek%2A> method of the `StreamReader` determines whether the file contains additional characters.</span></span>  
  
 [!code-vb[VbVbalrStatements#173](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbalrStatements/VB/class14.vb#173)]  
  
## <a name="see-also"></a><span data-ttu-id="15bd8-155">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="15bd8-155">See also</span></span>

- [<span data-ttu-id="15bd8-156">Structures de boucle</span><span class="sxs-lookup"><span data-stu-id="15bd8-156">Loop Structures</span></span>](../../../visual-basic/programming-guide/language-features/control-flow/loop-structures.md)
- [<span data-ttu-id="15bd8-157">Do...Loop (instruction)</span><span class="sxs-lookup"><span data-stu-id="15bd8-157">Do...Loop Statement</span></span>](../../../visual-basic/language-reference/statements/do-loop-statement.md)
- [<span data-ttu-id="15bd8-158">For...Next (instruction)</span><span class="sxs-lookup"><span data-stu-id="15bd8-158">For...Next Statement</span></span>](../../../visual-basic/language-reference/statements/for-next-statement.md)
- [<span data-ttu-id="15bd8-159">Booléen (type de données)</span><span class="sxs-lookup"><span data-stu-id="15bd8-159">Boolean Data Type</span></span>](../../../visual-basic/language-reference/data-types/boolean-data-type.md)
- [<span data-ttu-id="15bd8-160">Structures de contrôle imbriquées</span><span class="sxs-lookup"><span data-stu-id="15bd8-160">Nested Control Structures</span></span>](../../../visual-basic/programming-guide/language-features/control-flow/nested-control-structures.md)
- [<span data-ttu-id="15bd8-161">Exit (instruction)</span><span class="sxs-lookup"><span data-stu-id="15bd8-161">Exit Statement</span></span>](../../../visual-basic/language-reference/statements/exit-statement.md)
- [<span data-ttu-id="15bd8-162">Continue (instruction)</span><span class="sxs-lookup"><span data-stu-id="15bd8-162">Continue Statement</span></span>](../../../visual-basic/language-reference/statements/continue-statement.md)
