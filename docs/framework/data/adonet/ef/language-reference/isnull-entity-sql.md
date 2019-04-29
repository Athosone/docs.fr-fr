---
title: ISNULL (Entity SQL)
ms.date: 03/30/2017
ms.assetid: dc7a0173-3664-4c90-a57b-5cbb0a8ed7ee
ms.openlocfilehash: aaecce3ff74d64b8e07b31329ced5b5e581fca5b
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61780404"
---
# <a name="isnull-entity-sql"></a><span data-ttu-id="fdedd-102">ISNULL (Entity SQL)</span><span class="sxs-lookup"><span data-stu-id="fdedd-102">ISNULL (Entity SQL)</span></span>
<span data-ttu-id="fdedd-103">Détermine si une expression de requête a la valeur NULL.</span><span class="sxs-lookup"><span data-stu-id="fdedd-103">Determines if a query expression is null.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="fdedd-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="fdedd-104">Syntax</span></span>  
  
```  
expression IS [ NOT ] NULL  
```  
  
## <a name="arguments"></a><span data-ttu-id="fdedd-105">Arguments</span><span class="sxs-lookup"><span data-stu-id="fdedd-105">Arguments</span></span>  
 `expression`  
 <span data-ttu-id="fdedd-106">Toute expression de requête valide.</span><span class="sxs-lookup"><span data-stu-id="fdedd-106">Any valid query expression.</span></span> <span data-ttu-id="fdedd-107">Ne peut pas être une collection, posséder des membres de collection ou être un type d'enregistrement avec des propriétés de type collection.</span><span class="sxs-lookup"><span data-stu-id="fdedd-107">Cannot be a collection, have collection members, or a record type with collection type properties.</span></span>  
  
 <span data-ttu-id="fdedd-108">NOT</span><span class="sxs-lookup"><span data-stu-id="fdedd-108">NOT</span></span>  
 <span data-ttu-id="fdedd-109">Inverse le résultat EDM.Boolean de l'opérateur IS NULL.</span><span class="sxs-lookup"><span data-stu-id="fdedd-109">Negates the EDM.Boolean result of IS NULL.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="fdedd-110">Valeur de retour</span><span class="sxs-lookup"><span data-stu-id="fdedd-110">Return Value</span></span>  
 <span data-ttu-id="fdedd-111">`true` si `expression` retourne la valeur NULL ; sinon, `false`.</span><span class="sxs-lookup"><span data-stu-id="fdedd-111">`true` if `expression` returns null; otherwise, `false`.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="fdedd-112">Notes</span><span class="sxs-lookup"><span data-stu-id="fdedd-112">Remarks</span></span>  
 <span data-ttu-id="fdedd-113">Utilisez `IS NULL` pour déterminer si l'élément d'une jointure externe est NULL :</span><span class="sxs-lookup"><span data-stu-id="fdedd-113">Use `IS NULL` to determine if the element of an outer join is null:</span></span>  
  
```  
select c   
      from LOB.Customers as c left outer join LOB.Orders as o   
                              on c.ID = o.CustomerID    
      where o is not null and o.OrderQuantity = @x  
```  
  
 <span data-ttu-id="fdedd-114">Utilisez `IS NULL` pour déterminer si un membre a une valeur réelle :</span><span class="sxs-lookup"><span data-stu-id="fdedd-114">Use `IS NULL` to determine if a member has an actual value:</span></span>  
  
```  
select c from LOB.Customer as c where c.DOB is not null  
```  
  
 <span data-ttu-id="fdedd-115">Le tableau ci-dessous montre le comportement de l'opérateur `IS NULL` sur certains modèles.</span><span class="sxs-lookup"><span data-stu-id="fdedd-115">The following table shows the behavior of `IS NULL` over some patterns.</span></span> <span data-ttu-id="fdedd-116">Toutes les exceptions sont levées côté client avant que le fournisseur soit appelé :</span><span class="sxs-lookup"><span data-stu-id="fdedd-116">All exceptions are thrown from the client side before the provider gets invoked:</span></span>  
  
