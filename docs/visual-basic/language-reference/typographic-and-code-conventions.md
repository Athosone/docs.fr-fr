---
title: Conventions typographiques (Visual Basic)
ms.date: 07/20/2015
helpviewer_keywords:
- coding conventions [Visual Basic], Visual Basic
- best practices [Visual Basic], coding conventions
- conventions [Visual Basic], Visual Basic coding
- typographic conventions [Visual Basic]
- document conventions [Visual Basic]
- conventions [Visual Basic], documentation
- Visual Basic code, conventions
ms.assetid: 1916cd81-ea9d-4faa-81f7-4a0d864b60f4
ms.openlocfilehash: 3255dff8268cd5500a1244716f37bf30f5b43cfb
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61698601"
---
# <a name="typographic-and-code-conventions-visual-basic"></a>Conventions typographiques (Visual Basic)
Documentation de Visual Basic utilise les conventions de code et le suit typographiques.  
  
## <a name="typographic-conventions"></a>Conventions typographiques  
  
|Exemple|Description|  
|-------------|-----------------|  
|`Sub`, `If`, `ChDir`, `Print`, `True`, `Debug`|Mots clés spécifiques au langage et les membres du runtime ont des lettres majuscules initiales et sont mis en forme comme illustré dans cet exemple.|  
|**SmallProject**, **ButtonCollection**|Mots et expressions que vous êtes invité à taper sont mis en forme comme illustré dans cet exemple.|  
|[Module (instruction)](../../visual-basic/language-reference/statements/module-statement.md)|Vous pouvez cliquer pour accéder à une autre page d’aide de liens sont formatés comme indiqué dans cet exemple.|  
|*object*, *variableName*, `argumentList`|Des espaces réservés pour les informations que vous fournissez sont formatés comme indiqué dans cet exemple.|  
|[Ombres], [ *expressionList* ]|Dans la syntaxe, les éléments facultatifs sont placés entre crochets.|  
|{ `Public` &#124; `Friend` &#124; `Private` }|Dans la syntaxe, lorsque vous devez faire un choix entre deux éléments ou plus, les éléments sont placés entre accolades et séparés par des barres verticales.<br /><br /> Vous devez sélectionner un et un seul des éléments.|  
|[ `Protected` &#124; `Friend` ]|Dans la syntaxe, lorsque vous avez la possibilité de choisir entre deux éléments ou plus, les éléments sont placés entre crochets et séparés par des barres verticales.<br /><br /> Vous pouvez sélectionner n’importe quelle combinaison des éléments ou aucun élément.|  
|[{ `ByVal` &#124; `ByRef` }]|Dans la syntaxe, lorsque vous sélectionnez pas plus d’un élément, mais vous pouvez également omettre les éléments complètement, les éléments placés entre crochets carré entouré d’accolades et séparés par des barres verticales.|  
|*memberName*1, *memberName*2, *memberName*3|Plusieurs instances du même espace réservé sont différenciées par les indices, comme indiqué dans l’exemple.|  
|*memberName1*<br /><br /> ...<br /><br /> *memberNameN*|Dans la syntaxe, les points de suspension (...) est utilisé pour indiquer un nombre indéfini d’éléments du genre immédiatement devant les points de suspension.<br /><br /> Dans le code, points de suspension représentent le code omis par souci de clarté.|  
|ÉCHAP, ENTREZ|Les noms de clés et les séquences de touches du clavier apparaissent dans toutes les lettres majuscules.|  
|ALT + F1|Signes plus (+) qui s’affichent entre les noms de clé, vous devez maintenir une touche enfoncée tout en appuyant sur l’autre. Par exemple, ALT + F1 signifie maintenez la touche ALT enfoncée tout en appuyant sur la touche F1.|  
  
## <a name="code-conventions"></a>Conventions de code  
  
|Exemple|Description|  
|-------------|-----------------|  
|`sampleString = "Hello, world!"`|Exemples de code apparaissent dans une police à espacement fixe et sont mis en forme comme illustré dans cet exemple.|  
|L’instruction précédente définit la valeur de `sampleString` à « Hello, world ! »|Éléments de code dans un texte explicatif apparaissent dans une police à espacement fixe, comme illustré dans cet exemple.|  
|`' This is a comment.`<br /><br /> `REM This is also a comment.`|Commentaires de code sont introduites par une apostrophe (') ou le mot clé REM.|  
|`sampleVar = "This is an " _`<br /><br /> `& "example" _`<br /><br /> `& " of how to continue code."`|Un espace suivi par un trait de soulignement (_) à la fin d’une ligne indique que l’instruction continue sur la ligne suivante.|  
  
## <a name="see-also"></a>Voir aussi

- [Informations de référence sur le langage Visual Basic](../../visual-basic/language-reference/index.md)
- [Mots clés](../../visual-basic/language-reference/keywords/index.md)
- [Membres de la bibliothèque runtime Visual Basic](../../visual-basic/language-reference/runtime-library-members.md)
- [Conventions d’affectation de noms de Visual Basic](../../visual-basic/programming-guide/program-structure/naming-conventions.md)
- [Guide pratique pour diviser et combiner des instructions dans le code](../../visual-basic/programming-guide/program-structure/how-to-break-and-combine-statements-in-code.md)
- [Commentaires dans le code](../../visual-basic/programming-guide/program-structure/comments-in-code.md)
