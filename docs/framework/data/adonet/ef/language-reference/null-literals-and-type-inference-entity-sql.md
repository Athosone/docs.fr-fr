---
title: Littéraux null et inférence de type (Entity SQL)
ms.date: 03/30/2017
ms.assetid: edd56afb-af1b-4e7d-b210-cb8998143426
ms.openlocfilehash: 22b548f2fc889b20f76a41001438f75c25f99c00
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61760400"
---
# <a name="null-literals-and-type-inference-entity-sql"></a>Littéraux null et inférence de type (Entity SQL)
Les littéraux Null sont compatibles avec n'importe quel type dans le système de type [!INCLUDE[esql](../../../../../../includes/esql-md.md)]. Toutefois, pour le type d’un littéral null soit correctement déduit, [!INCLUDE[esql](../../../../../../includes/esql-md.md)] impose certaines contraintes sur où un littéral null peut être utilisé.  
  
## <a name="typed-nulls"></a>Valeurs Null typées  
 Les valeurs Null typées peuvent être utilisées dans n'importe quel contexte. L'inférence de type n'est pas requise pour les valeurs Null typées car leur type est connu. Par exemple, vous pouvez construire une valeur Null de type Int16 avec la construction [!INCLUDE[esql](../../../../../../includes/esql-md.md)] suivante :  
  
 `(cast(null as Int16))`  
  
## <a name="free-floating-null-literals"></a>Littéraux Null flottants  
 Les littéraux Null flottants peuvent être utilisés dans les contextes suivants :  
  
- En tant qu'argument d'une expression CAST ou TREAT. Il s'agit de la méthode recommandée pour produire une expression Null typée.  
  
- En tant qu'argument d'une méthode ou d'une fonction. Les règles de surcharge standard s'appliquent.  
  
- En tant qu'un des arguments d'une expression arithmétique, telle que +, -, ou /. Les autres arguments ne peuvent pas être des littéraux Null, sinon l’inférence de type n’est pas possible.  
  
- En tant qu'un des arguments d'une expression logique (AND, OR ou NOT). Tous les arguments sont de type Boolean.  
  
- En tant qu’argument d’une expression IS NULL ou IS NOT NULL.  
  
- En tant qu’un ou plusieurs des arguments d’une expression LIKE. Tous les arguments sont supposés être des chaînes.  
  
- En tant qu'un ou plusieurs des arguments d'un constructeur de type nommé.  
  
- En tant qu’un ou plusieurs des arguments d’un constructeur de type multiset. Au moins, un argument du constructeur de type multiset doit être une expression qui n’est pas un littéral Null.  
  
- En tant qu'une ou plusieurs des expressions THEN ou ELSE dans une expression CASE. Au moins l'une des expressions THEN ou ELSE dans l'expression CASE ne doit pas être un littéral Null.  
  
 Les littéraux Null flottants ne peuvent pas être utilisés dans d'autres scénarios. Par exemple, ils ne peuvent pas être servir d’arguments à un constructeur de lignes.  
  
## <a name="see-also"></a>Voir aussi

- [Vue d’ensemble d’Entity SQL](../../../../../../docs/framework/data/adonet/ef/language-reference/entity-sql-overview.md)
