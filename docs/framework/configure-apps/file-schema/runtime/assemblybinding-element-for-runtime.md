---
title: Élément <assemblyBinding> pour <runtime>
ms.date: 03/30/2017
f1_keywords:
- http://schemas.microsoft.com/.NetConfiguration/v2.0#configuration/runtime/assemblyBinding
helpviewer_keywords:
- <assemblyBinding> element
- assemblyBinding element
- container tags, <assemblyBinding> element
ms.assetid: 964cbb35-ab49-4498-8471-209689e5dada
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: eec77d4dd42a7b95d1e2cd0e353e2e54746676b7
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59225246"
---
# <a name="assemblybinding-element-for-runtime"></a><span data-ttu-id="fec4f-102">\<assemblyBinding >, élément pour \<runtime ></span><span class="sxs-lookup"><span data-stu-id="fec4f-102">\<assemblyBinding> Element for \<runtime></span></span>
<span data-ttu-id="fec4f-103">Contient des informations à propos de la redirection des versions d'assemblys et de l'emplacement de ces derniers.</span><span class="sxs-lookup"><span data-stu-id="fec4f-103">Contains information about assembly version redirection and the locations of assemblies.</span></span>  
  
 <span data-ttu-id="fec4f-104">\<configuration></span><span class="sxs-lookup"><span data-stu-id="fec4f-104">\<configuration></span></span>  
<span data-ttu-id="fec4f-105">\<runtime></span><span class="sxs-lookup"><span data-stu-id="fec4f-105">\<runtime></span></span>  
<span data-ttu-id="fec4f-106">\<assemblyBinding></span><span class="sxs-lookup"><span data-stu-id="fec4f-106">\<assemblyBinding></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="fec4f-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="fec4f-107">Syntax</span></span>  
  
