---
title: Noms d'assemblys et de DLL
ms.date: 10/22/2008
ms.technology: dotnet-standard
helpviewer_keywords:
- names [.NET Framework], DLLs
- names [.NET Framework], assemblies
- assemblies [.NET Framework], names
- DLLs, names
ms.assetid: e800b610-31b4-4949-9c14-cb60e9f254be
author: KrzysztofCwalina
ms.openlocfilehash: 1aeef9e1be6e5fe747f440a8cb7f21095cb22f49
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61945494"
---
# <a name="names-of-assemblies-and-dlls"></a>Noms d'assemblys et de DLL
Un assembly est l’unité de déploiement et d’identité pour les programmes de code managé. Bien que les assemblys peuvent s’étendre sur un ou plusieurs fichiers, en général, un assembly effectue un mappage avec une DLL. Par conséquent, cette section décrit les conventions d’affectation de noms de seul DLL peuvent alors être mappées aux conventions d’affectation de noms d’assembly.  
  
 **✓ DO** choisissez des noms pour vos DLL d’assembly qui suggèrent des grands segments de fonctionnalités, telles que System.Data.  
  
 Noms d’assembly et les DLL n’êtes pas obligé de correspondent aux noms d’espace de noms, mais il est raisonnable de suivre le nom de l’espace de noms lorsque vous nommez des assemblys. Une règle empirique consiste à nommer la DLL basée sur le préfixe commun des espaces de noms contenus dans l’assembly. Par exemple, un assembly avec deux espaces de noms, `MyCompany.MyTechnology.FirstFeature` et `MyCompany.MyTechnology.SecondFeature`, peut être appelée `MyCompany.MyTechnology.dll`.  
  
 **✓ CONSIDER** nommer les DLL selon le modèle suivant :  
  
 `<Company>.<Component>.dll`  
  
 où `<Component>` contient une ou plusieurs clauses séparés par des points. Exemple :  
  
 `Litware.Controls.dll`.  
  
 *Portions © 2005, 2009 Microsoft Corporation. Tous droits réservés.*  
  
 *Réimprimé avec l’autorisation de Pearson éducation, Inc. à partir de [instructions de conception Framework : Conventions, les idiomes et les modèles pour les bibliothèques .NET réutilisable, 2nd Edition](https://www.informit.com/store/framework-design-guidelines-conventions-idioms-and-9780321545619) Krzysztof Cwalina et Brad Abrams, publié le 22 octobre 2008 par Addison-Wesley Professional dans le cadre de la série de développement de Microsoft Windows.*  
  
## <a name="see-also"></a>Voir aussi

- [Règles de conception de .NET Framework](../../../docs/standard/design-guidelines/index.md)
- [Directives de nommage](../../../docs/standard/design-guidelines/naming-guidelines.md)
