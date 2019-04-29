---
title: Variance dans les délégués (Visual Basic)
ms.date: 07/20/2015
ms.assetid: 38e9353f-74f8-4211-a8f0-7a495414df4a
ms.openlocfilehash: 6d341c7c2b5adeebcafc5b0787b132ab6bd57e41
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61787229"
---
# <a name="variance-in-delegates-visual-basic"></a><span data-ttu-id="bb6f1-102">Variance dans les délégués (Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="bb6f1-102">Variance in Delegates (Visual Basic)</span></span>

<span data-ttu-id="bb6f1-103">.NET framework 3.5 introduit la prise en charge de la variance pour faire correspondre les signatures de méthode aux types délégués dans tous les délégués dans C# et Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="bb6f1-103">.NET Framework 3.5 introduced variance support for matching method signatures with delegate types in all delegates in C# and Visual Basic.</span></span> <span data-ttu-id="bb6f1-104">Cela signifie que vous pouvez assigner aux délégués non seulement les méthodes ayant des signatures correspondantes, mais également des méthodes qui retournent des types plus dérivés (covariance) ou qui acceptent des paramètres ayant des types moins dérivés (contravariance) que ceux spécifiés par le type délégué.</span><span class="sxs-lookup"><span data-stu-id="bb6f1-104">This means that you can assign to delegates not only methods that have matching signatures, but also methods that return more derived types (covariance) or that accept parameters that have less derived types (contravariance) than that specified by the delegate type.</span></span> <span data-ttu-id="bb6f1-105">Cela inclut à la fois des délégués génériques et non génériques.</span><span class="sxs-lookup"><span data-stu-id="bb6f1-105">This includes both generic and non-generic delegates.</span></span>

<span data-ttu-id="bb6f1-106">Par exemple, considérez le code suivant, qui a deux classes et deux délégués : génériques et non génériques.</span><span class="sxs-lookup"><span data-stu-id="bb6f1-106">For example, consider the following code, which has two classes and two delegates: generic and non-generic.</span></span>

```vb
Public Class First
End Class

Public Class Second
    Inherits First
End Class

Public Delegate Function SampleDelegate(ByVal a As Second) As First
Public Delegate Function SampleGenericDelegate(Of A, R)(ByVal a As A) As R
```

<span data-ttu-id="bb6f1-107">Quand vous créez des délégués des types `SampleDelegate` ou `SampleDelegate(Of A, R)`, vous pouvez assigner l’une des méthodes suivantes à ces délégués.</span><span class="sxs-lookup"><span data-stu-id="bb6f1-107">When you create delegates of the `SampleDelegate` or `SampleDelegate(Of A, R)` types, you can assign any one of the following methods to those delegates.</span></span>

```vb
' Matching signature.
Public Shared Function ASecondRFirst(
    ByVal second As Second) As First
    Return New First()
End Function

' The return type is more derived.
Public Shared Function ASecondRSecond(
    ByVal second As Second) As Second
    Return New Second()
End Function

' The argument type is less derived.
Public Shared Function AFirstRFirst(
    ByVal first As First) As First
    Return New First()
End Function

' The return type is more derived
' and the argument type is less derived.
Public Shared Function AFirstRSecond(
    ByVal first As First) As Second
    Return New Second()
End Function
```

<span data-ttu-id="bb6f1-108">L’exemple de code suivant illustre la conversion implicite entre la signature de méthode et le type délégué.</span><span class="sxs-lookup"><span data-stu-id="bb6f1-108">The following code example illustrates the implicit conversion between the method signature and the delegate type.</span></span>

```vb
' Assigning a method with a matching signature
' to a non-generic delegate. No conversion is necessary.
Dim dNonGeneric As SampleDelegate = AddressOf ASecondRFirst
' Assigning a method with a more derived return type
' and less derived argument type to a non-generic delegate.
' The implicit conversion is used.
Dim dNonGenericConversion As SampleDelegate = AddressOf AFirstRSecond

' Assigning a method with a matching signature to a generic delegate.
' No conversion is necessary.
Dim dGeneric As SampleGenericDelegate(Of Second, First) = AddressOf ASecondRFirst
' Assigning a method with a more derived return type
' and less derived argument type to a generic delegate.
' The implicit conversion is used.
Dim dGenericConversion As SampleGenericDelegate(Of Second, First) = AddressOf AFirstRSecond
```

