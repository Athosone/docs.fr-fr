---
title: Caractères de type (Visual Basic)
ms.date: 01/31/2018
helpviewer_keywords:
- '&H prefix for hexadecimal values'
- hexadecimal literals [Visual Basic]
- F literal type character [Visual Basic]
- '& identifier type character'
- type characters [Visual Basic]
- octal literals [Visual Basic]
- literals [Visual Basic], hexadecimal
- '&O prefix for octal values'
- literals [Visual Basic], default types
- defaults, literal types
- C literal type character [Visual Basic]
- type characters [Visual Basic], literal
- $ identifier type character
- L literal type character [Visual Basic]
- UI literal type characters [Visual Basic]
- default literal types [Visual Basic]
- D literal type character [Visual Basic]
- literals [Visual Basic], octal
- S literal type character [Visual Basic]
- '! identifier type character'
- US literal type characters [Visual Basic]
- '% identifier type character'
- data types [Visual Basic], type characters
- characters [Visual Basic], identifier type
- type characters [Visual Basic], identifier
- '# identifier type character'
- identifier type characters [Visual Basic]
- literal type characters [Visual Basic]
- I literal type character [Visual Basic]
- R literal type character [Visual Basic]
- '@ identifier type character'
- UL literal type characters [Visual Basic]
- literal types [Visual Basic], default
ms.assetid: 6353cb9b-6ee4-4af6-a5a8-88ce39f90cc5
ms.openlocfilehash: a469a08ebadd77d5abbfa95b270784c9ef534691
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61906748"
---
# <a name="type-characters-visual-basic"></a><span data-ttu-id="b6360-102">Tapez les caractères (Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="b6360-102">Type characters (Visual Basic)</span></span>

<span data-ttu-id="b6360-103">Outre la spécification d’un type de données dans une instruction de déclaration, vous pouvez forcer le type de données de certains éléments de programmation avec un *caractère de type*.</span><span class="sxs-lookup"><span data-stu-id="b6360-103">In addition to specifying a data type in a declaration statement, you can force the data type of some programming elements with a *type character*.</span></span> <span data-ttu-id="b6360-104">Le caractère de type doit suivre immédiatement l’élément, sans caractères intermédiaire d’aucune sorte.</span><span class="sxs-lookup"><span data-stu-id="b6360-104">The type character must immediately follow the element, with no intervening characters of any kind.</span></span>

<span data-ttu-id="b6360-105">Le caractère de type ne fait pas partie du nom de l’élément.</span><span class="sxs-lookup"><span data-stu-id="b6360-105">The type character is not part of the name of the element.</span></span> <span data-ttu-id="b6360-106">Un élément défini avec un caractère de type peut être référencé sans le caractère de type.</span><span class="sxs-lookup"><span data-stu-id="b6360-106">An element defined with a type character can be referenced without the type character.</span></span>

## <a name="identifier-type-characters"></a><span data-ttu-id="b6360-107">Caractères de type d’identificateur</span><span class="sxs-lookup"><span data-stu-id="b6360-107">Identifier type characters</span></span>

<span data-ttu-id="b6360-108">Visual Basic fournit un jeu de *caractères de type identificateur* que vous pouvez utiliser dans une déclaration pour spécifier le type de données d’une variable ou une constante.</span><span class="sxs-lookup"><span data-stu-id="b6360-108">Visual Basic supplies a set of *identifier type characters* that you can use in a declaration to specify the data type of a variable or constant.</span></span> <span data-ttu-id="b6360-109">Le tableau suivant présente les caractères de type identificateur disponible avec des exemples d’utilisation.</span><span class="sxs-lookup"><span data-stu-id="b6360-109">The following table shows the available identifier type characters with examples of usage.</span></span>
  
