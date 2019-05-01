---
title: Déduction des colonnes
ms.date: 03/30/2017
ms.assetid: 0e022699-c922-454c-93e2-957dd7e7247a
ms.openlocfilehash: 53e77f624c5af8f61a32d5b1399d2728f32011a7
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62034279"
---
# <a name="inferring-columns"></a>Déduction des colonnes
Après avoir déterminé les éléments à déduire en tant que tables pour un objet <xref:System.Data.DataSet> à partir d'un document XML, ADO.NET déduit les colonnes pour ces tables. ADO.NET 2.0 a introduit un nouveau moteur d’inférence de schéma qui déduit un type de données fortement typées pour chaque **simpleType** élément. Dans les versions précédentes, le type de données d’un élément déduit **simpleType** élément était toujours **xsd : String**.  
  
## <a name="migration-and-backward-compatibility"></a>Migration et compatibilité ascendante  
 Le **ReadXml** méthode prend un argument de type **InferSchema**. Cet argument vous permet de spécifier un comportement d’inférence compatible avec les versions précédentes. Les valeurs disponibles pour le **InferSchema** énumération sont affichés dans le tableau suivant.  
  
 <xref:System.Data.XmlReadMode.InferSchema>  
 Assure la compatibilité ascendante en déduisant toujours un type simple comme l'objet <xref:System.String>.  
  
 <xref:System.Data.XmlReadMode.InferTypedSchema>  
 Déduit un type de données fortement typées. Lève une exception s'il est utilisé avec un objet <xref:System.Data.DataTable>.  
  
 <xref:System.Data.XmlReadMode.IgnoreSchema>  
 Ignore tout schéma inline et lit les données dans le schéma <xref:System.Data.DataSet> existant.  
  
## <a name="attributes"></a>Attributs  
 Comme défini dans [inférence des Tables](../../../../../docs/framework/data/adonet/dataset-datatable-dataview/inferring-tables.md), un élément avec attributs sera déduit en tant que table. Les attributs de cet élément seront ensuite déduits en tant que colonnes de cette table. Le **ColumnMapping** propriété des colonnes est définie **MappingType.Attribute**pour vous assurer que les noms de colonnes seront écrits en tant qu’attributs si le schéma est réécrit en XML. Les valeurs des attributs sont stockées dans une ligne de la table. Examinons, par exemple, le code XML suivant :  
  
```xml  
<DocumentElement>  
  <Element1 attr1="value1" attr2="value2"/>  
</DocumentElement>  
```  
  
 Le processus d’inférence produira une table nommée **Element1** avec deux colonnes, **attr1** et **attr2**. Le **ColumnMapping** propriété des deux colonnes est définie **MappingType.Attribute**.  
  
 **Jeu de données :** DocumentElement  
  
 **Table :** Element1  
  
|attr1|attr2|  
|-----------|-----------|  
|valeur1|valeur2|  
  
## <a name="elements-without-attributes-or-child-elements"></a>Éléments dépourvus d'attributs ou d'éléments enfants  
 Si un élément ne comporte ni éléments enfants, ni attributs, il sera déduit en tant que colonne. Le **ColumnMapping** propriété de la colonne est définie **MappingType.Element**. Le texte des éléments enfants est stocké dans une ligne de la table. Examinons, par exemple, le code XML suivant :  
  
```xml  
<DocumentElement>  
  <Element1>  
    <ChildElement1>Text1</ChildElement1>  
    <ChildElement2>Text2</ChildElement2>  
  </Element1>  
</DocumentElement>  
```  
  
 Le processus d’inférence produira une table nommée **Element1** avec deux colonnes, **ChildElement1** et **ChildElement2**. Le **ColumnMapping** propriété des deux colonnes est définie **MappingType.Element**.  
  
 **Jeu de données :** DocumentElement  
  
 **Table :** Element1  
  
|ChildElement1|ChildElement2|  
|-------------------|-------------------|  
|Text1|Text2|  
  
## <a name="see-also"></a>Voir aussi

- [Inférence de la structure relationnelle d’un DataSet à partir de XML](../../../../../docs/framework/data/adonet/dataset-datatable-dataview/inferring-dataset-relational-structure-from-xml.md)
- [Chargement d’un DataSet à partir de XML](../../../../../docs/framework/data/adonet/dataset-datatable-dataview/loading-a-dataset-from-xml.md)
- [Chargement des informations de schéma de DataSet à partir de XML](../../../../../docs/framework/data/adonet/dataset-datatable-dataview/loading-dataset-schema-information-from-xml.md)
- [Utilisation de XML dans un DataSet](../../../../../docs/framework/data/adonet/dataset-datatable-dataview/using-xml-in-a-dataset.md)
- [DataSets, DataTables et DataViews](../../../../../docs/framework/data/adonet/dataset-datatable-dataview/index.md)
- [Fournisseurs managés ADO.NET et centre de développement DataSet](https://go.microsoft.com/fwlink/?LinkId=217917)
