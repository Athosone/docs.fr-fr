---
title: <proceduresignature1> n’est pas conforme CLS, car il surcharge <proceduresignature2> dont il diffère uniquement par un tableau de types de paramètres tableau ou par la dimension des types de paramètres tableau
ms.date: 07/20/2015
f1_keywords:
- vbc40035
- bc40035
helpviewer_keywords:
- BC40035
ms.assetid: 50a66dbe-2c1e-41bf-96bc-369301c891ac
ms.openlocfilehash: 0bda4ad6a4d5368d93e2ca603b78bf9db6aca858
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61920911"
---
# <a name="proceduresignature1-is-not-cls-compliant-because-it-overloads-proceduresignature2-which-differs-from-it-only-by-array-of-array-parameter-types-or-by-the-rank-of-the-array-parameter-types"></a><span data-ttu-id="828c1-102">\<proceduresignature1 > n’est pas conforme CLS, car il surcharge \<proceduresignature2 > dont il diffère uniquement par un tableau de types de paramètres tableau ou par la dimension des types de paramètres tableau</span><span class="sxs-lookup"><span data-stu-id="828c1-102">\<proceduresignature1> is not CLS-compliant because it overloads \<proceduresignature2> which differs from it only by array of array parameter types or by the rank of the array parameter types</span></span>
<span data-ttu-id="828c1-103">Une procédure ou la propriété est marquée comme `<CLSCompliant(True)>` quand il substitue à une autre procédure ou propriété et la seule différence entre leurs listes de paramètres est le niveau d’imbrication d’un tableau en escalier ou le rang d’un tableau.</span><span class="sxs-lookup"><span data-stu-id="828c1-103">A procedure or property is marked as `<CLSCompliant(True)>` when it overrides another procedure or property and the only difference between their parameter lists is the nesting level of a jagged array or the rank of an array.</span></span>  
  
 <span data-ttu-id="828c1-104">Dans les déclarations suivantes, les deuxième et troisième déclarations génèrent cette erreur.</span><span class="sxs-lookup"><span data-stu-id="828c1-104">In the following declarations, the second and third declarations generate this error.</span></span>  
  
 `Overloads Sub processArray(ByVal arrayParam() As Integer)`  
  
 `Overloads Sub processArray(ByVal arrayParam()() As Integer)`  
  
 `Overloads Sub processArray(ByVal arrayParam(,) As Integer)`  
  
 <span data-ttu-id="828c1-105">La deuxième déclaration remplace le paramètre unidimensionnel d’origine `arrayParam` à un tableau de tableaux.</span><span class="sxs-lookup"><span data-stu-id="828c1-105">The second declaration changes the original one-dimensional parameter `arrayParam` to an array of arrays.</span></span> <span data-ttu-id="828c1-106">La troisième déclaration remplace `arrayParam` un tableau à deux dimensions (rang 2).</span><span class="sxs-lookup"><span data-stu-id="828c1-106">The third declaration changes `arrayParam` to a two-dimensional array (rank 2).</span></span> <span data-ttu-id="828c1-107">Bien que Visual Basic autorise les surcharges à différer uniquement par l’une de ces modifications, une telle surcharge n’est pas conforme à la [indépendance du langage et composants indépendants du langage](../../../standard/language-independence-and-language-independent-components.md) (CLS).</span><span class="sxs-lookup"><span data-stu-id="828c1-107">While Visual Basic allows overloads to differ only by one of these changes, such overloading is not compliant with the [Language Independence and Language-Independent Components](../../../standard/language-independence-and-language-independent-components.md) (CLS).</span></span>  
  
 <span data-ttu-id="828c1-108">Quand vous appliquez l’attribut <xref:System.CLSCompliantAttribute> à un élément de programmation, vous affectez au paramètre `isCompliant` de l’attribut la valeur `True` ou `False` pour indiquer la conformité ou la non-conformité.</span><span class="sxs-lookup"><span data-stu-id="828c1-108">When you apply the <xref:System.CLSCompliantAttribute> to a programming element, you set the attribute's `isCompliant` parameter to either `True` or `False` to indicate compliance or noncompliance.</span></span> <span data-ttu-id="828c1-109">Il n’existe pas de valeur par défaut pour ce paramètre et vous devez fournir une valeur.</span><span class="sxs-lookup"><span data-stu-id="828c1-109">There is no default for this parameter, and you must supply a value.</span></span>  
  
 <span data-ttu-id="828c1-110">Si vous n’appliquez pas <xref:System.CLSCompliantAttribute> à un élément, il est considéré comme étant non conforme.</span><span class="sxs-lookup"><span data-stu-id="828c1-110">If you do not apply the <xref:System.CLSCompliantAttribute> to an element, it is considered to be noncompliant.</span></span>  
  
 <span data-ttu-id="828c1-111">Par défaut, ce message est un avertissement.</span><span class="sxs-lookup"><span data-stu-id="828c1-111">By default, this message is a warning.</span></span> <span data-ttu-id="828c1-112">Pour plus d’informations sur le masquage des avertissements ou leur traitement en tant qu’erreurs, consultez [Configuring Warnings in Visual Basic](/visualstudio/ide/configuring-warnings-in-visual-basic).</span><span class="sxs-lookup"><span data-stu-id="828c1-112">For information on hiding warnings or treating warnings as errors, see [Configuring Warnings in Visual Basic](/visualstudio/ide/configuring-warnings-in-visual-basic).</span></span>  
  
 <span data-ttu-id="828c1-113">**ID d’erreur :** BC40035</span><span class="sxs-lookup"><span data-stu-id="828c1-113">**Error ID:** BC40035</span></span>  
  
## <a name="to-correct-this-error"></a><span data-ttu-id="828c1-114">Pour corriger cette erreur</span><span class="sxs-lookup"><span data-stu-id="828c1-114">To correct this error</span></span>  
  
- <span data-ttu-id="828c1-115">Si vous avez besoin de la conformité CLS, définissez vos surcharges pour diffèrent entre eux dans plus de manières que seules les modifications mentionnées dans cette page d’aide.</span><span class="sxs-lookup"><span data-stu-id="828c1-115">If you require CLS compliance, define your overloads to differ from each other in more ways than only the changes cited on this Help page.</span></span>  
  
- <span data-ttu-id="828c1-116">Si vous avez besoin que les surcharges diffèrent uniquement par les modifications mentionnées dans cette aide page, supprimez le <xref:System.CLSCompliantAttribute> à partir de leurs définitions ou marquez-les comme `<CLSCompliant(False)>`.</span><span class="sxs-lookup"><span data-stu-id="828c1-116">If you require that the overloads differ only by the changes cited on this Help page, remove the <xref:System.CLSCompliantAttribute> from their definitions or mark them as `<CLSCompliant(False)>`.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="828c1-117">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="828c1-117">See also</span></span>

- [<span data-ttu-id="828c1-118">Surcharge de procédure</span><span class="sxs-lookup"><span data-stu-id="828c1-118">Procedure Overloading</span></span>](../../../visual-basic/programming-guide/language-features/procedures/procedure-overloading.md)
- [<span data-ttu-id="828c1-119">Overloads</span><span class="sxs-lookup"><span data-stu-id="828c1-119">Overloads</span></span>](../../../visual-basic/language-reference/modifiers/overloads.md)
