---
title: Le mot clé fixed
description: Découvrez comment vous pouvez « pin » une variable locale dans la pile pour éviter la collection avec le F# mot clé « fixed ».
ms.date: 04/24/2017
ms.openlocfilehash: 7fdf66560f3e2ab7584b00c7e4584d7f6c161858
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61772656"
---
# <a name="the-fixed-keyword"></a><span data-ttu-id="d389c-103">Le mot clé fixed</span><span class="sxs-lookup"><span data-stu-id="d389c-103">The fixed keyword</span></span>

<span data-ttu-id="d389c-104">F#4.1 introduit le `fixed` mot clé, qui vous permet de « épingler » une variable locale dans la pile pour éviter d’être collectées ou déplacé pendant le garbage collection.</span><span class="sxs-lookup"><span data-stu-id="d389c-104">F# 4.1 introduces the `fixed` keyword, which allows you to "pin" a local onto the stack to prevent it from being collected or moved during garbage-collection.</span></span>  <span data-ttu-id="d389c-105">Il est utilisé pour les scénarios de programmation de bas niveau.</span><span class="sxs-lookup"><span data-stu-id="d389c-105">It is used for low-level programming scenarios.</span></span>

## <a name="syntax"></a><span data-ttu-id="d389c-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="d389c-106">Syntax</span></span>

```fsharp
use ptr = fixed expression
```

## <a name="remarks"></a><span data-ttu-id="d389c-107">Notes</span><span class="sxs-lookup"><span data-stu-id="d389c-107">Remarks</span></span>

<span data-ttu-id="d389c-108">Cela permet d’étendre la syntaxe des expressions pour permettre l’extraction d’un pointeur et le lier à un nom qui ne peut pas être collectées ou déplacé pendant le garbage collection.</span><span class="sxs-lookup"><span data-stu-id="d389c-108">This extends the syntax of expressions to allow extracting a pointer and binding it to a name which is prevented from being collected or moved during garbage-collection.</span></span>  

<span data-ttu-id="d389c-109">Correction d’un pointeur à partir d’une expression via la `fixed` mot clé est lié à un identificateur via le `use` mot clé.</span><span class="sxs-lookup"><span data-stu-id="d389c-109">A pointer from an expression is fixed via the `fixed` keyword is bound to an identifier via the `use` keyword.</span></span>  <span data-ttu-id="d389c-110">La sémantique de cela est similaire à la gestion des ressources via les `use` mot clé.</span><span class="sxs-lookup"><span data-stu-id="d389c-110">The semantics of this are similar to resource management via the `use` keyword.</span></span>  <span data-ttu-id="d389c-111">Le pointeur est résolu pendant qu’il est dans la portée et une fois qu’il est hors de portée, il est fixe n’est plus.</span><span class="sxs-lookup"><span data-stu-id="d389c-111">The pointer is fixed while it is in scope, and once it is out of scope, it is no longer fixed.</span></span>  <span data-ttu-id="d389c-112">`fixed` ne peut pas être utilisé en dehors du contexte d’un `use` liaison.</span><span class="sxs-lookup"><span data-stu-id="d389c-112">`fixed` cannot be used outside the context of a `use` binding.</span></span>  <span data-ttu-id="d389c-113">Vous devez lier le pointeur à un nom avec `use`.</span><span class="sxs-lookup"><span data-stu-id="d389c-113">You must bind the pointer to a name with `use`.</span></span>

<span data-ttu-id="d389c-114">Utilisation de `fixed` doivent se produire dans une expression dans une fonction ou une méthode.</span><span class="sxs-lookup"><span data-stu-id="d389c-114">Use of `fixed` must occur within an expression in a function or a method.</span></span>  <span data-ttu-id="d389c-115">Il ne peut pas être utilisé dans une étendue au niveau du script ou au niveau du module.</span><span class="sxs-lookup"><span data-stu-id="d389c-115">It cannot be used at a script-level or module-level scope.</span></span>

<span data-ttu-id="d389c-116">Comme tout code de pointeur, cela est une fonctionnalité unsafe et émet un avertissement lorsqu’il est utilisé.</span><span class="sxs-lookup"><span data-stu-id="d389c-116">Like all pointer code, this is an unsafe feature and will emit a warning when used.</span></span>

## <a name="example"></a><span data-ttu-id="d389c-117">Exemple</span><span class="sxs-lookup"><span data-stu-id="d389c-117">Example</span></span>

```fsharp
open Microsoft.FSharp.NativeInterop

type Point = { mutable X: int; mutable Y: int}

let squareWithPointer (p: nativeptr<int>) =
    // Dereference the pointer at the 0th address.
    let mutable value = NativePtr.get p 0

    // Perform some work
    value <- value * value

    // Set the value in the pointer at the 0th address.
    NativePtr.set p 0 value

let pnt = { X = 1; Y = 2 }
printfn "pnt before - X: %d Y: %d" pnt.X pnt.Y // prints 1 and 2

// Note that the use of 'fixed' is inside a function.
// You cannot fix a pointer at a script-level or module-level scope.
let doPointerWork() =
    use ptr = fixed &pnt.Y

    // Square the Y value
    squareWithPointer ptr
    printfn "pnt after - X: %d Y: %d" pnt.X pnt.Y // prints 1 and 4

doPointerWork()
```

## <a name="see-also"></a><span data-ttu-id="d389c-118">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d389c-118">See also</span></span>

- [<span data-ttu-id="d389c-119">NativePtr (Module)</span><span class="sxs-lookup"><span data-stu-id="d389c-119">NativePtr Module</span></span>](https://msdn.microsoft.com/visualfsharpdocs/conceptual/nativeinterop.nativeptr-module-%5Bfsharp%5D)
