---
title: Élément <assemblyIdentity> pour <runtime>
ms.date: 03/30/2017
f1_keywords:
- http://schemas.microsoft.com/.NetConfiguration/v2.0#configuration/runtime/assemblyBinding/dependentAssembly/assemblyIdentity
- http://schemas.microsoft.com/.NetConfiguration/v2.0#assemblyIdentity
helpviewer_keywords:
- <assemblyIdentity> element
- container tags, <assemblyIdentity> element
- assemblyIdentity element
ms.assetid: cea4d187-6398-4da4-af09-c1abc6a349c1
ms.openlocfilehash: d5766b76f18dce441cb260887a753dcf64642a6f
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59098697"
---
# <a name="assemblyidentity-element-for-runtime"></a><span data-ttu-id="5f9c8-102">\<assemblyIdentity >, élément pour \<runtime ></span><span class="sxs-lookup"><span data-stu-id="5f9c8-102">\<assemblyIdentity> Element for \<runtime></span></span>
<span data-ttu-id="5f9c8-103">Contient des informations d’identification sur l’assembly.</span><span class="sxs-lookup"><span data-stu-id="5f9c8-103">Contains identifying information about the assembly.</span></span>  
  
 <span data-ttu-id="5f9c8-104">\<configuration></span><span class="sxs-lookup"><span data-stu-id="5f9c8-104">\<configuration></span></span>  
<span data-ttu-id="5f9c8-105">\<runtime></span><span class="sxs-lookup"><span data-stu-id="5f9c8-105">\<runtime></span></span>  
<span data-ttu-id="5f9c8-106">\<assemblyBinding></span><span class="sxs-lookup"><span data-stu-id="5f9c8-106">\<assemblyBinding></span></span>  
<span data-ttu-id="5f9c8-107">\<dependentAssembly></span><span class="sxs-lookup"><span data-stu-id="5f9c8-107">\<dependentAssembly></span></span>  
<span data-ttu-id="5f9c8-108">\<assemblyIdentity></span><span class="sxs-lookup"><span data-stu-id="5f9c8-108">\<assemblyIdentity></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="5f9c8-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="5f9c8-109">Syntax</span></span>  
  