|<span data-ttu-id="b6360-110">Caractère de type identificateur</span><span class="sxs-lookup"><span data-stu-id="b6360-110">Identifier type character</span></span>|<span data-ttu-id="b6360-111">Type de données</span><span class="sxs-lookup"><span data-stu-id="b6360-111">Data type</span></span>|<span data-ttu-id="b6360-112">Exemple</span><span class="sxs-lookup"><span data-stu-id="b6360-112">Example</span></span>|  
|-------------------------------|---------------|-------------|  
|`%`|`Integer`|`Dim L%`|  
|`&`|`Long`|`Dim M&`|  
|`@`|`Decimal`|`Const W@ = 37.5`|  
|`!`|`Single`|`Dim Q!`|  
|`#`|`Double`|`Dim X#`|  
|`$`|`String`|`Dim V$ = "Secret"`|  
  
 <span data-ttu-id="b6360-113">Il n’existe aucun caractère de type d’identificateur pour le `Boolean`, `Byte`, `Char`, `Date`, `Object`, `SByte`, `Short`, `UInteger`, `ULong`, ou `UShort` des types de données, ou pour tout types de données composites tels que les tableaux ou les structures.</span><span class="sxs-lookup"><span data-stu-id="b6360-113">No identifier type characters exist for the `Boolean`, `Byte`, `Char`, `Date`, `Object`, `SByte`, `Short`, `UInteger`, `ULong`, or `UShort` data types, or for any composite data types such as arrays or structures.</span></span>

<span data-ttu-id="b6360-114">Dans certains cas, vous pouvez ajouter la `$` de caractères à une fonction Visual Basic, par exemple `Left$` au lieu de `Left`, afin d’obtenir une valeur retournée de type `String`.</span><span class="sxs-lookup"><span data-stu-id="b6360-114">In some cases, you can append the `$` character to a Visual Basic function, for example `Left$` instead of `Left`, to obtain a returned value of type `String`.</span></span>

<span data-ttu-id="b6360-115">Dans tous les cas, le caractère de type identificateur doit suivre immédiatement le nom d’identificateur.</span><span class="sxs-lookup"><span data-stu-id="b6360-115">In all cases, the identifier type character must immediately follow the identifier name.</span></span>

## <a name="literal-type-characters"></a><span data-ttu-id="b6360-116">Caractères de type littéral</span><span class="sxs-lookup"><span data-stu-id="b6360-116">Literal type characters</span></span>

<span data-ttu-id="b6360-117">Un *littéral* est une représentation textuelle d’une valeur particulière d’un type de données.</span><span class="sxs-lookup"><span data-stu-id="b6360-117">A *literal* is a textual representation of a particular value of a data type.</span></span>  

### <a name="default-literal-types"></a><span data-ttu-id="b6360-118">Types de littéral par défaut</span><span class="sxs-lookup"><span data-stu-id="b6360-118">Default literal types</span></span>

<span data-ttu-id="b6360-119">La forme d’un littéral, tel qu’il apparaît dans votre code ordinaire détermine son type de données.</span><span class="sxs-lookup"><span data-stu-id="b6360-119">The form of a literal as it appears in your code ordinarily determines its data type.</span></span> <span data-ttu-id="b6360-120">Le tableau suivant présente les types par défaut.</span><span class="sxs-lookup"><span data-stu-id="b6360-120">The following table shows these default types.</span></span>  
  
|<span data-ttu-id="b6360-121">Forme textuelle de littéral</span><span class="sxs-lookup"><span data-stu-id="b6360-121">Textual form of literal</span></span>|<span data-ttu-id="b6360-122">Type de données par défaut</span><span class="sxs-lookup"><span data-stu-id="b6360-122">Default data type</span></span>|<span data-ttu-id="b6360-123">Exemple</span><span class="sxs-lookup"><span data-stu-id="b6360-123">Example</span></span>|  
|-----------------------------|-----------------------|-------------|  
|<span data-ttu-id="b6360-124">Numérique, aucune partie fractionnaire</span><span class="sxs-lookup"><span data-stu-id="b6360-124">Numeric, no fractional part</span></span>|`Integer`|`2147483647`|  
|<span data-ttu-id="b6360-125">Numérique, aucune partie fractionnaire, trop grand pour `Integer`</span><span class="sxs-lookup"><span data-stu-id="b6360-125">Numeric, no fractional part, too large for `Integer`</span></span>|`Long`|`2147483648`|  
|<span data-ttu-id="b6360-126">Numérique, partie fractionnaire</span><span class="sxs-lookup"><span data-stu-id="b6360-126">Numeric, fractional part</span></span>|`Double`|`1.2`|  
|<span data-ttu-id="b6360-127">Entourée de guillemets doubles</span><span class="sxs-lookup"><span data-stu-id="b6360-127">Enclosed in double quotation marks</span></span>|`String`|`"A"`|  
|<span data-ttu-id="b6360-128">Encadrée des signes dièse</span><span class="sxs-lookup"><span data-stu-id="b6360-128">Enclosed within number signs</span></span>|`Date`|`#5/17/1993 9:32 AM#`|  

