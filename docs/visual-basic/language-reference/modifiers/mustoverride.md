---
title: MustOverride (Visual Basic)
ms.date: 07/20/2015
f1_keywords:
- vb.MustOverride
- MustOverride
helpviewer_keywords:
- virtual elements [Visual Basic], pure
- elements [Visual Basic], pure virtual
- properties [Visual Basic], redefining
- procedures [Visual Basic], overriding
- overriding, MustOverride keyword
- procedures [Visual Basic], redefining
- pure virtual elements [Visual Basic]
- MustOverride keyword [Visual Basic]
- properties [Visual Basic], overriding
ms.assetid: 6e9d9ad6-bb64-433f-b32b-3ef84293bf96
ms.openlocfilehash: 0ddd7d0d2a57afc02aa7483ba5e83b65c48af534
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61920752"
---
# <a name="mustoverride-visual-basic"></a><span data-ttu-id="ec339-102">MustOverride (Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="ec339-102">MustOverride (Visual Basic)</span></span>
<span data-ttu-id="ec339-103">Spécifie qu’une propriété ou procédure n’est pas implémentée dans cette classe et doit être substitué dans une classe dérivée avant de pouvoir être utilisé.</span><span class="sxs-lookup"><span data-stu-id="ec339-103">Specifies that a property or procedure is not implemented in this class and must be overridden in a derived class before it can be used.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="ec339-104">Notes</span><span class="sxs-lookup"><span data-stu-id="ec339-104">Remarks</span></span>  
 <span data-ttu-id="ec339-105">Vous pouvez utiliser `MustOverride` uniquement dans une instruction de déclaration de propriété ou de procédure.</span><span class="sxs-lookup"><span data-stu-id="ec339-105">You can use `MustOverride` only in a property or procedure declaration statement.</span></span> <span data-ttu-id="ec339-106">La propriété ou procédure spécifie `MustOverride` doit être un membre d’une classe, et la classe doit être marquée [MustInherit](../../../visual-basic/language-reference/modifiers/mustinherit.md).</span><span class="sxs-lookup"><span data-stu-id="ec339-106">The property or procedure that specifies `MustOverride` must be a member of a class, and the class must be marked [MustInherit](../../../visual-basic/language-reference/modifiers/mustinherit.md).</span></span>  
  
## <a name="rules"></a><span data-ttu-id="ec339-107">Règles</span><span class="sxs-lookup"><span data-stu-id="ec339-107">Rules</span></span>  
  
- <span data-ttu-id="ec339-108">**Déclaration incomplète.**</span><span class="sxs-lookup"><span data-stu-id="ec339-108">**Incomplete Declaration.**</span></span> <span data-ttu-id="ec339-109">Lorsque vous spécifiez `MustOverride`, vous ne fournissez pas de lignes supplémentaires de code pour la propriété ou procédure, pas même le `End Function`, `End Property`, ou `End Sub` instruction.</span><span class="sxs-lookup"><span data-stu-id="ec339-109">When you specify `MustOverride`, you do not supply any additional lines of code for the property or procedure, not even the `End Function`, `End Property`, or `End Sub` statement.</span></span>  
  
- <span data-ttu-id="ec339-110">**Modificateurs combinés.**</span><span class="sxs-lookup"><span data-stu-id="ec339-110">**Combined Modifiers.**</span></span> <span data-ttu-id="ec339-111">Vous ne pouvez pas spécifier `MustOverride` avec `NotOverridable`, `Overridable`, ou `Shared` dans la même déclaration.</span><span class="sxs-lookup"><span data-stu-id="ec339-111">You cannot specify `MustOverride` together with `NotOverridable`, `Overridable`, or `Shared` in the same declaration.</span></span>  
  
- <span data-ttu-id="ec339-112">**Occultation et substitution.**</span><span class="sxs-lookup"><span data-stu-id="ec339-112">**Shadowing and Overriding.**</span></span> <span data-ttu-id="ec339-113">L'occultation et la substitution redéfinissent toutes les deux un élément hérité, mais il existe des différences importantes entre ces deux approches.</span><span class="sxs-lookup"><span data-stu-id="ec339-113">Both shadowing and overriding redefine an inherited element, but there are significant differences between the two approaches.</span></span> <span data-ttu-id="ec339-114">Pour plus d’informations, consultez [occultation dans Visual Basic](../../../visual-basic/programming-guide/language-features/declared-elements/shadowing.md).</span><span class="sxs-lookup"><span data-stu-id="ec339-114">For more information, see [Shadowing in Visual Basic](../../../visual-basic/programming-guide/language-features/declared-elements/shadowing.md).</span></span>  
  
- <span data-ttu-id="ec339-115">**Autres termes.**</span><span class="sxs-lookup"><span data-stu-id="ec339-115">**Alternate Terms.**</span></span> <span data-ttu-id="ec339-116">Un élément qui ne peut pas être utilisé sauf dans une substitution est parfois appelé un *pure virtuel* élément.</span><span class="sxs-lookup"><span data-stu-id="ec339-116">An element that cannot be used except in an override is sometimes called a *pure virtual* element.</span></span>  
  
 <span data-ttu-id="ec339-117">Le modificateur `MustOverride` peut être utilisé dans les contextes suivants :</span><span class="sxs-lookup"><span data-stu-id="ec339-117">The `MustOverride` modifier can be used in these contexts:</span></span>  
  
 [<span data-ttu-id="ec339-118">Function (instruction)</span><span class="sxs-lookup"><span data-stu-id="ec339-118">Function Statement</span></span>](../../../visual-basic/language-reference/statements/function-statement.md)  
  
 [<span data-ttu-id="ec339-119">Property (instruction)</span><span class="sxs-lookup"><span data-stu-id="ec339-119">Property Statement</span></span>](../../../visual-basic/language-reference/statements/property-statement.md)  
  
 [<span data-ttu-id="ec339-120">Sub (instruction)</span><span class="sxs-lookup"><span data-stu-id="ec339-120">Sub Statement</span></span>](../../../visual-basic/language-reference/statements/sub-statement.md)  
  
## <a name="see-also"></a><span data-ttu-id="ec339-121">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ec339-121">See also</span></span>

- [<span data-ttu-id="ec339-122">NotOverridable</span><span class="sxs-lookup"><span data-stu-id="ec339-122">NotOverridable</span></span>](../../../visual-basic/language-reference/modifiers/notoverridable.md)
- [<span data-ttu-id="ec339-123">Overridable</span><span class="sxs-lookup"><span data-stu-id="ec339-123">Overridable</span></span>](../../../visual-basic/language-reference/modifiers/overridable.md)
- [<span data-ttu-id="ec339-124">Overrides</span><span class="sxs-lookup"><span data-stu-id="ec339-124">Overrides</span></span>](../../../visual-basic/language-reference/modifiers/overrides.md)
- [<span data-ttu-id="ec339-125">MustInherit</span><span class="sxs-lookup"><span data-stu-id="ec339-125">MustInherit</span></span>](../../../visual-basic/language-reference/modifiers/mustinherit.md)
- [<span data-ttu-id="ec339-126">Mots clés</span><span class="sxs-lookup"><span data-stu-id="ec339-126">Keywords</span></span>](../../../visual-basic/language-reference/keywords/index.md)
- [<span data-ttu-id="ec339-127">Occultation dans Visual Basic</span><span class="sxs-lookup"><span data-stu-id="ec339-127">Shadowing in Visual Basic</span></span>](../../../visual-basic/programming-guide/language-features/declared-elements/shadowing.md)
