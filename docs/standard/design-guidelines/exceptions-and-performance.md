---
title: Exceptions et performances
ms.date: 10/22/2008
ms.technology: dotnet-standard
helpviewer_keywords:
- tester-doer pattern
- TryParse pattern
- exceptions, throwing
- exceptions, performance
- throwing exceptions, performance
ms.assetid: 3ad6aad9-08e6-4232-b336-0e301f2493e6
author: KrzysztofCwalina
ms.openlocfilehash: f9fe3045d8bd8b4d625c5cd49bc18574ebb740de
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62026430"
---
# <a name="exceptions-and-performance"></a><span data-ttu-id="c5065-102">Exceptions et performances</span><span class="sxs-lookup"><span data-stu-id="c5065-102">Exceptions and Performance</span></span>
<span data-ttu-id="c5065-103">Un problème courant lié aux exceptions est que si les exceptions sont utilisées pour le code qui échoue régulièrement, les performances de l’implémentation sera inacceptables.</span><span class="sxs-lookup"><span data-stu-id="c5065-103">One common concern related to exceptions is that if exceptions are used for code that routinely fails, the performance of the implementation will be unacceptable.</span></span> <span data-ttu-id="c5065-104">Il s’agit d’une inquiétude.</span><span class="sxs-lookup"><span data-stu-id="c5065-104">This is a valid concern.</span></span> <span data-ttu-id="c5065-105">Lorsqu’un membre lève une exception, ses performances peuvent être beaucoup plus lents.</span><span class="sxs-lookup"><span data-stu-id="c5065-105">When a member throws an exception, its performance can be orders of magnitude slower.</span></span> <span data-ttu-id="c5065-106">Toutefois, il est possible d’obtenir de bonnes performances tout en respectant strictement les instructions de l’exception qui interdisent l’utilisation de codes d’erreur.</span><span class="sxs-lookup"><span data-stu-id="c5065-106">However, it is possible to achieve good performance while strictly adhering to the exception guidelines that disallow using error codes.</span></span> <span data-ttu-id="c5065-107">Deux modèles décrits dans cette section proposent des solutions pour ce faire.</span><span class="sxs-lookup"><span data-stu-id="c5065-107">Two patterns described in this section suggest ways to do this.</span></span>  
  
 <span data-ttu-id="c5065-108">**X DO NOT** utiliser des codes d’erreur en raison de problèmes qu’exceptions peuvent affecter négativement les performances.</span><span class="sxs-lookup"><span data-stu-id="c5065-108">**X DO NOT** use error codes because of concerns that exceptions might affect performance negatively.</span></span>  
  
 <span data-ttu-id="c5065-109">Pour améliorer les performances, il est possible d’utiliser le modèle Doer ou le modèle d’essayer d’analyser, décrites dans les deux sections suivantes.</span><span class="sxs-lookup"><span data-stu-id="c5065-109">To improve performance, it is possible to use either the Tester-Doer Pattern or the Try-Parse Pattern, described in the next two sections.</span></span>  
  
## <a name="tester-doer-pattern"></a><span data-ttu-id="c5065-110">Tester-Doer (modèle)</span><span class="sxs-lookup"><span data-stu-id="c5065-110">Tester-Doer Pattern</span></span>  
 <span data-ttu-id="c5065-111">Parfois, les performances d’un membre de la levée d’exceptions peuvent être améliorées en divisant le membre en deux.</span><span class="sxs-lookup"><span data-stu-id="c5065-111">Sometimes performance of an exception-throwing member can be improved by breaking the member into two.</span></span> <span data-ttu-id="c5065-112">Examinons le <xref:System.Collections.Generic.ICollection%601.Add%2A> méthode de la <xref:System.Collections.Generic.ICollection%601> interface.</span><span class="sxs-lookup"><span data-stu-id="c5065-112">Let’s look at the <xref:System.Collections.Generic.ICollection%601.Add%2A> method of the <xref:System.Collections.Generic.ICollection%601> interface.</span></span>  
  
