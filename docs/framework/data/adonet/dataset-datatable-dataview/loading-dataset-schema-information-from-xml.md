---
title: Chargement des informations de schéma de DataSet à partir de XML
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
ms.assetid: 43dfb23b-5cef-46f2-8d87-78f0fba1eb8c
ms.openlocfilehash: 06dcbbedf8c1533b3da52b447c121746ce705083
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59083346"
---
# <a name="loading-dataset-schema-information-from-xml"></a>Chargement des informations de schéma de DataSet à partir de XML
Le schéma d’une <xref:System.Data.DataSet> (ses tables, colonnes, relations et contraintes) peuvent être définis par programme, créé par le **remplir** ou **FillSchema** méthodes d’un <xref:System.Data.Common.DataAdapter>, ou chargés à partir d’un Document XML. Pour charger **DataSet** informations de schéma à partir d’un document XML, vous pouvez utiliser la **ReadXmlSchema** ou le **InferXmlSchema** méthode de la **DataSet**. **ReadXmlSchema** vous permet de charger ou de déduire **DataSet** les informations de schéma à partir du document contenant le schéma XML Schema definition language (XSD) ou un document XML avec un schéma XML inline. **InferXmlSchema** vous permet de déduire le schéma du document XML tout en ignorant certains espaces de noms XML que vous spécifiez.  
  
> [!NOTE]
>  Classement des tables dans un **DataSet** risquent de ne pas être conservés lorsque vous utilisez des services Web ou la sérialisation XML pour transférer un **DataSet** qui a été créé en mémoire à l’aide de constructions XSD (telles que des relations imbriquées). Par conséquent, le destinataire de la **DataSet** ne doit pas varient selon le classement des tables dans ce cas. Toutefois, classement des tables est toujours préservé si le schéma de la **DataSet** en cours de transfert a été lu à partir des fichiers XSD, au lieu d’être créé en mémoire.  
  
## <a name="readxmlschema"></a>ReadXmlSchema  
 Pour charger le schéma d’un **DataSet** à partir d’un document XML sans charger les données, vous pouvez utiliser la **ReadXmlSchema** méthode de la **DataSet**. **ReadXmlSchema** crée **DataSet** schéma défini à l’aide du schéma XML Schema definition language (XSD).  
  
 Le **ReadXmlSchema** méthode accepte un seul argument d’un nom de fichier, un flux, ou un **XmlReader** contenant le document XML à charger. Le document XML peut contenir uniquement le schéma ou contenir le schéma inline avec des éléments XML contenant des données. Pour plus d’informations sur l’écriture de schéma inline sous forme de schéma XML, consultez [dérivation Structure relationnelle des DataSet à partir de XSD (XML Schema)](../../../../../docs/framework/data/adonet/dataset-datatable-dataview/deriving-dataset-relational-structure-from-xml-schema-xsd.md).  
  
 Si le document XML passé à **ReadXmlSchema** ne contient aucune information de schéma inline, **ReadXmlSchema** déduira le schéma à partir des éléments dans le document XML. Si le **DataSet** contient déjà un schéma, le schéma en cours sera étendu par l’ajout de nouvelles tables si elles n’existent pas déjà. De nouvelles colonnes ne seront pas ajoutées aux tables existantes. Si une colonne ajoutée déjà existe dans le **DataSet** mais a un type incompatible avec la colonne trouvée dans le fichier XML, une exception est levée. Pour plus d’informations sur la façon **ReadXmlSchema** déduit un schéma à partir d’un document XML, consultez [déduction Structure relationnelle des DataSet à partir de XML](../../../../../docs/framework/data/adonet/dataset-datatable-dataview/inferring-dataset-relational-structure-from-xml.md).  
  
 Bien que **ReadXmlSchema** charge ou déduit uniquement le schéma d’un **DataSet**, le **ReadXml** méthode de la **DataSet** charge ou déduit les deux le schéma et les données contenues dans le document XML. Pour plus d’informations, consultez [chargement d’un DataSet à partir de XML](../../../../../docs/framework/data/adonet/dataset-datatable-dataview/loading-a-dataset-from-xml.md).  
  
 Les exemples de code suivants montrent comment charger un **DataSet** schéma à partir d’un document XML ou un flux. Le premier exemple montre un nom de fichier de schéma XML passé à la **ReadXmlSchema** (méthode). Le second exemple illustre un **System.IO.StreamReader**.  
  
```vb  
Dim dataSet As DataSet = New DataSet  
dataSet.ReadXmlSchema("schema.xsd")  
```  
  
```csharp  
DataSet dataSet = new DataSet();  
dataSet.ReadXmlSchema("schema.xsd");  
```  
  
