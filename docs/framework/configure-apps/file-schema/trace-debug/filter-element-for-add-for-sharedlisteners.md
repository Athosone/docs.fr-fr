---
title: <filter> Élément pour <add> pour <sharedListeners>
ms.date: 03/30/2017
f1_keywords:
- http://schemas.microsoft.com/.NetConfiguration/v2.0#configuration/system.diagnostics/sharedListeners/add/filter
helpviewer_keywords:
- filter element for <add> for <sharedListeners>
- initializeData attribute
- <filter> element for <add> for <sharedListeners>
- filters, trace listeners
- trace listeners, filters
ms.assetid: 7d4e7faa-2e4e-4379-ac76-f6cd7f2f8fac
ms.openlocfilehash: 2bef729f179b41509d3c0381b26e38e364dbf86b
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59120742"
---
# <a name="filter-element-for-add-for-sharedlisteners"></a><span data-ttu-id="f0469-102">\<Filtre >, élément pour \<Ajouter > pour \<sharedListeners ></span><span class="sxs-lookup"><span data-stu-id="f0469-102">\<filter> Element for \<add> for \<sharedListeners></span></span>
<span data-ttu-id="f0469-103">Ajoute un filtre à un écouteur dans la collection `sharedListeners`.</span><span class="sxs-lookup"><span data-stu-id="f0469-103">Adds a filter to a listener in the `sharedListeners` collection.</span></span>  
  
 <span data-ttu-id="f0469-104">\<configuration></span><span class="sxs-lookup"><span data-stu-id="f0469-104">\<configuration></span></span>  
<span data-ttu-id="f0469-105">\<system.diagnostics></span><span class="sxs-lookup"><span data-stu-id="f0469-105">\<system.diagnostics></span></span>  
<span data-ttu-id="f0469-106">\<sharedListeners > élément</span><span class="sxs-lookup"><span data-stu-id="f0469-106">\<sharedListeners> Element</span></span>  
<span data-ttu-id="f0469-107">\<add></span><span class="sxs-lookup"><span data-stu-id="f0469-107">\<add></span></span>  
<span data-ttu-id="f0469-108">\<filter></span><span class="sxs-lookup"><span data-stu-id="f0469-108">\<filter></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="f0469-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="f0469-109">Syntax</span></span>  
  
