---
title: IN (Entity SQL)
ms.date: 03/30/2017
ms.assetid: 51662950-ee01-4857-b7b9-311dd8515966
ms.openlocfilehash: d88f79dbfcd27f0ca0d1e26815d7d2bbee731bcf
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59331271"
---
# <a name="in-entity-sql"></a><span data-ttu-id="c47e0-102">IN (Entity SQL)</span><span class="sxs-lookup"><span data-stu-id="c47e0-102">IN (Entity SQL)</span></span>
<span data-ttu-id="c47e0-103">Détermine si une valeur correspond à une valeur incluse dans une collection.</span><span class="sxs-lookup"><span data-stu-id="c47e0-103">Determines whether a value matches any value in a collection.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="c47e0-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="c47e0-104">Syntax</span></span>  
  
```  
value [ NOT ] IN expression  
```  
  
## <a name="arguments"></a><span data-ttu-id="c47e0-105">Arguments</span><span class="sxs-lookup"><span data-stu-id="c47e0-105">Arguments</span></span>  
 `value`  
 <span data-ttu-id="c47e0-106">Toute expression valide qui retourne la valeur dont rechercher une correspondance.</span><span class="sxs-lookup"><span data-stu-id="c47e0-106">Any valid expression that returns the value to match.</span></span>  
  
 <span data-ttu-id="c47e0-107">[ NOT ]</span><span class="sxs-lookup"><span data-stu-id="c47e0-107">[ NOT ]</span></span>  
 <span data-ttu-id="c47e0-108">Spécifie que la valeur du résultat `Boolean` de IN est inversée.</span><span class="sxs-lookup"><span data-stu-id="c47e0-108">Specifies that the `Boolean` result of IN be negated.</span></span>  
  
 `expression`  
 <span data-ttu-id="c47e0-109">Toute expression valide qui retourne la collection dans laquelle rechercher une correspondance.</span><span class="sxs-lookup"><span data-stu-id="c47e0-109">Any valid expression that returns the collection to test for a match.</span></span> <span data-ttu-id="c47e0-110">Toutes les expressions doivent être du même type que le `value`ou d'un type de base commun ou dérivé de celui-ci.</span><span class="sxs-lookup"><span data-stu-id="c47e0-110">All expressions must be of the same type or of a common base or derived type as `value`.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="c47e0-111">Valeur de retour</span><span class="sxs-lookup"><span data-stu-id="c47e0-111">Return Value</span></span>  
 <span data-ttu-id="c47e0-112">`true` si la valeur est trouvée dans la collection ; null si la valeur ou la collection est Null ; sinon, `false`.</span><span class="sxs-lookup"><span data-stu-id="c47e0-112">`true` if the value is found in the collection; null if the value is null or the collection is null; otherwise, `false`.</span></span> <span data-ttu-id="c47e0-113">L'utilisation de NOT IN inverse les résultats de IN.</span><span class="sxs-lookup"><span data-stu-id="c47e0-113">Using NOT IN negates the results of IN.</span></span>  
  
## <a name="example"></a><span data-ttu-id="c47e0-114">Exemple</span><span class="sxs-lookup"><span data-stu-id="c47e0-114">Example</span></span>  
 <span data-ttu-id="c47e0-115">La requête Entity SQL ci-dessous utilise l'opérateur IN pour déterminer si une valeur correspond à une valeur contenue dans une collection.</span><span class="sxs-lookup"><span data-stu-id="c47e0-115">The following Entity SQL query uses the IN operator to determine whether a value matches any value in a collection.</span></span> <span data-ttu-id="c47e0-116">Cette requête est basée sur le modèle de vente AdventureWorks Sales Model.</span><span class="sxs-lookup"><span data-stu-id="c47e0-116">The query is based on the AdventureWorks Sales Model.</span></span> <span data-ttu-id="c47e0-117">Pour compiler et exécuter cette requête, procédez comme suit :</span><span class="sxs-lookup"><span data-stu-id="c47e0-117">To compile and run this query, follow these steps:</span></span>  
  
1. <span data-ttu-id="c47e0-118">Suivez la procédure décrite dans [Comment : Exécuter une requête qui retourne des résultats StructuralType](../../../../../../docs/framework/data/adonet/ef/how-to-execute-a-query-that-returns-structuraltype-results.md).</span><span class="sxs-lookup"><span data-stu-id="c47e0-118">Follow the procedure in [How to: Execute a Query that Returns StructuralType Results](../../../../../../docs/framework/data/adonet/ef/how-to-execute-a-query-that-returns-structuraltype-results.md).</span></span>  
  
2. <span data-ttu-id="c47e0-119">Transmettez à la méthode `ExecuteStructuralTypeQuery` la requête suivante en tant qu'argument :</span><span class="sxs-lookup"><span data-stu-id="c47e0-119">Pass the following query as an argument to the `ExecuteStructuralTypeQuery` method:</span></span>  
  
 [!code-csharp[DP EntityServices Concepts 2#IN](../../../../../../samples/snippets/csharp/VS_Snippets_Data/dp entityservices concepts 2/cs/entitysql.cs#in)]  
  
## <a name="see-also"></a><span data-ttu-id="c47e0-120">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c47e0-120">See also</span></span>

- [<span data-ttu-id="c47e0-121">Référence Entity SQL</span><span class="sxs-lookup"><span data-stu-id="c47e0-121">Entity SQL Reference</span></span>](../../../../../../docs/framework/data/adonet/ef/language-reference/entity-sql-reference.md)
