---
title: < System.diagnostics > (élément)
ms.date: 03/30/2017
f1_keywords:
- http://schemas.microsoft.com/.NetConfiguration/v2.0#system.diagnostics
- http://schemas.microsoft.com/.NetConfiguration/v2.0#configuration/system.diagnostics
helpviewer_keywords:
- <system.diagnostics> element
- system.diagnostics element
ms.assetid: 3f348f42-fa72-4ff2-aa1c-bb9eecad4bb2
ms.openlocfilehash: 026805ffb9b89aa55e84cf9a5c4afb8ed63cec09
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59142705"
---
# <a name="systemdiagnostics-element"></a><span data-ttu-id="b8a47-102">\<System.Diagnostics > élément</span><span class="sxs-lookup"><span data-stu-id="b8a47-102">\<system.diagnostics> Element</span></span>
<span data-ttu-id="b8a47-103">Spécifie les écouteurs de trace qui collectent, stockent et acheminent les messages, ainsi que le niveau auquel un commutateur de trace est défini.</span><span class="sxs-lookup"><span data-stu-id="b8a47-103">Specifies trace listeners that collect, store, and route messages and the level where a trace switch is set.</span></span>  
  
 <span data-ttu-id="b8a47-104">\<configuration></span><span class="sxs-lookup"><span data-stu-id="b8a47-104">\<configuration></span></span>  
<span data-ttu-id="b8a47-105">\<system.diagnostics></span><span class="sxs-lookup"><span data-stu-id="b8a47-105">\<system.diagnostics></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="b8a47-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="b8a47-106">Syntax</span></span>  
  