```xml  
<filter type="System.Diagnostics.EventTypeFilter"   
  initializeData="Warning" />  
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="f0469-110">Attributs et éléments</span><span class="sxs-lookup"><span data-stu-id="f0469-110">Attributes and Elements</span></span>  
 <span data-ttu-id="f0469-111">Les sections suivantes décrivent des attributs, des éléments enfants et des éléments parents.</span><span class="sxs-lookup"><span data-stu-id="f0469-111">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="f0469-112">Attributs</span><span class="sxs-lookup"><span data-stu-id="f0469-112">Attributes</span></span>  
  
|<span data-ttu-id="f0469-113">Attribut</span><span class="sxs-lookup"><span data-stu-id="f0469-113">Attribute</span></span>|<span data-ttu-id="f0469-114">Description</span><span class="sxs-lookup"><span data-stu-id="f0469-114">Description</span></span>|  
|---------------|-----------------|  
|<span data-ttu-id="f0469-115">**type**</span><span class="sxs-lookup"><span data-stu-id="f0469-115">**type**</span></span>|<span data-ttu-id="f0469-116">Attribut requis.</span><span class="sxs-lookup"><span data-stu-id="f0469-116">Required attribute.</span></span><br /><br /> <span data-ttu-id="f0469-117">Spécifie le type du filtre.</span><span class="sxs-lookup"><span data-stu-id="f0469-117">Specifies the type of the filter.</span></span> <span data-ttu-id="f0469-118">Vous pouvez utiliser uniquement le nom complet du type (dans le format de la <xref:System.Type.FullName%2A?displayProperty=nameWithType> propriété), ou vous pouvez utiliser le nom de type qualifié complet, y compris les informations d’assembly (dans le format de la <xref:System.Type.AssemblyQualifiedName%2A?displayProperty=nameWithType> propriété).</span><span class="sxs-lookup"><span data-stu-id="f0469-118">You can use only the full name of the type (in the format of the <xref:System.Type.FullName%2A?displayProperty=nameWithType> property), or you can use the fully qualified type name including the assembly information (in the format of the <xref:System.Type.AssemblyQualifiedName%2A?displayProperty=nameWithType> property).</span></span> <span data-ttu-id="f0469-119">Pour plus d’informations sur la création d’un nom de type qualifié complet, consultez [spécifiant des noms de types qualifiés complets](../../../../../docs/framework/reflection-and-codedom/specifying-fully-qualified-type-names.md).</span><span class="sxs-lookup"><span data-stu-id="f0469-119">For information on creating a fully qualified type name, see [Specifying Fully Qualified Type Names](../../../../../docs/framework/reflection-and-codedom/specifying-fully-qualified-type-names.md).</span></span>|  
|<span data-ttu-id="f0469-120">**initializeData**</span><span class="sxs-lookup"><span data-stu-id="f0469-120">**initializeData**</span></span>|<span data-ttu-id="f0469-121">Attribut facultatif.</span><span class="sxs-lookup"><span data-stu-id="f0469-121">Optional attribute.</span></span><br /><br /> <span data-ttu-id="f0469-122">La chaîne passée au constructeur pour la classe spécifiée.</span><span class="sxs-lookup"><span data-stu-id="f0469-122">The string passed to the constructor for the specified class.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="f0469-123">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="f0469-123">Child Elements</span></span>  
 <span data-ttu-id="f0469-124">Aucun.</span><span class="sxs-lookup"><span data-stu-id="f0469-124">None.</span></span>  
  
### <a name="parent-elements"></a><span data-ttu-id="f0469-125">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="f0469-125">Parent Elements</span></span>  
  
|<span data-ttu-id="f0469-126">Élément</span><span class="sxs-lookup"><span data-stu-id="f0469-126">Element</span></span>|<span data-ttu-id="f0469-127">Description</span><span class="sxs-lookup"><span data-stu-id="f0469-127">Description</span></span>|  
|-------------|-----------------|  
|`configuration`|<span data-ttu-id="f0469-128">Élément racine de chaque fichier de configuration utilisé par le Common Language Runtime et les applications .NET Framework.</span><span class="sxs-lookup"><span data-stu-id="f0469-128">The root element in every configuration file used by the common language runtime and .NET Framework applications.</span></span>|  
|`system.diagnostics`|<span data-ttu-id="f0469-129">Spécifie les écouteurs de trace qui collectent, stockent et acheminent les messages, ainsi que le niveau auquel un commutateur de trace est défini.</span><span class="sxs-lookup"><span data-stu-id="f0469-129">Specifies trace listeners that collect, store, and route messages and the level where a trace switch is set.</span></span>|  
|`sharedListeners`|<span data-ttu-id="f0469-130">Une collection d’écouteurs de n’importe quel élément trace ou une source peut faire référence.</span><span class="sxs-lookup"><span data-stu-id="f0469-130">A collection of listeners that any source or trace element can reference.</span></span>|  
|`add`|<span data-ttu-id="f0469-131">Ajoute un écouteur à la **sharedListeners** collection.</span><span class="sxs-lookup"><span data-stu-id="f0469-131">Adds a listener to the **sharedListeners** collection.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="f0469-132">Notes</span><span class="sxs-lookup"><span data-stu-id="f0469-132">Remarks</span></span>  
 <span data-ttu-id="f0469-133">Si un écouteur est défini dans un `<add>` élément de la `<sharedListeners>` élément, le filtre de cet écouteur doit être défini dans un `<filter>` élément qui est un enfant de le `<add>` élément.</span><span class="sxs-lookup"><span data-stu-id="f0469-133">If a listener is defined in an `<add>` element of the `<sharedListeners>` element, the filter for that listener should be defined in a `<filter>` element that is a child of the `<add>` element.</span></span>  
  
 <span data-ttu-id="f0469-134">Cet élément peut être utilisé dans le fichier de configuration machine (Machine.config) et le fichier de configuration d’application.</span><span class="sxs-lookup"><span data-stu-id="f0469-134">This element can be used in the machine configuration file (Machine.config) and the application configuration file.</span></span>  
  
## <a name="example"></a><span data-ttu-id="f0469-135">Exemple</span><span class="sxs-lookup"><span data-stu-id="f0469-135">Example</span></span>  
 <span data-ttu-id="f0469-136">L’exemple suivant montre comment utiliser le `<filter>` élément pour ajouter un filtre à l’écouteur de suivi `console` dans le `sharedListeners` collection.</span><span class="sxs-lookup"><span data-stu-id="f0469-136">The following example shows how to use the `<filter>` element to add a filter to the trace listener `console` in the `sharedListeners` collection.</span></span>  
  
```xml  
<configuration>  
  <system.diagnostics>  
    <sources>  
      <source name="myTraceSource" >  
        <listeners>  
          <add name="console" />  
          <remove name="Default" />  
        </listeners>  
      </source>  
    </sources>  
    <sharedListeners>  
      <add name="console"   
        type="System.Diagnostics.ConsoleTraceListener" >  
        <filter type="System.Diagnostics.EventTypeFilter"   
          initializeData="Error" />  
      </add>  
    </sharedListeners>  
  </system.diagnostics>  
</configuration>  
```  
  
## <a name="see-also"></a><span data-ttu-id="f0469-137">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f0469-137">See also</span></span>

- <xref:System.Diagnostics.TraceFilter>
- <xref:System.Diagnostics.TraceListener>
- <xref:System.Diagnostics.TraceSource>
- [<span data-ttu-id="f0469-138">Schéma des paramètres de trace et de débogage</span><span class="sxs-lookup"><span data-stu-id="f0469-138">Trace and Debug Settings Schema</span></span>](../../../../../docs/framework/configure-apps/file-schema/trace-debug/index.md)
