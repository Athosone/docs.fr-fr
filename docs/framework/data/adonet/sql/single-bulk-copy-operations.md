---
title: Opérations uniques de copie en bloc
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
ms.assetid: 5e7ff0be-3f23-4996-a92c-bd54d65c3836
ms.openlocfilehash: b2783779965505d09f73c7203770c19ccaa78d26
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61876367"
---
# <a name="single-bulk-copy-operations"></a><span data-ttu-id="ff010-102">Opérations uniques de copie en bloc</span><span class="sxs-lookup"><span data-stu-id="ff010-102">Single Bulk Copy Operations</span></span>
<span data-ttu-id="ff010-103">L'approche la plus simple de l'exécution d'une opération de copie en bloc SQL Server consiste à exécuter une opération unique sur une base de données.</span><span class="sxs-lookup"><span data-stu-id="ff010-103">The simplest approach to performing a SQL Server bulk copy operation is to perform a single operation against a database.</span></span> <span data-ttu-id="ff010-104">Par défaut, une opération de copie en bloc s'effectue comme une opération isolée : l'opération de copie se produit de façon non traitée, sans possibilité de restauration.</span><span class="sxs-lookup"><span data-stu-id="ff010-104">By default, a bulk copy operation is performed as an isolated operation: the copy operation occurs in a non-transacted way, with no opportunity for rolling it back.</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="ff010-105">Si vous devez restaurer tout ou partie de la copie en bloc en cas d’erreur, vous pouvez soit utiliser une transaction <xref:System.Data.SqlClient.SqlBulkCopy> managée, soit effectuer une opération de copie en bloc à l’intérieur d’une transaction existante.</span><span class="sxs-lookup"><span data-stu-id="ff010-105">If you need to roll back all or part of the bulk copy when an error occurs, you can either use a <xref:System.Data.SqlClient.SqlBulkCopy>-managed transaction, or perform the bulk copy operation within an existing transaction.</span></span> <span data-ttu-id="ff010-106">**SqlBulkCopy** fonctionneront également avec <xref:System.Transactions> si la connexion est inscrite (implicitement ou explicitement) dans un **System.Transactions** transaction.</span><span class="sxs-lookup"><span data-stu-id="ff010-106">**SqlBulkCopy** will also work with <xref:System.Transactions> if the connection is enlisted (implicitly or explicitly) into a **System.Transactions** transaction.</span></span>  
>   
>  <span data-ttu-id="ff010-107">Pour plus d’informations, consultez [Transaction et opérations de copie en bloc](../../../../../docs/framework/data/adonet/sql/transaction-and-bulk-copy-operations.md).</span><span class="sxs-lookup"><span data-stu-id="ff010-107">For more information, see [Transaction and Bulk Copy Operations](../../../../../docs/framework/data/adonet/sql/transaction-and-bulk-copy-operations.md).</span></span>  
  
 <span data-ttu-id="ff010-108">Les étapes générales pour l'exécution d'une opération de copie en bloc sont les suivantes :</span><span class="sxs-lookup"><span data-stu-id="ff010-108">The general steps for performing a bulk copy operation are as follows:</span></span>  
  
1. <span data-ttu-id="ff010-109">Connectez-vous au serveur source et obtenez les données à copier.</span><span class="sxs-lookup"><span data-stu-id="ff010-109">Connect to the source server and obtain the data to be copied.</span></span> <span data-ttu-id="ff010-110">Les données peuvent également provenir d'autres sources si elles peuvent être extraites d'un objet <xref:System.Data.IDataReader> ou <xref:System.Data.DataTable>.</span><span class="sxs-lookup"><span data-stu-id="ff010-110">Data can also come from other sources, if it can be retrieved from an <xref:System.Data.IDataReader> or <xref:System.Data.DataTable> object.</span></span>  
  
2. <span data-ttu-id="ff010-111">Se connecter au serveur de destination (à moins que vous souhaitiez **SqlBulkCopy** pour établir une connexion pour vous).</span><span class="sxs-lookup"><span data-stu-id="ff010-111">Connect to the destination server (unless you want **SqlBulkCopy** to establish a connection for you).</span></span>  
  
3. <span data-ttu-id="ff010-112">Créez un objet <xref:System.Data.SqlClient.SqlBulkCopy> en définissant toutes les propriétés nécessaires.</span><span class="sxs-lookup"><span data-stu-id="ff010-112">Create a <xref:System.Data.SqlClient.SqlBulkCopy> object, setting any necessary properties.</span></span>  
  
