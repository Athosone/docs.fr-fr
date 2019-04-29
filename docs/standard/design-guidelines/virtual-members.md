---
title: Membres virtuels
ms.date: 10/22/2008
ms.technology: dotnet-standard
helpviewer_keywords:
- overridable members
- virtual members
- members [.NET Framework], virtual
ms.assetid: 8ff4eb97-0364-43ec-8a02-934b5cd94d19
author: KrzysztofCwalina
ms.openlocfilehash: 4943ddcdf1bc4e3e32c8d664cbcc5c50ae3959bd
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61778701"
---
# <a name="virtual-members"></a><span data-ttu-id="0fc09-102">Membres virtuels</span><span class="sxs-lookup"><span data-stu-id="0fc09-102">Virtual Members</span></span>
<span data-ttu-id="0fc09-103">Membres virtuels peuvent être remplacées, ce qui modifie le comportement de la sous-classe.</span><span class="sxs-lookup"><span data-stu-id="0fc09-103">Virtual members can be overridden, thus changing the behavior of the subclass.</span></span> <span data-ttu-id="0fc09-104">Ils sont assez semblables aux rappels en termes de l’extensibilité qu’ils fournissent, mais qu’ils sont mieux en termes de performances de l’exécution et la consommation de mémoire.</span><span class="sxs-lookup"><span data-stu-id="0fc09-104">They are quite similar to callbacks in terms of the extensibility they provide, but they are better in terms of execution performance and memory consumption.</span></span> <span data-ttu-id="0fc09-105">En outre, les membres virtuels sembler plus naturelles dans les scénarios qui nécessitent la création de type d’un type existant (spécialisation) spécial.</span><span class="sxs-lookup"><span data-stu-id="0fc09-105">Also, virtual members feel more natural in scenarios that require creating a special kind of an existing type (specialization).</span></span>  
  
 <span data-ttu-id="0fc09-106">Membres virtuels plus performant que les rappels et les événements, mais n’effectuent pas de meilleures performances que les méthodes non virtuelles.</span><span class="sxs-lookup"><span data-stu-id="0fc09-106">Virtual members perform better than callbacks and events, but do not perform better than non-virtual methods.</span></span>  
  
 <span data-ttu-id="0fc09-107">Le principal inconvénient de membres virtuels est que le comportement d’un membre virtuel peut uniquement être modifié au moment de la compilation.</span><span class="sxs-lookup"><span data-stu-id="0fc09-107">The main disadvantage of virtual members is that the behavior of a virtual member can only be modified at the time of compilation.</span></span> <span data-ttu-id="0fc09-108">Le comportement d’un rappel peut être modifié lors de l’exécution.</span><span class="sxs-lookup"><span data-stu-id="0fc09-108">The behavior of a callback can be modified at runtime.</span></span>  
  
 <span data-ttu-id="0fc09-109">Les membres virtuels, telles que des rappels (et peut-être plusieurs rappels) sont coûteuses à concevoir, tester et mettre en place car un appel à un membre virtuel peut être substitué de manière imprévisible et peut exécuter du code arbitraire.</span><span class="sxs-lookup"><span data-stu-id="0fc09-109">Virtual members, like callbacks (and maybe more than callbacks), are costly to design, test, and maintain because any call to a virtual member can be overridden in unpredictable ways and can execute arbitrary code.</span></span> <span data-ttu-id="0fc09-110">En outre, plus beaucoup d’efforts est généralement requis pour définir clairement le contrat de membres virtuels, ce qui augmente le coût de conception et de les documenter.</span><span class="sxs-lookup"><span data-stu-id="0fc09-110">Also, much more effort is usually required to clearly define the contract of virtual members, so the cost of designing and documenting them is higher.</span></span>  
  
 <span data-ttu-id="0fc09-111">**X DO NOT** rendre les membres virtuels sauf si vous avez une bonne raison à cela et que vous connaissez tous les coûts liés à la conception, de test et de maintenance des membres virtuels.</span><span class="sxs-lookup"><span data-stu-id="0fc09-111">**X DO NOT** make members virtual unless you have a good reason to do so and you are aware of all the costs related to designing, testing, and maintaining virtual members.</span></span>  
  
 <span data-ttu-id="0fc09-112">Membres virtuels sont moins indulgent en termes de modifications qui peuvent être apportées à leur sans perdre la compatibilité.</span><span class="sxs-lookup"><span data-stu-id="0fc09-112">Virtual members are less forgiving in terms of changes that can be made to them without breaking compatibility.</span></span> <span data-ttu-id="0fc09-113">En outre, ils sont plus lents que les membres non virtuelle, principalement parce que les appels aux membres virtuels ne sont pas inline.</span><span class="sxs-lookup"><span data-stu-id="0fc09-113">Also, they are slower than non-virtual members, mostly because calls to virtual members are not inlined.</span></span>  
  
 <span data-ttu-id="0fc09-114">**✓ CONSIDER** limiter l’extensibilité à celles qui sont absolument nécessaires.</span><span class="sxs-lookup"><span data-stu-id="0fc09-114">**✓ CONSIDER** limiting extensibility to only what is absolutely necessary.</span></span>  
  
 <span data-ttu-id="0fc09-115">**✓ DO** accessibilité protégée préférer une accessibilité publique pour les membres virtuels.</span><span class="sxs-lookup"><span data-stu-id="0fc09-115">**✓ DO** prefer protected accessibility over public accessibility for virtual members.</span></span> <span data-ttu-id="0fc09-116">Les membres publics doivent fournir l’extensibilité (si nécessaire) en appelant un membre virtuel protégé.</span><span class="sxs-lookup"><span data-stu-id="0fc09-116">Public members should provide extensibility (if required) by calling into a protected virtual member.</span></span>  
  
 <span data-ttu-id="0fc09-117">Les membres publics d’une classe doivent fournir l’ensemble approprié de fonctionnalités pour les consommateurs directs de cette classe.</span><span class="sxs-lookup"><span data-stu-id="0fc09-117">The public members of a class should provide the right set of functionality for direct consumers of that class.</span></span> <span data-ttu-id="0fc09-118">Membres virtuels sont conçus pour être substitué dans les sous-classes et accessibilité protégée est un excellent moyen pour définir l’étendue tous les points d’extension virtuel où ils peuvent être utilisés.</span><span class="sxs-lookup"><span data-stu-id="0fc09-118">Virtual members are designed to be overridden in subclasses, and protected accessibility is a great way to scope all virtual extensibility points to where they can be used.</span></span>  
  
 <span data-ttu-id="0fc09-119">*Portions © 2005, 2009 Microsoft Corporation. Tous droits réservés.*</span><span class="sxs-lookup"><span data-stu-id="0fc09-119">*Portions © 2005, 2009 Microsoft Corporation. All rights reserved.*</span></span>  
  
 <span data-ttu-id="0fc09-120">*Réimprimé avec l’autorisation de Pearson éducation, Inc. à partir de [instructions de conception Framework : Conventions, les idiomes et les modèles pour les bibliothèques .NET réutilisable, 2nd Edition](https://www.informit.com/store/framework-design-guidelines-conventions-idioms-and-9780321545619) Krzysztof Cwalina et Brad Abrams, publié le 22 octobre 2008 par Addison-Wesley Professional dans le cadre de la série de développement de Microsoft Windows.*</span><span class="sxs-lookup"><span data-stu-id="0fc09-120">*Reprinted by permission of Pearson Education, Inc. from [Framework Design Guidelines: Conventions, Idioms, and Patterns for Reusable .NET Libraries, 2nd Edition](https://www.informit.com/store/framework-design-guidelines-conventions-idioms-and-9780321545619) by Krzysztof Cwalina and Brad Abrams, published Oct 22, 2008 by Addison-Wesley Professional as part of the Microsoft Windows Development Series.*</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="0fc09-121">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0fc09-121">See also</span></span>

- [<span data-ttu-id="0fc09-122">Règles de conception de .NET Framework</span><span class="sxs-lookup"><span data-stu-id="0fc09-122">Framework Design Guidelines</span></span>](../../../docs/standard/design-guidelines/index.md)
- [<span data-ttu-id="0fc09-123">Conception en vue de l’extensibilité</span><span class="sxs-lookup"><span data-stu-id="0fc09-123">Designing for Extensibility</span></span>](../../../docs/standard/design-guidelines/designing-for-extensibility.md)
