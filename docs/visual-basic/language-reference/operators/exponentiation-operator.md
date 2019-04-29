---
title: ^, opérateur (Visual Basic)
ms.date: 07/20/2015
f1_keywords:
- vb.^
helpviewer_keywords:
- raising numbers to powers
- ^ operator [Visual Basic], exponentiation
- square operator [Visual Basic]
- ^ operator [Visual Basic]
- exponentiation operator [Visual Basic]
- exponent
- numbers [Visual Basic], rasing
- powers
- arithmetic operators [Visual Basic], exponentiation
ms.assetid: d89a1ca8-83da-4784-a87b-a9d7dceb3f62
ms.openlocfilehash: 54de9c91d4e166b8ca1733952dfa9c98ebf11ffe
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61778493"
---
# <a name="-operator-visual-basic"></a>^, opérateur (Visual Basic)

Élève un nombre à la puissance d’un autre nombre.

## <a name="syntax"></a>Syntaxe

```
number ^ exponent
```

## <a name="parts"></a>Composants

`number`\
Obligatoire. Toute expression numérique.

`exponent`\
Obligatoire. Toute expression numérique.

## <a name="result"></a>Résultat

Le résultat est `number` élevé à la puissance de `exponent`, toujours comme un `Double` valeur.

## <a name="supported-types"></a>Types pris en charge

`Double`. Opérandes de tous types sont convertis en `Double`.

## <a name="remarks"></a>Notes

Visual Basic exécute toujours l’élévation à la puissance dans le [Type de données Double](../../../visual-basic/language-reference/data-types/double-data-type.md).

La valeur de `exponent` peut être fractionnaire, négative ou les deux.

Lorsque plusieurs élévation est effectuée dans une expression unique, la `^` opérateur est évalué comme il est rencontré, de gauche à droite.

> [!NOTE]
> Le `^` opérateur peut être *surchargé*, ce qui signifie qu’une classe ou structure peut redéfinir son comportement lorsqu’un opérande a le type de cette classe ou structure. Si votre code utilise cet opérateur sur une telle classe ou structure, veillez à ce que vous comprenez son comportement redéfini. Pour plus d'informations, consultez [Operator Procedures](../../../visual-basic/programming-guide/language-features/procedures/operator-procedures.md).

## <a name="example"></a>Exemple

L’exemple suivant utilise le `^` opérateur pour élever un nombre à la puissance d’un exposant. Le résultat est le premier opérande élevé à la puissance de la seconde.

[!code-vb[VbVbalrOperators#20](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbalrOperators/VB/Class1.vb#20)]

L’exemple précédent produit les résultats suivants :

`exp1` a la valeur 4 (2 au carré).

`exp2` a la valeur 19 683 (3 au cube, puis cette valeur au cube).

`exp3` a la valeur-125 (-5 au cube).

`exp4` a la valeur 625 (-5 à la puissance quatre).

`exp5` est défini sur 2 (racine cubique de 8).

`exp6` a la valeur 0,5 (1,0 divisé par la racine cubique de 8).

Notez l’importance des parenthèses dans les expressions dans l’exemple précédent. Raison de *priorité des opérateurs*, Visual Basic exécute normalement le `^` opérateur avant les autres, même l’unaire `–` opérateur. Si `exp4` et `exp6` avait été calculée sans parenthèses, ils aurait produit les résultats suivants :

`exp4 = -5 ^ 4` sera calculée comme – (5 à la puissance quatrième), ce qui entraînerait-625.

`exp6 = 8 ^ -1.0 / 3.0` sera calculée comme (8 à la puissance-1, ou 0,125) divisé par 3.0, ce qui donnerait 0,041666666666666666666666666666667.

## <a name="see-also"></a>Voir aussi

- [^= (opérateur)](../../../visual-basic/language-reference/operators/exponentiation-assignment-operator.md)
- [Opérateurs arithmétiques](../../../visual-basic/language-reference/operators/arithmetic-operators.md)
- [Priorité des opérateurs en Visual Basic](../../../visual-basic/language-reference/operators/operator-precedence.md)
- [Opérateurs répertoriés par fonctionnalité](../../../visual-basic/language-reference/operators/operators-listed-by-functionality.md)
- [Opérateurs arithmétiques en Visual Basic](../../../visual-basic/programming-guide/language-features/operators-and-expressions/arithmetic-operators.md)
