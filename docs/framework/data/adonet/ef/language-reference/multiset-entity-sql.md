---
title: MULTISET (Entity SQL)
ms.date: 03/30/2017
ms.assetid: eb90a377-e47a-43a5-b308-e993b6d611e6
ms.openlocfilehash: 44e411b8ae2f43bf3a729ac091ffd1eb4c462c63
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61760491"
---
# <a name="multiset-entity-sql"></a><span data-ttu-id="cfc8b-102">MULTISET (Entity SQL)</span><span class="sxs-lookup"><span data-stu-id="cfc8b-102">MULTISET (Entity SQL)</span></span>
<span data-ttu-id="cfc8b-103">Crée une instance d'un multiensemble à partir d'une liste de valeurs.</span><span class="sxs-lookup"><span data-stu-id="cfc8b-103">Creates an instance of a multiset from a list of values.</span></span> <span data-ttu-id="cfc8b-104">Toutes les valeurs du constructeur MULTISET doivent être d'un type `T`compatible.</span><span class="sxs-lookup"><span data-stu-id="cfc8b-104">All the values in the MULTISET constructor must be of a compatible type `T`.</span></span> <span data-ttu-id="cfc8b-105">Les constructeurs de multiensemble vides ne sont pas autorisés.</span><span class="sxs-lookup"><span data-stu-id="cfc8b-105">Empty multiset constructors are not allowed.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="cfc8b-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="cfc8b-106">Syntax</span></span>  
  
```  
MULTISET ( expression [{, expression }] )  
or  
{ expression [{, expression }] }  
```  
  
## <a name="arguments"></a><span data-ttu-id="cfc8b-107">Arguments</span><span class="sxs-lookup"><span data-stu-id="cfc8b-107">Arguments</span></span>  
 `expression`  
 <span data-ttu-id="cfc8b-108">Toute liste de valeurs valide.</span><span class="sxs-lookup"><span data-stu-id="cfc8b-108">Any valid list of values.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="cfc8b-109">Valeur de retour</span><span class="sxs-lookup"><span data-stu-id="cfc8b-109">Return Value</span></span>  
 <span data-ttu-id="cfc8b-110">Une collection de type MULTISET\<T >.</span><span class="sxs-lookup"><span data-stu-id="cfc8b-110">A collection of type MULTISET\<T>.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="cfc8b-111">Notes</span><span class="sxs-lookup"><span data-stu-id="cfc8b-111">Remarks</span></span>  
 [!INCLUDE[esql](../../../../../../includes/esql-md.md)] <span data-ttu-id="cfc8b-112">propose trois types de constructeurs : constructeurs de ligne, constructeurs d'objets et constructeurs de multiensemble (ou de collection).</span><span class="sxs-lookup"><span data-stu-id="cfc8b-112">provides three kinds of constructors: row constructors, object constructors, and multiset (or collection) constructors.</span></span> <span data-ttu-id="cfc8b-113">Pour plus d’informations, consultez [Types construction](../../../../../../docs/framework/data/adonet/ef/language-reference/constructing-types-entity-sql.md).</span><span class="sxs-lookup"><span data-stu-id="cfc8b-113">For more information, see [Constructing Types](../../../../../../docs/framework/data/adonet/ef/language-reference/constructing-types-entity-sql.md).</span></span>  
  
 <span data-ttu-id="cfc8b-114">Le constructeur de multiensemble crée une instance d'un multiensemble à partir d'une liste de valeurs.</span><span class="sxs-lookup"><span data-stu-id="cfc8b-114">The multiset constructor creates an instance of a multiset from a list of values.</span></span> <span data-ttu-id="cfc8b-115">Toutes les valeurs du constructeur doivent être d'un type compatible.</span><span class="sxs-lookup"><span data-stu-id="cfc8b-115">All the values in the constructor must be of a compatible type.</span></span>  
  
 <span data-ttu-id="cfc8b-116">Par exemple, l'expression suivante crée un multiensemble d'entiers.</span><span class="sxs-lookup"><span data-stu-id="cfc8b-116">For example, the following expression creates a multiset of integers.</span></span>  
  
 `MULTISET(1, 2, 3)`  
  
 `{1, 2, 3}`  
  
