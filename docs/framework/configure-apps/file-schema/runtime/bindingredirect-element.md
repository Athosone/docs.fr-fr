---
title: Élément <bindingRedirect>
ms.date: 03/30/2017
f1_keywords:
- http://schemas.microsoft.com/.NetConfiguration/v2.0#configuration/runtime/assemblyBinding/dependentAssembly/bindingRedirect
- http://schemas.microsoft.com/.NetConfiguration/v2.0#bindingRedirect
helpviewer_keywords:
- <bindingRedirect> element
- container tags, <bindingRedirect> element
- bindingRedirect element
ms.assetid: 67784ecd-9663-434e-bd6a-26975e447ac0
ms.openlocfilehash: dda99bb4b96efbdd274e24e7cd548e4ed4df8b66
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59185911"
---
# <a name="bindingredirect-element"></a><span data-ttu-id="6ccde-102">\<bindingRedirect > élément</span><span class="sxs-lookup"><span data-stu-id="6ccde-102">\<bindingRedirect> Element</span></span>
<span data-ttu-id="6ccde-103">Redirige une version d'assembly vers une autre.</span><span class="sxs-lookup"><span data-stu-id="6ccde-103">Redirects one assembly version to another.</span></span>  
  
 <span data-ttu-id="6ccde-104">\<configuration></span><span class="sxs-lookup"><span data-stu-id="6ccde-104">\<configuration></span></span>  
<span data-ttu-id="6ccde-105">\<runtime></span><span class="sxs-lookup"><span data-stu-id="6ccde-105">\<runtime></span></span>  
<span data-ttu-id="6ccde-106">\<assemblyBinding></span><span class="sxs-lookup"><span data-stu-id="6ccde-106">\<assemblyBinding></span></span>  
<span data-ttu-id="6ccde-107">\<dependentAssembly></span><span class="sxs-lookup"><span data-stu-id="6ccde-107">\<dependentAssembly></span></span>  
<span data-ttu-id="6ccde-108">\<bindingRedirect></span><span class="sxs-lookup"><span data-stu-id="6ccde-108">\<bindingRedirect></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="6ccde-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="6ccde-109">Syntax</span></span>  
  
