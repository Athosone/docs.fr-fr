---
title: Conception de classes statiques
ms.date: 10/22/2008
ms.technology: dotnet-standard
helpviewer_keywords:
- type design guidelines, static classes
- class library design guidelines [.NET Framework], classes
- classes [.NET Framework], static
- static classes [.NET Framework]
- classes [.NET Framework], design guidelines
- type design guidelines, classes
ms.assetid: d67c14d8-c4dd-443f-affb-4ccae677c9b6
author: KrzysztofCwalina
ms.openlocfilehash: d0a2f11b53f50f2ec2f301f7b88df65e1cd7b811
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61762044"
---
# <a name="static-class-design"></a>Conception de classes statiques
Une classe statique est définie comme une classe qui contient uniquement des membres statiques (bien entendu, outre les membres d’instance hérités de <xref:System.Object?displayProperty=nameWithType> et éventuellement un constructeur privé). Certains langages fournissent la prise en charge intégrée pour les classes static. Dans c# 2.0 et versions ultérieures, quand une classe est déclarée comme statique, il est scellé, abstract, et aucun membre d’instance peut être remplacée ou déclaré.  
  
 Les classes statiques sont un compromis entre la conception orientée objet et la simplicité. Ils sont couramment utilisés pour fournir des raccourcis vers les autres opérations (telles que <xref:System.IO.File?displayProperty=nameWithType>), les détenteurs de méthodes d’extension ou de fonctionnalités pour lequel un wrapper orienté objet est injustifié (tel que <xref:System.Environment?displayProperty=nameWithType>).  
  
 **✓ DO** utilisent des classes statiques avec parcimonie.  
  
 Classes static doivent être utilisées uniquement comme prenant en charge de classes pour la core orientée objet du framework.  
  
 **X DO NOT** traiter des classes statiques comme un compartiment divers.  
  
 **X DO NOT** déclarer ou substituer des membres d’instance dans les classes static.  
  
 **✓ DO** déclarer des classes statiques comme sealed, abstract, et ajoutez un constructeur d’instance privée si votre langage de programmation ne dispose pas de prise en charge intégrée pour les classes static.  
  
 *Portions © 2005, 2009 Microsoft Corporation. Tous droits réservés.*  
  
 *Réimprimé avec l’autorisation de Pearson éducation, Inc. à partir de [instructions de conception Framework : Conventions, les idiomes et les modèles pour les bibliothèques .NET réutilisable, 2nd Edition](https://www.informit.com/store/framework-design-guidelines-conventions-idioms-and-9780321545619) Krzysztof Cwalina et Brad Abrams, publié le 22 octobre 2008 par Addison-Wesley Professional dans le cadre de la série de développement de Microsoft Windows.*  
  
## <a name="see-also"></a>Voir aussi

- [Instructions pour la conception des types](../../../docs/standard/design-guidelines/type.md)
- [Règles de conception de .NET Framework](../../../docs/standard/design-guidelines/index.md)
