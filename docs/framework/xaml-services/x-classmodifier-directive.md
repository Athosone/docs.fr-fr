---
title: x:ClassModifier, directive
ms.date: 03/30/2017
f1_keywords:
- xClassModifier
- x:ClassModifier
- ClassModifier
helpviewer_keywords:
- XAML [XAML Services], x:ClassModifier attribute
- x:ClassModifier attribute [XAML Services]
- ClassModifier attribute in XAML [XAML Services]
ms.assetid: ef30ab78-d334-4668-917d-c9f66c3b6aea
ms.openlocfilehash: fdbc69634e86992e71cfccdc080829b6b45f963c
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61971897"
---
# <a name="xclassmodifier-directive"></a><span data-ttu-id="1ca2c-102">x:ClassModifier, directive</span><span class="sxs-lookup"><span data-stu-id="1ca2c-102">x:ClassModifier Directive</span></span>
<span data-ttu-id="1ca2c-103">Modifie le comportement de compilation XAML lorsque `x:Class` est également fourni.</span><span class="sxs-lookup"><span data-stu-id="1ca2c-103">Modifies XAML compilation behavior when `x:Class` is also provided.</span></span> <span data-ttu-id="1ca2c-104">Plus précisément, au lieu de la création d’un partiel `class` qui a un `Public` (la valeur par défaut), de niveau d’accès fourni `x:Class` est créé avec un `NotPublic` niveau d’accès.</span><span class="sxs-lookup"><span data-stu-id="1ca2c-104">Specifically, instead of creating a partial `class` that has a `Public` access level (the default), the provided `x:Class` is created with a `NotPublic` access level.</span></span> <span data-ttu-id="1ca2c-105">Ce comportement affecte le niveau d’accès pour la classe dans les assemblys générés.</span><span class="sxs-lookup"><span data-stu-id="1ca2c-105">This behavior affects the access level for the class in the generated assemblies.</span></span>  
  
## <a name="xaml-attribute-usage"></a><span data-ttu-id="1ca2c-106">Utilisation d'attributs XAML</span><span class="sxs-lookup"><span data-stu-id="1ca2c-106">XAML Attribute Usage</span></span>  
  
```  
<object x:Class="namespace.classname" x:ClassModifier="NotPublic">  
   ...  
</object>  
```  
  
## <a name="xaml-values"></a><span data-ttu-id="1ca2c-107">Valeurs XAML</span><span class="sxs-lookup"><span data-stu-id="1ca2c-107">XAML Values</span></span>  
  
|||  
|-|-|  
|<span data-ttu-id="1ca2c-108">*NotPublic*</span><span class="sxs-lookup"><span data-stu-id="1ca2c-108">*NotPublic*</span></span>|<span data-ttu-id="1ca2c-109">La chaîne exacte à passer pour spécifier <xref:System.Reflection.TypeAttributes.Public?displayProperty=nameWithType> et <xref:System.Reflection.TypeAttributes.NotPublic?displayProperty=nameWithType> varie selon le langage de programmation de code-behind que vous utilisez.</span><span class="sxs-lookup"><span data-stu-id="1ca2c-109">The exact string to pass to specify <xref:System.Reflection.TypeAttributes.Public?displayProperty=nameWithType> versus <xref:System.Reflection.TypeAttributes.NotPublic?displayProperty=nameWithType> varies, depending on the code-behind programming language that you use.</span></span> <span data-ttu-id="1ca2c-110">Consultez la section Notes.</span><span class="sxs-lookup"><span data-stu-id="1ca2c-110">See Remarks.</span></span>|  
  
