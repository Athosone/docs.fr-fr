---
title: Fonctions canoniques
ms.date: 03/30/2017
ms.assetid: bbcc9928-36ea-4dff-9e31-96549ffed958
ms.openlocfilehash: 380c1dbcf86d8bbb844c2b226697d72d00c3e81a
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61606086"
---
# <a name="canonical-functions"></a>Fonctions canoniques
Cette section décrit les fonctions canoniques qui sont prises en charge par tous les fournisseurs de données et qui peuvent être utilisée par toutes les technologies de requête. Les fonctions canoniques ne peuvent pas être étendues par un fournisseur.  
  
 Ces fonctions canoniques seront traduites en fonctionnalités de source de données correspondantes pour le fournisseur. De ce fait, les appels de fonction peuvent être exprimés sous une forme commune dans toutes les sources de données.  
  
 Ces fonctions canoniques étant indépendantes des sources de données, les types d'arguments et de retour des fonctions canoniques sont définis par rapport aux types du modèle conceptuel. Toutefois, il est possible que certaines sources de données ne puissent pas prendre en charge tous les types du modèle conceptuel.  
  
 Lorsque des fonctions canoniques sont utilisées dans une requête [!INCLUDE[esql](../../../../../../includes/esql-md.md)], la fonction appropriée est appelée au niveau de la source de données.  
  
 Le comportement en cas d'entrée null et les conditions d'erreurs sont explicitement spécifiées pour toutes les fonctions canoniques. Les fournisseurs de magasins doivent respecter ce comportement, mais [!INCLUDE[adonet_ef](../../../../../../includes/adonet-ef-md.md)] ne l'applique pas de force.  
  
 Pour les scénarios LINQ, les requêtes sur le [!INCLUDE[adonet_ef](../../../../../../includes/adonet-ef-md.md)] impliquent un mappage entre les méthodes CLR aux méthodes dans la source de données sous-jacente. Les méthodes CLR sont mappées aux fonctions canoniques, ce qui garantit qu'un ensemble spécifique de méthodes sera correctement mappé, quelle que soit la source de données.  
  
## <a name="canonical-functions-namespace"></a>Espace de noms des fonctions canoniques  
 L'espace de noms des fonctions canoniques est <xref:System.Data.Metadata.Edm>. L'espace de noms <xref:System.Data.Metadata.Edm> est automatiquement inclus dans toutes les requêtes. Toutefois, si un autre espace de noms est importé et que celui-ci contient une fonction de même nom qu'une fonction canonique (dans l'espace de noms <xref:System.Data.Metadata.Edm>), vous devez spécifier l'espace de noms.  
  
## <a name="in-this-section"></a>Dans cette section  
 [Fonctions canoniques d’agrégation](../../../../../../docs/framework/data/adonet/ef/language-reference/aggregate-canonical-functions.md)  
 Décrit les fonctions canoniques d'agrégation [!INCLUDE[esql](../../../../../../includes/esql-md.md)].  
  
 [Fonctions canoniques mathématiques](../../../../../../docs/framework/data/adonet/ef/language-reference/math-canonical-functions.md)  
 Décrit les fonctions canoniques mathématiques [!INCLUDE[esql](../../../../../../includes/esql-md.md)].  
  
 [Fonctions canoniques de chaîne](../../../../../../docs/framework/data/adonet/ef/language-reference/string-canonical-functions.md)  
 Décrit les fonctions canoniques de chaîne [!INCLUDE[esql](../../../../../../includes/esql-md.md)].  
  
 [Fonctions canoniques de date et d’heure](../../../../../../docs/framework/data/adonet/ef/language-reference/date-and-time-canonical-functions.md)  
 Décrit les fonctions canoniques de date et d'heure [!INCLUDE[esql](../../../../../../includes/esql-md.md)].  
  
 [Fonctions canoniques au niveau du bit](../../../../../../docs/framework/data/adonet/ef/language-reference/bitwise-canonical-functions.md)  
 Décrit les fonctions canoniques au niveau du bit [!INCLUDE[esql](../../../../../../includes/esql-md.md)].  
  
 [Fonctions spatiales](../../../../../../docs/framework/data/adonet/ef/language-reference/spatial-functions.md)  
 Décrit les fonctions canoniques spatiales [!INCLUDE[esql](../../../../../../includes/esql-md.md)].  
  
 [Autres fonctions canoniques](../../../../../../docs/framework/data/adonet/ef/language-reference/other-canonical-functions.md)  
 Décrit les fonctions qui ne sont pas considérées comme des fonctions au niveau du bit, des fonctions de date/heure, des fonctions de chaîne, des fonctions mathématiques ni des fonctions d'agrégation.  
  
## <a name="see-also"></a>Voir aussi

- [Vue d’ensemble d’Entity SQL](../../../../../../docs/framework/data/adonet/ef/language-reference/entity-sql-overview.md)
- [Référence Entity SQL](../../../../../../docs/framework/data/adonet/ef/language-reference/entity-sql-reference.md)
- [Mappage du modèle conceptuel canonique aux fonctions SQL Server](../../../../../../docs/framework/data/adonet/ef/conceptual-model-canonical-to-sql-server-functions-mapping.md)
- [Fonctions définies par l’utilisateur](../../../../../../docs/framework/data/adonet/ef/language-reference/user-defined-functions-entity-sql.md)
