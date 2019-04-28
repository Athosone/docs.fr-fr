---
title: Opérateurs booléens
description: En savoir plus sur les opérateurs booléens sont disponibles dans le F# langage de programmation.
ms.date: 05/16/2016
ms.openlocfilehash: 5353b6ec6a0bd610f3446761a1d28f01f0403302
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61925812"
---
# <a name="boolean-operators"></a><span data-ttu-id="6434f-103">Opérateurs booléens</span><span class="sxs-lookup"><span data-stu-id="6434f-103">Boolean Operators</span></span>

<span data-ttu-id="6434f-104">Cette rubrique décrit la prise en charge pour les opérateurs booléens dans les F# langage.</span><span class="sxs-lookup"><span data-stu-id="6434f-104">This topic describes the support for Boolean operators in the F# language.</span></span>

## <a name="summary-of-boolean-operators"></a><span data-ttu-id="6434f-105">Résumé des opérateurs booléens</span><span class="sxs-lookup"><span data-stu-id="6434f-105">Summary of Boolean Operators</span></span>

<span data-ttu-id="6434f-106">Le tableau suivant récapitule les opérateurs booléens sont disponibles dans le F# langage.</span><span class="sxs-lookup"><span data-stu-id="6434f-106">The following table summarizes the Boolean operators that are available in the F# language.</span></span> <span data-ttu-id="6434f-107">Le seul type pris en charge par ces opérateurs est le `bool` type.</span><span class="sxs-lookup"><span data-stu-id="6434f-107">The only type supported by these operators is the `bool` type.</span></span>

|<span data-ttu-id="6434f-108">Opérateur</span><span class="sxs-lookup"><span data-stu-id="6434f-108">Operator</span></span>|<span data-ttu-id="6434f-109">Description</span><span class="sxs-lookup"><span data-stu-id="6434f-109">Description</span></span>|
|--------|-----------|
|`not`|<span data-ttu-id="6434f-110">Négation booléenne</span><span class="sxs-lookup"><span data-stu-id="6434f-110">Boolean negation</span></span>|
|<code>&#124;&#124;</code>|<span data-ttu-id="6434f-111">Booléen OR</span><span class="sxs-lookup"><span data-stu-id="6434f-111">Boolean OR</span></span>|
|`&&`|<span data-ttu-id="6434f-112">Booléen AND</span><span class="sxs-lookup"><span data-stu-id="6434f-112">Boolean AND</span></span>|

<span data-ttu-id="6434f-113">Les opérateurs booléens AND et OR effectuent *l’évaluation de court-circuit*, autrement dit, ils évaluent l’expression à droite de l’opérateur uniquement lorsqu’il est nécessaire déterminer le résultat global de l’expression.</span><span class="sxs-lookup"><span data-stu-id="6434f-113">The Boolean AND and OR operators perform *short-circuit evaluation*, that is, they evaluate the expression on the right of the operator only when it is necessary to determine the overall result of the expression.</span></span> <span data-ttu-id="6434f-114">La deuxième expression de la `&&` opérateur est évalué uniquement si la première expression a la valeur `true`; la deuxième expression de la `||` opérateur est évalué uniquement si la première expression a la valeur `false`.</span><span class="sxs-lookup"><span data-stu-id="6434f-114">The second expression of the `&&` operator is evaluated only if the first expression evaluates to `true`; the second expression of the `||` operator is evaluated only if the first expression evaluates to `false`.</span></span>

## <a name="see-also"></a><span data-ttu-id="6434f-115">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="6434f-115">See also</span></span>

- [<span data-ttu-id="6434f-116">Opérateurs au niveau du bit</span><span class="sxs-lookup"><span data-stu-id="6434f-116">Bitwise Operators</span></span>](bitwise-operators.md)
- [<span data-ttu-id="6434f-117">Opérateurs arithmétiques</span><span class="sxs-lookup"><span data-stu-id="6434f-117">Arithmetic Operators</span></span>](arithmetic-operators.md)
- [<span data-ttu-id="6434f-118">Informations de référence des symboles et opérateurs</span><span class="sxs-lookup"><span data-stu-id="6434f-118">Symbol and Operator Reference</span></span>](index.md)