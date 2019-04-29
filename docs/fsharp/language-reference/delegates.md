---
title: Délégués
description: Découvrez comment utiliser des délégués F#.
ms.date: 05/16/2016
ms.openlocfilehash: 772685488b7caef92123979d817929c631248afb
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61766075"
---
# <a name="delegates"></a><span data-ttu-id="149cb-103">Délégués</span><span class="sxs-lookup"><span data-stu-id="149cb-103">Delegates</span></span>

<span data-ttu-id="149cb-104">Un délégué représente un appel de fonction en tant qu’objet.</span><span class="sxs-lookup"><span data-stu-id="149cb-104">A delegate represents a function call as an object.</span></span> <span data-ttu-id="149cb-105">Dans F#, vous devez normalement utiliser les valeurs de fonction pour représenter des fonctions comme valeurs de première classe ; Toutefois, les délégués sont utilisés dans le .NET Framework et sont donc nécessaires lorsque vous interagissez avec les API qui attendent les.</span><span class="sxs-lookup"><span data-stu-id="149cb-105">In F#, you ordinarily should use function values to represent functions as first-class values; however, delegates are used in the .NET Framework and so are needed when you interoperate with APIs that expect them.</span></span> <span data-ttu-id="149cb-106">Ils peuvent également être utilisés lors de la création de bibliothèques conçues pour utiliser d’autres langages .NET Framework.</span><span class="sxs-lookup"><span data-stu-id="149cb-106">They may also be used when authoring libraries designed for use from other .NET Framework languages.</span></span>

## <a name="syntax"></a><span data-ttu-id="149cb-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="149cb-107">Syntax</span></span>

```fsharp
type delegate-typename = delegate of type1 -> type2
```

## <a name="remarks"></a><span data-ttu-id="149cb-108">Notes</span><span class="sxs-lookup"><span data-stu-id="149cb-108">Remarks</span></span>

<span data-ttu-id="149cb-109">Dans la syntaxe précédente, `type1` représente le type d’argument ou les types et `type2` représente le type de retour.</span><span class="sxs-lookup"><span data-stu-id="149cb-109">In the previous syntax, `type1` represents the argument type or types and `type2` represents the return type.</span></span> <span data-ttu-id="149cb-110">Les types d’arguments qui sont représentées par `type1` sont automatiquement curryfiés.</span><span class="sxs-lookup"><span data-stu-id="149cb-110">The argument types that are represented by `type1` are automatically curried.</span></span> <span data-ttu-id="149cb-111">Cela suggère que pour ce type que vous utilisez une forme de tuple si les arguments de la fonction cible sont curryfiés et un tuple entre parenthèses pour les arguments qui sont déjà sous la forme de tuple.</span><span class="sxs-lookup"><span data-stu-id="149cb-111">This suggests that for this type you use a tuple form if the arguments of the target function are curried, and a parenthesized tuple for arguments that are already in the tuple form.</span></span> <span data-ttu-id="149cb-112">La curryfication automatique supprime un jeu de parenthèses, laissant un argument de tuple qui correspond à la méthode cible.</span><span class="sxs-lookup"><span data-stu-id="149cb-112">The automatic currying removes a set of parentheses, leaving a tuple argument that matches the target method.</span></span> <span data-ttu-id="149cb-113">Consultez l’exemple de code pour la syntaxe à utiliser dans chaque cas.</span><span class="sxs-lookup"><span data-stu-id="149cb-113">Refer to the code example for the syntax you should use in each case.</span></span>

<span data-ttu-id="149cb-114">Les délégués peuvent être attachés à F# statiques et les valeurs de fonction ou de méthodes d’instance.</span><span class="sxs-lookup"><span data-stu-id="149cb-114">Delegates can be attached to F# function values, and static or instance methods.</span></span> <span data-ttu-id="149cb-115">F#les valeurs de fonction peuvent être passées directement en tant qu’arguments à déléguer des constructeurs.</span><span class="sxs-lookup"><span data-stu-id="149cb-115">F# function values can be passed directly as arguments to delegate constructors.</span></span> <span data-ttu-id="149cb-116">Pour une méthode statique, vous construisez le délégué en utilisant le nom de la classe et la méthode.</span><span class="sxs-lookup"><span data-stu-id="149cb-116">For a static method, you construct the delegate by using the name of the class and the method.</span></span> <span data-ttu-id="149cb-117">Pour une méthode d’instance, vous fournissez l’instance d’objet et la méthode dans un seul argument.</span><span class="sxs-lookup"><span data-stu-id="149cb-117">For an instance method, you provide the object instance and method in one argument.</span></span> <span data-ttu-id="149cb-118">Dans les deux cas, opérateur d’accès au membre (`.`) est utilisé.</span><span class="sxs-lookup"><span data-stu-id="149cb-118">In both cases, the member access operator (`.`) is used.</span></span>

<span data-ttu-id="149cb-119">Le `Invoke` méthode sur le type délégué appelle la fonction encapsulée.</span><span class="sxs-lookup"><span data-stu-id="149cb-119">The `Invoke` method on the delegate type calls the encapsulated function.</span></span> <span data-ttu-id="149cb-120">En outre, les délégués peuvent être passés en tant que valeurs de fonction en référençant le nom de la méthode Invoke sans les parenthèses.</span><span class="sxs-lookup"><span data-stu-id="149cb-120">Also, delegates can be passed as function values by referencing the Invoke method name without the parentheses.</span></span>

<span data-ttu-id="149cb-121">Le code suivant montre la syntaxe pour créer des délégués qui représentent les différentes méthodes dans une classe.</span><span class="sxs-lookup"><span data-stu-id="149cb-121">The following code shows the syntax for creating delegates that represent various methods in a class.</span></span> <span data-ttu-id="149cb-122">Selon si la méthode est une méthode statique ou une méthode d’instance, et s’il comporte des arguments sous la forme de tuple ou de la forme curryfiée, la syntaxe pour déclarer et affecter le délégué est un peu différente.</span><span class="sxs-lookup"><span data-stu-id="149cb-122">Depending on whether the method is a static method or an instance method, and whether it has arguments in the tuple form or the curried form, the syntax for declaring and assigning the delegate is a little different.</span></span>

[!code-fsharp[Main](../../../samples/snippets/fsharp/lang-ref-2/snippet4201.fs)]

<span data-ttu-id="149cb-123">Le code suivant montre certains des différents modes, que vous pouvez travailler avec les délégués.</span><span class="sxs-lookup"><span data-stu-id="149cb-123">The following code shows some of the different ways you can work with delegates.</span></span>

[!code-fsharp[Main](../../../samples/snippets/fsharp/lang-ref-2/snippet4202.fs)]

<span data-ttu-id="149cb-124">La sortie de l’exemple de code précédent est comme suit.</span><span class="sxs-lookup"><span data-stu-id="149cb-124">The output of the previous code example is as follows.</span></span>

```console
aaaaa
bbbbb
ccccc
[|"aaa"; "bbb"|]
```

## <a name="see-also"></a><span data-ttu-id="149cb-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="149cb-125">See also</span></span>

- [<span data-ttu-id="149cb-126">Informations de référence du langage F#</span><span class="sxs-lookup"><span data-stu-id="149cb-126">F# Language Reference</span></span>](index.md)
- [<span data-ttu-id="149cb-127">Paramètres et arguments</span><span class="sxs-lookup"><span data-stu-id="149cb-127">Parameters and Arguments</span></span>](parameters-and-arguments.md)
- [<span data-ttu-id="149cb-128">Événements</span><span class="sxs-lookup"><span data-stu-id="149cb-128">Events</span></span>](members/events.md)