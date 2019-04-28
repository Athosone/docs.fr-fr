---
title: Pagination à travers un résultat de requête
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
ms.assetid: fa360c46-e5f8-411e-a711-46997771133d
ms.openlocfilehash: 023efcc15d7080afc1583f4ad8984e152b86cf23
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61878382"
---
# <a name="paging-through-a-query-result"></a><span data-ttu-id="906ed-102">Pagination à travers un résultat de requête</span><span class="sxs-lookup"><span data-stu-id="906ed-102">Paging Through a Query Result</span></span>
<span data-ttu-id="906ed-103">Ce mode d'affichage consiste à retourner les résultats d'une requête sous forme de sous-ensembles, plus petits, de données, aussi appelés pages.</span><span class="sxs-lookup"><span data-stu-id="906ed-103">Paging through a query result is the process of returning the results of a query in smaller subsets of data, or pages.</span></span> <span data-ttu-id="906ed-104">Cette façon de procéder est courante lorsqu'il s'agit de présenter à l'utilisateur un affichage des résultats par petits segments, plus faciles à gérer.</span><span class="sxs-lookup"><span data-stu-id="906ed-104">This is a common practice for displaying results to a user in small, easy-to-manage chunks.</span></span>  
  
 <span data-ttu-id="906ed-105">Le **DataAdapter** propose une fonctionnalité permettant de retourner uniquement une page de données, via les surcharges de la **remplir** (méthode).</span><span class="sxs-lookup"><span data-stu-id="906ed-105">The **DataAdapter** provides a facility for returning only a page of data, through overloads of the **Fill** method.</span></span> <span data-ttu-id="906ed-106">Toutefois, cela peut être le meilleur choix pour la pagination des résultats de requête de grande taille, car, bien que le **DataAdapter** remplit la cible <xref:System.Data.DataTable> ou <xref:System.Data.DataSet> avec uniquement les enregistrements demandés, les ressources pour retourner le intégralité de la requête sont toujours utilisés.</span><span class="sxs-lookup"><span data-stu-id="906ed-106">However, this might not be the best choice for paging through large query results because, although the **DataAdapter** fills the target <xref:System.Data.DataTable> or <xref:System.Data.DataSet> with only the requested records, the resources to return the entire query are still used.</span></span> <span data-ttu-id="906ed-107">Pour retourner une page de données provenant d'une source de donnée sans solliciter les ressources requises pour retourner l'intégralité de la requête, spécifiez des critères supplémentaires pour votre requête afin de limiter le nombre de lignes retournées à celles qui sont requises.</span><span class="sxs-lookup"><span data-stu-id="906ed-107">To return a page of data from a data source without using the resources to return the entire query, specify additional criteria for your query that reduce the rows returned to only those required.</span></span>  
  
 <span data-ttu-id="906ed-108">Pour utiliser le **remplir** méthode pour retourner une page de données, spécifiez un **startRecord** paramètre, pour le premier enregistrement dans la page de données et un **maxRecords** paramètre, le nombre de enregistrements dans la page de données.</span><span class="sxs-lookup"><span data-stu-id="906ed-108">To use the **Fill** method to return a page of data, specify a **startRecord** parameter, for the first record in the page of data, and a **maxRecords** parameter, for the number of records in the page of data.</span></span>  
  
 <span data-ttu-id="906ed-109">L’exemple de code suivant montre comment utiliser le **remplir** méthode pour retourner la première page de résultats d’une requête dont la taille est de cinq enregistrements.</span><span class="sxs-lookup"><span data-stu-id="906ed-109">The following code example shows how to use the **Fill** method to return the first page of a query result where the page size is five records.</span></span>  
  
```vb  
Dim currentIndex As Integer = 0  
Dim pageSize As Integer = 5  
  
Dim orderSQL As String = "SELECT * FROM dbo.Orders ORDER BY OrderID"  
' Assumes that connection is a valid SqlConnection object.  
Dim adapter As SqlDataAdapter = _  
  New SqlDataAdapter(orderSQL, connection)  
  
Dim dataSet As DataSet = New DataSet()  
adapter.Fill(dataSet, currentIndex, pageSize, "Orders")  
```  
  
```csharp  
int currentIndex = 0;  
int pageSize = 5;  
  
string orderSQL = "SELECT * FROM Orders ORDER BY OrderID";  
// Assumes that connection is a valid SqlConnection object.  
SqlDataAdapter adapter = new SqlDataAdapter(orderSQL, connection);  
  
DataSet dataSet = new DataSet();  
adapter.Fill(dataSet, currentIndex, pageSize, "Orders");  
```  
  
 <span data-ttu-id="906ed-110">Dans l’exemple précédent, le **DataSet** ne reçoit que cinq enregistrements, mais l’intégralité de **commandes** table est retournée.</span><span class="sxs-lookup"><span data-stu-id="906ed-110">In the previous example, the **DataSet** is only filled with five records, but the entire **Orders** table is returned.</span></span> <span data-ttu-id="906ed-111">Pour remplir le **DataSet** avec ces cinq mêmes enregistrements, mais ne retournant que cinq enregistrements, utilisez la partie supérieure la clause WHERE dans votre instruction SQL, comme dans l’exemple de code suivant.</span><span class="sxs-lookup"><span data-stu-id="906ed-111">To fill the **DataSet** with those same five records, but only return five records, use the TOP and WHERE clauses in your SQL statement, as in the following code example.</span></span>  
  
```vb  
Dim pageSize As Integer = 5  
  
Dim orderSQL As String = "SELECT TOP " & pageSize & _  
  " * FROM Orders ORDER BY OrderID"  
Dim adapter As SqlDataAdapter = _  
  New SqlDataAdapter(orderSQL, connection)  
  
Dim dataSet As DataSet = New DataSet()  
adapter.Fill(dataSet, "Orders")   
```  
  
