---
title: Do...Loop, instruction (Visual Basic)
ms.date: 07/20/2015
f1_keywords:
- vb.Do
- vb.Loop
- vb.Until
helpviewer_keywords:
- conditional statements [Visual Basic], Do�Loop
- while statement [Visual Basic], Do...Loop
- execution [Visual Basic], conditional
- Do loops
- Until keyword [Visual Basic], Do...Loop statement
- Do...Loop statement
- instructions, repeating
- Do statement [Visual Basic]
- Exit statement [Visual Basic], in Do...Loop statements
- loop structures [Visual Basic], Do�Loop statements
- do-while statements [Visual Basic]
- loops, exiting
- Loop keyword [Visual Basic], Do...Loop statement
ms.assetid: 892f9096-b3e2-4aee-834d-83bc4e2c379d
ms.openlocfilehash: 3ff3d67f38f510b798da3e470de066cff1e98f29
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "58826039"
---
# <a name="doloop-statement-visual-basic"></a>Do...Loop, instruction (Visual Basic)
Répète un bloc d’instructions tant qu’un `Boolean` condition est `True` ou jusqu'à ce que la condition devient `True`.  
  
## <a name="syntax"></a>Syntaxe  
  
```  
Do { While | Until } condition  
    [ statements ]  
    [ Continue Do ]  
    [ statements ]  
    [ Exit Do ]  
    [ statements ]  
Loop  
-or-  
Do  
    [ statements ]  
    [ Continue Do ]  
    [ statements ]  
    [ Exit Do ]  
    [ statements ]  
Loop { While | Until } condition  
```  
  
## <a name="parts"></a>Composants  
  
|Terme|Définition|  
|---|---|  
|`Do`|Obligatoire. Démarre la définition de la `Do` boucle.|  
|`While`|Requis, sauf si l'option `Until` est utilisée. Répétez la boucle jusqu'à ce que `condition` est `False`.|  
|`Until`|Requis, sauf si l'option `While` est utilisée. Répétez la boucle jusqu'à ce que `condition` est `True`.|  
|`condition`|Facultatif. `Boolean` expression. Si `condition` est `Nothing`, Visual Basic traite en tant que `False`.|  
|`statements`|Optionnel. Une ou plusieurs instructions sont répétées lors ou jusqu'à ce que, `condition` est `True`.|  
|`Continue Do`|Optionnel. Transfère le contrôle à l’itération suivante de la `Do` boucle.|  
|`Exit Do`|Optionnel. Transfère le contrôle de la `Do` boucle.|  
|`Loop`|Obligatoire. Termine la définition de la `Do` boucle.|  
  
## <a name="remarks"></a>Notes  
 Utilisez un `Do...Loop` structure lorsque vous souhaitez répéter un ensemble d’instructions un nombre indéfini de fois, jusqu'à ce qu’une condition est satisfaite. Si vous souhaitez répéter les instructions un nombre défini de fois, le [pour... L’instruction suivante](../../../visual-basic/language-reference/statements/for-next-statement.md) constitue généralement un meilleur choix.  
  
 Vous pouvez utiliser `While` ou `Until` pour spécifier `condition`, mais pas les deux.  
  
 Vous pouvez tester `condition` qu’une seule fois, au début ou la fin de la boucle. Si vous testez `condition` au début de la boucle (dans le `Do` instruction), la boucle ne peut pas s’exécuter même une seule fois. Si vous testez à la fin de la boucle (dans le `Loop` instruction), la boucle s’exécute toujours au moins une fois.  
  
 La condition généralement le résultat d’une comparaison de deux valeurs, mais il peut être toute expression qui prend la valeur d’un [Type de données booléen](../../../visual-basic/language-reference/data-types/boolean-data-type.md) valeur (`True` ou `False`). Cela inclut les valeurs d’autres types de données, telles que des types numériques, qui ont été convertis en `Boolean`.  
  
 Vous pouvez imbriquer `Do` boucles en plaçant une boucle à l’intérieur d’une autre. Vous pouvez également imbriquer des différents types de structures de contrôle dans d’autres. Pour plus d’informations, consultez [Structures de contrôle imbriquées](../../../visual-basic/programming-guide/language-features/control-flow/nested-control-structures.md).  
  
