---
title: Attributs
ms.date: 10/22/2008
ms.technology: dotnet-standard
helpviewer_keywords:
- attributes [.NET Framework], about
- class library design guidelines [.NET Framework], attributes
ms.assetid: ee0038ef-b247-4747-a650-3c5c5cd58d8b
author: KrzysztofCwalina
ms.openlocfilehash: 6d4cc6615b7f7346e9c8fc2a7264025f318c8a3d
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61785565"
---
# <a name="attributes"></a>Attributs
<xref:System.Attribute?displayProperty=nameWithType> une classe de base permet de définir des attributs personnalisés.  
  
 Les attributs sont des annotations qui peuvent être ajoutées aux éléments de programmation tels que les assemblys, types, membres et paramètres. Ils sont stockés dans les métadonnées de l’assembly et sont accessibles lors de l’exécution à l’aide de l’API de réflexion. Par exemple, le Framework définit le <xref:System.ObsoleteAttribute>, qui peut être appliqué à un type ou un membre pour indiquer que le type ou membre a été déconseillée.  
  
 Attributs peuvent avoir une ou plusieurs propriétés qui transmettent des données supplémentaires relatives à l’attribut. Par exemple, `ObsoleteAttribute` peut comporter des informations complémentaires sur la version dans lequel un type ou un membre a été déconseillé et la description des nouvelles API en remplaçant l’API obsolète.  
  
 Certaines propriétés d’un attribut doivent être spécifiées lorsque l’attribut est appliqué. Ceux-ci sont appelés les propriétés requises ou les arguments requis, car ils sont représentés en tant que paramètres de constructeur positionnel. Par exemple, le <xref:System.Diagnostics.ConditionalAttribute.ConditionString%2A> propriété de la <xref:System.Diagnostics.ConditionalAttribute> est une propriété obligatoire.  
  
 Les propriétés qui n’ont pas nécessairement être spécifié lorsque l’attribut est appliqué sont appelées propriétés facultatives (ou les arguments facultatifs). Ils sont représentés par les propriétés définissables. Les compilateurs fournissent une syntaxe spéciale pour définir ces propriétés lorsqu’un attribut est appliqué. Par exemple, le <xref:System.AttributeUsageAttribute.Inherited%2A?displayProperty=nameWithType> propriété représente un argument facultatif.  
  
 **✓ DO** nommez des classes d’attributs personnalisés avec le suffixe « Attribut ».  
  
 **✓ DO** appliquer le <xref:System.AttributeUsageAttribute> à des attributs personnalisés.  
  
 **✓ DO** fournir les propriétés définissables pour les arguments facultatifs.  
  
 **✓ DO** fournissent des propriétés get uniquement pour les arguments requis.  
  
 **✓ DO** fournissent des paramètres du constructeur pour initialiser les propriétés qui correspondent aux arguments requis. Chaque paramètre doit avoir le même nom (mais avec une casse différente) en tant que la propriété correspondante.  
  
 **X AVOID** fournissant les paramètres du constructeur pour initialiser les propriétés qui correspondent aux arguments facultatifs.  
  
 En d’autres termes, n’ont pas de propriétés qui peuvent être définies avec un constructeur et un accesseur Set. Cette recommandation rend très explicite les arguments sont facultatifs et qui sont nécessaire et évite d’avoir deux façons de faire la même chose.  
  
 **X AVOID** surcharge des constructeurs d’attribut personnalisé.  
  
 Avoir un seul constructeur communique clairement à l’utilisateur quels sont les arguments requis et facultatifs.  
  
 **✓ DO** sceller des classes d’attributs personnalisés, si possible. Cela accélère la recherche de l’attribut.  
  
 *Portions © 2005, 2009 Microsoft Corporation. Tous droits réservés.*  
  
 *Réimprimé avec l’autorisation de Pearson éducation, Inc. à partir de [instructions de conception Framework : Conventions, les idiomes et les modèles pour les bibliothèques .NET réutilisable, 2nd Edition](https://www.informit.com/store/framework-design-guidelines-conventions-idioms-and-9780321545619) Krzysztof Cwalina et Brad Abrams, publié le 22 octobre 2008 par Addison-Wesley Professional dans le cadre de la série de développement de Microsoft Windows.*  
  
## <a name="see-also"></a>Voir aussi

- [Règles de conception de .NET Framework](../../../docs/standard/design-guidelines/index.md)
- [Indications relatives à l’utilisation](../../../docs/standard/design-guidelines/usage-guidelines.md)