> [!NOTE]
>  <span data-ttu-id="cfc8b-117">Littéraux de multiensemble imbriqués sont uniquement pris en charge lorsqu’un multiensemble d’encapsulation a un seul élément de multiensemble ; par exemple, `{{1, 2, 3}}`.</span><span class="sxs-lookup"><span data-stu-id="cfc8b-117">Nested multiset literals are only supported when a wrapping multiset has a single multiset element; for example, `{{1, 2, 3}}`.</span></span> <span data-ttu-id="cfc8b-118">Lorsqu'un multiensemble d'encapsulation a plusieurs éléments de multiensemble (par exemple, `{{1, 2}, {3, 4}}`), ils ne sont pas pris en charge.</span><span class="sxs-lookup"><span data-stu-id="cfc8b-118">When the wrapping multiset has multiple multiset elements (for example, `{{1, 2}, {3, 4}}`), nested multiset literals are not supported.</span></span>  
  
## <a name="example"></a><span data-ttu-id="cfc8b-119">Exemple</span><span class="sxs-lookup"><span data-stu-id="cfc8b-119">Example</span></span>  
 <span data-ttu-id="cfc8b-120">La requête Entity SQL suivante utilise l'opérateur MULTISET pour créer une instance d'un multiensemble à partir d'une liste de valeurs.</span><span class="sxs-lookup"><span data-stu-id="cfc8b-120">The following Entity SQL query uses the MULTISET operator to create an instance of a multiset from a list of values.</span></span> <span data-ttu-id="cfc8b-121">Cette requête est basée sur le modèle de vente AdventureWorks Sales Model.</span><span class="sxs-lookup"><span data-stu-id="cfc8b-121">The query is based on the AdventureWorks Sales Model.</span></span> <span data-ttu-id="cfc8b-122">Pour compiler et exécuter cette requête, procédez comme suit :</span><span class="sxs-lookup"><span data-stu-id="cfc8b-122">To compile and run this query, follow these steps:</span></span>  
  
1. <span data-ttu-id="cfc8b-123">Suivez la procédure décrite dans [Comment : Exécuter une requête qui retourne des résultats StructuralType](../../../../../../docs/framework/data/adonet/ef/how-to-execute-a-query-that-returns-structuraltype-results.md).</span><span class="sxs-lookup"><span data-stu-id="cfc8b-123">Follow the procedure in [How to: Execute a Query that Returns StructuralType Results](../../../../../../docs/framework/data/adonet/ef/how-to-execute-a-query-that-returns-structuraltype-results.md).</span></span>  
  
2. <span data-ttu-id="cfc8b-124">Transmettez à la méthode `ExecuteStructuralTypeQuery` la requête suivante en tant qu'argument :</span><span class="sxs-lookup"><span data-stu-id="cfc8b-124">Pass the following query as an argument to the `ExecuteStructuralTypeQuery` method:</span></span>  
  
 [!code-csharp[DP EntityServices Concepts 2#MULTISET](../../../../../../samples/snippets/csharp/VS_Snippets_Data/dp entityservices concepts 2/cs/entitysql.cs#multiset)]  
  
## <a name="see-also"></a><span data-ttu-id="cfc8b-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="cfc8b-125">See also</span></span>

- [<span data-ttu-id="cfc8b-126">Construction de types</span><span class="sxs-lookup"><span data-stu-id="cfc8b-126">Constructing Types</span></span>](../../../../../../docs/framework/data/adonet/ef/language-reference/constructing-types-entity-sql.md)
- [<span data-ttu-id="cfc8b-127">Référence Entity SQL</span><span class="sxs-lookup"><span data-stu-id="cfc8b-127">Entity SQL Reference</span></span>](../../../../../../docs/framework/data/adonet/ef/language-reference/entity-sql-reference.md)
