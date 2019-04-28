---
title: Expressions booléennes (Visual Basic)
ms.date: 07/20/2015
helpviewer_keywords:
- short-circuiting
- Boolean expressions
- logical operators [Visual Basic], Boolean expressions
- expressions [Visual Basic], Boolean
- expression evaluation [Visual Basic], Boolean expressions
- operators [Visual Basic], short-circuiting
- Visual Basic code, operators
- short-circuit evaluation
- logical operators [Visual Basic], short-circuiting
- operators [Visual Basic], Boolean
- Visual Basic code, expressions
ms.assetid: d3d90406-55c8-4404-8143-50fd7f0d0d1a
ms.openlocfilehash: ce9146791935a488108d110134e9273507b0da6f
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61864664"
---
# <a name="boolean-expressions-visual-basic"></a>Expressions booléennes (Visual Basic)
Un *expression booléenne* est une expression qui prend une valeur de la [Type de données booléen](../../../../visual-basic/language-reference/data-types/boolean-data-type.md): `True` ou `False`. `Boolean` expressions peuvent prendre plusieurs formes. La plus simple est la comparaison directe de la valeur d’un `Boolean` variable à un `Boolean` littéral, comme indiqué dans l’exemple suivant.  
  
 [!code-vb[VbVbalrOperators#87](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbalrOperators/VB/Class1.vb#87)]  
  
## <a name="two-meanings-of-the--operator"></a>Deux significations de l’opérateur =  
 Notez que l’instruction d’assignation `newCustomer = True` ressemble à l’expression dans l’exemple précédent, mais elle effectue une fonction différente et est utilisée différemment. Dans l’exemple précédent, l’expression `newCustomer = True` représente une valeur booléenne et le `=` signe est interprété comme un opérateur de comparaison. Dans une instruction autonome, le `=` signe est interprété comme un opérateur d’assignation et assigne la valeur de droite à la variable sur la gauche. L'exemple suivant illustre ce comportement.  
  
 [!code-vb[VbVbalrOperators#88](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbalrOperators/VB/Class1.vb#88)]  
  
 Pour plus d’informations, consultez [les comparaisons de valeurs](../../../../visual-basic/programming-guide/language-features/operators-and-expressions/value-comparisons.md) et [instructions](../../../../visual-basic/language-reference/statements/index.md).  
  
## <a name="comparison-operators"></a>Opérateurs de comparaison  
 Opérateurs de comparaison tels que `=`, `<`, `>`, `<>`, `<=`, et `>=` produire des expressions booléennes en comparant l’expression sur le côté gauche de l’opérateur à l’expression située à droite de l’opérateur et l’évaluation du résultat en tant que `True` ou `False`. L'exemple suivant illustre ce comportement.  
  
 `42 < 81`  
  
 Étant donné que 42 est inférieur à 81, l’expression booléenne dans l’exemple précédent prend la valeur `True`. Pour plus d’informations sur ce type d’expression, consultez [les comparaisons de valeurs](../../../../visual-basic/programming-guide/language-features/operators-and-expressions/value-comparisons.md).  
  
### <a name="comparison-operators-combined-with-logical-operators"></a>Opérateurs de comparaison combinées avec des opérateurs logiques  
 Expressions de comparaison peuvent être combinées à l’aide des opérateurs logiques pour produire des expressions booléennes plus complexes. L’exemple suivant illustre l’utilisation d’opérateurs de comparaison conjointement avec un opérateur logique.  
  
 `x > y And x < 1000`  
  
 Dans l’exemple précédent, la valeur de l’expression globale dépend des valeurs des expressions de chaque côté de la `And` opérateur. Si les deux expressions sont `True`, l’expression globale a la valeur `True`. Si des expressions sont `False`, l’expression entière a la valeur `False`.  
  
## <a name="short-circuiting-operators"></a>Opérateurs de court-circuit  
 Les opérateurs logiques `AndAlso` et `OrElse` se comportent comme *court-circuit*. Un opérateur de court-circuit évalue d’abord l’opérande de gauche. Si l’opérande gauche détermine la valeur de l’expression entière, l’exécution du programme se poursuit sans évaluer l’expression de droite. L'exemple suivant illustre ce comportement.  
  
 [!code-vb[VbVbalrOperators#89](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbalrOperators/VB/Class1.vb#89)]  
  
 Dans l’exemple précédent, l’opérateur évalue l’expression de gauche, `45 < 12`. Étant donné que l’expression de gauche a la valeur `False`, toute l’expression doit correspondre à `False`. L’exécution du programme ignore ainsi l’exécution du code dans le `If` bloc sans évaluer l’expression de droite, `testFunction(3)`. Cet exemple n’appelle pas `testFunction()` , car l’expression de gauche falsifie l’expression entière.  
  
 De même, si l’expression de gauche dans une expression logique à l’aide `OrElse` prend la valeur `True`, l’exécution se poursuit à la ligne suivante de code sans évaluer l’expression de droite, car l’expression de gauche a déjà validé l’ensemble expression.  
  
### <a name="comparison-with-non-short-circuiting-operators"></a>Comparaison avec des opérateurs Non pas de court-circuit  
 En revanche, les deux côtés de l’opérateur logique sont évalués lorsque les opérateurs logiques `And` et `Or` sont utilisés. L'exemple suivant illustre ce comportement.  
  
 [!code-vb[VbVbalrOperators#90](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbalrOperators/VB/Class1.vb#90)]  
  
 L’exemple précédent appelle `testFunction()` même si l’expression de gauche a la valeur `False`.  
  
## <a name="parenthetical-expressions"></a>Expressions entre parenthèses  
 Vous pouvez utiliser des parenthèses pour contrôler l’ordre d’évaluation d’expressions booléennes. Tout d’abord évaluent les expressions entourées parenthèses. Pour plusieurs niveaux d’imbrication, la priorité est accordée aux expressions plus profondément imbriquées. Dans les parenthèses, l’évaluation se poursuit selon les règles de priorité des opérateurs. Pour plus d’informations, consultez [priorité des opérateurs en Visual Basic](../../../../visual-basic/language-reference/operators/operator-precedence.md).  
  
## <a name="see-also"></a>Voir aussi

- [Opérateurs logiques et au niveau du bit en Visual Basic](../../../../visual-basic/programming-guide/language-features/operators-and-expressions/logical-and-bitwise-operators.md)
- [Comparaisons de valeurs](../../../../visual-basic/programming-guide/language-features/operators-and-expressions/value-comparisons.md)
- [Instructions](../../../../visual-basic/programming-guide/language-features/statements.md)
- [Opérateurs de comparaison](../../../../visual-basic/language-reference/operators/comparison-operators.md)
- [Association efficace d’opérateurs](../../../../visual-basic/programming-guide/language-features/operators-and-expressions/efficient-combination-of-operators.md)
- [Priorité des opérateurs en Visual Basic](../../../../visual-basic/language-reference/operators/operator-precedence.md)
- [Booléen (type de données)](../../../../visual-basic/language-reference/data-types/boolean-data-type.md)
