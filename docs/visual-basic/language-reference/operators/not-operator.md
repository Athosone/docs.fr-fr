---
title: Not, opérateur (Visual Basic)
ms.date: 07/20/2015
f1_keywords:
- vb.Not
helpviewer_keywords:
- Boolean expressions, negating
- operators [Visual Basic], bitwise
- negation operator [Visual Basic]
- inverse bit values in variables [Visual Basic]
- bitwise operators [Visual Basic], NOT operator
- bitwise comparison [Visual Basic]
- Not operator [Visual Basic]
- logical negation
- operators [Visual Basic], negation
ms.assetid: 8f2ea83c-d2ed-480a-a474-3042a1cad9b5
ms.openlocfilehash: 4e54fdca9123ad5595eb9a8c5e2ac5bc303a8f6a
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "58824199"
---
# <a name="not-operator-visual-basic"></a>Not, opérateur (Visual Basic)
Effectue une négation logique sur une `Boolean` expression, ou une négation au niveau du bit sur une expression numérique.  
  
## <a name="syntax"></a>Syntaxe  
  
```  
result = Not expression  
```  
  
## <a name="parts"></a>Composants  
 `result`  
 Obligatoire. N’importe quel `Boolean` ou expression numérique.  
  
 `expression`  
 Obligatoire. N’importe quel `Boolean` ou expression numérique.  
  
## <a name="remarks"></a>Notes  
 Pour `Boolean` expressions, le tableau suivant illustre comment `result` est déterminée.  
  
|Si `expression` est|La valeur de `result` est|  
|------------------------|------------------------------|  
|`True`|`False`|  
|`False`|`True`|  
  
 Pour les expressions numériques, la `Not` opérateur inverse les valeurs de bits de toute expression numérique et définit le bit dans correspondant `result` conformément au tableau suivant.  
  
|Si de transmission en `expression` est|Le bit `result` est|  
|-------------------------------|----------------------------|  
|1|0|  
|0|1|  
  
> [!NOTE]
>  Étant donné que les opérateurs logiques et au niveau du bit ont une priorité inférieure à celle des opérateurs arithmétiques et relationnels, toutes les opérations au niveau du bit doivent être mises entre parenthèses pour garantir une exécution précise.  
  
## <a name="data-types"></a>Types de données  
 Pour une négation Boolean, le type de données du résultat est `Boolean`. Pour une négation au niveau du bit, le type de données de résultat est identique à celui de `expression`. Toutefois, si l’expression est `Decimal`, le résultat est `Long`.  
  
## <a name="overloading"></a>Surcharge  
 Le `Not` opérateur peut être *surchargé*, ce qui signifie qu’une classe ou structure peut redéfinir son comportement lorsque son opérande a le type de cette classe ou structure. Si votre code utilise cet opérateur sur une telle classe ou structure, veillez à ce que vous comprenez son comportement redéfini. Pour plus d'informations, consultez [Operator Procedures](../../../visual-basic/programming-guide/language-features/procedures/operator-procedures.md).  
  
## <a name="example"></a>Exemple  
 L’exemple suivant utilise le `Not` opérateur effectue une négation logique sur une `Boolean` expression. Le résultat est un `Boolean` valeur qui représente l’inverse de la valeur de l’expression.  
  
 [!code-vb[VbVbalrOperators#33](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbalrOperators/VB/Class1.vb#33)]  
  
 L’exemple précédent produit des résultats de `False` et `True`, respectivement.  
  
## <a name="example"></a>Exemple  
 L’exemple suivant utilise le `Not` opérateur effectue une négation logique des bits individuels d’une expression numérique. Le bit du modèle de résultat est défini à l’inverse du bit correspondant dans le modèle d’opérande, y compris le bit de signe.  
  
 [!code-vb[VbVbalrOperators#34](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbalrOperators/VB/Class1.vb#34)]  
  
 L’exemple précédent produit les résultats de – 11, -9 et -7, respectivement.  
  
## <a name="see-also"></a>Voir aussi

- [Opérateurs logiques/de bits (Visual Basic)](../../../visual-basic/language-reference/operators/logical-bitwise-operators.md)
- [Priorité des opérateurs en Visual Basic](../../../visual-basic/language-reference/operators/operator-precedence.md)
- [Opérateurs répertoriés par fonctionnalité](../../../visual-basic/language-reference/operators/operators-listed-by-functionality.md)
- [Opérateurs logiques et au niveau du bit en Visual Basic](../../../visual-basic/programming-guide/language-features/operators-and-expressions/logical-and-bitwise-operators.md)
