---
title: x:Code, type XAML intrinsèque
ms.date: 03/30/2017
f1_keywords:
- Code
- x:Code
- xCode
helpviewer_keywords:
- Code directive in XAML [XAML Services]
- x:Code XAML directive element [XAML Services]
- XAML [XAML Services], x:Code directive element
ms.assetid: 87986b13-1a2e-4830-ae36-15f9dc5629e8
ms.openlocfilehash: 7bb78b05be7b3edc4471bc276010eabd92a07a14
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59145234"
---
# <a name="xcode-intrinsic-xaml-type"></a><span data-ttu-id="0a3ab-102">x:Code, type XAML intrinsèque</span><span class="sxs-lookup"><span data-stu-id="0a3ab-102">x:Code Intrinsic XAML Type</span></span>
<span data-ttu-id="0a3ab-103">Permet le placement du code au sein d’une production XAML.</span><span class="sxs-lookup"><span data-stu-id="0a3ab-103">Allows placement of code within a XAML production.</span></span> <span data-ttu-id="0a3ab-104">Ce code peut être compilé par une implémentation de processeur XAML qui compile XAML, ou à gauche dans la production XAML pour les utilisations ultérieures comme interprétation par un runtime.</span><span class="sxs-lookup"><span data-stu-id="0a3ab-104">Such code can either be compiled by any XAML processor implementation that compiles XAML, or left in the XAML production for later uses such as interpretation by a runtime.</span></span>  
  
## <a name="xaml-object-element-usage"></a><span data-ttu-id="0a3ab-105">Utilisation d'éléments objet XAML</span><span class="sxs-lookup"><span data-stu-id="0a3ab-105">XAML Object Element Usage</span></span>  
  
```  
<x:Code>  
   // code instructions, usually enclosed by CDATA...  
</x:Code>  
```  
  
## <a name="remarks"></a><span data-ttu-id="0a3ab-106">Notes</span><span class="sxs-lookup"><span data-stu-id="0a3ab-106">Remarks</span></span>  
 <span data-ttu-id="0a3ab-107">Le code dans le `x:Code` élément de directive XAML est toujours interprété dans l’espace de noms XML général et les espaces de noms XAML fourni.</span><span class="sxs-lookup"><span data-stu-id="0a3ab-107">The code within the `x:Code` XAML directive element is still interpreted within the general XML namespace and the XAML namespaces provided.</span></span> <span data-ttu-id="0a3ab-108">Par conséquent, il est généralement nécessaire de placer le code utilisé pour `x:Code` à l’intérieur d’un `CDATA` segment.</span><span class="sxs-lookup"><span data-stu-id="0a3ab-108">Therefore, it is usually necessary to enclose the code used for `x:Code` inside a `CDATA` segment.</span></span>  
  
 <span data-ttu-id="0a3ab-109">`x:Code` n’est pas autorisé pour tous les mécanismes de déploiement d’une production XAML.</span><span class="sxs-lookup"><span data-stu-id="0a3ab-109">`x:Code` is not permitted for all possible deployment mechanisms of a XAML production.</span></span> <span data-ttu-id="0a3ab-110">Le code doit être compilé dans les infrastructures spécifiques (par exemple WPF).</span><span class="sxs-lookup"><span data-stu-id="0a3ab-110">In specific frameworks (for example WPF) the code must be compiled.</span></span> <span data-ttu-id="0a3ab-111">Dans d’autres infrastructures, `x:Code` utilisation peut être interdite en général.</span><span class="sxs-lookup"><span data-stu-id="0a3ab-111">In other frameworks, `x:Code` usage might be generally disallowed.</span></span>  
  
 <span data-ttu-id="0a3ab-112">Pour les infrastructures qui autorisent managé `x:Code` de contenu, le compilateur de langage correct à utiliser pour `x:Code` contenu est déterminé par les paramètres et les cibles du projet contenant utilisé pour compiler l’application.</span><span class="sxs-lookup"><span data-stu-id="0a3ab-112">For frameworks that permit managed `x:Code` content, the correct language compiler to use for `x:Code` content is determined by settings and targets of the containing project that is used to compile the application.</span></span>  
  
## <a name="wpf-usage-notes"></a><span data-ttu-id="0a3ab-113">Remarques sur l’utilisation WPF</span><span class="sxs-lookup"><span data-stu-id="0a3ab-113">WPF Usage Notes</span></span>  
 <span data-ttu-id="0a3ab-114">Code déclaré dans `x:Code` pour WPF a plusieurs limitations notables :</span><span class="sxs-lookup"><span data-stu-id="0a3ab-114">Code declared within `x:Code` for WPF has several notable limitations:</span></span>  
  
