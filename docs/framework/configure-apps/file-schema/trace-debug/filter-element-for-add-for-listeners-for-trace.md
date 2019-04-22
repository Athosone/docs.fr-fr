---
title: <filter> Élément pour <add> pour <listeners> pour <trace>
ms.date: 03/30/2017
f1_keywords:
- http://schemas.microsoft.com/.NetConfiguration/v2.0#configuration/system.diagnostics/trace/listeners/add/filter
helpviewer_keywords:
- initializeData attribute
- filter element for <add> for <listeners> for <trace>
- <filter> element for <add> for <listeners> for <trace>
ms.assetid: eb9c18f5-dfa8-47c5-b91b-e4b93e76e1cc
ms.openlocfilehash: 5961125e1b8d0d0f5711f8b942b68ba71d61888f
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59143427"
---
# <a name="filter-element-for-add-for-listeners-for-trace"></a><span data-ttu-id="d85d5-102">\<Filtre >, élément pour \<Ajouter > pour \<écouteurs > pour \<trace ></span><span class="sxs-lookup"><span data-stu-id="d85d5-102">\<filter> Element for \<add> for \<listeners> for \<trace></span></span>
<span data-ttu-id="d85d5-103">Ajoute un filtre à un écouteur dans la `Listeners` collection pour une trace.</span><span class="sxs-lookup"><span data-stu-id="d85d5-103">Adds a filter to a listener in the `Listeners` collection for a trace.</span></span>  
  
 <span data-ttu-id="d85d5-104">\<configuration></span><span class="sxs-lookup"><span data-stu-id="d85d5-104">\<configuration></span></span>  
<span data-ttu-id="d85d5-105">\<system.diagnostics></span><span class="sxs-lookup"><span data-stu-id="d85d5-105">\<system.diagnostics></span></span>  
<span data-ttu-id="d85d5-106">\<trace></span><span class="sxs-lookup"><span data-stu-id="d85d5-106">\<trace></span></span>  
<span data-ttu-id="d85d5-107">\<listeners></span><span class="sxs-lookup"><span data-stu-id="d85d5-107">\<listeners></span></span>  
<span data-ttu-id="d85d5-108">\<add></span><span class="sxs-lookup"><span data-stu-id="d85d5-108">\<add></span></span>  
<span data-ttu-id="d85d5-109">\<filter></span><span class="sxs-lookup"><span data-stu-id="d85d5-109">\<filter></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="d85d5-110">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="d85d5-110">Syntax</span></span>  
  