```xml  
   <bindingRedirect    
oldVersion="existing assembly version"  
newVersion="new assembly version"/>  
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="6ccde-110">Attributs et éléments</span><span class="sxs-lookup"><span data-stu-id="6ccde-110">Attributes and Elements</span></span>  
 <span data-ttu-id="6ccde-111">Les sections suivantes décrivent des attributs, des éléments enfants et des éléments parents.</span><span class="sxs-lookup"><span data-stu-id="6ccde-111">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="6ccde-112">Attributs</span><span class="sxs-lookup"><span data-stu-id="6ccde-112">Attributes</span></span>  
  
|<span data-ttu-id="6ccde-113">Attribut</span><span class="sxs-lookup"><span data-stu-id="6ccde-113">Attribute</span></span>|<span data-ttu-id="6ccde-114">Description</span><span class="sxs-lookup"><span data-stu-id="6ccde-114">Description</span></span>|  
|---------------|-----------------|  
|`oldVersion`|<span data-ttu-id="6ccde-115">Attribut requis.</span><span class="sxs-lookup"><span data-stu-id="6ccde-115">Required attribute.</span></span><br /><br /> <span data-ttu-id="6ccde-116">Spécifie la version de l'assembly demandée initialement.</span><span class="sxs-lookup"><span data-stu-id="6ccde-116">Specifies the version of the assembly that was originally requested.</span></span> <span data-ttu-id="6ccde-117">Le format du numéro de version est *major.minor.build.revision*.</span><span class="sxs-lookup"><span data-stu-id="6ccde-117">The format of an assembly version number is *major.minor.build.revision*.</span></span> <span data-ttu-id="6ccde-118">Les valeurs valides pour chaque partie de ce numéro de version vont de 0 à 65535.</span><span class="sxs-lookup"><span data-stu-id="6ccde-118">Valid values for each part of this version number are 0 to 65535.</span></span><br /><br /> <span data-ttu-id="6ccde-119">Vous pouvez également spécifier une plage de versions en respectant le format suivant :</span><span class="sxs-lookup"><span data-stu-id="6ccde-119">You can also specify a range of versions in the following format:</span></span><br /><br /> <span data-ttu-id="6ccde-120">*n.n.n.n - n.n.n.n*</span><span class="sxs-lookup"><span data-stu-id="6ccde-120">*n.n.n.n - n.n.n.n*</span></span>|  
|`newVersion`|<span data-ttu-id="6ccde-121">Attribut requis.</span><span class="sxs-lookup"><span data-stu-id="6ccde-121">Required attribute.</span></span><br /><br /> <span data-ttu-id="6ccde-122">Spécifie la version de l’assembly à utiliser au lieu de la version initialement demandée dans le format : *n.n.n.n*</span><span class="sxs-lookup"><span data-stu-id="6ccde-122">Specifies the version of the assembly to use instead of the originally requested version in the format: *n.n.n.n*</span></span><br /><br /> <span data-ttu-id="6ccde-123">Cette valeur peut spécifier une version antérieure à `oldVersion`.</span><span class="sxs-lookup"><span data-stu-id="6ccde-123">This value can specify an earlier version than `oldVersion`.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="6ccde-124">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="6ccde-124">Child Elements</span></span>  
  
|<span data-ttu-id="6ccde-125">Élément</span><span class="sxs-lookup"><span data-stu-id="6ccde-125">Element</span></span>|<span data-ttu-id="6ccde-126">Description</span><span class="sxs-lookup"><span data-stu-id="6ccde-126">Description</span></span>|  
|-------------|-----------------|  
|<span data-ttu-id="6ccde-127">Aucun.</span><span class="sxs-lookup"><span data-stu-id="6ccde-127">None</span></span>||  
  
### <a name="parent-elements"></a><span data-ttu-id="6ccde-128">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="6ccde-128">Parent Elements</span></span>  
  
|<span data-ttu-id="6ccde-129">Élément</span><span class="sxs-lookup"><span data-stu-id="6ccde-129">Element</span></span>|<span data-ttu-id="6ccde-130">Description</span><span class="sxs-lookup"><span data-stu-id="6ccde-130">Description</span></span>|  
|-------------|-----------------|  
|`assemblyBinding`|<span data-ttu-id="6ccde-131">Contient des informations à propos de la redirection des versions d'assemblys et de l'emplacement de ces derniers.</span><span class="sxs-lookup"><span data-stu-id="6ccde-131">Contains information about assembly version redirection and the locations of assemblies.</span></span>|  
|`configuration`|<span data-ttu-id="6ccde-132">Élément racine de chaque fichier de configuration utilisé par le Common Language Runtime et les applications .NET Framework.</span><span class="sxs-lookup"><span data-stu-id="6ccde-132">The root element in every configuration file used by the common language runtime and .NET Framework applications.</span></span>|  
|`dependentAssembly`|<span data-ttu-id="6ccde-133">Encapsule la stratégie de liaisons et l’emplacement de chaque assembly.</span><span class="sxs-lookup"><span data-stu-id="6ccde-133">Encapsulates binding policy and assembly location for each assembly.</span></span> <span data-ttu-id="6ccde-134">Utilisez un élément dependentAssembly pour chaque assembly.</span><span class="sxs-lookup"><span data-stu-id="6ccde-134">Use one dependentAssembly element for each assembly.</span></span>|  
|`runtime`|<span data-ttu-id="6ccde-135">Contient des informations sur les liaisons d’assembly et l’opération garbage collection.</span><span class="sxs-lookup"><span data-stu-id="6ccde-135">Contains information about assembly binding and garbage collection.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="6ccde-136">Notes</span><span class="sxs-lookup"><span data-stu-id="6ccde-136">Remarks</span></span>  
 <span data-ttu-id="6ccde-137">Lorsque vous générez une application .NET Framework basée sur un assembly avec nom fort, l'application utilise par défaut cette version de l'assembly au moment de l'exécution, même si une nouvelle version est disponible.</span><span class="sxs-lookup"><span data-stu-id="6ccde-137">When you build a .NET Framework application against a strong-named assembly, the application uses that version of the assembly at run time by default, even if a new version is available.</span></span> <span data-ttu-id="6ccde-138">Vous pouvez toutefois configurer l'application pour faire en sorte qu'elle s'exécute en utilisant une version plus récente de l'assembly.</span><span class="sxs-lookup"><span data-stu-id="6ccde-138">However, you can configure the application to run against a newer version of the assembly.</span></span> <span data-ttu-id="6ccde-139">Pour plus d’informations sur la façon dont le runtime utilise ces fichiers pour déterminer la version d’assembly à utiliser, consultez [méthode de localisation des assemblys par le Runtime](../../../../../docs/framework/deployment/how-the-runtime-locates-assemblies.md).</span><span class="sxs-lookup"><span data-stu-id="6ccde-139">For details on how the runtime uses these files to determine which assembly version to use, see [How the Runtime Locates Assemblies](../../../../../docs/framework/deployment/how-the-runtime-locates-assemblies.md).</span></span>  
  
 <span data-ttu-id="6ccde-140">Vous pouvez rediriger plusieurs versions d'assembly en incluant plusieurs éléments `bindingRedirect` dans un élément `dependentAssembly`.</span><span class="sxs-lookup"><span data-stu-id="6ccde-140">You can redirect more than one assembly version by including multiple `bindingRedirect` elements in a `dependentAssembly` element.</span></span> <span data-ttu-id="6ccde-141">Vous pouvez également rediriger une version plus récente vers une version antérieure de l'assembly.</span><span class="sxs-lookup"><span data-stu-id="6ccde-141">You can also redirect from a newer version to an older version of the assembly.</span></span>  
  
 <span data-ttu-id="6ccde-142">La redirection de liaison d’assembly explicite dans un fichier de configuration de l’application nécessite une autorisation de sécurité.</span><span class="sxs-lookup"><span data-stu-id="6ccde-142">Explicit assembly binding redirection in an application configuration file requires a security permission.</span></span> <span data-ttu-id="6ccde-143">Cela s'applique à la redirection des assemblys .NET Framework et des assemblys tiers.</span><span class="sxs-lookup"><span data-stu-id="6ccde-143">This applies to redirection of .NET Framework assemblies and assemblies from third parties.</span></span> <span data-ttu-id="6ccde-144">L’autorisation est accordée en définissant le <xref:System.Security.Permissions.SecurityPermissionFlag> indicateur sur le <xref:System.Security.Permissions.SecurityPermission>.</span><span class="sxs-lookup"><span data-stu-id="6ccde-144">The permission is granted by setting the <xref:System.Security.Permissions.SecurityPermissionFlag> flag on the <xref:System.Security.Permissions.SecurityPermission>.</span></span> <span data-ttu-id="6ccde-145">Pour plus d’informations, consultez [autorisation de sécurité pour la Redirection de liaison d’Assembly](../../../../../docs/framework/configure-apps/assembly-binding-redirection-security-permission.md).</span><span class="sxs-lookup"><span data-stu-id="6ccde-145">For more information, see [Assembly Binding Redirection Security Permission](../../../../../docs/framework/configure-apps/assembly-binding-redirection-security-permission.md).</span></span>  
  
## <a name="example"></a><span data-ttu-id="6ccde-146">Exemple</span><span class="sxs-lookup"><span data-stu-id="6ccde-146">Example</span></span>  
 <span data-ttu-id="6ccde-147">L'exemple suivant montre comment rediriger une version d'assembly vers une autre.</span><span class="sxs-lookup"><span data-stu-id="6ccde-147">The following example shows how to redirect one assembly version to another.</span></span>  
  
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
         </dependentAssembly>  
      </assemblyBinding>  
   </runtime>  
</configuration>  
```  
  
## <a name="see-also"></a><span data-ttu-id="6ccde-148">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="6ccde-148">See also</span></span>

- [<span data-ttu-id="6ccde-149">Schéma des paramètres d’exécution</span><span class="sxs-lookup"><span data-stu-id="6ccde-149">Runtime Settings Schema</span></span>](../../../../../docs/framework/configure-apps/file-schema/runtime/index.md)
- [<span data-ttu-id="6ccde-150">Schéma des fichiers de configuration</span><span class="sxs-lookup"><span data-stu-id="6ccde-150">Configuration File Schema</span></span>](../../../../../docs/framework/configure-apps/file-schema/index.md)
- [<span data-ttu-id="6ccde-151">Redirection des versions d'assemblys</span><span class="sxs-lookup"><span data-stu-id="6ccde-151">Redirecting Assembly Versions</span></span>](../../../../../docs/framework/configure-apps/redirect-assembly-versions.md)
