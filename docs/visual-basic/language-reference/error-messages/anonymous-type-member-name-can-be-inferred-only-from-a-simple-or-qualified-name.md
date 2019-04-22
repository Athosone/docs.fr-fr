---
title: Le nom du membre de type anonyme ne peut être déduit qu’à partir d’un nom simple ou qualifié sans argument
ms.date: 07/20/2015
f1_keywords:
- vbc36556
- bc36556
helpviewer_keywords:
- BC36556
ms.assetid: e3ba1f33-3a71-4f03-9b04-ed5ec17de17c
ms.openlocfilehash: b798f296b62b51de34a7ec5ce5a8b608273f5748
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "58819227"
---
# <a name="anonymous-type-member-name-can-be-inferred-only-from-a-simple-or-qualified-name-with-no-arguments"></a><span data-ttu-id="5d738-102">Le nom du membre de type anonyme ne peut être déduit qu’à partir d’un nom simple ou qualifié sans argument</span><span class="sxs-lookup"><span data-stu-id="5d738-102">Anonymous type member name can be inferred only from a simple or qualified name with no arguments</span></span>
<span data-ttu-id="5d738-103">Impossible de déduire un nom de membre de type anonyme à partir d’une expression complexe.</span><span class="sxs-lookup"><span data-stu-id="5d738-103">You cannot infer an anonymous type member name from a complex expression.</span></span>  
  
```vb  
Dim numbers() As Integer = {1, 2, 3, 4, 5}  
' Not valid.  
' Dim instanceName1 = New With {numbers(3)}  
```  
  
 <span data-ttu-id="5d738-104">Pour plus d’informations sur les sources à partir de laquelle les types anonymes peuvent et ne peut pas déduire les types et les noms de membres, consultez [Comment : Déduire les Types dans les déclarations de types anonymes et les noms de propriété](../../../visual-basic/programming-guide/language-features/objects-and-classes/how-to-infer-property-names-and-types-in-anonymous-type-declarations.md).</span><span class="sxs-lookup"><span data-stu-id="5d738-104">For more information about sources from which anonymous types can and cannot infer member names and types, see [How to: Infer Property Names and Types in Anonymous Type Declarations](../../../visual-basic/programming-guide/language-features/objects-and-classes/how-to-infer-property-names-and-types-in-anonymous-type-declarations.md).</span></span>  
  
 <span data-ttu-id="5d738-105">**ID d’erreur :** BC36556</span><span class="sxs-lookup"><span data-stu-id="5d738-105">**Error ID:** BC36556</span></span>  
  
## <a name="to-correct-this-error"></a><span data-ttu-id="5d738-106">Pour corriger cette erreur</span><span class="sxs-lookup"><span data-stu-id="5d738-106">To correct this error</span></span>  
  
-   <span data-ttu-id="5d738-107">Assignez l’expression à un nom de membre, comme indiqué dans le code suivant :</span><span class="sxs-lookup"><span data-stu-id="5d738-107">Assign the expression to a member name, as shown in the following code:</span></span>  
  
    ```  
    Dim instanceName2 = New With {.number = numbers(3)}  
    ```  
  
## <a name="see-also"></a><span data-ttu-id="5d738-108">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="5d738-108">See also</span></span>

- [<span data-ttu-id="5d738-109">Types anonymes</span><span class="sxs-lookup"><span data-stu-id="5d738-109">Anonymous Types</span></span>](../../../visual-basic/programming-guide/language-features/objects-and-classes/anonymous-types.md)
- [<span data-ttu-id="5d738-110">Guide pratique pour Déduire les Types dans les déclarations de types anonymes et les noms de propriété</span><span class="sxs-lookup"><span data-stu-id="5d738-110">How to: Infer Property Names and Types in Anonymous Type Declarations</span></span>](../../../visual-basic/programming-guide/language-features/objects-and-classes/how-to-infer-property-names-and-types-in-anonymous-type-declarations.md)