```xml  
<filter   
  type="traceFilterClassName"   
  initializeData="data" />  
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="d85d5-111">Attributs et éléments</span><span class="sxs-lookup"><span data-stu-id="d85d5-111">Attributes and Elements</span></span>  
 <span data-ttu-id="d85d5-112">Les sections suivantes décrivent des attributs, des éléments enfants et des éléments parents.</span><span class="sxs-lookup"><span data-stu-id="d85d5-112">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="d85d5-113">Attributs</span><span class="sxs-lookup"><span data-stu-id="d85d5-113">Attributes</span></span>  
  
|<span data-ttu-id="d85d5-114">Attribut</span><span class="sxs-lookup"><span data-stu-id="d85d5-114">Attribute</span></span>|<span data-ttu-id="d85d5-115">Description</span><span class="sxs-lookup"><span data-stu-id="d85d5-115">Description</span></span>|  
|---------------|-----------------|  
|`type`|<span data-ttu-id="d85d5-116">Attribut requis.</span><span class="sxs-lookup"><span data-stu-id="d85d5-116">Required attribute.</span></span><br /><br /> <span data-ttu-id="d85d5-117">Spécifie le type du filtre, qui doit hériter la <xref:System.Diagnostics.TraceFilter> classe.</span><span class="sxs-lookup"><span data-stu-id="d85d5-117">Specifies the type of the filter, which should inherit from the <xref:System.Diagnostics.TraceFilter> class.</span></span> <span data-ttu-id="d85d5-118">Vous pouvez utiliser le nom qualifié d’espace de noms du type, qui correspond à du type <xref:System.Type.FullName%2A> propriété, ou vous pouvez utiliser le nom de type qualifié complet, y compris les informations d’assembly, qui correspondant à la <xref:System.Type.AssemblyQualifiedName%2A> propriété.</span><span class="sxs-lookup"><span data-stu-id="d85d5-118">You can use the namespace-qualified name of the type, which corresponds to the type's <xref:System.Type.FullName%2A> property, or you can use the fully qualified type name including the assembly information, which corresponds to the <xref:System.Type.AssemblyQualifiedName%2A> property.</span></span> <span data-ttu-id="d85d5-119">Pour plus d’informations sur les noms de types qualifiés complets, consultez [spécifiant des noms de types qualifiés complets](../../../../../docs/framework/reflection-and-codedom/specifying-fully-qualified-type-names.md).</span><span class="sxs-lookup"><span data-stu-id="d85d5-119">For information about fully qualified type names, see [Specifying Fully Qualified Type Names](../../../../../docs/framework/reflection-and-codedom/specifying-fully-qualified-type-names.md).</span></span>|  
|`initializeData`|<span data-ttu-id="d85d5-120">Attribut facultatif.</span><span class="sxs-lookup"><span data-stu-id="d85d5-120">Optional attribute.</span></span><br /><br /> <span data-ttu-id="d85d5-121">La chaîne passée au constructeur pour la classe de filtre spécifié.</span><span class="sxs-lookup"><span data-stu-id="d85d5-121">The string passed to the constructor for the specified filter class.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="d85d5-122">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="d85d5-122">Child Elements</span></span>  
 <span data-ttu-id="d85d5-123">Aucun.</span><span class="sxs-lookup"><span data-stu-id="d85d5-123">None.</span></span>  
  
### <a name="parent-elements"></a><span data-ttu-id="d85d5-124">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="d85d5-124">Parent Elements</span></span>  
  
|<span data-ttu-id="d85d5-125">Élément</span><span class="sxs-lookup"><span data-stu-id="d85d5-125">Element</span></span>|<span data-ttu-id="d85d5-126">Description</span><span class="sxs-lookup"><span data-stu-id="d85d5-126">Description</span></span>|  
|-------------|-----------------|  
|`configuration`|<span data-ttu-id="d85d5-127">Élément racine de chaque fichier de configuration utilisé par le Common Language Runtime et les applications .NET Framework.</span><span class="sxs-lookup"><span data-stu-id="d85d5-127">The root element in every configuration file used by the common language runtime and .NET Framework applications.</span></span>|  
|`system.diagnostics`|<span data-ttu-id="d85d5-128">Spécifie les écouteurs de trace qui collectent, stockent et acheminent les messages, ainsi que le niveau auquel un commutateur de trace est défini.</span><span class="sxs-lookup"><span data-stu-id="d85d5-128">Specifies trace listeners that collect, store, and route messages and the level where a trace switch is set.</span></span>|  
|`trace`|<span data-ttu-id="d85d5-129">Contient les écouteurs qui collectent, stockent et acheminent les messages de traçage.</span><span class="sxs-lookup"><span data-stu-id="d85d5-129">Contains listeners that collect, store, and route tracing messages.</span></span>|  
|`listeners`|<span data-ttu-id="d85d5-130">Contient des écouteurs qui collectent, stockent et acheminent les messages.</span><span class="sxs-lookup"><span data-stu-id="d85d5-130">Contains listeners that collect, store, and route messages.</span></span> <span data-ttu-id="d85d5-131">Les écouteurs dirigent la sortie de traçage vers une cible appropriée.</span><span class="sxs-lookup"><span data-stu-id="d85d5-131">Listeners direct the tracing output to an appropriate target.</span></span>|  
|`add`|<span data-ttu-id="d85d5-132">Ajoute un écouteur à la collection `Listeners`.</span><span class="sxs-lookup"><span data-stu-id="d85d5-132">Adds a listener to the `Listeners` collection.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="d85d5-133">Notes</span><span class="sxs-lookup"><span data-stu-id="d85d5-133">Remarks</span></span>  
 <span data-ttu-id="d85d5-134">Le `<filter>` élément doit être contenu dans un `<add>` élément pour un écouteur de trace qui spécifie le type de l’écouteur, pas seulement le nom d’un écouteur défini dans un [ \<sharedListeners >](../../../../../docs/framework/configure-apps/file-schema/trace-debug/sharedlisteners-element.md).</span><span class="sxs-lookup"><span data-stu-id="d85d5-134">The `<filter>` element must be contained in an `<add>` element for a trace listener that specifies the type of the listener, not just the name of a listener defined in a [\<sharedListeners>](../../../../../docs/framework/configure-apps/file-schema/trace-debug/sharedlisteners-element.md).</span></span> <span data-ttu-id="d85d5-135">Si l’écouteur est défini dans un [ \<sharedListeners >](../../../../../docs/framework/configure-apps/file-schema/trace-debug/sharedlisteners-element.md), le filtre de cet écouteur doit être défini dans cet élément.</span><span class="sxs-lookup"><span data-stu-id="d85d5-135">If the listener is defined in a [\<sharedListeners>](../../../../../docs/framework/configure-apps/file-schema/trace-debug/sharedlisteners-element.md), the filter for that listener must be defined in that element.</span></span>  
  
 <span data-ttu-id="d85d5-136">Cet élément peut être utilisé dans le fichier de configuration machine (Machine.config) et le fichier de configuration d’application.</span><span class="sxs-lookup"><span data-stu-id="d85d5-136">This element can be used in the machine configuration file (Machine.config) and the application configuration file.</span></span>  
  
## <a name="example"></a><span data-ttu-id="d85d5-137">Exemple</span><span class="sxs-lookup"><span data-stu-id="d85d5-137">Example</span></span>  
 <span data-ttu-id="d85d5-138">L’exemple suivant montre comment utiliser le `<filter>` élément pour ajouter un filtre à l’écouteur `console` dans le `Listeners` collection de la trace, en spécifiant le niveau d’événement de filtre en tant que `Error`.</span><span class="sxs-lookup"><span data-stu-id="d85d5-138">The following example shows how to use the `<filter>` element to add a filter to the listener `console` in the `Listeners` collection for trace, specifying the filter event level as `Error`.</span></span>  
  
```xml  
<configuration>  
  <system.diagnostics>  
    <trace autoflush="false" indentsize="4">  
      <listeners>  
        <add name="console"   
          type="System.Diagnostics.ConsoleTraceListener" >  
          <filter type="System.Diagnostics.EventTypeFilter"   
            initializeData="Error" />  
        </add>  
        <remove name="Default" />  
      </listeners>  
    </trace>  
  </system.diagnostics>  
</configuration>  
```  
  
## <a name="see-also"></a><span data-ttu-id="d85d5-139">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d85d5-139">See also</span></span>

- <xref:System.Diagnostics.Trace>
- <xref:System.Diagnostics.TraceListener>
- <xref:System.Diagnostics.TraceListener.Filter%2A?displayProperty=nameWithType>
- <xref:System.Diagnostics.TraceFilter>
- [<span data-ttu-id="d85d5-140">Schéma des paramètres de trace et de débogage</span><span class="sxs-lookup"><span data-stu-id="d85d5-140">Trace and Debug Settings Schema</span></span>](../../../../../docs/framework/configure-apps/file-schema/trace-debug/index.md)
