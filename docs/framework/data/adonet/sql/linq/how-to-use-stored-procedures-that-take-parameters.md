---
title: 'Procédure : Utiliser des procédures stockées qui prennent des paramètres'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
ms.assetid: b935fd84-cb9c-4205-8c48-658d5db2ec93
ms.openlocfilehash: 8dd463c895efcddfe288fe1dc8571981872d9d80
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59181764"
---
# <a name="how-to-use-stored-procedures-that-take-parameters"></a><span data-ttu-id="8c16b-102">Procédure : Utiliser des procédures stockées qui prennent des paramètres</span><span class="sxs-lookup"><span data-stu-id="8c16b-102">How to: Use Stored Procedures that Take Parameters</span></span>
[!INCLUDE[vbtecdlinq](../../../../../../includes/vbtecdlinq-md.md)] <span data-ttu-id="8c16b-103">mappe des paramètres de sortie à des paramètres de référence et, pour les types valeur, déclare le paramètre comme Nullable.</span><span class="sxs-lookup"><span data-stu-id="8c16b-103">maps output parameters to reference parameters, and for value types declares the parameter as nullable.</span></span>  
  
 <span data-ttu-id="8c16b-104">Pour obtenir un exemple montrant comment utiliser un paramètre d’entrée dans une requête qui retourne un ensemble de lignes, consultez [Comment : Retourner des ensembles de lignes](../../../../../../docs/framework/data/adonet/sql/linq/how-to-return-rowsets.md).</span><span class="sxs-lookup"><span data-stu-id="8c16b-104">For an example of how to use an input parameter in a query that returns a rowset, see [How to: Return Rowsets](../../../../../../docs/framework/data/adonet/sql/linq/how-to-return-rowsets.md).</span></span>  
  
## <a name="example"></a><span data-ttu-id="8c16b-105">Exemple</span><span class="sxs-lookup"><span data-stu-id="8c16b-105">Example</span></span>  
 <span data-ttu-id="8c16b-106">L'exemple suivant prend un paramètre d'entrée unique (ID client) et retourne un paramètre de sortie (total des ventes pour ce client).</span><span class="sxs-lookup"><span data-stu-id="8c16b-106">The following example takes a single input parameter (the customer ID) and returns an out parameter (the total sales for that customer).</span></span>  
  
```  
CREATE PROCEDURE [dbo].[CustOrderTotal]   
@CustomerID nchar(5),  
@TotalSales money OUTPUT  
AS  
SELECT @TotalSales = SUM(OD.UNITPRICE*(1-OD.DISCOUNT) * OD.QUANTITY)  
FROM ORDERS O, "ORDER DETAILS" OD  
where O.CUSTOMERID = @CustomerID AND O.ORDERID = OD.ORDERID  
```  
  
 [!code-csharp[DLinqSprox#2](../../../../../../samples/snippets/csharp/VS_Snippets_Data/DLinqSprox/cs/northwind-sprox.cs#2)]
 [!code-vb[DLinqSprox#2](../../../../../../samples/snippets/visualbasic/VS_Snippets_Data/DLinqSprox/vb/northwind-sprox.vb#2)]  
  
## <a name="example"></a><span data-ttu-id="8c16b-107">Exemple</span><span class="sxs-lookup"><span data-stu-id="8c16b-107">Example</span></span>  
 <span data-ttu-id="8c16b-108">Vous appelleriez cette procédure stockée comme suit :</span><span class="sxs-lookup"><span data-stu-id="8c16b-108">You would call this stored procedure as follows:</span></span>  
  
 [!code-csharp[DLinqSprox#3](../../../../../../samples/snippets/csharp/VS_Snippets_Data/DLinqSprox/cs/Program.cs#3)]
 [!code-vb[DLinqSprox#3](../../../../../../samples/snippets/visualbasic/VS_Snippets_Data/DLinqSprox/vb/Module1.vb#3)]  
  
## <a name="see-also"></a><span data-ttu-id="8c16b-109">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="8c16b-109">See also</span></span>

- [<span data-ttu-id="8c16b-110">Procédures stockées</span><span class="sxs-lookup"><span data-stu-id="8c16b-110">Stored Procedures</span></span>](../../../../../../docs/framework/data/adonet/sql/linq/stored-procedures.md)
- [<span data-ttu-id="8c16b-111">Téléchargement d’exemples de base de données</span><span class="sxs-lookup"><span data-stu-id="8c16b-111">Downloading Sample Databases</span></span>](../../../../../../docs/framework/data/adonet/sql/linq/downloading-sample-databases.md)
- [<span data-ttu-id="8c16b-112">Utilisation de types Nullable</span><span class="sxs-lookup"><span data-stu-id="8c16b-112">Using Nullable Types</span></span>](~/docs/csharp/programming-guide/nullable-types/using-nullable-types.md)
- [<span data-ttu-id="8c16b-113">Types valeur Nullable</span><span class="sxs-lookup"><span data-stu-id="8c16b-113">Nullable Value Types</span></span>](~/docs/visual-basic/programming-guide/language-features/data-types/nullable-value-types.md)
