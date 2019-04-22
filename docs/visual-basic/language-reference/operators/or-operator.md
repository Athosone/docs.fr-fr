---
title: Or, opérateur (Visual Basic)
ms.date: 07/20/2015
f1_keywords:
- vb.Or
helpviewer_keywords:
- Or operator [Visual Basic]
- operators [Visual Basic], bitwise
- inclusive Or operator [Visual Basic]
- bitwise operators [Visual Basic], OR operator
- Or keyword [Visual Basic]
- operators [Visual Basic], inclusive or
- operators [Visual Basic], disjunction
- bitwise comparison [Visual Basic]
- logical disjunction
- disjunction operator [Visual Basic]
ms.assetid: 41ed6905-bf3d-468a-9e3b-03c10d461891
ms.openlocfilehash: 0277b6f24e62ed5f0cad3dae225c86fffc4c09b9
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "58835295"
---
# <a name="or-operator-visual-basic"></a>Or, opérateur (Visual Basic)
Effectue une disjonction logique sur deux `Boolean` expressions ou une disjonction au niveau du bit sur deux expressions numériques.  
  
## <a name="syntax"></a>Syntaxe  
  
```  
result = expression1 Or expression2  
```  
  
## <a name="parts"></a>Composants  
 `result`  
 Obligatoire. N’importe quel `Boolean` ou expression numérique. Pour `Boolean` comparaison, `result` est la disjonction logique inclusive de deux `Boolean` valeurs. Pour les opérations au niveau du bit, `result` est une valeur numérique représentant la disjonction au niveau du bit inclusive de deux modèles binaires numériques.  
  
 `expression1`  
 Obligatoire. N’importe quel `Boolean` ou expression numérique.  
  
 `expression2`  
 Obligatoire. N’importe quel `Boolean` ou expression numérique.  
  
## <a name="remarks"></a>Notes  
 Pour `Boolean` comparaison, `result` est `False` si et seulement si `expression1` et `expression2` évaluer à `False`. Le tableau suivant illustre comment `result` est déterminée.  
  
|Si `expression1` est|Et `expression2` est|La valeur de `result` est|  
|-------------------------|--------------------------|------------------------------|  
|`True`|`True`|`True`|  
|`True`|`False`|`True`|  
|`False`|`True`|`True`|  
|`False`|`False`|`False`|  
  
> [!NOTE]
>  Dans un `Boolean` comparaison, le `Or` opérateur évalue toujours les deux expressions, ce qui peut inclure des appels de procédure. Le [OrElse Operator](../../../visual-basic/language-reference/operators/orelse-operator.md) effectue *court-circuit*, ce qui signifie que si `expression1` est `True`, puis `expression2` n’est pas évaluée.  
  
 Pour les opérations au niveau du bit, les `Or` opérateur effectue une comparaison au niveau du bit de position identique dans deux expressions numériques et définit le bit dans correspondant `result` conformément au tableau suivant.  
  
|Si de transmission en `expression1` est|Et que le bit dans `expression2` est|Le bit `result` est|  
|--------------------------------|---------------------------------|----------------------------|  
|1|1|1|  
|1|0|1|  
|0|1|1|  
|0|0|0|  
  
> [!NOTE]
>  Étant donné que les opérateurs logiques et au niveau du bit ont une priorité inférieure à celle des opérateurs arithmétiques et relationnels, toutes les opérations au niveau du bit doivent être mises entre parenthèses pour garantir une exécution précise.  
  
## <a name="data-types"></a>Types de données  
 Si les opérandes se composent d’une `Boolean` expression et une expression numérique, Visual Basic convertit le `Boolean` expression à une valeur numérique (-1 pour `True` et 0 pour `False`) et effectue une opération au niveau du bit.  
  
 Pour un `Boolean` comparaison, le type de données du résultat est `Boolean`. Pour obtenir une comparaison au niveau du bit, le type de données de résultat est un type numérique approprié pour les types de données de `expression1` et `expression2`. Consultez le tableau « Relationnelles et au niveau du bit des comparaisons » dans [Types de données de résultats de l’opérateur](../../../visual-basic/language-reference/operators/data-types-of-operator-results.md).  
  
## <a name="overloading"></a>Surcharge  
 Le `Or` opérateur peut être *surchargé*, ce qui signifie qu’une classe ou structure peut redéfinir son comportement lorsqu’un opérande a le type de cette classe ou structure. Si votre code utilise cet opérateur sur une telle classe ou structure, veillez à ce que vous comprenez son comportement redéfini. Pour plus d'informations, consultez [Operator Procedures](../../../visual-basic/programming-guide/language-features/procedures/operator-procedures.md).  
  
## <a name="example"></a>Exemple  
 L’exemple suivant utilise le `Or` opérateur effectue une disjonction logique inclusive sur deux expressions. Le résultat est un `Boolean` valeur qui représente si une des deux expressions est `True`.  
  
 [!code-vb[VbVbalrOperators#35](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbalrOperators/VB/Class1.vb#35)]  
  
 L’exemple précédent produit des résultats de `True`, `True`, et `False`, respectivement.  
  
## <a name="example"></a>Exemple  
 L’exemple suivant utilise le `Or` opérateur effectue une disjonction logique inclusive sur les bits individuels de deux expressions numériques. Le bit du modèle de résultat est défini si un des bits correspondants dans les opérandes est défini sur 1.  
  
 [!code-vb[VbVbalrOperators#36](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbalrOperators/VB/Class1.vb#36)]  
  
 L’exemple précédent produit les résultats de 10, 14 et 14, respectivement.  
  
## <a name="see-also"></a>Voir aussi

- [Opérateurs logiques/de bits (Visual Basic)](../../../visual-basic/language-reference/operators/logical-bitwise-operators.md)
- [Priorité des opérateurs en Visual Basic](../../../visual-basic/language-reference/operators/operator-precedence.md)
- [Opérateurs répertoriés par fonctionnalité](../../../visual-basic/language-reference/operators/operators-listed-by-functionality.md)
- [OrElse (opérateur)](../../../visual-basic/language-reference/operators/orelse-operator.md)
- [Opérateurs logiques et au niveau du bit en Visual Basic](../../../visual-basic/programming-guide/language-features/operators-and-expressions/logical-and-bitwise-operators.md)
