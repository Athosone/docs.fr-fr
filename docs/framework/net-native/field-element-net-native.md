---
title: <Field> Élément (.NET Native)
ms.date: 03/30/2017
ms.assetid: 6a14125f-1a8d-41a1-8a32-659ca0ad12de
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: c58be27334bcb862367464475a4eade5e01bdbb2
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61868536"
---
# <a name="field-element-net-native"></a>\<Champ >, élément (.NET Native)
Applique la stratégie de réflexion runtime à un champ.  
  
## <a name="syntax"></a>Syntaxe  
  
```xml  
<Field Name="field_name"  
       Browse="policy_type"  
       Dynamic="policy_type"  
       Serialize="policy_type" />  
```  
  
## <a name="attributes-and-elements"></a>Attributs et éléments  
 Les sections suivantes décrivent des attributs, des éléments enfants et des éléments parents.  
  
### <a name="attributes"></a>Attributs  
  
|Attribut|Type d'attribut|Description|  
|---------------|--------------------|-----------------|  
|`Name`|Général|Attribut requis. Spécifie le nom du champ.|  
|`Browse`|Réflexion|Attribut facultatif. Contrôle la demande d'informations sur le champ ou l'énumération de celui-ci, mais ne permet pas d'effectuer un accès dynamique au moment de l'exécution.|  
|`Dynamic`|Réflexion|Attribut facultatif. Contrôle l'accès au champ au moment de l'exécution pour autoriser la programmation dynamique. Grâce à cette stratégie, un champ peut être défini ou récupéré dynamiquement au moment de l'exécution.|  
|`Serialize`|Sérialisation|Attribut facultatif. Contrôle l'accès à un champ au moment de l'exécution pour permettre aux instances de type d'être sérialisées par des bibliothèques, telles que le sérialiseur JSON Newtonsoft, ou d'être utilisées pour la liaison de données.|  
  
## <a name="name-attribute"></a>Name (attribut)  
  
|Value|Description|  
|-----------|-----------------|  
|*nom_méthode*|Nom du champ. Le type du champ est défini par l’élément [\<Type>](../../../docs/framework/net-native/type-element-net-native.md) ou [\<TypeInstantiation>](../../../docs/framework/net-native/typeinstantiation-element-net-native.md) parent.|  
  
## <a name="all-other-attributes"></a>Tous les autres attributs  
  
|Value|Description|  
|-----------|-----------------|  
|*paramètre_stratégie*|Paramètre à appliquer à ce type de stratégie pour le champ. Les valeurs possibles sont `Auto`, `Excluded`, `Included` et `Required`. Pour plus d’informations, consultez [Paramètres de stratégie de directive runtime](../../../docs/framework/net-native/runtime-directive-policy-settings.md).|  
  
### <a name="child-elements"></a>Éléments enfants  
 Aucun.  
  
### <a name="parent-elements"></a>Éléments parents  
  
|Élément|Description|  
|-------------|-----------------|  
|[\<Type>](../../../docs/framework/net-native/type-element-net-native.md)|Applique la stratégie de réflexion à un type et à tous ses membres.|  
|[\<TypeInstantiation>](../../../docs/framework/net-native/typeinstantiation-element-net-native.md)|Applique la stratégie de réflexion à un type générique construit et à tous ses membres.|  
  
## <a name="remarks"></a>Notes  
 Si la stratégie d'un champ n'est pas définie explicitement, elle hérite la stratégie runtime de son élément parent.  
  
## <a name="see-also"></a>Voir aussi

- [Éléments de directive runtime](../../../docs/framework/net-native/runtime-directive-elements.md)
- [Guide de référence du fichier de configuration des directives runtime (rd.xml)](../../../docs/framework/net-native/runtime-directives-rd-xml-configuration-file-reference.md)
- [Paramètres de stratégie de directive runtime](../../../docs/framework/net-native/runtime-directive-policy-settings.md)
