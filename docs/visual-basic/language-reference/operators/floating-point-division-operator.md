---
title: /, opérateur (Visual Basic)
ms.date: 07/20/2015
f1_keywords:
- vb./
helpviewer_keywords:
- division operator [Visual Basic], floating point
- floating-point numbers [Visual Basic], division operator
- slash (/) operator
- zero, division by zero
- operators [Visual Basic], arithmetic
- arithmetic operators [Visual Basic], division
- division [Visual Basic], by zero
- operators [Visual Basic], division
- division operator [Visual Basic], syntax
- / operator [Visual Basic]
- math operators [Visual Basic]
ms.assetid: 335e97f2-c434-439e-9064-76973a051101
ms.openlocfilehash: af2316f92e2904eee1e8c046b34b8147e40cb513
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "58825064"
---
# <a name="-operator-visual-basic"></a><span data-ttu-id="5be8d-102">/, opérateur (Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="5be8d-102">/ Operator (Visual Basic)</span></span>
<span data-ttu-id="5be8d-103">Divise deux nombres et retourne un résultat à virgule flottante.</span><span class="sxs-lookup"><span data-stu-id="5be8d-103">Divides two numbers and returns a floating-point result.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="5be8d-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="5be8d-104">Syntax</span></span>  
  
```  
expression1 / expression2  
```  
  
## <a name="parts"></a><span data-ttu-id="5be8d-105">Composants</span><span class="sxs-lookup"><span data-stu-id="5be8d-105">Parts</span></span>  
 `expression1`  
 <span data-ttu-id="5be8d-106">Obligatoire.</span><span class="sxs-lookup"><span data-stu-id="5be8d-106">Required.</span></span> <span data-ttu-id="5be8d-107">Toute expression numérique.</span><span class="sxs-lookup"><span data-stu-id="5be8d-107">Any numeric expression.</span></span>  
  
 `expression2`  
 <span data-ttu-id="5be8d-108">Obligatoire.</span><span class="sxs-lookup"><span data-stu-id="5be8d-108">Required.</span></span> <span data-ttu-id="5be8d-109">Toute expression numérique.</span><span class="sxs-lookup"><span data-stu-id="5be8d-109">Any numeric expression.</span></span>  
  
## <a name="supported-types"></a><span data-ttu-id="5be8d-110">Types pris en charge</span><span class="sxs-lookup"><span data-stu-id="5be8d-110">Supported Types</span></span>  
 <span data-ttu-id="5be8d-111">Tous les types numériques, y compris les types non signés et à virgule flottante et `Decimal`.</span><span class="sxs-lookup"><span data-stu-id="5be8d-111">All numeric types, including the unsigned and floating-point types and `Decimal`.</span></span>  
  
## <a name="result"></a><span data-ttu-id="5be8d-112">Résultat</span><span class="sxs-lookup"><span data-stu-id="5be8d-112">Result</span></span>  
 <span data-ttu-id="5be8d-113">Le résultat est le quotient entier de `expression1` divisé par `expression2`, y compris tout élément restant.</span><span class="sxs-lookup"><span data-stu-id="5be8d-113">The result is the full quotient of `expression1` divided by `expression2`, including any remainder.</span></span>  
  
 <span data-ttu-id="5be8d-114">Le [\, opérateur (Visual Basic)](../../../visual-basic/language-reference/operators/integer-division-operator.md) renvoie le quotient entier, ce qui supprime le reste.</span><span class="sxs-lookup"><span data-stu-id="5be8d-114">The [\ Operator (Visual Basic)](../../../visual-basic/language-reference/operators/integer-division-operator.md) returns the integer quotient, which drops the remainder.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="5be8d-115">Notes</span><span class="sxs-lookup"><span data-stu-id="5be8d-115">Remarks</span></span>  
 <span data-ttu-id="5be8d-116">Le type de données du résultat dépend des types des opérandes.</span><span class="sxs-lookup"><span data-stu-id="5be8d-116">The data type of the result depends on the types of the operands.</span></span> <span data-ttu-id="5be8d-117">Le tableau suivant montre comment le type de données du résultat est déterminé.</span><span class="sxs-lookup"><span data-stu-id="5be8d-117">The following table shows how the data type of the result is determined.</span></span>  
  
