---
title: Annotation de DataSet typés
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
ms.assetid: f82aaa62-321e-4c8a-b51b-9d1114700170
ms.openlocfilehash: d8a1a12a4d8ab5e6f4b0fe6ad6c2a3759aa65aa9
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59085127"
---
# <a name="annotating-typed-datasets"></a>Annotation de DataSet typés
Les annotations vous permettent de modifier le nom des éléments de votre objet <xref:System.Data.DataSet> typé sans pour autant modifier le schéma sous-jacent. Modifier les noms des éléments de votre schéma sous-jacent entraînerait typée **DataSet** pour faire référence aux objets qui n'effectuer pas exister dans la source de données, ainsi que perdrait des références aux objets qui existent dans la source de données.  
  
 À l’aide des annotations, vous pouvez personnaliser les noms des objets dans votre typé **DataSet** avec des noms plus explicites, rendre le code plus lisible et votre typé **DataSet** plus facile pour les clients à utiliser, tout en laissant schéma sous-jacente intacte. Par exemple, l’élément de schéma suivant pour la **clients** table de la **Northwind** entraînerait des base de données un **DataRow** nom d’objet du  **CustomersRow** et un <xref:System.Data.DataRowCollection> nommé **clients**.  
  
```xml  
<xs:element name="Customers">  
  <xs:complexType>  
    <xs:sequence>  
      <xs:element name="CustomerID" type="xs:string" minOccurs="0" />  
    </xs:sequence>  
  </xs:complexType>  
</xs:element>  
```  
  
 Un **DataRowCollection** nom de **clients** est significative dans le code client, mais un **DataRow** nom de **CustomersRow** est trompeur s’agissant d’un seul objet. En outre, en commun des scénarios, l’objet est désigné sans le **ligne** identificateur et à la place aurait simplement appelé un **client** objet. La solution consiste à annoter le schéma et à identifier de nouveaux noms pour le **DataRow** et **DataRowCollection** objets. Voici une version annotée du précédent schéma.  
  
```xml  
<xs:element name="Customers" codegen:typedName="Customer" codegen:typedPlural="Customers">  
  <xs:complexType>  
    <xs:sequence>  
      <xs:element name="CustomerID" type="xs:string" minOccurs="0" />  
    </xs:sequence>  
  </xs:complexType>  
</xs:element>  
```  
  
 En spécifiant un **typedName** valeur **client** entraîne une **DataRow** nom de l’objet de **client**. En spécifiant un **typedPlural** valeur **clients** conserve la **DataRowCollection** nom de **clients**.  
  
 Le tableau suivant présente les différentes annotations disponibles.  
  
|Annotation|Description|  
|----------------|-----------------|  
|**typedName**|Nom de l'objet.|  
|**typedPlural**|Nom d’une collection d’objets.|  
|**typedParent**|Nom de l'objet lorsqu'il y est fait référence dans une relation parente.|  
|**typedChildren**|Nom de la méthode permettant de retourner des objets d'une relation enfant.|  
|**nullValue**|Valeur si la valeur sous-jacente est **DBNull**. Consultez le tableau suivant pour **nullValue** annotations. La valeur par défaut est **_throw**.|  
  
 Le tableau suivant présente les valeurs qui peuvent être spécifiées pour le **nullValue** annotation.  
  
|Valeur nullValue|Description|  
|---------------------|-----------------|  
|*Valeur de remplacement*|Spécifier une valeur à retourner. La valeur retournée doit correspondre au type de l'élément. Par exemple, utilisez `nullValue="0"` pour retourner 0 pour les champs de type null integer (entier nul).|  
|**_throw**|Levée d'une exception. Il s'agit de la valeur par défaut.|  
|**_null**|Retourner une référence null ou lever une exception si un type primitif est rencontré.|  
|**_empty**|Pour les chaînes, retourner **String.Empty**, sinon retourne un objet créé à partir d’un constructeur vide. Si un type primitif est rencontré, lever une exception.|  
  
 Le tableau suivant présente les valeurs par défaut pour les objets dans un **DataSet** et les annotations disponibles.  
  
