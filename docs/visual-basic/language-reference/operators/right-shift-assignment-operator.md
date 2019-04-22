---
title: '>>=, opérateur (Visual Basic)'
ms.date: 07/20/2015
f1_keywords:
- vb.>>=
helpviewer_keywords:
- assignment statements [Visual Basic], compound
- statements [Visual Basic], compound assignment
- operator >>= [Visual Basic]
- compound assignment statements [Visual Basic]
- '>>= operator [Visual Basic]'
ms.assetid: 2bcd9abb-7a8c-4229-b75d-8816ff1dc700
ms.openlocfilehash: 1076ce62077391f2c88ebdd621d1dbd6fb40d647
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "58838961"
---
# <a name="-operator-visual-basic"></a>>> =, opérateur (Visual Basic)
Effectue un décalage arithmétique vers la droite sur la valeur d’une propriété ou une variable et assigne le résultat à la variable ou propriété.  
  
## <a name="syntax"></a>Syntaxe  
  
```  
variableorproperty >>= amount  
```  
  
## <a name="parts"></a>Composants  
 `variableorproperty`  
 Obligatoire. Variable ou propriété d’un type intégral (`SByte`, `Byte`, `Short`, `UShort`, `Integer`, `UInteger`, `Long`, ou `ULong`).  
  
 `amount`  
 Obligatoire. Expression numérique d’un type de données qui s’étend à `Integer`.  
  
## <a name="remarks"></a>Notes  
 L’élément sur le côté gauche de la `>>=` opérateur peut être une simple variable scalaire, une propriété ou un élément d’un tableau. La variable ou la propriété ne peut pas être [ReadOnly](../../../visual-basic/language-reference/modifiers/readonly.md).  
  
 Le `>>=` opérateur effectue d’abord un décalage arithmétique vers la droite de la valeur de la variable ou propriété. Puis, l’opérateur assigne le résultat de cette opération à la variable ou propriété.  
  
 Les décalages arithmétiques ne sont pas circulaires, ce qui signifie que les bits décalés à une extrémité du résultat ne sont pas réintroduits à l’autre extrémité. Dans un décalage arithmétique à droite, les bits décalés au-delà de la position de bit plus à droite sont supprimés, et le bit le plus à gauche est propagé dans les positions de bit libérées à gauche. Cela signifie que si `variableorproperty` a une valeur négative, les positions libérées sont définies sur un. Si `variableorproperty` est positif, ou si son type de données est un type non signé, les positions libérées sont définies à zéro.  
  
## <a name="overloading"></a>Surcharge  
 Le [>> opérateur](../../../visual-basic/language-reference/operators/right-shift-operator.md) peut être *surchargé*, ce qui signifie qu’une classe ou structure peut redéfinir son comportement lorsqu’un opérande a le type de cette classe ou structure. La surcharge la `>>` opérateur affecte le comportement de la `>>=` opérateur. Si votre code utilise `>>=` sur une classe ou structure qui surcharge `>>`, assurez-vous que vous comprenez son comportement redéfini. Pour plus d'informations, consultez [Operator Procedures](../../../visual-basic/programming-guide/language-features/procedures/operator-procedures.md).  
  
## <a name="example"></a>Exemple  
 L’exemple suivant utilise le `>>=` opérateur pour décaler le modèle binaire d’une `Integer` variable directement par la quantité spécifiée et assigner le résultat à la variable.  
  
 [!code-vb[VbVbalrOperators#15](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbalrOperators/VB/Class1.vb#15)]  
  
## <a name="see-also"></a>Voir aussi

- [>> (opérateur)](../../../visual-basic/language-reference/operators/right-shift-operator.md)
- [Opérateurs d’assignation](../../../visual-basic/language-reference/operators/assignment-operators.md)
- [Opérateurs de décalage de bits](../../../visual-basic/language-reference/operators/bit-shift-operators.md)
- [Priorité des opérateurs en Visual Basic](../../../visual-basic/language-reference/operators/operator-precedence.md)
- [Opérateurs répertoriés par fonctionnalité](../../../visual-basic/language-reference/operators/operators-listed-by-functionality.md)
- [Instructions](../../../visual-basic/programming-guide/language-features/statements.md)
