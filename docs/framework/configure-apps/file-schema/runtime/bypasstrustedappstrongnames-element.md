---
title: Élément <bypassTrustedAppStrongNames>
ms.date: 03/30/2017
helpviewer_keywords:
- strong-name bypass feature
- bypassTrustedAppStrongNames element
- strong-named assemblies, loading into trusted application domains
- <bypassTrustedAppStrongNames> element
ms.assetid: 71b2ebf6-3843-41e2-ad52-ffa5cd083a40
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 6c39d9a1e3da9cccb2f027e9597a6f2272d187ec
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61674205"
---
# <a name="bypasstrustedappstrongnames-element"></a><span data-ttu-id="6ff10-102">\<bypassTrustedAppStrongNames>, élément</span><span class="sxs-lookup"><span data-stu-id="6ff10-102">\<bypassTrustedAppStrongNames> Element</span></span>
<span data-ttu-id="6ff10-103">Spécifie s’il faut ignorer la validation des noms forts sur les assemblys de confiance totale sont chargés dans un niveau de confiance totale <xref:System.AppDomain>.</span><span class="sxs-lookup"><span data-stu-id="6ff10-103">Specifies whether to bypass the validation of strong names on full-trust assemblies that are loaded into a full-trust <xref:System.AppDomain>.</span></span>  
  
 <span data-ttu-id="6ff10-104">\<configuration></span><span class="sxs-lookup"><span data-stu-id="6ff10-104">\<configuration></span></span>  
<span data-ttu-id="6ff10-105">\<runtime></span><span class="sxs-lookup"><span data-stu-id="6ff10-105">\<runtime></span></span>  
<span data-ttu-id="6ff10-106">\<bypassTrustedAppStrongNames></span><span class="sxs-lookup"><span data-stu-id="6ff10-106">\<bypassTrustedAppStrongNames></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="6ff10-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="6ff10-107">Syntax</span></span>  
  