### <a name="forced-literal-types"></a><span data-ttu-id="b6360-129">Types de littéral forcés</span><span class="sxs-lookup"><span data-stu-id="b6360-129">Forced literal types</span></span>

<span data-ttu-id="b6360-130">Visual Basic fournit un jeu de *caractères de type littéral*, que vous pouvez utiliser pour forcer un littéral à prendre un type de données autre que celui de son formulaire indique.</span><span class="sxs-lookup"><span data-stu-id="b6360-130">Visual Basic supplies a set of *literal type characters*, which you can use to force a literal to assume a data type other than the one its form indicates.</span></span> <span data-ttu-id="b6360-131">Pour cela, vous devez l’ajout du caractère à la fin du littéral.</span><span class="sxs-lookup"><span data-stu-id="b6360-131">You do this by appending the character to the end of the literal.</span></span> <span data-ttu-id="b6360-132">Le tableau suivant présente les caractères de type de littéral disponibles avec des exemples d’utilisation.</span><span class="sxs-lookup"><span data-stu-id="b6360-132">The following table shows the available literal type characters with examples of usage.</span></span>
  
|<span data-ttu-id="b6360-133">Caractère de type littéral</span><span class="sxs-lookup"><span data-stu-id="b6360-133">Literal type character</span></span>|<span data-ttu-id="b6360-134">Type de données</span><span class="sxs-lookup"><span data-stu-id="b6360-134">Data type</span></span>|<span data-ttu-id="b6360-135">Exemple</span><span class="sxs-lookup"><span data-stu-id="b6360-135">Example</span></span>|  
|----------------------------|---------------|-------------|  
|`S`|`Short`|`I = 347S`|
|`I`|`Integer`|`J = 347I`|
|`L`|`Long`|`K = 347L`|
|`D`|`Decimal`|`X = 347D`|
|`F`|`Single`|`Y = 347F`|
|`R`|`Double`|`Z = 347R`|
|`US`|`UShort`|`L = 347US`|
|`UI`|`UInteger`|`M = 347UI`|
|`UL`|`ULong`|`N = 347UL`|
|`C`|`Char`|`Q = "."C`|

<span data-ttu-id="b6360-136">Il n’existe aucun caractère de type littéral pour le `Boolean`, `Byte`, `Date`, `Object`, `SByte`, ou `String` des types de données, ni pour les types de données composites tels que les tableaux ou les structures.</span><span class="sxs-lookup"><span data-stu-id="b6360-136">No literal type characters exist for the `Boolean`, `Byte`, `Date`, `Object`, `SByte`, or `String` data types, or for any composite data types such as arrays or structures.</span></span>

<span data-ttu-id="b6360-137">Les littéraux peuvent également utiliser les caractères de type identificateur (`%`, `&`, `@`, `!`, `#`, `$`), comme vous peuvent les variables, constantes et expressions.</span><span class="sxs-lookup"><span data-stu-id="b6360-137">Literals can also use the identifier type characters (`%`, `&`, `@`, `!`, `#`, `$`), as can variables, constants, and expressions.</span></span> <span data-ttu-id="b6360-138">Toutefois, les caractères de type de littéral (`S`, `I`, `L`, `D`, `F`, `R`, `C`) peut être utilisé uniquement avec des littéraux.</span><span class="sxs-lookup"><span data-stu-id="b6360-138">However, the literal type characters (`S`, `I`, `L`, `D`, `F`, `R`, `C`) can be used only with literals.</span></span>

