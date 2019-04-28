---
title: Fin d'instruction attendue
ms.date: 07/20/2015
f1_keywords:
- bc30205
- vbc30205
helpviewer_keywords:
- BC30205
ms.assetid: 53c7f825-a737-4b76-a1fa-f67745b8bd40
ms.openlocfilehash: 1ce5c793a09df34ac17e70e3253e98108bf76fb8
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61803317"
---
# <a name="end-of-statement-expected"></a>Fin d'instruction attendue
L’instruction est syntaxiquement complète, mais un élément de programmation supplémentaire suit l’élément qui termine l’instruction. Un terminateur de ligne est nécessaire à la fin de chaque instruction.
  
 Un terminateur de ligne divise les caractères d’un fichier source Visual Basic en lignes. Exemples d’indicateurs de fin de ligne sont le Unicode chariot retour (& HD), le Unicode saut de ligne (& haute disponibilité), et Unicode retour chariot suivi du caractère de saut de ligne Unicode. Pour plus d’informations sur les indicateurs de fin de ligne, consultez le [spécification du langage Visual Basic](~/_vblang/spec/lexical-grammar.md#line-terminators).
  
 **ID d’erreur :** BC30205
  
## <a name="to-correct-this-error"></a>Pour corriger cette erreur
  
1. Vérifiez si deux instructions différentes ont été placées par inadvertance sur la même ligne.
  
2. Insérer un terminateur de ligne après l’élément qui se termine l’instruction.
  
## <a name="see-also"></a>Voir aussi

- [Guide pratique pour diviser et combiner des instructions dans le code](../../../visual-basic/programming-guide/program-structure/how-to-break-and-combine-statements-in-code.md)
- [Instructions](../../../visual-basic/programming-guide/language-features/statements.md)