> [!NOTE]
>  Le `Do...Loop` structure vous donne plus de souplesse que le [tandis que... Tandis que l’instruction End](../../../visual-basic/language-reference/statements/while-end-while-statement.md) , car elle vous permet de décider s’il faut mettre fin à la boucle lorsque `condition` cesse d’être `True` ou quand il devient `True`. Il vous permet également de tester `condition` au début ou la fin de la boucle.  
  
## <a name="exit-do"></a>Exit Do  
 Le [Exit Do](../../../visual-basic/language-reference/statements/exit-statement.md) instruction peut fournir une autre façon de quitter un `Do…Loop`. `Exit Do` transfère le contrôle immédiatement à l’instruction qui suit la `Loop` instruction.  
  
 `Exit Do` est souvent utilisé après l’évaluation de certaines conditions, par exemple dans un `If...Then...Else` structure. Vous souhaiterez peut-être quitter une boucle si vous détectez une condition qui rend inutile ou impossible pour poursuivre l’itération, comme une valeur erronée ou une demande d’arrêt. Une des utilisations de `Exit Do` pour tester une condition qui peut entraîner un *boucle sans fin*, qui est une boucle qui pourrait s’exécuter de volumineux ou même infini de fois. Vous pouvez utiliser `Exit Do` pour abandonner la boucle.  
  
 Vous pouvez inclure un nombre quelconque de `Exit Do` instructions n’importe où dans un `Do…Loop`.  
  
 Lorsqu’il est utilisé dans imbriqués `Do` boucles, `Exit Do` transfère le contrôle en dehors de la boucle la plus profonde et dans le niveau d’imbrication supérieur suivant.  
  
## <a name="example"></a>Exemple  
 Dans l’exemple suivant, les instructions dans la boucle continuent à s’exécuter jusqu'à ce que le `index` variable est supérieure à 10. Le `Until` clause est à la fin de la boucle.  
  
 [!code-vb[VbVbalrStatements#131](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbalrStatements/VB/class10.vb#131)]  
  
## <a name="example"></a>Exemple  
 L’exemple suivant utilise un `While` clause au lieu d’un `Until` clause, et `condition` est testée au début de la boucle et non à la fin.  
  
 [!code-vb[VbVbalrStatements#132](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbalrStatements/VB/class10.vb#132)]  
  
## <a name="example"></a>Exemple  
 Dans l’exemple suivant, `condition` arrête la boucle lorsque la `index` variable est supérieure à 100. Le `If` instruction dans la boucle, cependant, entraîne la `Exit Do` instruction pour arrêter la boucle lorsque la variable d’index est supérieure à 10.  
  
 [!code-vb[VbVbalrStatements#133](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbalrStatements/VB/class10.vb#133)]  
  
## <a name="example"></a>Exemple  
 L’exemple suivant lit toutes les lignes dans un fichier texte. Le <xref:System.IO.File.OpenText%2A> méthode ouvre le fichier et retourne un <xref:System.IO.StreamReader> qui lit les caractères. Dans le `Do...Loop` condition, le <xref:System.IO.StreamReader.Peek%2A> méthode de la `StreamReader` détermine s’il existe des caractères supplémentaires.  
  
 [!code-vb[VbVbalrStatements#134](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbalrStatements/VB/class10.vb#134)]  
  
## <a name="see-also"></a>Voir aussi

- [Structures de boucle](../../../visual-basic/programming-guide/language-features/control-flow/loop-structures.md)
- [For...Next (instruction)](../../../visual-basic/language-reference/statements/for-next-statement.md)
- [Booléen (type de données)](../../../visual-basic/language-reference/data-types/boolean-data-type.md)
- [Structures de contrôle imbriquées](../../../visual-basic/programming-guide/language-features/control-flow/nested-control-structures.md)
- [Exit (instruction)](../../../visual-basic/language-reference/statements/exit-statement.md)
- [While...End While (instruction)](../../../visual-basic/language-reference/statements/while-end-while-statement.md)
