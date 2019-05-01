---
title: Règles de conception de .NET Framework
ms.date: 10/22/2008
ms.technology: dotnet-standard
helpviewer_keywords:
- libraries, .NET Framework class library
- class library design guidelines [.NET Framework], about
- class library design guidelines [.NET Framework]
ms.assetid: 5fbcaf4f-ea2a-4d20-b0d6-e61dee202b4b
author: KrzysztofCwalina
ms.openlocfilehash: c20430f9cdcd71cc2e178d38aeed48f9fa4e75c5
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62026378"
---
# <a name="framework-design-guidelines"></a><span data-ttu-id="f489e-102">Règles de conception de .NET Framework</span><span class="sxs-lookup"><span data-stu-id="f489e-102">Framework Design Guidelines</span></span>
<span data-ttu-id="f489e-103">Cette section fournit des instructions pour la conception de bibliothèques qui étendent et interagissent avec le .NET Framework.</span><span class="sxs-lookup"><span data-stu-id="f489e-103">This section provides guidelines for designing libraries that extend and interact with the .NET Framework.</span></span> <span data-ttu-id="f489e-104">L’objectif est d’aider les concepteurs de bibliothèques à garantir la cohérence d’API et la facilité d’utilisation en fournissant un modèle de programmation unifié qui est indépendant du langage de programmation utilisé pour le développement.</span><span class="sxs-lookup"><span data-stu-id="f489e-104">The goal is to help library designers ensure API consistency and ease of use by providing a unified programming model that is independent of the programming language used for development.</span></span> <span data-ttu-id="f489e-105">Nous vous recommandons de suivre ces instructions de conception lors du développement de classes et composants qui étendent .NET Framework.</span><span class="sxs-lookup"><span data-stu-id="f489e-105">We recommend that you follow these design guidelines when developing classes and components that extend the .NET Framework.</span></span> <span data-ttu-id="f489e-106">Conception de la bibliothèque incohérent avoir un impact négatif la productivité des développeurs et décourage adoption.</span><span class="sxs-lookup"><span data-stu-id="f489e-106">Inconsistent library design adversely affects developer productivity and discourages adoption.</span></span>  
  
 <span data-ttu-id="f489e-107">Les directives sont organisées en tant que recommandation simple avec les termes du contrat le préfixe `Do`, `Consider`, `Avoid`, et `Do not`.</span><span class="sxs-lookup"><span data-stu-id="f489e-107">The guidelines are organized as simple recommendations prefixed with the terms `Do`, `Consider`, `Avoid`, and `Do not`.</span></span> <span data-ttu-id="f489e-108">Ces instructions sont destinées à aider les concepteurs de bibliothèque de classes à comprendre les compromis entre différentes solutions.</span><span class="sxs-lookup"><span data-stu-id="f489e-108">These guidelines are intended to help class library designers understand the trade-offs between different solutions.</span></span> <span data-ttu-id="f489e-109">Il existe peut-être enfreindre bon design de bibliothèque que vous ces instructions de conception.</span><span class="sxs-lookup"><span data-stu-id="f489e-109">There might be situations where good library design requires that you violate these design guidelines.</span></span> <span data-ttu-id="f489e-110">Ce cas est rare, et il est important que vous avez une raison claire et intéressante pour votre décision.</span><span class="sxs-lookup"><span data-stu-id="f489e-110">Such cases should be rare, and it is important that you have a clear and compelling reason for your decision.</span></span>  
  
 <span data-ttu-id="f489e-111">Ces instructions sont extraites de l’ouvrage *instructions de conception Framework : Conventions, les idiomes et les modèles pour les bibliothèques .NET réutilisables, 2nd Edition*, Krzysztof Cwalina et Brad Abrams.</span><span class="sxs-lookup"><span data-stu-id="f489e-111">These guidelines are excerpted from the book *Framework Design Guidelines: Conventions, Idioms, and Patterns for Reusable .NET Libraries, 2nd Edition*, by Krzysztof Cwalina and Brad Abrams.</span></span>  
  