|<span data-ttu-id="5be8d-118">Types de données d’opérande</span><span class="sxs-lookup"><span data-stu-id="5be8d-118">Operand data types</span></span>|<span data-ttu-id="5be8d-119">Type de données de résultat</span><span class="sxs-lookup"><span data-stu-id="5be8d-119">Result data type</span></span>|  
|------------------------|----------------------|  
|<span data-ttu-id="5be8d-120">Les deux expressions sont des types de données intégraux ([SByte](../../../visual-basic/language-reference/data-types/sbyte-data-type.md), [octets](../../../visual-basic/language-reference/data-types/byte-data-type.md), [court](../../../visual-basic/language-reference/data-types/short-data-type.md), [UShort](../../../visual-basic/language-reference/data-types/ushort-data-type.md), [entier](../../../visual-basic/language-reference/data-types/integer-data-type.md), [UInteger](../../../visual-basic/language-reference/data-types/uinteger-data-type.md), [Long](../../../visual-basic/language-reference/data-types/long-data-type.md), [ULong](../../../visual-basic/language-reference/data-types/ulong-data-type.md))</span><span class="sxs-lookup"><span data-stu-id="5be8d-120">Both expressions are integral data types ([SByte](../../../visual-basic/language-reference/data-types/sbyte-data-type.md), [Byte](../../../visual-basic/language-reference/data-types/byte-data-type.md), [Short](../../../visual-basic/language-reference/data-types/short-data-type.md), [UShort](../../../visual-basic/language-reference/data-types/ushort-data-type.md), [Integer](../../../visual-basic/language-reference/data-types/integer-data-type.md), [UInteger](../../../visual-basic/language-reference/data-types/uinteger-data-type.md), [Long](../../../visual-basic/language-reference/data-types/long-data-type.md), [ULong](../../../visual-basic/language-reference/data-types/ulong-data-type.md))</span></span>|`Double`|  
|<span data-ttu-id="5be8d-121">Une expression est un [unique](../../../visual-basic/language-reference/data-types/single-data-type.md) type de données et l’autre n’est pas un [Double](../../../visual-basic/language-reference/data-types/double-data-type.md)</span><span class="sxs-lookup"><span data-stu-id="5be8d-121">One expression is a [Single](../../../visual-basic/language-reference/data-types/single-data-type.md) data type and the other is not a [Double](../../../visual-basic/language-reference/data-types/double-data-type.md)</span></span>|`Single`|  
|<span data-ttu-id="5be8d-122">Une expression est un [décimal](../../../visual-basic/language-reference/data-types/decimal-data-type.md) type de données et l’autre n’est pas un [unique](../../../visual-basic/language-reference/data-types/single-data-type.md) ou un [Double](../../../visual-basic/language-reference/data-types/double-data-type.md)</span><span class="sxs-lookup"><span data-stu-id="5be8d-122">One expression is a [Decimal](../../../visual-basic/language-reference/data-types/decimal-data-type.md) data type and the other is not a [Single](../../../visual-basic/language-reference/data-types/single-data-type.md) or a [Double](../../../visual-basic/language-reference/data-types/double-data-type.md)</span></span>|`Decimal`|  
|<span data-ttu-id="5be8d-123">Des expressions sont un [Double](../../../visual-basic/language-reference/data-types/double-data-type.md) type de données</span><span class="sxs-lookup"><span data-stu-id="5be8d-123">Either expression is a [Double](../../../visual-basic/language-reference/data-types/double-data-type.md) data type</span></span>|`Double`|  
  
 <span data-ttu-id="5be8d-124">Avant d’effectuer la division, toutes les expressions numériques intégrées sont élargies à `Double`.</span><span class="sxs-lookup"><span data-stu-id="5be8d-124">Before division is performed, any integral numeric expressions are widened to `Double`.</span></span> <span data-ttu-id="5be8d-125">Si vous affectez le résultat à un type intégral, Visual Basic essaie de convertir le résultat à partir de `Double` à ce type.</span><span class="sxs-lookup"><span data-stu-id="5be8d-125">If you assign the result to an integral data type, Visual Basic attempts to convert the result from `Double` to that type.</span></span> <span data-ttu-id="5be8d-126">Cela peut lever une exception si le résultat ne tient pas dans ce type.</span><span class="sxs-lookup"><span data-stu-id="5be8d-126">This can throw an exception if the result does not fit in that type.</span></span> <span data-ttu-id="5be8d-127">En particulier, consultez « Tentative de Division par zéro » sur cette page d’aide.</span><span class="sxs-lookup"><span data-stu-id="5be8d-127">In particular, see "Attempted Division by Zero" on this Help page.</span></span>  
  
 <span data-ttu-id="5be8d-128">Si `expression1` ou `expression2` prend la valeur [rien](../../../visual-basic/language-reference/nothing.md), il est considéré comme égal à zéro.</span><span class="sxs-lookup"><span data-stu-id="5be8d-128">If `expression1` or `expression2` evaluates to [Nothing](../../../visual-basic/language-reference/nothing.md), it is treated as zero.</span></span>  
  