|<span data-ttu-id="fdedd-117">Motif</span><span class="sxs-lookup"><span data-stu-id="fdedd-117">Pattern</span></span>|<span data-ttu-id="fdedd-118">Comportement</span><span class="sxs-lookup"><span data-stu-id="fdedd-118">Behavior</span></span>|  
|-------------|--------------|  
|<span data-ttu-id="fdedd-119">null IS NULL</span><span class="sxs-lookup"><span data-stu-id="fdedd-119">null IS NULL</span></span>|<span data-ttu-id="fdedd-120">Retourne `true`.</span><span class="sxs-lookup"><span data-stu-id="fdedd-120">Returns `true`.</span></span>|  
|<span data-ttu-id="fdedd-121">TREAT (null AS EntityType) IS NULL</span><span class="sxs-lookup"><span data-stu-id="fdedd-121">TREAT (null AS EntityType) IS NULL</span></span>|<span data-ttu-id="fdedd-122">Retourne `true`.</span><span class="sxs-lookup"><span data-stu-id="fdedd-122">Returns `true`.</span></span>|  
|<span data-ttu-id="fdedd-123">TREAT (null AS ComplexType) IS NULL</span><span class="sxs-lookup"><span data-stu-id="fdedd-123">TREAT (null AS ComplexType) IS NULL</span></span>|<span data-ttu-id="fdedd-124">Génère une erreur.</span><span class="sxs-lookup"><span data-stu-id="fdedd-124">Throws an error.</span></span>|  
|<span data-ttu-id="fdedd-125">TREAT (null AS RowType) IS NULL</span><span class="sxs-lookup"><span data-stu-id="fdedd-125">TREAT (null AS RowType) IS NULL</span></span>|<span data-ttu-id="fdedd-126">Génère une erreur.</span><span class="sxs-lookup"><span data-stu-id="fdedd-126">Throws an error.</span></span>|  
|<span data-ttu-id="fdedd-127">EntityType IS NULL</span><span class="sxs-lookup"><span data-stu-id="fdedd-127">EntityType IS NULL</span></span>|<span data-ttu-id="fdedd-128">Retourne `true` ou la valeur `false`.</span><span class="sxs-lookup"><span data-stu-id="fdedd-128">Returns `true` or `false`.</span></span>|  
|<span data-ttu-id="fdedd-129">ComplexType IS NULL</span><span class="sxs-lookup"><span data-stu-id="fdedd-129">ComplexType IS NULL</span></span>|<span data-ttu-id="fdedd-130">Génère une erreur.</span><span class="sxs-lookup"><span data-stu-id="fdedd-130">Throws an error.</span></span>|  
|<span data-ttu-id="fdedd-131">RowType IS NULL</span><span class="sxs-lookup"><span data-stu-id="fdedd-131">RowType IS NULL</span></span>|<span data-ttu-id="fdedd-132">Génère une erreur.</span><span class="sxs-lookup"><span data-stu-id="fdedd-132">Throws an error.</span></span>|  
  
## <a name="example"></a><span data-ttu-id="fdedd-133">Exemple</span><span class="sxs-lookup"><span data-stu-id="fdedd-133">Example</span></span>  
 <span data-ttu-id="fdedd-134">Ce qui suit [!INCLUDE[esql](../../../../../../includes/esql-md.md)] requête utilise l’opérateur IS NOT NULL pour déterminer si une expression de requête n’est pas null.</span><span class="sxs-lookup"><span data-stu-id="fdedd-134">The following [!INCLUDE[esql](../../../../../../includes/esql-md.md)] query uses the IS NOT NULL operator to determine if a query expression is not null.</span></span> <span data-ttu-id="fdedd-135">Cette requête est basée sur le modèle de vente AdventureWorks Sales Model.</span><span class="sxs-lookup"><span data-stu-id="fdedd-135">The query is based on the AdventureWorks Sales Model.</span></span> <span data-ttu-id="fdedd-136">Pour compiler et exécuter cette requête, procédez comme suit :</span><span class="sxs-lookup"><span data-stu-id="fdedd-136">To compile and run this query, follow these steps:</span></span>  
  
1. <span data-ttu-id="fdedd-137">Suivez la procédure décrite dans [Comment : Exécuter une requête qui retourne des résultats StructuralType](../../../../../../docs/framework/data/adonet/ef/how-to-execute-a-query-that-returns-structuraltype-results.md).</span><span class="sxs-lookup"><span data-stu-id="fdedd-137">Follow the procedure in [How to: Execute a Query that Returns StructuralType Results](../../../../../../docs/framework/data/adonet/ef/how-to-execute-a-query-that-returns-structuraltype-results.md).</span></span>  
  
2. <span data-ttu-id="fdedd-138">Transmettez à la méthode `ExecuteStructuralTypeQuery` la requête suivante en tant qu'argument :</span><span class="sxs-lookup"><span data-stu-id="fdedd-138">Pass the following query as an argument to the `ExecuteStructuralTypeQuery` method:</span></span>  
  
 [!code-csharp[DP EntityServices Concepts 2#ISNULL](../../../../../../samples/snippets/csharp/VS_Snippets_Data/dp entityservices concepts 2/cs/entitysql.cs#isnull)]  
  
## <a name="see-also"></a><span data-ttu-id="fdedd-139">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="fdedd-139">See also</span></span>

- [<span data-ttu-id="fdedd-140">Référence Entity SQL</span><span class="sxs-lookup"><span data-stu-id="fdedd-140">Entity SQL Reference</span></span>](../../../../../../docs/framework/data/adonet/ef/language-reference/entity-sql-reference.md)
