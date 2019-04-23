---
title: Élément <gcServer>
ms.date: 03/30/2017
f1_keywords:
- http://schemas.microsoft.com/.NetConfiguration/v2.0#configuration/runtime/gcServer
- http://schemas.microsoft.com/.NetConfiguration/v2.0#gcServer
helpviewer_keywords:
- gcServer element
- <gcServer> element
ms.assetid: 8d25b80e-2581-4803-bd87-a59528e3cb03
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: fd91cf0179ef9731c456b41fdc865e3eacdb33eb
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59132806"
---
# <a name="gcserver-element"></a><span data-ttu-id="45d30-102">\<< gcServer > élément</span><span class="sxs-lookup"><span data-stu-id="45d30-102">\<gcServer> Element</span></span>
<span data-ttu-id="45d30-103">Spécifie si le common language runtime exécute le garbage collection côté serveur.</span><span class="sxs-lookup"><span data-stu-id="45d30-103">Specifies whether the common language runtime runs server garbage collection.</span></span>  
  
 <span data-ttu-id="45d30-104">\<configuration></span><span class="sxs-lookup"><span data-stu-id="45d30-104">\<configuration></span></span>  
<span data-ttu-id="45d30-105">\<runtime></span><span class="sxs-lookup"><span data-stu-id="45d30-105">\<runtime></span></span>  
<span data-ttu-id="45d30-106">\<gcServer></span><span class="sxs-lookup"><span data-stu-id="45d30-106">\<gcServer></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="45d30-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="45d30-107">Syntax</span></span>  
  