```xml  
   <assemblyIdentity    
name="assembly name"  
publicKeyToken="public key token"  
culture="assembly culture"/>  
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="5f9c8-110">Attributs et éléments</span><span class="sxs-lookup"><span data-stu-id="5f9c8-110">Attributes and Elements</span></span>  
 <span data-ttu-id="5f9c8-111">Les sections suivantes décrivent des attributs, des éléments enfants et des éléments parents.</span><span class="sxs-lookup"><span data-stu-id="5f9c8-111">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="5f9c8-112">Attributs</span><span class="sxs-lookup"><span data-stu-id="5f9c8-112">Attributes</span></span>  
  
|<span data-ttu-id="5f9c8-113">Attribut</span><span class="sxs-lookup"><span data-stu-id="5f9c8-113">Attribute</span></span>|<span data-ttu-id="5f9c8-114">Description</span><span class="sxs-lookup"><span data-stu-id="5f9c8-114">Description</span></span>|  
|---------------|-----------------|  
|`name`|<span data-ttu-id="5f9c8-115">Attribut requis.</span><span class="sxs-lookup"><span data-stu-id="5f9c8-115">Required attribute.</span></span><br /><br /> <span data-ttu-id="5f9c8-116">Le nom de l’assembly</span><span class="sxs-lookup"><span data-stu-id="5f9c8-116">The name of the assembly</span></span>|  
|`culture`|<span data-ttu-id="5f9c8-117">Attribut facultatif.</span><span class="sxs-lookup"><span data-stu-id="5f9c8-117">Optional attribute.</span></span><br /><br /> <span data-ttu-id="5f9c8-118">Chaîne qui spécifie la langue et le pays/région de l’assembly.</span><span class="sxs-lookup"><span data-stu-id="5f9c8-118">A string that specifies the language and country/region of the assembly.</span></span>|  
|`publicKeyToken`|<span data-ttu-id="5f9c8-119">Attribut facultatif.</span><span class="sxs-lookup"><span data-stu-id="5f9c8-119">Optional attribute.</span></span><br /><br /> <span data-ttu-id="5f9c8-120">Une valeur hexadécimale qui spécifie le nom fort de l’assembly.</span><span class="sxs-lookup"><span data-stu-id="5f9c8-120">A hexadecimal value that specifies the strong name of the assembly.</span></span>|  
|`processorArchitecture`|<span data-ttu-id="5f9c8-121">Attribut facultatif.</span><span class="sxs-lookup"><span data-stu-id="5f9c8-121">Optional attribute.</span></span><br /><br /> <span data-ttu-id="5f9c8-122">Une des valeurs « x86 », « amd64 », « msil » ou « ia64 », en spécifiant l’architecture de processeur pour un assembly qui contient le code spécifique au processeur.</span><span class="sxs-lookup"><span data-stu-id="5f9c8-122">One of the values "x86", "amd64", "msil", or "ia64", specifying the processor architecture for an assembly that contains processor-specific code.</span></span> <span data-ttu-id="5f9c8-123">Les valeurs ne respectent pas la casse.</span><span class="sxs-lookup"><span data-stu-id="5f9c8-123">The values are not case-sensitive.</span></span> <span data-ttu-id="5f9c8-124">Si l’attribut est assigné à une autre valeur, l’ensemble `<assemblyIdentity>` élément est ignoré.</span><span class="sxs-lookup"><span data-stu-id="5f9c8-124">If the attribute is assigned any other value, the entire `<assemblyIdentity>` element is ignored.</span></span> <span data-ttu-id="5f9c8-125">Consultez <xref:System.Reflection.ProcessorArchitecture>.</span><span class="sxs-lookup"><span data-stu-id="5f9c8-125">See <xref:System.Reflection.ProcessorArchitecture>.</span></span>|  
  
## <a name="processorarchitecture-attribute"></a><span data-ttu-id="5f9c8-126">processorArchitecture attribut</span><span class="sxs-lookup"><span data-stu-id="5f9c8-126">processorArchitecture Attribute</span></span>  
  
|<span data-ttu-id="5f9c8-127">Value</span><span class="sxs-lookup"><span data-stu-id="5f9c8-127">Value</span></span>|<span data-ttu-id="5f9c8-128">Description</span><span class="sxs-lookup"><span data-stu-id="5f9c8-128">Description</span></span>|  
|-----------|-----------------|  
|`amd64`|<span data-ttu-id="5f9c8-129">AMD 64 x86 uniquement à l’architecture.</span><span class="sxs-lookup"><span data-stu-id="5f9c8-129">AMD x86-64 architecture only.</span></span>|  
|`ia64`|<span data-ttu-id="5f9c8-130">Uniquement à l’architecture Intel Itanium.</span><span class="sxs-lookup"><span data-stu-id="5f9c8-130">Intel Itanium architecture only.</span></span>|  
|`msil`|<span data-ttu-id="5f9c8-131">Neutre en ce qui concerne le processeur et bits par mot.</span><span class="sxs-lookup"><span data-stu-id="5f9c8-131">Neutral with respect to processor and bits-per-word.</span></span>|  
|`x86`|<span data-ttu-id="5f9c8-132">Un x86 32 bits processeur, natif ou dans le Windows sur l’environnement Windows (WOW) sur une plateforme 64 bits.</span><span class="sxs-lookup"><span data-stu-id="5f9c8-132">A 32-bit x86 processor, either native or in the Windows on Windows (WOW) environment on a 64-bit platform.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="5f9c8-133">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="5f9c8-133">Child Elements</span></span>  
 <span data-ttu-id="5f9c8-134">Aucun.</span><span class="sxs-lookup"><span data-stu-id="5f9c8-134">None.</span></span>  
  
### <a name="parent-elements"></a><span data-ttu-id="5f9c8-135">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="5f9c8-135">Parent Elements</span></span>  
  
|<span data-ttu-id="5f9c8-136">Élément</span><span class="sxs-lookup"><span data-stu-id="5f9c8-136">Element</span></span>|<span data-ttu-id="5f9c8-137">Description</span><span class="sxs-lookup"><span data-stu-id="5f9c8-137">Description</span></span>|  
|-------------|-----------------|  
|`assemblyBinding`|<span data-ttu-id="5f9c8-138">Contient des informations à propos de la redirection des versions d'assemblys et de l'emplacement de ces derniers.</span><span class="sxs-lookup"><span data-stu-id="5f9c8-138">Contains information about assembly version redirection and the locations of assemblies.</span></span>|  
|`configuration`|<span data-ttu-id="5f9c8-139">Élément racine de chaque fichier de configuration utilisé par le Common Language Runtime et les applications .NET Framework.</span><span class="sxs-lookup"><span data-stu-id="5f9c8-139">The root element in every configuration file used by the common language runtime and .NET Framework applications.</span></span>|  
|`dependentAssembly`|<span data-ttu-id="5f9c8-140">Encapsule la stratégie de liaisons et l’emplacement de chaque assembly.</span><span class="sxs-lookup"><span data-stu-id="5f9c8-140">Encapsulates binding policy and assembly location for each assembly.</span></span> <span data-ttu-id="5f9c8-141">Utilisez une `<dependentAssembly>` élément pour chaque assembly.</span><span class="sxs-lookup"><span data-stu-id="5f9c8-141">Use one `<dependentAssembly>` element for each assembly.</span></span>|  
|`runtime`|<span data-ttu-id="5f9c8-142">Contient des informations sur les liaisons d’assembly et l’opération garbage collection.</span><span class="sxs-lookup"><span data-stu-id="5f9c8-142">Contains information about assembly binding and garbage collection.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="5f9c8-143">Notes</span><span class="sxs-lookup"><span data-stu-id="5f9c8-143">Remarks</span></span>  
 <span data-ttu-id="5f9c8-144">Chaque  **\<dependentAssembly >** élément doit avoir un  **\<assemblyIdentity >** élément enfant.</span><span class="sxs-lookup"><span data-stu-id="5f9c8-144">Every **\<dependentAssembly>** element must have one **\<assemblyIdentity>** child element.</span></span>  
  
 <span data-ttu-id="5f9c8-145">Si le `processorArchitecture` attribut n’est présent, le `<assemblyIdentity>` élément s’applique uniquement à l’assembly avec l’architecture de processeur correspondant.</span><span class="sxs-lookup"><span data-stu-id="5f9c8-145">If the `processorArchitecture` attribute is present, the `<assemblyIdentity>` element applies only to the assembly with the corresponding processor architecture.</span></span> <span data-ttu-id="5f9c8-146">Si le `processorArchitecture` attribut n’est pas présent, le `<assemblyIdentity>` élément peut s’appliquer à un assembly avec une architecture de processeur.</span><span class="sxs-lookup"><span data-stu-id="5f9c8-146">If the `processorArchitecture` attribute is not present, the `<assemblyIdentity>` element can apply to an assembly with any processor architecture.</span></span>  
  
 <span data-ttu-id="5f9c8-147">L’exemple suivant montre un fichier de configuration pour les deux assemblys portant le même nom qui ciblent deux architectures de processeur de deux différentes, et dont les versions n’ont pas été préservées restent synchronisées. Lorsque l’application s’exécute sur le x86 plate-forme le premier `<assemblyIdentity>` élément s’applique et l’autre est ignorée.</span><span class="sxs-lookup"><span data-stu-id="5f9c8-147">The following example shows a configuration file for two assemblies with the same name that target two different two processor architectures, and whose versions have not been maintained in synch. When the application executes on the x86 platform the first `<assemblyIdentity>` element applies and the other is ignored.</span></span> <span data-ttu-id="5f9c8-148">Si l’application s’exécute sur une plateforme différente x86 ou ia64, les deux sont ignorés.</span><span class="sxs-lookup"><span data-stu-id="5f9c8-148">If the application executes on a platform other than x86 or ia64, both are ignored.</span></span>  
  
```xml  
<configuration>  
   <runtime>  
      <assemblyBinding xmlns="urn:schemas-microsoft-com:asm.v1">  
         <dependentAssembly>  
            <assemblyIdentity name="MyAssembly"  
                  publicKeyToken="14a739be0244c389"  
                  culture="neutral"  
                  processorArchitecture="x86" />  
            <bindingRedirect oldVersion= "1.0.0.0"   
                  newVersion="1.1.0.0" />  
         </dependentAssembly>  
         <dependentAssembly>  
            <assemblyIdentity name="MyAssembly"  
                  publicKeyToken="14a739be0244c389"  
                  culture="neutral"   
                  processorArchitecture="ia64" />  
            <bindingRedirect oldVersion="1.0.0.0"   
                  newVersion="2.0.0.0" />  
         </dependentAssembly>  
      </assemblyBinding>  
   </runtime>  