```  
ICollection<int> numbers = ...   
numbers.Add(1);  
```  
  
 <span data-ttu-id="c5065-113">La méthode `Add` lève une exception si la collection est en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="c5065-113">The method `Add` throws if the collection is read-only.</span></span> <span data-ttu-id="c5065-114">Cela peut être un problème de performances dans les scénarios où l’appel de méthode est censé échouent souvent.</span><span class="sxs-lookup"><span data-stu-id="c5065-114">This can be a performance problem in scenarios where the method call is expected to fail often.</span></span> <span data-ttu-id="c5065-115">Un des moyens d’atténuer le problème consiste à vérifier si la collection est accessible en écriture avant d’essayer d’ajouter une valeur.</span><span class="sxs-lookup"><span data-stu-id="c5065-115">One of the ways to mitigate the problem is to test whether the collection is writable before trying to add a value.</span></span>  
  
```  
ICollection<int> numbers = ...   
...  
if(!numbers.IsReadOnly){  
    numbers.Add(1);  
}  
```  
  
 <span data-ttu-id="c5065-116">Le membre utilisé pour tester une condition qui, dans notre exemple, est la propriété `IsReadOnly`, est appelé par le testeur.</span><span class="sxs-lookup"><span data-stu-id="c5065-116">The member used to test a condition, which in our example is the property `IsReadOnly`, is referred to as the tester.</span></span> <span data-ttu-id="c5065-117">Le membre utilisé pour effectuer une opération potentiellement levant, le `Add` méthode dans notre exemple, est appelé à l’exécuteur.</span><span class="sxs-lookup"><span data-stu-id="c5065-117">The member used to perform a potentially throwing operation, the `Add` method in our example, is referred to as the doer.</span></span>  
  
 <span data-ttu-id="c5065-118">**✓ CONSIDER** le modèle utilisateur testeur pour les membres qui peuvent lever des exceptions en commun des scénarios pour éviter les problèmes de performances liés aux exceptions.</span><span class="sxs-lookup"><span data-stu-id="c5065-118">**✓ CONSIDER** the Tester-Doer Pattern for members that might throw exceptions in common scenarios to avoid performance problems related to exceptions.</span></span>  
  
## <a name="try-parse-pattern"></a><span data-ttu-id="c5065-119">Modèle d’analyse de try</span><span class="sxs-lookup"><span data-stu-id="c5065-119">Try-Parse Pattern</span></span>  
 <span data-ttu-id="c5065-120">Pour les API extrêmement sensibles aux performances, un modèle encore plus rapide que le testeur-Doer (modèle) décrit dans la section précédente doit être utilisé.</span><span class="sxs-lookup"><span data-stu-id="c5065-120">For extremely performance-sensitive APIs, an even faster pattern than the Tester-Doer Pattern described in the previous section should be used.</span></span> <span data-ttu-id="c5065-121">Le modèle appelle pour ajuster le nom de membre pour effectuer un test bien défini cas une partie de la sémantique de membre.</span><span class="sxs-lookup"><span data-stu-id="c5065-121">The pattern calls for adjusting the member name to make a well-defined test case a part of the member semantics.</span></span> <span data-ttu-id="c5065-122">Par exemple, <xref:System.DateTime> définit un <xref:System.DateTime.Parse%2A> méthode qui lève une exception en cas de l’analyse d’une chaîne.</span><span class="sxs-lookup"><span data-stu-id="c5065-122">For example, <xref:System.DateTime> defines a <xref:System.DateTime.Parse%2A> method that throws an exception if parsing of a string fails.</span></span> <span data-ttu-id="c5065-123">Il définit également un correspondant <xref:System.DateTime.TryParse%2A> méthode qui tente d’analyser, mais retourne false si l’analyse échoue et retourne le résultat d’une analyse réussie en utilisant un `out` paramètre.</span><span class="sxs-lookup"><span data-stu-id="c5065-123">It also defines a corresponding <xref:System.DateTime.TryParse%2A> method that attempts to parse, but returns false if parsing is unsuccessful and returns the result of a successful parsing using an `out` parameter.</span></span>  
  
