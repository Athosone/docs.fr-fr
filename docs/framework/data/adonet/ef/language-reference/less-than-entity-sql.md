---
title: < (Inférieur à) (Entity SQL)
ms.date: 03/30/2017
ms.assetid: 1fc2a039-3ad6-4b3c-b41d-09932e803f86
ms.openlocfilehash: 1ca1cbdf1282782295b659393e8f54aae3ec5649
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61772299"
---
# <a name="-less-than-entity-sql"></a><span data-ttu-id="1706b-102">\< (Inférieur à) (Entity SQL)</span><span class="sxs-lookup"><span data-stu-id="1706b-102">\< (Less Than) (Entity SQL)</span></span>
<span data-ttu-id="1706b-103">Compare deux expressions pour déterminer si la valeur de l'expression de gauche est inférieure à celle de l'expression de droite.</span><span class="sxs-lookup"><span data-stu-id="1706b-103">Compares two expressions to determine whether the left expression has a value less than the right expression.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="1706b-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="1706b-104">Syntax</span></span>  
  
```  
expression < expression  
```  
  
## <a name="arguments"></a><span data-ttu-id="1706b-105">Arguments</span><span class="sxs-lookup"><span data-stu-id="1706b-105">Arguments</span></span>  
 `expression`  
 <span data-ttu-id="1706b-106">Toute expression valide.</span><span class="sxs-lookup"><span data-stu-id="1706b-106">Any valid expression.</span></span> <span data-ttu-id="1706b-107">Les deux expressions doivent posséder des types de données implicitement convertibles.</span><span class="sxs-lookup"><span data-stu-id="1706b-107">Both expressions must have implicitly convertible data types.</span></span>  
  
## <a name="result-types"></a><span data-ttu-id="1706b-108">Types de résultats</span><span class="sxs-lookup"><span data-stu-id="1706b-108">Result Types</span></span>  
 <span data-ttu-id="1706b-109">`true` si la valeur de l'expression de gauche est inférieure à celle de l'expression de droite ; sinon, `false`.</span><span class="sxs-lookup"><span data-stu-id="1706b-109">`true` if the left expression has a value less than the right expression; otherwise, `false`.</span></span>  
  
## <a name="example"></a><span data-ttu-id="1706b-110">Exemple</span><span class="sxs-lookup"><span data-stu-id="1706b-110">Example</span></span>  
 <span data-ttu-id="1706b-111">La requête Entity SQL ci-dessous utilise l'opérateur de comparaison < pour comparer deux expressions afin de déterminer si la valeur de l'expression de gauche est inférieure à celle de l'expression de droite.</span><span class="sxs-lookup"><span data-stu-id="1706b-111">The following Entity SQL query uses < comparison operator to compare two expressions to determine whether the left expression has a value less than the right expression.</span></span> <span data-ttu-id="1706b-112">Cette requête est basée sur le modèle de vente AdventureWorks Sales Model.</span><span class="sxs-lookup"><span data-stu-id="1706b-112">The query is based on the AdventureWorks Sales Model.</span></span> <span data-ttu-id="1706b-113">Pour compiler et exécuter cette requête, procédez comme suit :</span><span class="sxs-lookup"><span data-stu-id="1706b-113">To compile and run this query, follow these steps:</span></span>  
  
1. <span data-ttu-id="1706b-114">Suivez la procédure décrite dans [Comment : Exécuter une requête qui retourne des résultats StructuralType](../../../../../../docs/framework/data/adonet/ef/how-to-execute-a-query-that-returns-structuraltype-results.md).</span><span class="sxs-lookup"><span data-stu-id="1706b-114">Follow the procedure in [How to: Execute a Query that Returns StructuralType Results](../../../../../../docs/framework/data/adonet/ef/how-to-execute-a-query-that-returns-structuraltype-results.md).</span></span>  
  
2. <span data-ttu-id="1706b-115">Transmettez à la méthode `ExecuteStructuralTypeQuery` la requête suivante en tant qu'argument :</span><span class="sxs-lookup"><span data-stu-id="1706b-115">Pass the following query as an argument to the `ExecuteStructuralTypeQuery` method:</span></span>  
  
 [!code-csharp[DP EntityServices Concepts 2#LESS](../../../../../../samples/snippets/csharp/VS_Snippets_Data/dp entityservices concepts 2/cs/entitysql.cs#less)]  
  
## <a name="see-also"></a><span data-ttu-id="1706b-116">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1706b-116">See also</span></span>

- [<span data-ttu-id="1706b-117">Référence Entity SQL</span><span class="sxs-lookup"><span data-stu-id="1706b-117">Entity SQL Reference</span></span>](../../../../../../docs/framework/data/adonet/ef/language-reference/entity-sql-reference.md)
