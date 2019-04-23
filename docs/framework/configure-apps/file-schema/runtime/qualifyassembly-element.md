---
title: Élément <qualifyAssembly>
ms.date: 03/30/2017
f1_keywords:
- http://schemas.microsoft.com/.NetConfiguration/v2.0#qualifyAssembly
- http://schemas.microsoft.com/.NetConfiguration/v2.0#configuration/runtime/assemblyBinding/qualifyAssembly
helpviewer_keywords:
- container tags, <qualifyAssembly> element
- <qualifyAssembly> element
- qualifyAssembly element
ms.assetid: ad6442f6-1a9d-43b6-b733-04ac1b7f9b82
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 6a4741c6a4745bdba00fdb525b39b70d0b15e005
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59109446"
---
# <a name="qualifyassembly-element"></a><span data-ttu-id="578ef-102">\<qualifyAssembly > élément</span><span class="sxs-lookup"><span data-stu-id="578ef-102">\<qualifyAssembly> Element</span></span>
<span data-ttu-id="578ef-103">Spécifie le nom complet de l'assembly qui doit être chargé dynamiquement quand un nom partiel est utilisé.</span><span class="sxs-lookup"><span data-stu-id="578ef-103">Specifies the full name of the assembly that should be dynamically loaded when a partial name is used.</span></span>  
  
 <span data-ttu-id="578ef-104">\<configuration></span><span class="sxs-lookup"><span data-stu-id="578ef-104">\<configuration></span></span>  
<span data-ttu-id="578ef-105">\<runtime></span><span class="sxs-lookup"><span data-stu-id="578ef-105">\<runtime></span></span>  
<span data-ttu-id="578ef-106">\<assemblyBinding></span><span class="sxs-lookup"><span data-stu-id="578ef-106">\<assemblyBinding></span></span>  
<span data-ttu-id="578ef-107">\<qualifyAssembly></span><span class="sxs-lookup"><span data-stu-id="578ef-107">\<qualifyAssembly></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="578ef-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="578ef-108">Syntax</span></span>  
  
