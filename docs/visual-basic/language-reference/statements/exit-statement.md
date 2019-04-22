---
title: Exit, instruction (Visual Basic)
ms.date: 07/20/2015
f1_keywords:
- vb.Exit
helpviewer_keywords:
- execution [Visual Basic], ending
- files [Visual Basic], closing
- programs [Visual Basic], quitting
- code, exiting
- Exit statement [Visual Basic]
- program termination
- execution [Visual Basic], stopping
ms.assetid: 760bfb32-5c3f-4bdb-a432-9a6001c92db7
ms.openlocfilehash: 1f386694bd7425ee530b9305ab684b730f9b73c8
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "58832630"
---
# <a name="exit-statement-visual-basic"></a><span data-ttu-id="301cf-102">Exit, instruction (Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="301cf-102">Exit Statement (Visual Basic)</span></span>
<span data-ttu-id="301cf-103">Quitte une procédure ou un bloc et transfère le contrôle immédiatement à l’instruction qui suit l’appel de procédure ou la définition de bloc.</span><span class="sxs-lookup"><span data-stu-id="301cf-103">Exits a procedure or block and transfers control immediately to the statement following the procedure call or the block definition.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="301cf-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="301cf-104">Syntax</span></span>  
  
```  
Exit { Do | For | Function | Property | Select | Sub | Try | While }  
```  
  
