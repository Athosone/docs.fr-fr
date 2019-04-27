---
title: "'Is' requiert des opérandes ayant des types référence, mais cet opérande a le type valeur '<typename>'"
ms.date: 07/20/2015
f1_keywords:
- bc30020
- vbc30020
helpviewer_keywords:
- BC30020
ms.assetid: 228afebd-1203-4bd3-8d7a-c5c56f3cedc4
ms.openlocfilehash: b828de196a12128a9f34ee1f9ff1e57fee22c687
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61799188"
---
# <a name="is-requires-operands-that-have-reference-types-but-this-operand-has-the-value-type-typename"></a><span data-ttu-id="bb6b6-102">'Is' requiert des opérandes qui ont des types référence, mais cet opérande a le type valeur '\<nom_type >'</span><span class="sxs-lookup"><span data-stu-id="bb6b6-102">'Is' requires operands that have reference types, but this operand has the value type '\<typename>'</span></span>
<span data-ttu-id="bb6b6-103">Le `Is` opérateur de comparaison détermine si deux variables d’objet font référence à la même instance.</span><span class="sxs-lookup"><span data-stu-id="bb6b6-103">The `Is` comparison operator determines whether two object variables refer to the same instance.</span></span> <span data-ttu-id="bb6b6-104">Cette comparaison n’est pas définie pour les types valeur.</span><span class="sxs-lookup"><span data-stu-id="bb6b6-104">This comparison is not defined for value types.</span></span>  
  
 <span data-ttu-id="bb6b6-105">**ID d’erreur :** BC30020</span><span class="sxs-lookup"><span data-stu-id="bb6b6-105">**Error ID:** BC30020</span></span>  
  
## <a name="to-correct-this-error"></a><span data-ttu-id="bb6b6-106">Pour corriger cette erreur</span><span class="sxs-lookup"><span data-stu-id="bb6b6-106">To correct this error</span></span>  
  
-   <span data-ttu-id="bb6b6-107">Utilisez l’opérateur de comparaison arithmétique approprié ou `Like` opérateur pour comparer deux types de valeur.</span><span class="sxs-lookup"><span data-stu-id="bb6b6-107">Use the appropriate arithmetic comparison operator or the `Like` operator to compare two value types.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="bb6b6-108">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="bb6b6-108">See also</span></span>

- [<span data-ttu-id="bb6b6-109">Is (opérateur)</span><span class="sxs-lookup"><span data-stu-id="bb6b6-109">Is Operator</span></span>](../../../visual-basic/language-reference/operators/is-operator.md)
- [<span data-ttu-id="bb6b6-110">Like (opérateur)</span><span class="sxs-lookup"><span data-stu-id="bb6b6-110">Like Operator</span></span>](../../../visual-basic/language-reference/operators/like-operator.md)
- [<span data-ttu-id="bb6b6-111">Opérateurs de comparaison</span><span class="sxs-lookup"><span data-stu-id="bb6b6-111">Comparison Operators</span></span>](../../../visual-basic/language-reference/operators/comparison-operators.md)
