---
title: Constantes et types de données littérales (Visual Basic)
ms.date: 07/20/2015
helpviewer_keywords:
- declaring constants [Visual Basic], literal data types
- data types [Visual Basic], declaring
- constants [Visual Basic], declaring
- explicit declarations
- literals [Visual Basic], coercing data type
- declarations [Visual Basic], data types
ms.assetid: 057206d2-3a5b-40b9-b3af-57446f9b52fa
ms.openlocfilehash: 50e36aa13439bafcca27a7153a8c5d6043f03975
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "58833501"
---
# <a name="constant-and-literal-data-types-visual-basic"></a><span data-ttu-id="17cbc-102">Constantes et types de données littérales (Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="17cbc-102">Constant and Literal Data Types (Visual Basic)</span></span>
<span data-ttu-id="17cbc-103">Un littéral est une valeur qui est exprimée en tant que telle, plutôt que comme valeur d’une variable ou le résultat d’une expression, telles que le nombre 3 ou la chaîne « Hello ».</span><span class="sxs-lookup"><span data-stu-id="17cbc-103">A literal is a value that is expressed as itself rather than as a variable's value or the result of an expression, such as the number 3 or the string "Hello".</span></span> <span data-ttu-id="17cbc-104">Une constante est un nom significatif qui prend la place d’un littéral et conserve cette même valeur tout au long du programme, par opposition à une variable, dont la valeur peut changer.</span><span class="sxs-lookup"><span data-stu-id="17cbc-104">A constant is a meaningful name that takes the place of a literal and retains this same value throughout the program, as opposed to a variable, whose value may change.</span></span>  
  
 <span data-ttu-id="17cbc-105">Lorsque [Option Infer](../../../../visual-basic/language-reference/statements/option-infer-statement.md) est `Off` et [Option Strict](../../../../visual-basic/language-reference/statements/option-strict-statement.md) est `On`, vous devez déclarer explicitement toutes les constantes avec un type de données.</span><span class="sxs-lookup"><span data-stu-id="17cbc-105">When [Option Infer](../../../../visual-basic/language-reference/statements/option-infer-statement.md) is `Off` and [Option Strict](../../../../visual-basic/language-reference/statements/option-strict-statement.md) is `On`, you must declare all constants explicitly with a data type.</span></span> <span data-ttu-id="17cbc-106">Dans l’exemple suivant, le type de données `MyByte` est déclaré explicitement comme type de données `Byte`:</span><span class="sxs-lookup"><span data-stu-id="17cbc-106">In the following example, the data type of `MyByte` is explicitly declared as data type `Byte`:</span></span>  
  
 [!code-vb[VbVbalrConstants#1](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbalrConstants/VB/Class1.vb#1)]  
  
 <span data-ttu-id="17cbc-107">Lorsque `Option Infer` est `On` ou `Option Strict` est `Off`, vous pouvez déclarer une constante sans spécifier un type de données avec un `As` clause.</span><span class="sxs-lookup"><span data-stu-id="17cbc-107">When `Option Infer` is `On` or `Option Strict` is `Off`, you can declare a constant without specifying a data type with an `As` clause.</span></span> <span data-ttu-id="17cbc-108">Le compilateur détermine le type de la constante à partir du type de l’expression.</span><span class="sxs-lookup"><span data-stu-id="17cbc-108">The compiler determines the type of the constant from the type of the expression.</span></span> <span data-ttu-id="17cbc-109">Effectuer un cast d’un littéral entier numérique par défaut pour le `Integer` type de données.</span><span class="sxs-lookup"><span data-stu-id="17cbc-109">A numeric integer literal is cast by default to the `Integer` data type.</span></span> <span data-ttu-id="17cbc-110">Type de données par défaut pour les nombres à virgule flottante est `Double`et les mots clés `True` et `False` spécifier un `Boolean` constante.</span><span class="sxs-lookup"><span data-stu-id="17cbc-110">The default data type for floating-point numbers is `Double`, and the keywords `True` and `False` specify a `Boolean` constant.</span></span>  
  
## <a name="literals-and-type-coercion"></a><span data-ttu-id="17cbc-111">Littéraux et forçage de Type</span><span class="sxs-lookup"><span data-stu-id="17cbc-111">Literals and Type Coercion</span></span>  
 <span data-ttu-id="17cbc-112">Dans certains cas, vous pouvez souhaiter forcer un littéral à un type de données particulier ; par exemple, lors de l’attribution d’une très grande valeur littérale intégrale à une variable de type `Decimal`.</span><span class="sxs-lookup"><span data-stu-id="17cbc-112">In some cases, you might want to force a literal to a particular data type; for example, when assigning a particularly large integral literal value to a variable of type `Decimal`.</span></span> <span data-ttu-id="17cbc-113">L’exemple suivant génère une erreur :</span><span class="sxs-lookup"><span data-stu-id="17cbc-113">The following example produces an error:</span></span>  
  
```  
Dim myDecimal as Decimal  
myDecimal = 100000000000000000000   ' This causes a compiler error.  
```  
  
 <span data-ttu-id="17cbc-114">L’erreur produit de la représentation du littéral.</span><span class="sxs-lookup"><span data-stu-id="17cbc-114">The error results from the representation of the literal.</span></span> <span data-ttu-id="17cbc-115">Le `Decimal` type de données peut contenir une valeur de cette taille, mais le littéral est implicitement représenté comme un `Long`, qui ne peut pas.</span><span class="sxs-lookup"><span data-stu-id="17cbc-115">The `Decimal` data type can hold a value this large, but the literal is implicitly represented as a `Long`, which cannot.</span></span>  
  
 <span data-ttu-id="17cbc-116">Vous pouvez forcer un littéral en un type de données particulier de deux manières : en ajoutant un caractère de type à elle, ou en le plaçant entre des caractères englobants.</span><span class="sxs-lookup"><span data-stu-id="17cbc-116">You can coerce a literal to a particular data type in two ways: by appending a type character to it, or by placing it within enclosing characters.</span></span> <span data-ttu-id="17cbc-117">Un caractère de type ou les caractères englobants doivent immédiatement précéder et/ou suivre le littéral, sans espace intermédiaire ou les caractères de n’importe quel type.</span><span class="sxs-lookup"><span data-stu-id="17cbc-117">A type character or enclosing characters must immediately precede and/or follow the literal, with no intervening space or characters of any kind.</span></span>  
  
 <span data-ttu-id="17cbc-118">Pour que l’exemple précédent fonctionne, vous pouvez ajouter la `D` tapez le caractère littéral, ce qui entraîne sa être représentée comme un `Decimal`:</span><span class="sxs-lookup"><span data-stu-id="17cbc-118">To make the previous example work, you can append the `D` type character to the literal, which causes it to be represented as a `Decimal`:</span></span>  
  
 [!code-vb[VbVbalrConstants#2](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbalrConstants/VB/Class1.vb#2)]  
  
 <span data-ttu-id="17cbc-119">L’exemple suivant montre une utilisation correcte des caractères de type et les caractères englobants :</span><span class="sxs-lookup"><span data-stu-id="17cbc-119">The following example demonstrates correct usage of type characters and enclosing characters:</span></span>  
  
 [!code-vb[VbVbalrConstants#3](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbalrConstants/VB/Class1.vb#3)]  
  
 <span data-ttu-id="17cbc-120">Le tableau suivant présente les caractères englobants et les caractères de type disponibles dans Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="17cbc-120">The following table shows the enclosing characters and type characters available in Visual Basic.</span></span>  
  
|<span data-ttu-id="17cbc-121">Type de données</span><span class="sxs-lookup"><span data-stu-id="17cbc-121">Data type</span></span>|<span data-ttu-id="17cbc-122">Caractère englobant</span><span class="sxs-lookup"><span data-stu-id="17cbc-122">Enclosing character</span></span>|<span data-ttu-id="17cbc-123">Caractère de type ajouté</span><span class="sxs-lookup"><span data-stu-id="17cbc-123">Appended type character</span></span>|  
|---|---|---|  
|`Boolean`|<span data-ttu-id="17cbc-124">(aucun)</span><span class="sxs-lookup"><span data-stu-id="17cbc-124">(none)</span></span>|<span data-ttu-id="17cbc-125">(aucun)</span><span class="sxs-lookup"><span data-stu-id="17cbc-125">(none)</span></span>|  
|`Byte`|<span data-ttu-id="17cbc-126">(aucun)</span><span class="sxs-lookup"><span data-stu-id="17cbc-126">(none)</span></span>|<span data-ttu-id="17cbc-127">(aucun)</span><span class="sxs-lookup"><span data-stu-id="17cbc-127">(none)</span></span>|  
|`Char`|<span data-ttu-id="17cbc-128">"</span><span class="sxs-lookup"><span data-stu-id="17cbc-128">"</span></span>|<span data-ttu-id="17cbc-129">C</span><span class="sxs-lookup"><span data-stu-id="17cbc-129">C</span></span>|  
|`Date`|#|<span data-ttu-id="17cbc-130">(aucun)</span><span class="sxs-lookup"><span data-stu-id="17cbc-130">(none)</span></span>|  
|`Decimal`|<span data-ttu-id="17cbc-131">(aucun)</span><span class="sxs-lookup"><span data-stu-id="17cbc-131">(none)</span></span>|<span data-ttu-id="17cbc-132">D ou @</span><span class="sxs-lookup"><span data-stu-id="17cbc-132">D or @</span></span>|  
|`Double`|<span data-ttu-id="17cbc-133">(aucun)</span><span class="sxs-lookup"><span data-stu-id="17cbc-133">(none)</span></span>|<span data-ttu-id="17cbc-134">R ou #</span><span class="sxs-lookup"><span data-stu-id="17cbc-134">R or #</span></span>|  
|`Integer`|<span data-ttu-id="17cbc-135">(aucun)</span><span class="sxs-lookup"><span data-stu-id="17cbc-135">(none)</span></span>|<span data-ttu-id="17cbc-136">I ou %</span><span class="sxs-lookup"><span data-stu-id="17cbc-136">I or %</span></span>|  
|`Long`|<span data-ttu-id="17cbc-137">(aucun)</span><span class="sxs-lookup"><span data-stu-id="17cbc-137">(none)</span></span>|<span data-ttu-id="17cbc-138">L ou &</span><span class="sxs-lookup"><span data-stu-id="17cbc-138">L or &</span></span>|  
|`Short`|<span data-ttu-id="17cbc-139">(aucun)</span><span class="sxs-lookup"><span data-stu-id="17cbc-139">(none)</span></span>|<span data-ttu-id="17cbc-140">S</span><span class="sxs-lookup"><span data-stu-id="17cbc-140">S</span></span>|  
|`Single`|<span data-ttu-id="17cbc-141">(aucun)</span><span class="sxs-lookup"><span data-stu-id="17cbc-141">(none)</span></span>|<span data-ttu-id="17cbc-142">F ou !</span><span class="sxs-lookup"><span data-stu-id="17cbc-142">F or !</span></span>|  
|`String`|<span data-ttu-id="17cbc-143">"</span><span class="sxs-lookup"><span data-stu-id="17cbc-143">"</span></span>|<span data-ttu-id="17cbc-144">(aucun)</span><span class="sxs-lookup"><span data-stu-id="17cbc-144">(none)</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="17cbc-145">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="17cbc-145">See also</span></span>

- [<span data-ttu-id="17cbc-146">Constantes définies par l’utilisateur</span><span class="sxs-lookup"><span data-stu-id="17cbc-146">User-Defined Constants</span></span>](../../../../visual-basic/programming-guide/language-features/constants-enums/user-defined-constants.md)
- [<span data-ttu-id="17cbc-147">Guide pratique pour Déclarer une constante</span><span class="sxs-lookup"><span data-stu-id="17cbc-147">How to: Declare A Constant</span></span>](../../../../visual-basic/programming-guide/language-features/constants-enums/how-to-declare-a-constant.md)
- [<span data-ttu-id="17cbc-148">Vue d’ensemble des constantes</span><span class="sxs-lookup"><span data-stu-id="17cbc-148">Constants Overview</span></span>](../../../../visual-basic/programming-guide/language-features/constants-enums/constants-overview.md)
- [<span data-ttu-id="17cbc-149">Option Strict (instruction)</span><span class="sxs-lookup"><span data-stu-id="17cbc-149">Option Strict Statement</span></span>](../../../../visual-basic/language-reference/statements/option-strict-statement.md)
- [<span data-ttu-id="17cbc-150">Option Explicit (instruction)</span><span class="sxs-lookup"><span data-stu-id="17cbc-150">Option Explicit Statement</span></span>](../../../../visual-basic/language-reference/statements/option-explicit-statement.md)
- [<span data-ttu-id="17cbc-151">Vue d’ensemble des énumérations</span><span class="sxs-lookup"><span data-stu-id="17cbc-151">Enumerations Overview</span></span>](../../../../visual-basic/programming-guide/language-features/constants-enums/enumerations-overview.md)
- [<span data-ttu-id="17cbc-152">Guide pratique pour Déclarer une énumération</span><span class="sxs-lookup"><span data-stu-id="17cbc-152">How to: Declare an Enumeration</span></span>](../../../../visual-basic/programming-guide/language-features/constants-enums/how-to-declare-enumerations.md)
- [<span data-ttu-id="17cbc-153">Énumérations et qualification de noms</span><span class="sxs-lookup"><span data-stu-id="17cbc-153">Enumerations and Name Qualification</span></span>](../../../../visual-basic/programming-guide/language-features/constants-enums/enumerations-and-name-qualification.md)
- [<span data-ttu-id="17cbc-154">Types de données</span><span class="sxs-lookup"><span data-stu-id="17cbc-154">Data Types</span></span>](../../../../visual-basic/language-reference/data-types/index.md)
- [<span data-ttu-id="17cbc-155">Constantes et énumérations</span><span class="sxs-lookup"><span data-stu-id="17cbc-155">Constants and Enumerations</span></span>](../../../../visual-basic/language-reference/constants-and-enumerations.md)