```xml  
<system.diagnostics>   
</system.diagnostics>  
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="b8a47-107">Attributs et éléments</span><span class="sxs-lookup"><span data-stu-id="b8a47-107">Attributes and Elements</span></span>  
 <span data-ttu-id="b8a47-108">Les sections suivantes décrivent des attributs, des éléments enfants et des éléments parents.</span><span class="sxs-lookup"><span data-stu-id="b8a47-108">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="b8a47-109">Attributs</span><span class="sxs-lookup"><span data-stu-id="b8a47-109">Attributes</span></span>  
 <span data-ttu-id="b8a47-110">Aucun.</span><span class="sxs-lookup"><span data-stu-id="b8a47-110">None.</span></span>  
  
### <a name="child-elements"></a><span data-ttu-id="b8a47-111">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="b8a47-111">Child Elements</span></span>  
  
|<span data-ttu-id="b8a47-112">Élément</span><span class="sxs-lookup"><span data-stu-id="b8a47-112">Element</span></span>|<span data-ttu-id="b8a47-113">Description</span><span class="sxs-lookup"><span data-stu-id="b8a47-113">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="b8a47-114">\<assert></span><span class="sxs-lookup"><span data-stu-id="b8a47-114">\<assert></span></span>](../../../../../docs/framework/configure-apps/file-schema/trace-debug/assert-element.md)|<span data-ttu-id="b8a47-115">Indique si une boîte de message doit s’afficher quand vous appelez la méthode <xref:System.Diagnostics.Debug.Assert%2A?displayProperty=nameWithType> ; spécifie également le nom du fichier dans lequel écrire les messages.</span><span class="sxs-lookup"><span data-stu-id="b8a47-115">Specifies whether to display a message box when you call the <xref:System.Diagnostics.Debug.Assert%2A?displayProperty=nameWithType> method; also specifies the name of the file to write messages to.</span></span>|  
|[<span data-ttu-id="b8a47-116">\<performanceCounters></span><span class="sxs-lookup"><span data-stu-id="b8a47-116">\<performanceCounters></span></span>](../../../../../docs/framework/configure-apps/file-schema/trace-debug/performancecounters-element.md)|<span data-ttu-id="b8a47-117">Spécifie la taille de la mémoire globale partagée par les compteurs de performances.</span><span class="sxs-lookup"><span data-stu-id="b8a47-117">Specifies the size of the global memory shared by performance counters.</span></span>|  
|[<span data-ttu-id="b8a47-118">\<sharedListeners></span><span class="sxs-lookup"><span data-stu-id="b8a47-118">\<sharedListeners></span></span>](../../../../../docs/framework/configure-apps/file-schema/trace-debug/sharedlisteners-element.md)|<span data-ttu-id="b8a47-119">Contient des écouteurs auxquels toute source ou tout élément de trace peuvent faire référence.</span><span class="sxs-lookup"><span data-stu-id="b8a47-119">Contains listeners that any source or trace element can reference.</span></span> <span data-ttu-id="b8a47-120">Écouteurs identifiés comme des écouteurs partagés peuvent être ajoutés à des sources ou des traces par nom.</span><span class="sxs-lookup"><span data-stu-id="b8a47-120">Listeners identified as shared listeners can be added to sources or traces by name.</span></span>|  
|[<span data-ttu-id="b8a47-121">\<sources></span><span class="sxs-lookup"><span data-stu-id="b8a47-121">\<sources></span></span>](../../../../../docs/framework/configure-apps/file-schema/trace-debug/sources-element.md)|<span data-ttu-id="b8a47-122">Spécifie les sources de trace qui initient des messages de suivi.</span><span class="sxs-lookup"><span data-stu-id="b8a47-122">Specifies trace sources that initiate tracing messages.</span></span>|  
|[<span data-ttu-id="b8a47-123">\<switches></span><span class="sxs-lookup"><span data-stu-id="b8a47-123">\<switches></span></span>](../../../../../docs/framework/configure-apps/file-schema/trace-debug/switches-element.md)|<span data-ttu-id="b8a47-124">Contient les commutateurs et les niveaux où les commutateurs de trace sont définies.</span><span class="sxs-lookup"><span data-stu-id="b8a47-124">Contains trace switches and the levels where the trace switches are set.</span></span>|  
|[<span data-ttu-id="b8a47-125">\<trace></span><span class="sxs-lookup"><span data-stu-id="b8a47-125">\<trace></span></span>](../../../../../docs/framework/configure-apps/file-schema/trace-debug/trace-element.md)|<span data-ttu-id="b8a47-126">Contient les écouteurs qui collectent, stockent et acheminent les messages de traçage.</span><span class="sxs-lookup"><span data-stu-id="b8a47-126">Contains listeners that collect, store, and route tracing messages.</span></span>|  
  
### <a name="parent-elements"></a><span data-ttu-id="b8a47-127">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="b8a47-127">Parent Elements</span></span>  
  
|<span data-ttu-id="b8a47-128">Élément</span><span class="sxs-lookup"><span data-stu-id="b8a47-128">Element</span></span>|<span data-ttu-id="b8a47-129">Description</span><span class="sxs-lookup"><span data-stu-id="b8a47-129">Description</span></span>|  
|-------------|-----------------|  
|`configuration`|<span data-ttu-id="b8a47-130">Élément racine de chaque fichier de configuration utilisé par le Common Language Runtime et les applications .NET Framework.</span><span class="sxs-lookup"><span data-stu-id="b8a47-130">The root element in every configuration file used by the common language runtime and .NET Framework applications.</span></span>|  
  
## <a name="example"></a><span data-ttu-id="b8a47-131">Exemple</span><span class="sxs-lookup"><span data-stu-id="b8a47-131">Example</span></span>  
 <span data-ttu-id="b8a47-132">L’exemple suivant montre comment incorporer un commutateur de trace et un écouteur de suivi à l’intérieur de la  **\<system.diagnostics >** élément.</span><span class="sxs-lookup"><span data-stu-id="b8a47-132">The following example shows how to embed a trace switch and a trace listener inside the **\<system.diagnostics>** element.</span></span> <span data-ttu-id="b8a47-133">Le `General` commutateur de trace est défini sur le <xref:System.Diagnostics.TraceLevel> niveau.</span><span class="sxs-lookup"><span data-stu-id="b8a47-133">The `General` trace switch is set to the <xref:System.Diagnostics.TraceLevel> level.</span></span> <span data-ttu-id="b8a47-134">L’écouteur de suivi `myListener` crée un fichier appelé `MyListener.log` et écrit la sortie dans le fichier.</span><span class="sxs-lookup"><span data-stu-id="b8a47-134">The trace listener `myListener` creates a file called `MyListener.log` and writes the output to the file.</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="b8a47-135">Dans .NET Framework 2.0, vous pouvez spécifier la valeur d'un commutateur avec du texte.</span><span class="sxs-lookup"><span data-stu-id="b8a47-135">In the .NET Framework version 2.0, you can use text to specify the value for a switch.</span></span> <span data-ttu-id="b8a47-136">Par exemple, vous pouvez spécifier `true` pour un <xref:System.Diagnostics.BooleanSwitch> ou utilisez le texte représentant une valeur d’énumération comme `Error` pour un <xref:System.Diagnostics.TraceSwitch>.</span><span class="sxs-lookup"><span data-stu-id="b8a47-136">For example, you can specify `true` for a <xref:System.Diagnostics.BooleanSwitch> or use the text representing an enumeration value such as `Error` for a <xref:System.Diagnostics.TraceSwitch>.</span></span> <span data-ttu-id="b8a47-137">La ligne `<add name="myTraceSwitch" value="Error" />` équivaut à `<add name="myTraceSwitch" value="1" />`.</span><span class="sxs-lookup"><span data-stu-id="b8a47-137">The line `<add name="myTraceSwitch" value="Error" />` is equivalent to `<add name="myTraceSwitch" value="1" />`.</span></span>  
  
```xml  
<configuration>  
   <system.diagnostics>  
      <switches>  
         <add name="General" value="4" />  
      </switches>  
      <trace autoflush="true" indentsize="2">  
         <listeners>  
            <add name="myListener" type="System.Diagnostics.TextWriterTraceListener, System, Version=1.0.3300.0, Culture=neutral, PublicKeyToken=b77a5c561934e089" initializeData="MyListener.log" traceOutputOptions="ProcessId, LogicalOperationStack, Timestamp, ThreadId, Callstack, DateTime" />  
         </listeners>  
      </trace>  
   </system.diagnostics>  
</configuration>  
```  
  
## <a name="see-also"></a><span data-ttu-id="b8a47-138">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b8a47-138">See also</span></span>

- <xref:System.Diagnostics.Trace>
- <xref:System.Diagnostics.Debug>
- [<span data-ttu-id="b8a47-139">Schéma des paramètres de trace et de débogage</span><span class="sxs-lookup"><span data-stu-id="b8a47-139">Trace and Debug Settings Schema</span></span>](../../../../../docs/framework/configure-apps/file-schema/trace-debug/index.md)