## <a name="in-this-section"></a><span data-ttu-id="f489e-112">Dans cette section</span><span class="sxs-lookup"><span data-stu-id="f489e-112">In This Section</span></span>  
 [<span data-ttu-id="f489e-113">Directives de nommage</span><span class="sxs-lookup"><span data-stu-id="f489e-113">Naming Guidelines</span></span>](../../../docs/standard/design-guidelines/naming-guidelines.md)  
 <span data-ttu-id="f489e-114">Fournit des instructions pour nommer les assemblys, espaces de noms, types et membres dans les bibliothèques de classes.</span><span class="sxs-lookup"><span data-stu-id="f489e-114">Provides guidelines for naming assemblies, namespaces, types, and members in class libraries.</span></span>  
  
 [<span data-ttu-id="f489e-115">Instructions pour la conception des types</span><span class="sxs-lookup"><span data-stu-id="f489e-115">Type Design Guidelines</span></span>](../../../docs/standard/design-guidelines/type.md)  
 <span data-ttu-id="f489e-116">Fournit des instructions pour l’utilisation des classes statiques et abstraites, des interfaces, des énumérations, des structures et autres types.</span><span class="sxs-lookup"><span data-stu-id="f489e-116">Provides guidelines for using static and abstract classes, interfaces, enumerations, structures, and other types.</span></span>  
  
 [<span data-ttu-id="f489e-117">Instructions de conception des membres</span><span class="sxs-lookup"><span data-stu-id="f489e-117">Member Design Guidelines</span></span>](../../../docs/standard/design-guidelines/member.md)  
 <span data-ttu-id="f489e-118">Fournit des instructions pour la conception et à l’aide des propriétés, méthodes, constructeurs, champs, événements, opérateurs et paramètres.</span><span class="sxs-lookup"><span data-stu-id="f489e-118">Provides guidelines for designing and using properties, methods, constructors, fields, events, operators, and parameters.</span></span>  
  
 [<span data-ttu-id="f489e-119">Conception en vue de l’extensibilité</span><span class="sxs-lookup"><span data-stu-id="f489e-119">Designing for Extensibility</span></span>](../../../docs/standard/design-guidelines/designing-for-extensibility.md)  
 <span data-ttu-id="f489e-120">Mécanismes d’extensibilité tels que le sous-classement, à l’aide d’événements, les membres virtuels et les rappels et explique comment choisir les mécanismes qui répondent le mieux aux exigences de votre infrastructure.</span><span class="sxs-lookup"><span data-stu-id="f489e-120">Discusses extensibility mechanisms such as subclassing, using events, virtual members, and callbacks, and explains how to choose the mechanisms that best meet your framework's requirements.</span></span>  
  
 [<span data-ttu-id="f489e-121">Instructions de conception pour les exceptions</span><span class="sxs-lookup"><span data-stu-id="f489e-121">Design Guidelines for Exceptions</span></span>](../../../docs/standard/design-guidelines/exceptions.md)  
 <span data-ttu-id="f489e-122">Décrit les instructions de conception pour la conception, la levée et l’interception des exceptions.</span><span class="sxs-lookup"><span data-stu-id="f489e-122">Describes design guidelines for designing, throwing, and catching exceptions.</span></span>  
  
 [<span data-ttu-id="f489e-123">Indications relatives à l’utilisation</span><span class="sxs-lookup"><span data-stu-id="f489e-123">Usage Guidelines</span></span>](../../../docs/standard/design-guidelines/usage-guidelines.md)  
 <span data-ttu-id="f489e-124">Fournit des instructions pour l’utilisation des types courants tels que des tableaux, des attributs et des collections, prenant en charge la sérialisation et la surcharge des opérateurs d’égalité.</span><span class="sxs-lookup"><span data-stu-id="f489e-124">Describes guidelines for using common types such as arrays, attributes, and collections, supporting serialization, and overloading equality operators.</span></span>  
  
 [<span data-ttu-id="f489e-125">Modèles de design courants</span><span class="sxs-lookup"><span data-stu-id="f489e-125">Common Design Patterns</span></span>](../../../docs/standard/design-guidelines/common-design-patterns.md)  
 <span data-ttu-id="f489e-126">Fournit des instructions pour le choix et l’implémentation des propriétés de dépendance.</span><span class="sxs-lookup"><span data-stu-id="f489e-126">Provides guidelines for choosing and implementing dependency properties.</span></span>  
  
 <span data-ttu-id="f489e-127">*Portions © 2005, 2009 Microsoft Corporation. Tous droits réservés.*</span><span class="sxs-lookup"><span data-stu-id="f489e-127">*Portions © 2005, 2009 Microsoft Corporation. All rights reserved.*</span></span>  
  
 <span data-ttu-id="f489e-128">*Réimprimé avec l’autorisation de Pearson éducation, Inc. à partir de [instructions de conception Framework : Conventions, les idiomes et les modèles pour les bibliothèques .NET réutilisable, 2nd Edition](https://www.informit.com/store/framework-design-guidelines-conventions-idioms-and-9780321545619) Krzysztof Cwalina et Brad Abrams, publié le 22 octobre 2008 par Addison-Wesley Professional dans le cadre de la série de développement de Microsoft Windows.*</span><span class="sxs-lookup"><span data-stu-id="f489e-128">*Reprinted by permission of Pearson Education, Inc. from [Framework Design Guidelines: Conventions, Idioms, and Patterns for Reusable .NET Libraries, 2nd Edition](https://www.informit.com/store/framework-design-guidelines-conventions-idioms-and-9780321545619) by Krzysztof Cwalina and Brad Abrams, published Oct 22, 2008 by Addison-Wesley Professional as part of the Microsoft Windows Development Series.*</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="f489e-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f489e-129">See also</span></span>

- [<span data-ttu-id="f489e-130">Vue d’ensemble</span><span class="sxs-lookup"><span data-stu-id="f489e-130">Overview</span></span>](../../../docs/framework/get-started/overview.md)
- [<span data-ttu-id="f489e-131">Guide de développement</span><span class="sxs-lookup"><span data-stu-id="f489e-131">Development Guide</span></span>](../../../docs/framework/development-guide.md)
