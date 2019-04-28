---
title: L'espace de noms ou le type spécifié dans les Imports '<qualifiedelementname>' au niveau du projet ne contient aucun membre public ou est introuvable
ms.date: 07/20/2015
f1_keywords:
- vbc40057
- bc40057
helpviewer_keywords:
- BC40057
ms.assetid: 4ae3506e-2ebe-4ff3-995d-14ac60db5e9f
ms.openlocfilehash: 105fa8da838938d13022c210c1f65cdafd251003
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61918305"
---
# <a name="namespace-or-type-specified-in-the-project-level-imports-qualifiedelementname-doesnt-contain-any-public-member-or-cannot-be-found"></a>Namespace ou type spécifié dans les Imports' au niveau du projet\<nom_qualifié_élément >' ne contient aucun membre public ou est introuvable
Namespace ou type spécifié dans les Imports' au niveau du projet\<nom_qualifié_élément >' ne contient aucun membre public ou est introuvable. Assurez-vous que l’espace de noms ou le type est défini et contient au moins un membre public. Assurez-vous que le nom d’alias ne contient pas d’autres alias.  
  
 Une propriété de l’importation d’un projet spécifie un élément conteneur qui ne peut pas être trouvé ou ne définit pas `Public` membres.  
  
 Un *contenant l’élément* peut être un espace de noms, une classe, une structure, un module, une interface ou une énumération. L’élément conteneur contient des membres, tels que des variables, procédures ou d’autres éléments qui le contient.  
  
 L’objectif de l’importation consiste à autoriser votre code pour accéder aux membres de type ou espace de noms sans devoir les qualifier. Votre projet devrez peut-être également ajouter une référence à l’espace de noms ou type. Pour plus d’informations, consultez « Importation d’éléments conteneurs » dans [References to Declared Elements](../../../visual-basic/programming-guide/language-features/declared-elements/references-to-declared-elements.md).  
  
 Si le compilateur ne peut pas trouver l’élément conteneur spécifié, il ne peut pas résoudre les références qui l’utilisent. Si elle recherche l’élément, mais l’élément n’expose pas `Public` membres, aucune référence peut être réussie. Dans les deux cas, il est sans signification pour importer l’élément.  
  
 Vous utilisez le **Concepteur de projet** pour spécifier les éléments à importer. Utilisez le **espaces de noms importés** section de la **références** page. Vous pouvez accéder à la **Concepteur de projets** en double-cliquant sur le **mon projet** icône dans **l’Explorateur de solutions**.  
  
 **ID d’erreur :** BC40057  
  
## <a name="to-correct-this-error"></a>Pour corriger cette erreur  
  
1. Ouvrez le **Concepteur de projets** et basculez vers le **référence** page.  
  
2. Dans le **espaces de noms importés** section, vérifiez que l’élément conteneur est accessible à partir de votre projet.  
  
3. Vérifiez que l’élément conteneur expose au moins un `Public` membre.  
  
## <a name="see-also"></a>Voir aussi

- [Page Références, Concepteur de projets (Visual Basic)](/visualstudio/ide/reference/references-page-project-designer-visual-basic)
- [Gestion des propriétés des projets et des solutions](/visualstudio/ide/managing-project-and-solution-properties)
- [Public](../../../visual-basic/language-reference/modifiers/public.md)
- [Espaces de noms dans Visual Basic](../../../visual-basic/programming-guide/program-structure/namespaces.md)
- [Références aux éléments déclarés](../../../visual-basic/programming-guide/language-features/declared-elements/references-to-declared-elements.md)
