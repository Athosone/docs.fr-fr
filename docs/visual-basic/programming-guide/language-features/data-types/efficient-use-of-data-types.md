---
title: Utilisation efficace des types de données (Visual Basic)
ms.date: 07/20/2015
helpviewer_keywords:
- performance, data type efficiency
- data types [Visual Basic], weak typing
- AscW function [Visual Basic], preferred to Asc
- data types [Visual Basic], using efficiently
- optimization [Visual Basic], data types
- data types [Visual Basic], strong typing
- strong typing
- typing, strong
- data types [Visual Basic], optimizing
- ChrW function [Visual Basic], preferred to Chr
ms.assetid: 28f5e4ba-ec24-4f37-b90a-e8ee822f778a
ms.openlocfilehash: 0b517bca3a9e296eb891e30df91c1d32eb357432
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61907216"
---
# <a name="efficient-use-of-data-types-visual-basic"></a><span data-ttu-id="c14f9-102">Utilisation efficace des types de données (Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="c14f9-102">Efficient Use of Data Types (Visual Basic)</span></span>
<span data-ttu-id="c14f9-103">Variables non déclarées et les variables déclarées sans type de données sont voient attribuer le `Object` type de données.</span><span class="sxs-lookup"><span data-stu-id="c14f9-103">Undeclared variables and variables declared without a data type are assigned the `Object` data type.</span></span> <span data-ttu-id="c14f9-104">Cela rend plus facile d’écrire rapidement des programmes, mais il peut les rendre s’exécute plus lentement.</span><span class="sxs-lookup"><span data-stu-id="c14f9-104">This makes it easy to write programs quickly, but it can cause them to execute more slowly.</span></span>  
  
## <a name="strong-typing"></a><span data-ttu-id="c14f9-105">Typage fort</span><span class="sxs-lookup"><span data-stu-id="c14f9-105">Strong Typing</span></span>  
 <span data-ttu-id="c14f9-106">Spécifier les types de données pour toutes les variables est appelé *un typage fort*.</span><span class="sxs-lookup"><span data-stu-id="c14f9-106">Specifying data types for all your variables is known as *strong typing*.</span></span> <span data-ttu-id="c14f9-107">À l’aide d’un typage fort présente plusieurs avantages :</span><span class="sxs-lookup"><span data-stu-id="c14f9-107">Using strong typing has several advantages:</span></span>  
  
- <span data-ttu-id="c14f9-108">Il permet la prise en charge IntelliSense pour vos variables.</span><span class="sxs-lookup"><span data-stu-id="c14f9-108">It enables IntelliSense support for your variables.</span></span> <span data-ttu-id="c14f9-109">Cela vous permet de vous permet de voir leurs propriétés et autres membres en cours de frappe dans le code.</span><span class="sxs-lookup"><span data-stu-id="c14f9-109">This allows you to see their properties and other members as you type in the code.</span></span>  
  
- <span data-ttu-id="c14f9-110">Il tire parti de la vérification du type du compilateur.</span><span class="sxs-lookup"><span data-stu-id="c14f9-110">It takes advantage of compiler type checking.</span></span> <span data-ttu-id="c14f9-111">Il intercepte les instructions qui peuvent échouer au moment de l’exécution en raison d’erreurs de dépassement de capacité.</span><span class="sxs-lookup"><span data-stu-id="c14f9-111">This catches statements that can fail at run time due to errors such as overflow.</span></span> <span data-ttu-id="c14f9-112">Il intercepte également les appels aux méthodes sur des objets qui ne les prennent pas en charge.</span><span class="sxs-lookup"><span data-stu-id="c14f9-112">It also catches calls to methods on objects that do not support them.</span></span>  
  
- <span data-ttu-id="c14f9-113">Il en résulte dans une exécution plus rapide de votre code.</span><span class="sxs-lookup"><span data-stu-id="c14f9-113">It results in faster execution of your code.</span></span>  
  
