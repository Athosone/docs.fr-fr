---
title: Opérateur IsTrue (Visual Basic)
ms.date: 07/20/2015
f1_keywords:
- vb.istrue
helpviewer_keywords:
- IsTrue operator [Visual Basic]
- OrElse operator [Visual Basic]
ms.assetid: b6cec0f2-61b1-4331-a7f0-4d07ee3179d6
ms.openlocfilehash: 6c5ec6d953d174b525dee7ad3034d2d01ae4950f
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59344947"
---
# <a name="istrue-operator-visual-basic"></a>Opérateur IsTrue (Visual Basic)
Détermine si une expression est `True`.  
  
 Vous ne pouvez pas appeler `IsTrue` explicitement dans votre code, mais le Visual Basic compilateur peut l’utiliser pour générer le code à partir de `OrElse` clauses. Si vous définissez une classe ou une structure et ensuite utiliser une variable de ce type dans un `OrElse` clause, vous devez définir `IsTrue` sur cette classe ou structure.  
  
 Le compilateur considère les `IsTrue` et `IsFalse` opérateurs comme un *mis en correspondance de paire*. Cela signifie que si vous définissez un d’eux, vous devez également définir le.  
  
## <a name="compiler-use-of-istrue"></a>Utilisation du compilateur de IsTrue  
 Lorsque vous avez défini une classe ou structure, vous pouvez utiliser une variable de ce type dans un `For`, `If`, `Else If`, ou `While` instruction, ou dans un `When` clause. Si vous procédez ainsi, le compilateur requiert un opérateur qui convertit votre type en un `Boolean` valeur de façon à pouvoir tester une condition. Il recherche un opérateur adéquat dans l’ordre suivant :  
  
1. Un opérateur de conversion étendue de votre classe ou structure à `Boolean`.  
  
2. Un opérateur de conversion étendue de votre classe ou structure à `Boolean?`.  
  
3. Le `IsTrue` opérateur sur votre classe ou structure.  
  
4. Une conversion restrictive en `Boolean?` qui n’implique pas de conversion de `Boolean` à `Boolean?`.  
  
5. Un opérateur de conversion restrictive de votre classe ou structure à `Boolean`.  
  
 Si vous n’avez pas défini de conversion en `Boolean` ou un `IsTrue` opérateur, le compilateur signale une erreur.  
  
> [!NOTE]
>  Le `IsTrue` opérateur peut être *surchargé*, ce qui signifie qu’une classe ou structure peut redéfinir son comportement lorsque son opérande a le type de cette classe ou structure. Si votre code utilise cet opérateur sur une telle classe ou structure, veillez à ce que vous comprenez son comportement redéfini. Pour plus d'informations, consultez [Operator Procedures](../../../visual-basic/programming-guide/language-features/procedures/operator-procedures.md).  
  
## <a name="example"></a>Exemple  
 L’exemple de code suivant définit le contour d’une structure qui contient les définitions pour le `IsFalse` et `IsTrue` opérateurs.  
  
 [!code-vb[VbVbalrOperators#28](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbalrOperators/VB/Class1.vb#28)]  
  
## <a name="see-also"></a>Voir aussi

- [IsFalse (opérateur)](../../../visual-basic/language-reference/operators/isfalse-operator.md)
- [Guide pratique pour Définir un opérateur](../../../visual-basic/programming-guide/language-features/procedures/how-to-define-an-operator.md)
- [OrElse (opérateur)](../../../visual-basic/language-reference/operators/orelse-operator.md)
