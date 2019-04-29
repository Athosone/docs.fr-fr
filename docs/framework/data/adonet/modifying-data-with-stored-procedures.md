---
title: Modification des données avec les procédures stockées
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
ms.assetid: 7d8e9a46-1af6-4a02-bf61-969d77ae07e0
ms.openlocfilehash: 7dfd4f07ba0a0473975d87c7cd166635473344a6
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61772097"
---
# <a name="modifying-data-with-stored-procedures"></a><span data-ttu-id="b1ee1-102">Modification des données avec les procédures stockées</span><span class="sxs-lookup"><span data-stu-id="b1ee1-102">Modifying Data with Stored Procedures</span></span>
<span data-ttu-id="b1ee1-103">Les procédures stockées peuvent accepter des données en tant que paramètres d'entrée et retourner des données en tant que paramètres de sortie, jeux de résultats et valeurs de retour.</span><span class="sxs-lookup"><span data-stu-id="b1ee1-103">Stored procedures can accept data as input parameters and can return data as output parameters, result sets, or return values.</span></span> <span data-ttu-id="b1ee1-104">L'exemple ci-dessous montre comment ADO.NET envoie et reçoit des paramètres d'entrée, des paramètres de sortie et des valeurs de retour.</span><span class="sxs-lookup"><span data-stu-id="b1ee1-104">The sample below illustrates how ADO.NET sends and receives input parameters, output parameters, and return values.</span></span> <span data-ttu-id="b1ee1-105">L'exemple insère un nouvel enregistrement dans une table où la colonne de clé primaire est une colonne d'identité dans une base de données SQL Server.</span><span class="sxs-lookup"><span data-stu-id="b1ee1-105">The example inserts a new record into a table where the primary key column is an identity column in a SQL Server database.</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="b1ee1-106">Si vous utilisez des procédures stockées SQL Server pour modifier ou supprimer des données à l'aide de <xref:System.Data.SqlClient.SqlDataAdapter>, assurez-vous que vous n'utilisez pas SET NOCOUNT ON dans la définition de procédure stockée.</span><span class="sxs-lookup"><span data-stu-id="b1ee1-106">If you are using SQL Server stored procedures to edit or delete data using a <xref:System.Data.SqlClient.SqlDataAdapter>, make sure that you do not use SET NOCOUNT ON in the stored procedure definition.</span></span> <span data-ttu-id="b1ee1-107">En effet, le nombre de lignes affectées retourné serait alors la valeur zéro, ce que `DataAdapter` interprète comme un conflit d'accès concurrentiel.</span><span class="sxs-lookup"><span data-stu-id="b1ee1-107">This causes the rows affected count returned to be zero, which the `DataAdapter` interprets as a concurrency conflict.</span></span> <span data-ttu-id="b1ee1-108">Dans ce cas, l'exception <xref:System.Data.DBConcurrencyException> est levée.</span><span class="sxs-lookup"><span data-stu-id="b1ee1-108">In this event, a <xref:System.Data.DBConcurrencyException> will be thrown.</span></span>  
  
## <a name="example"></a><span data-ttu-id="b1ee1-109">Exemple</span><span class="sxs-lookup"><span data-stu-id="b1ee1-109">Example</span></span>  
 <span data-ttu-id="b1ee1-110">L’exemple utilise la procédure stockée suivante pour insérer une nouvelle catégorie dans le **Northwind** **catégories** table.</span><span class="sxs-lookup"><span data-stu-id="b1ee1-110">The sample uses the following stored procedure to insert a new category into the **Northwind** **Categories** table.</span></span> <span data-ttu-id="b1ee1-111">La procédure stockée prend la valeur de la **CategoryName** colonne en tant que paramètre d’entrée et utilise le SCOPE_IDENTITY() à récupérer la nouvelle valeur du champ d’identité, la fonction **CategoryID**et le retourner dans un paramètre output.</span><span class="sxs-lookup"><span data-stu-id="b1ee1-111">The stored procedure takes the value in the **CategoryName** column as an input parameter and uses the SCOPE_IDENTITY() function to retrieve the new value of the identity field, **CategoryID**, and return it in an output parameter.</span></span> <span data-ttu-id="b1ee1-112">L’instruction RETURN utilise la @@ROWCOUNT fonction pour retourner le nombre de lignes insérées.</span><span class="sxs-lookup"><span data-stu-id="b1ee1-112">The RETURN statement uses the @@ROWCOUNT function to return the number of rows inserted.</span></span>  
  
