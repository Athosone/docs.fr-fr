---
title: Skip While, clause (Visual Basic)
ms.date: 07/20/2015
f1_keywords:
- vb.QuerySkipWhile
helpviewer_keywords:
- Skip While statement [Visual Basic]
- Skip While clause [Visual Basic]
- queries [Visual Basic], Skip While
ms.assetid: 5dee8350-7520-4f1a-b00d-590cacd572d6
ms.openlocfilehash: 3d6caeb1938e8e53e8ec2575f740cd5e49496f62
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "58839897"
---
# <a name="skip-while-clause-visual-basic"></a>Skip While, clause (Visual Basic)
Ignore les éléments d’une collection tant qu’une condition spécifiée a la valeur `true`, puis retourne les éléments restants.  
  
## <a name="syntax"></a>Syntaxe  
  
```  
Skip While expression  
```  
  
## <a name="parts"></a>Composants  
  
|Terme|Définition|  
|---|---|  
|`expression`|Obligatoire. Une expression qui représente une condition pour tester des éléments. L’expression doit retourner un `Boolean` valeur ou un équivalent fonctionnel, comme un `Integer` soit évaluée comme un `Boolean`.|  
  
## <a name="remarks"></a>Notes  
 Le `Skip While` clause ignore des éléments à partir du début d’un résultat de requête jusqu'à ce que le texte fourni `expression` retourne `false`. Après avoir `expression` retourne `false`, la requête retourne tous les éléments restants. Le `expression` est ignoré pour les autres résultats.  
  
 Le `Skip While` clause diffère la `Where` clause dans qui le `Where` clause peut être utilisée pour exclure tous les éléments à partir d’une requête qui ne répondent pas à une condition particulière. Le `Skip While` clause exclut des éléments uniquement jusqu'à la première fois que la condition n’est pas satisfaite. Le `Skip While` clause est particulièrement utile lorsque vous travaillez avec un résultat de requête ordonnée.  
  
 Vous pouvez ignorer un nombre spécifique de résultats à partir du début d’un résultat de requête à l’aide de la `Skip` clause.  
  
## <a name="example"></a>Exemple  
 Le code suivant exemple utilise le `Skip While` clause d’ignorer les résultats jusqu'à ce que le premier client à partir des États-Unis est trouvé.  
  
 [!code-vb[VbSimpleQuerySamples#3](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbSimpleQuerySamples/VB/QuerySamples1.vb#3)]  
  
## <a name="see-also"></a>Voir aussi

- [Introduction à LINQ en Visual Basic](../../../visual-basic/programming-guide/language-features/linq/introduction-to-linq.md)
- [Requêtes](../../../visual-basic/language-reference/queries/index.md)
- [Select (clause)](../../../visual-basic/language-reference/queries/select-clause.md)
- [From (clause)](../../../visual-basic/language-reference/queries/from-clause.md)
- [Skip (clause)](../../../visual-basic/language-reference/queries/skip-clause.md)
- [Take While (clause)](../../../visual-basic/language-reference/queries/take-while-clause.md)
- [Where (clause)](../../../visual-basic/language-reference/queries/where-clause.md)
