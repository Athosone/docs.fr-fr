---
title: Une instruction 'Class' doit se terminer par une 'End Class' correspondante
ms.date: 07/20/2015
f1_keywords:
- vbc30481
- bc30481
helpviewer_keywords:
- BC30481
ms.assetid: 583f3029-bc3a-4e06-866f-92dbecc46f19
ms.openlocfilehash: 0619db618abd562bda86836bdd41bbcd6caee0f9
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "58836504"
---
# <a name="class-statement-must-end-with-a-matching-end-class"></a>Une instruction 'Class' doit se terminer par une 'End Class' correspondante
`Class` permet de lancer un `Class` bloquer ; il ne peut donc apparaître au début du bloc, avec une mise en correspondance `End Class` instruction fin du bloc. Soit vous avez un redondant `Class` instruction, ou vous n’avez pas terminé votre `Class` bloc avec `End Class`.  
  
 **ID d’erreur :** BC30481  
  
## <a name="to-correct-this-error"></a>Pour corriger cette erreur  
  
-   Recherchez et supprimez l’instruction `Class` inutile.  
  
-   Conclure le `Class` bloc avec une mise en correspondance `End Class`.  
  
## <a name="see-also"></a>Voir aussi

- [Fin \<mot clé > instruction](../../../visual-basic/language-reference/statements/end-keyword-statement.md)
- [Class (instruction)](../../../visual-basic/language-reference/statements/class-statement.md)