4. <span data-ttu-id="ff010-113">Définir le **DestinationTableName** propriété pour indiquer la table cible pour la majeure partie l’opération d’insertion.</span><span class="sxs-lookup"><span data-stu-id="ff010-113">Set the **DestinationTableName** property to indicate the target table for the bulk insert operation.</span></span>  
  
5. <span data-ttu-id="ff010-114">Appelez une de la **WriteToServer** méthodes.</span><span class="sxs-lookup"><span data-stu-id="ff010-114">Call one of the **WriteToServer** methods.</span></span>  
  
6. <span data-ttu-id="ff010-115">Si vous le souhaitez, mettez à jour des propriétés et appelez **WriteToServer** si nécessaire.</span><span class="sxs-lookup"><span data-stu-id="ff010-115">Optionally, update properties and call **WriteToServer** again as necessary.</span></span>  
  
7. <span data-ttu-id="ff010-116">Appelez <xref:System.Data.SqlClient.SqlBulkCopy.Close%2A> ou enveloppez les opérations de copie en bloc dans une instruction `Using`.</span><span class="sxs-lookup"><span data-stu-id="ff010-116">Call <xref:System.Data.SqlClient.SqlBulkCopy.Close%2A>, or wrap the bulk copy operations within a `Using` statement.</span></span>  
  
> [!CAUTION]
>  <span data-ttu-id="ff010-117">Il est recommandé que les types de données des colonnes source et cible correspondent.</span><span class="sxs-lookup"><span data-stu-id="ff010-117">We recommend that the source and target column data types match.</span></span> <span data-ttu-id="ff010-118">Si les types de données ne correspondent pas, **SqlBulkCopy** tente de convertir chaque valeur source du type de données cible, en utilisant les règles employées par <xref:System.Data.SqlClient.SqlParameter.Value%2A>.</span><span class="sxs-lookup"><span data-stu-id="ff010-118">If the data types do not match, **SqlBulkCopy** attempts to convert each source value to the target data type, using the rules employed by <xref:System.Data.SqlClient.SqlParameter.Value%2A>.</span></span> <span data-ttu-id="ff010-119">Les conversions peuvent affecter les performances et générer des erreurs inattendues.</span><span class="sxs-lookup"><span data-stu-id="ff010-119">Conversions can affect performance, and also can result in unexpected errors.</span></span> <span data-ttu-id="ff010-120">Par exemple, un type de données `Double` peut généralement être converti en un type de données `Decimal`, mais pas toujours.</span><span class="sxs-lookup"><span data-stu-id="ff010-120">For example, a `Double` data type can be converted to a `Decimal` data type most of the time, but not always.</span></span>  
  
## <a name="example"></a><span data-ttu-id="ff010-121">Exemple</span><span class="sxs-lookup"><span data-stu-id="ff010-121">Example</span></span>  
 <span data-ttu-id="ff010-122">L'application console suivante montre comment charger des données à l'aide de la classe <xref:System.Data.SqlClient.SqlBulkCopy>.</span><span class="sxs-lookup"><span data-stu-id="ff010-122">The following console application demonstrates how to load data using the <xref:System.Data.SqlClient.SqlBulkCopy> class.</span></span> <span data-ttu-id="ff010-123">Dans cet exemple, un <xref:System.Data.SqlClient.SqlDataReader> est utilisé pour copier des données à partir de la **Production.Product** table dans SQL Server **AdventureWorks** base de données vers une table semblable dans la même base de données.</span><span class="sxs-lookup"><span data-stu-id="ff010-123">In this example, a <xref:System.Data.SqlClient.SqlDataReader> is used to copy data from the **Production.Product** table in the SQL Server **AdventureWorks** database to a similar table in the same database.</span></span>  
  
