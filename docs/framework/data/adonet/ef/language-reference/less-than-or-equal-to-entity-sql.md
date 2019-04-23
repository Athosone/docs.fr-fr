---
title: < = (inférieur ou égal à) (Entity SQL)
ms.date: 03/30/2017
ms.assetid: 7c46da5c-fa09-4d90-adcc-c7e1b769d8e6
ms.openlocfilehash: 7a65984da22d125bdbdd5cfadb5a2051fa3dafdc
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59304764"
---
# <a name="-less-than-or-equal-to-entity-sql"></a><span data-ttu-id="9311c-102">\<= (Inférieur ou égal à) (Entity SQL)</span><span class="sxs-lookup"><span data-stu-id="9311c-102">\<= (Less Than or Equal To) (Entity SQL)</span></span>
<span data-ttu-id="9311c-103">Compare deux expressions pour déterminer si la valeur de l'expression de gauche est inférieure ou égale à celle de l'expression de droite.</span><span class="sxs-lookup"><span data-stu-id="9311c-103">Compares two expressions to determine whether the left expression has a value less than or equal to the right expression.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="9311c-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="9311c-104">Syntax</span></span>  
  
```  
expression <= expression  
```  
  
## <a name="arguments"></a><span data-ttu-id="9311c-105">Arguments</span><span class="sxs-lookup"><span data-stu-id="9311c-105">Arguments</span></span>  
 `expression`  
 <span data-ttu-id="9311c-106">Toute expression valide.</span><span class="sxs-lookup"><span data-stu-id="9311c-106">Any valid expression.</span></span> <span data-ttu-id="9311c-107">Les deux expressions doivent posséder des types de données implicitement convertibles.</span><span class="sxs-lookup"><span data-stu-id="9311c-107">Both expressions must have implicitly convertible data types.</span></span>  
  
## <a name="result-types"></a><span data-ttu-id="9311c-108">Types de résultats</span><span class="sxs-lookup"><span data-stu-id="9311c-108">Result Types</span></span>  
 <span data-ttu-id="9311c-109">`true` si la valeur de l'expression de gauche est inférieure ou égale à celle de l'expression de droite ; sinon, `false`.</span><span class="sxs-lookup"><span data-stu-id="9311c-109">`true` if the left expression has a value less than or equal to the right expression; otherwise, `false`.</span></span>  
  
## <a name="example"></a><span data-ttu-id="9311c-110">Exemple</span><span class="sxs-lookup"><span data-stu-id="9311c-110">Example</span></span>  
 <span data-ttu-id="9311c-111">La requête Entity SQL ci-dessous utilise l'opérateur de comparaison <= pour comparer deux expressions afin de déterminer si la valeur de l'expression de gauche est inférieure ou égale à celle de l'expression de droite.</span><span class="sxs-lookup"><span data-stu-id="9311c-111">The following Entity SQL query uses <= comparison operator to compare two expressions to determine whether the left expression has a value less than or equal to the right expression.</span></span> <span data-ttu-id="9311c-112">Cette requête est basée sur le modèle de vente AdventureWorks Sales Model.</span><span class="sxs-lookup"><span data-stu-id="9311c-112">The query is based on the AdventureWorks Sales Model.</span></span> <span data-ttu-id="9311c-113">Pour compiler et exécuter cette requête, procédez comme suit :</span><span class="sxs-lookup"><span data-stu-id="9311c-113">To compile and run this query, follow these steps:</span></span>  
  
1. <span data-ttu-id="9311c-114">Suivez la procédure décrite dans [Comment : Exécuter une requête qui retourne des résultats StructuralType](../../../../../../docs/framework/data/adonet/ef/how-to-execute-a-query-that-returns-structuraltype-results.md).</span><span class="sxs-lookup"><span data-stu-id="9311c-114">Follow the procedure in [How to: Execute a Query that Returns StructuralType Results](../../../../../../docs/framework/data/adonet/ef/how-to-execute-a-query-that-returns-structuraltype-results.md).</span></span>  
  
2. <span data-ttu-id="9311c-115">Transmettez à la méthode `ExecuteStructuralTypeQuery` la requête suivante en tant qu'argument :</span><span class="sxs-lookup"><span data-stu-id="9311c-115">Pass the following query as an argument to the `ExecuteStructuralTypeQuery` method:</span></span>  
  
 [!code-csharp[DP EntityServices Concepts 2#LESS_OR_EQUALS](../../../../../../samples/snippets/csharp/VS_Snippets_Data/dp entityservices concepts 2/cs/entitysql.cs#less_or_equals)]  
  
## <a name="see-also"></a><span data-ttu-id="9311c-116">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="9311c-116">See also</span></span>

- [<span data-ttu-id="9311c-117">Référence Entity SQL</span><span class="sxs-lookup"><span data-stu-id="9311c-117">Entity SQL Reference</span></span>](../../../../../../docs/framework/data/adonet/ef/language-reference/entity-sql-reference.md)
