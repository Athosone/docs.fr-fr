---
title: Pagination à travers un résultat de requête
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
ms.assetid: fa360c46-e5f8-411e-a711-46997771133d
ms.openlocfilehash: 023efcc15d7080afc1583f4ad8984e152b86cf23
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59140320"
---
# <a name="paging-through-a-query-result"></a>Pagination à travers un résultat de requête
Ce mode d'affichage consiste à retourner les résultats d'une requête sous forme de sous-ensembles, plus petits, de données, aussi appelés pages. Cette façon de procéder est courante lorsqu'il s'agit de présenter à l'utilisateur un affichage des résultats par petits segments, plus faciles à gérer.  
  
 Le **DataAdapter** propose une fonctionnalité permettant de retourner uniquement une page de données, via les surcharges de la **remplir** (méthode). Toutefois, cela peut être le meilleur choix pour la pagination des résultats de requête de grande taille, car, bien que le **DataAdapter** remplit la cible <xref:System.Data.DataTable> ou <xref:System.Data.DataSet> avec uniquement les enregistrements demandés, les ressources pour retourner le intégralité de la requête sont toujours utilisés. Pour retourner une page de données provenant d'une source de donnée sans solliciter les ressources requises pour retourner l'intégralité de la requête, spécifiez des critères supplémentaires pour votre requête afin de limiter le nombre de lignes retournées à celles qui sont requises.  
  
 Pour utiliser le **remplir** méthode pour retourner une page de données, spécifiez un **startRecord** paramètre, pour le premier enregistrement dans la page de données et un **maxRecords** paramètre, le nombre de enregistrements dans la page de données.  
  
 L’exemple de code suivant montre comment utiliser le **remplir** méthode pour retourner la première page de résultats d’une requête dont la taille est de cinq enregistrements.  
  
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
  
 Dans l’exemple précédent, le **DataSet** ne reçoit que cinq enregistrements, mais l’intégralité de **commandes** table est retournée. Pour remplir le **DataSet** avec ces cinq mêmes enregistrements, mais ne retournant que cinq enregistrements, utilisez la partie supérieure la clause WHERE dans votre instruction SQL, comme dans l’exemple de code suivant.  
  
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
  
 Notez que, lorsque vous choisissez ce mode d'affichage par pages des résultats d'une requête, vous devez conserver l'identificateur unique en fonction duquel les lignes sont organisées, afin de passer cet identificateur unique à la commande pour retourner la page d'enregistrements suivante, comme le montre l'exemple de code ci-après.  
  
```vb  
Dim lastRecord As String = _  
  dataSet.Tables("Orders").Rows(pageSize - 1)("OrderID").ToString()  
```  
  
```csharp  
string lastRecord =   
  dataSet.Tables["Orders"].Rows[pageSize - 1]["OrderID"].ToString();  
```  
  
 Pour retourner la page suivante des enregistrements à l’aide de la surcharge de la **remplir** méthode qui prend le **startRecord** et **maxRecords** paramètres, incrémentez l’index en cours d’enregistrement par la taille de page et le remplissage de la table. N’oubliez pas que le serveur de base de données retourne les résultats de la requête entière, bien qu’une seule page d’enregistrements est ajoutée à la **DataSet**. Dans l'exemple de code suivant, les lignes de la table sont vidées de leur contenu avant de recevoir la page de données suivante. Vous avez la possibilité de conserver dans un cache local un certain nombre de lignes retournées afin de limiter les sollicitations du serveur de base de données.  
  
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
  
 Pour retourner la page d'enregistrements suivante sans que le serveur de base de données ne retourne l'intégralité de la requête, spécifiez des critères restrictifs pour l'instruction SELECT. Parce que l'exemple précédent conservait le dernier enregistrement retourné, vous pouvez l'utiliser dans la clause WHERE afin de spécifier le point de départ de la requête, comme le montre l'exemple de code suivant.  
  
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
  
## <a name="see-also"></a>Voir aussi

- [DataAdapters et DataReaders](../../../../docs/framework/data/adonet/dataadapters-and-datareaders.md)
- [Fournisseurs managés ADO.NET et centre de développement DataSet](https://go.microsoft.com/fwlink/?LinkId=217917)
