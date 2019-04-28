---
title: <add> Élément pour <listeners> pour <trace>
ms.date: 03/30/2017
f1_keywords:
- http://schemas.microsoft.com/.NetConfiguration/v2.0#configuration/system.diagnostics/trace/listeners/add
helpviewer_keywords:
- initializeData attribute
- <add> element for <listeners>
- add element for <listeners>
ms.assetid: 81e804a3-ef11-4d39-bbde-bfa012c179e2
ms.openlocfilehash: ba0ffc4f95b9af7fcd319068501ce0bb9714c2ad
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61673971"
---
# <a name="add-element-for-listeners-for-trace"></a><span data-ttu-id="43417-102">\<Ajouter > élément pour \<écouteurs > pour \<trace ></span><span class="sxs-lookup"><span data-stu-id="43417-102">\<add> Element for \<listeners> for \<trace></span></span>
<span data-ttu-id="43417-103">Ajoute un écouteur à la **écouteurs** collection.</span><span class="sxs-lookup"><span data-stu-id="43417-103">Adds a listener to the **Listeners** collection.</span></span>  
  
 <span data-ttu-id="43417-104">\<configuration></span><span class="sxs-lookup"><span data-stu-id="43417-104">\<configuration></span></span>  
<span data-ttu-id="43417-105">\<system.diagnostics></span><span class="sxs-lookup"><span data-stu-id="43417-105">\<system.diagnostics></span></span>  
<span data-ttu-id="43417-106">\<trace></span><span class="sxs-lookup"><span data-stu-id="43417-106">\<trace></span></span>  
<span data-ttu-id="43417-107">\<listeners></span><span class="sxs-lookup"><span data-stu-id="43417-107">\<listeners></span></span>  
<span data-ttu-id="43417-108">\<add></span><span class="sxs-lookup"><span data-stu-id="43417-108">\<add></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="43417-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="43417-109">Syntax</span></span>  
  
