---
title: <remove> Élément pour <listeners> pour <source>
ms.date: 03/30/2017
f1_keywords:
- http://schemas.microsoft.com/.NetConfiguration/v2.0#configuration/system.diagnostics/sources/source/listeners/remove
helpviewer_keywords:
- remove element for <listeners> for <source>
- <remove> element for <listeners> for <source>
ms.assetid: 3ff6b578-273d-407f-b07f-8251f1f9f5d0
ms.openlocfilehash: 4809c471deb51e0560b438b5a2c8849daad34ca0
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59120131"
---
# <a name="remove-element-for-listeners-for-source"></a>\<Supprimer >, élément pour \<écouteurs > pour \<source >
Supprime un écouteur de la collection `Listeners` pour une source de trace.  
  
 \<configuration>  
\<system.diagnostics>  
\<sources>  
\<source>  
\<listeners>  
\<remove>  
  
## <a name="syntax"></a>Syntaxe  
  
```xml  
<remove name="listenerName" />  
```  
  
## <a name="attributes-and-elements"></a>Attributs et éléments  
 Les sections suivantes décrivent des attributs, des éléments enfants et des éléments parents.  
  
### <a name="attributes"></a>Attributs  
  
|Attribut|Description|  
|---------------|-----------------|  
|`name`|Attribut requis.<br /><br /> Le nom de l’écouteur à supprimer de la `Listeners` collection.|  
  
### <a name="child-elements"></a>Éléments enfants  
 Aucun.  
  
### <a name="parent-elements"></a>Éléments parents  
  
|Élément|Description|  
|-------------|-----------------|  
|`configuration`|Élément racine de chaque fichier de configuration utilisé par le Common Language Runtime et les applications .NET Framework.|  
|`system.diagnostics`|Spécifie les écouteurs de trace qui collectent, stockent et acheminent les messages, ainsi que le niveau auquel un commutateur de trace est défini.|  
|`sources`|Contient les sources de trace qui lancent des messages de traçage.|  
|`source`|Spécifie une source de trace qui lance des messages de traçage.|  
|`listeners`|Spécifie des écouteurs qui collectent, stockent et acheminent les messages.|  
  
## <a name="remarks"></a>Notes  
 Le `<remove>` élément supprime un écouteur spécifié de la `Listeners` collection pour une source de trace.  
  
 Vous pouvez supprimer un élément à partir de la `Listeners` collection pour une source de suivi par programme en appelant le <xref:System.Diagnostics.TraceListenerCollection.Remove%2A> méthode sur le <xref:System.Diagnostics.TraceSource.Listeners%2A> propriété de la <xref:System.Diagnostics.TraceSource> instance.  
  
 Cet élément peut être utilisé dans le fichier de configuration machine (Machine.config) et le fichier de configuration d’application.  
  
## <a name="example"></a>Exemple  
 L’exemple suivant montre comment utiliser le `<remove>` élément avant d’utiliser le `<add>` élément pour ajouter l’écouteur `console` à la `Listeners` collection pour la source de suivi `TraceSourceApp`.  
  
```xml  
<configuration>  
  <system.diagnostics>  
    <sources>  
      <source name="TraceSourceApp" switchName="sourceSwitch"   
         switchType="System.Diagnostics.SourceSwitch" >  
         <listeners>  
           <remove name="Default"/>  
           <add name="console"   
             type="System.Diagnostics.ConsoleTraceListener" />  
         </listeners>  
      </source>  
    </sources>  
  </system.diagnostics>  
</configuration>   
```  
  
## <a name="see-also"></a>Voir aussi

- <xref:System.Diagnostics.TraceSource.Listeners%2A>
- <xref:System.Diagnostics.TraceSource>
- [Schéma des paramètres de trace et de débogage](../../../../../docs/framework/configure-apps/file-schema/trace-debug/index.md)
- [\<clear>](../../../../../docs/framework/configure-apps/file-schema/trace-debug/clear-element-for-listeners-for-source.md)
- [Écouteurs de suivi](../../../../../docs/framework/debug-trace-profile/trace-listeners.md)
