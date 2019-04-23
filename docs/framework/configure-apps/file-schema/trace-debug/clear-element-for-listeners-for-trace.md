---
title: <clear> Élément pour <listeners> pour <trace>
ms.date: 03/30/2017
f1_keywords:
- http://schemas.microsoft.com/.NetConfiguration/v2.0#configuration/system.diagnostics/trace/listeners/clear
helpviewer_keywords:
- clear element for <listeners> for <trace>
- <clear> element for <listeners> for <trace>
ms.assetid: b44732a8-271f-4a06-ba9e-fe3298d6f192
ms.openlocfilehash: 97b18f9d6baa618b0f535955b232e2119c758b11
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59124889"
---
# <a name="clear-element-for-listeners-for-trace"></a>\<Désactivez >, élément pour \<écouteurs > pour \<trace >
Efface la collection `Listeners` de la trace.  
  
 \<configuration>  
\<system.diagnostics>  
\<trace>  
\<listeners>  
\<clear>  
  
## <a name="syntax"></a>Syntaxe  
  
```xml  
<clear/>  
```  
  
## <a name="attributes-and-elements"></a>Attributs et éléments  
 Les sections suivantes décrivent des attributs, des éléments enfants et des éléments parents.  
  
### <a name="attributes"></a>Attributs  
 Aucun.  
  
### <a name="child-elements"></a>Éléments enfants  
 Aucun.  
  
### <a name="parent-elements"></a>Éléments parents  
  
|Élément|Description|  
|-------------|-----------------|  
|`configuration`|Élément racine de chaque fichier de configuration utilisé par le Common Language Runtime et les applications .NET Framework.|  
|`system.diagnostics`|Spécifie les écouteurs de trace qui collectent, stockent et acheminent les messages, ainsi que le niveau auquel un commutateur de trace est défini.|  
|`trace`|Contient les écouteurs qui collectent, stockent et acheminent les messages de traçage.|  
|`listeners`|Contient des écouteurs qui collectent, stockent et acheminent les messages. Les écouteurs dirigent la sortie de traçage vers une cible appropriée.|  
  
## <a name="remarks"></a>Notes  
 Le `<clear>` élément supprime tous les écouteurs de la `Listeners` collection de la trace. Vous pouvez utiliser la `<clear>` élément avant d’utiliser le `<add>` pour garantir l’aucun autres écouteurs actifs dans la collection.  
  
 Vous pouvez effacer le `Listeners` collection par programmation en appelant le <xref:System.Diagnostics.TraceListenerCollection.Clear%2A> méthode sur le <xref:System.Diagnostics.Trace.Listeners%2A?displayProperty=nameWithType> propriété (`System.Diagnostics.Trace.Listeners.Clear()`).  
  
 Cet élément peut être utilisé dans le fichier de configuration machine (Machine.config) et le fichier de configuration d’application.  
  
> [!NOTE]
>  Le `<clear>` élément supprime le <xref:System.Diagnostics.DefaultTraceListener> à partir de la `Listeners` collection, la modification du comportement de la <xref:System.Diagnostics.Debug.Assert%2A?displayProperty=nameWithType>, <xref:System.Diagnostics.Trace.Assert%2A?displayProperty=nameWithType>, <xref:System.Diagnostics.Debug.Fail%2A?displayProperty=nameWithType>, et <xref:System.Diagnostics.Trace.Fail%2A?displayProperty=nameWithType> méthodes. Appeler un `Assert` ou `Fail` aboutit généralement à la méthode dans l’affichage d’un message. Toutefois, la boîte de message s’affiche pas si le <xref:System.Diagnostics.DefaultTraceListener> n’est pas dans le `Listeners` collection.  
  
## <a name="example"></a>Exemple  
 L’exemple suivant montre comment utiliser le `<clear>` élément avant d’utiliser le `<add>` élément pour ajouter l’écouteur `console` à la `Listeners` collection de la trace.  
  
```xml  
<configuration>  
  <system.diagnostics>  
    <trace autoflush="false" indentsize="4">  
      <listeners>  
        <clear/>  
        <add name="console"   
          type="System.Diagnostics.ConsoleTraceListener" >  
          <filter type="System.Diagnostics.EventTypeFilter"   
            initializeData="Error" />  
        </add>  
      </listeners>  
    </trace>  
  </system.diagnostics>  
</configuration>   
```  
  
## <a name="see-also"></a>Voir aussi

- <xref:System.Diagnostics.Trace.Listeners%2A>
- <xref:System.Diagnostics.Trace>
- <xref:System.Diagnostics.Debug>
- <xref:System.Diagnostics.TraceSource>
- [Schéma des paramètres de trace et de débogage](../../../../../docs/framework/configure-apps/file-schema/trace-debug/index.md)
- [\<remove>](../../../../../docs/framework/configure-apps/file-schema/trace-debug/remove-element-for-listeners-for-trace.md)
- [Écouteurs de suivi](../../../../../docs/framework/debug-trace-profile/trace-listeners.md)
