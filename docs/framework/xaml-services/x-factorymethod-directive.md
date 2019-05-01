---
title: x:FactoryMethod, directive
ms.date: 03/30/2017
helpviewer_keywords:
- XAML. x:FactoryMethod directive [XAML Services]
- FactoryMethod directive in XAML [XAML Services]
- x:FactoryMethod directive [XAML Services]
ms.assetid: 829bcbdf-5318-4afb-9a03-c310e0d2f23d
ms.openlocfilehash: 8fff4d62e07bdfd4ecc27d2692c391251afdd6d5
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61971832"
---
# <a name="xfactorymethod-directive"></a><span data-ttu-id="4c93a-102">x:FactoryMethod, directive</span><span class="sxs-lookup"><span data-stu-id="4c93a-102">x:FactoryMethod Directive</span></span>
<span data-ttu-id="4c93a-103">Spécifie une méthode autre qu’un constructeur qu’un processeur XAML doit utiliser pour initialiser un objet après avoir résolu son type de stockage.</span><span class="sxs-lookup"><span data-stu-id="4c93a-103">Specifies a method other than a constructor that a XAML processor should use to initialize an object after resolving its backing type.</span></span>  
  
## <a name="xaml-attribute-usage-no-xarguments"></a><span data-ttu-id="4c93a-104">Utilisation d’attribut XAML, aucune x : Arguments</span><span class="sxs-lookup"><span data-stu-id="4c93a-104">XAML Attribute Usage, no x:Arguments</span></span>  
  
```  
<object x:FactoryMethod="methodname"...>  
  ...  
</object>  
```  
  
## <a name="xaml-attribute-usage-xarguments-as-elements"></a><span data-ttu-id="4c93a-105">Utilisation d’attribut XAML, x : Arguments comme élément (s)</span><span class="sxs-lookup"><span data-stu-id="4c93a-105">XAML Attribute Usage, x:Arguments as Element(s)</span></span>  
  
```  
<object x:FactoryMethod="methodname"...>  
  <x:Arguments>  
    oneOrMoreObjectElements  
  </x:Arguments>  
</object>  
```  
  
## <a name="xaml-values"></a><span data-ttu-id="4c93a-106">Valeurs XAML</span><span class="sxs-lookup"><span data-stu-id="4c93a-106">XAML Values</span></span>  
  
