---
title: Where, clause (Visual Basic)
ms.date: 07/20/2015
f1_keywords:
- vb.QueryWhere
helpviewer_keywords:
- Where statement [Visual Basic]
- queries [Visual Basic], Where
- Where clause [Visual Basic]
ms.assetid: 48b5c2c5-3181-429c-8545-894296798c89
ms.openlocfilehash: 5632e69039baebb3d1f1fd90c04586d9e50fe40f
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "58834502"
---
# <a name="where-clause-visual-basic"></a>Where, clause (Visual Basic)
Spécifie la condition de filtrage pour une requête.  
  
## <a name="syntax"></a>Syntaxe  
  
```  
Where condition  
```  
  
## <a name="parts"></a>Composants  
 `condition`  
 Obligatoire. Une expression qui détermine si les valeurs de l’élément actuel dans la collection sont inclus dans la collection de sortie. L’expression doit correspondre à un `Boolean` valeur ou l’équivalent d’un `Boolean` valeur. Si la condition prend la valeur `True`, l’élément est inclus dans le résultat de la requête ; sinon, l’élément est exclu des résultats de la requête.  
  
## <a name="remarks"></a>Notes  
 Le `Where` clause vous permet de filtrer les données de requête en sélectionnant uniquement les éléments qui répondent à certains critères. Les éléments dont les valeurs font la `Where` clause soit évaluée comme `True` sont inclus dans le résultat de la requête ; autres éléments sont exclus. L’expression qui est utilisée dans un `Where` clause doit correspondre à un `Boolean` ou l’équivalent d’un `Boolean`, comme un entier qui prend la valeur `False` lorsque sa valeur est égale à zéro. Vous pouvez combiner plusieurs expressions dans un `Where` clause à l’aide des opérateurs logiques tels que `And`, `Or`, `AndAlso`, `OrElse`, `Is`, et `IsNot`.  
  
 Par défaut, les expressions de requête ne sont pas évaluées jusqu'à ce qu’ils sont accessibles, par exemple, lorsqu’ils sont liés aux données ou itérées via dans un `For` boucle. Par conséquent, le `Where` clause n’est pas évaluée jusqu'à ce que la requête est accessible. Si des valeurs externes à la requête sont utilisées dans le `Where` clause, vérifiez que la valeur appropriée est utilisée dans le `Where` clause au moment de la requête est exécutée. Pour plus d’informations sur l’exécution des requêtes, consultez [écrire votre première requête LINQ](../../../visual-basic/programming-guide/concepts/linq/writing-your-first-linq-query.md).  
  
 Vous pouvez appeler des fonctions dans un `Where` clause pour effectuer un calcul ou une opération sur une valeur de l’élément actuel dans la collection. Appel d’une fonction un `Where` clause peut entraîner la requête doit être exécutée immédiatement lorsqu’il est défini à la place de lorsqu’il est accessible. Pour plus d’informations sur l’exécution des requêtes, consultez [écrire votre première requête LINQ](../../../visual-basic/programming-guide/concepts/linq/writing-your-first-linq-query.md).  
  
## <a name="example"></a>Exemple  
 La requête suivante expression utilise un `From` clause pour déclarer une variable de portée `cust` pour chaque `Customer` de l’objet dans le `customers` collection. Le `Where` clause utilise la variable de portée pour restreindre la sortie aux clients à partir de la région spécifiée. Le `For Each` boucle affiche le nom de société pour chaque client dans le résultat de la requête.  
  
 [!code-vb[VbSimpleQuerySamples#23](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbSimpleQuerySamples/VB/QuerySamples1.vb#23)]  
  
## <a name="example"></a>Exemple  
 L’exemple suivant utilise `And` et `Or` des opérateurs logiques dans le `Where` clause.  
  
 [!code-vb[VbSimpleQuerySamples#31](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbSimpleQuerySamples/VB/QuerySamples1.vb#31)]  
  
## <a name="see-also"></a>Voir aussi

- [Introduction à LINQ en Visual Basic](../../../visual-basic/programming-guide/language-features/linq/introduction-to-linq.md)
- [Requêtes](../../../visual-basic/language-reference/queries/index.md)
- [From (clause)](../../../visual-basic/language-reference/queries/from-clause.md)
- [Select (clause)](../../../visual-basic/language-reference/queries/select-clause.md)
- [For Each...Next (instruction)](../../../visual-basic/language-reference/statements/for-each-next-statement.md)
