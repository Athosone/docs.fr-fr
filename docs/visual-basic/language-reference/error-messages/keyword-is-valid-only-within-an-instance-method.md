---
title: "'<keyword>' est valide uniquement dans une méthode d'instance"
ms.date: 07/20/2015
f1_keywords:
- bc30043
- vbc30043
helpviewer_keywords:
- BC30043
ms.assetid: 7973aa82-a681-440c-9bca-242627d7ba86
ms.openlocfilehash: 5ff82b932f9bea4c7fd087651e34277ef94bc27c
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61946638"
---
# <a name="keyword-is-valid-only-within-an-instance-method"></a>'\<mot clé >' est valide uniquement dans une méthode d’instance
Le `Me`, `MyClass`, et `MyBase` mots clés font référence aux instances de classe spécifique. Vous ne pouvez pas les utiliser à l’intérieur d’un partage `Function` ou `Sub` procédure.  
  
 **ID d’erreur :** BC30043  
  
## <a name="to-correct-this-error"></a>Pour corriger cette erreur  
  
- Supprimez le mot clé à partir de la procédure ou supprimez le `Shared` mot clé à partir de la déclaration de procédure.  
  
## <a name="see-also"></a>Voir aussi

- [Assignation des variables objets](../../../visual-basic/programming-guide/language-features/variables/object-variable-assignment.md)
- [Me, My, MyBase et MyClass](../../../visual-basic/programming-guide/program-structure/me-my-mybase-and-myclass.md)
- [Éléments fondamentaux de l’héritage](../../../visual-basic/programming-guide/language-features/objects-and-classes/inheritance-basics.md)