```  
public struct DateTime {  
    public static DateTime Parse(string dateTime){   
        ...   
    }  
    public static bool TryParse(string dateTime, out DateTime result){  
        ...  
    }  
}  
```  
  
 <span data-ttu-id="c5065-124">Lorsque vous utilisez ce modèle, il est important de définir les fonctionnalités de try en termes stricts.</span><span class="sxs-lookup"><span data-stu-id="c5065-124">When using this pattern, it is important to define the try functionality in strict terms.</span></span> <span data-ttu-id="c5065-125">Si le membre échoue pour une raison quelconque autre que la tentative de bien définie, le membre doit lève toujours une exception correspondante.</span><span class="sxs-lookup"><span data-stu-id="c5065-125">If the member fails for any reason other than the well-defined try, the member must still throw a corresponding exception.</span></span>  
  
 <span data-ttu-id="c5065-126">**✓ CONSIDER** le modèle d’analyse de Try pour les membres qui peuvent lever des exceptions en commun des scénarios pour éviter les problèmes de performances liés aux exceptions.</span><span class="sxs-lookup"><span data-stu-id="c5065-126">**✓ CONSIDER** the Try-Parse Pattern for members that might throw exceptions in common scenarios to avoid performance problems related to exceptions.</span></span>  
  
 <span data-ttu-id="c5065-127">**✓ DO** utilisent le préfixe « Try » et la valeur booléenne de type de retour pour les méthodes d’implémentation de ce schéma.</span><span class="sxs-lookup"><span data-stu-id="c5065-127">**✓ DO** use the prefix "Try" and Boolean return type for methods implementing this pattern.</span></span>  
  
 <span data-ttu-id="c5065-128">**✓ DO** fournissent un membre levant des exceptions pour chaque membre de l’utilisation du modèle d’analyse de Try.</span><span class="sxs-lookup"><span data-stu-id="c5065-128">**✓ DO** provide an exception-throwing member for each member using the Try-Parse Pattern.</span></span>  
  
 <span data-ttu-id="c5065-129">*Portions © 2005, 2009 Microsoft Corporation. Tous droits réservés.*</span><span class="sxs-lookup"><span data-stu-id="c5065-129">*Portions © 2005, 2009 Microsoft Corporation. All rights reserved.*</span></span>  
  
 <span data-ttu-id="c5065-130">*Réimprimé avec l’autorisation de Pearson éducation, Inc. à partir de [instructions de conception Framework : Conventions, les idiomes et les modèles pour les bibliothèques .NET réutilisable, 2nd Edition](https://www.informit.com/store/framework-design-guidelines-conventions-idioms-and-9780321545619) Krzysztof Cwalina et Brad Abrams, publié le 22 octobre 2008 par Addison-Wesley Professional dans le cadre de la série de développement de Microsoft Windows.*</span><span class="sxs-lookup"><span data-stu-id="c5065-130">*Reprinted by permission of Pearson Education, Inc. from [Framework Design Guidelines: Conventions, Idioms, and Patterns for Reusable .NET Libraries, 2nd Edition](https://www.informit.com/store/framework-design-guidelines-conventions-idioms-and-9780321545619) by Krzysztof Cwalina and Brad Abrams, published Oct 22, 2008 by Addison-Wesley Professional as part of the Microsoft Windows Development Series.*</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="c5065-131">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c5065-131">See also</span></span>

- [<span data-ttu-id="c5065-132">Règles de conception de .NET Framework</span><span class="sxs-lookup"><span data-stu-id="c5065-132">Framework Design Guidelines</span></span>](../../../docs/standard/design-guidelines/index.md)
- [<span data-ttu-id="c5065-133">Instructions de conception pour les exceptions</span><span class="sxs-lookup"><span data-stu-id="c5065-133">Design Guidelines for Exceptions</span></span>](../../../docs/standard/design-guidelines/exceptions.md)
