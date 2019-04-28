---
title: Élément <appDomainManagerAssembly>
ms.date: 03/30/2017
helpviewer_keywords:
- <appDomainManagerAssembly> element
- appDomainManagerAssembly element
ms.assetid: c7c56e39-a700-44f5-b94e-411bfce339d9
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 4fe1dfbd62a6967ae51031fa12f80e9c5563dc44
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61704919"
---
# <a name="appdomainmanagerassembly-element"></a><span data-ttu-id="868a0-102">\<appDomainManagerAssembly> Element</span><span class="sxs-lookup"><span data-stu-id="868a0-102">\<appDomainManagerAssembly> Element</span></span>
<span data-ttu-id="868a0-103">Spécifie l’assembly qui fournit le Gestionnaire du domaine d’application par défaut du processus.</span><span class="sxs-lookup"><span data-stu-id="868a0-103">Specifies the assembly that provides the application domain manager for the default application domain in the process.</span></span>  
  
 <span data-ttu-id="868a0-104">\<configuration></span><span class="sxs-lookup"><span data-stu-id="868a0-104">\<configuration></span></span>  
<span data-ttu-id="868a0-105">\<runtime></span><span class="sxs-lookup"><span data-stu-id="868a0-105">\<runtime></span></span>  
<span data-ttu-id="868a0-106">\<appDomainManagerAssembly></span><span class="sxs-lookup"><span data-stu-id="868a0-106">\<appDomainManagerAssembly></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="868a0-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="868a0-107">Syntax</span></span>  
  
