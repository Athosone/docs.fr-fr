---
title: SET (Entity SQL)
ms.date: 03/30/2017
ms.assetid: 28b4deac-c7e4-4f09-b428-4d352ef2dc94
ms.openlocfilehash: 4e2a387cf400a881dfd91c61b36ee3ce0f5a4431
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61797772"
---
# <a name="set-entity-sql"></a>SET (Entity SQL)
L'expression SET est utilisée pour convertir une collection d'objets en ensemble grâce à la production d'une nouvelle collection dans laquelle toutes les éléments en double ont été supprimés.  
  
## <a name="syntax"></a>Syntaxe  
  
```  
SET ( expression )  
```  
  
## <a name="arguments"></a>Arguments  
 `expression`  
 Toute expression de requête valide qui retourne une collection.  
  
## <a name="remarks"></a>Notes  
 L'expression d'ensemble `SET(c)` est logiquement équivalente à l'instruction select suivante :  
  
```  
SELECT VALUE DISTINCT c FROM c  
```  
  
 `SET` est l'un des opérateurs de jeu [!INCLUDE[esql](../../../../../../includes/esql-md.md)] . Tous les opérateurs de jeu [!INCLUDE[esql](../../../../../../includes/esql-md.md)] sont évalués de gauche à droite. Consultez [EXCEPT](../../../../../../docs/framework/data/adonet/ef/language-reference/except-entity-sql.md) pour des informations de priorité pour la [!INCLUDE[esql](../../../../../../includes/esql-md.md)] opérateurs de jeu.  
  
## <a name="example"></a>Exemple  
 La requête Entity SQL ci-dessous utilise l'expression SET pour convertir une collection d'objets en ensemble. Cette requête est basée sur le modèle de vente AdventureWorks Sales Model. Pour compiler et exécuter cette requête, procédez comme suit :  
  
1. Suivez la procédure décrite dans [Comment : Exécuter une requête qui retourne les résultats PrimitiveType](../../../../../../docs/framework/data/adonet/ef/how-to-execute-a-query-that-returns-primitivetype-results.md).  
  
2. Transmettez à la méthode `ExecutePrimitiveTypeQuery` la requête suivante en tant qu'argument :  
  
 [!code-csharp[DP EntityServices Concepts 2#SET](../../../../../../samples/snippets/csharp/VS_Snippets_Data/dp entityservices concepts 2/cs/entitysql.cs#set)]  
  
## <a name="see-also"></a>Voir aussi

- [Référence Entity SQL](../../../../../../docs/framework/data/adonet/ef/language-reference/entity-sql-reference.md)
