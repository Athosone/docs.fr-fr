---
title: UNION (Entity SQL)
ms.date: 03/30/2017
ms.assetid: df98a4db-b00d-4c8b-bd74-0d285f27e1df
ms.openlocfilehash: 736b92f7aac89c309b37a8ac61a295c8d1495d6b
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59323289"
---
# <a name="union-entity-sql"></a>UNION (Entity SQL)
Combine les résultats de deux requêtes, ou plus, en une collection unique.  
  
## <a name="syntax"></a>Syntaxe  
  
```  
expression  
UNION [ ALL ]  
expression  
```  
  
## <a name="arguments"></a>Arguments  
 `expression`  
 Toute expression de requête valide qui retourne une collection à combiner à la collection. Toutes les expressions doivent être du même type que la valeur `expression`ou d'un type de base commun ou dérivé de celui-ci.  
  
 UNION  
 Spécifie que plusieurs collections doivent être combinées et retournées sous la forme d'une collection unique.  
  
 ALL  
 Spécifie que plusieurs collections doivent être combinées et retournées sous la forme d'une collection unique, y compris les doublons. Si cet argument n'est pas spécifié, les doublons sont supprimés de la collection des résultats.  
  
## <a name="return-value"></a>Valeur de retour  
 Collection du même type que l' `expression`ou d'un type de base commun ou dérivé de celui-ci.  
  
## <a name="remarks"></a>Notes  
 UNION est l'un des opérateurs de jeu [!INCLUDE[esql](../../../../../../includes/esql-md.md)] . Tous les opérateurs de jeu [!INCLUDE[esql](../../../../../../includes/esql-md.md)] sont évalués de gauche à droite. Pour plus d’informations de priorité pour le [!INCLUDE[esql](../../../../../../includes/esql-md.md)] opérateurs de jeu, consultez [EXCEPT](../../../../../../docs/framework/data/adonet/ef/language-reference/except-entity-sql.md).  
  
## <a name="example"></a>Exemple  
 La requête Entity SQL ci-dessous utilise l'opérateur UNION ALL pour combiner les résultats de deux requêtes en une collection unique. Cette requête est basée sur le modèle de vente AdventureWorks Sales Model. Pour compiler et exécuter cette requête, procédez comme suit :  
  
1. Suivez la procédure décrite dans [Comment : Exécuter une requête qui retourne des résultats StructuralType](../../../../../../docs/framework/data/adonet/ef/how-to-execute-a-query-that-returns-structuraltype-results.md).  
  
2. Transmettez à la méthode `ExecuteStructuralTypeQuery` la requête suivante en tant qu'argument :  
  
 [!code-csharp[DP EntityServices Concepts 2#UNION](../../../../../../samples/snippets/csharp/VS_Snippets_Data/dp entityservices concepts 2/cs/entitysql.cs#union)]  
  
## <a name="see-also"></a>Voir aussi

- [Référence Entity SQL](../../../../../../docs/framework/data/adonet/ef/language-reference/entity-sql-reference.md)