```xml  
<appDomainManagerAssembly   
   value="assembly display name" />  
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="868a0-108">Attributs et éléments</span><span class="sxs-lookup"><span data-stu-id="868a0-108">Attributes and Elements</span></span>  
 <span data-ttu-id="868a0-109">Les sections suivantes décrivent des attributs, des éléments enfants et des éléments parents.</span><span class="sxs-lookup"><span data-stu-id="868a0-109">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="868a0-110">Attributs</span><span class="sxs-lookup"><span data-stu-id="868a0-110">Attributes</span></span>  
  
|<span data-ttu-id="868a0-111">Attribut</span><span class="sxs-lookup"><span data-stu-id="868a0-111">Attribute</span></span>|<span data-ttu-id="868a0-112">Description</span><span class="sxs-lookup"><span data-stu-id="868a0-112">Description</span></span>|  
|---------------|-----------------|  
|`value`|<span data-ttu-id="868a0-113">Attribut requis.</span><span class="sxs-lookup"><span data-stu-id="868a0-113">Required attribute.</span></span> <span data-ttu-id="868a0-114">Spécifie le nom complet de l’assembly qui fournit le Gestionnaire de domaine d’application pour le domaine d’application par défaut dans le processus.</span><span class="sxs-lookup"><span data-stu-id="868a0-114">Specifies the display name of the assembly that provides the application domain manager for the default application domain in the process.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="868a0-115">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="868a0-115">Child Elements</span></span>  
 <span data-ttu-id="868a0-116">Aucun.</span><span class="sxs-lookup"><span data-stu-id="868a0-116">None.</span></span>  
  
### <a name="parent-elements"></a><span data-ttu-id="868a0-117">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="868a0-117">Parent Elements</span></span>  
  
|<span data-ttu-id="868a0-118">Élément</span><span class="sxs-lookup"><span data-stu-id="868a0-118">Element</span></span>|<span data-ttu-id="868a0-119">Description</span><span class="sxs-lookup"><span data-stu-id="868a0-119">Description</span></span>|  
|-------------|-----------------|  
|`configuration`|<span data-ttu-id="868a0-120">Élément racine de chaque fichier de configuration utilisé par le Common Language Runtime et les applications .NET Framework.</span><span class="sxs-lookup"><span data-stu-id="868a0-120">The root element in every configuration file used by the common language runtime and .NET Framework applications.</span></span>|  
|`runtime`|<span data-ttu-id="868a0-121">Contient des informations sur les liaisons d’assembly et l’opération garbage collection.</span><span class="sxs-lookup"><span data-stu-id="868a0-121">Contains information about assembly binding and garbage collection.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="868a0-122">Notes</span><span class="sxs-lookup"><span data-stu-id="868a0-122">Remarks</span></span>  
 <span data-ttu-id="868a0-123">Pour spécifier le type du Gestionnaire de domaine, vous devez spécifier cet élément et le [ \<appDomainManagerType >](../../../../../docs/framework/configure-apps/file-schema/runtime/appdomainmanagertype-element.md) élément.</span><span class="sxs-lookup"><span data-stu-id="868a0-123">To specify the type of the application domain manager, you must specify both this element and the [\<appDomainManagerType>](../../../../../docs/framework/configure-apps/file-schema/runtime/appdomainmanagertype-element.md) element.</span></span> <span data-ttu-id="868a0-124">Si un de ces éléments n’est pas spécifié, l’autre est ignorée.</span><span class="sxs-lookup"><span data-stu-id="868a0-124">If either of these elements is not specified, the other is ignored.</span></span>  
  
 <span data-ttu-id="868a0-125">Lorsque le domaine d’application par défaut est chargé, <xref:System.TypeLoadException> est levée si l’assembly spécifié n’existe pas ou si l’assembly ne contient pas le type spécifié par le [ \<appDomainManagerType >](../../../../../docs/framework/configure-apps/file-schema/runtime/appdomainmanagertype-element.md) élément ; et le processus ne parvient pas à démarrer.</span><span class="sxs-lookup"><span data-stu-id="868a0-125">When the default application domain is loaded, <xref:System.TypeLoadException> is thrown if the specified assembly does not exist or if the assembly does not contain the type specified by the [\<appDomainManagerType>](../../../../../docs/framework/configure-apps/file-schema/runtime/appdomainmanagertype-element.md) element; and the process fails to start.</span></span> <span data-ttu-id="868a0-126">Si l’assembly est trouvé, mais les informations de version ne correspondent pas, un <xref:System.IO.FileLoadException> est levée.</span><span class="sxs-lookup"><span data-stu-id="868a0-126">If the assembly is found but the version information does not match, a <xref:System.IO.FileLoadException> is thrown.</span></span>  
  
 <span data-ttu-id="868a0-127">Lorsque vous spécifiez le type de gestionnaire de domaine application pour le domaine d’application par défaut, les autres domaines d’application créés à partir du domaine d’application par défaut héritent le type de gestionnaire de domaine application.</span><span class="sxs-lookup"><span data-stu-id="868a0-127">When you specify the application domain manager type for the default application domain, other application domains created from the default application domain inherit the application domain manager type.</span></span> <span data-ttu-id="868a0-128">Utilisez le <xref:System.AppDomainSetup.AppDomainManagerType%2A?displayProperty=nameWithType> et <xref:System.AppDomainSetup.AppDomainManagerAssembly%2A?displayProperty=nameWithType> propriétés pour spécifier un type de gestionnaire de domaine d’application pour un nouveau domaine d’application.</span><span class="sxs-lookup"><span data-stu-id="868a0-128">Use the <xref:System.AppDomainSetup.AppDomainManagerType%2A?displayProperty=nameWithType> and <xref:System.AppDomainSetup.AppDomainManagerAssembly%2A?displayProperty=nameWithType> properties to specify a different application domain manager type for a new application domain.</span></span>  
  
 <span data-ttu-id="868a0-129">En spécifiant le type de gestionnaire de domaine application nécessite l’application ait une confiance totale.</span><span class="sxs-lookup"><span data-stu-id="868a0-129">Specifying the application domain manager type requires the application to have full trust.</span></span> <span data-ttu-id="868a0-130">(Par exemple, une application en cours d’exécution sur le bureau a une confiance totale.) Si l’application n’a pas une confiance totale, un <xref:System.TypeLoadException> est levée.</span><span class="sxs-lookup"><span data-stu-id="868a0-130">(For example, an application running on the desktop has full trust.) If the application does not have full trust, a <xref:System.TypeLoadException> is thrown.</span></span>  
  
 <span data-ttu-id="868a0-131">Pour le format du nom complet d’assembly, consultez le <xref:System.Reflection.Assembly.FullName%2A?displayProperty=nameWithType> propriété.</span><span class="sxs-lookup"><span data-stu-id="868a0-131">For the format of the assembly display name, see the <xref:System.Reflection.Assembly.FullName%2A?displayProperty=nameWithType> property.</span></span>  
  
 <span data-ttu-id="868a0-132">Cet élément de configuration est disponible uniquement dans le [!INCLUDE[net_v40_long](../../../../../includes/net-v40-long-md.md)] et versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="868a0-132">This configuration element is available only in the [!INCLUDE[net_v40_long](../../../../../includes/net-v40-long-md.md)] and later.</span></span>  
  
## <a name="example"></a><span data-ttu-id="868a0-133">Exemple</span><span class="sxs-lookup"><span data-stu-id="868a0-133">Example</span></span>  
 <span data-ttu-id="868a0-134">L’exemple suivant montre comment spécifier que le Gestionnaire de domaine d’application pour le domaine d’application par défaut d’un processus est le `MyMgr` tapez dans le `AdMgrExample` assembly.</span><span class="sxs-lookup"><span data-stu-id="868a0-134">The following example shows how to specify that the application domain manager for the default application domain of a process is the `MyMgr` type in the `AdMgrExample` assembly.</span></span>  
  
```xml  
<configuration>  
   <runtime>  
      <appDomainManagerType value="MyMgr" />  
      <appDomainManagerAssembly   
         value="AdMgrExample, Version=1.0.0.0, Culture=neutral, PublicKeyToken=6856bccf150f00b3" />  
   </runtime>  
</configuration>  
```  
  
## <a name="see-also"></a><span data-ttu-id="868a0-135">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="868a0-135">See also</span></span>

- <xref:System.AppDomainSetup.AppDomainManagerType%2A?displayProperty=nameWithType>
- <xref:System.AppDomainSetup.AppDomainManagerAssembly%2A?displayProperty=nameWithType>
- [<span data-ttu-id="868a0-136">\<appDomainManagerType > élément</span><span class="sxs-lookup"><span data-stu-id="868a0-136">\<appDomainManagerType> Element</span></span>](../../../../../docs/framework/configure-apps/file-schema/runtime/appdomainmanagertype-element.md)
- [<span data-ttu-id="868a0-137">Schéma des paramètres d’exécution</span><span class="sxs-lookup"><span data-stu-id="868a0-137">Runtime Settings Schema</span></span>](../../../../../docs/framework/configure-apps/file-schema/runtime/index.md)
- [<span data-ttu-id="868a0-138">Schéma des fichiers de configuration</span><span class="sxs-lookup"><span data-stu-id="868a0-138">Configuration File Schema</span></span>](../../../../../docs/framework/configure-apps/file-schema/index.md)
- [<span data-ttu-id="868a0-139">SetAppDomainManagerType, méthode</span><span class="sxs-lookup"><span data-stu-id="868a0-139">SetAppDomainManagerType Method</span></span>](../../../../../docs/framework/unmanaged-api/hosting/iclrcontrol-setappdomainmanagertype-method.md)