> [!IMPORTANT]
>  <span data-ttu-id="ff010-124">Cet exemple ne s’exécutera pas, sauf si vous avez créé les tables de travail comme décrit dans [exemple de configuration de copie en bloc](../../../../../docs/framework/data/adonet/sql/bulk-copy-example-setup.md).</span><span class="sxs-lookup"><span data-stu-id="ff010-124">This sample will not run unless you have created the work tables as described in [Bulk Copy Example Setup](../../../../../docs/framework/data/adonet/sql/bulk-copy-example-setup.md).</span></span> <span data-ttu-id="ff010-125">Ce code est fourni pour illustrer la syntaxe pour l’utilisation de **SqlBulkCopy** uniquement.</span><span class="sxs-lookup"><span data-stu-id="ff010-125">This code is provided to demonstrate the syntax for using **SqlBulkCopy** only.</span></span> <span data-ttu-id="ff010-126">Si les tables sources et de destination se trouvent dans la même instance SQL Server, il est plus facile et plus rapide d'utiliser une instruction Transact-SQL `INSERT … SELECT` pour copier les données.</span><span class="sxs-lookup"><span data-stu-id="ff010-126">If the source and destination tables are located in the same SQL Server instance, it is easier and faster to use a Transact-SQL `INSERT … SELECT` statement to copy the data.</span></span>  
  
 [!code-csharp[DataWorks BulkCopy.Single#1](../../../../../samples/snippets/csharp/VS_Snippets_ADO.NET/DataWorks BulkCopy.Single/CS/source.cs#1)]
 [!code-vb[DataWorks BulkCopy.Single#1](../../../../../samples/snippets/visualbasic/VS_Snippets_ADO.NET/DataWorks BulkCopy.Single/VB/source.vb#1)]  
  
## <a name="performing-a-bulk-copy-operation-using-transact-sql-and-the-command-class"></a><span data-ttu-id="ff010-127">Exécution d'une opération de copie en bloc à l'aide de Transact-SQL et de la classe Command</span><span class="sxs-lookup"><span data-stu-id="ff010-127">Performing a Bulk Copy Operation Using Transact-SQL and the Command Class</span></span>  
 <span data-ttu-id="ff010-128">L'exemple suivant illustre la manière d'utiliser la méthode <xref:System.Data.SqlClient.SqlCommand.ExecuteNonQuery%2A> pour exécuter l'instruction BULK INSERT.</span><span class="sxs-lookup"><span data-stu-id="ff010-128">The following example illustrates how to use the <xref:System.Data.SqlClient.SqlCommand.ExecuteNonQuery%2A> method to execute the BULK INSERT statement.</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="ff010-129">Le chemin d'accès au fichier de la source de données est relatif par rapport au serveur.</span><span class="sxs-lookup"><span data-stu-id="ff010-129">The file path for the data source is relative to the server.</span></span> <span data-ttu-id="ff010-130">Le processus serveur doit avoir accès à ce chemin d'accès pour que l'opération de copie en bloc réussisse.</span><span class="sxs-lookup"><span data-stu-id="ff010-130">The server process must have access to that path in order for the bulk copy operation to succeed.</span></span>  
  
```vb  
Using connection As SqlConnection = New SqlConnection(connectionString)  
Dim queryString As String = _  
    "BULK INSERT Northwind.dbo.[Order Details] FROM " & _  
    "'f:\mydata\data.tbl' WITH (FORMATFILE='f:\mydata\data.fmt' )"  
connection.Open()  
SqlCommand command = New SqlCommand(queryString, connection);  
  
command.ExecuteNonQuery()  
End Using  
```  
  
```csharp  
using (SqlConnection connection = New SqlConnection(connectionString))  
{  
string queryString =  "BULK INSERT Northwind.dbo.[Order Details] " +  
    "FROM 'f:\mydata\data.tbl' " +  
    "WITH ( FORMATFILE='f:\mydata\data.fmt' )";  
connection.Open();  
SqlCommand command = new SqlCommand(queryString, connection);  
  
command.ExecuteNonQuery();  
}  
```  
  
## <a name="see-also"></a><span data-ttu-id="ff010-131">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ff010-131">See also</span></span>

- [<span data-ttu-id="ff010-132">Opérations de copie en bloc dans SQL Server</span><span class="sxs-lookup"><span data-stu-id="ff010-132">Bulk Copy Operations in SQL Server</span></span>](../../../../../docs/framework/data/adonet/sql/bulk-copy-operations-in-sql-server.md)
- [<span data-ttu-id="ff010-133">Fournisseurs managés ADO.NET et centre de développement DataSet</span><span class="sxs-lookup"><span data-stu-id="ff010-133">ADO.NET Managed Providers and DataSet Developer Center</span></span>](https://go.microsoft.com/fwlink/?LinkId=217917)