```vb  
Dim xmlStream As System.IO.StreamReader = New System.IO.StreamReader ("schema.xsd");  
Dim dataSet As DataSet = New DataSet  
dataSet.ReadXmlSchema(xmlStream)  
xmlStream.Close()  
```  
  
```csharp  
System.IO.StreamReader xmlStream = new System.IO.StreamReader("schema.xsd");  
DataSet dataSet = new DataSet();  
dataSet.ReadXmlSchema(xmlStream);  
xmlStream.Close();  
```  
  
## <a name="inferxmlschema"></a>InferXmlSchema  
 Vous pouvez également demander à la **DataSet** déduise son schéma à partir d’un document XML en utilisant le **InferXmlSchema** méthode de la **DataSet**. **InferXmlSchema** fonctionne de la même manière que **ReadXml** avec un **XmlReadMode** de **InferSchema** (charge les données comme déduit le schéma) et **ReadXmlSchema** si le document lu ne contient pas de schéma inline. Toutefois, **InferXmlSchema** fournit la plus la possibilité de vous pour spécifier les espaces de noms XML qui doivent être ignorés lorsque le schéma est déduit. **InferXmlSchema** accepte deux arguments requis : l’emplacement du document XML, spécifié par un nom de fichier, un flux, ou un **XmlReader**; et un tableau de chaînes d’espaces de noms XML doivent être ignorés par l’opération.  
  
 Examinons, par exemple, le code XML suivant :  
  
```xml  
<NewDataSet xmlns:od="urn:schemas-microsoft-com:officedata">  
<Categories>  
  <CategoryID od:adotype="3">1</CategoryID>   
  <CategoryName od:maxLength="15" od:adotype="130">Beverages</CategoryName>   
  <Description od:adotype="203">Soft drinks and teas</Description>   
</Categories>  
<Products>  
  <ProductID od:adotype="20">1</ProductID>   
  <ReorderLevel od:adotype="3">10</ReorderLevel>   
  <Discontinued od:adotype="11">0</Discontinued>   
</Products>  
</NewDataSet>  
```  
  
 À cause des attributs spécifiés pour les éléments dans le document XML précédent, à la fois le **ReadXmlSchema** (méthode) et le **ReadXml** méthode avec un **XmlReadMode** de **InferSchema** créerait des tables pour chaque élément dans le document : **Catégories**, **CategoryID**, **CategoryName**, **Description**, **produits**, **ProductID**, **ReorderLevel**, et **abandonné**. (Pour plus d’informations, consultez [déduction Structure relationnelle des DataSet à partir de XML](../../../../../docs/framework/data/adonet/dataset-datatable-dataview/inferring-dataset-relational-structure-from-xml.md).) Toutefois, une structure plus appropriée serait pour créer uniquement la **catégories** et **produits** tables, puis comment créer **CategoryID**, **CategoryName** , et **Description** colonnes dans le **catégories** table, et **ProductID**, **ReorderLevel**, et **Discontinued** colonnes dans le **produits** table. Pour vous assurer que le schéma déduit ignore les attributs spécifiés dans les éléments XML, utilisez la **InferXmlSchema** (méthode) et spécifiez l’espace de noms XML **officedata** est ignoré, comme indiqué dans le exemple suivant.  
  
```vb  
Dim dataSet As DataSet = New DataSet  
dataSet.InferXmlSchema("input_od.xml", New String() {"urn:schemas-microsoft-com:officedata"})  
```  
  
```csharp  
DataSet dataSet = new DataSet();  
dataSet.InferXmlSchema("input_od.xml", new string[] "urn:schemas-microsoft-com:officedata");  
```  
  
## <a name="see-also"></a>Voir aussi

- [Utilisation de XML dans un DataSet](../../../../../docs/framework/data/adonet/dataset-datatable-dataview/using-xml-in-a-dataset.md)
- [Dérivation de la structure relationnelle des DataSets à partir du schéma XML (XSD)](../../../../../docs/framework/data/adonet/dataset-datatable-dataview/deriving-dataset-relational-structure-from-xml-schema-xsd.md)
- [Inférence de la structure relationnelle d’un DataSet à partir de XML](../../../../../docs/framework/data/adonet/dataset-datatable-dataview/inferring-dataset-relational-structure-from-xml.md)
- [Chargement d’un DataSet à partir de XML](../../../../../docs/framework/data/adonet/dataset-datatable-dataview/loading-a-dataset-from-xml.md)
- [DataSets, DataTables et DataViews](../../../../../docs/framework/data/adonet/dataset-datatable-dataview/index.md)
- [Fournisseurs managés ADO.NET et centre de développement DataSet](https://go.microsoft.com/fwlink/?LinkId=217917)
