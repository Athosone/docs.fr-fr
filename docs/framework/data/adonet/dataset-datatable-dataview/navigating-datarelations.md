---
title: Parcours des DataRelations
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
ms.assetid: e5e673f4-9b44-45ae-aaea-c504d1cc5d3e
ms.openlocfilehash: f4dfccad23bf5d15f5cbd0a33e76a136417e13ea
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61607257"
---
# <a name="navigating-datarelations"></a><span data-ttu-id="3dafd-102">Parcours des DataRelations</span><span class="sxs-lookup"><span data-stu-id="3dafd-102">Navigating DataRelations</span></span>
<span data-ttu-id="3dafd-103">L'une des principales fonctions d'un objet <xref:System.Data.DataRelation> est de permettre de passer d'un objet <xref:System.Data.DataTable> à un autre à l'intérieur d'un objet <xref:System.Data.DataSet>.</span><span class="sxs-lookup"><span data-stu-id="3dafd-103">One of the primary functions of a <xref:System.Data.DataRelation> is to allow navigation from one <xref:System.Data.DataTable> to another within a <xref:System.Data.DataSet>.</span></span> <span data-ttu-id="3dafd-104">Cela vous permet de récupérer tous les connexe <xref:System.Data.DataRow> les objets **DataTable** lorsqu’un **DataRow** à partir d’un connexes **DataTable**.</span><span class="sxs-lookup"><span data-stu-id="3dafd-104">This allows you to retrieve all the related <xref:System.Data.DataRow> objects in one **DataTable** when given a single **DataRow** from a related **DataTable**.</span></span> <span data-ttu-id="3dafd-105">Par exemple, après avoir établi un **DataRelation** entre une table de clients et une table de commandes, vous pouvez récupérer toutes les lignes de commande pour une ligne de client spécifique à l’aide **GetChildRows**.</span><span class="sxs-lookup"><span data-stu-id="3dafd-105">For example, after establishing a **DataRelation** between a table of customers and a table of orders, you can retrieve all the order rows for a particular customer row using **GetChildRows**.</span></span>  
  
 <span data-ttu-id="3dafd-106">L’exemple de code suivant crée un **DataRelation** entre le **clients** table et le **commandes** table d’un **DataSet** et retourne toutes les commandes pour chaque client.</span><span class="sxs-lookup"><span data-stu-id="3dafd-106">The following code example creates a **DataRelation** between the **Customers** table and the **Orders** table of a **DataSet** and returns all the orders for each customer.</span></span>  
  
 [!code-csharp[DataWorks Data.DataTableRelation#1](../../../../../samples/snippets/csharp/VS_Snippets_ADO.NET/DataWorks Data.DataTableRelation/CS/source.cs#1)]
 [!code-vb[DataWorks Data.DataTableRelation#1](../../../../../samples/snippets/visualbasic/VS_Snippets_ADO.NET/DataWorks Data.DataTableRelation/VB/source.vb#1)]  
  
 <span data-ttu-id="3dafd-107">L'exemple suivant s'appuie sur le précédent, en créant des relations entre quatre tables et en explorant ces relations.</span><span class="sxs-lookup"><span data-stu-id="3dafd-107">The next example builds on the preceding example, relating four tables together and navigating those relationships.</span></span> <span data-ttu-id="3dafd-108">Comme dans l’exemple précédent, **CustomerID** se rapporte la **clients** de la table vers le **commandes** table.</span><span class="sxs-lookup"><span data-stu-id="3dafd-108">As in the previous example, **CustomerID** relates the **Customers** table to the **Orders** table.</span></span> <span data-ttu-id="3dafd-109">Pour chaque client dans le **clients** table, toutes les lignes enfants de la **commandes** table sont déterminées, afin de retourner le nombre de commandes passées par un client et leurs **OrderID** valeurs.</span><span class="sxs-lookup"><span data-stu-id="3dafd-109">For each customer in the **Customers** table, all the child rows in the **Orders** table are determined, in order to return the number of orders a particular customer has and their **OrderID** values.</span></span>  
  
 <span data-ttu-id="3dafd-110">L’exemple développé retourne également les valeurs à partir de la **OrderDetails** et **produits** tables.</span><span class="sxs-lookup"><span data-stu-id="3dafd-110">The expanded example also returns the values from the **OrderDetails** and **Products** tables.</span></span> <span data-ttu-id="3dafd-111">Le **commandes** table est associée à la **OrderDetails** à l’aide de la table **OrderID** pour déterminer, pour chaque commande client, de quels produits et quantités commandées.</span><span class="sxs-lookup"><span data-stu-id="3dafd-111">The **Orders** table is related to the **OrderDetails** table using **OrderID** to determine, for each customer order, what products and quantities were ordered.</span></span> <span data-ttu-id="3dafd-112">Étant donné que le **OrderDetails** table contient uniquement le **ProductID** d’un produit commandé, **OrderDetails** est liée à **produits** à l’aide de **ProductID** afin de retourner le **ProductName**.</span><span class="sxs-lookup"><span data-stu-id="3dafd-112">Because the **OrderDetails** table only contains the **ProductID** of an ordered product, **OrderDetails** is related to **Products** using **ProductID** in order to return the **ProductName**.</span></span> <span data-ttu-id="3dafd-113">Dans cette relation, le **produits** est la table parente et la **Order Details** table est l’enfant.</span><span class="sxs-lookup"><span data-stu-id="3dafd-113">In this relation, the **Products** table is the parent and the **Order Details** table is the child.</span></span> <span data-ttu-id="3dafd-114">Par conséquent, lors de l’itération via la **OrderDetails** table, **GetParentRow** est appelée pour extraire la **ProductName** valeur.</span><span class="sxs-lookup"><span data-stu-id="3dafd-114">As a result, when iterating through the **OrderDetails** table, **GetParentRow** is called to retrieve the related **ProductName** value.</span></span>  
  
 <span data-ttu-id="3dafd-115">Notez que lorsque le **DataRelation** est créé pour le **clients** et **commandes** tables, aucune valeur n’est spécifiée pour le **createConstraints**indicateur (la valeur par défaut est **true**).</span><span class="sxs-lookup"><span data-stu-id="3dafd-115">Notice that when the **DataRelation** is created for the **Customers** and **Orders** tables, no value is specified for the **createConstraints** flag (the default is **true**).</span></span> <span data-ttu-id="3dafd-116">Cela suppose que toutes les les lignes dans le **commandes** table ont une **CustomerID** valeur qui existe dans le parent **clients** table.</span><span class="sxs-lookup"><span data-stu-id="3dafd-116">This assumes that all the rows in the **Orders** table have a **CustomerID** value that exists in the parent **Customers** table.</span></span> <span data-ttu-id="3dafd-117">Si un **CustomerID** existe dans le **commandes** table qui n’existe pas dans le **clients** table, un <xref:System.Data.ForeignKeyConstraint> provoque une exception levée.</span><span class="sxs-lookup"><span data-stu-id="3dafd-117">If a **CustomerID** exists in the **Orders** table that does not exist in the **Customers** table, a <xref:System.Data.ForeignKeyConstraint> causes an exception to be thrown.</span></span>  
  
 <span data-ttu-id="3dafd-118">Lorsque la colonne enfant peut contenir des valeurs de la colonne parent ne contient-elle pas, définissez le **createConstraints** indicateur **false** lors de l’ajout du **DataRelation**.</span><span class="sxs-lookup"><span data-stu-id="3dafd-118">When the child column might contain values that the parent column does not contain, set the **createConstraints** flag to **false** when adding the **DataRelation**.</span></span> <span data-ttu-id="3dafd-119">Dans l’exemple, le **createConstraints** indicateur a la valeur **false** pour le **DataRelation** entre le **commandes** table et le  **OrderDetails** table.</span><span class="sxs-lookup"><span data-stu-id="3dafd-119">In the example, the **createConstraints** flag is set to **false** for the **DataRelation** between the **Orders** table and the **OrderDetails** table.</span></span> <span data-ttu-id="3dafd-120">Cela permet à l’application retourner tous les enregistrements à partir de la **OrderDetails** table et uniquement un sous-ensemble d’enregistrements à partir de la **commandes** table sans générer une exception au moment de l’exécution.</span><span class="sxs-lookup"><span data-stu-id="3dafd-120">This enables the application to return all the records from the **OrderDetails** table and only a subset of records from the **Orders** table without generating a run-time exception.</span></span> <span data-ttu-id="3dafd-121">La sortie de l’exemple développé se présente comme suit.</span><span class="sxs-lookup"><span data-stu-id="3dafd-121">The expanded sample generates output in the following format.</span></span>  
  
```  
Customer ID: NORTS  
  Order ID: 10517  
        Order Date: 4/24/1997 12:00:00 AM  
           Product: Filo Mix  
          Quantity: 6  
           Product: Raclette Courdavault  
          Quantity: 4  
           Product: Outback Lager  
          Quantity: 6  
  Order ID: 11057  
        Order Date: 4/29/1998 12:00:00 AM  
           Product: Outback Lager  
          Quantity: 3  
```  
  
 <span data-ttu-id="3dafd-122">L’exemple de code suivant est un exemple développé où les valeurs à partir de la **OrderDetails** et **produits** les tables sont retournées, avec uniquement un sous-ensemble des enregistrements dans la **commandes**table qui est retournée.</span><span class="sxs-lookup"><span data-stu-id="3dafd-122">The following code example is an expanded sample where the values from the **OrderDetails** and **Products** tables are returned, with only a subset of the records in the **Orders** table being returned.</span></span>  
  
 [!code-csharp[DataWorks Data.DataTableNavigation#1](../../../../../samples/snippets/csharp/VS_Snippets_ADO.NET/DataWorks Data.DataTableNavigation/CS/source.cs#1)]
 [!code-vb[DataWorks Data.DataTableNavigation#1](../../../../../samples/snippets/visualbasic/VS_Snippets_ADO.NET/DataWorks Data.DataTableNavigation/VB/source.vb#1)]  
  
## <a name="see-also"></a><span data-ttu-id="3dafd-123">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="3dafd-123">See also</span></span>

- [<span data-ttu-id="3dafd-124">DataSets, DataTables et DataViews</span><span class="sxs-lookup"><span data-stu-id="3dafd-124">DataSets, DataTables, and DataViews</span></span>](../../../../../docs/framework/data/adonet/dataset-datatable-dataview/index.md)
- [<span data-ttu-id="3dafd-125">Fournisseurs managés ADO.NET et centre de développement DataSet</span><span class="sxs-lookup"><span data-stu-id="3dafd-125">ADO.NET Managed Providers and DataSet Developer Center</span></span>](https://go.microsoft.com/fwlink/?LinkId=217917)
