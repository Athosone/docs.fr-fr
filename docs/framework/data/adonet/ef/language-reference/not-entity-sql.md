---
title: '! (NOT) (Entity SQL)'
ms.date: 03/30/2017
ms.assetid: a1447a34-df06-4393-93c3-0612ebd41abc
ms.openlocfilehash: 51d3bdbc4adb0b5fd6275629219698dd9b42fa86
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59306766"
---
# <a name="-not-entity-sql"></a><span data-ttu-id="d5fe5-103">!</span><span class="sxs-lookup"><span data-stu-id="d5fe5-103">!</span></span> <span data-ttu-id="d5fe5-104">(NOT) (Entity SQL)</span><span class="sxs-lookup"><span data-stu-id="d5fe5-104">(NOT) (Entity SQL)</span></span>
<span data-ttu-id="d5fe5-105">Inverse une expression `Boolean` .</span><span class="sxs-lookup"><span data-stu-id="d5fe5-105">Negates a `Boolean` expression.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="d5fe5-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="d5fe5-106">Syntax</span></span>  
  
```  
NOT boolean_expression  
or  
! boolean_expression  
```  
  
## <a name="arguments"></a><span data-ttu-id="d5fe5-107">Arguments</span><span class="sxs-lookup"><span data-stu-id="d5fe5-107">Arguments</span></span>  
 `boolean_expression`  
 <span data-ttu-id="d5fe5-108">Toute expression valide qui retourne une valeur booléenne.</span><span class="sxs-lookup"><span data-stu-id="d5fe5-108">Any valid expression that returns a Boolean.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="d5fe5-109">Notes</span><span class="sxs-lookup"><span data-stu-id="d5fe5-109">Remarks</span></span>  
 <span data-ttu-id="d5fe5-110">Le point d'exclamation (!) a la même fonctionnalité que l'opérateur NOT.</span><span class="sxs-lookup"><span data-stu-id="d5fe5-110">The exclamation point (!) has the same functionality as the NOT operator.</span></span>  
  
## <a name="example"></a><span data-ttu-id="d5fe5-111">Exemple</span><span class="sxs-lookup"><span data-stu-id="d5fe5-111">Example</span></span>  
 <span data-ttu-id="d5fe5-112">La requête Entity SQL ci-dessous utilise l'opérateur NOT pour inverser une expression `Boolean` .</span><span class="sxs-lookup"><span data-stu-id="d5fe5-112">The following Entity SQL query uses the NOT operator to negates a `Boolean` expression.</span></span> <span data-ttu-id="d5fe5-113">Cette requête est basée sur le modèle de vente AdventureWorks Sales Model.</span><span class="sxs-lookup"><span data-stu-id="d5fe5-113">The query is based on the AdventureWorks Sales Model.</span></span> <span data-ttu-id="d5fe5-114">Pour compiler et exécuter cette requête, procédez comme suit :</span><span class="sxs-lookup"><span data-stu-id="d5fe5-114">To compile and run this query, follow these steps:</span></span>  
  
1. <span data-ttu-id="d5fe5-115">Suivez la procédure décrite dans [Comment : Exécuter une requête qui retourne des résultats StructuralType](../../../../../../docs/framework/data/adonet/ef/how-to-execute-a-query-that-returns-structuraltype-results.md).</span><span class="sxs-lookup"><span data-stu-id="d5fe5-115">Follow the procedure in [How to: Execute a Query that Returns StructuralType Results](../../../../../../docs/framework/data/adonet/ef/how-to-execute-a-query-that-returns-structuraltype-results.md).</span></span>  
  
2. <span data-ttu-id="d5fe5-116">Transmettez à la méthode `ExecuteStructuralTypeQuery` la requête suivante en tant qu'argument :</span><span class="sxs-lookup"><span data-stu-id="d5fe5-116">Pass the following query as an argument to the `ExecuteStructuralTypeQuery` method:</span></span>  
  
 [!code-csharp[DP EntityServices Concepts 2#NOT](../../../../../../samples/snippets/csharp/VS_Snippets_Data/dp entityservices concepts 2/cs/entitysql.cs#not)]  
  
## <a name="see-also"></a><span data-ttu-id="d5fe5-117">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d5fe5-117">See also</span></span>

- [<span data-ttu-id="d5fe5-118">Référence Entity SQL</span><span class="sxs-lookup"><span data-stu-id="d5fe5-118">Entity SQL Reference</span></span>](../../../../../../docs/framework/data/adonet/ef/language-reference/entity-sql-reference.md)