## <a name="statements"></a><span data-ttu-id="301cf-105">Instructions</span><span class="sxs-lookup"><span data-stu-id="301cf-105">Statements</span></span>  
 `Exit Do`  
 <span data-ttu-id="301cf-106">Quitte immédiatement la `Do` boucle dans laquelle elle apparaît.</span><span class="sxs-lookup"><span data-stu-id="301cf-106">Immediately exits the `Do` loop in which it appears.</span></span> <span data-ttu-id="301cf-107">L’exécution se poursuit avec l’instruction qui suit la `Loop` instruction.</span><span class="sxs-lookup"><span data-stu-id="301cf-107">Execution continues with the statement following the `Loop` statement.</span></span> <span data-ttu-id="301cf-108">`Exit Do` peut être utilisé uniquement à l’intérieur d’un `Do` boucle.</span><span class="sxs-lookup"><span data-stu-id="301cf-108">`Exit Do` can be used only inside a `Do` loop.</span></span> <span data-ttu-id="301cf-109">Lorsqu’il est utilisé dans imbriqués `Do` boucles, `Exit Do` quitte la boucle la plus profonde et transfère le contrôle au niveau d’imbrication supérieur suivant.</span><span class="sxs-lookup"><span data-stu-id="301cf-109">When used within nested `Do` loops, `Exit Do` exits the innermost loop and transfers control to the next higher level of nesting.</span></span>  
  
 `Exit For`  
 <span data-ttu-id="301cf-110">Quitte immédiatement la `For` boucle dans laquelle elle apparaît.</span><span class="sxs-lookup"><span data-stu-id="301cf-110">Immediately exits the `For` loop in which it appears.</span></span> <span data-ttu-id="301cf-111">L’exécution se poursuit avec l’instruction qui suit la `Next` instruction.</span><span class="sxs-lookup"><span data-stu-id="301cf-111">Execution continues with the statement following the `Next` statement.</span></span> <span data-ttu-id="301cf-112">`Exit For` peut être utilisé uniquement à l’intérieur d’un `For`... `Next` ou `For Each`... `Next` boucle.</span><span class="sxs-lookup"><span data-stu-id="301cf-112">`Exit For` can be used only inside a `For`...`Next` or `For Each`...`Next` loop.</span></span> <span data-ttu-id="301cf-113">Lorsqu’il est utilisé dans imbriqués `For` boucles, `Exit For` quitte la boucle la plus profonde et transfère le contrôle au niveau d’imbrication supérieur suivant.</span><span class="sxs-lookup"><span data-stu-id="301cf-113">When used within nested `For` loops, `Exit For` exits the innermost loop and transfers control to the next higher level of nesting.</span></span>  
  
 `Exit Function`  
 <span data-ttu-id="301cf-114">Quitte immédiatement la `Function` procédure dans laquelle elle apparaît.</span><span class="sxs-lookup"><span data-stu-id="301cf-114">Immediately exits the `Function` procedure in which it appears.</span></span> <span data-ttu-id="301cf-115">L’exécution se poursuit avec l’instruction qui suit l’instruction qui a appelé le `Function` procédure.</span><span class="sxs-lookup"><span data-stu-id="301cf-115">Execution continues with the statement following the statement that called the `Function` procedure.</span></span> <span data-ttu-id="301cf-116">`Exit Function` peut être utilisé uniquement à l’intérieur d’un `Function` procédure.</span><span class="sxs-lookup"><span data-stu-id="301cf-116">`Exit Function` can be used only inside a `Function` procedure.</span></span>  
  
 <span data-ttu-id="301cf-117">Pour spécifier une valeur de retour, vous pouvez affecter la valeur pour le nom de fonction sur une ligne avant le `Exit Function` instruction.</span><span class="sxs-lookup"><span data-stu-id="301cf-117">To specify a return value, you can assign the value to the function name on a line before the `Exit Function` statement.</span></span> <span data-ttu-id="301cf-118">Pour affecter la valeur de retour et quitter la fonction dans une instruction, vous pouvez utiliser la [instruction Return](../../../visual-basic/language-reference/statements/return-statement.md).</span><span class="sxs-lookup"><span data-stu-id="301cf-118">To assign the return value and exit the function in one statement, you can instead use the [Return Statement](../../../visual-basic/language-reference/statements/return-statement.md).</span></span>  
  
 `Exit Property`  
 <span data-ttu-id="301cf-119">Quitte immédiatement la `Property` procédure dans laquelle elle apparaît.</span><span class="sxs-lookup"><span data-stu-id="301cf-119">Immediately exits the `Property` procedure in which it appears.</span></span> <span data-ttu-id="301cf-120">L’exécution se poursuit avec l’instruction qui a appelé le `Property` procédure, autrement dit, avec l’instruction qui demande ou définit la valeur de propriété.</span><span class="sxs-lookup"><span data-stu-id="301cf-120">Execution continues with the statement that called the `Property` procedure, that is, with the statement requesting or setting the property's value.</span></span> <span data-ttu-id="301cf-121">`Exit Property` peut être utilisé uniquement à l’intérieur d’une propriété `Get` ou `Set` procédure.</span><span class="sxs-lookup"><span data-stu-id="301cf-121">`Exit Property` can be used only inside a property's `Get` or `Set` procedure.</span></span>  
  
 <span data-ttu-id="301cf-122">Pour spécifier une valeur de retour dans une `Get` procédure, vous pouvez affecter la valeur pour le nom de fonction sur une ligne avant le `Exit Property` instruction.</span><span class="sxs-lookup"><span data-stu-id="301cf-122">To specify a return value in a `Get` procedure, you can assign the value to the function name on a line before the `Exit Property` statement.</span></span> <span data-ttu-id="301cf-123">Pour affecter la valeur de retour et quitter le `Get` procédure dans une instruction, vous pouvez utiliser la `Return` instruction.</span><span class="sxs-lookup"><span data-stu-id="301cf-123">To assign the return value and exit the `Get` procedure in one statement, you can instead use the `Return` statement.</span></span>  
  
 <span data-ttu-id="301cf-124">Dans un `Set` procédure, le `Exit Property` instruction est équivalente à la `Return` instruction.</span><span class="sxs-lookup"><span data-stu-id="301cf-124">In a `Set` procedure, the `Exit Property` statement is equivalent to the `Return` statement.</span></span>  
  
 `Exit Select`  
 <span data-ttu-id="301cf-125">Quitte immédiatement la `Select Case` bloc dans lequel elle apparaît.</span><span class="sxs-lookup"><span data-stu-id="301cf-125">Immediately exits the `Select Case` block in which it appears.</span></span> <span data-ttu-id="301cf-126">L’exécution se poursuit avec l’instruction qui suit la `End Select` instruction.</span><span class="sxs-lookup"><span data-stu-id="301cf-126">Execution continues with the statement following the `End Select` statement.</span></span> <span data-ttu-id="301cf-127">`Exit Select` peut être utilisé uniquement à l’intérieur d’un `Select Case` instruction.</span><span class="sxs-lookup"><span data-stu-id="301cf-127">`Exit Select` can be used only inside a `Select Case` statement.</span></span>  
  
 `Exit Sub`  
 <span data-ttu-id="301cf-128">Quitte immédiatement la `Sub` procédure dans laquelle elle apparaît.</span><span class="sxs-lookup"><span data-stu-id="301cf-128">Immediately exits the `Sub` procedure in which it appears.</span></span> <span data-ttu-id="301cf-129">L’exécution se poursuit avec l’instruction qui suit l’instruction qui a appelé le `Sub` procédure.</span><span class="sxs-lookup"><span data-stu-id="301cf-129">Execution continues with the statement following the statement that called the `Sub` procedure.</span></span> <span data-ttu-id="301cf-130">`Exit Sub` peut être utilisé uniquement à l’intérieur d’un `Sub` procédure.</span><span class="sxs-lookup"><span data-stu-id="301cf-130">`Exit Sub` can be used only inside a `Sub` procedure.</span></span>  
  
 <span data-ttu-id="301cf-131">Dans un `Sub` procédure, le `Exit Sub` instruction est équivalente à la `Return` instruction.</span><span class="sxs-lookup"><span data-stu-id="301cf-131">In a `Sub` procedure, the `Exit Sub` statement is equivalent to the `Return` statement.</span></span>  
  
 `Exit Try`  
 <span data-ttu-id="301cf-132">Quitte immédiatement la `Try` ou `Catch` bloc dans lequel elle apparaît.</span><span class="sxs-lookup"><span data-stu-id="301cf-132">Immediately exits the `Try` or `Catch` block in which it appears.</span></span> <span data-ttu-id="301cf-133">L’exécution se poursuit avec le `Finally` bloquer le cas échéant, ou avec l’instruction qui suit la `End Try` instruction sinon.</span><span class="sxs-lookup"><span data-stu-id="301cf-133">Execution continues with the `Finally` block if there is one, or with the statement following the `End Try` statement otherwise.</span></span> <span data-ttu-id="301cf-134">`Exit Try` peut être utilisé uniquement à l’intérieur d’un `Try` ou `Catch` bloc et pas à l’intérieur un `Finally` bloc.</span><span class="sxs-lookup"><span data-stu-id="301cf-134">`Exit Try` can be used only inside a `Try` or `Catch` block, and not inside a `Finally` block.</span></span>  
  
 `Exit While`  
 <span data-ttu-id="301cf-135">Quitte immédiatement la `While` boucle dans laquelle elle apparaît.</span><span class="sxs-lookup"><span data-stu-id="301cf-135">Immediately exits the `While` loop in which it appears.</span></span> <span data-ttu-id="301cf-136">L’exécution se poursuit avec l’instruction qui suit la `End While` instruction.</span><span class="sxs-lookup"><span data-stu-id="301cf-136">Execution continues with the statement following the `End While` statement.</span></span> <span data-ttu-id="301cf-137">`Exit While` peut être utilisé uniquement à l’intérieur d’un `While` boucle.</span><span class="sxs-lookup"><span data-stu-id="301cf-137">`Exit While` can be used only inside a `While` loop.</span></span> <span data-ttu-id="301cf-138">Lorsqu’il est utilisé dans imbriqués `While` boucles, `Exit While` transfère le contrôle à la boucle qui est un niveau au-dessus de la boucle où `Exit While` se produit.</span><span class="sxs-lookup"><span data-stu-id="301cf-138">When used within nested `While` loops, `Exit While` transfers control to the loop that is one nested level above the loop where `Exit While` occurs.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="301cf-139">Notes</span><span class="sxs-lookup"><span data-stu-id="301cf-139">Remarks</span></span>  
 <span data-ttu-id="301cf-140">Ne confondez pas `Exit` instructions avec `End` instructions.</span><span class="sxs-lookup"><span data-stu-id="301cf-140">Do not confuse `Exit` statements with `End` statements.</span></span> <span data-ttu-id="301cf-141">`Exit` ne définit pas la fin d’une instruction.</span><span class="sxs-lookup"><span data-stu-id="301cf-141">`Exit` does not define the end of a statement.</span></span>  
  
