---
title: 'Procédure : Assigner un tableau à un autre tableau (Visual Basic)'
ms.date: 07/20/2015
helpviewer_keywords:
- covariance, arrays
- arrays [Visual Basic], assigning
- arrays [Visual Basic], covariance
ms.assetid: 1ae89ea5-f292-4282-bcfc-e9b06b37fbd5
ms.openlocfilehash: 78497de3a9aea55320639c55a151a1260a960159
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62053676"
---
# <a name="how-to-assign-one-array-to-another-array-visual-basic"></a>Procédure : Assigner un tableau à un autre tableau (Visual Basic)

Étant donné que les tableaux sont des objets, vous pouvez les utiliser dans les instructions d’assignation, comme d’autres types d’objets. Une variable de tableau conserve un pointeur vers les données constituant les éléments du tableau et les informations de classement et de longueur et une attribution de copie uniquement ce pointeur.

### <a name="to-assign-one-array-to-another-array"></a>Pour assigner un tableau à un autre tableau

1. Assurez-vous que les deux tableaux ont le même rang (nombre de dimensions) et les types de données d’élément compatibles.

2. Utilisez une instruction d’assignation standard pour assigner le tableau source vers le tableau de destination. Ne suivez pas les noms du tableau de parenthèses.

    ```vb
    Dim formArray() As System.Windows.Forms.Form
    Dim controlArray() As System.Windows.Forms.Control
    controlArray = formArray
    ```

Lorsque vous affectez un tableau à un autre, les règles suivantes s’appliquent :

- **Rangs identiques.** Le rang (nombre de dimensions) du tableau de destination doit être identique à celui du tableau source.

  Condition les rangs des deux tableaux sont égaux, les dimensions n’avez pas besoin être égale. Le nombre d’éléments dans une dimension donnée peut changer lors de l’attribution.

- **Types d’éléments.** Soit les deux tableaux doivent avoir *type référence* éléments ou les deux tableaux doit avoir *type valeur* éléments. Pour plus d'informations, consultez [Value Types and Reference Types](../../../../visual-basic/programming-guide/language-features/data-types/value-types-and-reference-types.md).

  - Si les deux tableaux ont des éléments de type valeur, les types de données d’élément doivent être exactement le même. La seule exception à cela est que vous pouvez assigner un tableau de `Enum` éléments vers un tableau de type de base de qui `Enum`.

  - Si les deux tableaux ont des éléments de type référence, le type d’élément source doit dériver du type d’élément de destination. Lorsque c’est le cas, les deux tableaux ont la même relation d’héritage que leurs éléments. Il s’agit *covariance de tableau*.

Le compilateur signale une erreur si les règles ci-dessus sont violées, par exemple si les types de données ne sont pas compatibles ou les rangs sont inégaux. Vous pouvez ajouter à votre code pour vous assurer que les tableaux sont compatibles avant de tenter une affectation de gestion des erreurs. Vous pouvez également utiliser le [opérateur TryCast](../../../../visual-basic/language-reference/operators/trycast-operator.md) mot clé si vous souhaitez éviter de lever une exception.

## <a name="see-also"></a>Voir aussi

- [Tableaux](../../../../visual-basic/programming-guide/language-features/arrays/index.md)
- [Dépannage des tableaux](../../../../visual-basic/programming-guide/language-features/arrays/troubleshooting-arrays.md)
- [Enum (instruction)](../../../../visual-basic/language-reference/statements/enum-statement.md)
- [Conversions de tableau](../../../../visual-basic/programming-guide/language-features/data-types/array-conversions.md)
