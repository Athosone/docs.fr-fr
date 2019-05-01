---
title: Types d'erreurs (Visual Basic)
ms.date: 07/20/2015
helpviewer_keywords:
- exceptions, types
- errors [Visual Basic], types
- errors [Visual Basic], logic
- errors [Visual Basic], syntax
- logic errors [Visual Basic], Visual Basic
- run-time errors [Visual Basic], types of errors
- syntax errors [Visual Basic], Visual Basic
ms.assetid: 3048aabf-8c97-4e13-9150-853769cb5f6f
ms.openlocfilehash: 07db963ac3cf9d1c0d17c420480189d362cdaf2c
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61973171"
---
# <a name="error-types-visual-basic"></a>Types d'erreurs (Visual Basic)
En Visual Basic, les erreurs (également appelé *exceptions*) se répartissent en trois catégories : erreurs de syntaxe, les erreurs d’exécution et les erreurs de logique.  
  
## <a name="syntax-errors"></a>Erreurs de syntaxe  
 *Erreurs de syntaxe* sont celles qui s’affichent lorsque vous écrivez du code. Visual Basic vérifie votre code en cours de frappe dans le **éditeur de Code** fenêtre et vous avertit si vous commettez une erreur, comme un mot mal orthographié ou l’utilisation incorrecte d’un élément de langage. Erreurs de syntaxe sont le type le plus courant d’erreurs. Vous pouvez les résoudre facilement dans l’environnement de codage dès qu’elles se produisent.  
  
> [!NOTE]
>  La `Option Explicit` instruction est d’éviter les erreurs de syntaxe. Il vous oblige à déclarer à l’avance, toutes les variables à utiliser dans l’application. Par conséquent, lorsque ces variables sont utilisées dans le code, les erreurs typographiques sont interceptées immédiatement et peuvent être résolus.  
  
## <a name="run-time-errors"></a>Erreurs d’exécution  
 *Erreurs d’exécution* sont celles qui apparaissent uniquement une fois que vous compilez et exécutez votre code. Elles peuvent donner lieu code semble correct dans la mesure où il n’a aucune erreur de syntaxe, mais qui ne s’exécutera pas. Par exemple, vous pouvez écrire correctement une ligne de code pour ouvrir un fichier. Mais si le fichier est endommagé, l’application ne peut pas exécuter le `Open` (fonction) et il cesse de s’exécuter. Vous pouvez résoudre la plupart des erreurs d’exécution en réécrivant le code erroné, puis recompiler et exécuter à nouveau.  
  
## <a name="logic-errors"></a>Erreurs de logique  
 *Erreurs de logique* sont celles qui apparaissent lorsque l’application est en cours d’utilisation. Ils sont la plupart des résultats souvent indésirables ou inattendues en réponse aux actions de l’utilisateur. Par exemple, une mauvaise touche ou influence extérieure peut-être vous aider à conduire votre application à cesser de fonctionner dans les paramètres prévus ou complètement. Erreurs de logique sont les plus difficiles à résoudre, car il n’est pas toujours évident de déterminer leur origine.  
  
## <a name="see-also"></a>Voir aussi

- [Try...Catch...Finally (instruction)](../../../visual-basic/language-reference/statements/try-catch-finally-statement.md)
- [Principes de base du débogueur](/visualstudio/debugger/debugger-basics)
