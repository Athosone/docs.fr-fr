---
title: Expressions dans les requêtes LINQ to Entities
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
ms.assetid: d70b502f-6a15-4120-b4fe-500b173ad9cc
ms.openlocfilehash: 234b3059f9109c23b8ecae4da37e15f7f094fbd1
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62034188"
---
# <a name="expressions-in-linq-to-entities-queries"></a>Expressions dans les requêtes LINQ to Entities
Une expression est un fragment de code qui peut correspondre à une valeur, un objet, une méthode ou un espace de noms. Elle peut contenir une valeur littérale, un appel de méthode, un opérateur et ses opérandes ou un nom simple. Un nom simple peut être le nom d'une variable, d'un membre de type, d'un paramètre de méthode, d'un espace de noms ou d'un type. Les expressions peuvent utiliser des opérateurs qui à leur tour utilisent d'autres expressions comme des paramètres, ou des appels de méthode dont les paramètres sont à leur tour d'autres appels de méthode. Par conséquent, les expressions peuvent être simples ou très complexes.  
  
 Dans [!INCLUDE[linq_entities](../../../../../../includes/linq-entities-md.md)] requêtes, les expressions peuvent contenir tout élément autorisé par les types dans le <xref:System.Linq.Expressions> espace de noms, y compris les expressions lambda. Les expressions utilisables dans les requêtes [!INCLUDE[linq_entities](../../../../../../includes/linq-entities-md.md)] sont un surensemble des expressions qui permettent d'interroger [!INCLUDE[adonet_ef](../../../../../../includes/adonet-ef-md.md)].  Les expressions qui font partie des requêtes sur le [!INCLUDE[adonet_ef](../../../../../../includes/adonet-ef-md.md)] sont limitées aux opérations prises en charge par `ObjectQuery<T>` et la source de données sous-jacente.  
  
 Dans l'exemple suivant, la comparaison dans la clause `Where` est une expression :  
  
 [!code-csharp[DP L2E Conceptual Examples#WhereExpression](../../../../../../samples/snippets/csharp/VS_Snippets_Data/DP L2E Conceptual Examples/CS/Program.cs#whereexpression)]
 [!code-vb[DP L2E Conceptual Examples#WhereExpression](../../../../../../samples/snippets/visualbasic/VS_Snippets_Data/DP L2E Conceptual Examples/VB/Module1.vb#whereexpression)]  
  
> [!NOTE]
>  Les constructions de langage spécifiques, telles que C# `unchecked`, n'ont aucune signification dans [!INCLUDE[linq_entities](../../../../../../includes/linq-entities-md.md)].  
  
## <a name="in-this-section"></a>Dans cette section  
 [Expressions de constantes](../../../../../../docs/framework/data/adonet/ef/language-reference/constant-expressions.md)  
  
 [Expressions de comparaison](../../../../../../docs/framework/data/adonet/ef/language-reference/comparison-expressions.md)  
  
 [Comparaisons Null](../../../../../../docs/framework/data/adonet/ef/language-reference/null-comparisons.md)  
  
 [Expressions d’initialisation](../../../../../../docs/framework/data/adonet/ef/language-reference/initialization-expressions.md)  
  
 [Relations, les propriétés de navigation et les clés étrangères](/ef/ef6/fundamentals/relationships)  
  
## <a name="see-also"></a>Voir aussi

- [ADO.NET Entity Framework](../../../../../../docs/framework/data/adonet/ef/index.md)