<span data-ttu-id="bb6f1-109">Pour plus d’exemples, consultez [à l’aide de la Variance dans les délégués (Visual Basic)](../../../../visual-basic/programming-guide/concepts/covariance-contravariance/using-variance-in-delegates.md) et [à l’aide de la Variance pour les délégués Func et Action générique (Visual Basic)](../../../../visual-basic/programming-guide/concepts/covariance-contravariance/using-variance-for-func-and-action-generic-delegates.md).</span><span class="sxs-lookup"><span data-stu-id="bb6f1-109">For more examples, see [Using Variance in Delegates (Visual Basic)](../../../../visual-basic/programming-guide/concepts/covariance-contravariance/using-variance-in-delegates.md) and [Using Variance for Func and Action Generic Delegates (Visual Basic)](../../../../visual-basic/programming-guide/concepts/covariance-contravariance/using-variance-for-func-and-action-generic-delegates.md).</span></span>

## <a name="variance-in-generic-type-parameters"></a><span data-ttu-id="bb6f1-110">Variance dans les paramètres de type générique</span><span class="sxs-lookup"><span data-stu-id="bb6f1-110">Variance in Generic Type Parameters</span></span>

<span data-ttu-id="bb6f1-111">Dans .NET Framework 4 et versions ultérieures vous pouvez activer la conversion implicite entre les délégués, afin que les délégués génériques ayant des types différents spécifiés par les paramètres de type générique puissent être assignés à l’autre, si les types sont hérités de l’autre comme requis par variance.</span><span class="sxs-lookup"><span data-stu-id="bb6f1-111">In .NET Framework 4 and later you can enable implicit conversion between delegates, so that generic delegates that have different types specified by generic type parameters can be assigned to each other, if the types are inherited from each other as required by variance.</span></span>

<span data-ttu-id="bb6f1-112">Pour activer la conversion implicite, vous devez déclarer explicitement les paramètres génériques dans un délégué comme covariant ou contravariant à l’aide du mot clé `in` ou `out`.</span><span class="sxs-lookup"><span data-stu-id="bb6f1-112">To enable implicit conversion, you must explicitly declare generic parameters in a delegate as covariant or contravariant by using the `in` or `out` keyword.</span></span>

<span data-ttu-id="bb6f1-113">L’exemple de code suivant indique comment vous pouvez créer un délégué ayant un paramètre de type générique covariant.</span><span class="sxs-lookup"><span data-stu-id="bb6f1-113">The following code example shows how you can create a delegate that has a covariant generic type parameter.</span></span>

```vb
' Type T is declared covariant by using the out keyword.
Public Delegate Function SampleGenericDelegate(Of Out T)() As T
Sub Test()
    Dim dString As SampleGenericDelegate(Of String) = Function() " "
    ' You can assign delegates to each other,
    ' because the type T is declared covariant.
    Dim dObject As SampleGenericDelegate(Of Object) = dString
End Sub
```

<span data-ttu-id="bb6f1-114">Si vous utilisez uniquement la prise en charge de la variance pour faire correspondre les signatures de méthode aux types délégués et que vous n’utilisez pas les mots clés `in` et `out`, vous pouvez réaliser qu’il est parfois possible d’instancier des délégués avec des expressions ou méthodes lambda identiques, mais que vous ne pouvez pas assigner un délégué à un autre.</span><span class="sxs-lookup"><span data-stu-id="bb6f1-114">If you use only variance support to match method signatures with delegate types and do not use the `in` and `out` keywords, you may find that sometimes you can instantiate delegates with identical lambda expressions or methods, but you cannot assign one delegate to another.</span></span>

<span data-ttu-id="bb6f1-115">Dans l’exemple de code suivant, `SampleGenericDelegate(Of String)` ne peut pas être converti explicitement en `SampleGenericDelegate(Of Object)`, bien que `String` hérite `Object`.</span><span class="sxs-lookup"><span data-stu-id="bb6f1-115">In the following code example, `SampleGenericDelegate(Of String)` can't be explicitly converted to `SampleGenericDelegate(Of Object)`, although `String` inherits `Object`.</span></span> <span data-ttu-id="bb6f1-116">Vous pouvez résoudre ce problème en marquant le paramètre générique `T` avec le mot clé `out`.</span><span class="sxs-lookup"><span data-stu-id="bb6f1-116">You can fix this problem by marking the generic parameter `T` with the `out` keyword.</span></span>

```vb
Public Delegate Function SampleGenericDelegate(Of T)() As T
Sub Test()
    Dim dString As SampleGenericDelegate(Of String) = Function() " "

    ' You can assign the dObject delegate
    ' to the same lambda expression as dString delegate
    ' because of the variance support for
    ' matching method signatures with delegate types.
    Dim dObject As SampleGenericDelegate(Of Object) = Function() " "

    ' The following statement generates a compiler error
    ' because the generic type T is not marked as covariant.
    ' Dim dObject As SampleGenericDelegate(Of Object) = dString

End Sub
```

