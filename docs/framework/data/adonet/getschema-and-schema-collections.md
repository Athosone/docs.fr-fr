---
title: Collections GetSchema et Schema
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
ms.assetid: 7ab93b89-1221-427c-84ad-04803b3c64b4
ms.openlocfilehash: 11cfad81e40e76691db9f99efd1d60f5528600d2
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59230172"
---
# <a name="getschema-and-schema-collections"></a><span data-ttu-id="a6a5a-102">Collections GetSchema et Schema</span><span class="sxs-lookup"><span data-stu-id="a6a5a-102">GetSchema and Schema Collections</span></span>
<span data-ttu-id="a6a5a-103">Le **connexion** classes dans chacun de l’implémentation de fournisseurs managés .NET Framework un **GetSchema** méthode qui est utilisée pour récupérer des informations de schéma sur la base de données qui est actuellement connecté, et les informations de schéma retournées par la **GetSchema** méthode est fourni sous la forme d’un <xref:System.Data.DataTable>.</span><span class="sxs-lookup"><span data-stu-id="a6a5a-103">The **Connection** classes in each of the .NET Framework managed providers implement a **GetSchema** method which is used to retrieve schema information about the database that is currently connected, and the schema information returned from the **GetSchema** method comes in the form of a <xref:System.Data.DataTable>.</span></span> <span data-ttu-id="a6a5a-104">Le **GetSchema** méthode est une méthode surchargée qui fournit des paramètres facultatifs pour spécifier la collection de schémas à retourner et restreindre la quantité d’informations retournées.</span><span class="sxs-lookup"><span data-stu-id="a6a5a-104">The **GetSchema** method is an overloaded method that provides optional parameters for specifying the schema collection to return, and restricting the amount of information returned.</span></span>  
  
## <a name="specifying-the-schema-collections"></a><span data-ttu-id="a6a5a-105">Spécification des collections de schémas</span><span class="sxs-lookup"><span data-stu-id="a6a5a-105">Specifying the Schema Collections</span></span>  
 <span data-ttu-id="a6a5a-106">Le premier paramètre facultatif de la **GetSchema** méthode correspond au nom de la collection qui est spécifié sous forme de chaîne.</span><span class="sxs-lookup"><span data-stu-id="a6a5a-106">The first optional parameter of the **GetSchema** method is the collection name which is specified as a string.</span></span> <span data-ttu-id="a6a5a-107">Il y a deux types de collection de schémas : les collections de schémas communes qui sont communes à tous les fournisseurs et les collections de schémas spécifiques qui sont spécifiques à chaque fournisseur.</span><span class="sxs-lookup"><span data-stu-id="a6a5a-107">There are two types of schema collections: common schema collections that are common to all providers, and specific schema collections which are specific to each provider.</span></span>  
  
 <span data-ttu-id="a6a5a-108">Vous pouvez interroger un fournisseur .NET Framework managé afin de déterminer la liste des collections de schémas prises en charge en appelant le **GetSchema** méthode sans argument ou avec le nom de collection de schémas « MetaDataCollections ».</span><span class="sxs-lookup"><span data-stu-id="a6a5a-108">You can query a .NET Framework managed provider to determine the list of supported schema collections by calling the **GetSchema** method with no arguments, or with the schema collection name "MetaDataCollections".</span></span> <span data-ttu-id="a6a5a-109">Cette opération retourne un <xref:System.Data.DataTable> avec une liste des collections de schémas prises en charge, le nombre de restrictions qu’elles prennent en charge et le nombre d’éléments d’identification qu’elles utilisent.</span><span class="sxs-lookup"><span data-stu-id="a6a5a-109">This will return a <xref:System.Data.DataTable> with a list of the supported schema collections, the number of restrictions that they each support, and the number of identifier parts that they use.</span></span>  
  