## <a name="attempted-division-by-zero"></a><span data-ttu-id="5be8d-129">Tentative de Division par zéro</span><span class="sxs-lookup"><span data-stu-id="5be8d-129">Attempted Division by Zero</span></span>  
 <span data-ttu-id="5be8d-130">Si `expression2` correspond à zéro, le `/` opérateur se comporte différemment pour les types de données différents d’opérande.</span><span class="sxs-lookup"><span data-stu-id="5be8d-130">If `expression2` evaluates to zero, the `/` operator behaves differently for different operand data types.</span></span> <span data-ttu-id="5be8d-131">Le tableau suivant répertorie les comportements possibles.</span><span class="sxs-lookup"><span data-stu-id="5be8d-131">The following table shows the possible behaviors.</span></span>  
  
|<span data-ttu-id="5be8d-132">Types de données d’opérande</span><span class="sxs-lookup"><span data-stu-id="5be8d-132">Operand data types</span></span>|<span data-ttu-id="5be8d-133">Comportement si `expression2` est égal à zéro</span><span class="sxs-lookup"><span data-stu-id="5be8d-133">Behavior if `expression2` is zero</span></span>|  
|------------------------|---------------------------------------|  
|<span data-ttu-id="5be8d-134">À virgule flottante (`Single` ou `Double`)</span><span class="sxs-lookup"><span data-stu-id="5be8d-134">Floating-point (`Single` or `Double`)</span></span>|<span data-ttu-id="5be8d-135">Retourne l’infini (<xref:System.Double.PositiveInfinity> ou <xref:System.Double.NegativeInfinity>), ou <xref:System.Double.NaN> (pas un nombre) si `expression1` est également égal à zéro</span><span class="sxs-lookup"><span data-stu-id="5be8d-135">Returns infinity (<xref:System.Double.PositiveInfinity> or <xref:System.Double.NegativeInfinity>), or <xref:System.Double.NaN> (not a number) if `expression1` is also zero</span></span>|  
|`Decimal`|<span data-ttu-id="5be8d-136">Lève <xref:System.DivideByZeroException></span><span class="sxs-lookup"><span data-stu-id="5be8d-136">Throws <xref:System.DivideByZeroException></span></span>|  
|<span data-ttu-id="5be8d-137">Entier (signé ou non signé)</span><span class="sxs-lookup"><span data-stu-id="5be8d-137">Integral (signed or unsigned)</span></span>|<span data-ttu-id="5be8d-138">Tentative de conversion en type intégral lève <xref:System.OverflowException> , car les types intégraux ne peut pas accepter <xref:System.Double.PositiveInfinity>, <xref:System.Double.NegativeInfinity>, ou <xref:System.Double.NaN></span><span class="sxs-lookup"><span data-stu-id="5be8d-138">Attempted conversion back to integral type throws <xref:System.OverflowException> because integral types cannot accept <xref:System.Double.PositiveInfinity>, <xref:System.Double.NegativeInfinity>, or <xref:System.Double.NaN></span></span>|  
  
