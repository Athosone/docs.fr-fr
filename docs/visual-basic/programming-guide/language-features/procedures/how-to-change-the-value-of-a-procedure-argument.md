---
title: 'Procédure : Modifiez la valeur d’un Argument de procédure (Visual Basic)'
ms.date: 07/20/2015
helpviewer_keywords:
- procedures [Visual Basic], arguments
- procedures [Visual Basic], parameters
- procedure arguments
- arguments [Visual Basic], passing by reference
- Visual Basic code, procedures
- arguments [Visual Basic], ByVal
- arguments [Visual Basic], passing by value
- procedure parameters
- arguments [Visual Basic], ByRef
- arguments [Visual Basic], changing value
ms.assetid: 6fad2368-5da7-4c07-8bf8-0f4e65a1be67
ms.openlocfilehash: a56bdf888163c9559b87e857abb33522c547ed45
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59316620"
---
# <a name="how-to-change-the-value-of-a-procedure-argument-visual-basic"></a><span data-ttu-id="e7b85-102">Procédure : Modifiez la valeur d’un Argument de procédure (Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="e7b85-102">How to: Change the Value of a Procedure Argument (Visual Basic)</span></span>
<span data-ttu-id="e7b85-103">Lorsque vous appelez une procédure, chaque argument que vous fournissez correspond à un des paramètres définis dans la procédure.</span><span class="sxs-lookup"><span data-stu-id="e7b85-103">When you call a procedure, each argument you supply corresponds to one of the parameters defined in the procedure.</span></span> <span data-ttu-id="e7b85-104">Dans certains cas, le code de procédure peut modifier la valeur sous-jacente d’un argument dans le code appelant.</span><span class="sxs-lookup"><span data-stu-id="e7b85-104">In some cases, the procedure code can change the value underlying an argument in the calling code.</span></span> <span data-ttu-id="e7b85-105">Dans d’autres cas, la procédure peut modifier uniquement sa copie locale d’un argument.</span><span class="sxs-lookup"><span data-stu-id="e7b85-105">In other cases, the procedure can change only its local copy of an argument.</span></span>  
  
 <span data-ttu-id="e7b85-106">Lorsque vous appelez la procédure, Visual Basic effectue une copie locale de chaque argument est passé [ByVal](../../../../visual-basic/language-reference/modifiers/byval.md).</span><span class="sxs-lookup"><span data-stu-id="e7b85-106">When you call the procedure, Visual Basic makes a local copy of every argument that is passed [ByVal](../../../../visual-basic/language-reference/modifiers/byval.md).</span></span> <span data-ttu-id="e7b85-107">Pour chaque argument passé [ByRef](../../../../visual-basic/language-reference/modifiers/byref.md), Visual Basic fournit le code de procédure une référence directe à l’élément de programmation sous-jacent à l’argument dans le code appelant.</span><span class="sxs-lookup"><span data-stu-id="e7b85-107">For each argument passed [ByRef](../../../../visual-basic/language-reference/modifiers/byref.md), Visual Basic gives the procedure code a direct reference to the programming element underlying the argument in the calling code.</span></span>  
  
 <span data-ttu-id="e7b85-108">Si l’élément sous-jacent dans le code appelant est un élément modifiable et que l’argument est passé `ByRef`, le code de procédure peut utiliser la référence directe pour modifier la valeur de l’élément dans le code appelant.</span><span class="sxs-lookup"><span data-stu-id="e7b85-108">If the underlying element in the calling code is a modifiable element and the argument is passed `ByRef`, the procedure code can use the direct reference to change the element's value in the calling code.</span></span>  
  
## <a name="changing-the-underlying-value"></a><span data-ttu-id="e7b85-109">Modification de la valeur sous-jacente</span><span class="sxs-lookup"><span data-stu-id="e7b85-109">Changing the Underlying Value</span></span>  
  
#### <a name="to-change-the-underlying-value-of-a-procedure-argument-in-the-calling-code"></a><span data-ttu-id="e7b85-110">Pour modifier la valeur sous-jacente d’un argument de procédure dans le code appelant</span><span class="sxs-lookup"><span data-stu-id="e7b85-110">To change the underlying value of a procedure argument in the calling code</span></span>  
  
1. <span data-ttu-id="e7b85-111">Dans la déclaration de procédure, spécifiez [ByRef](../../../../visual-basic/language-reference/modifiers/byref.md) pour le paramètre correspondant à l’argument.</span><span class="sxs-lookup"><span data-stu-id="e7b85-111">In the procedure declaration, specify [ByRef](../../../../visual-basic/language-reference/modifiers/byref.md) for the parameter corresponding to the argument.</span></span>  
  
