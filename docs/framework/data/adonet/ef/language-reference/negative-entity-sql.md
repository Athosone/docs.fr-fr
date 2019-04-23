---
title: '- (Négatif) (Entity SQL)'
ms.date: 03/30/2017
ms.assetid: 208e54ef-4741-4ec5-89d6-6ff700863cb0
ms.openlocfilehash: 6e5512546faeaa9760dcf135165a999a6f95322b
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59311004"
---
# <a name="--negative-entity-sql"></a><span data-ttu-id="2e604-102">- (négatif) (Entity SQL)</span><span class="sxs-lookup"><span data-stu-id="2e604-102">- (Negative) (Entity SQL)</span></span>
<span data-ttu-id="2e604-103">Retourne la forme négative de la valeur d'une expression numérique.</span><span class="sxs-lookup"><span data-stu-id="2e604-103">Returns the negative of the value of a numeric expression.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="2e604-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="2e604-104">Syntax</span></span>  
  
```  
- expression  
```  
  
## <a name="arguments"></a><span data-ttu-id="2e604-105">Arguments</span><span class="sxs-lookup"><span data-stu-id="2e604-105">Arguments</span></span>  
 `expression`  
 <span data-ttu-id="2e604-106">Toute expression valide de l'un des types de données numériques.</span><span class="sxs-lookup"><span data-stu-id="2e604-106">Any valid expression of any one of the numeric data types.</span></span>  
  
## <a name="result-types"></a><span data-ttu-id="2e604-107">Types de résultats</span><span class="sxs-lookup"><span data-stu-id="2e604-107">Result Types</span></span>  
 <span data-ttu-id="2e604-108">Type de données de l' `expression`.</span><span class="sxs-lookup"><span data-stu-id="2e604-108">The data type of `expression`.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="2e604-109">Notes</span><span class="sxs-lookup"><span data-stu-id="2e604-109">Remarks</span></span>  
 <span data-ttu-id="2e604-110">Si l' `expression` est un type non signé, le type du résultat sera le type signé le plus proche du type de l' `expression`.</span><span class="sxs-lookup"><span data-stu-id="2e604-110">If `expression` is an unsigned type, the result type will be the signed type that most closely relates to the type of `expression`.</span></span> <span data-ttu-id="2e604-111">Par exemple, si l' `expression` est de type Byte, une valeur de type Int16 sera retournée.</span><span class="sxs-lookup"><span data-stu-id="2e604-111">For example, if `expression` is of type Byte, a value of type Int16 will be returned.</span></span>  
  
## <a name="example"></a><span data-ttu-id="2e604-112">Exemple</span><span class="sxs-lookup"><span data-stu-id="2e604-112">Example</span></span>  
 <span data-ttu-id="2e604-113">La requête Entity SQL ci-dessous utilise l'opérateur arithmétique - pour retourner la forme négative de la valeur d'une expression numérique.</span><span class="sxs-lookup"><span data-stu-id="2e604-113">The following Entity SQL query uses the - arithmetic operator to return the negative of the value of a numeric expression.</span></span> <span data-ttu-id="2e604-114">Cette requête est basée sur le modèle de vente AdventureWorks Sales Model.</span><span class="sxs-lookup"><span data-stu-id="2e604-114">The query is based on the AdventureWorks Sales Model.</span></span> <span data-ttu-id="2e604-115">Pour compiler et exécuter cette requête, procédez comme suit :</span><span class="sxs-lookup"><span data-stu-id="2e604-115">To compile and run this query, follow these steps:</span></span>  
  
1. <span data-ttu-id="2e604-116">Suivez la procédure décrite dans [Comment : Exécuter une requête qui retourne des résultats StructuralType](../../../../../../docs/framework/data/adonet/ef/how-to-execute-a-query-that-returns-structuraltype-results.md).</span><span class="sxs-lookup"><span data-stu-id="2e604-116">Follow the procedure in [How to: Execute a Query that Returns StructuralType Results](../../../../../../docs/framework/data/adonet/ef/how-to-execute-a-query-that-returns-structuraltype-results.md).</span></span>  
  
2. <span data-ttu-id="2e604-117">Transmettez à la méthode `ExecuteStructuralTypeQuery` la requête suivante en tant qu'argument :</span><span class="sxs-lookup"><span data-stu-id="2e604-117">Pass the following query as an argument to the `ExecuteStructuralTypeQuery` method:</span></span>  
  
 [!code-csharp[DP EntityServices Concepts 2#NEGATIVE](../../../../../../samples/snippets/csharp/VS_Snippets_Data/dp entityservices concepts 2/cs/entitysql.cs#negative)]  
  
## <a name="see-also"></a><span data-ttu-id="2e604-118">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="2e604-118">See also</span></span>

- [<span data-ttu-id="2e604-119">Référence Entity SQL</span><span class="sxs-lookup"><span data-stu-id="2e604-119">Entity SQL Reference</span></span>](../../../../../../docs/framework/data/adonet/ef/language-reference/entity-sql-reference.md)
