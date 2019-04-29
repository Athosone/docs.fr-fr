---
title: Contraintes et relations du schéma XML
ms.date: 03/30/2017
ms.assetid: 165bc2bc-60a1-40e0-9b89-7c68ef979079
ms.openlocfilehash: 990ae2eef8d9fbd28472494c989ae9ecca34251d
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61606981"
---
# <a name="xml-schema-constraints-and-relationships"></a><span data-ttu-id="358d8-102">Contraintes et relations du schéma XML</span><span class="sxs-lookup"><span data-stu-id="358d8-102">XML Schema Constraints and Relationships</span></span>
<span data-ttu-id="358d8-103">Dans un schéma de langage (XSD XML) de définition de schéma XML, vous pouvez spécifier des contraintes (unique, contraintes key et keyref) et des relations (à l’aide de la **msdata : Relationship** annotation).</span><span class="sxs-lookup"><span data-stu-id="358d8-103">In an XML Schema definition language (XSD) schema, you can specify constraints (unique, key, and keyref constraints) and relationships (using the **msdata:Relationship** annotation).</span></span> <span data-ttu-id="358d8-104">Cette rubrique explique comment les contraintes et relations spécifiées dans un schéma XML sont interprétées pour générer l'objet <xref:System.Data.DataSet>.</span><span class="sxs-lookup"><span data-stu-id="358d8-104">This topic explains how the constraints and relationships specified in an XML Schema are interpreted to generate the <xref:System.Data.DataSet>.</span></span>  
  
 <span data-ttu-id="358d8-105">En règle générale, dans un schéma XML, vous spécifiez le **msdata : Relationship** annotation si vous souhaitez générer uniquement des relations dans le **DataSet**.</span><span class="sxs-lookup"><span data-stu-id="358d8-105">In general, in an XML Schema, you specify the **msdata:Relationship** annotation if you want to generate only relationships in the **DataSet**.</span></span> <span data-ttu-id="358d8-106">Pour plus d’informations, consultez [génération de Relations d’un DataSet à partir de XSD (XML Schema)](../../../../../docs/framework/data/adonet/dataset-datatable-dataview/generating-dataset-relations-from-xml-schema-xsd.md).</span><span class="sxs-lookup"><span data-stu-id="358d8-106">For more information, see [Generating DataSet Relations from XML Schema (XSD)](../../../../../docs/framework/data/adonet/dataset-datatable-dataview/generating-dataset-relations-from-xml-schema-xsd.md).</span></span> <span data-ttu-id="358d8-107">Vous spécifiez des contraintes (unique, key et keyref) si vous souhaitez générer des contraintes dans le **DataSet**.</span><span class="sxs-lookup"><span data-stu-id="358d8-107">You specify constraints (unique, key, and keyref) if you want to generate constraints in the **DataSet**.</span></span> <span data-ttu-id="358d8-108">Notez que les contraintes key et keyref peuvent aussi servir à générer des relations, comme expliqué plus loin dans cette rubrique.</span><span class="sxs-lookup"><span data-stu-id="358d8-108">Note that the key and keyref constraints are also used to generate relationships, as explained later in this topic.</span></span>  
  
