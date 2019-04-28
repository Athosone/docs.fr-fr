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
# <a name="add-element-for-listeners-for-trace"></a>\<Ajouter > élément pour \<écouteurs > pour \<trace >
Ajoute un écouteur à la **écouteurs** collection.  
  
 \<configuration>  
\<system.diagnostics>  
\<trace>  
\<listeners>  
\<add>  
  
## <a name="syntax"></a>Syntaxe  
  
```xml  
<add name="name"   
     type="trace listener class name, Version, Culture, PublicKeyToken"  
     initializeData="data"/>  
```  
  
## <a name="attributes-and-elements"></a>Attributs et éléments  
 Les sections suivantes décrivent des attributs, des éléments enfants et des éléments parents.  
  
### <a name="attributes"></a>Attributs  
  
|Attribut|Description|  
|---------------|-----------------|  
|**type**|Attribut requis.<br /><br /> Spécifie le type de l’écouteur. Vous devez utiliser une chaîne conforme aux exigences spécifiées dans [spécifiant des noms de types qualifiés complets](../../../../../docs/framework/reflection-and-codedom/specifying-fully-qualified-type-names.md).|  
|**initializeData**|Attribut facultatif.<br /><br /> La chaîne passée au constructeur pour la classe spécifiée.|  
|**name**|Attribut facultatif.<br /><br /> Spécifie le nom de l’écouteur.|  
  
### <a name="child-elements"></a>Éléments enfants  
  
|Élément|Description|  
|-------------|-----------------|  
|[\<filter>](../../../../../docs/framework/configure-apps/file-schema/trace-debug/filter-element-for-add-for-listeners-for-trace.md)|Ajoute un filtre à un écouteur dans la `Listeners` collection pour une trace.|  
  
### <a name="parent-elements"></a>Éléments parents  
  
|Élément|Description|  
|-------------|-----------------|  
|`configuration`|Élément racine de chaque fichier de configuration utilisé par le Common Language Runtime et les applications .NET Framework.|  
|`listeners`|Spécifie un écouteur qui collecte, stocke et achemine les messages. Les écouteurs dirigent la sortie de traçage vers une cible appropriée.|  
|`system.diagnostics`|Spécifie l'élément racine de la section de configuration ASP.NET.|  
|`trace`|Contient les écouteurs qui collectent, stockent et acheminent les messages de traçage.|  
  
## <a name="remarks"></a>Notes  
 Le <xref:System.Diagnostics.Debug> et <xref:System.Diagnostics.Trace> classes partagent le même **écouteurs** collection. Si vous ajoutez un objet écouteur à la collection dans un de ces classes, l’autre classe utilise le même écouteur. Les classes d’écouteur dérivent le <xref:System.Diagnostics.TraceListener>.  
  
 Si vous ne spécifiez pas le `name` attribut de l’écouteur de suivi, le <xref:System.Diagnostics.TraceListener.Name%2A> de l’écouteur trace par défaut, une chaîne vide (« »). Si votre application comporte un seul écouteur, vous pouvez ajouter sans spécifier un nom et supprimez-la en spécifiant une chaîne vide pour le nom. Toutefois, si votre application a plusieurs écouteurs, vous devez spécifier des noms uniques pour chaque écouteur de trace, qui vous permet d’identifier et de gérer des écouteurs de trace individuels dans le <xref:System.Diagnostics.Debug.Listeners%2A> et <xref:System.Diagnostics.Trace.Listeners%2A> collections.  
  
> [!NOTE]
>  Ajout de plusieurs écouteurs de trace du même type et avec le même nommez entraîne l’écouteur de suivi qu’un seul de ce type et ajouté à la `Listeners` collection. Toutefois, vous pouvez ajouter par programmation plusieurs écouteurs identiques à la `Listeners` collection.  
  
 La valeur de la **initializeData** attribut varie selon le type d’écouteur que vous créez. Pas tous les écouteurs de trace nécessitent que vous spécifiez **initializeData**.  
  
> [!NOTE]
>  Lorsque vous utilisez le `initializeData` attribut, vous risquez d’obtenir le compilateur Avertissement : « l’attribut 'initializeData' n’est pas déclaré. ». Cet avertissement se produit parce que les paramètres de configuration sont validés par rapport à la classe de base abstraite <xref:System.Diagnostics.TraceListener>, qui ne reconnaît pas le `initializeData` attribut. En règle générale, vous pouvez ignorer cet avertissement pour les implémentations d’écouteur de trace qui ont un constructeur qui accepte un paramètre.  
  
 Le tableau suivant présente les écouteurs de trace qui sont inclus avec le .NET Framework et décrit la valeur de leur **initializeData** attributs.  
  
|Classe d’écouteur de trace|valeur de l’attribut initializeData|  
|--------------------------|------------------------------------|  
|<xref:System.Diagnostics.ConsoleTraceListener?displayProperty=nameWithType>|Le `useErrorStream` valeur pour le <xref:System.Diagnostics.ConsoleTraceListener.%23ctor%2A> constructeur.  Définir le `initializeData` attribut «`true`» pour écrire la trace et debug de sortie à <xref:System.Console.Error%2A?displayProperty=nameWithType>; «`false`» pour écrire dans <xref:System.Console.Out%2A?displayProperty=nameWithType>.|  
|<xref:System.Diagnostics.DelimitedListTraceListener?displayProperty=nameWithType>|Le nom du fichier le <xref:System.Diagnostics.DelimitedListTraceListener> écrit dans.|  
|<xref:System.Diagnostics.EventLogTraceListener?displayProperty=nameWithType>|Le nom du nom d’une source existante de journal des événements.|  
|<xref:System.Diagnostics.EventSchemaTraceListener?displayProperty=nameWithType>|Le nom du fichier qui le <xref:System.Diagnostics.EventSchemaTraceListener> écrit dans.|  
|<xref:System.Diagnostics.TextWriterTraceListener?displayProperty=nameWithType>|Le nom du fichier qui le <xref:System.Diagnostics.TextWriterTraceListener> écrit dans.|  
|<xref:System.Diagnostics.XmlWriterTraceListener?displayProperty=nameWithType>|Le nom du fichier qui le <xref:System.Diagnostics.XmlWriterTraceListener> écrit dans.|  
  
## <a name="example"></a>Exemple  
 L’exemple suivant montre comment utiliser  **\<Ajouter >** éléments à ajouter les écouteurs `MyListener` et `MyEventListener` à la **écouteurs** collection. `MyListener` Crée un fichier appelé `MyListener.log` et écrit la sortie dans le fichier. `MyEventListener` Crée une entrée dans le journal des événements.  
  
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
  
## <a name="see-also"></a>Voir aussi

- <xref:System.Diagnostics.Trace>
- <xref:System.Diagnostics.Debug>
- <xref:System.Diagnostics.EventLogTraceListener>
- <xref:System.Diagnostics.ConsoleTraceListener>
- <xref:System.Diagnostics.TextWriterTraceListener>
- [Schéma des paramètres de trace et de débogage](../../../../../docs/framework/configure-apps/file-schema/trace-debug/index.md)
- [Écouteurs de suivi](../../../../../docs/framework/debug-trace-profile/trace-listeners.md)