2. <span data-ttu-id="e7b85-112">Dans le code appelant, passez un élément de programmation modifiable comme argument.</span><span class="sxs-lookup"><span data-stu-id="e7b85-112">In the calling code, pass a modifiable programming element as the argument.</span></span>  
  
3. <span data-ttu-id="e7b85-113">Dans le code appelant, ne placez pas l’argument entre parenthèses dans la liste d’arguments.</span><span class="sxs-lookup"><span data-stu-id="e7b85-113">In the calling code, do not enclose the argument in parentheses in the argument list.</span></span>  
  
4. <span data-ttu-id="e7b85-114">Dans le code de procédure, utilisez le nom de paramètre pour affecter une valeur à l’élément sous-jacent dans le code appelant.</span><span class="sxs-lookup"><span data-stu-id="e7b85-114">In the procedure code, use the parameter name to assign a value to the underlying element in the calling code.</span></span>  
  
 <span data-ttu-id="e7b85-115">Consultez l’exemple ci-dessous pour une démonstration.</span><span class="sxs-lookup"><span data-stu-id="e7b85-115">See the example further down for a demonstration.</span></span>  
  
## <a name="changing-local-copies"></a><span data-ttu-id="e7b85-116">Modification des Copies locales</span><span class="sxs-lookup"><span data-stu-id="e7b85-116">Changing Local Copies</span></span>  
 <span data-ttu-id="e7b85-117">Si l’élément sous-jacent dans le code appelant est un élément non modifiable, ou si l’argument est passé `ByVal`, la procédure ne peut pas modifier sa valeur dans le code appelant.</span><span class="sxs-lookup"><span data-stu-id="e7b85-117">If the underlying element in the calling code is a nonmodifiable element, or if the argument is passed `ByVal`, the procedure cannot change its value in the calling code.</span></span> <span data-ttu-id="e7b85-118">Toutefois, la procédure peut modifier sa copie locale de l’argument.</span><span class="sxs-lookup"><span data-stu-id="e7b85-118">However, the procedure can change its local copy of such an argument.</span></span>  
  
#### <a name="to-change-the-copy-of-a-procedure-argument-in-the-procedure-code"></a><span data-ttu-id="e7b85-119">Pour modifier la copie d’un argument de procédure dans le code de procédure</span><span class="sxs-lookup"><span data-stu-id="e7b85-119">To change the copy of a procedure argument in the procedure code</span></span>  
  
1. <span data-ttu-id="e7b85-120">Dans la déclaration de procédure, spécifiez [ByVal](../../../../visual-basic/language-reference/modifiers/byval.md) pour le paramètre correspondant à l’argument.</span><span class="sxs-lookup"><span data-stu-id="e7b85-120">In the procedure declaration, specify [ByVal](../../../../visual-basic/language-reference/modifiers/byval.md) for the parameter corresponding to the argument.</span></span>  
  
     <span data-ttu-id="e7b85-121">- ou -</span><span class="sxs-lookup"><span data-stu-id="e7b85-121">-or-</span></span>  
  
     <span data-ttu-id="e7b85-122">Dans le code appelant, mettez l’argument entre parenthèses dans la liste d’arguments.</span><span class="sxs-lookup"><span data-stu-id="e7b85-122">In the calling code, enclose the argument in parentheses in the argument list.</span></span> <span data-ttu-id="e7b85-123">Cela force Visual Basic pour passer l’argument par valeur, même si le paramètre correspondant spécifie `ByRef`.</span><span class="sxs-lookup"><span data-stu-id="e7b85-123">This forces Visual Basic to pass the argument by value, even if the corresponding parameter specifies `ByRef`.</span></span>  
  
2. <span data-ttu-id="e7b85-124">Dans le code de procédure, utilisez le nom de paramètre pour assigner une valeur à la copie locale de l’argument.</span><span class="sxs-lookup"><span data-stu-id="e7b85-124">In the procedure code, use the parameter name to assign a value to the local copy of the argument.</span></span> <span data-ttu-id="e7b85-125">La valeur sous-jacente dans le code appelant n’est pas modifiée.</span><span class="sxs-lookup"><span data-stu-id="e7b85-125">The underlying value in the calling code is not changed.</span></span>  
  
