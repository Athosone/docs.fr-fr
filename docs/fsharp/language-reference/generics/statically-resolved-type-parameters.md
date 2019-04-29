---
title: Paramètres de type résolus statiquement
description: Découvrez comment utiliser un F# paramètre de type résolus statiquement, qui est remplacé par un type réel au moment de la compilation plutôt qu’au moment de l’exécution.
ms.date: 05/16/2016
ms.openlocfilehash: 9ad23a881e644dfe2bccd56fa04d3c219b51cf7d
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61937486"
---
# <a name="statically-resolved-type-parameters"></a><span data-ttu-id="cb5f1-103">Paramètres de type résolus statiquement</span><span class="sxs-lookup"><span data-stu-id="cb5f1-103">Statically Resolved Type Parameters</span></span>

<span data-ttu-id="cb5f1-104">Un *paramètre de type résolus statiquement* est un paramètre de type est remplacé par un type réel au moment de la compilation plutôt qu’au moment de l’exécution.</span><span class="sxs-lookup"><span data-stu-id="cb5f1-104">A *statically resolved type parameter* is a type parameter that is replaced with an actual type at compile time instead of at run time.</span></span> <span data-ttu-id="cb5f1-105">Elles sont précédées d’un symbole de signe insertion (^).</span><span class="sxs-lookup"><span data-stu-id="cb5f1-105">They are preceded by a caret (^) symbol.</span></span>

## <a name="syntax"></a><span data-ttu-id="cb5f1-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="cb5f1-106">Syntax</span></span>

```
ˆtype-parameter
```

## <a name="remarks"></a><span data-ttu-id="cb5f1-107">Notes</span><span class="sxs-lookup"><span data-stu-id="cb5f1-107">Remarks</span></span>

<span data-ttu-id="cb5f1-108">Dans le F# langage, il existe deux types distincts de paramètres de type.</span><span class="sxs-lookup"><span data-stu-id="cb5f1-108">In the F# language, there are two distinct kinds of type parameters.</span></span> <span data-ttu-id="cb5f1-109">Le premier type est le paramètre de type générique standard.</span><span class="sxs-lookup"><span data-stu-id="cb5f1-109">The first kind is the standard generic type parameter.</span></span> <span data-ttu-id="cb5f1-110">Elles sont signalées par une apostrophe ('), comme dans `'T` et `'U`.</span><span class="sxs-lookup"><span data-stu-id="cb5f1-110">These are indicated by an apostrophe ('), as in `'T` and `'U`.</span></span> <span data-ttu-id="cb5f1-111">Ils sont équivalents aux paramètres de type générique dans d’autres langages .NET Framework.</span><span class="sxs-lookup"><span data-stu-id="cb5f1-111">They are equivalent to generic type parameters in other .NET Framework languages.</span></span> <span data-ttu-id="cb5f1-112">L’autre type est résolu statiquement et est indiqué par un symbole de signe insertion, comme dans `^T` et `^U`.</span><span class="sxs-lookup"><span data-stu-id="cb5f1-112">The other kind is statically resolved and is indicated by a caret symbol, as in `^T` and `^U`.</span></span>

<span data-ttu-id="cb5f1-113">Paramètres de type résolus statiquement sont principalement utiles conjointement avec les contraintes de membre, qui sont des contraintes qui vous permettent de spécifier qu’un argument de type doit avoir un membre particulier ou membres pour pouvoir être utilisé.</span><span class="sxs-lookup"><span data-stu-id="cb5f1-113">Statically resolved type parameters are primarily useful in conjunction with member constraints, which are constraints that allow you to specify that a type argument must have a particular member or members in order to be used.</span></span> <span data-ttu-id="cb5f1-114">Il n’existe aucun moyen de créer ce type de contrainte en utilisant un paramètre de type générique standard.</span><span class="sxs-lookup"><span data-stu-id="cb5f1-114">There is no way to create this kind of constraint by using a regular generic type parameter.</span></span>

