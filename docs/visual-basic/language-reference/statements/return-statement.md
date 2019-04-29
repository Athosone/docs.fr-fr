---
title: Return, instruction (Visual Basic)
ms.date: 07/20/2015
f1_keywords:
- vb.Return
helpviewer_keywords:
- Return statement [Visual Basic], syntax
- control flow [Visual Basic], returning control to expressions
- Return statement [Visual Basic]
- expressions [Visual Basic], returning control to
ms.assetid: ac86e7f0-5a67-42c3-9834-0e0381efa3ec
ms.openlocfilehash: 7f8ec0456576133d37dd19b5c0f8878a7ac57dab
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61783901"
---
# <a name="return-statement-visual-basic"></a><span data-ttu-id="44b32-102">Return, instruction (Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="44b32-102">Return Statement (Visual Basic)</span></span>
<span data-ttu-id="44b32-103">Retourne le contrôle au code qui a appelé un `Function`, `Sub`, `Get`, `Set`, ou `Operator` procédure.</span><span class="sxs-lookup"><span data-stu-id="44b32-103">Returns control to the code that called a `Function`, `Sub`, `Get`, `Set`, or `Operator` procedure.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="44b32-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="44b32-104">Syntax</span></span>  
  
```  
Return  
-or-  
Return expression  
```  
  
## <a name="part"></a><span data-ttu-id="44b32-105">Élément</span><span class="sxs-lookup"><span data-stu-id="44b32-105">Part</span></span>  
 `expression`  
 <span data-ttu-id="44b32-106">Requis dans un `Function`, `Get`, ou `Operator` procédure.</span><span class="sxs-lookup"><span data-stu-id="44b32-106">Required in a `Function`, `Get`, or `Operator` procedure.</span></span> <span data-ttu-id="44b32-107">Expression qui représente la valeur à retourner au code appelant.</span><span class="sxs-lookup"><span data-stu-id="44b32-107">Expression that represents the value to be returned to the calling code.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="44b32-108">Notes</span><span class="sxs-lookup"><span data-stu-id="44b32-108">Remarks</span></span>  
 <span data-ttu-id="44b32-109">Dans un `Sub` ou `Set` procédure, le `Return` instruction est équivalente à une `Exit Sub` ou `Exit Property` instruction, et `expression` ne doit être fournie.</span><span class="sxs-lookup"><span data-stu-id="44b32-109">In a `Sub` or `Set` procedure, the `Return` statement is equivalent to an `Exit Sub` or `Exit Property` statement, and `expression` must not be supplied.</span></span>  
  
 <span data-ttu-id="44b32-110">Dans un `Function`, `Get`, ou `Operator` procédure, le `Return` instruction doit inclure `expression`, et `expression` doit correspondre à un type de données qui est convertible en type de retour de la procédure.</span><span class="sxs-lookup"><span data-stu-id="44b32-110">In a `Function`, `Get`, or `Operator` procedure, the `Return` statement must include `expression`, and `expression` must evaluate to a data type that is convertible to the return type of the procedure.</span></span> <span data-ttu-id="44b32-111">Dans un `Function` ou `Get` procédure, vous avez également la possibilité d’assigner une expression au nom de la procédure pour servir de la valeur de retour et en exécutant ensuite une `Exit Function` ou `Exit Property` instruction.</span><span class="sxs-lookup"><span data-stu-id="44b32-111">In a `Function` or `Get` procedure, you also have the alternative of assigning an expression to the procedure name to serve as the return value, and then executing an `Exit Function` or `Exit Property` statement.</span></span> <span data-ttu-id="44b32-112">Dans un `Operator` procédure, vous devez utiliser `Return expression`.</span><span class="sxs-lookup"><span data-stu-id="44b32-112">In an `Operator` procedure, you must use `Return expression`.</span></span>  
  
 <span data-ttu-id="44b32-113">Vous pouvez inclure autant `Return` instructions comme il convient dans la même procédure.</span><span class="sxs-lookup"><span data-stu-id="44b32-113">You can include as many `Return` statements as appropriate in the same procedure.</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="44b32-114">Le code dans un `Finally` bloc s’exécute après un `Return` instruction dans un `Try` ou `Catch` bloc est rencontré, mais avant que `Return` instruction s’exécute.</span><span class="sxs-lookup"><span data-stu-id="44b32-114">The code in a `Finally` block runs after a `Return` statement in a `Try` or `Catch` block is encountered, but before that `Return` statement executes.</span></span> <span data-ttu-id="44b32-115">Un `Return` instruction ne peut pas être incluse dans un `Finally` bloc.</span><span class="sxs-lookup"><span data-stu-id="44b32-115">A `Return` statement cannot be included in a `Finally` block.</span></span>  
  
## <a name="example"></a><span data-ttu-id="44b32-116">Exemple</span><span class="sxs-lookup"><span data-stu-id="44b32-116">Example</span></span>  
 <span data-ttu-id="44b32-117">L’exemple suivant utilise la `Return` instruction plusieurs fois pour retourner au code appelant lorsque la procédure n’a pas de faire autre chose.</span><span class="sxs-lookup"><span data-stu-id="44b32-117">The following example uses the `Return` statement several times to return to the calling code when the procedure does not have to do anything else.</span></span>  
  
 [!code-vb[VbVbalrStatements#53](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbalrStatements/VB/Class1.vb#53)]  
  
## <a name="see-also"></a><span data-ttu-id="44b32-118">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="44b32-118">See also</span></span>

- [<span data-ttu-id="44b32-119">Function (instruction)</span><span class="sxs-lookup"><span data-stu-id="44b32-119">Function Statement</span></span>](../../../visual-basic/language-reference/statements/function-statement.md)
- [<span data-ttu-id="44b32-120">Sub (instruction)</span><span class="sxs-lookup"><span data-stu-id="44b32-120">Sub Statement</span></span>](../../../visual-basic/language-reference/statements/sub-statement.md)
- [<span data-ttu-id="44b32-121">Get (instruction)</span><span class="sxs-lookup"><span data-stu-id="44b32-121">Get Statement</span></span>](../../../visual-basic/language-reference/statements/get-statement.md)
- [<span data-ttu-id="44b32-122">Set (instruction)</span><span class="sxs-lookup"><span data-stu-id="44b32-122">Set Statement</span></span>](../../../visual-basic/language-reference/statements/set-statement.md)
- [<span data-ttu-id="44b32-123">Operator (instruction)</span><span class="sxs-lookup"><span data-stu-id="44b32-123">Operator Statement</span></span>](../../../visual-basic/language-reference/statements/operator-statement.md)
- [<span data-ttu-id="44b32-124">Property (instruction)</span><span class="sxs-lookup"><span data-stu-id="44b32-124">Property Statement</span></span>](../../../visual-basic/language-reference/statements/property-statement.md)
- [<span data-ttu-id="44b32-125">Exit (instruction)</span><span class="sxs-lookup"><span data-stu-id="44b32-125">Exit Statement</span></span>](../../../visual-basic/language-reference/statements/exit-statement.md)
- [<span data-ttu-id="44b32-126">Try...Catch...Finally (instruction)</span><span class="sxs-lookup"><span data-stu-id="44b32-126">Try...Catch...Finally Statement</span></span>](../../../visual-basic/language-reference/statements/try-catch-finally-statement.md)
