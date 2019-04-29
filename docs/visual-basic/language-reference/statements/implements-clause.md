---
title: Implements, clause (Visual Basic)
ms.date: 07/20/2015
f1_keywords:
- vb.ImplementsClause
helpviewer_keywords:
- interface implementation [Visual Basic], reimplementation
- interface members [Visual Basic], reimplementation
- interface members [Visual Basic], Implements keyword
- interface members
- members [Visual Basic], reimplementation
- interface implementation [Visual Basic], Implements keyword
- interface members [Visual Basic], implementing
- Implements keyword [Visual Basic]
- Implements statement [Visual Basic], about Implements
- members [Visual Basic], implementing
- members [Visual Basic], Implements keyword
- reimplementation
ms.assetid: 5252cdf9-964d-4fc6-af0f-0449b7126b5a
ms.openlocfilehash: 05de1d9f8966c17d84deba34f27819cce4aff3fe
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61637762"
---
# <a name="implements-clause-visual-basic"></a>Implements, clause (Visual Basic)
Indique qu’un membre de classe ou structure fournit l’implémentation d’un membre défini dans une interface.  
  
## <a name="remarks"></a>Notes  
Le `Implements` mot clé n’est pas le même que le [Implements, instruction](../../../visual-basic/language-reference/statements/implements-statement.md). Vous utilisez le `Implements` instruction pour spécifier qu’une classe ou structure implémente une ou plusieurs interfaces, et ensuite pour chaque membre que vous utilisez le `Implements` mot clé pour spécifier quelle interface et le membre qu’il implémente.

Si une classe ou structure implémente une interface, elle doit inclure le `Implements` instruction immédiatement après le [Class, instruction](../../../visual-basic/language-reference/statements/class-statement.md) ou [Structure (instruction)](../../../visual-basic/language-reference/statements/structure-statement.md), et il doit implémenter tous les membres définies par l’interface.

## <a name="reimplementation"></a>Nouvelle implémentation  
Dans une classe dérivée, vous pouvez implémenter de nouveau un membre d’interface que la classe de base a déjà implémenté. Cela est différent de substituer le membre de classe de base selon les critères suivants :

- Le membre de classe de base n’a pas besoin être [Overridable](../../../visual-basic/language-reference/modifiers/overridable.md) à être implémentées de nouveau.
- Vous pouvez implémenter de nouveau le membre avec un nom différent.

Le `Implements` mot clé peut être utilisé dans les contextes suivants :
- [Event (instruction)](../../../visual-basic/language-reference/statements/event-statement.md)
- [Function (instruction)](../../../visual-basic/language-reference/statements/function-statement.md)
- [Property (instruction)](../../../visual-basic/language-reference/statements/property-statement.md)
- [Sub (instruction)](../../../visual-basic/language-reference/statements/sub-statement.md)  
  
## <a name="see-also"></a>Voir aussi

- [Implements (instruction)](../../../visual-basic/language-reference/statements/implements-statement.md)
- [Interface (instruction)](../../../visual-basic/language-reference/statements/interface-statement.md)
- [Class (instruction)](../../../visual-basic/language-reference/statements/class-statement.md)
- [Structure (instruction)](../../../visual-basic/language-reference/statements/structure-statement.md)