<span data-ttu-id="cb5f1-115">Le tableau suivant résume les similitudes et les différences entre les deux types de paramètres de type.</span><span class="sxs-lookup"><span data-stu-id="cb5f1-115">The following table summarizes the similarities and differences between the two kinds of type parameters.</span></span>

|<span data-ttu-id="cb5f1-116">Fonctionnalité</span><span class="sxs-lookup"><span data-stu-id="cb5f1-116">Feature</span></span>|<span data-ttu-id="cb5f1-117">Generic</span><span class="sxs-lookup"><span data-stu-id="cb5f1-117">Generic</span></span>|<span data-ttu-id="cb5f1-118">Résolus statiquement</span><span class="sxs-lookup"><span data-stu-id="cb5f1-118">Statically resolved</span></span>|
|-------|-------|-------------------|
|<span data-ttu-id="cb5f1-119">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="cb5f1-119">Syntax</span></span>|<span data-ttu-id="cb5f1-120">`'T`, `'U`</span><span class="sxs-lookup"><span data-stu-id="cb5f1-120">`'T`, `'U`</span></span>|<span data-ttu-id="cb5f1-121">`^T`, `^U`</span><span class="sxs-lookup"><span data-stu-id="cb5f1-121">`^T`, `^U`</span></span>|
|<span data-ttu-id="cb5f1-122">Temps de résolution</span><span class="sxs-lookup"><span data-stu-id="cb5f1-122">Resolution time</span></span>|<span data-ttu-id="cb5f1-123">Au moment de l'exécution</span><span class="sxs-lookup"><span data-stu-id="cb5f1-123">Run time</span></span>|<span data-ttu-id="cb5f1-124">Temps de compilation</span><span class="sxs-lookup"><span data-stu-id="cb5f1-124">Compile time</span></span>|
|<span data-ttu-id="cb5f1-125">Contraintes de membre</span><span class="sxs-lookup"><span data-stu-id="cb5f1-125">Member constraints</span></span>|<span data-ttu-id="cb5f1-126">Ne peut pas être utilisé avec les contraintes de membre.</span><span class="sxs-lookup"><span data-stu-id="cb5f1-126">Cannot be used with member constraints.</span></span>|<span data-ttu-id="cb5f1-127">Peut être utilisé avec les contraintes de membre.</span><span class="sxs-lookup"><span data-stu-id="cb5f1-127">Can be used with member constraints.</span></span>|
|<span data-ttu-id="cb5f1-128">Génération de code</span><span class="sxs-lookup"><span data-stu-id="cb5f1-128">Code generation</span></span>|<span data-ttu-id="cb5f1-129">Un type (ou méthode) avec les paramètres de type générique standard entraîne la génération d’un type générique unique ou d’une méthode.</span><span class="sxs-lookup"><span data-stu-id="cb5f1-129">A type (or method) with standard generic type parameters results in the generation of a single generic type or method.</span></span>|<span data-ttu-id="cb5f1-130">Plusieurs instanciations de types et méthodes sont générées, un pour chaque type qui est nécessaire.</span><span class="sxs-lookup"><span data-stu-id="cb5f1-130">Multiple instantiations of types and methods are generated, one for each type that is needed.</span></span>|
|<span data-ttu-id="cb5f1-131">Utiliser avec des types</span><span class="sxs-lookup"><span data-stu-id="cb5f1-131">Use with types</span></span>|<span data-ttu-id="cb5f1-132">Peut être utilisé sur les types.</span><span class="sxs-lookup"><span data-stu-id="cb5f1-132">Can be used on types.</span></span>|<span data-ttu-id="cb5f1-133">Ne peut pas être utilisé sur les types.</span><span class="sxs-lookup"><span data-stu-id="cb5f1-133">Cannot be used on types.</span></span>|
|<span data-ttu-id="cb5f1-134">Utiliser avec les fonctions inline</span><span class="sxs-lookup"><span data-stu-id="cb5f1-134">Use with inline functions</span></span>|<span data-ttu-id="cb5f1-135">Non.</span><span class="sxs-lookup"><span data-stu-id="cb5f1-135">No.</span></span> <span data-ttu-id="cb5f1-136">Une fonction inline ne peut pas être paramétrée avec un paramètre de type générique standard.</span><span class="sxs-lookup"><span data-stu-id="cb5f1-136">An inline function cannot be parameterized with a standard generic type parameter.</span></span>|<span data-ttu-id="cb5f1-137">Oui.</span><span class="sxs-lookup"><span data-stu-id="cb5f1-137">Yes.</span></span> <span data-ttu-id="cb5f1-138">Paramètres de type résolus statiquement ne peut pas être utilisés sur les fonctions ou méthodes qui ne sont pas inline.</span><span class="sxs-lookup"><span data-stu-id="cb5f1-138">Statically resolved type parameters cannot be used on functions or methods that are not inline.</span></span>|

