---
title: Problèmes connus et éléments à prendre en compte dans LINQ to Entities
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
ms.assetid: acd71129-5ff0-4b4e-b266-c72cc0c53601
ms.openlocfilehash: 3945d4fc92bea2c4212da0507618203603ae8aba
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61780550"
---
# <a name="known-issues-and-considerations-in-linq-to-entities"></a><span data-ttu-id="86e3a-102">Problèmes connus et éléments à prendre en compte dans LINQ to Entities</span><span class="sxs-lookup"><span data-stu-id="86e3a-102">Known Issues and Considerations in LINQ to Entities</span></span>
<span data-ttu-id="86e3a-103">Cette section fournit des informations sur les problèmes connus au niveau des requêtes [!INCLUDE[linq_entities](../../../../../../includes/linq-entities-md.md)].</span><span class="sxs-lookup"><span data-stu-id="86e3a-103">This section provides information about known issues with [!INCLUDE[linq_entities](../../../../../../includes/linq-entities-md.md)] queries.</span></span>  
  
- [<span data-ttu-id="86e3a-104">Requêtes LINQ qui ne peut pas être mis en cache</span><span class="sxs-lookup"><span data-stu-id="86e3a-104">LINQ Queries That cannot be Cached</span></span>](#LINQQueriesThatAreNotCached)  
  
- [<span data-ttu-id="86e3a-105">Perte des informations de classement</span><span class="sxs-lookup"><span data-stu-id="86e3a-105">Ordering Information Lost</span></span>](#OrderingInfoLost)  
  
- [<span data-ttu-id="86e3a-106">Entiers non signés non pris en charge.</span><span class="sxs-lookup"><span data-stu-id="86e3a-106">Unsigned Integers Not Supported</span></span>](#UnsignedIntsUnsupported)  
  
- [<span data-ttu-id="86e3a-107">Erreurs de Conversion de type</span><span class="sxs-lookup"><span data-stu-id="86e3a-107">Type Conversion Errors</span></span>](#TypeConversionErrors)  
  
- [<span data-ttu-id="86e3a-108">Référencement des Variables Non scalaires non pris en charge.</span><span class="sxs-lookup"><span data-stu-id="86e3a-108">Referencing Non-Scalar Variables Not Supported</span></span>](#RefNonScalarClosures)  
  
- [<span data-ttu-id="86e3a-109">Requêtes imbriquées peuvent échouer avec SQL Server 2000</span><span class="sxs-lookup"><span data-stu-id="86e3a-109">Nested Queries May Fail with SQL Server 2000</span></span>](#NestedQueriesSQL2000)  
  
- [<span data-ttu-id="86e3a-110">Projection dans un Type anonyme</span><span class="sxs-lookup"><span data-stu-id="86e3a-110">Projecting to an Anonymous Type</span></span>](#ProjectToAnonymousType)  
  
<a name="LINQQueriesThatAreNotCached"></a>   
## <a name="linq-queries-that-cannot-be-cached"></a><span data-ttu-id="86e3a-111">Requêtes LINQ qui ne peuvent pas être mises en cache</span><span class="sxs-lookup"><span data-stu-id="86e3a-111">LINQ Queries That cannot be Cached</span></span>  
 <span data-ttu-id="86e3a-112">Depuis le .NET Framework 4.5, les requêtes LINQ to Entities sont automatiquement mises en cache.</span><span class="sxs-lookup"><span data-stu-id="86e3a-112">Starting with .NET Framework 4.5, LINQ to Entities queries are automatically cached.</span></span> <span data-ttu-id="86e3a-113">Cependant, les requêtes LINQ to Entities qui appliquent l’opérateur `Enumerable.Contains` aux collections en mémoire ne sont pas automatiquement mises en cache.</span><span class="sxs-lookup"><span data-stu-id="86e3a-113">However, LINQ to Entities queries that apply the `Enumerable.Contains` operator to in-memory collections are not automatically cached.</span></span> <span data-ttu-id="86e3a-114">Le paramétrage des collections en mémoire dans les requêtes LINQ compilées n’est pas autorisé.</span><span class="sxs-lookup"><span data-stu-id="86e3a-114">Also parameterizing in-memory collections in compiled LINQ queries is not allowed.</span></span>  
  
<a name="OrderingInfoLost"></a>   
## <a name="ordering-information-lost"></a><span data-ttu-id="86e3a-115">Perte des informations de tri</span><span class="sxs-lookup"><span data-stu-id="86e3a-115">Ordering Information Lost</span></span>  
 <span data-ttu-id="86e3a-116">La projection de colonnes dans un type anonyme entraînera la perte des informations de tri dans certains requêtes exécutées sur une base de données [!INCLUDE[ssVersion2005](../../../../../../includes/ssversion2005-md.md)] définie à un niveau de compatibilité de « 80 ».</span><span class="sxs-lookup"><span data-stu-id="86e3a-116">Projecting columns into an anonymous type will cause ordering information to be lost in some queries that are executed against a [!INCLUDE[ssVersion2005](../../../../../../includes/ssversion2005-md.md)] database set to a compatibility level of "80".</span></span>  <span data-ttu-id="86e3a-117">Cela se produit lorsqu'un nom de colonne figurant dans la liste Order by correspond à un nom de colonne dans le sélecteur, comme l'illustre l'exemple suivant :</span><span class="sxs-lookup"><span data-stu-id="86e3a-117">This occurs when a column name in the order-by list matches a column name in the selector, as shown in the following example:</span></span>  
  
 [!code-csharp[DP L2E Conceptual Examples#SBUDT543840](../../../../../../samples/snippets/csharp/VS_Snippets_Data/DP L2E Conceptual Examples/CS/Program.cs#sbudt543840)]
 [!code-vb[DP L2E Conceptual Examples#SBUDT543840](../../../../../../samples/snippets/visualbasic/VS_Snippets_Data/DP L2E Conceptual Examples/VB/Module1.vb#sbudt543840)]  
  
<a name="UnsignedIntsUnsupported"></a>   
## <a name="unsigned-integers-not-supported"></a><span data-ttu-id="86e3a-118">Entiers non signés non pris en charge</span><span class="sxs-lookup"><span data-stu-id="86e3a-118">Unsigned Integers Not Supported</span></span>  
 <span data-ttu-id="86e3a-119">La définition d'un type d'entier non signé dans une requête [!INCLUDE[linq_entities](../../../../../../includes/linq-entities-md.md)] n'est pas prise en charge, car [!INCLUDE[adonet_ef](../../../../../../includes/adonet-ef-md.md)] ne prend pas en charge les entiers non signés.</span><span class="sxs-lookup"><span data-stu-id="86e3a-119">Specifying an unsigned integer type in a [!INCLUDE[linq_entities](../../../../../../includes/linq-entities-md.md)] query is not supported because the [!INCLUDE[adonet_ef](../../../../../../includes/adonet-ef-md.md)] does not support unsigned integers.</span></span> <span data-ttu-id="86e3a-120">Si vous spécifiez un entier non signé, un <xref:System.ArgumentException> exception est levée pendant la traduction d’expression de requête, comme illustré dans l’exemple suivant.</span><span class="sxs-lookup"><span data-stu-id="86e3a-120">If you specify an unsigned integer, an <xref:System.ArgumentException> exception will be thrown during the query expression translation, as shown in the following example.</span></span> <span data-ttu-id="86e3a-121">Dans cet exemple, la requête vise à extraire une commande dont le numéro est 48000.</span><span class="sxs-lookup"><span data-stu-id="86e3a-121">This example queries for an order with ID 48000.</span></span>  
  
 [!code-csharp[DP L2E Conceptual Examples#UIntAsQueryParam](../../../../../../samples/snippets/csharp/VS_Snippets_Data/DP L2E Conceptual Examples/CS/Program.cs#uintasqueryparam)]
 [!code-vb[DP L2E Conceptual Examples#UIntAsQueryParam](../../../../../../samples/snippets/visualbasic/VS_Snippets_Data/DP L2E Conceptual Examples/VB/Module1.vb#uintasqueryparam)]  
  
<a name="TypeConversionErrors"></a>   
## <a name="type-conversion-errors"></a><span data-ttu-id="86e3a-122">Erreurs de conversion de type</span><span class="sxs-lookup"><span data-stu-id="86e3a-122">Type Conversion Errors</span></span>  
 <span data-ttu-id="86e3a-123">En Visual Basic, lorsqu'une propriété est mappée à une colonne de type bit SQL Server avec une valeur de 1 à l'aide de la fonction `CByte`, une exception <xref:System.Data.SqlClient.SqlException> est levée avec un message « Erreur de dépassement arithmétique ».</span><span class="sxs-lookup"><span data-stu-id="86e3a-123">In Visual Basic, when a property is mapped to a column of SQL Server bit type with a value of 1 using the `CByte` function, a <xref:System.Data.SqlClient.SqlException> is thrown with an "Arithmetic overflow error" message.</span></span> <span data-ttu-id="86e3a-124">L'exemple suivant interroge la colonne `Product.MakeFlag` dans l'exemple de base de données AdventureWorks et une exception est levée lorsque les résultats de la requête sont itérés.</span><span class="sxs-lookup"><span data-stu-id="86e3a-124">The following example queries the `Product.MakeFlag` column in the AdventureWorks sample database and an exception is thrown when the query results are iterated over.</span></span>  
  
 [!code-vb[DP L2E Conceptual Examples#SBUDT544355](../../../../../../samples/snippets/visualbasic/VS_Snippets_Data/DP L2E Conceptual Examples/VB/Module1.vb#sbudt544355)]  
  
<a name="RefNonScalarClosures"></a>   
## <a name="referencing-non-scalar-variables-not-supported"></a><span data-ttu-id="86e3a-125">Référencement de variables non scalaires non pris en charge</span><span class="sxs-lookup"><span data-stu-id="86e3a-125">Referencing Non-Scalar Variables Not Supported</span></span>  
 <span data-ttu-id="86e3a-126">Le référencement d'une variable non scalaire, telle qu'une entité, dans une requête n'est pas pris en charge.</span><span class="sxs-lookup"><span data-stu-id="86e3a-126">Referencing a non-scalar variables, such as an entity, in a query is not supported.</span></span> <span data-ttu-id="86e3a-127">Lorsqu'une telle requête s'exécute, une exception <xref:System.NotSupportedException> est levée avec un message indiquant « Impossible de créer une valeur constante de type «`EntityType`.</span><span class="sxs-lookup"><span data-stu-id="86e3a-127">When such a query executes, a <xref:System.NotSupportedException> exception is thrown with a message that states "Unable to create a constant value of type `EntityType`.</span></span> <span data-ttu-id="86e3a-128">Seuls les types primitifs (« Int32, String et Guid ») sont pris en charge dans ce contexte. »</span><span class="sxs-lookup"><span data-stu-id="86e3a-128">Only primitive types ('such as Int32, String, and Guid') are supported in this context."</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="86e3a-129">Le référencement d’une collection de variables scalaires est pris en charge.</span><span class="sxs-lookup"><span data-stu-id="86e3a-129">Referencing a collection of scalar variables is supported.</span></span>  
  
 [!code-csharp[DP L2E Conceptual Examples#SBUDT555877](../../../../../../samples/snippets/csharp/VS_Snippets_Data/DP L2E Conceptual Examples/CS/Program.cs#sbudt555877)]
 [!code-vb[DP L2E Conceptual Examples#SBUDT555877](../../../../../../samples/snippets/visualbasic/VS_Snippets_Data/DP L2E Conceptual Examples/VB/Module1.vb#sbudt555877)]  
  
<a name="NestedQueriesSQL2000"></a>   
## <a name="nested-queries-may-fail-with-sql-server-2000"></a><span data-ttu-id="86e3a-130">Les requêtes imbriquées peuvent échouer avec SQL Server 2000</span><span class="sxs-lookup"><span data-stu-id="86e3a-130">Nested Queries May Fail with SQL Server 2000</span></span>  
 <span data-ttu-id="86e3a-131">Avec SQL Server 2000, les requêtes LINQ to Entities peuvent échouer si elles produisent des requêtes Transact-SQL imbriquées qui ont trois niveaux ou plus de profondeur.</span><span class="sxs-lookup"><span data-stu-id="86e3a-131">With SQL Server 2000, LINQ to Entities queries may fail if they produce nested Transact-SQL queries that are three or more levels deep.</span></span>  
  
<a name="ProjectToAnonymousType"></a>   
## <a name="projecting-to-an-anonymous-type"></a><span data-ttu-id="86e3a-132">Projection dans un type anonyme</span><span class="sxs-lookup"><span data-stu-id="86e3a-132">Projecting to an Anonymous Type</span></span>  
 <span data-ttu-id="86e3a-133">Si vous définissez le chemin d’accès de votre requête initiale pour inclure des objets connexes à l’aide de la méthode <xref:System.Data.Objects.ObjectQuery%601.Include%2A> sur <xref:System.Data.Objects.ObjectQuery%601> et si vous utilisez LINQ pour projeter les objets retournés dans un type anonyme, les objets spécifiés dans la méthode d’inclusion ne sont pas inclus dans les résultats de la requête.</span><span class="sxs-lookup"><span data-stu-id="86e3a-133">If you define your initial query path to include related objects by using the <xref:System.Data.Objects.ObjectQuery%601.Include%2A> method on the <xref:System.Data.Objects.ObjectQuery%601> and then use LINQ to project the returned objects to an anonymous type, the objects specified in the include method are not included in the query results.</span></span>  
  
 [!code-csharp[DP L2E Conceptual Examples#ProjToAnonType1](../../../../../../samples/snippets/csharp/VS_Snippets_Data/DP L2E Conceptual Examples/CS/Program.cs#projtoanontype1)]
 [!code-vb[DP L2E Conceptual Examples#ProjToAnonType1](../../../../../../samples/snippets/visualbasic/VS_Snippets_Data/DP L2E Conceptual Examples/VB/Module1.vb#projtoanontype1)]  
  
 <span data-ttu-id="86e3a-134">Pour obtenir des objets connexes, ne projetez pas les types retournés dans un type anonyme.</span><span class="sxs-lookup"><span data-stu-id="86e3a-134">To get related objects, do not project returned types to an anonymous type.</span></span>  
  
 [!code-csharp[DP L2E Conceptual Examples#ProjToAnonType2](../../../../../../samples/snippets/csharp/VS_Snippets_Data/DP L2E Conceptual Examples/CS/Program.cs#projtoanontype2)]
 [!code-vb[DP L2E Conceptual Examples#ProjToAnonType2](../../../../../../samples/snippets/visualbasic/VS_Snippets_Data/DP L2E Conceptual Examples/VB/Module1.vb#projtoanontype2)]  
  
## <a name="see-also"></a><span data-ttu-id="86e3a-135">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="86e3a-135">See also</span></span>

- [<span data-ttu-id="86e3a-136">LINQ to Entities</span><span class="sxs-lookup"><span data-stu-id="86e3a-136">LINQ to Entities</span></span>](../../../../../../docs/framework/data/adonet/ef/language-reference/linq-to-entities.md)