```xml  
      <assemblyBinding    
   xmlns="urn:schemas-microsoft-com:asm.v1" appliesTo="v1.0.3705">  
</assemblyBinding>  
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="fec4f-108">Attributs et éléments</span><span class="sxs-lookup"><span data-stu-id="fec4f-108">Attributes and Elements</span></span>  
 <span data-ttu-id="fec4f-109">Les sections suivantes décrivent des attributs, des éléments enfants et des éléments parents.</span><span class="sxs-lookup"><span data-stu-id="fec4f-109">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="fec4f-110">Attributs</span><span class="sxs-lookup"><span data-stu-id="fec4f-110">Attributes</span></span>  
  
|<span data-ttu-id="fec4f-111">Attribut</span><span class="sxs-lookup"><span data-stu-id="fec4f-111">Attribute</span></span>|<span data-ttu-id="fec4f-112">Description</span><span class="sxs-lookup"><span data-stu-id="fec4f-112">Description</span></span>|  
|---------------|-----------------|  
|<span data-ttu-id="fec4f-113">**xmlns**</span><span class="sxs-lookup"><span data-stu-id="fec4f-113">**xmlns**</span></span>|<span data-ttu-id="fec4f-114">Attribut requis.</span><span class="sxs-lookup"><span data-stu-id="fec4f-114">Required attribute.</span></span><br /><br /> <span data-ttu-id="fec4f-115">Spécifie l'espace de noms XML requis pour la liaison d'assembly.</span><span class="sxs-lookup"><span data-stu-id="fec4f-115">Specifies the XML namespace required for assembly binding.</span></span> <span data-ttu-id="fec4f-116">Utilisez la chaîne « urn:schemas-microsoft-com:asm.v1 » comme valeur.</span><span class="sxs-lookup"><span data-stu-id="fec4f-116">Use the string "urn:schemas-microsoft-com:asm.v1" as the value.</span></span>|  
|<span data-ttu-id="fec4f-117">**appliesTo**</span><span class="sxs-lookup"><span data-stu-id="fec4f-117">**appliesTo**</span></span>|<span data-ttu-id="fec4f-118">Spécifie la version du runtime à laquelle s'applique la redirection d'assembly .NET Framework.</span><span class="sxs-lookup"><span data-stu-id="fec4f-118">Specifies the runtime version the .NET Framework assembly redirection applies to.</span></span> <span data-ttu-id="fec4f-119">Cet attribut facultatif utilise un numéro de version .NET Framework pour indiquer la version à laquelle il s'applique.</span><span class="sxs-lookup"><span data-stu-id="fec4f-119">This optional attribute uses a .NET Framework version number to indicate what version it applies to.</span></span> <span data-ttu-id="fec4f-120">Si l’attribut **appliesTo** n’est pas spécifié, l’élément **\<assemblyBinding>** s’applique à toutes les versions du .NET Framework.</span><span class="sxs-lookup"><span data-stu-id="fec4f-120">If no **appliesTo** attribute is specified, the **\<assemblyBinding>** element applies to all versions of the .NET Framework.</span></span> <span data-ttu-id="fec4f-121">Le **appliesTo** attribut a été introduit dans .NET Framework version 1.1 ; il est ignoré par le .NET Framework version 1.0.</span><span class="sxs-lookup"><span data-stu-id="fec4f-121">The **appliesTo** attribute was introduced in .NET Framework version 1.1; it is ignored by the .NET Framework version 1.0.</span></span> <span data-ttu-id="fec4f-122">Cela signifie que tous les éléments **\<assemblyBinding>** sont appliqués lors de l’utilisation du .NET Framework 1.0, même si un attribut **appliesTo** est spécifié.</span><span class="sxs-lookup"><span data-stu-id="fec4f-122">This means that all **\<assemblyBinding>** elements are applied when using the .NET Framework version 1.0, even if an **appliesTo** attribute is specified.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="fec4f-123">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="fec4f-123">Child Elements</span></span>  
  
|<span data-ttu-id="fec4f-124">Élément</span><span class="sxs-lookup"><span data-stu-id="fec4f-124">Element</span></span>|<span data-ttu-id="fec4f-125">Description</span><span class="sxs-lookup"><span data-stu-id="fec4f-125">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="fec4f-126">\<dependentAssembly></span><span class="sxs-lookup"><span data-stu-id="fec4f-126">\<dependentAssembly></span></span>](../../../../../docs/framework/configure-apps/file-schema/runtime/dependentassembly-element.md)|<span data-ttu-id="fec4f-127">Encapsule la stratégie de liaison et l'emplacement d'un assembly.</span><span class="sxs-lookup"><span data-stu-id="fec4f-127">Encapsulates binding policy and assembly location for an assembly.</span></span> <span data-ttu-id="fec4f-128">Utilisez une  **\<dependentAssembly >** balise pour chaque assembly.</span><span class="sxs-lookup"><span data-stu-id="fec4f-128">Use one **\<dependentAssembly>** tag for each assembly.</span></span>|  
|[<span data-ttu-id="fec4f-129">\<probing></span><span class="sxs-lookup"><span data-stu-id="fec4f-129">\<probing></span></span>](../../../../../docs/framework/configure-apps/file-schema/runtime/probing-element.md)|<span data-ttu-id="fec4f-130">Spécifie les sous-répertoires interrogés par le Common Language Runtime lors du chargement des assemblys.</span><span class="sxs-lookup"><span data-stu-id="fec4f-130">Specifies subdirectories the common language runtime searches when loading assemblies.</span></span>|  
|[<span data-ttu-id="fec4f-131">\<publisherPolicy></span><span class="sxs-lookup"><span data-stu-id="fec4f-131">\<publisherPolicy></span></span>](../../../../../docs/framework/configure-apps/file-schema/runtime/publisherpolicy-element.md)|<span data-ttu-id="fec4f-132">Spécifie si le runtime applique la stratégie de l'éditeur.</span><span class="sxs-lookup"><span data-stu-id="fec4f-132">Specifies whether the runtime applies publisher policy.</span></span>|  
|[<span data-ttu-id="fec4f-133">\<qualifyAssembly></span><span class="sxs-lookup"><span data-stu-id="fec4f-133">\<qualifyAssembly></span></span>](../../../../../docs/framework/configure-apps/file-schema/runtime/qualifyassembly-element.md)|<span data-ttu-id="fec4f-134">Spécifie le nom complet de l'assembly qui doit être chargé dynamiquement quand un nom partiel est utilisé.</span><span class="sxs-lookup"><span data-stu-id="fec4f-134">Specifies the full name of the assembly that should be dynamically loaded when a partial name is used.</span></span>|  
  
### <a name="parent-elements"></a><span data-ttu-id="fec4f-135">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="fec4f-135">Parent Elements</span></span>  
  
|<span data-ttu-id="fec4f-136">Élément</span><span class="sxs-lookup"><span data-stu-id="fec4f-136">Element</span></span>|<span data-ttu-id="fec4f-137">Description</span><span class="sxs-lookup"><span data-stu-id="fec4f-137">Description</span></span>|  
|-------------|-----------------|  
|`configuration`|<span data-ttu-id="fec4f-138">Élément racine de chaque fichier de configuration utilisé par le Common Language Runtime et les applications .NET Framework.</span><span class="sxs-lookup"><span data-stu-id="fec4f-138">The root element in every configuration file used by the common language runtime and .NET Framework applications.</span></span>|  
|`runtime`|<span data-ttu-id="fec4f-139">Contient des informations sur les liaisons d’assembly et l’opération garbage collection.</span><span class="sxs-lookup"><span data-stu-id="fec4f-139">Contains information about assembly binding and garbage collection.</span></span>|  
  
## <a name="example"></a><span data-ttu-id="fec4f-140">Exemple</span><span class="sxs-lookup"><span data-stu-id="fec4f-140">Example</span></span>  
 <span data-ttu-id="fec4f-141">L'exemple suivant montre comment rediriger une version d'assembly vers une autre et fournir une base de code.</span><span class="sxs-lookup"><span data-stu-id="fec4f-141">The following example shows how to redirect one assembly version to another and provide a codebase.</span></span>  
  
```xml  
<configuration>  
   <runtime>  
      <assemblyBinding xmlns="urn:schemas-microsoft-com:asm.v1">  
         <dependentAssembly>  
            <assemblyIdentity name="myAssembly"  
                              publicKeyToken="32ab4ba45e0a69a1"  
                              culture="neutral" />  
            <bindingRedirect oldVersion="1.0.0.0"  
                             newVersion="2.0.0.0"/>  
            <codeBase version="2.0.0.0"  
                      href="http://www.litwareinc.com/myAssembly.dll"/>  
         </dependentAssembly>  
      </assemblyBinding>  
   </runtime>  