```sql
CREATE PROCEDURE dbo.InsertCategory  
  @CategoryName nvarchar(15),  
  @Identity int OUT  
AS  
INSERT INTO Categories (CategoryName) VALUES(@CategoryName)  
SET @Identity = SCOPE_IDENTITY()  
RETURN @@ROWCOUNT  
```  
  
 <span data-ttu-id="b1ee1-113">L'exemple de code suivant utilise la procédure stockée `InsertCategory` présentée ci-dessus comme source pour <xref:System.Data.SqlClient.SqlDataAdapter.InsertCommand%2A> de <xref:System.Data.SqlClient.SqlDataAdapter>.</span><span class="sxs-lookup"><span data-stu-id="b1ee1-113">The following code example uses the `InsertCategory` stored procedure shown above as the source for the <xref:System.Data.SqlClient.SqlDataAdapter.InsertCommand%2A> of the <xref:System.Data.SqlClient.SqlDataAdapter>.</span></span> <span data-ttu-id="b1ee1-114">Le paramètre de sortie `@Identity` se reflète dans <xref:System.Data.DataSet> après que l'enregistrement a été inséré dans la base de données lors de l'appel de la méthode `Update` de <xref:System.Data.SqlClient.SqlDataAdapter>.</span><span class="sxs-lookup"><span data-stu-id="b1ee1-114">The `@Identity` output parameter will be reflected in the <xref:System.Data.DataSet> after the record has been inserted into the database when the `Update` method of the <xref:System.Data.SqlClient.SqlDataAdapter> is called.</span></span> <span data-ttu-id="b1ee1-115">Le code récupère également la valeur de retour.</span><span class="sxs-lookup"><span data-stu-id="b1ee1-115">The code also retrieves the return value.</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="b1ee1-116">Lorsque vous utilisez le <xref:System.Data.OleDb.OleDbDataAdapter>, vous devez spécifier des paramètres avec un <xref:System.Data.ParameterDirection> de **ReturnValue** avant les autres paramètres.</span><span class="sxs-lookup"><span data-stu-id="b1ee1-116">When using the <xref:System.Data.OleDb.OleDbDataAdapter>, you must specify parameters with a <xref:System.Data.ParameterDirection> of **ReturnValue** before the other parameters.</span></span>  
  
 [!code-csharp[DataWorks SqlClient.SprocIdentityReturn#1](../../../../samples/snippets/csharp/VS_Snippets_ADO.NET/DataWorks SqlClient.SprocIdentityReturn/CS/source.cs#1)]
 [!code-vb[DataWorks SqlClient.SprocIdentityReturn#1](../../../../samples/snippets/visualbasic/VS_Snippets_ADO.NET/DataWorks SqlClient.SprocIdentityReturn/VB/source.vb#1)]  
  
## <a name="see-also"></a><span data-ttu-id="b1ee1-117">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b1ee1-117">See also</span></span>

- [<span data-ttu-id="b1ee1-118">Extraction et modification de données dans ADO.NET</span><span class="sxs-lookup"><span data-stu-id="b1ee1-118">Retrieving and Modifying Data in ADO.NET</span></span>](../../../../docs/framework/data/adonet/retrieving-and-modifying-data.md)
- [<span data-ttu-id="b1ee1-119">DataAdapters et DataReaders</span><span class="sxs-lookup"><span data-stu-id="b1ee1-119">DataAdapters and DataReaders</span></span>](../../../../docs/framework/data/adonet/dataadapters-and-datareaders.md)
- [<span data-ttu-id="b1ee1-120">Exécution d’une commande</span><span class="sxs-lookup"><span data-stu-id="b1ee1-120">Executing a Command</span></span>](../../../../docs/framework/data/adonet/executing-a-command.md)
- [<span data-ttu-id="b1ee1-121">Fournisseurs managés ADO.NET et centre de développement DataSet</span><span class="sxs-lookup"><span data-stu-id="b1ee1-121">ADO.NET Managed Providers and DataSet Developer Center</span></span>](https://go.microsoft.com/fwlink/?LinkId=217917)