|Objet/méthode/événement|Par défaut|Annotation|  
|---------------------------|-------------|----------------|  
|**DataTable**|TableNameDataTable|typedPlural|  
|**DataTable** méthodes|NewTableNameRow<br /><br /> AddTableNameRow<br /><br /> DeleteTableNameRow|typedName|  
|**DataRowCollection**|TableName|typedPlural|  
|**DataRow**|TableNameRow|typedName|  
|**DataColumn**|DataTable.ColumnNameColumn<br /><br /> DataRow.ColumnName|typedName|  
|**Property**|PropertyName|typedName|  
|**Enfant** accesseur|GetChildTableNameRows|typedChildren|  
|**Parent** accesseur|TableNameRow|typedParent|  
|**Jeu de données** événements|TableNameRowChangeEvent<br /><br /> TableNameRowChangeEventHandler|typedName|  
  
 Pour utiliser automatiquement **DataSet** annotations, vous devez inclure ce qui suit **xmlns** référence dans votre schéma de langage (XSD XML) de définition de schéma XML. Pour créer un xsd à partir des tables de base de données, consultez <xref:System.Data.DataSet.WriteXmlSchema%2A> ou [utilisation de Datasets dans Visual Studio](/visualstudio/data-tools/dataset-tools-in-visual-studio).  
  
```  
xmlns:codegen="urn:schemas-microsoft-com:xml-msprop"  
```  
  
 Voici un exemple de schéma annoté qui expose le **clients** table du **Northwind** base de données avec une relation avec le **Orders** table incluse.  
  
```xml  
<?xml version="1.0" encoding="utf-8"?>  
<xs:schema id="CustomerDataSet"   
      xmlns:codegen="urn:schemas-microsoft-com:xml-msprop"  
      xmlns=""   
      xmlns:xs="http://www.w3.org/2001/XMLSchema"   
      xmlns:msdata="urn:schemas-microsoft-com:xml-msdata">  
  <xs:element name="CustomerDataSet" msdata:IsDataSet="true">  
    <xs:complexType>  
      <xs:choice maxOccurs="unbounded">  
        <xs:element name="Customers" codegen:typedName="Customer" codegen:typedPlural="Customers">  
          <xs:complexType>  
            <xs:sequence>  
              <xs:element name="CustomerID"  
codegen:typedName="CustomerID" type="xs:string" minOccurs="0" />  
              <xs:element name="CompanyName"  
codegen:typedName="CompanyName" type="xs:string" minOccurs="0" />  
              <xs:element name="Phone" codegen:typedName="Phone" codegen:nullValue="" type="xs:string" minOccurs="0" />  
            </xs:sequence>  
          </xs:complexType>  
        </xs:element>  
        <xs:element name="Orders" codegen:typedName="Order" codegen:typedPlural="Orders">  
          <xs:complexType>  
            <xs:sequence>  
              <xs:element name="OrderID" codegen:typedName="OrderID"  
type="xs:int" minOccurs="0" />  
              <xs:element name="CustomerID"  
codegen:typedName="CustomerID"                  codegen:nullValue="" type="xs:string" minOccurs="0" />  
              <xs:element name="EmployeeID"  
codegen:typedName="EmployeeID" codegen:nullValue="0"   
type="xs:int" minOccurs="0" />  
              <xs:element name="OrderAdapter"  
codegen:typedName="OrderAdapter" codegen:nullValue="1980-01-01T00:00:00"   
type="xs:dateTime" minOccurs="0" />  
            </xs:sequence>  
          </xs:complexType>  
        </xs:element>  
      </xs:choice>  
    </xs:complexType>  
    <xs:unique name="Constraint1">  
      <xs:selector xpath=".//Customers" />  
      <xs:field xpath="CustomerID" />  
    </xs:unique>  
    <xs:keyref name="CustOrders" refer="Constraint1"  
codegen:typedParent="Customer" codegen:typedChildren="GetOrders">  
      <xs:selector xpath=".//Orders" />  
      <xs:field xpath="CustomerID" />  
    </xs:keyref>  
  </xs:element>  
</xs:schema>  
```  
  
 L’exemple de code suivant utilise fortement typé **DataSet** créé à partir de l’exemple de schéma. Il utilise un <xref:System.Data.SqlClient.SqlDataAdapter> pour remplir le **clients** table et une autre <xref:System.Data.SqlClient.SqlDataAdapter> pour remplir le **commandes** table. Fortement typé **DataSet** définit le **DataRelations**.  
  