-   <span data-ttu-id="0a3ab-115">Le `x:Code` élément de directive doit être un élément enfant immédiat de l’élément racine de la production XAML.</span><span class="sxs-lookup"><span data-stu-id="0a3ab-115">The `x:Code` directive element must be an immediate child element of the root element of the XAML production.</span></span>  
  
-   <span data-ttu-id="0a3ab-116">[x : Class Directive](x-class-directive.md) doit être fourni sur l’élément racine parent.</span><span class="sxs-lookup"><span data-stu-id="0a3ab-116">[x:Class Directive](x-class-directive.md) must be provided on the parent root element.</span></span>  
  
-   <span data-ttu-id="0a3ab-117">Le code placé dans `x:Code` sera traité par compilation pour figurer dans la portée de la classe partielle qui est déjà en cours de création pour cette page XAML.</span><span class="sxs-lookup"><span data-stu-id="0a3ab-117">The code placed within `x:Code` will be treated by compilation to be within the scope of the partial class that is already being created for that XAML page.</span></span> <span data-ttu-id="0a3ab-118">Par conséquent, tout code que vous définissez doit être membres ou des variables de cette classe partielle.</span><span class="sxs-lookup"><span data-stu-id="0a3ab-118">Therefore all code you define must be members or variables of that partial class.</span></span>  
  
-   <span data-ttu-id="0a3ab-119">Vous ne pouvez pas définir de classes supplémentaires autrement qu’en imbriquant une classe à l’intérieur de la classe partielle (l’imbrication est autorisée, mais il n’est pas courant, car les classes imbriquées ne peuvent pas être référencées dans XAML).</span><span class="sxs-lookup"><span data-stu-id="0a3ab-119">You cannot define additional classes, other than by nesting a class inside the partial class (nesting is allowed, but it is not typical because nested classes cannot be referenced in XAML).</span></span> <span data-ttu-id="0a3ab-120">Espaces de noms CLR autres que l’espace de noms qui est utilisé pour la classe partielle existante ne peut pas être définie ou ajouté à.</span><span class="sxs-lookup"><span data-stu-id="0a3ab-120">CLR namespaces other than the namespace that is used for the existing partial class cannot be defined or added to.</span></span>  
  
-   <span data-ttu-id="0a3ab-121">Références aux entités de code en dehors de l’espace de noms CLR classe partielle doivent être qualifiés complet.</span><span class="sxs-lookup"><span data-stu-id="0a3ab-121">References to code entities outside the partial class CLR namespace must all be fully qualified.</span></span> <span data-ttu-id="0a3ab-122">Si les membres déclarés sont des remplacements pour les membres substituables de classe partielle, cela doit être spécifié avec le mot clé override de spécifique à la langue.</span><span class="sxs-lookup"><span data-stu-id="0a3ab-122">If members being declared are overrides to the partial class overridable members, this must be specified with the language-specific override keyword.</span></span> <span data-ttu-id="0a3ab-123">Si les membres déclarés dans `x:Code` étendue sont en conflit avec les membres de la classe partielle créée à partir du XAML, de sorte que le compilateur signale le conflit, le fichier XAML ne peut pas compiler ou charger.</span><span class="sxs-lookup"><span data-stu-id="0a3ab-123">If members declared in `x:Code` scope conflict with members of the partial class created out of the XAML, in such a way that the compiler reports the conflict, the XAML file cannot compile or load.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="0a3ab-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0a3ab-124">See also</span></span>

- [<span data-ttu-id="0a3ab-125">x:Class, directive</span><span class="sxs-lookup"><span data-stu-id="0a3ab-125">x:Class Directive</span></span>](x-class-directive.md)
- [<span data-ttu-id="0a3ab-126">Code-behind et XAML dans WPF</span><span class="sxs-lookup"><span data-stu-id="0a3ab-126">Code-Behind and XAML in WPF</span></span>](../wpf/advanced/code-behind-and-xaml-in-wpf.md)
- [<span data-ttu-id="0a3ab-127">Vue d’ensemble du langage XAML (WPF)</span><span class="sxs-lookup"><span data-stu-id="0a3ab-127">XAML Overview (WPF)</span></span>](../wpf/advanced/xaml-overview-wpf.md)
