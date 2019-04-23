---
title: Concepts clés d'Entity Data Model
ms.date: 03/30/2017
ms.assetid: c635a16d-6674-45aa-9344-dcb7df992bab
ms.openlocfilehash: 2efa54b6bd656129812cc9dd7c2ce38a4fb2a89a
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59074444"
---
# <a name="entity-data-model-key-concepts"></a>Concepts clés d'Entity Data Model
Le modèle EDM (Entity Data Model) utilise trois concepts clés pour décrire la structure des données : *type d’entité*, *type d’association*, et *propriété*. Il s'agit des concepts les plus importants pour décrire la structure des données dans n'importe quelle implémentation du modèle EDM.  
  
## <a name="entity-type"></a>Type d'entité  
 Le [type d’entité](../../../../docs/framework/data/adonet/entity-type.md) est le bloc de construction fondamental pour décrire la structure de données avec l’Entity Data Model. Dans un modèle conceptuel, les types d’entité sont construites à partir [propriétés](../../../../docs/framework/data/adonet/property.md) et décrivent la structure des concepts de niveau supérieur, comme les clients et commandes dans une application métier. De la même manière qu'une définition de classe dans un logiciel est un modèle pour les instances de la classe, un type d'entité est un modèle pour les entités. Une entité représente un objet spécifique (tel qu'un client ou une commande spécifique). Chaque entité doit avoir une valeur unique [clé d’entité](../../../../docs/framework/data/adonet/entity-key.md) au sein d’un [jeu d’entités](../../../../docs/framework/data/adonet/entity-set.md).  Un jeu d'entités est une collection d'instances d'un type d'entité spécifique. Jeux d’entités (et [ensembles d’associations](../../../../docs/framework/data/adonet/association-set.md)) sont regroupés logiquement dans un [conteneur d’entités](../../../../docs/framework/data/adonet/entity-container.md).  
  
 Les types d'entité prennent en charge l'héritage ; autrement dit, un type d'entité peut être dérivé d'un autre. Pour plus d’informations, consultez [Entity Data Model : L’héritage](../../../../docs/framework/data/adonet/entity-data-model-inheritance.md).  
  
## <a name="association-type"></a>Type d'association  
 Un [type d’association](../../../../docs/framework/data/adonet/association-type.md) (également appelé une association) est le bloc de construction fondamental pour la description des relations dans l’Entity Data Model. Dans un modèle conceptuel, une association représente une relation entre deux types d'entité (tels que Customer et Order). Chaque association possède deux [terminaisons d’association](../../../../docs/framework/data/adonet/association-end.md) qui spécifient les types d’entité impliqués dans l’association. Chaque terminaison d’association spécifie également une [multiplicité de terminaison d’association](../../../../docs/framework/data/adonet/association-end-multiplicity.md) qui indique le nombre d’entités pouvant figurer à cette fin de l’association. La multiplicité de terminaison d'association peut avoir une valeur égale à un (1), zéro ou un (0..1), ou plusieurs (*). Entités à une extrémité d’une association est accessible via [propriétés de navigation](../../../../docs/framework/data/adonet/navigation-property.md), ou via les clés étrangères si elles sont exposées sur un type d’entité. Pour plus d’informations, consultez [propriété de clé étrangère](../../../../docs/framework/data/adonet/foreign-key-property.md).  
  
 Dans une application, une instance d'une association représente une association spécifique (par exemple une association entre une instance de Customer et des instances d'Order). Instances d’association sont regroupées logiquement dans un [ensemble d’associations](../../../../docs/framework/data/adonet/association-set.md). Ensembles d’associations (et [jeux d’entités](../../../../docs/framework/data/adonet/entity-set.md)) sont regroupés logiquement dans un [conteneur d’entités](../../../../docs/framework/data/adonet/entity-container.md).  
  
## <a name="property"></a>Propriété  
 [Types d’entité](../../../../docs/framework/data/adonet/entity-type.md) contiennent [propriétés](../../../../docs/framework/data/adonet/property.md) qui définissent leur structure et leurs caractéristiques. Par exemple, un type d'entité Customer peut avoir des propriétés telles que CustomerId, Name et Address.  
  
 Les propriétés dans un modèle conceptuel sont analogues à celles définies sur une classe dans un logiciel. De même que les propriétés sur une classe définissent la forme de la classe et acheminent des informations sur les objets, les propriétés dans un modèle conceptuel définissent la forme d'un type d'entité et acheminent des informations sur les instances de type d'entité.  
  
 Une propriété peut contenir des données de type primitif (comme une chaîne, un entier ou une valeur booléenne) ou des données structurées (comme un type complexe). Pour plus d’informations, consultez [Entity Data Model : Types de données primitifs](../../../../docs/framework/data/adonet/entity-data-model-primitive-data-types.md).  
  
## <a name="representations-of-a-conceptual-model"></a>Représentations d'un modèle conceptuel  
 Un *modèle conceptuel* est une représentation spécifique de la structure de données en tant qu’entités et relations. Un diagramme est une façon de représenter un modèle conceptuel. Le diagramme suivant représente un modèle conceptuel avec trois types d'entité (`Book`, `Publisher` et `Author`) et deux associations (`PublishedBy` et `WrittenBy`) :  
  
 ![Diagramme montrant un modèle conceptuel avec trois types d’entité.](./media/entity-data-model-key-concepts/conceptual-model-entity-types-associations.gif)  
  
 Toutefois, cette représentation présente des défauts en matière de transmission de détails sur le modèle. Par exemple, les informations sur le type de propriété et le jeu d'entités ne sont pas représentées sur le diagramme. La richesse d’un modèle conceptuel peut être transmise plus clairement dans un langage spécifique à un domaine (DSL). Le [ADO.NET Entity Framework](../../../../docs/framework/data/adonet/ef/index.md) utilise un langage DSL basé sur XML appelé *langage de définition de schéma conceptuel* ([CSDL](../../../../docs/framework/data/adonet/ef/language-reference/csdl-specification.md)) pour définir des modèles conceptuels. Voici la définition CSDL du modèle conceptuel dans le diagramme ci-dessus :  
  
 [!code-xml[EDM_Example_Model#EDMExampleCSDL](../../../../samples/snippets/xml/VS_Snippets_Data/edm_example_model/xml/books.edmx#edmexamplecsdl)]  
  
## <a name="see-also"></a>Voir aussi

- [Entity Data Model](../../../../docs/framework/data/adonet/entity-data-model.md)