```xml  
      <qualifyAssembly partialName=  
      "PartialAssemblyName"  
                 fullName="FullAssemblyName"/>  
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="578ef-109">Attributs et éléments</span><span class="sxs-lookup"><span data-stu-id="578ef-109">Attributes and Elements</span></span>  
 <span data-ttu-id="578ef-110">Les sections suivantes décrivent des attributs, des éléments enfants et des éléments parents.</span><span class="sxs-lookup"><span data-stu-id="578ef-110">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="578ef-111">Attributs</span><span class="sxs-lookup"><span data-stu-id="578ef-111">Attributes</span></span>  
  
|<span data-ttu-id="578ef-112">Attribut</span><span class="sxs-lookup"><span data-stu-id="578ef-112">Attribute</span></span>|<span data-ttu-id="578ef-113">Description</span><span class="sxs-lookup"><span data-stu-id="578ef-113">Description</span></span>|  
|---------------|-----------------|  
|`partialName`|<span data-ttu-id="578ef-114">Attribut requis.</span><span class="sxs-lookup"><span data-stu-id="578ef-114">Required attribute.</span></span><br /><br /> <span data-ttu-id="578ef-115">Spécifie le nom partiel de l’assembly tel qu’il apparaît dans le code.</span><span class="sxs-lookup"><span data-stu-id="578ef-115">Specifies the partial name of the assembly as it appears in the code.</span></span>|  
|`fullName`|<span data-ttu-id="578ef-116">Attribut requis.</span><span class="sxs-lookup"><span data-stu-id="578ef-116">Required attribute.</span></span><br /><br /> <span data-ttu-id="578ef-117">Spécifie le nom complet de l’assembly tel qu’il apparaît dans le global assembly cache.</span><span class="sxs-lookup"><span data-stu-id="578ef-117">Specifies the full name of the assembly as it appears in the global assembly cache.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="578ef-118">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="578ef-118">Child Elements</span></span>  
 <span data-ttu-id="578ef-119">Aucun.</span><span class="sxs-lookup"><span data-stu-id="578ef-119">None.</span></span>  
  
### <a name="parent-elements"></a><span data-ttu-id="578ef-120">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="578ef-120">Parent Elements</span></span>  
  
|<span data-ttu-id="578ef-121">Élément</span><span class="sxs-lookup"><span data-stu-id="578ef-121">Element</span></span>|<span data-ttu-id="578ef-122">Description</span><span class="sxs-lookup"><span data-stu-id="578ef-122">Description</span></span>|  
|-------------|-----------------|  
|`assemblyBinding`|<span data-ttu-id="578ef-123">Contient des informations à propos de la redirection des versions d'assemblys et de l'emplacement de ces derniers.</span><span class="sxs-lookup"><span data-stu-id="578ef-123">Contains information about assembly version redirection and the locations of assemblies.</span></span>|  
|`configuration`|<span data-ttu-id="578ef-124">Élément racine de chaque fichier de configuration utilisé par le Common Language Runtime et les applications .NET Framework.</span><span class="sxs-lookup"><span data-stu-id="578ef-124">The root element in every configuration file used by the common language runtime and .NET Framework applications.</span></span>|  
|`runtime`|<span data-ttu-id="578ef-125">Contient des informations sur les liaisons d’assembly et l’opération garbage collection.</span><span class="sxs-lookup"><span data-stu-id="578ef-125">Contains information about assembly binding and garbage collection.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="578ef-126">Notes</span><span class="sxs-lookup"><span data-stu-id="578ef-126">Remarks</span></span>  
 <span data-ttu-id="578ef-127">Appel de la <xref:System.Reflection.Assembly.Load%2A?displayProperty=nameWithType> méthode à l’aide de noms d’assemblys partiels provoque le common language runtime à rechercher l’assembly uniquement dans le répertoire de base d’application.</span><span class="sxs-lookup"><span data-stu-id="578ef-127">Calling the <xref:System.Reflection.Assembly.Load%2A?displayProperty=nameWithType> method using partial assembly names causes the common language runtime to look for the assembly only in the application base directory.</span></span> <span data-ttu-id="578ef-128">Utilisez le  **\<qualifyAssembly >** élément dans votre fichier de configuration d’application pour fournir les informations d’assembly complet (nom, version, jeton de clé publique et culture) et forcer le common language runtime à rechercher l’assembly dans le global assembly cache.</span><span class="sxs-lookup"><span data-stu-id="578ef-128">Use the **\<qualifyAssembly>** element in your application configuration file to provide the full assembly information (name, version, public key token, and culture) and cause the common language runtime to search for the assembly in the global assembly cache.</span></span>  
  
 <span data-ttu-id="578ef-129">Le **fullName** attribut doit inclure les quatre champs d’identité d’assembly : nom, version, jeton de clé publique et culture.</span><span class="sxs-lookup"><span data-stu-id="578ef-129">The **fullName** attribute must include the four fields of assembly identity: name, version, public key token, and culture.</span></span> <span data-ttu-id="578ef-130">Le **partialName** attribut doit référencer partiellement un assembly.</span><span class="sxs-lookup"><span data-stu-id="578ef-130">The **partialName** attribute must partially reference an assembly.</span></span> <span data-ttu-id="578ef-131">Vous devez spécifier au moins le nom d’assembly texte (le cas le plus courant), mais vous pouvez également inclure la version, jeton de clé publique ou culture (ou n’importe quelle combinaison de quatre, mais pas les quatre).</span><span class="sxs-lookup"><span data-stu-id="578ef-131">You must specify at least the assembly's text name (the most common case), but you can also include version, public key token, or culture (or any combination of the four, but not all four).</span></span> <span data-ttu-id="578ef-132">Le **partialName** doit correspondre au nom spécifié dans votre appel.</span><span class="sxs-lookup"><span data-stu-id="578ef-132">The **partialName** must match the name specified in your call.</span></span> <span data-ttu-id="578ef-133">Par exemple, vous ne pouvez pas spécifier `"math"` en tant que le **partialName** attribut dans votre fichier de configuration et l’appel `Assembly.Load("math, Version=3.3.3.3")` dans votre code.</span><span class="sxs-lookup"><span data-stu-id="578ef-133">For example, you cannot specify `"math"` as the **partialName** attribute in your configuration file and call `Assembly.Load("math, Version=3.3.3.3")` in your code.</span></span>  
  
## <a name="example"></a><span data-ttu-id="578ef-134">Exemple</span><span class="sxs-lookup"><span data-stu-id="578ef-134">Example</span></span>  
 <span data-ttu-id="578ef-135">L’exemple suivant transforme logiquement l’appel `Assembly.Load("math")` dans `Assembly.Load("math,version=1.0.0.0,publicKeyToken=a1690a5ea44bab32,culture=neutral")`.</span><span class="sxs-lookup"><span data-stu-id="578ef-135">The following example logically turns the call `Assembly.Load("math")` into `Assembly.Load("math,version=1.0.0.0,publicKeyToken=a1690a5ea44bab32,culture=neutral")`.</span></span>  
  
```xml  
<configuration>  
   <runtime>  
      <assemblyBinding xmlns="urn:schemas-microsoft-com:asm.v1">  
         <qualifyAssembly partialName="math"   
                         fullName=  
"math,version=1.0.0.0,publicKeyToken=a1690a5ea44bab32,culture=neutral"/>  
      </assemblyBinding>  
   </runtime>  
</configuration>  
```  
  
## <a name="see-also"></a><span data-ttu-id="578ef-136">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="578ef-136">See also</span></span>

- [<span data-ttu-id="578ef-137">Schéma des paramètres d’exécution</span><span class="sxs-lookup"><span data-stu-id="578ef-137">Runtime Settings Schema</span></span>](../../../../../docs/framework/configure-apps/file-schema/runtime/index.md)
- [<span data-ttu-id="578ef-138">Méthode de localisation des assemblys par le runtime</span><span class="sxs-lookup"><span data-stu-id="578ef-138">How the Runtime Locates Assemblies</span></span>](../../../../../docs/framework/deployment/how-the-runtime-locates-assemblies.md)
- <span data-ttu-id="578ef-139">[Références d’Assembly partielles](https://docs.microsoft.com/previous-versions/dotnet/netframework-4.0/0a7zy9z5(v=vs.100))</span><span class="sxs-lookup"><span data-stu-id="578ef-139">[Partial Assembly References](https://docs.microsoft.com/previous-versions/dotnet/netframework-4.0/0a7zy9z5(v=vs.100))</span></span>