> [!NOTE]
>  <span data-ttu-id="5be8d-139">Le `/` opérateur peut être *surchargé*, ce qui signifie qu’une classe ou structure peut redéfinir son comportement lorsqu’un opérande a le type de cette classe ou structure.</span><span class="sxs-lookup"><span data-stu-id="5be8d-139">The `/` operator can be *overloaded*, which means that a class or structure can redefine its behavior when an operand has the type of that class or structure.</span></span> <span data-ttu-id="5be8d-140">Si votre code utilise cet opérateur sur une telle classe ou structure, veillez à ce que vous comprenez son comportement redéfini.</span><span class="sxs-lookup"><span data-stu-id="5be8d-140">If your code uses this operator on such a class or structure, be sure you understand its redefined behavior.</span></span> <span data-ttu-id="5be8d-141">Pour plus d'informations, consultez [Operator Procedures](../../../visual-basic/programming-guide/language-features/procedures/operator-procedures.md).</span><span class="sxs-lookup"><span data-stu-id="5be8d-141">For more information, see [Operator Procedures](../../../visual-basic/programming-guide/language-features/procedures/operator-procedures.md).</span></span>  
  
## <a name="example"></a><span data-ttu-id="5be8d-142">Exemple</span><span class="sxs-lookup"><span data-stu-id="5be8d-142">Example</span></span>  
 <span data-ttu-id="5be8d-143">Cet exemple utilise le `/` opérateur d’effectuer une division à virgule flottante.</span><span class="sxs-lookup"><span data-stu-id="5be8d-143">This example uses the `/` operator to perform floating-point division.</span></span> <span data-ttu-id="5be8d-144">Le résultat est le quotient de deux opérandes.</span><span class="sxs-lookup"><span data-stu-id="5be8d-144">The result is the quotient of the two operands.</span></span>  
  
 [!code-vb[VbVbalrOperators#16](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbalrOperators/VB/Class1.vb#16)]  
  
 <span data-ttu-id="5be8d-145">Les expressions dans l’exemple précédent retournent les valeurs 2,5 et 3,333333.</span><span class="sxs-lookup"><span data-stu-id="5be8d-145">The expressions in the preceding example return values of 2.5 and 3.333333.</span></span> <span data-ttu-id="5be8d-146">Notez que le résultat est toujours à virgule flottante (`Double`), même si les deux opérandes sont des constantes entières.</span><span class="sxs-lookup"><span data-stu-id="5be8d-146">Note that the result is always floating-point (`Double`), even though both operands are integer constants.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="5be8d-147">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="5be8d-147">See also</span></span>

- [<span data-ttu-id="5be8d-148">/ =, Opérateur (Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="5be8d-148">/= Operator (Visual Basic)</span></span>](../../../visual-basic/language-reference/operators/floating-point-division-assignment-operator.md)
- [<span data-ttu-id="5be8d-149">\, Opérateur (Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="5be8d-149">\ Operator (Visual Basic)</span></span>](../../../visual-basic/language-reference/operators/integer-division-operator.md)
- [<span data-ttu-id="5be8d-150">Types de données des résultats d’opérateur</span><span class="sxs-lookup"><span data-stu-id="5be8d-150">Data Types of Operator Results</span></span>](../../../visual-basic/language-reference/operators/data-types-of-operator-results.md)
- [<span data-ttu-id="5be8d-151">Opérateurs arithmétiques</span><span class="sxs-lookup"><span data-stu-id="5be8d-151">Arithmetic Operators</span></span>](../../../visual-basic/language-reference/operators/arithmetic-operators.md)
- [<span data-ttu-id="5be8d-152">Priorité des opérateurs en Visual Basic</span><span class="sxs-lookup"><span data-stu-id="5be8d-152">Operator Precedence in Visual Basic</span></span>](../../../visual-basic/language-reference/operators/operator-precedence.md)
- [<span data-ttu-id="5be8d-153">Opérateurs répertoriés par fonctionnalité</span><span class="sxs-lookup"><span data-stu-id="5be8d-153">Operators Listed by Functionality</span></span>](../../../visual-basic/language-reference/operators/operators-listed-by-functionality.md)
- [<span data-ttu-id="5be8d-154">Opérateurs arithmétiques en Visual Basic</span><span class="sxs-lookup"><span data-stu-id="5be8d-154">Arithmetic Operators in Visual Basic</span></span>](../../../visual-basic/programming-guide/language-features/operators-and-expressions/arithmetic-operators.md)
