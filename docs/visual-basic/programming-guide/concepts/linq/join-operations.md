---
title: Assembler les opérations (Visual Basic)
ms.date: 07/20/2015
ms.assetid: 39ab4854-ac84-4738-9d0b-3cb79be84db4
ms.openlocfilehash: c7bd81f729558c8ec41baacda99765eb2f862b29
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61834380"
---
# <a name="join-operations-visual-basic"></a>Assembler les opérations (Visual Basic)
Une *jointure* de deux sources de données est l’association des objets d’une source de données aux objets qui partagent un attribut commun dans une autre source de données.  
  
 La jointure est une opération importante dans les requêtes qui ciblent les sources de données dont les relations ne peuvent pas être suivies directement. En programmation orientée objet, cela peut correspondre à une corrélation entre objets qui n'est pas modélisée, par exemple la direction vers l'arrière dans une relation à sens unique. Voici un exemple de relation à sens unique : une classe Customer a une propriété de type City, alors que la classe City n'a aucune propriété correspondant à une collection d'objets Customer. Si vous avez une liste d'objets City et si vous souhaitez rechercher tous les clients de chaque ville, vous pouvez recourir à une opération de jointure.  
  
 Les méthodes de jointure fournies dans le framework LINQ sont <xref:System.Linq.Enumerable.Join%2A> et <xref:System.Linq.Enumerable.GroupJoin%2A>. Ces méthodes effectuent des équijointures, qui sont des jointures associant deux sources de données en fonction de l’égalité de leurs clés. (À titre de comparaison, Transact-SQL prend en charge d'autres opérateurs de jointure que « égal », par exemple, l'opérateur « inférieur à »). Dans le contexte des bases de données relationnelles, <xref:System.Linq.Enumerable.Join%2A> implémente une jointure interne, qui est un type de jointure dans lequel seuls sont retournés les objets qui ont une correspondance dans l’autre jeu de données. La méthode <xref:System.Linq.Enumerable.GroupJoin%2A> n’a aucun équivalent direct dans le contexte des bases de données relationnelles, mais elle implémente un sur-ensemble de jointures internes et de jointures externes gauches. Une jointure externe gauche est une jointure qui retourne chaque élément de la source de données (gauche), même si elle n’a pas d’éléments corrélés dans l’autre source de données.  
  
 L'illustration suivante présente une vue conceptuelle de deux ensembles, ainsi que leurs éléments inclus dans une jointure interne ou une jointure externe gauche.  
  
 ![Deux cercles se chevauchant montrant l’interne&#47;externe.](./media/join-operations/join-method-overlapping-circles.png)  
  
## <a name="methods"></a>Méthodes  
  
|Nom de la méthode|Description|Syntaxe d’Expression de requête de Visual Basic|Informations complémentaires|  
|-----------------|-----------------|------------------------------------------|----------------------|  
|Join|Joint deux séquences selon les fonctions de sélection de clé et extrait des paires de valeurs.|`From x In …, y In … Where x.a = y.a`<br /><br /> - ou -<br /><br /> `Join … [As …]In … On …`|<xref:System.Linq.Enumerable.Join%2A?displayProperty=nameWithType><br /><br /> <xref:System.Linq.Queryable.Join%2A?displayProperty=nameWithType>|  
|GroupJoin|Joint deux séquences selon les fonctions de sélection de clé et regroupe les résultats correspondants pour chaque élément.|`Group Join … In … On …`|<xref:System.Linq.Enumerable.GroupJoin%2A?displayProperty=nameWithType><br /><br /> <xref:System.Linq.Queryable.GroupJoin%2A?displayProperty=nameWithType>|  
  
## <a name="see-also"></a>Voir aussi

- <xref:System.Linq>
- [Vue d’ensemble des opérateurs de requête standard (Visual Basic)](../../../../visual-basic/programming-guide/concepts/linq/standard-query-operators-overview.md)
- [Types anonymes](../../../../visual-basic/programming-guide/language-features/objects-and-classes/anonymous-types.md)
- [Formuler des jointures et des requêtes de produit croisé](../../../../framework/data/adonet/sql/linq/formulate-joins-and-cross-product-queries.md)
- [Join (clause)](../../../../visual-basic/language-reference/queries/join-clause.md)
- [Guide pratique pour Joindre du contenu issu de fichiers (LINQ) (Visual Basic)](../../../../visual-basic/programming-guide/concepts/linq/how-to-join-content-from-dissimilar-files-linq.md)
- [Guide pratique pour Remplir des Collections d’objets issues de plusieurs Sources (LINQ) (Visual Basic)](../../../../visual-basic/programming-guide/concepts/linq/how-to-populate-object-collections-from-multiple-sources-linq.md)