### <a name="generic-delegates-that-have-variant-type-parameters-in-the-net-framework"></a><span data-ttu-id="bb6f1-117">Délégués génériques ayant des paramètres de type variant dans le .NET Framework</span><span class="sxs-lookup"><span data-stu-id="bb6f1-117">Generic Delegates That Have Variant Type Parameters in the .NET Framework</span></span>

<span data-ttu-id="bb6f1-118">.NET Framework 4 a introduit la prise en charge de la variance pour les paramètres de type générique dans plusieurs délégués génériques existants :</span><span class="sxs-lookup"><span data-stu-id="bb6f1-118">.NET Framework 4 introduced variance support for generic type parameters in several existing generic delegates:</span></span>

- <span data-ttu-id="bb6f1-119">Les délégués `Action` de l’espace de noms <xref:System>, par exemple, <xref:System.Action%601> et <xref:System.Action%602></span><span class="sxs-lookup"><span data-stu-id="bb6f1-119">`Action` delegates from the <xref:System> namespace, for example, <xref:System.Action%601> and <xref:System.Action%602></span></span>

- <span data-ttu-id="bb6f1-120">Les délégués `Func` de l’espace de noms <xref:System>, par exemple, <xref:System.Func%601> et <xref:System.Func%602></span><span class="sxs-lookup"><span data-stu-id="bb6f1-120">`Func` delegates from the <xref:System> namespace, for example, <xref:System.Func%601> and <xref:System.Func%602></span></span>

- <span data-ttu-id="bb6f1-121">Le délégué <xref:System.Predicate%601></span><span class="sxs-lookup"><span data-stu-id="bb6f1-121">The <xref:System.Predicate%601> delegate</span></span>

- <span data-ttu-id="bb6f1-122">Le délégué <xref:System.Comparison%601></span><span class="sxs-lookup"><span data-stu-id="bb6f1-122">The <xref:System.Comparison%601> delegate</span></span>

- <span data-ttu-id="bb6f1-123">Le délégué <xref:System.Converter%602></span><span class="sxs-lookup"><span data-stu-id="bb6f1-123">The <xref:System.Converter%602> delegate</span></span>

<span data-ttu-id="bb6f1-124">Pour plus d’informations et des exemples, consultez [à l’aide de la Variance pour les délégués Func et Action générique (Visual Basic)](../../../../visual-basic/programming-guide/concepts/covariance-contravariance/using-variance-for-func-and-action-generic-delegates.md).</span><span class="sxs-lookup"><span data-stu-id="bb6f1-124">For more information and examples, see [Using Variance for Func and Action Generic Delegates (Visual Basic)](../../../../visual-basic/programming-guide/concepts/covariance-contravariance/using-variance-for-func-and-action-generic-delegates.md).</span></span>

### <a name="declaring-variant-type-parameters-in-generic-delegates"></a><span data-ttu-id="bb6f1-125">Déclaration de paramètres de type variant dans les délégués génériques</span><span class="sxs-lookup"><span data-stu-id="bb6f1-125">Declaring Variant Type Parameters in Generic Delegates</span></span>

<span data-ttu-id="bb6f1-126">Si un délégué générique possède des paramètres de type générique covariant ou contravariant, il peut être désigné sous le nom de *délégué générique variant*.</span><span class="sxs-lookup"><span data-stu-id="bb6f1-126">If a generic delegate has covariant or contravariant generic type parameters, it can be referred to as a *variant generic delegate*.</span></span>

<span data-ttu-id="bb6f1-127">Vous pouvez déclarer un paramètre de type générique covariant dans un délégué générique à l’aide du mot clé `out`.</span><span class="sxs-lookup"><span data-stu-id="bb6f1-127">You can declare a generic type parameter covariant in a generic delegate by using the `out` keyword.</span></span> <span data-ttu-id="bb6f1-128">Le type covariant peut être utilisé uniquement comme type de retour de méthode et non comme type d’arguments de méthode.</span><span class="sxs-lookup"><span data-stu-id="bb6f1-128">The covariant type can be used only as a method return type and not as a type of method arguments.</span></span> <span data-ttu-id="bb6f1-129">L’exemple de code suivant indique comment déclarer un délégué générique covariant.</span><span class="sxs-lookup"><span data-stu-id="bb6f1-129">The following code example shows how to declare a covariant generic delegate.</span></span>

