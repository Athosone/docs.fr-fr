---
title: '- (Soustraction) (Entity SQL)'
ms.date: 03/30/2017
ms.assetid: bc4327f9-09c0-438f-a008-927c5c478040
ms.openlocfilehash: 2e4c08788ea57000e189c8371f0494641931184b
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59316685"
---
# <a name="--subtract-entity-sql"></a>- (soustraction) (Entity SQL)
Soustrait deux nombres.  
  
## <a name="syntax"></a>Syntaxe  
  
```  
expression - expression  
```  
  
## <a name="arguments"></a>Arguments  
 `expression`  
 Toute expression valide de l'un des types de données numériques.  
  
## <a name="result-types"></a>Types de résultats  
 Type de données qui résulte de la promotion de type implicite de deux arguments. Pour plus d’informations sur la promotion de type implicite, consultez [système de Type](../../../../../../docs/framework/data/adonet/ef/language-reference/type-system-entity-sql.md).  
  
## <a name="example"></a>Exemple  
 La requête Entity SQL ci-dessous utilise l'opérateur arithmétique - pour soustraire deux nombres. Cette requête est basée sur le modèle de vente AdventureWorks Sales Model. Pour compiler et exécuter cette requête, procédez comme suit :  
  
1. Suivez la procédure décrite dans [Comment : Exécuter une requête qui retourne des résultats StructuralType](../../../../../../docs/framework/data/adonet/ef/how-to-execute-a-query-that-returns-structuraltype-results.md).  
  
2. Transmettez à la méthode `ExecuteStructuralTypeQuery` la requête suivante en tant qu'argument :  
  
 [!code-csharp[DP EntityServices Concepts 2#SUBTRACT](../../../../../../samples/snippets/csharp/VS_Snippets_Data/dp entityservices concepts 2/cs/entitysql.cs#subtract)]  
  
## <a name="see-also"></a>Voir aussi

- [Référence Entity SQL](../../../../../../docs/framework/data/adonet/ef/language-reference/entity-sql-reference.md)
