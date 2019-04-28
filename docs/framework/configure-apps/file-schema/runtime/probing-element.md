---
title: Élément <probing>
ms.date: 03/30/2017
f1_keywords:
- http://schemas.microsoft.com/.NetConfiguration/v2.0#configuration/runtime/assemblyBinding/probing
- http://schemas.microsoft.com/.NetConfiguration/v2.0#probing
helpviewer_keywords:
- <probing> element
- container tags, <probing> element
- probing element
ms.assetid: 09c80fc9-1ba5-4192-89f7-3a79b2e4b024
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 9402c9f28c123affb7b90fc189484bb1fd43db46
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61704607"
---
# <a name="probing-element"></a><span data-ttu-id="822e3-102">\<probing > élément</span><span class="sxs-lookup"><span data-stu-id="822e3-102">\<probing> Element</span></span>
<span data-ttu-id="822e3-103">Spécifie les sous-répertoires de base d’application pour le common language runtime à rechercher lors du chargement d’assemblys.</span><span class="sxs-lookup"><span data-stu-id="822e3-103">Specifies application base subdirectories for the common language runtime to search when loading assemblies.</span></span>  
  
 <span data-ttu-id="822e3-104">\<configuration></span><span class="sxs-lookup"><span data-stu-id="822e3-104">\<configuration></span></span>  
<span data-ttu-id="822e3-105">\<runtime></span><span class="sxs-lookup"><span data-stu-id="822e3-105">\<runtime></span></span>  
<span data-ttu-id="822e3-106">\<assemblyBinding></span><span class="sxs-lookup"><span data-stu-id="822e3-106">\<assemblyBinding></span></span>  
<span data-ttu-id="822e3-107">\<probing></span><span class="sxs-lookup"><span data-stu-id="822e3-107">\<probing></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="822e3-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="822e3-108">Syntax</span></span>  
  
```xml  
<probing privatePath="paths"/>  
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="822e3-109">Attributs et éléments</span><span class="sxs-lookup"><span data-stu-id="822e3-109">Attributes and Elements</span></span>  
 <span data-ttu-id="822e3-110">Les sections suivantes décrivent des attributs, des éléments enfants et des éléments parents.</span><span class="sxs-lookup"><span data-stu-id="822e3-110">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="822e3-111">Attributs</span><span class="sxs-lookup"><span data-stu-id="822e3-111">Attributes</span></span>  
  
|<span data-ttu-id="822e3-112">Attribut</span><span class="sxs-lookup"><span data-stu-id="822e3-112">Attribute</span></span>|<span data-ttu-id="822e3-113">Description</span><span class="sxs-lookup"><span data-stu-id="822e3-113">Description</span></span>|  
|---------------|-----------------|  
|`privatePath`|<span data-ttu-id="822e3-114">Attribut requis.</span><span class="sxs-lookup"><span data-stu-id="822e3-114">Required attribute.</span></span><br /><br /> <span data-ttu-id="822e3-115">Spécifie les sous-répertoires du répertoire de base de l’application qui peut contenir des assemblys.</span><span class="sxs-lookup"><span data-stu-id="822e3-115">Specifies subdirectories of the application's base directory that might contain assemblies.</span></span> <span data-ttu-id="822e3-116">Délimiter chaque sous-répertoire par un point-virgule.</span><span class="sxs-lookup"><span data-stu-id="822e3-116">Delimit each subdirectory with a semicolon.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="822e3-117">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="822e3-117">Child Elements</span></span>  
 <span data-ttu-id="822e3-118">Aucun.</span><span class="sxs-lookup"><span data-stu-id="822e3-118">None.</span></span>  
  
### <a name="parent-elements"></a><span data-ttu-id="822e3-119">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="822e3-119">Parent Elements</span></span>  
  
|<span data-ttu-id="822e3-120">Élément</span><span class="sxs-lookup"><span data-stu-id="822e3-120">Element</span></span>|<span data-ttu-id="822e3-121">Description</span><span class="sxs-lookup"><span data-stu-id="822e3-121">Description</span></span>|  
|-------------|-----------------|  
|`assemblyBinding`|<span data-ttu-id="822e3-122">Contient des informations à propos de la redirection des versions d'assemblys et de l'emplacement de ces derniers.</span><span class="sxs-lookup"><span data-stu-id="822e3-122">Contains information about assembly version redirection and the locations of assemblies.</span></span>|  
|`configuration`|<span data-ttu-id="822e3-123">Élément racine de chaque fichier de configuration utilisé par le Common Language Runtime et les applications .NET Framework.</span><span class="sxs-lookup"><span data-stu-id="822e3-123">The root element in every configuration file used by the common language runtime and .NET Framework applications.</span></span>|  
|`runtime`|<span data-ttu-id="822e3-124">Contient des informations sur les liaisons d’assembly et l’opération garbage collection.</span><span class="sxs-lookup"><span data-stu-id="822e3-124">Contains information about assembly binding and garbage collection.</span></span>|  
  
## <a name="example"></a><span data-ttu-id="822e3-125">Exemple</span><span class="sxs-lookup"><span data-stu-id="822e3-125">Example</span></span>  
 <span data-ttu-id="822e3-126">L’exemple suivant montre comment spécifier les sous-répertoires de base d’application que le runtime doit rechercher les assemblys.</span><span class="sxs-lookup"><span data-stu-id="822e3-126">The following example shows how to specify application base subdirectories the runtime should search for assemblies.</span></span>  
  
```xml  
<configuration>  
   <runtime>  
      <assemblyBinding xmlns="urn:schemas-microsoft-com:asm.v1">  
         <probing privatePath="bin;bin2\subbin;bin3"/>  
      </assemblyBinding>  
   </runtime>  
</configuration>  
```  
  
## <a name="see-also"></a><span data-ttu-id="822e3-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="822e3-127">See also</span></span>

- [<span data-ttu-id="822e3-128">Schéma des paramètres d’exécution</span><span class="sxs-lookup"><span data-stu-id="822e3-128">Runtime Settings Schema</span></span>](../../../../../docs/framework/configure-apps/file-schema/runtime/index.md)
- [<span data-ttu-id="822e3-129">Schéma des fichiers de configuration</span><span class="sxs-lookup"><span data-stu-id="822e3-129">Configuration File Schema</span></span>](../../../../../docs/framework/configure-apps/file-schema/index.md)
- [<span data-ttu-id="822e3-130">Spécification de l'emplacement d'un assembly</span><span class="sxs-lookup"><span data-stu-id="822e3-130">Specifying an Assembly's Location</span></span>](../../../../../docs/framework/configure-apps/specify-assembly-location.md)
- [<span data-ttu-id="822e3-131">Méthode de localisation des assemblys par le runtime</span><span class="sxs-lookup"><span data-stu-id="822e3-131">How the Runtime Locates Assemblies</span></span>](../../../../../docs/framework/deployment/how-the-runtime-locates-assemblies.md)