## <a name="most-efficient-data-types"></a><span data-ttu-id="c14f9-114">Types de données plus efficaces</span><span class="sxs-lookup"><span data-stu-id="c14f9-114">Most Efficient Data Types</span></span>  
 <span data-ttu-id="c14f9-115">Pour les variables qui ne contiennent jamais de fractions, les types de données intégraux sont plus efficaces que les types non intégraux.</span><span class="sxs-lookup"><span data-stu-id="c14f9-115">For variables that never contain fractions, the integral data types are more efficient than the nonintegral types.</span></span> <span data-ttu-id="c14f9-116">En Visual Basic, `Integer` et `UInteger` sont les types numériques plus efficaces.</span><span class="sxs-lookup"><span data-stu-id="c14f9-116">In Visual Basic, `Integer` and `UInteger` are the most efficient numeric types.</span></span>  
  
 <span data-ttu-id="c14f9-117">Pour les nombres fractionnaires, `Double` est le type de données plus efficace, car les processeurs sur les plateformes actuelles exécutent des opérations à virgule flottante à double précision.</span><span class="sxs-lookup"><span data-stu-id="c14f9-117">For fractional numbers, `Double` is the most efficient data type, because the processors on current platforms perform floating-point operations in double precision.</span></span> <span data-ttu-id="c14f9-118">Toutefois, les opérations avec `Double` ne sont pas aussi rapides qu’avec les types intégraux tels que `Integer`.</span><span class="sxs-lookup"><span data-stu-id="c14f9-118">However, operations with `Double` are not as fast as with the integral types such as `Integer`.</span></span>  
  
## <a name="specifying-data-type"></a><span data-ttu-id="c14f9-119">Spécifiant le Type de données</span><span class="sxs-lookup"><span data-stu-id="c14f9-119">Specifying Data Type</span></span>  
 <span data-ttu-id="c14f9-120">Utilisez le [instruction Dim](../../../../visual-basic/language-reference/statements/dim-statement.md) pour déclarer une variable d’un type spécifique.</span><span class="sxs-lookup"><span data-stu-id="c14f9-120">Use the [Dim Statement](../../../../visual-basic/language-reference/statements/dim-statement.md) to declare a variable of a specific type.</span></span> <span data-ttu-id="c14f9-121">Vous pouvez spécifier simultanément son niveau d’accès à l’aide de la [Public](../../../../visual-basic/language-reference/modifiers/public.md), [protégé](../../../../visual-basic/language-reference/modifiers/protected.md), [Friend](../../../../visual-basic/language-reference/modifiers/friend.md), ou [privé](../../../../visual-basic/language-reference/modifiers/private.md) mot clé, comme dans le exemple suivant.</span><span class="sxs-lookup"><span data-stu-id="c14f9-121">You can simultaneously specify its access level by using the [Public](../../../../visual-basic/language-reference/modifiers/public.md), [Protected](../../../../visual-basic/language-reference/modifiers/protected.md), [Friend](../../../../visual-basic/language-reference/modifiers/friend.md), or [Private](../../../../visual-basic/language-reference/modifiers/private.md) keyword, as in the following example.</span></span>  
  
```  
Private x As Double  
Protected s As String  
```  
  
## <a name="character-conversion"></a><span data-ttu-id="c14f9-122">Conversion de caractères</span><span class="sxs-lookup"><span data-stu-id="c14f9-122">Character Conversion</span></span>  
 <span data-ttu-id="c14f9-123">Le `AscW` et `ChrW` fonctions opèrent en Unicode.</span><span class="sxs-lookup"><span data-stu-id="c14f9-123">The `AscW` and `ChrW` functions operate in Unicode.</span></span> <span data-ttu-id="c14f9-124">Vous devez les utiliser de préférence à `Asc` et `Chr`, qui doit traduire dans et hors d’Unicode.</span><span class="sxs-lookup"><span data-stu-id="c14f9-124">You should use them in preference to `Asc` and `Chr`, which must translate into and out of Unicode.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="c14f9-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c14f9-125">See also</span></span>

- <xref:Microsoft.VisualBasic.Strings.Asc%2A>
- <xref:Microsoft.VisualBasic.Strings.AscW%2A>
- <xref:Microsoft.VisualBasic.Strings.Chr%2A>
- <xref:Microsoft.VisualBasic.Strings.ChrW%2A>
- [<span data-ttu-id="c14f9-126">Types de données</span><span class="sxs-lookup"><span data-stu-id="c14f9-126">Data Types</span></span>](../../../../visual-basic/programming-guide/language-features/data-types/index.md)
- [<span data-ttu-id="c14f9-127">Types de données numériques</span><span class="sxs-lookup"><span data-stu-id="c14f9-127">Numeric Data Types</span></span>](../../../../visual-basic/programming-guide/language-features/data-types/numeric-data-types.md)
- [<span data-ttu-id="c14f9-128">Déclaration de variable</span><span class="sxs-lookup"><span data-stu-id="c14f9-128">Variable Declaration</span></span>](../../../../visual-basic/programming-guide/language-features/variables/variable-declaration.md)
- [<span data-ttu-id="c14f9-129">Utilisation de la fonctionnalité IntelliSense</span><span class="sxs-lookup"><span data-stu-id="c14f9-129">Using IntelliSense</span></span>](/visualstudio/ide/using-intellisense)