<span data-ttu-id="b6360-139">Dans tous les cas, le caractère de type de littéral doit suivre immédiatement la valeur littérale.</span><span class="sxs-lookup"><span data-stu-id="b6360-139">In all cases, the literal type character must immediately follow the literal value.</span></span>

## <a name="hexadecimal-binary-and-octal-literals"></a><span data-ttu-id="b6360-140">Littéraux hexadécimaux, binaires et octaux</span><span class="sxs-lookup"><span data-stu-id="b6360-140">Hexadecimal, binary, and octal literals</span></span>

<span data-ttu-id="b6360-141">Le compilateur interprète normalement un littéral d’entier pour être dans le système de nombre décimal (base 10).</span><span class="sxs-lookup"><span data-stu-id="b6360-141">The compiler normally interprets an integer literal to be in the decimal (base 10) number system.</span></span> <span data-ttu-id="b6360-142">Vous pouvez également définir un littéral d’entier comme un nombre hexadécimal (base 16) avec le `&H` préfixe, sous la forme d’un nombre binaire (base 2) avec le `&B` préfixe et comme octal (base 8) nombre avec la `&O` préfixe.</span><span class="sxs-lookup"><span data-stu-id="b6360-142">You can also define an integer literal as a hexadecimal (base 16) number with the `&H` prefix, as a binary (base 2) number with the `&B` prefix, and as an octal (base 8) number with the `&O` prefix.</span></span> <span data-ttu-id="b6360-143">Les chiffres qui suivent le préfixe doivent être adaptées pour le système.</span><span class="sxs-lookup"><span data-stu-id="b6360-143">The digits that follow the prefix must be appropriate for the number system.</span></span> <span data-ttu-id="b6360-144">Le tableau suivant illustre cela.</span><span class="sxs-lookup"><span data-stu-id="b6360-144">The following table illustrates this.</span></span>  
  
|<span data-ttu-id="b6360-145">Base numérique</span><span class="sxs-lookup"><span data-stu-id="b6360-145">Number base</span></span>|<span data-ttu-id="b6360-146">Préfixe</span><span class="sxs-lookup"><span data-stu-id="b6360-146">Prefix</span></span>|<span data-ttu-id="b6360-147">Valeurs de chiffre valide</span><span class="sxs-lookup"><span data-stu-id="b6360-147">Valid digit values</span></span>|<span data-ttu-id="b6360-148">Exemple</span><span class="sxs-lookup"><span data-stu-id="b6360-148">Example</span></span>|
|-----------------|------------|------------------------|-------------|
|<span data-ttu-id="b6360-149">Hexadécimale (base 16)</span><span class="sxs-lookup"><span data-stu-id="b6360-149">Hexadecimal (base 16)</span></span>|`&H`|<span data-ttu-id="b6360-150">0-9 et A-F</span><span class="sxs-lookup"><span data-stu-id="b6360-150">0-9 and A-F</span></span>|`&HFFFF`|
|<span data-ttu-id="b6360-151">Binaire (base 2)</span><span class="sxs-lookup"><span data-stu-id="b6360-151">Binary (base 2)</span></span>|`&B`|<span data-ttu-id="b6360-152">0-1</span><span class="sxs-lookup"><span data-stu-id="b6360-152">0-1</span></span>|`&B01111100`|
|<span data-ttu-id="b6360-153">Octale (base 8)</span><span class="sxs-lookup"><span data-stu-id="b6360-153">Octal (base 8)</span></span>|`&O`|<span data-ttu-id="b6360-154">0-7</span><span class="sxs-lookup"><span data-stu-id="b6360-154">0-7</span></span>|`&O77`|

