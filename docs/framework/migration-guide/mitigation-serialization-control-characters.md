---
title: 'Atténuation : sérialisation des caractères de contrôle avec DataContractJsonSerializer'
ms.date: 04/07/2017
helpviewer_keywords:
- .NET Framework 4.7 retargeting changes
- retargeting changes
- DataContractJsonSerializer changes
- serialization changes
ms.assetid: e065d458-a128-44f2-9f17-66af9d5be954
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 3355841298e039652eb81918eac98186c1a1f833
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59182115"
---
# <a name="mitigation-serialization-of-control-characters-with-the-datacontractjsonserializer"></a>Atténuation : sérialisation des caractères de contrôle avec DataContractJsonSerializer

À compter du .NET Framework 4.7, la manière dont les caractères de contrôle sont sérialisés avec le <xref:System.Runtime.Serialization.Json.DataContractJsonSerializer> a changé pour être conforme à ECMAScript V6 et V8. 
 
## <a name="impact"></a>Impact

Dans le .NET Framework 4.6.2 et versions antérieures, le <xref:System.Runtime.Serialization.Json.DataContractJsonSerializer> ne sérialise pas certains caractères de contrôle spéciaux, comme `\b`, `\f` et `\t`, d’une manière compatible avec les normes ECMAScript V6 et V8.

Pour les applications qui ciblent des versions de .NET Framework ultérieures à 4.7, la sérialisation de ces caractères de contrôle est compatible avec ECMAScript V6 et V8. Les API suivantes sont concernées :

- <xref:System.Runtime.Serialization.Json.DataContractJsonSerializer.WriteObject%2A> 
- <xref:System.Runtime.Serialization.Json.DataContractJsonSerializer.WriteObject%2A>
- <xref:System.Runtime.Serialization.Json.DataContractJsonSerializer.WriteObject%2A>

## <a name="mitigation"></a>Atténuation

Pour les applications qui ciblent des versions de .NET Framework ultérieures à la 4.7, ce comportement est activé par défaut.

Si ce comportement n’est pas souhaitable, vous pouvez désactiver cette fonctionnalité en ajoutant la ligne suivante à la section `<runtime>` du fichier app.config ou au fichier web.config :

```xml
<runtime>
   <AppContextSwitchOverrides value="Switch.System.Runtime.Serialization.DoNotUseECMAScriptV6EscapeControlCharacter=false" />
</runtime>
```
 
## <a name="see-also"></a>Voir aussi

- [Reciblage des modifications dans le .NET Framework 4.7](../../../docs/framework/migration-guide/retargeting-changes-in-the-net-framework-4-7.md)
