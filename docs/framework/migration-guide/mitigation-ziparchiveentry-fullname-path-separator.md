---
title: 'Atténuation : séparateur de chemin ZipArchiveEntry.FullName'
ms.date: 03/30/2017
helpviewer_keywords:
- application compatibility
- ',NET Framework application compatibility'
- .NET Framework 4.6.1
- .NET Framework 4.6.1 retargeting changes
- retargeting changes
ms.assetid: 8d575722-4fb6-49a2-8a06-f72d62dc3766
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: eba871215f33e4d3b50054e9ceaa92be090d0143
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59125105"
---
# <a name="mitigation-ziparchiveentryfullname-path-separator"></a>Atténuation : séparateur de chemin ZipArchiveEntry.FullName
À compter des applications qui ciblent le [!INCLUDE[net_v461](../../../includes/net-v461-md.md)], le séparateur de chemin utilisé dans la propriété <xref:System.IO.Compression.ZipArchiveEntry.FullName%2A?displayProperty=nameWithType> a été changé. Il ne s’agit plus de la barre oblique inverse (« \\ ») utilisée dans les versions antérieures du .NET Framework, mais de la barre oblique (« / »).   <xref:System.IO.Compression.ZipArchiveEntry?displayProperty=nameWithType> Les objets sont créés par un appel à l’une des surcharges de la méthode <xref:System.IO.Compression.ZipFile.CreateFromDirectory%2A?displayProperty=nameWithType>.  
  
## <a name="impact"></a>Impact  
 L’implémentation .NET est ainsi conforme à la section 4.4.17.1 des [Spécifications relatives au format des fichiers ZIP](https://pkware.cachefly.net/webdocs/casestudies/APPNOTE.TXT) et permet aux archives ZIP d’être décompressées sur des systèmes non Windows.  
  
 Décompresser un fichier zip créé par une application qui cible une version antérieure de .NET Framework sur les systèmes d’exploitation non Windows tels que les ordinateurs Macintosh ne permet pas de conserver la structure de répertoire. Par exemple, pour les ordinateurs Macintosh, cela crée un ensemble de fichiers dont le nom concatène le chemin d’accès, ainsi que toute barre oblique inverse (« \\ ») et le nom de fichier. Par conséquent, la structure de répertoires des fichiers décompressés n’est pas conservée.  
  
 L’impact de ce changement sur les fichiers .ZIP qui sont décompressés sur le système d’exploitation Windows par les API dans l’espace de noms <xref:System.IO> du .NET Framework doit être minimal, étant donné que ces API peuvent gérer sans problème aussi bien une barre oblique (« / ») qu’une barre oblique inverse (« \\ ») comme séparateur de chemin.  
  
## <a name="mitigation"></a>Atténuation  
 Si ce comportement n’est pas souhaitable, vous pouvez choisir de l’annuler en ajoutant un paramètre de configuration pour la section [\<runtime>](../../../docs/framework/configure-apps/file-schema/runtime/runtime-element.md) du fichier de configuration de votre application. L’exemple suivant montre la section `<runtime>` et l’option d’annulation.  
  
```xml  
<runtime>  
   <AppContextSwitchOverrides value="Switch.System.IO.Compression.ZipFile.UseBackslash=true" />  
</runtime>  
```  
  
 De plus, les applications qui ciblent des versions antérieures du .NET Framework, mais qui s’exécutent sur le [!INCLUDE[net_v461](../../../includes/net-v461-md.md)] ou ultérieur peuvent adhérer à ce comportement en ajoutant un paramètre de configuration dans la section [\<runtime>](../../../docs/framework/configure-apps/file-schema/runtime/runtime-element.md) du fichier de configuration de l’application. L’exemple suivant montre la section `<runtime>` et l’option d’activation.  
  
```xml  
<runtime>  
   <AppContextSwitchOverrides value="Switch.System.IO.Compression.ZipFile.UseBackslash=false" />  
</runtime>  
```  
  
## <a name="see-also"></a>Voir aussi

- [Modifications de reciblage](../../../docs/framework/migration-guide/retargeting-changes-in-the-net-framework-4-6-1.md)
- [Compatibilité des applications dans la version 4.6.1](../../../docs/framework/migration-guide/application-compatibility-in-the-net-framework-4-6-1.md)