```xml  
<bypassTrustedAppStrongNames    
   enabled="true|false"/>  
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="6ff10-108">Attributs et éléments</span><span class="sxs-lookup"><span data-stu-id="6ff10-108">Attributes and Elements</span></span>  
 <span data-ttu-id="6ff10-109">Les sections suivantes décrivent des attributs, des éléments enfants et des éléments parents.</span><span class="sxs-lookup"><span data-stu-id="6ff10-109">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="6ff10-110">Attributs</span><span class="sxs-lookup"><span data-stu-id="6ff10-110">Attributes</span></span>  
  
|<span data-ttu-id="6ff10-111">Attribut</span><span class="sxs-lookup"><span data-stu-id="6ff10-111">Attribute</span></span>|<span data-ttu-id="6ff10-112">Description</span><span class="sxs-lookup"><span data-stu-id="6ff10-112">Description</span></span>|  
|---------------|-----------------|  
|`enabled`|<span data-ttu-id="6ff10-113">Attribut requis.</span><span class="sxs-lookup"><span data-stu-id="6ff10-113">Required attribute.</span></span><br /><br /> <span data-ttu-id="6ff10-114">Spécifie si la fonctionnalité de contournement qui évite la validation des noms forts pour les assemblys de confiance totale est activée.</span><span class="sxs-lookup"><span data-stu-id="6ff10-114">Specifies whether the bypass feature that avoids validating strong names for full-trust assemblies is enabled.</span></span> <span data-ttu-id="6ff10-115">Lorsque cette fonctionnalité est activée, les noms forts ne sont pas validés est correcte lors de l’assembly est chargé.</span><span class="sxs-lookup"><span data-stu-id="6ff10-115">When this feature is enabled, strong names are not validated for correctness when the assembly is loaded.</span></span> <span data-ttu-id="6ff10-116">La valeur par défaut est `true`.</span><span class="sxs-lookup"><span data-stu-id="6ff10-116">The default is `true`.</span></span>|  
  
## <a name="enabled-attribute"></a><span data-ttu-id="6ff10-117">Attribut enabled</span><span class="sxs-lookup"><span data-stu-id="6ff10-117">enabled Attribute</span></span>  
  
|<span data-ttu-id="6ff10-118">Value</span><span class="sxs-lookup"><span data-stu-id="6ff10-118">Value</span></span>|<span data-ttu-id="6ff10-119">Description</span><span class="sxs-lookup"><span data-stu-id="6ff10-119">Description</span></span>|  
|-----------|-----------------|  
|`true`|<span data-ttu-id="6ff10-120">Les signatures avec nom fort sur les assemblys de confiance totale ne sont pas validées lorsque les assemblys sont chargés dans un niveau de confiance totale <xref:System.AppDomain>.</span><span class="sxs-lookup"><span data-stu-id="6ff10-120">Strong-name signatures on full-trust assemblies are not validated when the assemblies are loaded into a full-trust <xref:System.AppDomain>.</span></span> <span data-ttu-id="6ff10-121">Il s'agit de la valeur par défaut.</span><span class="sxs-lookup"><span data-stu-id="6ff10-121">This is the default.</span></span>|  
|`false`|<span data-ttu-id="6ff10-122">Les signatures avec nom fort sur les assemblys de confiance totale sont validées lorsque les assemblys sont chargés dans un niveau de confiance totale <xref:System.AppDomain>.</span><span class="sxs-lookup"><span data-stu-id="6ff10-122">Strong-name signatures on full-trust assemblies are validated when the assemblies are loaded into a full-trust <xref:System.AppDomain>.</span></span> <span data-ttu-id="6ff10-123">La signature de nom fort est vérifiée uniquement pour l’exactitude de la signature ; Il n’est pas comparée à un autre nom fort pour une correspondance.</span><span class="sxs-lookup"><span data-stu-id="6ff10-123">The strong-name signature is checked only for signature correctness; it is not compared to another strong name for a match.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="6ff10-124">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="6ff10-124">Child Elements</span></span>  
 <span data-ttu-id="6ff10-125">Aucun.</span><span class="sxs-lookup"><span data-stu-id="6ff10-125">None.</span></span>  
  
### <a name="parent-elements"></a><span data-ttu-id="6ff10-126">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="6ff10-126">Parent Elements</span></span>  
  
|<span data-ttu-id="6ff10-127">Élément</span><span class="sxs-lookup"><span data-stu-id="6ff10-127">Element</span></span>|<span data-ttu-id="6ff10-128">Description</span><span class="sxs-lookup"><span data-stu-id="6ff10-128">Description</span></span>|  
|-------------|-----------------|  
|`configuration`|<span data-ttu-id="6ff10-129">Élément racine de chaque fichier de configuration utilisé par le Common Language Runtime et les applications .NET Framework.</span><span class="sxs-lookup"><span data-stu-id="6ff10-129">The root element in every configuration file used by the common language runtime and .NET Framework applications.</span></span>|  
|`runtime`|<span data-ttu-id="6ff10-130">Contient des informations sur les liaisons d’assembly et l’opération garbage collection.</span><span class="sxs-lookup"><span data-stu-id="6ff10-130">Contains information about assembly binding and garbage collection.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="6ff10-131">Notes</span><span class="sxs-lookup"><span data-stu-id="6ff10-131">Remarks</span></span>  
 <span data-ttu-id="6ff10-132">La fonctionnalité de contournement de noms forts évite la surcharge liée à la vérification de signature de nom fort des assemblys de confiance totale.</span><span class="sxs-lookup"><span data-stu-id="6ff10-132">The strong-name bypass feature avoids the overhead of strong-name signature verification of full-trust assemblies.</span></span>  
  
 <span data-ttu-id="6ff10-133">Cette fonctionnalité s'applique à tout assembly signé avec un nom fort qui présente les caractéristiques suivantes :</span><span class="sxs-lookup"><span data-stu-id="6ff10-133">The bypass feature applies to any assembly that is signed with a strong name and that has the following characteristics:</span></span>  
  
- <span data-ttu-id="6ff10-134">Confiance totale sans la <xref:System.Security.Policy.StrongName> preuves (par exemple, a `MyComputer` preuve de zone).</span><span class="sxs-lookup"><span data-stu-id="6ff10-134">Fully trusted without the <xref:System.Security.Policy.StrongName> evidence (for example, has `MyComputer` zone evidence).</span></span>  
  
- <span data-ttu-id="6ff10-135">Chargé dans un <xref:System.AppDomain> de confiance totale.</span><span class="sxs-lookup"><span data-stu-id="6ff10-135">Loaded into a fully trusted <xref:System.AppDomain>.</span></span>  
  
- <span data-ttu-id="6ff10-136">Chargé à partir d'un emplacement sous la propriété <xref:System.AppDomainSetup.ApplicationBase%2A> de cet <xref:System.AppDomain>.</span><span class="sxs-lookup"><span data-stu-id="6ff10-136">Loaded from a location under the <xref:System.AppDomainSetup.ApplicationBase%2A> property of that <xref:System.AppDomain>.</span></span>  
  
- <span data-ttu-id="6ff10-137">Sans signature différée.</span><span class="sxs-lookup"><span data-stu-id="6ff10-137">Not delay-signed.</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="6ff10-138">Si cette fonctionnalité a été désactivée pour toutes les applications sur l’ordinateur à l’aide d’une clé de Registre, ce paramètre de fichier de configuration n’a aucun effet.</span><span class="sxs-lookup"><span data-stu-id="6ff10-138">If the bypass feature has been turned off for all applications on the computer by using a registry key, this configuration file setting has no effect.</span></span> <span data-ttu-id="6ff10-139">Pour plus d'informations, voir [Procédure : Désactiver la fonctionnalité consistant à ignorer les noms forts](../../../../../docs/framework/app-domains/how-to-disable-the-strong-name-bypass-feature.md).</span><span class="sxs-lookup"><span data-stu-id="6ff10-139">For more information, see [How to: Disable the Strong-Name Bypass Feature](../../../../../docs/framework/app-domains/how-to-disable-the-strong-name-bypass-feature.md).</span></span>  
  
## <a name="example"></a><span data-ttu-id="6ff10-140">Exemple</span><span class="sxs-lookup"><span data-stu-id="6ff10-140">Example</span></span>  
 <span data-ttu-id="6ff10-141">L’exemple suivant montre comment spécifier le comportement qui valide la signature de nom fort sur les assemblys de confiance totale.</span><span class="sxs-lookup"><span data-stu-id="6ff10-141">The following example shows how to specify the behavior that validates the strong-name signature on full-trust assemblies.</span></span>  
  
```xml  
<configuration>  
   <runtime>  
      <bypassTrustedAppStrongNames enabled="false"/>  
   </runtime>  
</configuration>  
```  
  
## <a name="see-also"></a><span data-ttu-id="6ff10-142">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="6ff10-142">See also</span></span>

- [<span data-ttu-id="6ff10-143">Schéma des paramètres d’exécution</span><span class="sxs-lookup"><span data-stu-id="6ff10-143">Runtime Settings Schema</span></span>](../../../../../docs/framework/configure-apps/file-schema/runtime/index.md)
- [<span data-ttu-id="6ff10-144">Schéma des fichiers de configuration</span><span class="sxs-lookup"><span data-stu-id="6ff10-144">Configuration File Schema</span></span>](../../../../../docs/framework/configure-apps/file-schema/index.md)
- [<span data-ttu-id="6ff10-145">Guide pratique pour désactiver la fonctionnalité consistant à ignorer les noms forts</span><span class="sxs-lookup"><span data-stu-id="6ff10-145">How to: Disable the Strong-Name Bypass Feature</span></span>](../../../../../docs/framework/app-domains/how-to-disable-the-strong-name-bypass-feature.md)
