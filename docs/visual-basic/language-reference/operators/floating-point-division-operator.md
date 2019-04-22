---
title: /, opérateur (Visual Basic)
ms.date: 07/20/2015
f1_keywords:
- vb./
helpviewer_keywords:
- division operator [Visual Basic], floating point
- floating-point numbers [Visual Basic], division operator
- slash (/) operator
- zero, division by zero
- operators [Visual Basic], arithmetic
- arithmetic operators [Visual Basic], division
- division [Visual Basic], by zero
- operators [Visual Basic], division
- division operator [Visual Basic], syntax
- / operator [Visual Basic]
- math operators [Visual Basic]
ms.assetid: 335e97f2-c434-439e-9064-76973a051101
ms.openlocfilehash: af2316f92e2904eee1e8c046b34b8147e40cb513
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "58825064"
---
# <a name="-operator-visual-basic"></a>/, opérateur (Visual Basic)
Divise deux nombres et retourne un résultat à virgule flottante.  
  
## <a name="syntax"></a>Syntaxe  
  
```  
expression1 / expression2  
```  
  
## <a name="parts"></a>Composants  
 `expression1`  
 Obligatoire. Toute expression numérique.  
  
 `expression2`  
 Obligatoire. Toute expression numérique.  
  
## <a name="supported-types"></a>Types pris en charge  
 Tous les types numériques, y compris les types non signés et à virgule flottante et `Decimal`.  
  
## <a name="result"></a>Résultat  
 Le résultat est le quotient entier de `expression1` divisé par `expression2`, y compris tout élément restant.  
  
 Le [\, opérateur (Visual Basic)](../../../visual-basic/language-reference/operators/integer-division-operator.md) renvoie le quotient entier, ce qui supprime le reste.  
  
## <a name="remarks"></a>Notes  
 Le type de données du résultat dépend des types des opérandes. Le tableau suivant montre comment le type de données du résultat est déterminé.  
  
|Types de données d’opérande|Type de données de résultat|  
|------------------------|----------------------|  
|Les deux expressions sont des types de données intégraux ([SByte](../../../visual-basic/language-reference/data-types/sbyte-data-type.md), [octets](../../../visual-basic/language-reference/data-types/byte-data-type.md), [court](../../../visual-basic/language-reference/data-types/short-data-type.md), [UShort](../../../visual-basic/language-reference/data-types/ushort-data-type.md), [entier](../../../visual-basic/language-reference/data-types/integer-data-type.md), [UInteger](../../../visual-basic/language-reference/data-types/uinteger-data-type.md), [Long](../../../visual-basic/language-reference/data-types/long-data-type.md), [ULong](../../../visual-basic/language-reference/data-types/ulong-data-type.md))|`Double`|  
|Une expression est un [unique](../../../visual-basic/language-reference/data-types/single-data-type.md) type de données et l’autre n’est pas un [Double](../../../visual-basic/language-reference/data-types/double-data-type.md)|`Single`|  
|Une expression est un [décimal](../../../visual-basic/language-reference/data-types/decimal-data-type.md) type de données et l’autre n’est pas un [unique](../../../visual-basic/language-reference/data-types/single-data-type.md) ou un [Double](../../../visual-basic/language-reference/data-types/double-data-type.md)|`Decimal`|  
|Des expressions sont un [Double](../../../visual-basic/language-reference/data-types/double-data-type.md) type de données|`Double`|  
  
 Avant d’effectuer la division, toutes les expressions numériques intégrées sont élargies à `Double`. Si vous affectez le résultat à un type intégral, Visual Basic essaie de convertir le résultat à partir de `Double` à ce type. Cela peut lever une exception si le résultat ne tient pas dans ce type. En particulier, consultez « Tentative de Division par zéro » sur cette page d’aide.  
  
 Si `expression1` ou `expression2` prend la valeur [rien](../../../visual-basic/language-reference/nothing.md), il est considéré comme égal à zéro.  
  
## <a name="attempted-division-by-zero"></a>Tentative de Division par zéro  
 Si `expression2` correspond à zéro, le `/` opérateur se comporte différemment pour les types de données différents d’opérande. Le tableau suivant répertorie les comportements possibles.  
  
|Types de données d’opérande|Comportement si `expression2` est égal à zéro|  
|------------------------|---------------------------------------|  
|À virgule flottante (`Single` ou `Double`)|Retourne l’infini (<xref:System.Double.PositiveInfinity> ou <xref:System.Double.NegativeInfinity>), ou <xref:System.Double.NaN> (pas un nombre) si `expression1` est également égal à zéro|  
|`Decimal`|Lève <xref:System.DivideByZeroException>|  
|Entier (signé ou non signé)|Tentative de conversion en type intégral lève <xref:System.OverflowException> , car les types intégraux ne peut pas accepter <xref:System.Double.PositiveInfinity>, <xref:System.Double.NegativeInfinity>, ou <xref:System.Double.NaN>|  
  
> [!NOTE]
>  Le `/` opérateur peut être *surchargé*, ce qui signifie qu’une classe ou structure peut redéfinir son comportement lorsqu’un opérande a le type de cette classe ou structure. Si votre code utilise cet opérateur sur une telle classe ou structure, veillez à ce que vous comprenez son comportement redéfini. Pour plus d'informations, consultez [Operator Procedures](../../../visual-basic/programming-guide/language-features/procedures/operator-procedures.md).  
  
## <a name="example"></a>Exemple  
 Cet exemple utilise le `/` opérateur d’effectuer une division à virgule flottante. Le résultat est le quotient de deux opérandes.  
  
 [!code-vb[VbVbalrOperators#16](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbalrOperators/VB/Class1.vb#16)]  
  
 Les expressions dans l’exemple précédent retournent les valeurs 2,5 et 3,333333. Notez que le résultat est toujours à virgule flottante (`Double`), même si les deux opérandes sont des constantes entières.  
  
## <a name="see-also"></a>Voir aussi

- [/ =, Opérateur (Visual Basic)](../../../visual-basic/language-reference/operators/floating-point-division-assignment-operator.md)
- [\, Opérateur (Visual Basic)](../../../visual-basic/language-reference/operators/integer-division-operator.md)
- [Types de données des résultats d’opérateur](../../../visual-basic/language-reference/operators/data-types-of-operator-results.md)
- [Opérateurs arithmétiques](../../../visual-basic/language-reference/operators/arithmetic-operators.md)
- [Priorité des opérateurs en Visual Basic](../../../visual-basic/language-reference/operators/operator-precedence.md)
- [Opérateurs répertoriés par fonctionnalité](../../../visual-basic/language-reference/operators/operators-listed-by-functionality.md)
- [Opérateurs arithmétiques en Visual Basic](../../../visual-basic/programming-guide/language-features/operators-and-expressions/arithmetic-operators.md)