## <a name="example"></a><span data-ttu-id="e7b85-126">Exemple</span><span class="sxs-lookup"><span data-stu-id="e7b85-126">Example</span></span>  
 <span data-ttu-id="e7b85-127">L’exemple suivant montre deux procédures qui acceptent une variable tableau et opèrent sur ses éléments.</span><span class="sxs-lookup"><span data-stu-id="e7b85-127">The following example shows two procedures that take an array variable and operate on its elements.</span></span> <span data-ttu-id="e7b85-128">Le `increase` procédure ajoute simplement 1 à chaque élément.</span><span class="sxs-lookup"><span data-stu-id="e7b85-128">The `increase` procedure simply adds one to each element.</span></span> <span data-ttu-id="e7b85-129">Le `replace` procédure assigne un nouveau tableau au paramètre `a()` , puis ajoute 1 à chaque élément.</span><span class="sxs-lookup"><span data-stu-id="e7b85-129">The `replace` procedure assigns a new array to the parameter `a()` and then adds one to each element.</span></span>  
  
 [!code-vb[VbVbcnProcedures#35](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbcnProcedures/VB/Class1.vb#35)]  
  
 [!code-vb[VbVbcnProcedures#36](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbcnProcedures/VB/Class1.vb#36)]  
  
 [!code-vb[VbVbcnProcedures#37](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbcnProcedures/VB/Class1.vb#37)]  
  
 <span data-ttu-id="e7b85-130">Le premier `MsgBox` appel affiche « après Increase (n) : 11, 21, 31, 41".</span><span class="sxs-lookup"><span data-stu-id="e7b85-130">The first `MsgBox` call displays "After increase(n): 11, 21, 31, 41".</span></span> <span data-ttu-id="e7b85-131">Étant donné que le tableau `n` est un type référence, `replace` peut modifier ses membres, même si le mécanisme de passage est `ByVal`.</span><span class="sxs-lookup"><span data-stu-id="e7b85-131">Because the array `n` is a reference type, `replace` can change its members, even though the passing mechanism is `ByVal`.</span></span>  
  
 <span data-ttu-id="e7b85-132">La seconde `MsgBox` appel affiche « après Replace (n) : 101, 201, 301".</span><span class="sxs-lookup"><span data-stu-id="e7b85-132">The second `MsgBox` call displays "After replace(n): 101, 201, 301".</span></span> <span data-ttu-id="e7b85-133">Étant donné que `n` est passée `ByRef`, `replace` peut modifier la variable `n` dans le code appelant et affecter un nouveau tableau.</span><span class="sxs-lookup"><span data-stu-id="e7b85-133">Because `n` is passed `ByRef`, `replace` can modify the variable `n` in the calling code and assign a new array to it.</span></span> <span data-ttu-id="e7b85-134">Étant donné que `n` est un type référence, `replace` peut également modifier ses membres.</span><span class="sxs-lookup"><span data-stu-id="e7b85-134">Because `n` is a reference type, `replace` can also change its members.</span></span>  
  
 <span data-ttu-id="e7b85-135">Vous pouvez empêcher la procédure de modification de la variable elle-même dans le code appelant.</span><span class="sxs-lookup"><span data-stu-id="e7b85-135">You can prevent the procedure from modifying the variable itself in the calling code.</span></span> <span data-ttu-id="e7b85-136">Voir [Guide pratique pour Protéger un Argument de procédure contre les modifications de valeur](./how-to-protect-a-procedure-argument-against-value-changes.md).</span><span class="sxs-lookup"><span data-stu-id="e7b85-136">See [How to: Protect a Procedure Argument Against Value Changes](./how-to-protect-a-procedure-argument-against-value-changes.md).</span></span>  
  
## <a name="compiling-the-code"></a><span data-ttu-id="e7b85-137">Compilation du code</span><span class="sxs-lookup"><span data-stu-id="e7b85-137">Compiling the Code</span></span>  
 <span data-ttu-id="e7b85-138">Lorsque vous passez une variable par référence, vous devez utiliser le `ByRef` mot clé pour spécifier ce mécanisme.</span><span class="sxs-lookup"><span data-stu-id="e7b85-138">When you pass a variable by reference, you must use the `ByRef` keyword to specify this mechanism.</span></span>  
  
 <span data-ttu-id="e7b85-139">La valeur par défaut en Visual Basic consiste à passer des arguments par valeur.</span><span class="sxs-lookup"><span data-stu-id="e7b85-139">The default in Visual Basic is to pass arguments by value.</span></span> <span data-ttu-id="e7b85-140">Toutefois, il est conseillé en programmation pour inclure le [ByVal](../../../../visual-basic/language-reference/modifiers/byval.md) ou [ByRef](../../../../visual-basic/language-reference/modifiers/byref.md) keyword avec chaque paramètre déclaré.</span><span class="sxs-lookup"><span data-stu-id="e7b85-140">However, it is good programming practice to include either the [ByVal](../../../../visual-basic/language-reference/modifiers/byval.md) or [ByRef](../../../../visual-basic/language-reference/modifiers/byref.md) keyword with every declared parameter.</span></span> <span data-ttu-id="e7b85-141">Cela rend votre code plus facile à lire.</span><span class="sxs-lookup"><span data-stu-id="e7b85-141">This makes your code easier to read.</span></span>  
  
## <a name="net-framework-security"></a><span data-ttu-id="e7b85-142">Sécurité .NET Framework</span><span class="sxs-lookup"><span data-stu-id="e7b85-142">.NET Framework Security</span></span>  
 <span data-ttu-id="e7b85-143">Il y a toujours un risque de permettre à une procédure modifier la valeur sous-jacente à un argument dans le code appelant.</span><span class="sxs-lookup"><span data-stu-id="e7b85-143">There is always a potential risk in allowing a procedure to change the value underlying an argument in the calling code.</span></span> <span data-ttu-id="e7b85-144">Assurez-vous que cette valeur pour être modifié et être prêt à vérifier la validité avant de l’utiliser.</span><span class="sxs-lookup"><span data-stu-id="e7b85-144">Make sure you expect this value to be changed, and be prepared to check it for validity before using it.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="e7b85-145">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e7b85-145">See also</span></span>

- [<span data-ttu-id="e7b85-146">Procédures</span><span class="sxs-lookup"><span data-stu-id="e7b85-146">Procedures</span></span>](./index.md)
- [<span data-ttu-id="e7b85-147">Paramètres et arguments d’une procédure</span><span class="sxs-lookup"><span data-stu-id="e7b85-147">Procedure Parameters and Arguments</span></span>](./procedure-parameters-and-arguments.md)
- [<span data-ttu-id="e7b85-148">Guide pratique pour Passer des Arguments à une procédure</span><span class="sxs-lookup"><span data-stu-id="e7b85-148">How to: Pass Arguments to a Procedure</span></span>](./how-to-pass-arguments-to-a-procedure.md)
- [<span data-ttu-id="e7b85-149">Passage d’un argument par valeur et par référence</span><span class="sxs-lookup"><span data-stu-id="e7b85-149">Passing Arguments by Value and by Reference</span></span>](./passing-arguments-by-value-and-by-reference.md)
- [<span data-ttu-id="e7b85-150">Différences entre les arguments modifiables et non modifiables</span><span class="sxs-lookup"><span data-stu-id="e7b85-150">Differences Between Modifiable and Nonmodifiable Arguments</span></span>](./differences-between-modifiable-and-nonmodifiable-arguments.md)
- [<span data-ttu-id="e7b85-151">Différences entre le passage d’un argument par valeur et par référence</span><span class="sxs-lookup"><span data-stu-id="e7b85-151">Differences Between Passing an Argument By Value and By Reference</span></span>](./differences-between-passing-an-argument-by-value-and-by-reference.md)
- [<span data-ttu-id="e7b85-152">Guide pratique pour Protéger un Argument de procédure contre les modifications de valeur</span><span class="sxs-lookup"><span data-stu-id="e7b85-152">How to: Protect a Procedure Argument Against Value Changes</span></span>](./how-to-protect-a-procedure-argument-against-value-changes.md)
- [<span data-ttu-id="e7b85-153">Guide pratique pour Forcer un Argument d’être passés par valeur</span><span class="sxs-lookup"><span data-stu-id="e7b85-153">How to: Force an Argument to Be Passed by Value</span></span>](./how-to-force-an-argument-to-be-passed-by-value.md)
- [<span data-ttu-id="e7b85-154">Passage des arguments par position et par nom</span><span class="sxs-lookup"><span data-stu-id="e7b85-154">Passing Arguments by Position and by Name</span></span>](./passing-arguments-by-position-and-by-name.md)
- [<span data-ttu-id="e7b85-155">Value Types and Reference Types</span><span class="sxs-lookup"><span data-stu-id="e7b85-155">Value Types and Reference Types</span></span>](../../../../visual-basic/programming-guide/language-features/data-types/value-types-and-reference-types.md)
