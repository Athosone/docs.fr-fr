---
title: Élément <assemblyIdentity> pour <runtime>
ms.date: 03/30/2017
f1_keywords:
- http://schemas.microsoft.com/.NetConfiguration/v2.0#configuration/runtime/assemblyBinding/dependentAssembly/assemblyIdentity
- http://schemas.microsoft.com/.NetConfiguration/v2.0#assemblyIdentity
helpviewer_keywords:
- <assemblyIdentity> element
- container tags, <assemblyIdentity> element
- assemblyIdentity element
ms.assetid: cea4d187-6398-4da4-af09-c1abc6a349c1
ms.openlocfilehash: d5766b76f18dce441cb260887a753dcf64642a6f
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59098697"
---
# <a name="assemblyidentity-element-for-runtime"></a>\<assemblyIdentity >, élément pour \<runtime >
Contient des informations d’identification sur l’assembly.  
  
 \<configuration>  
\<runtime>  
\<assemblyBinding>  
\<dependentAssembly>  
\<assemblyIdentity>  
  
## <a name="syntax"></a>Syntaxe  
  
```xml  
   <assemblyIdentity    
name="assembly name"  
publicKeyToken="public key token"  
culture="assembly culture"/>  
```  
  
## <a name="attributes-and-elements"></a>Attributs et éléments  
 Les sections suivantes décrivent des attributs, des éléments enfants et des éléments parents.  
  
### <a name="attributes"></a>Attributs  
  
|Attribut|Description|  
|---------------|-----------------|  
|`name`|Attribut requis.<br /><br /> Le nom de l’assembly|  
|`culture`|Attribut facultatif.<br /><br /> Chaîne qui spécifie la langue et le pays/région de l’assembly.|  
|`publicKeyToken`|Attribut facultatif.<br /><br /> Une valeur hexadécimale qui spécifie le nom fort de l’assembly.|  
|`processorArchitecture`|Attribut facultatif.<br /><br /> Une des valeurs « x86 », « amd64 », « msil » ou « ia64 », en spécifiant l’architecture de processeur pour un assembly qui contient le code spécifique au processeur. Les valeurs ne respectent pas la casse. Si l’attribut est assigné à une autre valeur, l’ensemble `<assemblyIdentity>` élément est ignoré. Consultez <xref:System.Reflection.ProcessorArchitecture>.|  
  
## <a name="processorarchitecture-attribute"></a>processorArchitecture attribut  
  
|Value|Description|  
|-----------|-----------------|  
|`amd64`|AMD 64 x86 uniquement à l’architecture.|  
|`ia64`|Uniquement à l’architecture Intel Itanium.|  
|`msil`|Neutre en ce qui concerne le processeur et bits par mot.|  
|`x86`|Un x86 32 bits processeur, natif ou dans le Windows sur l’environnement Windows (WOW) sur une plateforme 64 bits.|  
  
### <a name="child-elements"></a>Éléments enfants  
 Aucun.  
  
### <a name="parent-elements"></a>Éléments parents  
  
|Élément|Description|  
|-------------|-----------------|  
|`assemblyBinding`|Contient des informations à propos de la redirection des versions d'assemblys et de l'emplacement de ces derniers.|  
|`configuration`|Élément racine de chaque fichier de configuration utilisé par le Common Language Runtime et les applications .NET Framework.|  
|`dependentAssembly`|Encapsule la stratégie de liaisons et l’emplacement de chaque assembly. Utilisez une `<dependentAssembly>` élément pour chaque assembly.|  
|`runtime`|Contient des informations sur les liaisons d’assembly et l’opération garbage collection.|  
  
## <a name="remarks"></a>Notes  
 Chaque  **\<dependentAssembly >** élément doit avoir un  **\<assemblyIdentity >** élément enfant.  
  
 Si le `processorArchitecture` attribut n’est présent, le `<assemblyIdentity>` élément s’applique uniquement à l’assembly avec l’architecture de processeur correspondant. Si le `processorArchitecture` attribut n’est pas présent, le `<assemblyIdentity>` élément peut s’appliquer à un assembly avec une architecture de processeur.  
  
 L’exemple suivant montre un fichier de configuration pour les deux assemblys portant le même nom qui ciblent deux architectures de processeur de deux différentes, et dont les versions n’ont pas été préservées restent synchronisées. Lorsque l’application s’exécute sur le x86 plate-forme le premier `<assemblyIdentity>` élément s’applique et l’autre est ignorée. Si l’application s’exécute sur une plateforme différente x86 ou ia64, les deux sont ignorés.  
  
```xml  
<configuration>  
   <runtime>  
      <assemblyBinding xmlns="urn:schemas-microsoft-com:asm.v1">  
         <dependentAssembly>  
            <assemblyIdentity name="MyAssembly"  
                  publicKeyToken="14a739be0244c389"  
                  culture="neutral"  
                  processorArchitecture="x86" />  
            <bindingRedirect oldVersion= "1.0.0.0"   
                  newVersion="1.1.0.0" />  
         </dependentAssembly>  
         <dependentAssembly>  
            <assemblyIdentity name="MyAssembly"  
                  publicKeyToken="14a739be0244c389"  
                  culture="neutral"   
                  processorArchitecture="ia64" />  
            <bindingRedirect oldVersion="1.0.0.0"   
                  newVersion="2.0.0.0" />  
         </dependentAssembly>  
      </assemblyBinding>  
   </runtime>  
</configuration>  
```  
  
 Si un fichier de configuration contient un `<assemblyIdentity>` élément sans `processorArchitecture` d’attribut et ne contient pas d’élément qui correspond à la plateforme, l’élément sans le `processorArchitecture` attribut est utilisé.  
  
## <a name="example"></a>Exemple  
 L’exemple suivant montre comment fournir des informations relatives à un assembly.  
  
```xml  
<configuration>  
   <runtime>  
      <assemblyBinding xmlns="urn:schemas-microsoft-com:asm.v1">  
         <dependentAssembly>  
            <assemblyIdentity name="myAssembly"  
                              publicKeyToken="32ab4ba45e0a69a1"  
                              culture="neutral" />  
            <!--Redirection and codeBase policy for myAssembly.-->  
         </dependentAssembly>  
      </assemblyBinding>  
   </runtime>  
</configuration>  
```  
  
## <a name="see-also"></a>Voir aussi

- [Schéma des paramètres d’exécution](../../../../../docs/framework/configure-apps/file-schema/runtime/index.md)
- [Schéma des fichiers de configuration](../../../../../docs/framework/configure-apps/file-schema/index.md)
- [Redirection des versions d'assemblys](../../../../../docs/framework/configure-apps/redirect-assembly-versions.md)
