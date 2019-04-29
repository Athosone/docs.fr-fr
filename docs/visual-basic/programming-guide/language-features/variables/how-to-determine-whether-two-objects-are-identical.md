---
title: 'Procédure : Déterminer si deux objets sont identiques (Visual Basic)'
ms.date: 07/20/2015
helpviewer_keywords:
- testing [Visual Basic], objects
- objects [Visual Basic], comparing
- object variables [Visual Basic], determining identity
ms.assetid: 7829f817-0d1f-4749-a707-de0b95e0cf5c
ms.openlocfilehash: aae053ae0473ed6ced0f28da3d5e5afc0be629df
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61769081"
---
# <a name="how-to-determine-whether-two-objects-are-identical-visual-basic"></a>Procédure : Déterminer si deux objets sont identiques (Visual Basic)
En Visual Basic, deux références de variable sont considérés comme identiques si leurs pointeurs sont les mêmes, autrement dit, si les deux variables pointent vers la même instance de classe en mémoire. Par exemple, dans une application Windows Forms, vous souhaiterez effectuer une comparaison pour déterminer si l’instance actuelle (`Me`) est identique à une instance particulière, tel que `Form2`.  
  
 Visual Basic fournit deux opérateurs pour comparer des pointeurs. Le [opérateur Is](../../../../visual-basic/language-reference/operators/is-operator.md) retourne `True` si les objets sont identiques et le [opérateur IsNot](../../../../visual-basic/language-reference/operators/isnot-operator.md) retourne `True` si elles ne sont pas.  
  
## <a name="determining-if-two-objects-are-identical"></a>Comment déterminer si deux objets sont identiques  
  
#### <a name="to-determine-if-two-objects-are-identical"></a>Pour déterminer si deux objets sont identiques  
  
1. Configurer un `Boolean` expression pour tester les deux objets.  
  
2. Dans votre expression de test, utilisez le `Is` opérateur avec les deux objets en tant qu’opérandes.  
  
     `Is` Retourne `True` si les objets pointent vers la même instance de classe.  
  
## <a name="determining-if-two-objects-are-not-identical"></a>Déterminer si deux objets ne sont pas identiques  
 Parfois, vous souhaitez effectuer une action si les deux objets ne sont pas identiques, et il peut être délicat de combiner `Not` et `Is`, par exemple `If Not obj1 Is obj2`. Dans ce cas, vous pouvez utiliser le `IsNot` opérateur.  
  
#### <a name="to-determine-if-two-objects-are-not-identical"></a>Pour déterminer si deux objets ne sont pas identiques  
  
1. Configurer un `Boolean` expression pour tester les deux objets.  
  
2. Dans votre expression de test, utilisez le `IsNot` opérateur avec les deux objets en tant qu’opérandes.  
  
     `IsNot` Retourne `True` si les objets ne pointent pas vers la même instance de classe.  
  
## <a name="example"></a>Exemple  
 L’exemple suivant teste des paires de `Object` variables pour voir si elles pointent vers la même instance de classe.  
  
 [!code-vb[VbVbalrKeywords#14](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbalrKeywords/VB/class7.vb#14)]  
  
 L’exemple précédent affiche la sortie suivante.  
  
 `objA different from objB? True`  
  
 `objA identical to objC? True`  
  
## <a name="see-also"></a>Voir aussi

- [Object (type de données)](../../../../visual-basic/language-reference/data-types/object-data-type.md)
- [Variables objets](../../../../visual-basic/programming-guide/language-features/variables/object-variables.md)
- [Valeurs des variables objets](../../../../visual-basic/programming-guide/language-features/variables/object-variable-values.md)
- [Is (opérateur)](../../../../visual-basic/language-reference/operators/is-operator.md)
- [IsNot (opérateur)](../../../../visual-basic/language-reference/operators/isnot-operator.md)
- [Guide pratique pour Déterminer si deux objets sont liés](../../../../visual-basic/programming-guide/language-features/variables/how-to-determine-whether-two-objects-are-related.md)
- [Me, My, MyBase et MyClass](../../../../visual-basic/programming-guide/program-structure/me-my-mybase-and-myclass.md)
