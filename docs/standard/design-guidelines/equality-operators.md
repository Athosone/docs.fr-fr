---
title: Opérateurs d'égalité
ms.date: 10/22/2008
ms.technology: dotnet-standard
helpviewer_keywords:
- class library design guidelines [.NET Framework], Equals method
- class library design guidelines [.NET Framework], equality operator
- equality operator (==) [.NET Framework]
- Equals method
- == operator (equality) [.NET Framework]
ms.assetid: bc496a91-fefb-4ce0-ab4c-61f09964119a
author: KrzysztofCwalina
ms.openlocfilehash: ef1a0aff1ac59434d9d9a6f0371bf236f637050e
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61960329"
---
# <a name="equality-operators"></a><span data-ttu-id="2aae4-102">Opérateurs d'égalité</span><span class="sxs-lookup"><span data-stu-id="2aae4-102">Equality Operators</span></span>
<span data-ttu-id="2aae4-103">Cette section traite de surcharge les opérateurs d’égalité et fait référence à `operator==` et `operator!=` en tant que les opérateurs d’égalité.</span><span class="sxs-lookup"><span data-stu-id="2aae4-103">This section discusses overloading equality operators and refers to `operator==` and `operator!=` as equality operators.</span></span>  
  
 <span data-ttu-id="2aae4-104">**X DO NOT** un des opérateurs d’égalité et pas dans l’autre surcharge.</span><span class="sxs-lookup"><span data-stu-id="2aae4-104">**X DO NOT** overload one of the equality operators and not the other.</span></span>  
  
 <span data-ttu-id="2aae4-105">**✓ DO** vous assurer que <xref:System.Object.Equals%2A?displayProperty=nameWithType> et les opérateurs d’égalité ont exactement la même sémantique et des caractéristiques similaires.</span><span class="sxs-lookup"><span data-stu-id="2aae4-105">**✓ DO** ensure that <xref:System.Object.Equals%2A?displayProperty=nameWithType> and the equality operators have exactly the same semantics and similar performance characteristics.</span></span>  
  
 <span data-ttu-id="2aae4-106">Cela signifie souvent que `Object.Equals` doit être remplacée lorsque les opérateurs d’égalité sont surchargés.</span><span class="sxs-lookup"><span data-stu-id="2aae4-106">This often means that `Object.Equals` needs to be overridden when the equality operators are overloaded.</span></span>  
  
 <span data-ttu-id="2aae4-107">**X AVOID** lever des exceptions à partir des opérateurs d’égalité.</span><span class="sxs-lookup"><span data-stu-id="2aae4-107">**X AVOID** throwing exceptions from equality operators.</span></span>  
  
 <span data-ttu-id="2aae4-108">Par exemple, retourner false si l’un des arguments est null au lieu de lever `NullReferenceException`.</span><span class="sxs-lookup"><span data-stu-id="2aae4-108">For example, return false if one of the arguments is null instead of throwing `NullReferenceException`.</span></span>  
  
## <a name="equality-operators-on-value-types"></a><span data-ttu-id="2aae4-109">Opérateurs d’égalité sur les Types valeur</span><span class="sxs-lookup"><span data-stu-id="2aae4-109">Equality Operators on Value Types</span></span>  
 <span data-ttu-id="2aae4-110">**✓ DO** surcharger les opérateurs d’égalité sur les types valeur, si l’égalité est explicite.</span><span class="sxs-lookup"><span data-stu-id="2aae4-110">**✓ DO** overload the equality operators on value types, if equality is meaningful.</span></span>  
  
 <span data-ttu-id="2aae4-111">Dans la plupart des langages de programmation, il n’existe aucune implémentation par défaut de `operator==` pour les types valeur.</span><span class="sxs-lookup"><span data-stu-id="2aae4-111">In most programming languages, there is no default implementation of `operator==` for value types.</span></span>  
  
