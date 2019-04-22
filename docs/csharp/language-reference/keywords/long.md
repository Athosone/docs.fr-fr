---
title: long - Référence C#
ms.custom: seodec18
ms.date: 03/14/2017
f1_keywords:
- long_CSharpKeyword
- long
helpviewer_keywords:
- long keyword [C#]
ms.assetid: f9b24319-1f39-48be-a42b-d528ee28a7fd
ms.openlocfilehash: 997ce7399dc9742076932b213811abd1f847e60b
ms.sourcegitcommit: 438919211260bb415fc8f96ca3eabc33cf2d681d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/16/2019
ms.locfileid: "59613289"
---
# <a name="long-c-reference"></a><span data-ttu-id="59cb3-102">long (référence C#)</span><span class="sxs-lookup"><span data-stu-id="59cb3-102">long (C# Reference)</span></span>

<span data-ttu-id="59cb3-103">`long` désigne un type intégral qui stocke des valeurs en fonction de la taille et de la plage indiquées dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="59cb3-103">`long` denotes an integral type that stores values according to the size and range shown in the following table.</span></span>

|<span data-ttu-id="59cb3-104">Type</span><span class="sxs-lookup"><span data-stu-id="59cb3-104">Type</span></span>|<span data-ttu-id="59cb3-105">Plage</span><span class="sxs-lookup"><span data-stu-id="59cb3-105">Range</span></span>|<span data-ttu-id="59cb3-106">Size</span><span class="sxs-lookup"><span data-stu-id="59cb3-106">Size</span></span>|<span data-ttu-id="59cb3-107">Type .NET</span><span class="sxs-lookup"><span data-stu-id="59cb3-107">.NET type</span></span>|
|----------|-----------|----------|-------------------------|
|`long`|<span data-ttu-id="59cb3-108">-9 223 372 036 854 775 808 à 9 223 372 036 854 775 807</span><span class="sxs-lookup"><span data-stu-id="59cb3-108">-9,223,372,036,854,775,808 to 9,223,372,036,854,775,807</span></span>|<span data-ttu-id="59cb3-109">Entier 64 bits signé</span><span class="sxs-lookup"><span data-stu-id="59cb3-109">Signed 64-bit integer</span></span>|<xref:System.Int64?displayProperty=nameWithType>|

## <a name="literals"></a><span data-ttu-id="59cb3-110">Littéraux</span><span class="sxs-lookup"><span data-stu-id="59cb3-110">Literals</span></span>

<span data-ttu-id="59cb3-111">Vous pouvez déclarer et initialiser une variable `long` en lui assignant un littéral décimal, hexadécimal ou binaire (à compter de C# 7.0).</span><span class="sxs-lookup"><span data-stu-id="59cb3-111">You can declare and initialize a `long` variable by assigning a decimal literal, a hexadecimal literal, or (starting with C# 7.0) a binary literal to it.</span></span>

<span data-ttu-id="59cb3-112">Dans l’exemple suivant, les entiers égaux à 4 294 967 296 représentés comme des littéraux décimaux, hexadécimaux et binaires sont assignés aux valeurs `long`.</span><span class="sxs-lookup"><span data-stu-id="59cb3-112">In the following example, integers equal to 4,294,967,296 that are represented as decimal, hexadecimal, and binary literals are assigned to `long` values.</span></span>

[!code-csharp[long](../../../../samples/snippets/csharp/language-reference/keywords/numeric-literals.cs#Long)]

> [!NOTE]
> <span data-ttu-id="59cb3-113">Vous utilisez le préfixe `0x` ou `0X` pour désigner un littéral hexadécimal, et le préfixe `0b` ou `0B` pour désigner un littéral binaire.</span><span class="sxs-lookup"><span data-stu-id="59cb3-113">You use the prefix `0x` or `0X` to denote a hexadecimal literal and the prefix `0b` or `0B` to denote a binary literal.</span></span> <span data-ttu-id="59cb3-114">Les littéraux décimaux n’ont pas de préfixe.</span><span class="sxs-lookup"><span data-stu-id="59cb3-114">Decimal literals have no prefix.</span></span>

<span data-ttu-id="59cb3-115">À compter de C# 7.0, des fonctionnalités ont été ajoutées pour améliorer la lisibilité.</span><span class="sxs-lookup"><span data-stu-id="59cb3-115">Starting with C# 7.0, a couple of features have been added to enhance readability.</span></span>
- <span data-ttu-id="59cb3-116">C# 7.0 prend en charge l’utilisation du caractère de soulignement (`_`) comme séparateur numérique.</span><span class="sxs-lookup"><span data-stu-id="59cb3-116">C# 7.0 allows the usage of the underscore character, `_`, as a digit separator.</span></span>
- <span data-ttu-id="59cb3-117">C# 7.2 prend en charge l’utilisation de `_` comme séparateur de chiffres pour un littéral binaire ou hexadécimal, après le préfixe.</span><span class="sxs-lookup"><span data-stu-id="59cb3-117">C# 7.2 allows `_` to be used as a digit separator for a binary or hexadecimal literal, after the prefix.</span></span> <span data-ttu-id="59cb3-118">Un trait de soulignement n’est pas autorisé au début d’un littéral décimal.</span><span class="sxs-lookup"><span data-stu-id="59cb3-118">A decimal literal isn't permitted to have a leading underscore.</span></span>

<span data-ttu-id="59cb3-119">Voici quelques exemples.</span><span class="sxs-lookup"><span data-stu-id="59cb3-119">Some examples are shown below.</span></span>

[!code-csharp[long](../../../../samples/snippets/csharp/language-reference/keywords/numeric-literals.cs#LongS)]

<span data-ttu-id="59cb3-120">Les littéraux entiers peuvent également inclure un suffixe qui désigne le type.</span><span class="sxs-lookup"><span data-stu-id="59cb3-120">Integer literals can also include a suffix that denotes the type.</span></span> <span data-ttu-id="59cb3-121">Le suffixe `L` désigne un type `long`.</span><span class="sxs-lookup"><span data-stu-id="59cb3-121">The suffix `L` denotes a `long`.</span></span> <span data-ttu-id="59cb3-122">L’exemple suivant utilise le suffixe `L` pour désigner un entier long :</span><span class="sxs-lookup"><span data-stu-id="59cb3-122">The following example uses the `L` suffix to denote a long integer:</span></span>

```csharp
long value = 4294967296L;
```

> [!NOTE]
> <span data-ttu-id="59cb3-123">Vous pouvez aussi utiliser la lettre minuscule « l » comme suffixe.</span><span class="sxs-lookup"><span data-stu-id="59cb3-123">You can also use the lowercase letter "l" as a suffix.</span></span> <span data-ttu-id="59cb3-124">Ceci génère cependant un avertissement du compilateur, car la lettre « l » peut être facilement confondue avec le chiffre « 1 ».</span><span class="sxs-lookup"><span data-stu-id="59cb3-124">However, this generates a compiler warning because the letter "l" is easily confused with the digit "1."</span></span> <span data-ttu-id="59cb3-125">Utilisez « L » pour plus de clarté.</span><span class="sxs-lookup"><span data-stu-id="59cb3-125">Use "L" for clarity.</span></span>

<span data-ttu-id="59cb3-126">Quand vous utilisez le suffixe `L`, le type du littéral entier est déterminé comme étant `long` ou [ulong](../../../csharp/language-reference/keywords/ulong.md), en fonction de sa taille.</span><span class="sxs-lookup"><span data-stu-id="59cb3-126">When you use the suffix `L`, the type of the literal integer is determined to be either `long` or [ulong](../../../csharp/language-reference/keywords/ulong.md), depending on its size.</span></span> <span data-ttu-id="59cb3-127">Dans ce cas, le type est `long`, car le littéral est inférieur à la plage de [ulong](../../../csharp/language-reference/keywords/ulong.md).</span><span class="sxs-lookup"><span data-stu-id="59cb3-127">In this case, it is `long` because it less than the range of [ulong](../../../csharp/language-reference/keywords/ulong.md).</span></span>

<span data-ttu-id="59cb3-128">Le suffixe est souvent utilisé pour appeler des méthodes surchargées.</span><span class="sxs-lookup"><span data-stu-id="59cb3-128">A common use of the suffix is to call overloaded methods.</span></span> <span data-ttu-id="59cb3-129">Par exemple, les méthodes surchargées suivantes ont des paramètres de type `long` et [int](../../../csharp/language-reference/keywords/int.md) :</span><span class="sxs-lookup"><span data-stu-id="59cb3-129">For example, the following overloaded methods have parameters of type `long` and [int](../../../csharp/language-reference/keywords/int.md):</span></span>

```csharp
public static void SampleMethod(int i) {}
public static void SampleMethod(long l) {}
```

<span data-ttu-id="59cb3-130">Le suffixe `L` garantit que la surcharge appropriée est appelée :</span><span class="sxs-lookup"><span data-stu-id="59cb3-130">The `L` suffix guarantees that the correct overload is called:</span></span>

```csharp
SampleMethod(5);    // Calls the method with the int parameter
SampleMethod(5L);   // Calls the method with the long parameter
```

<span data-ttu-id="59cb3-131">Quand un littéral entier n’a pas de suffixe, son type est le premier des types suivants dans lesquels sa valeur peut être représentée :</span><span class="sxs-lookup"><span data-stu-id="59cb3-131">If an integer literal has no suffix, its type is the first of the following types in which its value can be represented:</span></span>

1. [<span data-ttu-id="59cb3-132">int</span><span class="sxs-lookup"><span data-stu-id="59cb3-132">int</span></span>](int.md)
2. [<span data-ttu-id="59cb3-133">uint</span><span class="sxs-lookup"><span data-stu-id="59cb3-133">uint</span></span>](../../../csharp/language-reference/keywords/uint.md)
3. `long`
4. [<span data-ttu-id="59cb3-134">ulong</span><span class="sxs-lookup"><span data-stu-id="59cb3-134">ulong</span></span>](../../../csharp/language-reference/keywords/ulong.md)

<span data-ttu-id="59cb3-135">Dans l’exemple précédent, le littéral 4294967296 est de type `long`, car il dépasse la plage de [uint](../../../csharp/language-reference/keywords/uint.md) (consultez le [Tableau des types intégraux](../../../csharp/language-reference/keywords/integral-types-table.md) pour les tailles de stockage des types intégraux).</span><span class="sxs-lookup"><span data-stu-id="59cb3-135">The literal 4294967296 in the previous examples is of type `long`, because it exceeds the range of [uint](../../../csharp/language-reference/keywords/uint.md) (see [Integral Types Table](../../../csharp/language-reference/keywords/integral-types-table.md) for the storage sizes of integral types).</span></span>

<span data-ttu-id="59cb3-136">Vous pouvez utiliser le type `long` avec d’autres types intégraux dans la même expression, l’expression est évaluée comme `long` (ou [bool](../../../csharp/language-reference/keywords/bool.md) dans le cas d’expressions relationnelles ou booléennes).</span><span class="sxs-lookup"><span data-stu-id="59cb3-136">If you use the `long` type with other integral types in the same expression, the expression is evaluated as `long` (or [bool](../../../csharp/language-reference/keywords/bool.md) in the case of relational or Boolean expressions).</span></span> <span data-ttu-id="59cb3-137">Par exemple, l’expression suivante s’évalue en `long` :</span><span class="sxs-lookup"><span data-stu-id="59cb3-137">For example, the following expression evaluates as `long`:</span></span>

```csharp
898L + 88
```

<span data-ttu-id="59cb3-138">Pour plus d’informations sur les expressions arithmétiques combinant des types virgule flottante et des types intégraux, consultez [float](../../../csharp/language-reference/keywords/float.md) et [double](../../../csharp/language-reference/keywords/double.md).</span><span class="sxs-lookup"><span data-stu-id="59cb3-138">For information on arithmetic expressions with mixed floating-point types and integral types, see [float](../../../csharp/language-reference/keywords/float.md) and [double](../../../csharp/language-reference/keywords/double.md).</span></span>

## <a name="conversions"></a><span data-ttu-id="59cb3-139">Conversions</span><span class="sxs-lookup"><span data-stu-id="59cb3-139">Conversions</span></span>

<span data-ttu-id="59cb3-140">Il existe une conversion implicite prédéfinie de `long` en [float](../../../csharp/language-reference/keywords/float.md), [double](../../../csharp/language-reference/keywords/double.md) ou [decimal](../../../csharp/language-reference/keywords/decimal.md).</span><span class="sxs-lookup"><span data-stu-id="59cb3-140">There is a predefined implicit conversion from `long` to [float](../../../csharp/language-reference/keywords/float.md), [double](../../../csharp/language-reference/keywords/double.md), or [decimal](../../../csharp/language-reference/keywords/decimal.md).</span></span> <span data-ttu-id="59cb3-141">Dans le cas contraire, vous devez utiliser un cast.</span><span class="sxs-lookup"><span data-stu-id="59cb3-141">Otherwise a cast must be used.</span></span> <span data-ttu-id="59cb3-142">Par exemple, l’instruction suivante génère une erreur de compilation sans un cast explicite :</span><span class="sxs-lookup"><span data-stu-id="59cb3-142">For example, the following statement will produce a compilation error without an explicit cast:</span></span>

```csharp
int x = 8L;        // Error: no implicit conversion from long to int
int y = (int)8L;   // OK: explicit conversion to int
```

<span data-ttu-id="59cb3-143">Il existe une conversion implicite prédéfinie de [sbyte](../../../csharp/language-reference/keywords/sbyte.md), [byte](../../../csharp/language-reference/keywords/byte.md), [short](../../../csharp/language-reference/keywords/short.md), [ushort](../../../csharp/language-reference/keywords/ushort.md), [int](../../../csharp/language-reference/keywords/int.md), [uint](../../../csharp/language-reference/keywords/uint.md) ou [char](../../../csharp/language-reference/keywords/char.md) vers `long`.</span><span class="sxs-lookup"><span data-stu-id="59cb3-143">There is a predefined implicit conversion from [sbyte](../../../csharp/language-reference/keywords/sbyte.md), [byte](../../../csharp/language-reference/keywords/byte.md), [short](../../../csharp/language-reference/keywords/short.md), [ushort](../../../csharp/language-reference/keywords/ushort.md), [int](../../../csharp/language-reference/keywords/int.md), [uint](../../../csharp/language-reference/keywords/uint.md), or [char](../../../csharp/language-reference/keywords/char.md) to `long`.</span></span>

<span data-ttu-id="59cb3-144">Notez aussi qu’il n’existe pas de conversion implicite des types virgule flottante vers `long`.</span><span class="sxs-lookup"><span data-stu-id="59cb3-144">Notice also that there is no implicit conversion from floating-point types to `long`.</span></span> <span data-ttu-id="59cb3-145">Par exemple, l’instruction suivante génère une erreur du compilateur, sauf si vous utilisez un cast explicite :</span><span class="sxs-lookup"><span data-stu-id="59cb3-145">For example, the following statement generates a compiler error unless an explicit cast is used:</span></span>

```csharp
long x = 3.0;         // Error: no implicit conversion from double
long y = (long)3.0;   // OK: explicit conversion
```

## <a name="c-language-specification"></a><span data-ttu-id="59cb3-146">Spécification du langage C#</span><span class="sxs-lookup"><span data-stu-id="59cb3-146">C# Language Specification</span></span>

<span data-ttu-id="59cb3-147">Pour plus d’informations, consultez [Types intégraux](~/_csharplang/spec/types.md#integral-types) dans la [spécification du langage C#](../language-specification/index.md).</span><span class="sxs-lookup"><span data-stu-id="59cb3-147">For more information, see [Integral types](~/_csharplang/spec/types.md#integral-types) in the [C# Language Specification](../language-specification/index.md).</span></span> <span data-ttu-id="59cb3-148">La spécification du langage est la source de référence pour la syntaxe C# et son utilisation.</span><span class="sxs-lookup"><span data-stu-id="59cb3-148">The language specification is the definitive source for C# syntax and usage.</span></span>

## <a name="see-also"></a><span data-ttu-id="59cb3-149">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="59cb3-149">See also</span></span>

- <xref:System.Int64>
- [<span data-ttu-id="59cb3-150">Référence C#</span><span class="sxs-lookup"><span data-stu-id="59cb3-150">C# Reference</span></span>](../../../csharp/language-reference/index.md)
- [<span data-ttu-id="59cb3-151">Guide de programmation C#</span><span class="sxs-lookup"><span data-stu-id="59cb3-151">C# Programming Guide</span></span>](../../../csharp/programming-guide/index.md)
- [<span data-ttu-id="59cb3-152">Mots clés C#</span><span class="sxs-lookup"><span data-stu-id="59cb3-152">C# Keywords</span></span>](../../../csharp/language-reference/keywords/index.md)
- [<span data-ttu-id="59cb3-153">Tableau des types intégraux</span><span class="sxs-lookup"><span data-stu-id="59cb3-153">Integral Types Table</span></span>](../../../csharp/language-reference/keywords/integral-types-table.md)
- [<span data-ttu-id="59cb3-154">Tableau des types intégrés</span><span class="sxs-lookup"><span data-stu-id="59cb3-154">Built-In Types Table</span></span>](../../../csharp/language-reference/keywords/built-in-types-table.md)
- [<span data-ttu-id="59cb3-155">Tableau des conversions numériques implicites</span><span class="sxs-lookup"><span data-stu-id="59cb3-155">Implicit Numeric Conversions Table</span></span>](../../../csharp/language-reference/keywords/implicit-numeric-conversions-table.md)
- [<span data-ttu-id="59cb3-156">Tableau des conversions numériques explicites</span><span class="sxs-lookup"><span data-stu-id="59cb3-156">Explicit Numeric Conversions Table</span></span>](../../../csharp/language-reference/keywords/explicit-numeric-conversions-table.md)