```xml  
<gcServer    
   enabled="true|false"/>  
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="45d30-108">Attributs et éléments</span><span class="sxs-lookup"><span data-stu-id="45d30-108">Attributes and Elements</span></span>  
 <span data-ttu-id="45d30-109">Les sections suivantes décrivent des attributs, des éléments enfants et des éléments parents.</span><span class="sxs-lookup"><span data-stu-id="45d30-109">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="45d30-110">Attributs</span><span class="sxs-lookup"><span data-stu-id="45d30-110">Attributes</span></span>  
  
|<span data-ttu-id="45d30-111">Attribut</span><span class="sxs-lookup"><span data-stu-id="45d30-111">Attribute</span></span>|<span data-ttu-id="45d30-112">Description</span><span class="sxs-lookup"><span data-stu-id="45d30-112">Description</span></span>|  
|---------------|-----------------|  
|`enabled`|<span data-ttu-id="45d30-113">Attribut requis.</span><span class="sxs-lookup"><span data-stu-id="45d30-113">Required attribute.</span></span><br /><br /> <span data-ttu-id="45d30-114">Spécifie si le runtime exécute le garbage collection côté serveur.</span><span class="sxs-lookup"><span data-stu-id="45d30-114">Specifies whether the runtime runs server garbage collection.</span></span>|  
  
## <a name="enabled-attribute"></a><span data-ttu-id="45d30-115">Attribut enabled</span><span class="sxs-lookup"><span data-stu-id="45d30-115">enabled Attribute</span></span>  
  
|<span data-ttu-id="45d30-116">Value</span><span class="sxs-lookup"><span data-stu-id="45d30-116">Value</span></span>|<span data-ttu-id="45d30-117">Description</span><span class="sxs-lookup"><span data-stu-id="45d30-117">Description</span></span>|  
|-----------|-----------------|  
|`false`|<span data-ttu-id="45d30-118">N'exécute pas le garbage collection côté serveur.</span><span class="sxs-lookup"><span data-stu-id="45d30-118">Does not run server garbage collection.</span></span> <span data-ttu-id="45d30-119">Il s'agit de la valeur par défaut.</span><span class="sxs-lookup"><span data-stu-id="45d30-119">This is the default.</span></span>|  
|`true`|<span data-ttu-id="45d30-120">Exécute le garbage collection côté serveur.</span><span class="sxs-lookup"><span data-stu-id="45d30-120">Runs server garbage collection.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="45d30-121">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="45d30-121">Child Elements</span></span>  
 <span data-ttu-id="45d30-122">Aucun.</span><span class="sxs-lookup"><span data-stu-id="45d30-122">None.</span></span>  
  
### <a name="parent-elements"></a><span data-ttu-id="45d30-123">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="45d30-123">Parent Elements</span></span>  
  
|<span data-ttu-id="45d30-124">Élément</span><span class="sxs-lookup"><span data-stu-id="45d30-124">Element</span></span>|<span data-ttu-id="45d30-125">Description</span><span class="sxs-lookup"><span data-stu-id="45d30-125">Description</span></span>|  
|-------------|-----------------|  
|`configuration`|<span data-ttu-id="45d30-126">Élément racine de chaque fichier de configuration utilisé par le Common Language Runtime et les applications .NET Framework.</span><span class="sxs-lookup"><span data-stu-id="45d30-126">The root element in every configuration file used by the common language runtime and .NET Framework applications.</span></span>|  
|`runtime`|<span data-ttu-id="45d30-127">Contient des informations sur les liaisons d’assembly et l’opération garbage collection.</span><span class="sxs-lookup"><span data-stu-id="45d30-127">Contains information about assembly binding and garbage collection.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="45d30-128">Notes</span><span class="sxs-lookup"><span data-stu-id="45d30-128">Remarks</span></span>  
 <span data-ttu-id="45d30-129">Le common language runtime (ou CLR) prend en charge deux types de garbage collection : le garbage collection côté station de travail, qui est disponible sur tous les systèmes, et le garbage collection côté serveur, qui est disponible sur les systèmes multiprocesseurs.</span><span class="sxs-lookup"><span data-stu-id="45d30-129">The common language runtime (CLR) supports two types of garbage collection: workstation garbage collection, which is available on all systems, and server garbage collection, which is available on multiprocessor systems.</span></span> <span data-ttu-id="45d30-130">Utilisez l’élément `<gcServer>` pour contrôler le type de garbage collection effectué par le CLR.</span><span class="sxs-lookup"><span data-stu-id="45d30-130">You use the `<gcServer>` element to control the type of garbage collection the CLR performs.</span></span> <span data-ttu-id="45d30-131">Utilisez la propriété <xref:System.Runtime.GCSettings.IsServerGC%2A?displayProperty=nameWithType> pour déterminer si le garbage collection côté serveur est activé.</span><span class="sxs-lookup"><span data-stu-id="45d30-131">Use the <xref:System.Runtime.GCSettings.IsServerGC%2A?displayProperty=nameWithType> property to determine if server garbage collection is enabled.</span></span>  
  
 <span data-ttu-id="45d30-132">Pour les ordinateurs monoprocesseurs, le garbage collection côté station de travail configuré par défaut représente normalement l'option la plus rapide.</span><span class="sxs-lookup"><span data-stu-id="45d30-132">For single-processor computers, the default workstation garbage collection should be the fastest option.</span></span> <span data-ttu-id="45d30-133">L'option station de travail ou serveur peut être utilisée pour les ordinateurs biprocesseurs.</span><span class="sxs-lookup"><span data-stu-id="45d30-133">Either workstation or server can be used for two-processor computers.</span></span> <span data-ttu-id="45d30-134">Le garbage collection côté serveur est normalement l'option la plus rapide pour les ordinateurs comptant plus de deux processeurs.</span><span class="sxs-lookup"><span data-stu-id="45d30-134">Server garbage collection should be the fastest option for more than two processors.</span></span>  
  
 <span data-ttu-id="45d30-135">Cet élément peut être défini uniquement dans le fichier de configuration de l'application (il est ignoré s'il est défini dans le fichier de configuration de l'ordinateur).</span><span class="sxs-lookup"><span data-stu-id="45d30-135">This element can be used only in the application configuration file; it is ignored if it is in the machine configuration file.</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="45d30-136">Dans .NET Framework 4 et les versions antérieures, le garbage collection simultané n'est pas disponible si le garbage collection côté serveur est activé.</span><span class="sxs-lookup"><span data-stu-id="45d30-136">In the .NET Framework 4 and earlier versions, concurrent garbage collection is not available when server garbage collection is enabled.</span></span> <span data-ttu-id="45d30-137">Depuis [!INCLUDE[net_v45](../../../../../includes/net-v45-md.md)], le garbage collection côté serveur est simultané.</span><span class="sxs-lookup"><span data-stu-id="45d30-137">Starting with the [!INCLUDE[net_v45](../../../../../includes/net-v45-md.md)], server garbage collection is concurrent.</span></span> <span data-ttu-id="45d30-138">Pour utiliser le garbage collection de serveur non simultané, définissez le `<gcServer>` élément `true` et [ \<gcConcurrent > élément](../../../../../docs/framework/configure-apps/file-schema/runtime/gcconcurrent-element.md) à `false`.</span><span class="sxs-lookup"><span data-stu-id="45d30-138">To use non-concurrent server garbage collection, set the `<gcServer>` element to `true` and the [\<gcConcurrent> element](../../../../../docs/framework/configure-apps/file-schema/runtime/gcconcurrent-element.md) to `false`.</span></span>  
  
## <a name="example"></a><span data-ttu-id="45d30-139">Exemple</span><span class="sxs-lookup"><span data-stu-id="45d30-139">Example</span></span>  
 <span data-ttu-id="45d30-140">L’exemple suivant active le garbage collection côté serveur.</span><span class="sxs-lookup"><span data-stu-id="45d30-140">The following example enables server garbage collection.</span></span>  
  
```xml  
<configuration>  
   <runtime>  
      <gcServer enabled="true"/>  
   </runtime>  
</configuration>  
```  
  
## <a name="see-also"></a><span data-ttu-id="45d30-141">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="45d30-141">See also</span></span>

- <xref:System.Runtime.GCSettings.IsServerGC%2A?displayProperty=nameWithType>
- [<span data-ttu-id="45d30-142">Schéma des paramètres d’exécution</span><span class="sxs-lookup"><span data-stu-id="45d30-142">Runtime Settings Schema</span></span>](../../../../../docs/framework/configure-apps/file-schema/runtime/index.md)
- [<span data-ttu-id="45d30-143">Schéma des fichiers de configuration</span><span class="sxs-lookup"><span data-stu-id="45d30-143">Configuration File Schema</span></span>](../../../../../docs/framework/configure-apps/file-schema/index.md)
- [<span data-ttu-id="45d30-144">Pour désactiver le garbage collection simultané</span><span class="sxs-lookup"><span data-stu-id="45d30-144">To disable concurrent garbage collection</span></span>](gcconcurrent-element.md#to-disable-background-garbage-collection)