```vb  
' Assumes a valid SqlConnection object named connection.  
Dim customerAdapter As SqlDataAdapter = New SqlDataAdapter( _  
    "SELECT CustomerID, CompanyName, Phone FROM Customers", &  
    connection)  
Dim orderAdapter As SqlDataAdapter = New SqlDataAdapter( _  
    "SELECT OrderID, CustomerID, EmployeeID, OrderAdapter FROM Orders", &  
    connection)  
  
' Populate a strongly typed DataSet.  
connection.Open()  
Dim customers As CustomerDataSet = New CustomerDataSet()  
customerAdapter.Fill(customers, "Customers")  
orderAdapter.Fill(customers, "Orders")  
connection.Close()  
  
' Add a strongly typed event.  
AddHandler customers.Customers.CustomerChanged, &  
    New CustomerDataSet.CustomerChangeEventHandler( _  
    AddressOf OnCustomerChanged)  
  
' Add a strongly typed DataRow.  
Dim newCustomer As CustomerDataSet.Customer = _  
    customers.Customers.NewCustomer()  
newCustomer.CustomerID = "NEW01"  
newCustomer.CompanyName = "My New Company"  
customers.Customers.AddCustomer(newCustomer)  
  
' Navigate the child relation.  
Dim customer As CustomerDataSet.Customer  
Dim order As CustomerDataSet.Order  
  
For Each customer In customers.Customers  
  Console.WriteLine(customer.CustomerID)  
  For Each order In customer.GetOrders()  
    Console.WriteLine(vbTab & order.OrderID)  
  Next  
Next  
  
Private Shared Sub OnCustomerChanged( _  
    sender As Object, e As CustomerDataSet.CustomerChangeEvent)  
  
End Sub  
```  
  
```csharp  
// Assumes a valid SqlConnection object named connection.  
SqlDataAdapter customerAdapter = new SqlDataAdapter(  
    "SELECT CustomerID, CompanyName, Phone FROM Customers",  
    connection);  
SqlDataAdapter orderAdapter = new SqlDataAdapter(  
    "SELECT OrderID, CustomerID, EmployeeID, OrderAdapter FROM Orders",   
    connection);  
  
// Populate a strongly typed DataSet.  
connection.Open();  
CustomerDataSet customers = new CustomerDataSet();  
customerAdapter.Fill(customers, "Customers");  
orderAdapter.Fill(customers, "Orders");  
connection.Close();  
  
// Add a strongly typed event.  
customers.Customers.CustomerChanged += new   
  CustomerDataSet.CustomerChangeEventHandler(OnCustomerChanged);  
  
// Add a strongly typed DataRow.  
CustomerDataSet.Customer newCustomer =   
    customers.Customers.NewCustomer();  
newCustomer.CustomerID = "NEW01";  
newCustomer.CompanyName = "My New Company";  
customers.Customers.AddCustomer(newCustomer);  
  
// Navigate the child relation.  
foreach(CustomerDataSet.Customer customer in customers.Customers)  
{  
  Console.WriteLine(customer.CustomerID);  
  foreach(CustomerDataSet.Order order in customer.GetOrders())  
    Console.WriteLine("\t" + order.OrderID);  
}  
  
protected static void OnCustomerChanged(object sender, CustomerDataSet.CustomerChangeEvent e)  
    {  
  
    }  
```  
  
## <a name="see-also"></a>Voir aussi

- <xref:System.Data.DataColumnCollection>
- <xref:System.Data.DataSet>
- [Datasets typés](../../../../../docs/framework/data/adonet/dataset-datatable-dataview/typed-datasets.md)
- [DataSets, DataTables et DataViews](../../../../../docs/framework/data/adonet/dataset-datatable-dataview/index.md)
- [Fournisseurs managés ADO.NET et centre de développement DataSet](https://go.microsoft.com/fwlink/?LinkId=217917)
