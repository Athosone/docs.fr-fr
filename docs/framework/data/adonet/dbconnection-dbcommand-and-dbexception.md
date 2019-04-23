---
title: DbConnection, DbCommand et DbException
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
ms.assetid: 58aab611-7e6f-4749-b983-28ab7ae87dbe
ms.openlocfilehash: 759b2f36f9d38cdac0cfe4ff8e451b38012493e1
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59143830"
---
# <a name="dbconnection-dbcommand-and-dbexception"></a><span data-ttu-id="ec2eb-102">DbConnection, DbCommand et DbException</span><span class="sxs-lookup"><span data-stu-id="ec2eb-102">DbConnection, DbCommand and DbException</span></span>
<span data-ttu-id="ec2eb-103">Une fois que vous avez créé un <xref:System.Data.Common.DbProviderFactory> et un <xref:System.Data.Common.DbConnection>, vous pouvez utiliser des commandes et des lecteurs de données pour extraire des données de la source de données.</span><span class="sxs-lookup"><span data-stu-id="ec2eb-103">Once you have created a <xref:System.Data.Common.DbProviderFactory> and a <xref:System.Data.Common.DbConnection>, you can then work with commands and data readers to retrieve data from the data source.</span></span>  
  
## <a name="retrieving-data-example"></a><span data-ttu-id="ec2eb-104">Exemple d'extraction de données</span><span class="sxs-lookup"><span data-stu-id="ec2eb-104">Retrieving Data Example</span></span>  
 <span data-ttu-id="ec2eb-105">Cet exemple utilise un objet `DbConnection` comme argument.</span><span class="sxs-lookup"><span data-stu-id="ec2eb-105">This example takes a `DbConnection` object as an argument.</span></span> <span data-ttu-id="ec2eb-106">Un <xref:System.Data.Common.DbCommand> est créé pour sélectionner des données à partir de la table Categories en spécifiant le <xref:System.Data.Common.DbCommand.CommandText%2A> pour une instruction SQL SELECT.</span><span class="sxs-lookup"><span data-stu-id="ec2eb-106">A <xref:System.Data.Common.DbCommand> is created to select data from the Categories table by setting the <xref:System.Data.Common.DbCommand.CommandText%2A> to a SQL SELECT statement.</span></span> <span data-ttu-id="ec2eb-107">Le code suppose que la table Categories existe au niveau de la source de données.</span><span class="sxs-lookup"><span data-stu-id="ec2eb-107">The code assumes that the Categories table exists at the data source.</span></span> <span data-ttu-id="ec2eb-108">La connexion est ouverte et les données sont extraites à l'aide d'un <xref:System.Data.Common.DbDataReader>.</span><span class="sxs-lookup"><span data-stu-id="ec2eb-108">The connection is opened and the data is retrieved using a <xref:System.Data.Common.DbDataReader>.</span></span>  
  
 [!code-csharp[DataWorks DbProviderFactories.DbCommandData#1](../../../../samples/snippets/csharp/VS_Snippets_ADO.NET/DataWorks DbProviderFactories.DbCommandData/CS/source.cs#1)]
 [!code-vb[DataWorks DbProviderFactories.DbCommandData#1](../../../../samples/snippets/visualbasic/VS_Snippets_ADO.NET/DataWorks DbProviderFactories.DbCommandData/VB/source.vb#1)]  
  
## <a name="executing-a-command-example"></a><span data-ttu-id="ec2eb-109">Exemple d'exécution d'une commande</span><span class="sxs-lookup"><span data-stu-id="ec2eb-109">Executing a Command Example</span></span>  
 <span data-ttu-id="ec2eb-110">Cet exemple utilise un objet `DbConnection` comme argument.</span><span class="sxs-lookup"><span data-stu-id="ec2eb-110">This example takes a `DbConnection` object as an argument.</span></span> <span data-ttu-id="ec2eb-111">Si le `DbConnection` est valide, la connexion est ouverte et un <xref:System.Data.Common.DbCommand> est créé et exécuté.</span><span class="sxs-lookup"><span data-stu-id="ec2eb-111">If the `DbConnection` is valid, the connection is opened and a <xref:System.Data.Common.DbCommand> is created and executed.</span></span> <span data-ttu-id="ec2eb-112">Le <xref:System.Data.Common.DbCommand.CommandText%2A> est spécifié pour une instruction SQL INSERT, qui effectue une insertion dans la table Categories, dans la base de données Northwind.</span><span class="sxs-lookup"><span data-stu-id="ec2eb-112">The <xref:System.Data.Common.DbCommand.CommandText%2A> is set to a SQL INSERT statement that performs an insert to the Categories table in the Northwind database.</span></span> <span data-ttu-id="ec2eb-113">Le code suppose que la base de données Northwind existe au niveau de la source de données et que la syntaxe SQL utilisée dans l'instruction INSERT est valide pour le fournisseur spécifié.</span><span class="sxs-lookup"><span data-stu-id="ec2eb-113">The code assumes that the Northwind database exists at the data source, and that the SQL syntax used in the INSERT statement is valid for the specified provider.</span></span> <span data-ttu-id="ec2eb-114">Les erreurs qui se produisent au niveau de la source de données sont traitées par le bloc de code <xref:System.Data.Common.DbException> et toutes les autres exceptions sont traitées dans le bloc <xref:System.Exception>.</span><span class="sxs-lookup"><span data-stu-id="ec2eb-114">Errors occurring at the data source are handled by the <xref:System.Data.Common.DbException> code block, and all other exceptions are handled in the <xref:System.Exception> block.</span></span>  
  
 [!code-csharp[DataWorks DbProviderFactories.DbCommand#1](../../../../samples/snippets/csharp/VS_Snippets_ADO.NET/DataWorks DbProviderFactories.DbCommand/CS/source.cs#1)]
 [!code-vb[DataWorks DbProviderFactories.DbCommand#1](../../../../samples/snippets/visualbasic/VS_Snippets_ADO.NET/DataWorks DbProviderFactories.DbCommand/VB/source.vb#1)]  
  
## <a name="handling-data-errors-with-dbexception"></a><span data-ttu-id="ec2eb-115">Gestion des erreurs de données avec DbException</span><span class="sxs-lookup"><span data-stu-id="ec2eb-115">Handling Data Errors with DbException</span></span>  
 <span data-ttu-id="ec2eb-116">La classe <xref:System.Data.Common.DbException> correspond à la classe de base pour toutes les exceptions levées pour le compte d'une source de données.</span><span class="sxs-lookup"><span data-stu-id="ec2eb-116">The <xref:System.Data.Common.DbException> class is the base class for all exceptions thrown on behalf of a data source.</span></span> <span data-ttu-id="ec2eb-117">Vous pouvez l'utiliser dans votre code de gestion des exceptions pour gérer les exceptions levées par des fournisseurs différents sans avoir à référencer une classe d'exception spécifique.</span><span class="sxs-lookup"><span data-stu-id="ec2eb-117">You can use it in your exception handling code to handle exceptions thrown by different providers without having to reference a specific exception class.</span></span> <span data-ttu-id="ec2eb-118">Le fragment de code ci-dessous montre comment utiliser <xref:System.Data.Common.DbException> pour afficher les informations relatives aux erreurs retournées par la source de données à l'aide des propriétés <xref:System.Exception.GetType%2A>, <xref:System.Exception.Source%2A>, <xref:System.Runtime.InteropServices.ExternalException.ErrorCode%2A> et <xref:System.Exception.Message%2A>.</span><span class="sxs-lookup"><span data-stu-id="ec2eb-118">The following code fragment demonstrates how to use <xref:System.Data.Common.DbException> to display error information returned by the data source using <xref:System.Exception.GetType%2A>, <xref:System.Exception.Source%2A>, <xref:System.Runtime.InteropServices.ExternalException.ErrorCode%2A>, and <xref:System.Exception.Message%2A> properties.</span></span> <span data-ttu-id="ec2eb-119">La sortie indiquera le type d'erreur, la source indiquant le nom du fournisseur, un code d'erreur et le message associé à l'erreur.</span><span class="sxs-lookup"><span data-stu-id="ec2eb-119">The output will display the type of error, the source indicating the provider name, an error code, and the message associated with the error.</span></span>  
  
```vb  
Try  
    ' Do work here.  
Catch ex As DbException  
    ' Display information about the exception.  
    Console.WriteLine("GetType: {0}", ex.GetType())  
    Console.WriteLine("Source: {0}", ex.Source)  
    Console.WriteLine("ErrorCode: {0}", ex.ErrorCode)  
    Console.WriteLine("Message: {0}", ex.Message)  
Finally  
    ' Perform cleanup here.  
End Try  
```  
  
```csharp  
try  
{  
    // Do work here.  
}  
catch (DbException ex)  
{  
    // Display information about the exception.  
    Console.WriteLine("GetType: {0}", ex.GetType());  
    Console.WriteLine("Source: {0}", ex.Source);  
    Console.WriteLine("ErrorCode: {0}", ex.ErrorCode);  
    Console.WriteLine("Message: {0}", ex.Message);  
}  
finally  
{  
    // Perform cleanup here.  
}  
```  
  
## <a name="see-also"></a><span data-ttu-id="ec2eb-120">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ec2eb-120">See also</span></span>

- [<span data-ttu-id="ec2eb-121">DbProviderFactories</span><span class="sxs-lookup"><span data-stu-id="ec2eb-121">DbProviderFactories</span></span>](../../../../docs/framework/data/adonet/dbproviderfactories.md)
- [<span data-ttu-id="ec2eb-122">Obtention d’un DbProviderFactory</span><span class="sxs-lookup"><span data-stu-id="ec2eb-122">Obtaining a DbProviderFactory</span></span>](../../../../docs/framework/data/adonet/obtaining-a-dbproviderfactory.md)
- [<span data-ttu-id="ec2eb-123">Modification des données avec un DbDataAdapter</span><span class="sxs-lookup"><span data-stu-id="ec2eb-123">Modifying Data with a DbDataAdapter</span></span>](../../../../docs/framework/data/adonet/modifying-data-with-a-dbdataadapter.md)
- [<span data-ttu-id="ec2eb-124">Fournisseurs managés ADO.NET et centre de développement DataSet</span><span class="sxs-lookup"><span data-stu-id="ec2eb-124">ADO.NET Managed Providers and DataSet Developer Center</span></span>](https://go.microsoft.com/fwlink/?LinkId=217917)