<span data-ttu-id="b6360-155">À partir de Visual Basic 2017, vous pouvez utiliser le caractère de soulignement (`_`) comme séparateur de groupes pour améliorer la lisibilité d’un littéral intégral.</span><span class="sxs-lookup"><span data-stu-id="b6360-155">Starting in Visual Basic 2017, you can use the underscore character (`_`) as a group separator to enhance the readability of an integral literal.</span></span> <span data-ttu-id="b6360-156">L’exemple suivant utilise le `_` caractère à regrouper un littéral binaire dans les groupes de 8 bits :</span><span class="sxs-lookup"><span data-stu-id="b6360-156">The following example uses the `_` character to group a binary literal into 8-bit groups:</span></span>

```vb
Dim number As Integer = &B00100010_11000101_11001111_11001101
```

<span data-ttu-id="b6360-157">Vous pouvez suivre un littéral préfixé avec un caractère de type littéral.</span><span class="sxs-lookup"><span data-stu-id="b6360-157">You can follow a prefixed literal with a literal type character.</span></span> <span data-ttu-id="b6360-158">L’exemple suivant illustre cela.</span><span class="sxs-lookup"><span data-stu-id="b6360-158">The following example shows this.</span></span>

```vb
Dim counter As Short = &H8000S
Dim flags As UShort = &H8000US
```

<span data-ttu-id="b6360-159">Dans l’exemple précédent, `counter` a la valeur décimale-32 768 et `flags` a la valeur décimale + 32 768.</span><span class="sxs-lookup"><span data-stu-id="b6360-159">In the previous example, `counter` has the decimal value of -32768, and `flags` has the decimal value of +32768.</span></span>

<span data-ttu-id="b6360-160">À partir de Visual Basic 15.5, vous pouvez également utiliser le caractère de soulignement (`_`) comme séparateur de début entre le préfixe et les chiffres hexadécimaux, binaires ou octaux.</span><span class="sxs-lookup"><span data-stu-id="b6360-160">Starting with Visual Basic 15.5, you can also use the underscore character (`_`) as a leading separator between the prefix and the hexadecimal, binary, or octal digits.</span></span> <span data-ttu-id="b6360-161">Exemple :</span><span class="sxs-lookup"><span data-stu-id="b6360-161">For example:</span></span>

```vb
Dim number As Integer = &H_C305_F860
```

[!INCLUDE [supporting-underscores](../../../../../includes/vb-separator-langversion.md)]

## <a name="see-also"></a><span data-ttu-id="b6360-162">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b6360-162">See also</span></span>

- [<span data-ttu-id="b6360-163">Types de données</span><span class="sxs-lookup"><span data-stu-id="b6360-163">Data Types</span></span>](../../../../visual-basic/programming-guide/language-features/data-types/index.md)
- [<span data-ttu-id="b6360-164">Types de données élémentaires</span><span class="sxs-lookup"><span data-stu-id="b6360-164">Elementary Data Types</span></span>](../../../../visual-basic/programming-guide/language-features/data-types/elementary-data-types.md)
- [<span data-ttu-id="b6360-165">Value Types and Reference Types</span><span class="sxs-lookup"><span data-stu-id="b6360-165">Value Types and Reference Types</span></span>](../../../../visual-basic/programming-guide/language-features/data-types/value-types-and-reference-types.md)
- [<span data-ttu-id="b6360-166">Conversions de type en Visual Basic</span><span class="sxs-lookup"><span data-stu-id="b6360-166">Type Conversions in Visual Basic</span></span>](../../../../visual-basic/programming-guide/language-features/data-types/type-conversions.md)
- [<span data-ttu-id="b6360-167">Dépannage des types de données</span><span class="sxs-lookup"><span data-stu-id="b6360-167">Troubleshooting Data Types</span></span>](../../../../visual-basic/programming-guide/language-features/data-types/troubleshooting-data-types.md)
- [<span data-ttu-id="b6360-168">Déclaration de variable</span><span class="sxs-lookup"><span data-stu-id="b6360-168">Variable Declaration</span></span>](../../../../visual-basic/programming-guide/language-features/variables/variable-declaration.md)
- [<span data-ttu-id="b6360-169">Types de données</span><span class="sxs-lookup"><span data-stu-id="b6360-169">Data Types</span></span>](../../../../visual-basic/language-reference/data-types/index.md)
