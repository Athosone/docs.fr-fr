---
title: 'Procédure : Déclarer une propriété avec des niveaux d’accès mixtes (Visual Basic)'
ms.date: 07/20/2015
helpviewer_keywords:
- access levels [Visual Basic], properties
- procedures [Visual Basic], defining
- Visual Basic code, procedures
- mixed access levels
- Visual Basic code, properties
- properties [Visual Basic], access levels
- Property statement [Visual Basic], declaring mixed access levels
ms.assetid: fdbb2d97-279a-4956-b26c-cbdfbc34915a
ms.openlocfilehash: e899b57e02f492b0e4909aca84c069e5b7688618
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59339812"
---
# <a name="how-to-declare-a-property-with-mixed-access-levels-visual-basic"></a><span data-ttu-id="f590b-102">Procédure : Déclarer une propriété avec des niveaux d’accès mixtes (Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="f590b-102">How to: Declare a Property with Mixed Access Levels (Visual Basic)</span></span>
<span data-ttu-id="f590b-103">Si vous souhaitez que le `Get` et `Set` procédures sur une propriété d’avoir différents niveaux d’accès, vous pouvez utiliser le niveau le plus permissif dans le `Property` instruction et le niveau le plus restrictif dans un le `Get` ou `Set` instruction.</span><span class="sxs-lookup"><span data-stu-id="f590b-103">If you want the `Get` and `Set` procedures on a property to have different access levels, you can use the more permissive level in the `Property` statement and the more restrictive level in either the `Get` or `Set` statement.</span></span> <span data-ttu-id="f590b-104">Vous utilisez des niveaux d’accès mixtes sur une propriété lorsque vous souhaitez que certaines parties du code pour être en mesure d’obtenir la valeur de propriété et que d’autres parties du code pour être en mesure de modifier la valeur.</span><span class="sxs-lookup"><span data-stu-id="f590b-104">You use mixed access levels on a property when you want certain parts of the code to be able to get the property's value, and certain other parts of the code to be able to change the value.</span></span>  
  
 <span data-ttu-id="f590b-105">Pour plus d’informations sur les niveaux d’accès, consultez [niveaux en Visual Basic d’accès](../../../../visual-basic/programming-guide/language-features/declared-elements/access-levels.md).</span><span class="sxs-lookup"><span data-stu-id="f590b-105">For more information on access levels, see [Access levels in Visual Basic](../../../../visual-basic/programming-guide/language-features/declared-elements/access-levels.md).</span></span>  
  
### <a name="to-declare-a-property-with-mixed-access-levels"></a><span data-ttu-id="f590b-106">Pour déclarer une propriété avec des niveaux d’accès mixtes</span><span class="sxs-lookup"><span data-stu-id="f590b-106">To declare a property with mixed access levels</span></span>  
  
1. <span data-ttu-id="f590b-107">Déclarez la propriété de façon normale et spécifiez le niveau d’accès moins restrictif (tel que `Public`) dans le `Property` instruction.</span><span class="sxs-lookup"><span data-stu-id="f590b-107">Declare the property in the normal way, and specify the less restrictive access level (such as `Public`) in the `Property` statement.</span></span>  
  
2. <span data-ttu-id="f590b-108">Déclarez le `Get` ou le `Set` procédure en spécifiant le niveau d’accès plus restrictif (tel que `Friend`).</span><span class="sxs-lookup"><span data-stu-id="f590b-108">Declare either the `Get` or the `Set` procedure specifying the more restrictive access level (such as `Friend`).</span></span>  
  
3. <span data-ttu-id="f590b-109">Ne spécifiez pas un niveau d’accès sur les autres procédures de propriété.</span><span class="sxs-lookup"><span data-stu-id="f590b-109">Do not specify an access level on the other property procedure.</span></span> <span data-ttu-id="f590b-110">Il suppose que le niveau d’accès déclaré dans le `Property` instruction.</span><span class="sxs-lookup"><span data-stu-id="f590b-110">It assumes the access level declared in the `Property` statement.</span></span> <span data-ttu-id="f590b-111">Vous pouvez restreindre l’accès sur un seul des procédures de propriété.</span><span class="sxs-lookup"><span data-stu-id="f590b-111">You can restrict access on only one of the property procedures.</span></span>  
  
     [!code-vb[VbVbcnProcedures#10](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbcnProcedures/VB/Class1.vb#10)]  
  
     <span data-ttu-id="f590b-112">Dans l’exemple précédent, le `Get` procédure a les mêmes `Protected` accès en tant que la propriété proprement dite, tandis que le `Set` procédure a `Private` accès.</span><span class="sxs-lookup"><span data-stu-id="f590b-112">In the preceding example, the `Get` procedure has the same `Protected` access as the property itself, while the `Set` procedure has `Private` access.</span></span> <span data-ttu-id="f590b-113">Une classe dérivée de `employee` peut lire le `salary` valeur, mais uniquement la `employee` classe peut la définir.</span><span class="sxs-lookup"><span data-stu-id="f590b-113">A class derived from `employee` can read the `salary` value, but only the `employee` class can set it.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="f590b-114">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f590b-114">See also</span></span>

- [<span data-ttu-id="f590b-115">Procédures</span><span class="sxs-lookup"><span data-stu-id="f590b-115">Procedures</span></span>](./index.md)
- [<span data-ttu-id="f590b-116">Procédures de propriété</span><span class="sxs-lookup"><span data-stu-id="f590b-116">Property Procedures</span></span>](./property-procedures.md)
- [<span data-ttu-id="f590b-117">Paramètres et arguments d’une procédure</span><span class="sxs-lookup"><span data-stu-id="f590b-117">Procedure Parameters and Arguments</span></span>](./procedure-parameters-and-arguments.md)
- [<span data-ttu-id="f590b-118">Property (instruction)</span><span class="sxs-lookup"><span data-stu-id="f590b-118">Property Statement</span></span>](../../../../visual-basic/language-reference/statements/property-statement.md)
- [<span data-ttu-id="f590b-119">Différences entre les propriétés et les Variables en Visual Basic</span><span class="sxs-lookup"><span data-stu-id="f590b-119">Differences Between Properties and Variables in Visual Basic</span></span>](./differences-between-properties-and-variables.md)
- [<span data-ttu-id="f590b-120">Guide pratique pour Créer une propriété</span><span class="sxs-lookup"><span data-stu-id="f590b-120">How to: Create a Property</span></span>](./how-to-create-a-property.md)
- [<span data-ttu-id="f590b-121">Guide pratique pour Appeler une procédure de propriété</span><span class="sxs-lookup"><span data-stu-id="f590b-121">How to: Call a Property Procedure</span></span>](./how-to-call-a-property-procedure.md)
- [<span data-ttu-id="f590b-122">Guide pratique pour Déclarer et appeler une propriété par défaut en Visual Basic</span><span class="sxs-lookup"><span data-stu-id="f590b-122">How to: Declare and Call a Default Property in Visual Basic</span></span>](./how-to-declare-and-call-a-default-property.md)
- [<span data-ttu-id="f590b-123">Guide pratique pour Placer une valeur dans une propriété</span><span class="sxs-lookup"><span data-stu-id="f590b-123">How to: Put a Value in a Property</span></span>](./how-to-put-a-value-in-a-property.md)
- [<span data-ttu-id="f590b-124">Guide pratique pour Obtenir une valeur d’une propriété</span><span class="sxs-lookup"><span data-stu-id="f590b-124">How to: Get a Value from a Property</span></span>](./how-to-get-a-value-from-a-property.md)