## <a name="dependencies"></a><span data-ttu-id="1ca2c-111">Dépendances</span><span class="sxs-lookup"><span data-stu-id="1ca2c-111">Dependencies</span></span>  
 <span data-ttu-id="1ca2c-112">[x : Class](x-class-directive.md) doit également être fourni dans le même élément, et cet élément doit être l’élément racine dans une page.</span><span class="sxs-lookup"><span data-stu-id="1ca2c-112">[x:Class](x-class-directive.md) must also be provided on the same element, and that element must be the root element in a page.</span></span> <span data-ttu-id="1ca2c-113">Pour plus d’informations, consultez [ \[MS-XAML\] Section 4.3.1.8](https://go.microsoft.com/fwlink/?LinkId=114525).</span><span class="sxs-lookup"><span data-stu-id="1ca2c-113">For more information, see [\[MS-XAML\] Section 4.3.1.8](https://go.microsoft.com/fwlink/?LinkId=114525).</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="1ca2c-114">Notes</span><span class="sxs-lookup"><span data-stu-id="1ca2c-114">Remarks</span></span>  
 <span data-ttu-id="1ca2c-115">La valeur de `x:ClassModifier` dans les Services XAML .NET Framework, l’utilisation varie par langage de programmation.</span><span class="sxs-lookup"><span data-stu-id="1ca2c-115">The value of `x:ClassModifier` in .NET Framework XAML Services usage varies by programming language.</span></span> <span data-ttu-id="1ca2c-116">La chaîne à utiliser dépend de la façon dont chaque langage implémente son <xref:System.CodeDom.Compiler.CodeDomProvider> et les convertisseurs de type qu’il retourne pour définir les significations de <xref:System.Reflection.TypeAttributes.Public?displayProperty=nameWithType> et <xref:System.Reflection.TypeAttributes.NotPublic?displayProperty=nameWithType>, et si cette langue est sensible à la casse.</span><span class="sxs-lookup"><span data-stu-id="1ca2c-116">The string to use depends on how each language implements its <xref:System.CodeDom.Compiler.CodeDomProvider> and the type converters it returns to define the meanings for <xref:System.Reflection.TypeAttributes.Public?displayProperty=nameWithType> and <xref:System.Reflection.TypeAttributes.NotPublic?displayProperty=nameWithType>, and whether that language is case sensitive.</span></span>  
  
- <span data-ttu-id="1ca2c-117">Pour c#, la chaîne à passer pour désigner <xref:System.Reflection.TypeAttributes.NotPublic?displayProperty=nameWithType> est `internal`.</span><span class="sxs-lookup"><span data-stu-id="1ca2c-117">For C#, the string to pass to designate <xref:System.Reflection.TypeAttributes.NotPublic?displayProperty=nameWithType> is `internal`.</span></span>  
  
- <span data-ttu-id="1ca2c-118">Pour Microsoft Visual Basic .NET, la chaîne à passer pour désigner <xref:System.Reflection.TypeAttributes.NotPublic?displayProperty=nameWithType> est `Friend`.</span><span class="sxs-lookup"><span data-stu-id="1ca2c-118">For Microsoft Visual Basic .NET, the string to pass to designate <xref:System.Reflection.TypeAttributes.NotPublic?displayProperty=nameWithType> is `Friend`.</span></span>  
  
- <span data-ttu-id="1ca2c-119">Pour [!INCLUDE[TLA2#tla_cppcli](../../../includes/tla2sharptla-cppcli-md.md)], qui prennent en charge compilation XAML n’existe aucune cible ; par conséquent, la valeur à passer n’est pas spécifiée.</span><span class="sxs-lookup"><span data-stu-id="1ca2c-119">For [!INCLUDE[TLA2#tla_cppcli](../../../includes/tla2sharptla-cppcli-md.md)], no targets exist that support compiling XAML; therefore, the value to pass is unspecified.</span></span>  
  
 <span data-ttu-id="1ca2c-120">Vous pouvez également spécifier <xref:System.Reflection.TypeAttributes.Public?displayProperty=nameWithType> (`public` en c#, `Public` en Visual Basic) ; Toutefois, en spécifiant <xref:System.Reflection.TypeAttributes.Public?displayProperty=nameWithType> est rarement car <xref:System.Reflection.TypeAttributes.Public?displayProperty=nameWithType> est déjà le comportement par défaut.</span><span class="sxs-lookup"><span data-stu-id="1ca2c-120">You can also specify <xref:System.Reflection.TypeAttributes.Public?displayProperty=nameWithType> (`public` in C#, `Public` in Visual Basic); however, specifying <xref:System.Reflection.TypeAttributes.Public?displayProperty=nameWithType> is infrequently done because <xref:System.Reflection.TypeAttributes.Public?displayProperty=nameWithType> is already the default behavior.</span></span>  
  
 <span data-ttu-id="1ca2c-121">Autres valeurs avec le code utilisateur équivalente-niveau d’accès restrictions, telles que `private` en c#, ne sont pas pertinentes pour `x:ClassModifier` , car les références de classe imbriquées ne sont pas pris en charge dans XAML et par conséquent, le <xref:System.Reflection.TypeAttributes.NotPublic?displayProperty=nameWithType> modificateur a le même effet.</span><span class="sxs-lookup"><span data-stu-id="1ca2c-121">Other values with equivalent user code access-level restrictions, such as `private` in C#, are not relevant for `x:ClassModifier` because nested class references are not supported in XAML, and therefore, the <xref:System.Reflection.TypeAttributes.NotPublic?displayProperty=nameWithType> modifier has the same effect.</span></span>  
  
## <a name="security-notes"></a><span data-ttu-id="1ca2c-122">Notes de sécurité</span><span class="sxs-lookup"><span data-stu-id="1ca2c-122">Security Notes</span></span>  
 <span data-ttu-id="1ca2c-123">Le niveau d’accès tel que déclaré dans `x:ClassModifier` est toujours soumis à l’interprétation par les infrastructures particulières et leurs fonctionnalités.</span><span class="sxs-lookup"><span data-stu-id="1ca2c-123">The access level as declared in `x:ClassModifier` is still subject to interpretation by particular frameworks and their capabilities.</span></span> <span data-ttu-id="1ca2c-124">WPF inclut des fonctions pour charger et instancier des types où `x:ClassModifier` est `internal`, si cette classe est référencée à partir d’une ressource WPF via une référence URI à en-tête pack.</span><span class="sxs-lookup"><span data-stu-id="1ca2c-124">WPF includes capabilities to load and instantiate types where `x:ClassModifier` is `internal`, if that class is referenced from a WPF resource through a pack URI reference.</span></span> <span data-ttu-id="1ca2c-125">En raison de ce cas et potentiellement d’autres similaires implémentés par d’autres infrastructures, ne comptez pas exclusivement sur `x:ClassModifier` pour bloquer l’instanciation de toutes les tentatives.</span><span class="sxs-lookup"><span data-stu-id="1ca2c-125">As a consequence of this case and potentially others like it implemented by other frameworks, do not rely exclusively on `x:ClassModifier` to block all possible instantiation attempts.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="1ca2c-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1ca2c-126">See also</span></span>

- [<span data-ttu-id="1ca2c-127">x:Class, directive</span><span class="sxs-lookup"><span data-stu-id="1ca2c-127">x:Class Directive</span></span>](x-class-directive.md)
- [<span data-ttu-id="1ca2c-128">Code-behind et XAML dans WPF</span><span class="sxs-lookup"><span data-stu-id="1ca2c-128">Code-Behind and XAML in WPF</span></span>](../wpf/advanced/code-behind-and-xaml-in-wpf.md)
- [<span data-ttu-id="1ca2c-129">x:FieldModifier, directive</span><span class="sxs-lookup"><span data-stu-id="1ca2c-129">x:FieldModifier Directive</span></span>](x-fieldmodifier-directive.md)
- [<span data-ttu-id="1ca2c-130">Sécurité (WPF)</span><span class="sxs-lookup"><span data-stu-id="1ca2c-130">Security (WPF)</span></span>](../wpf/security-wpf.md)
- [<span data-ttu-id="1ca2c-131">Types migrés de WPF vers System.Xaml</span><span class="sxs-lookup"><span data-stu-id="1ca2c-131">Types Migrated from WPF to System.Xaml</span></span>](types-migrated-from-wpf-to-system-xaml.md)