## <a name="generating-a-relationship-from-key-and-keyref-constraints"></a><span data-ttu-id="358d8-109">Génération d'une relation à partir des contraintes key et keyref</span><span class="sxs-lookup"><span data-stu-id="358d8-109">Generating a Relationship from key and keyref Constraints</span></span>  
 <span data-ttu-id="358d8-110">Au lieu de spécifier le **msdata : Relationship** annotation, vous pouvez spécifier des contraintes key et keyref, qui sont utilisés pendant le processus de mappage de schéma XML pour générer non seulement les contraintes, mais aussi la relation dans le  **Jeu de données**.</span><span class="sxs-lookup"><span data-stu-id="358d8-110">Instead of specifying the **msdata:Relationship** annotation, you can specify key and keyref constraints, which are used during the XML Schema mapping process to generate not only the constraints but also the relationship in the **DataSet**.</span></span> <span data-ttu-id="358d8-111">Toutefois, si vous spécifiez `msdata:ConstraintOnly="true"` dans le **keyref** élément, le **DataSet** inclura uniquement les contraintes et n’inclut pas la relation.</span><span class="sxs-lookup"><span data-stu-id="358d8-111">However, if you specify `msdata:ConstraintOnly="true"` in the **keyref** element, the **DataSet** will include only the constraints and will not include the relationship.</span></span>  
  
 <span data-ttu-id="358d8-112">L’exemple suivant montre un schéma XML qui inclut **ordre** et **OrderDetail** éléments qui ne sont pas imbriqués.</span><span class="sxs-lookup"><span data-stu-id="358d8-112">The following example shows an XML Schema that includes **Order** and **OrderDetail** elements, which are not nested.</span></span> <span data-ttu-id="358d8-113">Le schéma spécifie également des contraintes key et keyref.</span><span class="sxs-lookup"><span data-stu-id="358d8-113">The schema also specifies key and keyref constraints.</span></span>  
  
```xml  
<xs:schema id="MyDataSet" xmlns=""   
            xmlns:xs="http://www.w3.org/2001/XMLSchema"   
            xmlns:msdata="urn:schemas-microsoft-com:xml-msdata">  
  
 <xs:element name="MyDataSet" msdata:IsDataSet="true">  
  <xs:complexType>  
    <xs:choice maxOccurs="unbounded">  
      <xs:element name="OrderDetail">  
       <xs:complexType>  
         <xs:sequence>  
           <xs:element name="OrderNo" type="xs:integer" />  
           <xs:element name="ItemNo" type="xs:string" />  
         </xs:sequence>  
       </xs:complexType>  
      </xs:element>  
      <xs:element name="Order">  
        <xs:complexType>  
          <xs:sequence>  
            <xs:element name="OrderNumber" type="xs:integer" />  
            <xs:element name="EmpNumber" type="xs:integer" />  
          </xs:sequence>  
        </xs:complexType>  
      </xs:element>  
    </xs:choice>  
  </xs:complexType>  
  
  <xs:key name="OrderNumberKey"  >  
    <xs:selector xpath=".//Order" />  
    <xs:field xpath="OrderNumber" />  
  </xs:key>  
  
  <xs:keyref name="OrderNoRef" refer="OrderNumberKey">  
    <xs:selector xpath=".//OrderDetail" />  
    <xs:field xpath="OrderNo" />  
  </xs:keyref>  
 </xs:element>  
</xs:schema>  
```  
  
 <span data-ttu-id="358d8-114">Le **DataSet** qui est généré pendant le schéma XML inclut des processus de mappage du **ordre** et **OrderDetail** tables.</span><span class="sxs-lookup"><span data-stu-id="358d8-114">The **DataSet** that is generated during the XML Schema mapping process includes the **Order** and **OrderDetail** tables.</span></span> <span data-ttu-id="358d8-115">En outre, le **DataSet** inclut des relations et contraintes.</span><span class="sxs-lookup"><span data-stu-id="358d8-115">In addition, the **DataSet** includes relationships and constraints.</span></span> <span data-ttu-id="358d8-116">L'exemple suivant illustre ces relations et contraintes.</span><span class="sxs-lookup"><span data-stu-id="358d8-116">The following example shows these relationships and constraints.</span></span> <span data-ttu-id="358d8-117">Notez que le schéma ne spécifie pas le **msdata : Relationship** annotation ; au lieu de cela, les contraintes key et keyref sont utilisées pour générer la relation.</span><span class="sxs-lookup"><span data-stu-id="358d8-117">Note that the schema does not specify the **msdata:Relationship** annotation; instead, the key and keyref constraints are used to generate the relation.</span></span>  
  
