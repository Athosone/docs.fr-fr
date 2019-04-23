---
title: La classe déléguée '<classname>' n'a pas de méthode Invoke, c'est pourquoi une expression de ce type ne peut pas être la cible d'un appel de méthode
ms.date: 07/20/2015
f1_keywords:
- vbc30220
- bc30220
helpviewer_keywords:
- BC30220
ms.assetid: 6be0d61c-f2f9-4f9b-ab90-8871a0d7206d
ms.openlocfilehash: 3fe164d868ee7bde0e687e1d592f4d5a17565aea
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59321300"
---
# <a name="delegate-class-classname-has-no-invoke-method-so-an-expression-of-this-type-cannot-be-the-target-of-a-method-call"></a><span data-ttu-id="7eb5d-102">Classe déléguée\<nom_classe >' n’a aucun méthode Invoke, donc une expression de ce type ne peut pas être la cible d’un appel de méthode</span><span class="sxs-lookup"><span data-stu-id="7eb5d-102">Delegate class '\<classname>' has no Invoke method, so an expression of this type cannot be the target of a method call</span></span>
<span data-ttu-id="7eb5d-103">Un appel à `Invoke` via un délégué a échoué, car `Invoke` n’est pas implémentée sur la classe déléguée.</span><span class="sxs-lookup"><span data-stu-id="7eb5d-103">A call to `Invoke` through a delegate has failed because `Invoke` is not implemented on the delegate class.</span></span>  
  
 <span data-ttu-id="7eb5d-104">**ID d’erreur :** BC30220</span><span class="sxs-lookup"><span data-stu-id="7eb5d-104">**Error ID:** BC30220</span></span>  
  
## <a name="to-correct-this-error"></a><span data-ttu-id="7eb5d-105">Pour corriger cette erreur</span><span class="sxs-lookup"><span data-stu-id="7eb5d-105">To correct this error</span></span>  
  
1. <span data-ttu-id="7eb5d-106">Vérifiez qu’une instance de la classe déléguée a été créée avec un `Dim` instruction et qu’une procédure a été assignée à l’instance de délégué avec le `AddressOf` opérateur.</span><span class="sxs-lookup"><span data-stu-id="7eb5d-106">Ensure that an instance of the delegate class has been created with a `Dim` statement and that a procedure has been assigned to the delegate instance with the `AddressOf` operator.</span></span>  
  
2. <span data-ttu-id="7eb5d-107">Recherchez le code qui implémente la classe déléguée et vérifiez qu’il implémente la `Invoke` procédure.</span><span class="sxs-lookup"><span data-stu-id="7eb5d-107">Locate the code that implements the delegate class and make sure it implements the `Invoke` procedure.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="7eb5d-108">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="7eb5d-108">See also</span></span>

- [<span data-ttu-id="7eb5d-109">Délégués</span><span class="sxs-lookup"><span data-stu-id="7eb5d-109">Delegates</span></span>](../../../visual-basic/programming-guide/language-features/delegates/index.md)
- [<span data-ttu-id="7eb5d-110">Delegate (instruction)</span><span class="sxs-lookup"><span data-stu-id="7eb5d-110">Delegate Statement</span></span>](../../../visual-basic/language-reference/statements/delegate-statement.md)
- [<span data-ttu-id="7eb5d-111">AddressOf (opérateur)</span><span class="sxs-lookup"><span data-stu-id="7eb5d-111">AddressOf Operator</span></span>](../../../visual-basic/language-reference/operators/addressof-operator.md)
- [<span data-ttu-id="7eb5d-112">Dim (instruction)</span><span class="sxs-lookup"><span data-stu-id="7eb5d-112">Dim Statement</span></span>](../../../visual-basic/language-reference/statements/dim-statement.md)
