---
title: '- (Soustraction) (Entity SQL)'
ms.date: 03/30/2017
ms.assetid: bc4327f9-09c0-438f-a008-927c5c478040
ms.openlocfilehash: 2e4c08788ea57000e189c8371f0494641931184b
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61797655"
---
# <a name="--subtract-entity-sql"></a><span data-ttu-id="c28f2-102">- (soustraction) (Entity SQL)</span><span class="sxs-lookup"><span data-stu-id="c28f2-102">- (Subtract) (Entity SQL)</span></span>
<span data-ttu-id="c28f2-103">Soustrait deux nombres.</span><span class="sxs-lookup"><span data-stu-id="c28f2-103">Subtracts two numbers.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="c28f2-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="c28f2-104">Syntax</span></span>  
  
```  
expression - expression  
```  
  
## <a name="arguments"></a><span data-ttu-id="c28f2-105">Arguments</span><span class="sxs-lookup"><span data-stu-id="c28f2-105">Arguments</span></span>  
 `expression`  
 <span data-ttu-id="c28f2-106">Toute expression valide de l'un des types de données numériques.</span><span class="sxs-lookup"><span data-stu-id="c28f2-106">Any valid expression of any one of the numeric data types.</span></span>  
  
## <a name="result-types"></a><span data-ttu-id="c28f2-107">Types de résultats</span><span class="sxs-lookup"><span data-stu-id="c28f2-107">Result Types</span></span>  
 <span data-ttu-id="c28f2-108">Type de données qui résulte de la promotion de type implicite de deux arguments.</span><span class="sxs-lookup"><span data-stu-id="c28f2-108">The data type that results from the implicit type promotion of the two arguments.</span></span> <span data-ttu-id="c28f2-109">Pour plus d’informations sur la promotion de type implicite, consultez [système de Type](../../../../../../docs/framework/data/adonet/ef/language-reference/type-system-entity-sql.md).</span><span class="sxs-lookup"><span data-stu-id="c28f2-109">For more information about implicit type promotion, see [Type System](../../../../../../docs/framework/data/adonet/ef/language-reference/type-system-entity-sql.md).</span></span>  
  
## <a name="example"></a><span data-ttu-id="c28f2-110">Exemple</span><span class="sxs-lookup"><span data-stu-id="c28f2-110">Example</span></span>  
 <span data-ttu-id="c28f2-111">La requête Entity SQL ci-dessous utilise l'opérateur arithmétique - pour soustraire deux nombres.</span><span class="sxs-lookup"><span data-stu-id="c28f2-111">The following Entity SQL query uses the - arithmetic operator to subtract two numbers.</span></span> <span data-ttu-id="c28f2-112">Cette requête est basée sur le modèle de vente AdventureWorks Sales Model.</span><span class="sxs-lookup"><span data-stu-id="c28f2-112">The query is based on the AdventureWorks Sales Model.</span></span> <span data-ttu-id="c28f2-113">Pour compiler et exécuter cette requête, procédez comme suit :</span><span class="sxs-lookup"><span data-stu-id="c28f2-113">To compile and run this query, follow these steps:</span></span>  
  
1. <span data-ttu-id="c28f2-114">Suivez la procédure décrite dans [Comment : Exécuter une requête qui retourne des résultats StructuralType](../../../../../../docs/framework/data/adonet/ef/how-to-execute-a-query-that-returns-structuraltype-results.md).</span><span class="sxs-lookup"><span data-stu-id="c28f2-114">Follow the procedure in [How to: Execute a Query that Returns StructuralType Results](../../../../../../docs/framework/data/adonet/ef/how-to-execute-a-query-that-returns-structuraltype-results.md).</span></span>  
  
2. <span data-ttu-id="c28f2-115">Transmettez à la méthode `ExecuteStructuralTypeQuery` la requête suivante en tant qu'argument :</span><span class="sxs-lookup"><span data-stu-id="c28f2-115">Pass the following query as an argument to the `ExecuteStructuralTypeQuery` method:</span></span>  
  
 [!code-csharp[DP EntityServices Concepts 2#SUBTRACT](../../../../../../samples/snippets/csharp/VS_Snippets_Data/dp entityservices concepts 2/cs/entitysql.cs#subtract)]  
  
## <a name="see-also"></a><span data-ttu-id="c28f2-116">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c28f2-116">See also</span></span>

- [<span data-ttu-id="c28f2-117">Référence Entity SQL</span><span class="sxs-lookup"><span data-stu-id="c28f2-117">Entity SQL Reference</span></span>](../../../../../../docs/framework/data/adonet/ef/language-reference/entity-sql-reference.md)
