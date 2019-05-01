---
title: Résolution de surcharge des fonctions (Entity SQL)
ms.date: 03/30/2017
ms.assetid: 9c648054-3808-4a69-9d3e-98e6a4f9c5ca
ms.openlocfilehash: 0248fdd3f3ba6afb5c7edca740d9aad3ca74bd03
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62034175"
---
# <a name="function-overload-resolution-entity-sql"></a>Résolution de surcharge des fonctions (Entity SQL)
Cette rubrique décrit comment résoudre les fonctions [!INCLUDE[esql](../../../../../../includes/esql-md.md)].  
  
 Plusieurs fonctions peuvent être définies avec le même nom à condition que ces fonctions aient des signatures uniques.  
  
 Lorsque cela est le cas, les critères suivants doivent être appliqués pour déterminer quelle fonction est référencée par une expression donnée. Ces critères sont appliqués dans l'ordre donné. Le premier critère qui s'applique uniquement à une fonction unique est la fonction résolue.  
  
1. **Numéro du paramètre**. La fonction a le même nombre de paramètres spécifiés dans l'expression.  
  
2. **Correspondance exacte sur le type**. Chaque type d’argument de la fonction correspond exactement au type de paramètre ou correspond au littéral Null.  
  
3. **Concordance sur le sous-type**. Chaque type d'argument de la fonction correspond exactement au type de paramètre ou en est un sous-type, ou l'argument correspond au littéral Null. Au cas où plusieurs fonctions diffèrent uniquement par le nombre de conversions de sous-types requis, la fonction avec le moins de conversions de sous-types est la fonction résolue.  
  
4. **Correspondance sur la promotion de type ou sous-type**. Chaque type d'argument de la fonction correspond exactement au type de paramètre, en est un sous-type ou peut être converti dans le type de paramètre, ou l'argument correspond au littéral Null. Encore une fois, au cas où plusieurs fonctions diffèrent uniquement par le nombre de promotions et de conversions de sous-types, la fonction avec le moins de promotions et de conversions de sous-types est la fonction résolue.  
  
 Si aucun de ces critères ne permet la sélection d'une fonction unique, l'expression d'appel de la fonction est ambiguë.  
  
 Même si une fonction unique peut être extraite à l’aide de ces règles, les arguments peuvent ne pas correspondre encore aux paramètres. Dans ce cas, une erreur est générée.  
  
 Pour les fonctions définies par l'utilisateur, la définition pour une fonction de requête inline est prioritaire même lorsqu'une fonction définie par modèle existe avec une signature qui est une meilleure correspondance pour la fonction définie par l'utilisateur.  
  
## <a name="see-also"></a>Voir aussi

- [Référence Entity SQL](../../../../../../docs/framework/data/adonet/ef/language-reference/entity-sql-reference.md)
- [Vue d’ensemble d’Entity SQL](../../../../../../docs/framework/data/adonet/ef/language-reference/entity-sql-overview.md)
- [Fonctions](../../../../../../docs/framework/data/adonet/ef/language-reference/functions-entity-sql.md)