|||  
|-|-|  
|`methodname`|<span data-ttu-id="4c93a-107">Le nom de méthode de chaîne d’une méthode que les processeurs XAML appellent pour initialiser l’instance spécifiée en tant que `object`.</span><span class="sxs-lookup"><span data-stu-id="4c93a-107">The string method name of a method that XAML processors call to initialize the instance specified as `object`.</span></span> <span data-ttu-id="4c93a-108">Consultez la section Notes.</span><span class="sxs-lookup"><span data-stu-id="4c93a-108">See Remarks.</span></span>|  
|`oneOrMoreObjectElements`|<span data-ttu-id="4c93a-109">Un ou plusieurs éléments objet pour les objets qui spécifient les paramètres de méthode de fabrique.</span><span class="sxs-lookup"><span data-stu-id="4c93a-109">One or more object elements for objects that specify factory method parameters.</span></span> <span data-ttu-id="4c93a-110">Ordre est significatif ; Il désigne l’ordre dans lequel les arguments doivent être passés à la méthode de fabrique.</span><span class="sxs-lookup"><span data-stu-id="4c93a-110">Order is significant; it signifies the order in which arguments should be passed to the factory method.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="4c93a-111">Notes</span><span class="sxs-lookup"><span data-stu-id="4c93a-111">Remarks</span></span>  
 <span data-ttu-id="4c93a-112">Si `methodname` est une méthode d’instance, il ne peut pas être qualifié.</span><span class="sxs-lookup"><span data-stu-id="4c93a-112">If `methodname` is an instance method, it cannot be qualified.</span></span>  
  
 <span data-ttu-id="4c93a-113">Les méthodes statiques en tant que méthodes de fabrique sont prises en charge.</span><span class="sxs-lookup"><span data-stu-id="4c93a-113">Static methods as factory methods are supported.</span></span> <span data-ttu-id="4c93a-114">Si `methodname` est une méthode statique, `methodname` est fourni comme un *typeName*. *methodName* combinaison, où *typeName* nomme la classe qui définit la méthode de fabrique statique.</span><span class="sxs-lookup"><span data-stu-id="4c93a-114">If `methodname` is a static method, `methodname` is provided as a *typeName*.*methodName* combination, where *typeName* names the class that defines the static factory method.</span></span> <span data-ttu-id="4c93a-115">*typeName* peut être qualifié par un préfixe s’il fait référence à un type dans un fichier xmlns mappé.</span><span class="sxs-lookup"><span data-stu-id="4c93a-115">*typeName* can be prefix-qualified if referring to a type in a mapped xmlns.</span></span> <span data-ttu-id="4c93a-116">*typeName* peut être un type différent de `typeof(object)`.</span><span class="sxs-lookup"><span data-stu-id="4c93a-116">*typeName* can be a different type than `typeof(object)`.</span></span>  
  
 <span data-ttu-id="4c93a-117">La méthode de fabrique doit être une méthode déclarée publique du type qui stocke l’élément objet appropriée.</span><span class="sxs-lookup"><span data-stu-id="4c93a-117">The factory method must be a declared public method of the type that backs the relevant object element.</span></span>  
  
 <span data-ttu-id="4c93a-118">La méthode de fabrique doit retourner une instance qui ne peut être assignée à l’objet correspondant.</span><span class="sxs-lookup"><span data-stu-id="4c93a-118">The factory method must return an instance that is assignable to the relevant object.</span></span> <span data-ttu-id="4c93a-119">Méthodes de fabrique ne doivent jamais retourner null.</span><span class="sxs-lookup"><span data-stu-id="4c93a-119">Factory methods should never return null.</span></span>  
  
 <span data-ttu-id="4c93a-120">`x:Arguments` fonctionne sur un principe de meilleure correspondance pour les signatures de méthodes de fabrique.</span><span class="sxs-lookup"><span data-stu-id="4c93a-120">`x:Arguments` operates on a principle of best match for signatures of factory methods.</span></span> <span data-ttu-id="4c93a-121">Mise en correspondance évalue d’abord le nombre de paramètres.</span><span class="sxs-lookup"><span data-stu-id="4c93a-121">Matching evaluates the parameter count first.</span></span> <span data-ttu-id="4c93a-122">S’il existe plusieurs correspondances possibles pour un nombre de paramètres, type de paramètre est évaluée et la meilleure correspondance est déterminée.</span><span class="sxs-lookup"><span data-stu-id="4c93a-122">If there is more than one possible match for a parameter count, parameter type is then evaluated and best match is determined.</span></span> <span data-ttu-id="4c93a-123">S’il reste une ambiguïté après cette phase d’évaluation, le comportement du processeur XAML est indéfini.</span><span class="sxs-lookup"><span data-stu-id="4c93a-123">If there is still ambiguity after this phase of evaluation, XAML processor behavior is undefined.</span></span>  
  
 <span data-ttu-id="4c93a-124">Le `x:FactoryMethod` utilisation de l’élément n’est pas utilisation d’élément de propriété dans le sens classique, étant donné que le balisage de directive ne référence pas de type de l’élément objet contenant.</span><span class="sxs-lookup"><span data-stu-id="4c93a-124">The `x:FactoryMethod` element usage is not property element usage in the typical sense, because the directive markup does not reference the containing object element's type.</span></span> <span data-ttu-id="4c93a-125">Il est probable que l’utilisation d’élément est moins fréquentes que l’utilisation d’attribut.</span><span class="sxs-lookup"><span data-stu-id="4c93a-125">It is expected that element usage is less common than attribute usage.</span></span> <span data-ttu-id="4c93a-126">`x:Arguments` (utilisation d’attribut ou élément) peut être utilisée avec `x:FactoryMethod` utilisation de l’élément, mais cela n’est pas spécifiquement indiqué dans les sections de l’utilisation.</span><span class="sxs-lookup"><span data-stu-id="4c93a-126">`x:Arguments` (either attribute or element usage) can be used along with `x:FactoryMethod` element usage, but this is not specifically shown in the Usage sections.</span></span>  
  
 <span data-ttu-id="4c93a-127">`x:FactoryMethod` comme un élément doit précéder tous les autres éléments de propriété, il doit précéder tout `x:Arguments` également fourni en tant qu’éléments et doit précéder n’importe quel contenu/interne texte/texte d’initialisation.</span><span class="sxs-lookup"><span data-stu-id="4c93a-127">`x:FactoryMethod` as an element must precede any other property elements, must precede any `x:Arguments` also provided as elements, and must precede any content/inner text/initialization text.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="4c93a-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="4c93a-128">See also</span></span>

- [<span data-ttu-id="4c93a-129">x:Arguments (directive)</span><span class="sxs-lookup"><span data-stu-id="4c93a-129">x:Arguments Directive</span></span>](x-arguments-directive.md)
