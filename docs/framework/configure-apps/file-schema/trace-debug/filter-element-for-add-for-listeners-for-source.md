---
title: <filter> Élément pour <add> pour <listeners> pour <source>
ms.date: 03/30/2017
f1_keywords:
- http://schemas.microsoft.com/.NetConfiguration/v2.0#filter
- http://schemas.microsoft.com/.NetConfiguration/v2.0#configuration/system.diagnostics/sources/source/listeners/add/filter
helpviewer_keywords:
- initializeData attribute
- <filter> element for <add> for <listeners> for <source>
- filter element for <add> for <listeners> for <source>
ms.assetid: 15808b80-4579-4c25-b385-178cfdf154ba
ms.openlocfilehash: 3abfd0bdd40f98a9e4774677fc2cd5068c14333f
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61673769"
---
# <a name="filter-element-for-add-for-listeners-for-source"></a><span data-ttu-id="06af0-102">\<Filtre >, élément pour \<Ajouter > pour \<écouteurs > pour \<source ></span><span class="sxs-lookup"><span data-stu-id="06af0-102">\<filter> Element for \<add> for \<listeners> for \<source></span></span>
<span data-ttu-id="06af0-103">Ajoute un filtre à un écouteur dans la collection `Listeners` pour une source de trace.</span><span class="sxs-lookup"><span data-stu-id="06af0-103">Adds a filter to a listener in the `Listeners` collection for a trace source.</span></span>  
  
 <span data-ttu-id="06af0-104">\<configuration></span><span class="sxs-lookup"><span data-stu-id="06af0-104">\<configuration></span></span>  
<span data-ttu-id="06af0-105">\<system.diagnostics></span><span class="sxs-lookup"><span data-stu-id="06af0-105">\<system.diagnostics></span></span>  
<span data-ttu-id="06af0-106">\<sources></span><span class="sxs-lookup"><span data-stu-id="06af0-106">\<sources></span></span>  
<span data-ttu-id="06af0-107">\<source></span><span class="sxs-lookup"><span data-stu-id="06af0-107">\<source></span></span>  
<span data-ttu-id="06af0-108">\<listeners></span><span class="sxs-lookup"><span data-stu-id="06af0-108">\<listeners></span></span>  
<span data-ttu-id="06af0-109">\<add></span><span class="sxs-lookup"><span data-stu-id="06af0-109">\<add></span></span>  
<span data-ttu-id="06af0-110">\<filter></span><span class="sxs-lookup"><span data-stu-id="06af0-110">\<filter></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="06af0-111">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="06af0-111">Syntax</span></span>  
  