</configuration>  
```  
  
 <span data-ttu-id="fec4f-142">L’exemple suivant montre comment utiliser le **appliesTo** attribut pour rediriger la liaison d’un assembly .NET Framework.</span><span class="sxs-lookup"><span data-stu-id="fec4f-142">The following example shows how to use the **appliesTo** attribute to redirect binding of a .NET Framework assembly.</span></span>  
  
```xml  
<runtime>  
   <assemblyBinding xmlns="urn:schemas-microsoft-com:asm.v1" appliesTo="v1.0.3705">  
      <dependentAssembly>   
         <assemblyIdentity name="mscorcfg" publicKeyToken="b03f5f7f11d50a3a" culture=""/>  
         <bindingRedirect oldVersion="0.0.0.0-65535.65535.65535.65535" newVersion="1.0.3300.0"/>  
      </dependentAssembly>  
   </assemblyBinding>  
</runtime>  
```  
  
## <a name="see-also"></a><span data-ttu-id="fec4f-143">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="fec4f-143">See also</span></span>

- [<span data-ttu-id="fec4f-144">Schéma des paramètres d’exécution</span><span class="sxs-lookup"><span data-stu-id="fec4f-144">Runtime Settings Schema</span></span>](../../../../../docs/framework/configure-apps/file-schema/runtime/index.md)
- [<span data-ttu-id="fec4f-145">Schéma des fichiers de configuration</span><span class="sxs-lookup"><span data-stu-id="fec4f-145">Configuration File Schema</span></span>](../../../../../docs/framework/configure-apps/file-schema/index.md)
- [<span data-ttu-id="fec4f-146">Redirection des versions d'assemblys</span><span class="sxs-lookup"><span data-stu-id="fec4f-146">Redirecting Assembly Versions</span></span>](../../../../../docs/framework/configure-apps/redirect-assembly-versions.md)
