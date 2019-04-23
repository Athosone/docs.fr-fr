---
title: '* (Multiplication) (Entity SQL)'
ms.date: 03/30/2017
ms.assetid: 508ce246-4e86-47dd-a605-4af4bebb9891
ms.openlocfilehash: 308df758d59a7e12a8b5a19ae72fcbee2f168490
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59329724"
---
# <a name="-multiply-entity-sql"></a><span data-ttu-id="ee0da-102">\* (Multiplier) (Entity SQL)</span><span class="sxs-lookup"><span data-stu-id="ee0da-102">\* (Multiply) (Entity SQL)</span></span>
<span data-ttu-id="ee0da-103">Multiplie deux expressions.</span><span class="sxs-lookup"><span data-stu-id="ee0da-103">Multiplies two expressions.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="ee0da-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="ee0da-104">Syntax</span></span>  
  
```  
expression * expression  
```  
  
## <a name="arguments"></a><span data-ttu-id="ee0da-105">Arguments</span><span class="sxs-lookup"><span data-stu-id="ee0da-105">Arguments</span></span>  
 `expression`  
 <span data-ttu-id="ee0da-106">Toute expression valide de l'un des types de données numériques.</span><span class="sxs-lookup"><span data-stu-id="ee0da-106">Any valid expression of any one of the numeric data types.</span></span>  
  
## <a name="result-types"></a><span data-ttu-id="ee0da-107">Types de résultats</span><span class="sxs-lookup"><span data-stu-id="ee0da-107">Result Types</span></span>  
 <span data-ttu-id="ee0da-108">Type de données qui résulte de la promotion de type implicite de deux arguments.</span><span class="sxs-lookup"><span data-stu-id="ee0da-108">The data type that results from the implicit type promotion of the two arguments.</span></span> <span data-ttu-id="ee0da-109">Pour plus d’informations sur la promotion de type implicite, consultez [système de Type](../../../../../../docs/framework/data/adonet/ef/language-reference/type-system-entity-sql.md).</span><span class="sxs-lookup"><span data-stu-id="ee0da-109">For more information about implicit type promotion, see [Type System](../../../../../../docs/framework/data/adonet/ef/language-reference/type-system-entity-sql.md).</span></span>  
  
## <a name="example"></a><span data-ttu-id="ee0da-110">Exemple</span><span class="sxs-lookup"><span data-stu-id="ee0da-110">Example</span></span>  
 <span data-ttu-id="ee0da-111">La requête Entity SQL ci-dessous utilise l'opérateur arithmétique \* pour multiplier deux nombres.</span><span class="sxs-lookup"><span data-stu-id="ee0da-111">The following Entity SQL query uses the \* arithmetic operator to multiply two numbers.</span></span> <span data-ttu-id="ee0da-112">Cette requête est basée sur le modèle de vente AdventureWorks Sales Model.</span><span class="sxs-lookup"><span data-stu-id="ee0da-112">The query is based on the AdventureWorks Sales Model.</span></span> <span data-ttu-id="ee0da-113">Pour compiler et exécuter cette requête, procédez comme suit :</span><span class="sxs-lookup"><span data-stu-id="ee0da-113">To compile and run this query, follow these steps:</span></span>  
  
1. <span data-ttu-id="ee0da-114">Suivez la procédure décrite dans [Comment : Exécuter une requête qui retourne des résultats StructuralType](../../../../../../docs/framework/data/adonet/ef/how-to-execute-a-query-that-returns-structuraltype-results.md).</span><span class="sxs-lookup"><span data-stu-id="ee0da-114">Follow the procedure in [How to: Execute a Query that Returns StructuralType Results](../../../../../../docs/framework/data/adonet/ef/how-to-execute-a-query-that-returns-structuraltype-results.md).</span></span>  
  
2. <span data-ttu-id="ee0da-115">Transmettez à la méthode `ExecuteStructuralTypeQuery` la requête suivante en tant qu'argument :</span><span class="sxs-lookup"><span data-stu-id="ee0da-115">Pass the following query as an argument to the `ExecuteStructuralTypeQuery` method:</span></span>  
  
 [!code-csharp[DP EntityServices Concepts 2#MULTIPLY](../../../../../../samples/snippets/csharp/VS_Snippets_Data/dp entityservices concepts 2/cs/entitysql.cs#multiply)]  
  
## <a name="see-also"></a><span data-ttu-id="ee0da-116">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ee0da-116">See also</span></span>

- [<span data-ttu-id="ee0da-117">Référence Entity SQL</span><span class="sxs-lookup"><span data-stu-id="ee0da-117">Entity SQL Reference</span></span>](../../../../../../docs/framework/data/adonet/ef/language-reference/entity-sql-reference.md)