```  
....ConstraintName: OrderNumberKey  
....Type: UniqueConstraint  
....Table: Order  
....Columns: OrderNumber  
....IsPrimaryKey: False  
  
....ConstraintName: OrderNoRef  
....Type: ForeignKeyConstraint  
....Table: OrderDetail  
....Columns: OrderNo  
....RelatedTable: Order  
....RelatedColumns: OrderNumber  
  
..RelationName: OrderNoRef  
..ParentTable: Order  
..ParentColumns: OrderNumber  
..ChildTable: OrderDetail  
..ChildColumns: OrderNo  
..ParentKeyConstraint: OrderNumberKey  
..ChildKeyConstraint: OrderNoRef  
..Nested: False  
```  
  
 <span data-ttu-id="358d8-118">Dans l’exemple de schéma précédent, le **ordre** et **OrderDetail** éléments ne sont pas imbriqués.</span><span class="sxs-lookup"><span data-stu-id="358d8-118">In the previous schema example, the **Order** and **OrderDetail** elements are not nested.</span></span> <span data-ttu-id="358d8-119">Ils le sont dans l'exemple qui suit.</span><span class="sxs-lookup"><span data-stu-id="358d8-119">In the following schema example, these elements are nested.</span></span> <span data-ttu-id="358d8-120">Toutefois, aucun **msdata : Relationship** annotation est spécifiée ; par conséquent, une relation implicite est supposée.</span><span class="sxs-lookup"><span data-stu-id="358d8-120">However, no **msdata:Relationship** annotation is specified; therefore, an implicit relation is assumed.</span></span> <span data-ttu-id="358d8-121">Pour plus d’informations, consultez [implicite Relations entre imbriqués schéma éléments cartographiques](../../../../../docs/framework/data/adonet/dataset-datatable-dataview/map-implicit-relations-between-nested-schema-elements.md).</span><span class="sxs-lookup"><span data-stu-id="358d8-121">For more information, see [Map Implicit Relations Between Nested Schema Elements](../../../../../docs/framework/data/adonet/dataset-datatable-dataview/map-implicit-relations-between-nested-schema-elements.md).</span></span> <span data-ttu-id="358d8-122">Le schéma spécifie également des contraintes key et keyref.</span><span class="sxs-lookup"><span data-stu-id="358d8-122">The schema also specifies key and keyref constraints.</span></span>  
  
```xml  
<xs:schema id="MyDataSet" xmlns=""   
            xmlns:xs="http://www.w3.org/2001/XMLSchema"   
            xmlns:msdata="urn:schemas-microsoft-com:xml-msdata">  
  
 <xs:element name="MyDataSet" msdata:IsDataSet="true">  
  <xs:complexType>  
    <xs:choice maxOccurs="unbounded">  
  
      <xs:element name="Order">  
        <xs:complexType>  
          <xs:sequence>  
            <xs:element name="OrderNumber" type="xs:integer" />  
            <xs:element name="EmpNumber" type="xs:integer" />  
  
            <xs:element name="OrderDetail">  
              <xs:complexType>  
                <xs:sequence>  
                  <xs:element name="OrderNo" type="xs:integer" />  
                  <xs:element name="ItemNo" type="xs:string" />  
                </xs:sequence>  
              </xs:complexType>  
            </xs:element>  
          </xs:sequence>  
        </xs:complexType>  
      </xs:element>  
    </xs:choice>  
  </xs:complexType>  
  
  <xs:key name="OrderNumberKey"  >  
    <xs:selector xpath=".//Order" />  
    <xs:field xpath="OrderNumber" />  
  </xs:key>  
  
  <xs:keyref name="OrderNoRef" refer="OrderNumberKey">  
    <xs:selector xpath=".//OrderDetail" />  
    <xs:field xpath="OrderNo" />  
  </xs:keyref>  
 </xs:element>  
</xs:schema>  
```  
  
 <span data-ttu-id="358d8-123">Le **DataSet** résultant du processus de mappage de schéma XML comprend deux tables :</span><span class="sxs-lookup"><span data-stu-id="358d8-123">The **DataSet** resulting from the XML Schema mapping process includes two tables:</span></span>  
  
