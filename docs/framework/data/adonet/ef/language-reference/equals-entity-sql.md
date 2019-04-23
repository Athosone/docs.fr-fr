---
title: = (égal à) (Entity SQL)
ms.date: 03/30/2017
ms.assetid: 948eb588-7080-4046-bb48-633b007393bf
ms.openlocfilehash: d50ede1964f6d6b9025a7214efe90e878aa55a0c
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59333156"
---
# <a name="-equals-entity-sql"></a><span data-ttu-id="4b6c2-102">= (égal à) (Entity SQL)</span><span class="sxs-lookup"><span data-stu-id="4b6c2-102">= (Equals) (Entity SQL)</span></span>
<span data-ttu-id="4b6c2-103">Compare l'égalité de deux expressions.</span><span class="sxs-lookup"><span data-stu-id="4b6c2-103">Compares the equality of two expressions.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="4b6c2-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="4b6c2-104">Syntax</span></span>  
  
```  
expression = expression  
or   
expression == expression  
```  
  
## <a name="arguments"></a><span data-ttu-id="4b6c2-105">Arguments</span><span class="sxs-lookup"><span data-stu-id="4b6c2-105">Arguments</span></span>  
 `expression`  
 <span data-ttu-id="4b6c2-106">Toute expression valide.</span><span class="sxs-lookup"><span data-stu-id="4b6c2-106">Any valid expression.</span></span> <span data-ttu-id="4b6c2-107">Les deux expressions doivent posséder des types de données implicitement convertibles.</span><span class="sxs-lookup"><span data-stu-id="4b6c2-107">Both expressions must have implicitly convertible data types.</span></span>  
  
## <a name="result-types"></a><span data-ttu-id="4b6c2-108">Types de résultats</span><span class="sxs-lookup"><span data-stu-id="4b6c2-108">Result Types</span></span>  
 <span data-ttu-id="4b6c2-109">`true` si l'expression de gauche est égale à l'expression de droite ; sinon, `false`.</span><span class="sxs-lookup"><span data-stu-id="4b6c2-109">`true` if the left expression is equal to the right expression; otherwise, `false`.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="4b6c2-110">Notes</span><span class="sxs-lookup"><span data-stu-id="4b6c2-110">Remarks</span></span>  
 <span data-ttu-id="4b6c2-111">L'opérateur « = = » est équivalent à « = ».</span><span class="sxs-lookup"><span data-stu-id="4b6c2-111">The == operator is equivalent to =.</span></span>  
  
## <a name="example"></a><span data-ttu-id="4b6c2-112">Exemple</span><span class="sxs-lookup"><span data-stu-id="4b6c2-112">Example</span></span>  
 <span data-ttu-id="4b6c2-113">La requête Entity SQL ci-dessous utilise l'opérateur de comparaison « = » pour comparer l'égalité de deux expressions.</span><span class="sxs-lookup"><span data-stu-id="4b6c2-113">The following Entity SQL query uses = comparison operator to compare the equality of two expressions.</span></span> <span data-ttu-id="4b6c2-114">Cette requête est basée sur le modèle de vente AdventureWorks Sales Model.</span><span class="sxs-lookup"><span data-stu-id="4b6c2-114">The query is based on the AdventureWorks Sales Model.</span></span> <span data-ttu-id="4b6c2-115">Pour compiler et exécuter cette requête, procédez comme suit :</span><span class="sxs-lookup"><span data-stu-id="4b6c2-115">To compile and run this query, follow these steps:</span></span>  
  
1. <span data-ttu-id="4b6c2-116">Suivez la procédure décrite dans [Comment : Exécuter une requête qui retourne des résultats StructuralType](../../../../../../docs/framework/data/adonet/ef/how-to-execute-a-query-that-returns-structuraltype-results.md).</span><span class="sxs-lookup"><span data-stu-id="4b6c2-116">Follow the procedure in [How to: Execute a Query that Returns StructuralType Results](../../../../../../docs/framework/data/adonet/ef/how-to-execute-a-query-that-returns-structuraltype-results.md).</span></span>  
  
2. <span data-ttu-id="4b6c2-117">Transmettez à la méthode `ExecuteStructuralTypeQuery` la requête suivante en tant qu'argument :</span><span class="sxs-lookup"><span data-stu-id="4b6c2-117">Pass the following query as an argument to the `ExecuteStructuralTypeQuery` method:</span></span>  
  
 [!code-csharp[DP EntityServices Concepts 2#EQUALS](../../../../../../samples/snippets/csharp/VS_Snippets_Data/dp entityservices concepts 2/cs/entitysql.cs#equals)]  
  
## <a name="see-also"></a><span data-ttu-id="4b6c2-118">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="4b6c2-118">See also</span></span>

- [<span data-ttu-id="4b6c2-119">Référence Entity SQL</span><span class="sxs-lookup"><span data-stu-id="4b6c2-119">Entity SQL Reference</span></span>](../../../../../../docs/framework/data/adonet/ef/language-reference/entity-sql-reference.md)