## <a name="equality-operators-on-reference-types"></a><span data-ttu-id="2aae4-112">Opérateurs d’égalité sur les Types référence</span><span class="sxs-lookup"><span data-stu-id="2aae4-112">Equality Operators on Reference Types</span></span>  
 <span data-ttu-id="2aae4-113">**X AVOID** la surcharge des opérateurs d’égalité sur les types référence mutables.</span><span class="sxs-lookup"><span data-stu-id="2aae4-113">**X AVOID** overloading equality operators on mutable reference types.</span></span>  
  
 <span data-ttu-id="2aae4-114">De nombreux langages ont des opérateurs d’égalité intégrés pour les types référence.</span><span class="sxs-lookup"><span data-stu-id="2aae4-114">Many languages have built-in equality operators for reference types.</span></span> <span data-ttu-id="2aae4-115">Les opérateurs intégrés implémentent généralement l’égalité de référence et de nombreux développeurs sont surpris lorsque le comportement par défaut est modifié à l’égalité de valeur.</span><span class="sxs-lookup"><span data-stu-id="2aae4-115">The built-in operators usually implement the reference equality, and many developers are surprised when the default behavior is changed to the value equality.</span></span>  
  
 <span data-ttu-id="2aae4-116">Ce problème est atténué pour les types référence immuable, car l’immuabilité rend beaucoup plus difficile à remarquer la différence entre une égalité de référence et l’égalité des valeurs.</span><span class="sxs-lookup"><span data-stu-id="2aae4-116">This problem is mitigated for immutable reference types because immutability makes it much harder to notice the difference between reference equality and value equality.</span></span>  
  
 <span data-ttu-id="2aae4-117">**X AVOID** surcharge des opérateurs d’égalité sur les types référence si l’implémentation est beaucoup plus lente que celui de l’égalité des références.</span><span class="sxs-lookup"><span data-stu-id="2aae4-117">**X AVOID** overloading equality operators on reference types if the implementation would be significantly slower than that of reference equality.</span></span>  
  
 <span data-ttu-id="2aae4-118">*Portions © 2005, 2009 Microsoft Corporation. Tous droits réservés.*</span><span class="sxs-lookup"><span data-stu-id="2aae4-118">*Portions © 2005, 2009 Microsoft Corporation. All rights reserved.*</span></span>  
  
 <span data-ttu-id="2aae4-119">*Réimprimé avec l’autorisation de Pearson éducation, Inc. à partir de [instructions de conception Framework : Conventions, les idiomes et les modèles pour les bibliothèques .NET réutilisable, 2nd Edition](https://www.informit.com/store/framework-design-guidelines-conventions-idioms-and-9780321545619) Krzysztof Cwalina et Brad Abrams, publié le 22 octobre 2008 par Addison-Wesley Professional dans le cadre de la série de développement de Microsoft Windows.*</span><span class="sxs-lookup"><span data-stu-id="2aae4-119">*Reprinted by permission of Pearson Education, Inc. from [Framework Design Guidelines: Conventions, Idioms, and Patterns for Reusable .NET Libraries, 2nd Edition](https://www.informit.com/store/framework-design-guidelines-conventions-idioms-and-9780321545619) by Krzysztof Cwalina and Brad Abrams, published Oct 22, 2008 by Addison-Wesley Professional as part of the Microsoft Windows Development Series.*</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="2aae4-120">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="2aae4-120">See also</span></span>

- [<span data-ttu-id="2aae4-121">Règles de conception de .NET Framework</span><span class="sxs-lookup"><span data-stu-id="2aae4-121">Framework Design Guidelines</span></span>](../../../docs/standard/design-guidelines/index.md)
- [<span data-ttu-id="2aae4-122">Indications relatives à l’utilisation</span><span class="sxs-lookup"><span data-stu-id="2aae4-122">Usage Guidelines</span></span>](../../../docs/standard/design-guidelines/usage-guidelines.md)