```xml  
<add name="name"   
     type="trace listener class name, Version, Culture, PublicKeyToken"  
     initializeData="data"/>  
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="43417-110">Attributs et éléments</span><span class="sxs-lookup"><span data-stu-id="43417-110">Attributes and Elements</span></span>  
 <span data-ttu-id="43417-111">Les sections suivantes décrivent des attributs, des éléments enfants et des éléments parents.</span><span class="sxs-lookup"><span data-stu-id="43417-111">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="43417-112">Attributs</span><span class="sxs-lookup"><span data-stu-id="43417-112">Attributes</span></span>  
  
|<span data-ttu-id="43417-113">Attribut</span><span class="sxs-lookup"><span data-stu-id="43417-113">Attribute</span></span>|<span data-ttu-id="43417-114">Description</span><span class="sxs-lookup"><span data-stu-id="43417-114">Description</span></span>|  
|---------------|-----------------|  
|<span data-ttu-id="43417-115">**type**</span><span class="sxs-lookup"><span data-stu-id="43417-115">**type**</span></span>|<span data-ttu-id="43417-116">Attribut requis.</span><span class="sxs-lookup"><span data-stu-id="43417-116">Required attribute.</span></span><br /><br /> <span data-ttu-id="43417-117">Spécifie le type de l’écouteur.</span><span class="sxs-lookup"><span data-stu-id="43417-117">Specifies the type of the listener.</span></span> <span data-ttu-id="43417-118">Vous devez utiliser une chaîne conforme aux exigences spécifiées dans [spécifiant des noms de types qualifiés complets](../../../../../docs/framework/reflection-and-codedom/specifying-fully-qualified-type-names.md).</span><span class="sxs-lookup"><span data-stu-id="43417-118">You must use a string that meets the requirements specified in [Specifying Fully Qualified Type Names](../../../../../docs/framework/reflection-and-codedom/specifying-fully-qualified-type-names.md).</span></span>|  
|<span data-ttu-id="43417-119">**initializeData**</span><span class="sxs-lookup"><span data-stu-id="43417-119">**initializeData**</span></span>|<span data-ttu-id="43417-120">Attribut facultatif.</span><span class="sxs-lookup"><span data-stu-id="43417-120">Optional attribute.</span></span><br /><br /> <span data-ttu-id="43417-121">La chaîne passée au constructeur pour la classe spécifiée.</span><span class="sxs-lookup"><span data-stu-id="43417-121">The string passed to the constructor for the specified class.</span></span>|  
|<span data-ttu-id="43417-122">**name**</span><span class="sxs-lookup"><span data-stu-id="43417-122">**name**</span></span>|<span data-ttu-id="43417-123">Attribut facultatif.</span><span class="sxs-lookup"><span data-stu-id="43417-123">Optional attribute.</span></span><br /><br /> <span data-ttu-id="43417-124">Spécifie le nom de l’écouteur.</span><span class="sxs-lookup"><span data-stu-id="43417-124">Specifies the name of the listener.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="43417-125">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="43417-125">Child Elements</span></span>  
  
|<span data-ttu-id="43417-126">Élément</span><span class="sxs-lookup"><span data-stu-id="43417-126">Element</span></span>|<span data-ttu-id="43417-127">Description</span><span class="sxs-lookup"><span data-stu-id="43417-127">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="43417-128">\<filter></span><span class="sxs-lookup"><span data-stu-id="43417-128">\<filter></span></span>](../../../../../docs/framework/configure-apps/file-schema/trace-debug/filter-element-for-add-for-listeners-for-trace.md)|<span data-ttu-id="43417-129">Ajoute un filtre à un écouteur dans la `Listeners` collection pour une trace.</span><span class="sxs-lookup"><span data-stu-id="43417-129">Adds a filter to a listener in the `Listeners` collection for a trace.</span></span>|  
  
### <a name="parent-elements"></a><span data-ttu-id="43417-130">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="43417-130">Parent Elements</span></span>  
  
|<span data-ttu-id="43417-131">Élément</span><span class="sxs-lookup"><span data-stu-id="43417-131">Element</span></span>|<span data-ttu-id="43417-132">Description</span><span class="sxs-lookup"><span data-stu-id="43417-132">Description</span></span>|  
|-------------|-----------------|  
|`configuration`|<span data-ttu-id="43417-133">Élément racine de chaque fichier de configuration utilisé par le Common Language Runtime et les applications .NET Framework.</span><span class="sxs-lookup"><span data-stu-id="43417-133">The root element in every configuration file used by the common language runtime and .NET Framework applications.</span></span>|  
|`listeners`|<span data-ttu-id="43417-134">Spécifie un écouteur qui collecte, stocke et achemine les messages.</span><span class="sxs-lookup"><span data-stu-id="43417-134">Specifies a listener that collects, stores, and routes messages.</span></span> <span data-ttu-id="43417-135">Les écouteurs dirigent la sortie de traçage vers une cible appropriée.</span><span class="sxs-lookup"><span data-stu-id="43417-135">Listeners direct the tracing output to an appropriate target.</span></span>|  
|`system.diagnostics`|<span data-ttu-id="43417-136">Spécifie l'élément racine de la section de configuration ASP.NET.</span><span class="sxs-lookup"><span data-stu-id="43417-136">Specifies the root element for the ASP.NET configuration section.</span></span>|  
|`trace`|<span data-ttu-id="43417-137">Contient les écouteurs qui collectent, stockent et acheminent les messages de traçage.</span><span class="sxs-lookup"><span data-stu-id="43417-137">Contains listeners that collect, store, and route tracing messages.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="43417-138">Notes</span><span class="sxs-lookup"><span data-stu-id="43417-138">Remarks</span></span>  
 <span data-ttu-id="43417-139">Le <xref:System.Diagnostics.Debug> et <xref:System.Diagnostics.Trace> classes partagent le même **écouteurs** collection.</span><span class="sxs-lookup"><span data-stu-id="43417-139">The <xref:System.Diagnostics.Debug> and <xref:System.Diagnostics.Trace> classes share the same **Listeners** collection.</span></span> <span data-ttu-id="43417-140">Si vous ajoutez un objet écouteur à la collection dans un de ces classes, l’autre classe utilise le même écouteur.</span><span class="sxs-lookup"><span data-stu-id="43417-140">If you add a listener object to the collection in one of these classes, the other class uses the same listener.</span></span> <span data-ttu-id="43417-141">Les classes d’écouteur dérivent le <xref:System.Diagnostics.TraceListener>.</span><span class="sxs-lookup"><span data-stu-id="43417-141">The listener classes derive from the <xref:System.Diagnostics.TraceListener>.</span></span>  
  
 <span data-ttu-id="43417-142">Si vous ne spécifiez pas le `name` attribut de l’écouteur de suivi, le <xref:System.Diagnostics.TraceListener.Name%2A> de l’écouteur trace par défaut, une chaîne vide (« »).</span><span class="sxs-lookup"><span data-stu-id="43417-142">If you do not specify the `name` attribute of the trace listener, the <xref:System.Diagnostics.TraceListener.Name%2A> of the trace listener defaults to an empty string ("").</span></span> <span data-ttu-id="43417-143">Si votre application comporte un seul écouteur, vous pouvez ajouter sans spécifier un nom et supprimez-la en spécifiant une chaîne vide pour le nom.</span><span class="sxs-lookup"><span data-stu-id="43417-143">If your application has only one listener, you can add it without specifying a name, and remove it by specifying an empty string for the name.</span></span> <span data-ttu-id="43417-144">Toutefois, si votre application a plusieurs écouteurs, vous devez spécifier des noms uniques pour chaque écouteur de trace, qui vous permet d’identifier et de gérer des écouteurs de trace individuels dans le <xref:System.Diagnostics.Debug.Listeners%2A> et <xref:System.Diagnostics.Trace.Listeners%2A> collections.</span><span class="sxs-lookup"><span data-stu-id="43417-144">However, if your application has more than one listener, you should specify unique names for each trace listener, which allows you to identify and manage individual trace listeners within the <xref:System.Diagnostics.Debug.Listeners%2A> and <xref:System.Diagnostics.Trace.Listeners%2A> collections.</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="43417-145">Ajout de plusieurs écouteurs de trace du même type et avec le même nommez entraîne l’écouteur de suivi qu’un seul de ce type et ajouté à la `Listeners` collection.</span><span class="sxs-lookup"><span data-stu-id="43417-145">Adding more than one trace listener of the same type and with the same name results in only one trace listener of that type and name being added to the `Listeners` collection.</span></span> <span data-ttu-id="43417-146">Toutefois, vous pouvez ajouter par programmation plusieurs écouteurs identiques à la `Listeners` collection.</span><span class="sxs-lookup"><span data-stu-id="43417-146">However, you can programmatically add multiple identical listeners to the `Listeners` collection.</span></span>  
  
 <span data-ttu-id="43417-147">La valeur de la **initializeData** attribut varie selon le type d’écouteur que vous créez.</span><span class="sxs-lookup"><span data-stu-id="43417-147">The value for the **initializeData** attribute depends on the type of listener you create.</span></span> <span data-ttu-id="43417-148">Pas tous les écouteurs de trace nécessitent que vous spécifiez **initializeData**.</span><span class="sxs-lookup"><span data-stu-id="43417-148">Not all trace listeners require that you specify **initializeData**.</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="43417-149">Lorsque vous utilisez le `initializeData` attribut, vous risquez d’obtenir le compilateur Avertissement : « l’attribut 'initializeData' n’est pas déclaré. ».</span><span class="sxs-lookup"><span data-stu-id="43417-149">When you use the `initializeData` attribute, you may get the compiler warning "The 'initializeData' attribute is not declared."</span></span> <span data-ttu-id="43417-150">Cet avertissement se produit parce que les paramètres de configuration sont validés par rapport à la classe de base abstraite <xref:System.Diagnostics.TraceListener>, qui ne reconnaît pas le `initializeData` attribut.</span><span class="sxs-lookup"><span data-stu-id="43417-150">This warning occurs because the configuration settings are validated against the abstract base class <xref:System.Diagnostics.TraceListener>, which does not recognize the `initializeData` attribute.</span></span> <span data-ttu-id="43417-151">En règle générale, vous pouvez ignorer cet avertissement pour les implémentations d’écouteur de trace qui ont un constructeur qui accepte un paramètre.</span><span class="sxs-lookup"><span data-stu-id="43417-151">Typically, you can ignore this warning for trace listener implementations that have a constructor that takes a parameter.</span></span>  
  
 <span data-ttu-id="43417-152">Le tableau suivant présente les écouteurs de trace qui sont inclus avec le .NET Framework et décrit la valeur de leur **initializeData** attributs.</span><span class="sxs-lookup"><span data-stu-id="43417-152">The following table shows the trace listeners that are included with the .NET Framework and describes the value of their **initializeData** attributes.</span></span>  
  
|<span data-ttu-id="43417-153">Classe d’écouteur de trace</span><span class="sxs-lookup"><span data-stu-id="43417-153">Trace listener class</span></span>|<span data-ttu-id="43417-154">valeur de l’attribut initializeData</span><span class="sxs-lookup"><span data-stu-id="43417-154">initializeData attribute value</span></span>|  
|--------------------------|------------------------------------|  
|<xref:System.Diagnostics.ConsoleTraceListener?displayProperty=nameWithType>|<span data-ttu-id="43417-155">Le `useErrorStream` valeur pour le <xref:System.Diagnostics.ConsoleTraceListener.%23ctor%2A> constructeur.</span><span class="sxs-lookup"><span data-stu-id="43417-155">The `useErrorStream` value for the <xref:System.Diagnostics.ConsoleTraceListener.%23ctor%2A> constructor.</span></span>  <span data-ttu-id="43417-156">Définir le `initializeData` attribut «`true`» pour écrire la trace et debug de sortie à <xref:System.Console.Error%2A?displayProperty=nameWithType>; «`false`» pour écrire dans <xref:System.Console.Out%2A?displayProperty=nameWithType>.</span><span class="sxs-lookup"><span data-stu-id="43417-156">Set the `initializeData` attribute to "`true`" to write trace and debug output to <xref:System.Console.Error%2A?displayProperty=nameWithType>; "`false`" to write to <xref:System.Console.Out%2A?displayProperty=nameWithType>.</span></span>|  
|<xref:System.Diagnostics.DelimitedListTraceListener?displayProperty=nameWithType>|<span data-ttu-id="43417-157">Le nom du fichier le <xref:System.Diagnostics.DelimitedListTraceListener> écrit dans.</span><span class="sxs-lookup"><span data-stu-id="43417-157">The name of the file the <xref:System.Diagnostics.DelimitedListTraceListener> writes to.</span></span>|  
|<xref:System.Diagnostics.EventLogTraceListener?displayProperty=nameWithType>|<span data-ttu-id="43417-158">Le nom du nom d’une source existante de journal des événements.</span><span class="sxs-lookup"><span data-stu-id="43417-158">The name of the name of an existing event log source.</span></span>|  
|<xref:System.Diagnostics.EventSchemaTraceListener?displayProperty=nameWithType>|<span data-ttu-id="43417-159">Le nom du fichier qui le <xref:System.Diagnostics.EventSchemaTraceListener> écrit dans.</span><span class="sxs-lookup"><span data-stu-id="43417-159">The name of the file that the <xref:System.Diagnostics.EventSchemaTraceListener> writes to.</span></span>|  
|<xref:System.Diagnostics.TextWriterTraceListener?displayProperty=nameWithType>|<span data-ttu-id="43417-160">Le nom du fichier qui le <xref:System.Diagnostics.TextWriterTraceListener> écrit dans.</span><span class="sxs-lookup"><span data-stu-id="43417-160">The name of the file that the <xref:System.Diagnostics.TextWriterTraceListener> writes to.</span></span>|  
|<xref:System.Diagnostics.XmlWriterTraceListener?displayProperty=nameWithType>|<span data-ttu-id="43417-161">Le nom du fichier qui le <xref:System.Diagnostics.XmlWriterTraceListener> écrit dans.</span><span class="sxs-lookup"><span data-stu-id="43417-161">The name of the file that the <xref:System.Diagnostics.XmlWriterTraceListener> writes to.</span></span>|  
  
## <a name="example"></a><span data-ttu-id="43417-162">Exemple</span><span class="sxs-lookup"><span data-stu-id="43417-162">Example</span></span>  
 <span data-ttu-id="43417-163">L’exemple suivant montre comment utiliser  **\<Ajouter >** éléments à ajouter les écouteurs `MyListener` et `MyEventListener` à la **écouteurs** collection.</span><span class="sxs-lookup"><span data-stu-id="43417-163">The following example shows how to use **\<add>** elements to add the listeners `MyListener` and `MyEventListener` to the **Listeners** collection.</span></span> <span data-ttu-id="43417-164">`MyListener` Crée un fichier appelé `MyListener.log` et écrit la sortie dans le fichier.</span><span class="sxs-lookup"><span data-stu-id="43417-164">`MyListener` creates a file called `MyListener.log` and writes the output to the file.</span></span> <span data-ttu-id="43417-165">`MyEventListener` Crée une entrée dans le journal des événements.</span><span class="sxs-lookup"><span data-stu-id="43417-165">`MyEventListener` creates an entry in the event log.</span></span>  
  
```xml  
<configuration>  
   <system.diagnostics>  
      <trace autoflush="true" indentsize="0">  
         <listeners>  
            <add name="myListener" type="System.Diagnostics.TextWriterTraceListener, system, version=1.0.3300.0, Culture=neutral, PublicKeyToken=b77a5c561934e089" initializeData="c:\myListener.log" />  
            <add name="MyEventListener"  
                 type="System.Diagnostics.EventLogTraceListener, system, version=1.0.3300.0, Culture=neutral, PublicKeyToken=b77a5c561934e089"                 initializeData="MyConfigEventLog"/>  
            <add name="configConsoleListener"  
                 type="System.Diagnostics.ConsoleTraceListener, system, version=1.0.3300.0, Culture=neutral, PublicKeyToken=b77a5c561934e089"/>  
         </listeners>  
      </trace>  
   </system.diagnostics>  
</configuration>  
```  
  
## <a name="see-also"></a><span data-ttu-id="43417-166">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="43417-166">See also</span></span>

- <xref:System.Diagnostics.Trace>
- <xref:System.Diagnostics.Debug>
- <xref:System.Diagnostics.EventLogTraceListener>
- <xref:System.Diagnostics.ConsoleTraceListener>
- <xref:System.Diagnostics.TextWriterTraceListener>
- [<span data-ttu-id="43417-167">Schéma des paramètres de trace et de débogage</span><span class="sxs-lookup"><span data-stu-id="43417-167">Trace and Debug Settings Schema</span></span>](../../../../../docs/framework/configure-apps/file-schema/trace-debug/index.md)
- [<span data-ttu-id="43417-168">Écouteurs de suivi</span><span class="sxs-lookup"><span data-stu-id="43417-168">Trace Listeners</span></span>](../../../../../docs/framework/debug-trace-profile/trace-listeners.md)