```  
Order(OrderNumber, EmpNumber, Order_Id)  
OrderDetail(OrderNumber, ItemNumber, Order_Id)  
```  
  
 <span data-ttu-id="358d8-124">Le **DataSet** inclut également les deux relations (une basée sur le **msdata : Relationship** annotation et l’autre selon les contraintes key et keyref) ainsi que diverses contraintes.</span><span class="sxs-lookup"><span data-stu-id="358d8-124">The **DataSet** also includes the two relationships (one based on the **msdata:relationship** annotation and the other based on the key and keyref constraints) and various constraints.</span></span> <span data-ttu-id="358d8-125">L'exemple suivant illustre ces relations et contraintes.</span><span class="sxs-lookup"><span data-stu-id="358d8-125">The following example shows the relations and constraints.</span></span>  
  
```  
..RelationName: Order_OrderDetail  
..ParentTable: Order  
..ParentColumns: Order_Id  
..ChildTable: OrderDetail  
..ChildColumns: Order_Id  
..ParentKeyConstraint: Constraint1  
..ChildKeyConstraint: Order_OrderDetail  
..Nested: True  
  
..RelationName: OrderNoRef  
..ParentTable: Order  
..ParentColumns: OrderNumber  
..ChildTable: OrderDetail  
..ChildColumns: OrderNo  
..ParentKeyConstraint: OrderNumberKey  
..ChildKeyConstraint: OrderNoRef  
..Nested: False  
  
..ConstraintName: OrderNumberKey  
..Type: UniqueConstraint  
..Table: Order  
..Columns: OrderNumber  
..IsPrimaryKey: False  
  
..ConstraintName: Constraint1  
..Type: UniqueConstraint  
..Table: Order  
..Columns: Order_Id  
..IsPrimaryKey: True  
  
..ConstraintName: Order_OrderDetail  
..Type: ForeignKeyConstraint  
..Table: OrderDetail  
..Columns: Order_Id  
..RelatedTable: Order  
..RelatedColumns: Order_Id  
  
..ConstraintName: OrderNoRef  
..Type: ForeignKeyConstraint  
..Table: OrderDetail  
..Columns: OrderNo  
..RelatedTable: Order  
..RelatedColumns: OrderNumber  
```  
  
 <span data-ttu-id="358d8-126">Si une contrainte keyref faisant référence à une table imbriquée contient la **msdata : IsNested = « true »** annotation, le **DataSet** créera une seule relation imbriquée qui est basée sur la contrainte keyref et la contrainte de clé unique/connexe.</span><span class="sxs-lookup"><span data-stu-id="358d8-126">If a keyref constraint referring to a nested table contains the **msdata:IsNested="true"** annotation, the **DataSet** will create a single nested relationship that is based on the keyref constraint and the related unique/key constraint.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="358d8-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="358d8-127">See also</span></span>

- [<span data-ttu-id="358d8-128">Dérivation de la structure relationnelle des DataSets à partir du schéma XML (XSD)</span><span class="sxs-lookup"><span data-stu-id="358d8-128">Deriving DataSet Relational Structure from XML Schema (XSD)</span></span>](../../../../../docs/framework/data/adonet/dataset-datatable-dataview/deriving-dataset-relational-structure-from-xml-schema-xsd.md)
- [<span data-ttu-id="358d8-129">Fournisseurs managés ADO.NET et centre de développement DataSet</span><span class="sxs-lookup"><span data-stu-id="358d8-129">ADO.NET Managed Providers and DataSet Developer Center</span></span>](https://go.microsoft.com/fwlink/?LinkId=217917)