## <a name="example"></a><span data-ttu-id="301cf-142">Exemple</span><span class="sxs-lookup"><span data-stu-id="301cf-142">Example</span></span>  
 <span data-ttu-id="301cf-143">Dans l’exemple suivant, la condition de boucle s’arrête la boucle lorsque la `index` variable est supérieure à 100.</span><span class="sxs-lookup"><span data-stu-id="301cf-143">In the following example, the loop condition stops the loop when the `index` variable is greater than 100.</span></span> <span data-ttu-id="301cf-144">Le `If` instruction dans la boucle, cependant, entraîne la `Exit Do` instruction pour arrêter la boucle lorsque la variable d’index est supérieure à 10.</span><span class="sxs-lookup"><span data-stu-id="301cf-144">The `If` statement in the loop, however, causes the `Exit Do` statement to stop the loop when the index variable is greater than 10.</span></span>  
  
 [!code-vb[VbVbalrStatements#133](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbalrStatements/VB/class10.vb#133)]  
  
## <a name="example"></a><span data-ttu-id="301cf-145">Exemple</span><span class="sxs-lookup"><span data-stu-id="301cf-145">Example</span></span>  
 <span data-ttu-id="301cf-146">L’exemple suivant affecte la valeur de retour pour le nom de fonction `myFunction`, puis utilise `Exit Function` à retourner à partir de la fonction.</span><span class="sxs-lookup"><span data-stu-id="301cf-146">The following example assigns the return value to the function name `myFunction`, and then uses `Exit Function` to return from the function.</span></span>  
  
 [!code-vb[VbVbalrStatements#23](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbalrStatements/VB/Class1.vb#23)]  
  
## <a name="example"></a><span data-ttu-id="301cf-147">Exemple</span><span class="sxs-lookup"><span data-stu-id="301cf-147">Example</span></span>  
 <span data-ttu-id="301cf-148">L’exemple suivant utilise le [instruction Return](../../../visual-basic/language-reference/statements/return-statement.md) pour affecter la valeur de retour et de quitter la fonction.</span><span class="sxs-lookup"><span data-stu-id="301cf-148">The following example uses the [Return Statement](../../../visual-basic/language-reference/statements/return-statement.md) to assign the return value and exit the function.</span></span>  
  
 [!code-vb[VbVbalrStatements#24](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbalrStatements/VB/Class1.vb#24)]  
  
## <a name="see-also"></a><span data-ttu-id="301cf-149">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="301cf-149">See also</span></span>

- [<span data-ttu-id="301cf-150">Continue (instruction)</span><span class="sxs-lookup"><span data-stu-id="301cf-150">Continue Statement</span></span>](../../../visual-basic/language-reference/statements/continue-statement.md)
- [<span data-ttu-id="301cf-151">Do...Loop (instruction)</span><span class="sxs-lookup"><span data-stu-id="301cf-151">Do...Loop Statement</span></span>](../../../visual-basic/language-reference/statements/do-loop-statement.md)
- [<span data-ttu-id="301cf-152">End (instruction)</span><span class="sxs-lookup"><span data-stu-id="301cf-152">End Statement</span></span>](../../../visual-basic/language-reference/statements/end-statement.md)
- [<span data-ttu-id="301cf-153">For Each...Next (instruction)</span><span class="sxs-lookup"><span data-stu-id="301cf-153">For Each...Next Statement</span></span>](../../../visual-basic/language-reference/statements/for-each-next-statement.md)
- [<span data-ttu-id="301cf-154">For...Next (instruction)</span><span class="sxs-lookup"><span data-stu-id="301cf-154">For...Next Statement</span></span>](../../../visual-basic/language-reference/statements/for-next-statement.md)
- [<span data-ttu-id="301cf-155">Function (instruction)</span><span class="sxs-lookup"><span data-stu-id="301cf-155">Function Statement</span></span>](../../../visual-basic/language-reference/statements/function-statement.md)
- [<span data-ttu-id="301cf-156">Return (instruction)</span><span class="sxs-lookup"><span data-stu-id="301cf-156">Return Statement</span></span>](../../../visual-basic/language-reference/statements/return-statement.md)
- [<span data-ttu-id="301cf-157">Stop (instruction)</span><span class="sxs-lookup"><span data-stu-id="301cf-157">Stop Statement</span></span>](../../../visual-basic/language-reference/statements/stop-statement.md)
- [<span data-ttu-id="301cf-158">Sub (instruction)</span><span class="sxs-lookup"><span data-stu-id="301cf-158">Sub Statement</span></span>](../../../visual-basic/language-reference/statements/sub-statement.md)
- [<span data-ttu-id="301cf-159">Try...Catch...Finally (instruction)</span><span class="sxs-lookup"><span data-stu-id="301cf-159">Try...Catch...Finally Statement</span></span>](../../../visual-basic/language-reference/statements/try-catch-finally-statement.md)
