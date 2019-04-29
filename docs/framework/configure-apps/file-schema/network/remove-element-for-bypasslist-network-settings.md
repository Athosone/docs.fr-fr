---
title: <remove>, élément de bypasslist (paramètres réseau)
ms.date: 03/30/2017
f1_keywords:
- http://schemas.microsoft.com/.NetConfiguration/v2.0#configuration/system.net/defaultProxy/bypasslist/remove
- http://schemas.microsoft.com/.NetConfiguration/v2.0#remove
helpviewer_keywords:
- <bypasslist>, remove element
- remove element, bypasslist
- bypasslist, remove element
- remove element, bypasslist
ms.assetid: 61dcfb4a-e3d9-4abf-a2cd-7d685fe2f64b
ms.openlocfilehash: a04cca3e57af5cc422776c5b2444a140e86f98b9
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61674465"
---
# <a name="remove-element-for-bypasslist-network-settings"></a>\<Supprimer >, élément de bypasslist (paramètres réseau)

Supprime une adresse IP ou le nom DNS de la liste de contournement proxy.

\<configuration>\
\<system.net>\
\<defaultProxy>\
\<BypassList > \
\<remove>

## <a name="syntax"></a>Syntaxe

```xml
<remove
  address="regular expression"
/>
```

## <a name="attributes-and-elements"></a>Attributs et éléments

Les sections suivantes décrivent des attributs, des éléments enfants et des éléments parents.

### <a name="attributes"></a>Attributs

|**Attribut**|**Description**|
|-------------------|---------------------|
|`address`|Une expression régulière décrivant une adresse IP ou un nom DNS.|

### <a name="child-elements"></a>Éléments enfants

Aucun.

### <a name="parent-elements"></a>Éléments parents

|**Élément**|**Description**|
|-----------------|---------------------|
|[bypasslist](../../../../../docs/framework/configure-apps/file-schema/network/bypasslist-element-network-settings.md)|Fournit un ensemble d’expressions régulières décrivant les adresses qui n’utilisent pas un proxy.|

## <a name="remarks"></a>Notes

Le `remove` élément supprime des expressions régulières décrivant les adresses IP ou des noms de serveur DNS dans la liste des adresses qui contournent un serveur proxy. Les adresses ont été définis précédemment dans le fichier de configuration ou à un niveau supérieur dans la hiérarchie de configuration.

La valeur de la `address` attribut doit être une expression régulière qui décrit un ensemble d’adresses IP ou noms d’hôte.

Pour plus d’informations sur les expressions régulières, consultez. [Expressions régulières .NET framework](../../../../../docs/standard/base-types/regular-expressions.md).

## <a name="configuration-files"></a>Fichiers de configuration

Cet élément peut être défini dans le fichier de configuration de l'application ou dans le fichier de configuration de l'ordinateur (Machine.config).

## <a name="example"></a>Exemple

L’exemple suivant supprime toute définition précédente pour le domaine adventure-works.com, puis ajoute le domaine contoso.com à la liste de contournement.

```xml
<configuration>
  <system.net>
    <defaultProxy>
      <bypasslist>
        <remove address="[a-z]+\.adventure-works\.com$" />
        <add address="[a-z]+\.contoso\.com$" />
      </bypasslist>
    </defaultProxy>
  </system.net>
</configuration>
```

## <a name="see-also"></a>Voir aussi

- <xref:System.Net.WebProxy?displayProperty=nameWithType>
- [Schéma des paramètres réseau](../../../../../docs/framework/configure-apps/file-schema/network/index.md)