<span data-ttu-id="cb5f1-139">Nombreux F# fonctions de bibliothèque principales, notamment les opérateurs, ont résolus statiquement de paramètres de type.</span><span class="sxs-lookup"><span data-stu-id="cb5f1-139">Many F# core library functions, especially operators, have statically resolved type parameters.</span></span> <span data-ttu-id="cb5f1-140">Ces fonctions et opérateurs sont inline et entraînent la génération de code efficace pour effectuer des calculs numériques.</span><span class="sxs-lookup"><span data-stu-id="cb5f1-140">These functions and operators are inline, and result in efficient code generation for numeric computations.</span></span>

<span data-ttu-id="cb5f1-141">Méthodes inline et les fonctions qui utilisent des opérateurs, ou utilisent d’autres fonctions qui ont des paramètres de type résolus statiquement peuvent également utiliser les paramètres de type résolus statiquement proprement dits.</span><span class="sxs-lookup"><span data-stu-id="cb5f1-141">Inline methods and functions that use operators, or use other functions that have statically resolved type parameters, can also use statically resolved type parameters themselves.</span></span> <span data-ttu-id="cb5f1-142">Souvent, l’inférence de type déduit de ces fonctions inline ont des paramètres de type résolus statiquement.</span><span class="sxs-lookup"><span data-stu-id="cb5f1-142">Often, type inference infers such inline functions to have statically resolved type parameters.</span></span> <span data-ttu-id="cb5f1-143">L’exemple suivant illustre une définition d’opérateur qui est déduite pour avoir un paramètre de type résolus statiquement.</span><span class="sxs-lookup"><span data-stu-id="cb5f1-143">The following example illustrates an operator definition that is inferred to have a statically resolved type parameter.</span></span>

[!code-fsharp[Main](../../../../samples/snippets/fsharp/lang-ref-3/snippet401.fs)]

<span data-ttu-id="cb5f1-144">Le type résolu de `(+@)` repose sur l’utilisation des deux `(+)` et `(*)`, les deux qui amènent l’inférence de type déduire les contraintes de membre sur les paramètres de type résolus statiquement.</span><span class="sxs-lookup"><span data-stu-id="cb5f1-144">The resolved type of `(+@)` is based on the use of both `(+)` and `(*)`, both of which cause type inference to infer member constraints on the statically resolved type parameters.</span></span> <span data-ttu-id="cb5f1-145">Le type résolu, comme indiqué dans le F# interpréteur, se présente comme suit.</span><span class="sxs-lookup"><span data-stu-id="cb5f1-145">The resolved type, as shown in the F# interpreter, is as follows.</span></span>

```fsharp
^a -> ^c -> ^d
when (^a or ^b) : (static member ( + ) : ^a * ^b -> ^d) and
(^a or ^c) : (static member ( * ) : ^a * ^c -> ^b)
```