### <a name="retrieving-schema-collections-example"></a><span data-ttu-id="a6a5a-110">Exemple d'extraction de collections de schémas</span><span class="sxs-lookup"><span data-stu-id="a6a5a-110">Retrieving Schema Collections Example</span></span>  
 <span data-ttu-id="a6a5a-111">Les exemples suivants montrent comment utiliser le <xref:System.Data.SqlClient.SqlConnection.GetSchema%2A> méthode du fournisseur de données .NET Framework pour SQL Server <xref:System.Data.SqlClient.SqlConnection> classe à récupérer les informations de schéma sur toutes les tables contenues dans le **AdventureWorks**base de données exemple :</span><span class="sxs-lookup"><span data-stu-id="a6a5a-111">The following examples demonstrate how to use the <xref:System.Data.SqlClient.SqlConnection.GetSchema%2A> method of the .NET Framework Data Provider for the SQL Server <xref:System.Data.SqlClient.SqlConnection> class to retrieve schema information about all of the tables contained in the **AdventureWorks** sample database:</span></span>  
  
```vb  
Imports System.Data.SqlClient  
  
Module Module1  
   Sub Main()  
      Dim connectionString As String = GetConnectionString()  
      Using connection As New SqlConnection(connectionString)  
         'Connect to the database then retrieve the schema information.  
         connection.Open()  
         Dim table As DataTable = connection.GetSchema("Tables")  
  
         ' Display the contents of the table.  
         DisplayData(table)  
         Console.WriteLine("Press any key to continue.")  
         Console.ReadKey()  
      End Using  
   End Sub  
  
   Private Function GetConnectionString() As String  
      ' To avoid storing the connection string in your code,    
      ' you can retrieve it from a configuration file.  
      Return "Data Source=(local);Database=AdventureWorks;" _  
         & "Integrated Security=true;"  
   End Function  
  
   Private Sub DisplayData(ByVal table As DataTable)  
      For Each row As DataRow In table.Rows  
         For Each col As DataColumn In table.Columns  
            Console.WriteLine("{0} = {1}", col.ColumnName, row(col))  
         Next  
         Console.WriteLine("============================")  
      Next  
   End Sub  
End Module  
```  
  
```csharp  
using System;  
using System.Data;  
using System.Data.SqlClient;  
  
class Program  
{  
  static void Main()  
  {  
  string connectionString = GetConnectionString();  
  using (SqlConnection connection = new SqlConnection(connectionString))  
  {  
   // Connect to the database then retrieve the schema information.  
   connection.Open();  
   DataTable table = connection.GetSchema("Tables");  
  
   // Display the contents of the table.  
   DisplayData(table);  
   Console.WriteLine("Press any key to continue.");  
   Console.ReadKey();  
   }  
 }  
  
  private static string GetConnectionString()  
  {  
   // To avoid storing the connection string in your code,  
   // you can retrieve it from a configuration file.  
   return "Data Source=(local);Database=AdventureWorks;" +  
      "Integrated Security=true;";  
  }  
  
  private static void DisplayData(System.Data.DataTable table)  
  {  
     foreach (System.Data.DataRow row in table.Rows)  
     {  
        foreach (System.Data.DataColumn col in table.Columns)  
        {  
           Console.WriteLine("{0} = {1}", col.ColumnName, row[col]);  
        }  
     Console.WriteLine("============================");  
     }  
  }  
}  
```  
  
## <a name="see-also"></a><span data-ttu-id="a6a5a-112">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a6a5a-112">See also</span></span>

- [<span data-ttu-id="a6a5a-113">Récupération des informations de schéma de base de données</span><span class="sxs-lookup"><span data-stu-id="a6a5a-113">Retrieving Database Schema Information</span></span>](../../../../docs/framework/data/adonet/retrieving-database-schema-information.md)
- [<span data-ttu-id="a6a5a-114">Fournisseurs managés ADO.NET et centre de développement DataSet</span><span class="sxs-lookup"><span data-stu-id="a6a5a-114">ADO.NET Managed Providers and DataSet Developer Center</span></span>](https://go.microsoft.com/fwlink/?LinkId=217917)