```vb
Public Delegate Function DCovariant(Of Out R)() As R
```

<span data-ttu-id="bb6f1-130">Vous pouvez déclarer un paramètre de type générique contravariant dans un délégué générique à l’aide du mot clé `in`.</span><span class="sxs-lookup"><span data-stu-id="bb6f1-130">You can declare a generic type parameter contravariant in a generic delegate by using the `in` keyword.</span></span> <span data-ttu-id="bb6f1-131">Le type contravariant peut être utilisé uniquement comme type d’arguments de méthode et non comme type de retour de méthode.</span><span class="sxs-lookup"><span data-stu-id="bb6f1-131">The contravariant type can be used only as a type of method arguments and not as a method return type.</span></span> <span data-ttu-id="bb6f1-132">L’exemple de code suivant indique comment déclarer un délégué générique contravariant.</span><span class="sxs-lookup"><span data-stu-id="bb6f1-132">The following code example shows how to declare a contravariant generic delegate.</span></span>

```vb
Public Delegate Sub DContravariant(Of In A)(ByVal a As A)
```

> [!IMPORTANT]
> <span data-ttu-id="bb6f1-133">`ByRef` paramètres en Visual Basic ne peut pas être marqués comme variants.</span><span class="sxs-lookup"><span data-stu-id="bb6f1-133">`ByRef` parameters in Visual Basic can't be marked as variant.</span></span>

<span data-ttu-id="bb6f1-134">Il est également possible de prendre en charge à la fois la variance et la covariance dans le même délégué, mais pour des paramètres de type différents.</span><span class="sxs-lookup"><span data-stu-id="bb6f1-134">It is also possible to support both variance and covariance in the same delegate, but for different type parameters.</span></span> <span data-ttu-id="bb6f1-135">L'exemple suivant le démontre.</span><span class="sxs-lookup"><span data-stu-id="bb6f1-135">This is shown in the following example.</span></span>

```vb
Public Delegate Function DVariant(Of In A, Out R)(ByVal a As A) As R
```

### <a name="instantiating-and-invoking-variant-generic-delegates"></a><span data-ttu-id="bb6f1-136">Instanciation et appel de délégués génériques variants</span><span class="sxs-lookup"><span data-stu-id="bb6f1-136">Instantiating and Invoking Variant Generic Delegates</span></span>

<span data-ttu-id="bb6f1-137">Vous pouvez instancier et appeler des délégués variants de la même façon que vous instanciez et appelez des délégués invariants.</span><span class="sxs-lookup"><span data-stu-id="bb6f1-137">You can instantiate and invoke variant delegates just as you instantiate and invoke invariant delegates.</span></span> <span data-ttu-id="bb6f1-138">Dans l’exemple suivant, le délégué est instancié par une expression lambda.</span><span class="sxs-lookup"><span data-stu-id="bb6f1-138">In the following example, the delegate is instantiated by a lambda expression.</span></span>

```vb
Dim dvariant As DVariant(Of String, String) = Function(str) str + " "
dvariant("test")
```

### <a name="combining-variant-generic-delegates"></a><span data-ttu-id="bb6f1-139">Combinaison des délégués génériques variants</span><span class="sxs-lookup"><span data-stu-id="bb6f1-139">Combining Variant Generic Delegates</span></span>

