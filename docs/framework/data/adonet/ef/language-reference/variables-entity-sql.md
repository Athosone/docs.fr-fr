---
title: Variables (Entity SQL)
ms.date: 03/30/2017
ms.assetid: 3eed222a-f8f6-46b6-9cd5-220cc0e4e5d8
ms.openlocfilehash: bf6fa95e38d1eb5817fd67165b6993cbb0755fd1
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59153580"
---
# <a name="variables-entity-sql"></a>Variables (Entity SQL)
## <a name="variable"></a>Variable  
 Une expression de variable est une référence à une expression nommée dans la portée actuelle. Une référence de variable doit être un [!INCLUDE[esql](../../../../../../includes/esql-md.md)] identificateur, tel que défini dans [identificateurs](../../../../../../docs/framework/data/adonet/ef/language-reference/identifiers-entity-sql.md).  
  
 L'exemple suivant montre l'utilisation d'une variable dans l'expression. Le `c` dans la clause FROM représente la définition de la variable. Le `c` dans la clause SELECT représente la référence à la variable.  
  
```  
select c   
from LOB.customers as c  
```  
  
## <a name="see-also"></a>Voir aussi

- [Identificateurs](../../../../../../docs/framework/data/adonet/ef/language-reference/identifiers-entity-sql.md)
- [Paramètres](../../../../../../docs/framework/data/adonet/ef/language-reference/parameters-entity-sql.md)
- [Vue d’ensemble d’Entity SQL](../../../../../../docs/framework/data/adonet/ef/language-reference/entity-sql-overview.md)
