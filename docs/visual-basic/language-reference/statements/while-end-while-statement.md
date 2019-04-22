---
title: While...End While, instruction (Visual Basic)
ms.date: 07/20/2015
f1_keywords:
- vb.While
- vb.While...EndWhile
helpviewer_keywords:
- While statement [Visual Basic], While...End While
- While statement [Visual Basic]
- While...End While statements [Visual Basic]
ms.assetid: b931d1ce-e8ed-44d8-a13d-92a4f5458a1e
ms.openlocfilehash: 00ca0ad24231128b25a988921386d6bd3265e9a0
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "58843706"
---
# <a name="whileend-while-statement-visual-basic"></a>While...End While, instruction (Visual Basic)
Exécute une série d’instructions tant qu’une condition donnée est `True`.  
  
## <a name="syntax"></a>Syntaxe  
  
```  
While condition  
    [ statements ]  
    [ Continue While ]  
    [ statements ]  
    [ Exit While ]  
    [ statements ]  
End While  
```  
  
## <a name="parts"></a>Composants  
  
|Terme|Définition|  
|---|---|  
|`condition`|Obligatoire. `Boolean` expression. Si `condition` est `Nothing`, Visual Basic traite en tant que `False`.|  
|`statements`|Optionnel. Une ou plusieurs instructions qui suivent `While`, qui exécutera chaque fois `condition` est `True`.|  
|`Continue While`|Optionnel. Transfère le contrôle à l’itération suivante de la `While` bloc.|  
|`Exit While`|Optionnel. Transfère le contrôle de la `While` bloc.|  
|`End While`|Obligatoire. Met fin à la définition du bloc `While`.|  
  
## <a name="remarks"></a>Notes  
 Utilisez un `While...End While` structure lorsque vous souhaitez répéter un ensemble d’instructions un nombre indéfini de fois, tant qu’une condition reste `True`. Si vous souhaitez davantage de flexibilité avec où vous testez la condition ou du résultat vous tester cela, vous préférerez peut-être la [faire... Instruction de boucle](../../../visual-basic/language-reference/statements/do-loop-statement.md). Si vous souhaitez répéter les instructions un nombre défini de fois, le [pour... L’instruction suivante](../../../visual-basic/language-reference/statements/for-next-statement.md) constitue généralement un meilleur choix.  
  
> [!NOTE]
>  Le `While` clé est également utilisé dans le [faire... Instruction de boucle](../../../visual-basic/language-reference/statements/do-loop-statement.md), le [Skip While, Clause](../../../visual-basic/language-reference/queries/skip-while-clause.md) et [Take While, Clause](../../../visual-basic/language-reference/queries/take-while-clause.md).  
  
 Si `condition` est `True`, tous les de la `statements` exécution jusqu'à ce que le `End While` est rencontrée. Contrôle puis le retourne à la `While` instruction, et `condition` est à nouveau vérifié. Si `condition` est toujours `True`, le processus est répété. S’il a `False`, le contrôle passe à l’instruction qui suit la `End While` instruction.  
  
 La `While` instruction toujours vérifie la condition avant le début de la boucle. La boucle continue tant que la condition est `True`. Si `condition` est `False` lorsque vous entrez tout d’abord la boucle, il ne s’exécute même une seule fois.  
  
 Le `condition` généralement les résultats à partir d’une comparaison de deux valeurs, mais elle peuvent être toute expression qui prend la valeur un [Type de données booléen](../../../visual-basic/language-reference/data-types/boolean-data-type.md) valeur (`True` ou `False`). Cette expression peut inclure une valeur d’un autre type de données, comme un type numérique, ce qui a été converti en `Boolean`.  
  
 Vous pouvez imbriquer `While` boucles en plaçant une boucle dans une autre. Vous pouvez également imbriquer des différents types de structures de contrôle dans l’autre. Pour plus d’informations, consultez [Structures de contrôle imbriquées](../../../visual-basic/programming-guide/language-features/control-flow/nested-control-structures.md).  
  
## <a name="exit-while"></a>Sortie lors de la  
 Le [quitter tandis que](../../../visual-basic/language-reference/statements/exit-statement.md) instruction peut fournir une autre façon de quitter un `While` boucle. `Exit While` transfère le contrôle à l’instruction qui suit immédiatement la `End While` instruction.  
  
 Vous utilisez généralement `Exit While` après une condition est évaluée (par exemple, dans un `If...Then...Else` structure). Vous souhaiterez peut-être quitter une boucle si vous détectez une condition qui rend inutile ou impossible pour poursuivre l’itération, comme une valeur erronée ou une demande d’arrêt. Vous pouvez utiliser `Exit While` lorsque vous testez une condition qui peut entraîner un *boucle sans fin*, qui est une boucle qui pourrait s’exécuter très volumineux ou même infini de fois. Vous pouvez ensuite utiliser `Exit While` pour abandonner la boucle.  
  
 Vous pouvez placer un nombre quelconque de `Exit While` instructions n’importe où dans le `While` boucle.  
  
 Lorsqu’il est utilisé dans imbriqués `While` boucles, `Exit While` transfère le contrôle en dehors de la boucle la plus profonde et dans le niveau d’imbrication supérieur suivant.  
  
 La `Continue While` instruction transfère le contrôle immédiatement à l’itération suivante de la boucle. Pour plus d’informations, consultez [instruction Continue](../../../visual-basic/language-reference/statements/continue-statement.md).  
  
## <a name="example"></a>Exemple  
 Dans l’exemple suivant, les instructions dans la boucle continuent à s’exécuter jusqu'à ce que le `index` variable est supérieure à 10.  
  
 [!code-vb[VbVbalrStatements#171](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbalrStatements/VB/class14.vb#171)]  
  
## <a name="example"></a>Exemple  
 L’exemple suivant illustre l’utilisation de la `Continue While` et `Exit While` instructions.  
  
 [!code-vb[VbVbalrStatements#172](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbalrStatements/VB/class14.vb#172)]  
  
## <a name="example"></a>Exemple  
 L’exemple suivant lit toutes les lignes dans un fichier texte. Le <xref:System.IO.File.OpenText%2A> méthode ouvre le fichier et retourne un <xref:System.IO.StreamReader> qui lit les caractères. Dans le `While` condition, le <xref:System.IO.StreamReader.Peek%2A> méthode de la `StreamReader` détermine si le fichier contient des caractères supplémentaires.  
  
 [!code-vb[VbVbalrStatements#173](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbalrStatements/VB/class14.vb#173)]  
  
## <a name="see-also"></a>Voir aussi

- [Structures de boucle](../../../visual-basic/programming-guide/language-features/control-flow/loop-structures.md)
- [Do...Loop (instruction)](../../../visual-basic/language-reference/statements/do-loop-statement.md)
- [For...Next (instruction)](../../../visual-basic/language-reference/statements/for-next-statement.md)
- [Booléen (type de données)](../../../visual-basic/language-reference/data-types/boolean-data-type.md)
- [Structures de contrôle imbriquées](../../../visual-basic/programming-guide/language-features/control-flow/nested-control-structures.md)
- [Exit (instruction)](../../../visual-basic/language-reference/statements/exit-statement.md)
- [Continue (instruction)](../../../visual-basic/language-reference/statements/continue-statement.md)