<span data-ttu-id="cb5f1-146">La sortie est la suivante.</span><span class="sxs-lookup"><span data-stu-id="cb5f1-146">The output is as follows.</span></span>

```
2
1.500000
```

<span data-ttu-id="cb5f1-147">En commençant par F# 4.1, vous pouvez également spécifier des noms de type concret dans les signatures de paramètres de type résolus statiquement.</span><span class="sxs-lookup"><span data-stu-id="cb5f1-147">Starting with F# 4.1, you can also specify concrete type names in statically resolved type parameter signatures.</span></span>  <span data-ttu-id="cb5f1-148">Dans les versions précédentes de la langue, le nom de type peut réellement être déduit par le compilateur, mais ne peut pas réellement spécifié dans la signature.</span><span class="sxs-lookup"><span data-stu-id="cb5f1-148">In previous versions of the language, the type name could actually be inferred by the compiler, but could not actually be specified in the signature.</span></span>  <span data-ttu-id="cb5f1-149">En tant que de F# 4.1, vous pouvez également spécifier des noms de type concret dans les signatures de paramètres de type résolus statiquement.</span><span class="sxs-lookup"><span data-stu-id="cb5f1-149">As of F# 4.1, you may also specify concrete type names in statically resolved type parameter signatures.</span></span> <span data-ttu-id="cb5f1-150">Voici un exemple :</span><span class="sxs-lookup"><span data-stu-id="cb5f1-150">Here's an example:</span></span>

```fsharp
let inline konst x _ = x

type CFunctor() = 
    static member inline fmap (f: ^a -> ^b, a: ^a list) = List.map f a
    static member inline fmap (f: ^a -> ^b, a: ^a option) =
        match a with
        | None -> None
        | Some x -> Some (f x)

    // default implementation of replace
    static member inline replace< ^a, ^b, ^c, ^d, ^e when ^a :> CFunctor and (^a or ^d): (static member fmap: (^b -> ^c) * ^d -> ^e) > (a, f) =
        ((^a or ^d) : (static member fmap : (^b -> ^c) * ^d -> ^e) (konst a, f))

    // call overridden replace if present
    static member inline replace< ^a, ^b, ^c when ^b: (static member replace: ^a * ^b -> ^c)>(a: ^a, f: ^b) =
        (^b : (static member replace: ^a * ^b -> ^c) (a, f))

let inline replace_instance< ^a, ^b, ^c, ^d when (^a or ^c): (static member replace: ^b * ^c -> ^d)> (a: ^b, f: ^c) =
        ((^a or ^c): (static member replace: ^b * ^c -> ^d) (a, f))

// Note the concrete type 'CFunctor' specified in the signature
let inline replace (a: ^a) (f: ^b): ^a0 when (CFunctor or  ^b): (static member replace: ^a *  ^b ->  ^a0) =
    replace_instance<CFunctor, _, _, _> (a, f)
```

## <a name="see-also"></a><span data-ttu-id="cb5f1-151">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="cb5f1-151">See also</span></span>

- [<span data-ttu-id="cb5f1-152">Génériques</span><span class="sxs-lookup"><span data-stu-id="cb5f1-152">Generics</span></span>](index.md)
- [<span data-ttu-id="cb5f1-153">Inférence de type</span><span class="sxs-lookup"><span data-stu-id="cb5f1-153">Type Inference</span></span>](../type-inference.md)
- [<span data-ttu-id="cb5f1-154">Généralisation automatique</span><span class="sxs-lookup"><span data-stu-id="cb5f1-154">Automatic Generalization</span></span>](automatic-generalization.md)
- [<span data-ttu-id="cb5f1-155">Contraintes</span><span class="sxs-lookup"><span data-stu-id="cb5f1-155">Constraints</span></span>](constraints.md)
- [<span data-ttu-id="cb5f1-156">Fonctions inline</span><span class="sxs-lookup"><span data-stu-id="cb5f1-156">Inline Functions</span></span>](../functions/inline-functions.md)