<span data-ttu-id="bb6f1-140">Vous ne devez pas combiner les délégués variants.</span><span class="sxs-lookup"><span data-stu-id="bb6f1-140">You should not combine variant delegates.</span></span> <span data-ttu-id="bb6f1-141">La méthode <xref:System.Delegate.Combine%2A> ne prend pas en charge la conversion des délégués variants et nécessite le même type pour tous les délégués.</span><span class="sxs-lookup"><span data-stu-id="bb6f1-141">The <xref:System.Delegate.Combine%2A> method does not support variant delegate conversion and expects delegates to be of exactly the same type.</span></span> <span data-ttu-id="bb6f1-142">Cela peut entraîner une exception au moment de l’exécution quand vous combinez les délégués en utilisant le <xref:System.Delegate.Combine%2A> (méthode) (dans C# et Visual Basic) ou à l’aide de la `+` opérateur (dans C#), comme illustré dans l’exemple de code suivant.</span><span class="sxs-lookup"><span data-stu-id="bb6f1-142">This can lead to a run-time exception when you combine delegates either by using the <xref:System.Delegate.Combine%2A> method (in C# and Visual Basic) or by using the `+` operator (in C#), as shown in the following code example.</span></span>

```vb
Dim actObj As Action(Of Object) = Sub(x) Console.WriteLine("object: {0}", x)
Dim actStr As Action(Of String) = Sub(x) Console.WriteLine("string: {0}", x)

' The following statement throws an exception at run time.
' Dim actCombine = [Delegate].Combine(actStr, actObj)
```

## <a name="variance-in-generic-type-parameters-for-value-and-reference-types"></a><span data-ttu-id="bb6f1-143">Variance dans les paramètres de type générique pour les types valeur et référence</span><span class="sxs-lookup"><span data-stu-id="bb6f1-143">Variance in Generic Type Parameters for Value and Reference Types</span></span>

<span data-ttu-id="bb6f1-144">La variance pour les paramètres de type générique est prise en charge uniquement pour les types référence.</span><span class="sxs-lookup"><span data-stu-id="bb6f1-144">Variance for generic type parameters is supported for reference types only.</span></span> <span data-ttu-id="bb6f1-145">Par exemple, `DVariant(Of Int)`ne peut pas être converti implicitement en `DVariant(Of Object)` ou `DVariant(Of Long)`, car entier est un type valeur.</span><span class="sxs-lookup"><span data-stu-id="bb6f1-145">For example, `DVariant(Of Int)`can't be implicitly converted to `DVariant(Of Object)` or `DVariant(Of Long)`, because integer is a value type.</span></span>

<span data-ttu-id="bb6f1-146">L’exemple suivant montre que la variance dans les paramètres de type générique n’est pas prise en charge pour les types valeur.</span><span class="sxs-lookup"><span data-stu-id="bb6f1-146">The following example demonstrates that variance in generic type parameters is not supported for value types.</span></span>

```vb
' The type T is covariant.
Public Delegate Function DVariant(Of Out T)() As T
' The type T is invariant.
Public Delegate Function DInvariant(Of T)() As T
Sub Test()
    Dim i As Integer = 0
    Dim dInt As DInvariant(Of Integer) = Function() i
    Dim dVariantInt As DVariant(Of Integer) = Function() i

    ' All of the following statements generate a compiler error
    ' because type variance in generic parameters is not supported
    ' for value types, even if generic type parameters are declared variant.
    ' Dim dObject As DInvariant(Of Object) = dInt
    ' Dim dLong As DInvariant(Of Long) = dInt
    ' Dim dVariantObject As DInvariant(Of Object) = dInt
    ' Dim dVariantLong As DInvariant(Of Long) = dInt
End Sub
```

## <a name="relaxed-delegate-conversion-in-visual-basic"></a><span data-ttu-id="bb6f1-147">Conversion simplifiée des délégués en Visual Basic</span><span class="sxs-lookup"><span data-stu-id="bb6f1-147">Relaxed Delegate Conversion in Visual Basic</span></span>

<span data-ttu-id="bb6f1-148">Conversion simplifiée des délégués permet plus de souplesse pour faire correspondre les signatures de méthode aux types délégués.</span><span class="sxs-lookup"><span data-stu-id="bb6f1-148">Relaxed delegate conversion enables more flexibility in matching method signatures with delegate types.</span></span> <span data-ttu-id="bb6f1-149">Par exemple, il vous permet d’omettre des spécifications de paramètre et omettez les valeurs de retour de fonction lorsque vous assignez une méthode à un délégué.</span><span class="sxs-lookup"><span data-stu-id="bb6f1-149">For example, it lets you omit parameter specifications and omit function return values when you assign a method to a delegate.</span></span> <span data-ttu-id="bb6f1-150">Pour plus d’informations, consultez [Conversion souple des délégués](../../../../visual-basic/programming-guide/language-features/delegates/relaxed-delegate-conversion.md).</span><span class="sxs-lookup"><span data-stu-id="bb6f1-150">For more information, see [Relaxed Delegate Conversion](../../../../visual-basic/programming-guide/language-features/delegates/relaxed-delegate-conversion.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="bb6f1-151">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="bb6f1-151">See also</span></span>

- [<span data-ttu-id="bb6f1-152">Génériques</span><span class="sxs-lookup"><span data-stu-id="bb6f1-152">Generics</span></span>](~/docs/standard/generics/index.md)
- [<span data-ttu-id="bb6f1-153">Utilisation de la variance pour les délégués génériques Func et Action (Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="bb6f1-153">Using Variance for Func and Action Generic Delegates (Visual Basic)</span></span>](../../../../visual-basic/programming-guide/concepts/covariance-contravariance/using-variance-for-func-and-action-generic-delegates.md)
