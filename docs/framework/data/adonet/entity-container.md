---
title: conteneur d'entités
ms.date: 03/30/2017
ms.assetid: 16e80405-2c75-42fc-b0e4-b1df53b1c584
ms.openlocfilehash: 4a629a800df63c67dc17d3fc1531a9862861e9c4
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61667246"
---
# <a name="entity-container"></a>conteneur d'entités
Un *conteneur d’entités* est un regroupement logique de [jeux d’entités](../../../../docs/framework/data/adonet/entity-set.md), [ensembles d’associations](../../../../docs/framework/data/adonet/association-set.md), et [importations de fonction](../../../../docs/framework/data/adonet/model-declared-function.md).  
  
 Un conteneur d'entités défini dans un modèle conceptuel doit répondre aux spécifications suivantes :  
  
- Au moins un conteneur d'entités doit être défini dans chaque modèle conceptuel.  
  
- Le conteneur d'entités doit avoir un nom unique dans chaque modèle conceptuel.  
  
 Un conteneur d'entités peut définir des jeux d'entités ou des ensembles d'associations qui utilisent des types d'entité ou des associations définis dans un ou plusieurs espaces de noms. Pour plus d’informations, consultez [Entity Data Model : Espaces de noms](../../../../docs/framework/data/adonet/entity-data-model-namespaces.md).  
  
## <a name="example"></a>Exemple  
 Le diagramme suivant montre un modèle conceptuel avec trois types d'entités : `Book`, `Publisher` et `Author`.  Pour plus d'informations, consultez l'exemple suivant.  
  
 ![Exemple de modèle avec trois types d’entité](./media/entity-container/example-model-three-entity-types.gif)  
  
 Bien que le diagramme n'achemine pas d'informations sur le conteneur d'entités, le modèle conceptuel doit définir un conteneur d'entités. Le [ADO.NET Entity Framework](../../../../docs/framework/data/adonet/ef/index.md) utilise un langage DSL appelé langage de définition de schéma conceptuel ([CSDL](../../../../docs/framework/data/adonet/ef/language-reference/csdl-specification.md)) pour définir des modèles conceptuels. Le CSDL suivant définit un conteneur d'entités pour le modèle conceptuel présenté dans le diagramme ci-dessus. Notez que le nom du conteneur d'entités est défini dans un attribut XML.  
  
 [!code-xml[EDM_Example_Model#EntityContainerExample](../../../../samples/snippets/xml/VS_Snippets_Data/edm_example_model/xml/books.edmx#entitycontainerexample)]  
  
## <a name="see-also"></a>Voir aussi

- [Concepts clés d’Entity Data Model](../../../../docs/framework/data/adonet/entity-data-model-key-concepts.md)
- [Entity Data Model](../../../../docs/framework/data/adonet/entity-data-model.md)