</configuration>  
```  
  
 <span data-ttu-id="5f9c8-149">Si un fichier de configuration contient un `<assemblyIdentity>` élément sans `processorArchitecture` d’attribut et ne contient pas d’élément qui correspond à la plateforme, l’élément sans le `processorArchitecture` attribut est utilisé.</span><span class="sxs-lookup"><span data-stu-id="5f9c8-149">If a configuration file contains an `<assemblyIdentity>` element with no `processorArchitecture` attribute, and does not contain an element that matches the platform, the element without the `processorArchitecture` attribute is used.</span></span>  
  
## <a name="example"></a><span data-ttu-id="5f9c8-150">Exemple</span><span class="sxs-lookup"><span data-stu-id="5f9c8-150">Example</span></span>  
 <span data-ttu-id="5f9c8-151">L’exemple suivant montre comment fournir des informations relatives à un assembly.</span><span class="sxs-lookup"><span data-stu-id="5f9c8-151">The following example shows how to provide information about an assembly.</span></span>  
  
```xml  
<configuration>  
   <runtime>  
      <assemblyBinding xmlns="urn:schemas-microsoft-com:asm.v1">  
         <dependentAssembly>  
            <assemblyIdentity name="myAssembly"  
                              publicKeyToken="32ab4ba45e0a69a1"  
                              culture="neutral" />  
            <!--Redirection and codeBase policy for myAssembly.-->  
         </dependentAssembly>  
      </assemblyBinding>  
   </runtime>  
</configuration>  
```  
  
## <a name="see-also"></a><span data-ttu-id="5f9c8-152">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="5f9c8-152">See also</span></span>

- [<span data-ttu-id="5f9c8-153">Schéma des paramètres d’exécution</span><span class="sxs-lookup"><span data-stu-id="5f9c8-153">Runtime Settings Schema</span></span>](../../../../../docs/framework/configure-apps/file-schema/runtime/index.md)
- [<span data-ttu-id="5f9c8-154">Schéma des fichiers de configuration</span><span class="sxs-lookup"><span data-stu-id="5f9c8-154">Configuration File Schema</span></span>](../../../../../docs/framework/configure-apps/file-schema/index.md)
- [<span data-ttu-id="5f9c8-155">Redirection des versions d'assemblys</span><span class="sxs-lookup"><span data-stu-id="5f9c8-155">Redirecting Assembly Versions</span></span>](../../../../../docs/framework/configure-apps/redirect-assembly-versions.md)