```xml  
<filter   
  type="traceFilterClassName"   
  initializeData="data" />  
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="06af0-112">Attributs et éléments</span><span class="sxs-lookup"><span data-stu-id="06af0-112">Attributes and Elements</span></span>  
 <span data-ttu-id="06af0-113">Les sections suivantes décrivent des attributs, des éléments enfants et des éléments parents.</span><span class="sxs-lookup"><span data-stu-id="06af0-113">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="06af0-114">Attributs</span><span class="sxs-lookup"><span data-stu-id="06af0-114">Attributes</span></span>  
  
|<span data-ttu-id="06af0-115">Attribut</span><span class="sxs-lookup"><span data-stu-id="06af0-115">Attribute</span></span>|<span data-ttu-id="06af0-116">Description</span><span class="sxs-lookup"><span data-stu-id="06af0-116">Description</span></span>|  
|---------------|-----------------|  
|`type`|<span data-ttu-id="06af0-117">Attribut requis.</span><span class="sxs-lookup"><span data-stu-id="06af0-117">Required attribute.</span></span><br /><br /> <span data-ttu-id="06af0-118">Spécifie le type du filtre, qui doit hériter la <xref:System.Diagnostics.TraceFilter> classe.</span><span class="sxs-lookup"><span data-stu-id="06af0-118">Specifies the type of the filter, which should inherit from the <xref:System.Diagnostics.TraceFilter> class.</span></span> <span data-ttu-id="06af0-119">Vous pouvez utiliser le nom qualifié d’espace de noms du type, qui correspond à du type <xref:System.Type.FullName%2A> propriété, ou vous pouvez utiliser le nom de type qualifié complet, y compris les informations d’assembly, qui correspondant à la <xref:System.Type.AssemblyQualifiedName%2A> propriété.</span><span class="sxs-lookup"><span data-stu-id="06af0-119">You can use the namespace-qualified name of the type, which corresponds to the type's <xref:System.Type.FullName%2A> property, or you can use the fully qualified type name including the assembly information, which corresponds to the <xref:System.Type.AssemblyQualifiedName%2A> property.</span></span> <span data-ttu-id="06af0-120">Pour plus d’informations sur les noms de types qualifiés complets, consultez [spécifiant des noms de types qualifiés complets](../../../../../docs/framework/reflection-and-codedom/specifying-fully-qualified-type-names.md).</span><span class="sxs-lookup"><span data-stu-id="06af0-120">For information about fully qualified type names, see [Specifying Fully Qualified Type Names](../../../../../docs/framework/reflection-and-codedom/specifying-fully-qualified-type-names.md).</span></span>|  
|`initializeData`|<span data-ttu-id="06af0-121">Attribut facultatif.</span><span class="sxs-lookup"><span data-stu-id="06af0-121">Optional attribute.</span></span><br /><br /> <span data-ttu-id="06af0-122">La chaîne passée au constructeur pour la classe de filtre spécifié.</span><span class="sxs-lookup"><span data-stu-id="06af0-122">The string passed to the constructor for the specified filter class.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="06af0-123">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="06af0-123">Child Elements</span></span>  
 <span data-ttu-id="06af0-124">Aucun.</span><span class="sxs-lookup"><span data-stu-id="06af0-124">None.</span></span>  
  
### <a name="parent-elements"></a><span data-ttu-id="06af0-125">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="06af0-125">Parent Elements</span></span>  
  
|<span data-ttu-id="06af0-126">Élément</span><span class="sxs-lookup"><span data-stu-id="06af0-126">Element</span></span>|<span data-ttu-id="06af0-127">Description</span><span class="sxs-lookup"><span data-stu-id="06af0-127">Description</span></span>|  
|-------------|-----------------|  
|`configuration`|<span data-ttu-id="06af0-128">Élément racine de chaque fichier de configuration utilisé par le Common Language Runtime et les applications .NET Framework.</span><span class="sxs-lookup"><span data-stu-id="06af0-128">The root element in every configuration file used by the common language runtime and .NET Framework applications.</span></span>|  
|`system.diagnostics`|<span data-ttu-id="06af0-129">Spécifie les écouteurs de trace qui collectent, stockent et acheminent les messages, ainsi que le niveau auquel un commutateur de trace est défini.</span><span class="sxs-lookup"><span data-stu-id="06af0-129">Specifies trace listeners that collect, store, and route messages and the level where a trace switch is set.</span></span>|  
|`sources`|<span data-ttu-id="06af0-130">Contient les sources de trace qui lancent des messages de traçage.</span><span class="sxs-lookup"><span data-stu-id="06af0-130">Contains trace sources that initiate tracing messages.</span></span>|  
|`source`|<span data-ttu-id="06af0-131">Spécifie une source de trace qui lance des messages de traçage.</span><span class="sxs-lookup"><span data-stu-id="06af0-131">Specifies a trace source that initiates tracing messages.</span></span>|  
|`listeners`|<span data-ttu-id="06af0-132">Contient des écouteurs qui collectent, stockent et acheminent les messages.</span><span class="sxs-lookup"><span data-stu-id="06af0-132">Contains listeners that collect, store, and route messages.</span></span> <span data-ttu-id="06af0-133">Les écouteurs dirigent la sortie de traçage vers une cible appropriée.</span><span class="sxs-lookup"><span data-stu-id="06af0-133">Listeners direct the tracing output to an appropriate target.</span></span>|  
|`add`|<span data-ttu-id="06af0-134">Ajoute un écouteur à la collection `Listeners` pour une source de trace.</span><span class="sxs-lookup"><span data-stu-id="06af0-134">Adds a listener to the `Listeners` collection for a trace source.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="06af0-135">Notes</span><span class="sxs-lookup"><span data-stu-id="06af0-135">Remarks</span></span>  
 <span data-ttu-id="06af0-136">Le `<filter>` élément doit être contenu dans un `<add>` élément pour un écouteur de source de trace qui spécifie le type de l’écouteur, pas seulement le nom d’un écouteur défini dans un [ \<sharedListeners >](../../../../../docs/framework/configure-apps/file-schema/trace-debug/sharedlisteners-element.md).</span><span class="sxs-lookup"><span data-stu-id="06af0-136">The `<filter>` element must be contained in an `<add>` element for a trace source listener that specifies the type of the listener, not just the name of a listener defined in a [\<sharedListeners>](../../../../../docs/framework/configure-apps/file-schema/trace-debug/sharedlisteners-element.md).</span></span> <span data-ttu-id="06af0-137">Si l’écouteur est défini dans un [ \<sharedListeners >](../../../../../docs/framework/configure-apps/file-schema/trace-debug/sharedlisteners-element.md), le filtre de cet écouteur doit être défini dans cet élément.</span><span class="sxs-lookup"><span data-stu-id="06af0-137">If the listener is defined in a [\<sharedListeners>](../../../../../docs/framework/configure-apps/file-schema/trace-debug/sharedlisteners-element.md), the filter for that listener must be defined in that element.</span></span>  
  
 <span data-ttu-id="06af0-138">Cet élément peut être utilisé dans le fichier de configuration machine (Machine.config) et le fichier de configuration d’application.</span><span class="sxs-lookup"><span data-stu-id="06af0-138">This element can be used in the machine configuration file (Machine.config) and the application configuration file.</span></span>  
  
## <a name="example"></a><span data-ttu-id="06af0-139">Exemple</span><span class="sxs-lookup"><span data-stu-id="06af0-139">Example</span></span>  
 <span data-ttu-id="06af0-140">L’exemple suivant montre comment utiliser le `<filter>` élément pour ajouter un filtre à l’écouteur `console` dans le `Listeners` collection pour la source de suivi `myTraceSource`, en spécifiant le niveau d’événement de filtre en tant que `Error`.</span><span class="sxs-lookup"><span data-stu-id="06af0-140">The following example shows how to use the `<filter>` element to add a filter to the listener `console` in the `Listeners` collection for the trace source `myTraceSource`, specifying the filter event level as `Error`.</span></span>  
  
```xml  
<configuration>  
  <system.diagnostics>  
    <sources>  
      <source name="myTraceSource" switchName="SourceSwitch"   
        switchType="System.Diagnostics.SourceSwitch"  >  
        <listeners>  
          <add name="console"   
            type="System.Diagnostics.ConsoleTraceListener" >  
            <filter type="System.Diagnostics.EventTypeFilter"   
              initializeData="Error" />  
          </add>  
          <remove name="Default" />  
        </listeners>  
      </source>  
    </sources>  
    <switches>  
      <add name="SourceSwitch" value="Warning" />  
    </switches>  
  </system.diagnostics>  
</configuration>  
```  
  
## <a name="see-also"></a><span data-ttu-id="06af0-141">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="06af0-141">See also</span></span>

- <xref:System.Diagnostics.TraceSource>
- <xref:System.Diagnostics.TraceListener>
- <xref:System.Diagnostics.TraceListener.Filter%2A?displayProperty=nameWithType>
- <xref:System.Diagnostics.TraceFilter>
- [<span data-ttu-id="06af0-142">Schéma des paramètres de trace et de débogage</span><span class="sxs-lookup"><span data-stu-id="06af0-142">Trace and Debug Settings Schema</span></span>](../../../../../docs/framework/configure-apps/file-schema/trace-debug/index.md)