```csharp  
int pageSize = 5;  
  
string orderSQL = "SELECT TOP " + pageSize +   
  " * FROM Orders ORDER BY OrderID";  
SqlDataAdapter adapter = new SqlDataAdapter(orderSQL, connection);  
  
DataSet dataSet = new DataSet();  
adapter.Fill(dataSet, "Orders");  
```  
  
 <span data-ttu-id="906ed-112">Notez que, lorsque vous choisissez ce mode d'affichage par pages des résultats d'une requête, vous devez conserver l'identificateur unique en fonction duquel les lignes sont organisées, afin de passer cet identificateur unique à la commande pour retourner la page d'enregistrements suivante, comme le montre l'exemple de code ci-après.</span><span class="sxs-lookup"><span data-stu-id="906ed-112">Note that, when paging through the query results in this way, you must preserve the unique identifier that orders the rows, in order to pass the unique ID to the command to return the next page of records, as shown in the following code example.</span></span>  
  
```vb  
Dim lastRecord As String = _  
  dataSet.Tables("Orders").Rows(pageSize - 1)("OrderID").ToString()  
```  
  
```csharp  
string lastRecord =   
  dataSet.Tables["Orders"].Rows[pageSize - 1]["OrderID"].ToString();  
```  
  
 <span data-ttu-id="906ed-113">Pour retourner la page suivante des enregistrements à l’aide de la surcharge de la **remplir** méthode qui prend le **startRecord** et **maxRecords** paramètres, incrémentez l’index en cours d’enregistrement par la taille de page et le remplissage de la table.</span><span class="sxs-lookup"><span data-stu-id="906ed-113">To return the next page of records using the overload of the **Fill** method that takes the **startRecord** and **maxRecords** parameters, increment the current record index by the page size and fill the table.</span></span> <span data-ttu-id="906ed-114">N’oubliez pas que le serveur de base de données retourne les résultats de la requête entière, bien qu’une seule page d’enregistrements est ajoutée à la **DataSet**.</span><span class="sxs-lookup"><span data-stu-id="906ed-114">Remember that the database server returns the entire query results even though only one page of records is added to the **DataSet**.</span></span> <span data-ttu-id="906ed-115">Dans l'exemple de code suivant, les lignes de la table sont vidées de leur contenu avant de recevoir la page de données suivante.</span><span class="sxs-lookup"><span data-stu-id="906ed-115">In the following code example, the table rows are cleared before they are filled with the next page of data.</span></span> <span data-ttu-id="906ed-116">Vous avez la possibilité de conserver dans un cache local un certain nombre de lignes retournées afin de limiter les sollicitations du serveur de base de données.</span><span class="sxs-lookup"><span data-stu-id="906ed-116">You might want to preserve a certain number of returned rows in a local cache to reduce trips to the database server.</span></span>  
  
```vb  
currentIndex = currentIndex + pageSize  
  
dataSet.Tables("Orders").Rows.Clear()  
  
adapter.Fill(dataSet, currentIndex, pageSize, "Orders")  
```  
  
```csharp  
currentIndex += pageSize;  
  
dataSet.Tables["Orders"].Rows.Clear();  
  
adapter.Fill(dataSet, currentIndex, pageSize, "Orders");  
```  
  
 <span data-ttu-id="906ed-117">Pour retourner la page d'enregistrements suivante sans que le serveur de base de données ne retourne l'intégralité de la requête, spécifiez des critères restrictifs pour l'instruction SELECT.</span><span class="sxs-lookup"><span data-stu-id="906ed-117">To return the next page of records without having the database server return the entire query, specify restrictive criteria to the SELECT statement.</span></span> <span data-ttu-id="906ed-118">Parce que l'exemple précédent conservait le dernier enregistrement retourné, vous pouvez l'utiliser dans la clause WHERE afin de spécifier le point de départ de la requête, comme le montre l'exemple de code suivant.</span><span class="sxs-lookup"><span data-stu-id="906ed-118">Because the preceding example preserved the last record returned, you can use it in the WHERE clause to specify a starting point for the query, as shown in the following code example.</span></span>  
  
```vb  
orderSQL = "SELECT TOP " & pageSize & _  
  " * FROM Orders WHERE OrderID > " & lastRecord & " ORDER BY OrderID"  
adapter.SelectCommand.CommandText = orderSQL  
  
dataSet.Tables("Orders").Rows.Clear()  
  
adapter.Fill(dataSet, "Orders")  
```  
  
```csharp  
orderSQL = "SELECT TOP " + pageSize +   
  " * FROM Orders WHERE OrderID > " + lastRecord + " ORDER BY OrderID";  
adapter.SelectCommand.CommandText = orderSQL;  
  
dataSet.Tables["Orders"].Rows.Clear();  
  
adapter.Fill(dataSet, "Orders");  
```  
  
## <a name="see-also"></a><span data-ttu-id="906ed-119">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="906ed-119">See also</span></span>

- [<span data-ttu-id="906ed-120">DataAdapters et DataReaders</span><span class="sxs-lookup"><span data-stu-id="906ed-120">DataAdapters and DataReaders</span></span>](../../../../docs/framework/data/adonet/dataadapters-and-datareaders.md)
- [<span data-ttu-id="906ed-121">Fournisseurs managés ADO.NET et centre de développement DataSet</span><span class="sxs-lookup"><span data-stu-id="906ed-121">ADO.NET Managed Providers and DataSet Developer Center</span></span>](https://go.microsoft.com/fwlink/?LinkId=217917)
