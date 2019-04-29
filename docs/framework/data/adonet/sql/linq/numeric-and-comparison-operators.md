---
title: Opérateurs de comparaison et opérateurs numériques
ms.date: 03/30/2017
ms.assetid: 25b4a26a-06f2-4f80-87a9-76705ed46197
ms.openlocfilehash: b29f78a13d6d0313e0ad29754f6d13ac08be1092
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61783134"
---
# <a name="numeric-and-comparison-operators"></a><span data-ttu-id="bd3a2-102">Opérateurs de comparaison et opérateurs numériques</span><span class="sxs-lookup"><span data-stu-id="bd3a2-102">Numeric and Comparison Operators</span></span>

<span data-ttu-id="bd3a2-103">Les opérateurs arithmétiques et de comparaison fonctionnent conformément aux attentes dans le Common Language Runtime (CLR), à l'exception des points suivants :</span><span class="sxs-lookup"><span data-stu-id="bd3a2-103">Arithmetic and comparison operators work as expected in the common language runtime (CLR) except as follows:</span></span>

- <span data-ttu-id="bd3a2-104">SQL ne prend pas en charge l'opérateur modulo sur les nombres à virgule flottante.</span><span class="sxs-lookup"><span data-stu-id="bd3a2-104">SQL does not support the modulus operator on floating-point numbers.</span></span>

- <span data-ttu-id="bd3a2-105">SQL ne prend pas en charge l'arithmétique non contrôlée.</span><span class="sxs-lookup"><span data-stu-id="bd3a2-105">SQL does not support unchecked arithmetic.</span></span>

- <span data-ttu-id="bd3a2-106">Les opérateurs d'incrémentation et de décrémentation ne sont pas pris en charge car ils présentent des effets secondaires lorsqu'ils sont utilisés dans des expressions qui ne peuvent pas être répliquées dans SQL.</span><span class="sxs-lookup"><span data-stu-id="bd3a2-106">Increment and decrement operators cause side-effects when you use them in expressions that cannot be replicated in SQL and are, therefore, not supported.</span></span>

## <a name="supported-operators"></a><span data-ttu-id="bd3a2-107">Opérateurs pris en charge</span><span class="sxs-lookup"><span data-stu-id="bd3a2-107">Supported Operators</span></span>

[!INCLUDE[vbtecdlinq](../../../../../../includes/vbtecdlinq-md.md)] <span data-ttu-id="bd3a2-108">prend en charge les opérateurs suivants.</span><span class="sxs-lookup"><span data-stu-id="bd3a2-108">supports the following operators.</span></span>

- <span data-ttu-id="bd3a2-109">Opérateurs arithmétiques de base :</span><span class="sxs-lookup"><span data-stu-id="bd3a2-109">Basic arithmetic operators:</span></span>

  - `+`

  - <span data-ttu-id="bd3a2-110">`-` (soustraction)</span><span class="sxs-lookup"><span data-stu-id="bd3a2-110">`-` (subtraction)</span></span>

  - `*`

  - `/`

  - <span data-ttu-id="bd3a2-111">Division d'entier Visual Basic (`\`)</span><span class="sxs-lookup"><span data-stu-id="bd3a2-111">Visual Basic integer division (`\`)</span></span>

  - <span data-ttu-id="bd3a2-112">`%` (`Mod` Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="bd3a2-112">`%` (Visual Basic `Mod`)</span></span>

  - `<<`

  - `>>`

  - <span data-ttu-id="bd3a2-113">`-` (négation unaire)</span><span class="sxs-lookup"><span data-stu-id="bd3a2-113">`-` (unary negation)</span></span>

- <span data-ttu-id="bd3a2-114">Opérateurs de comparaison de base :</span><span class="sxs-lookup"><span data-stu-id="bd3a2-114">Basic comparison operators:</span></span>

  - <span data-ttu-id="bd3a2-115">`=` Visual Basic et `==` C#</span><span class="sxs-lookup"><span data-stu-id="bd3a2-115">Visual Basic `=` and C# `==`</span></span>

  - <span data-ttu-id="bd3a2-116">`<>` Visual Basic et `!=` C#</span><span class="sxs-lookup"><span data-stu-id="bd3a2-116">Visual Basic `<>` and C# `!=`</span></span>

  - <span data-ttu-id="bd3a2-117">Visual Basic `Is/IsNot`</span><span class="sxs-lookup"><span data-stu-id="bd3a2-117">Visual Basic `Is/IsNot`</span></span>

  - `<`

  - `<=`

  - `>`

  - `>=`

## <a name="see-also"></a><span data-ttu-id="bd3a2-118">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="bd3a2-118">See also</span></span>

- [<span data-ttu-id="bd3a2-119">Fonctions et types de données</span><span class="sxs-lookup"><span data-stu-id="bd3a2-119">Data Types and Functions</span></span>](../../../../../../docs/framework/data/adonet/sql/linq/data-types-and-functions.md)
- [<span data-ttu-id="bd3a2-120">Opérateurs C#</span><span class="sxs-lookup"><span data-stu-id="bd3a2-120">C# Operators</span></span>](../../../../../../docs/csharp/language-reference/operators/index.md)
- [<span data-ttu-id="bd3a2-121">Opérateurs</span><span class="sxs-lookup"><span data-stu-id="bd3a2-121">Operators</span></span>](../../../../../visual-basic/language-reference/operators/index.md)
