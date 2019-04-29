---
title: Spécifier les relations entre éléments sans imbrication
ms.date: 03/30/2017
ms.assetid: e31325da-7691-4d33-acf4-99fccca67006
ms.openlocfilehash: 4b7b216e58f36302db29c4b4b5176339521b0f17
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61607915"
---
# <a name="specify-relations-between-elements-with-no-nesting"></a><span data-ttu-id="09123-102">Spécifier les relations entre éléments sans imbrication</span><span class="sxs-lookup"><span data-stu-id="09123-102">Specify Relations Between Elements with No Nesting</span></span>
<span data-ttu-id="09123-103">Lorsque des éléments ne sont pas imbriqués, aucune relation implicite n'est créée.</span><span class="sxs-lookup"><span data-stu-id="09123-103">When elements are not nested, no implicit relations are created.</span></span> <span data-ttu-id="09123-104">Toutefois, vous pouvez spécifier explicitement des relations entre les éléments qui ne sont pas imbriqués à l’aide de la **msdata : Relationship** annotation.</span><span class="sxs-lookup"><span data-stu-id="09123-104">You can, however, explicitly specify relations between elements that are not nested by using the **msdata:Relationship** annotation.</span></span>  
  
 <span data-ttu-id="09123-105">L’exemple suivant montre un schéma XML dans lequel le **msdata : Relationship** annotation est spécifiée entre la **ordre** et **OrderDetail** éléments qui ne sont pas imbriquées.</span><span class="sxs-lookup"><span data-stu-id="09123-105">The following example shows an XML Schema in which the **msdata:Relationship** annotation is specified between the **Order** and **OrderDetail** elements, which are not nested.</span></span> <span data-ttu-id="09123-106">Le **msdata : Relationship** annotation est spécifiée comme élément enfant de le **schéma** élément.</span><span class="sxs-lookup"><span data-stu-id="09123-106">The **msdata:Relationship** annotation is specified as the child element of the **Schema** element.</span></span>  
  
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
           <xs:element name="OrderNo" type="xs:string" />  
           <xs:element name="ItemNo" type="xs:string" />  
         </xs:sequence>  
       </xs:complexType>  
      </xs:element>  
      <xs:element name="Order">  
       <xs:complexType>  
         <xs:sequence>  
           <xs:element name="OrderNumber" type="xs:string" />  
           <xs:element name="EmpNumber" type="xs:string" />  
         </xs:sequence>  
       </xs:complexType>  
      </xs:element>  
    </xs:choice>  
  </xs:complexType>  
  
  </xs:element>  
   <xs:annotation>  
     <xs:appinfo>  
       <msdata:Relationship name="OrdOrderDetailRelation"  
                            msdata:parent="Order"   
                            msdata:child="OrderDetail"   
                            msdata:parentkey="OrderNumber"   
                            msdata:childkey="OrderNo"/>  
     </xs:appinfo>  
  </xs:annotation>  
</xs:schema>  
```  
  
 <span data-ttu-id="09123-107">Le processus de mappage de schéma XML Schema definition langage (XSD XML) crée un <xref:System.Data.DataSet> avec **ordre** et **OrderDetail** tables et une relation spécifiée entre ces deux tables, comme indiqué ci-dessous.</span><span class="sxs-lookup"><span data-stu-id="09123-107">The XML Schema definition language (XSD) schema mapping process creates a <xref:System.Data.DataSet> with **Order** and **OrderDetail** tables and a relationship specified between these two tables, as shown below.</span></span>  
  
```  
RelationName: OrdOrderDetailRelation  
ParentTable: Order  
ParentColumns: OrderNumber   
ChildTable: OrderDetail  
ChildColumns: OrderNo   
Nested: False  
```  
  
## <a name="see-also"></a><span data-ttu-id="09123-108">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="09123-108">See also</span></span>

- [<span data-ttu-id="09123-109">Génération de relations de DataSet à partir du schéma XML (XSD)</span><span class="sxs-lookup"><span data-stu-id="09123-109">Generating DataSet Relations from XML Schema (XSD)</span></span>](../../../../../docs/framework/data/adonet/dataset-datatable-dataview/generating-dataset-relations-from-xml-schema-xsd.md)
- [<span data-ttu-id="09123-110">Mappage des contraintes de schéma XML (XSD) aux contraintes de DataSet</span><span class="sxs-lookup"><span data-stu-id="09123-110">Mapping XML Schema (XSD) Constraints to DataSet Constraints</span></span>](../../../../../docs/framework/data/adonet/dataset-datatable-dataview/mapping-xml-schema-xsd-constraints-to-dataset-constraints.md)
- [<span data-ttu-id="09123-111">Fournisseurs managés ADO.NET et centre de développement DataSet</span><span class="sxs-lookup"><span data-stu-id="09123-111">ADO.NET Managed Providers and DataSet Developer Center</span></span>](https://go.microsoft.com/fwlink/?LinkId=217917)
