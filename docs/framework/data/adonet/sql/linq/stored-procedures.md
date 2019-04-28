---
title: Procédures stockées
ms.date: 03/30/2017
ms.assetid: 4d23dd7a-a85f-44ff-a717-af7d0950c0fc
ms.openlocfilehash: 9201965192f300de62679c1e5be75cf98a24e700
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61917941"
---
# <a name="stored-procedures"></a><span data-ttu-id="5736c-102">Procédures stockées</span><span class="sxs-lookup"><span data-stu-id="5736c-102">Stored Procedures</span></span>
[!INCLUDE[vbtecdlinq](../../../../../../includes/vbtecdlinq-md.md)] <span data-ttu-id="5736c-103">utilise des méthodes dans votre modèle objet pour représenter des procédures stockées dans la base de données.</span><span class="sxs-lookup"><span data-stu-id="5736c-103">uses methods in your object model to represent stored procedures in the database.</span></span> <span data-ttu-id="5736c-104">Vous désignez des méthodes comme des procédures stockées en appliquant l'attribut <xref:System.Data.Linq.Mapping.FunctionAttribute> et, si nécessaire, l'attribut <xref:System.Data.Linq.Mapping.ParameterAttribute>.</span><span class="sxs-lookup"><span data-stu-id="5736c-104">You designate methods as stored procedures by applying the <xref:System.Data.Linq.Mapping.FunctionAttribute> attribute and, where required, the <xref:System.Data.Linq.Mapping.ParameterAttribute> attribute.</span></span> <span data-ttu-id="5736c-105">Pour plus d’informations, consultez [le modèle LINQ to SQL objet](../../../../../../docs/framework/data/adonet/sql/linq/the-linq-to-sql-object-model.md).</span><span class="sxs-lookup"><span data-stu-id="5736c-105">For more information, see [The LINQ to SQL Object Model](../../../../../../docs/framework/data/adonet/sql/linq/the-linq-to-sql-object-model.md).</span></span>  
  
 <span data-ttu-id="5736c-106">Les développeurs qui utilisent Visual Studio utilisent généralement le [!INCLUDE[vs_ordesigner_long](../../../../../../includes/vs-ordesigner-long-md.md)] pour mapper des procédures stockées.</span><span class="sxs-lookup"><span data-stu-id="5736c-106">Developers using Visual Studio would typically use the [!INCLUDE[vs_ordesigner_long](../../../../../../includes/vs-ordesigner-long-md.md)] to map stored procedures.</span></span> <span data-ttu-id="5736c-107">Les rubriques de cette section montrent comment former et appeler ces méthodes dans votre application si vous écrivez vous-même le code.</span><span class="sxs-lookup"><span data-stu-id="5736c-107">The topics in this section show how to form and call these methods in your application if you write the code yourself.</span></span>  
  
## <a name="in-this-section"></a><span data-ttu-id="5736c-108">Dans cette section</span><span class="sxs-lookup"><span data-stu-id="5736c-108">In This Section</span></span>  
 [<span data-ttu-id="5736c-109">Guide pratique pour Retourner des ensembles de lignes</span><span class="sxs-lookup"><span data-stu-id="5736c-109">How to: Return Rowsets</span></span>](../../../../../../docs/framework/data/adonet/sql/linq/how-to-return-rowsets.md)  
 <span data-ttu-id="5736c-110">Décrit comment retourner des lignes de données et comment utiliser un paramètre d'entrée.</span><span class="sxs-lookup"><span data-stu-id="5736c-110">Describes how to return rows of data and shows how to use an input parameter.</span></span>  
  
 [<span data-ttu-id="5736c-111">Guide pratique pour Utiliser des procédures stockées qui prennent des paramètres</span><span class="sxs-lookup"><span data-stu-id="5736c-111">How to: Use Stored Procedures that Take Parameters</span></span>](../../../../../../docs/framework/data/adonet/sql/linq/how-to-use-stored-procedures-that-take-parameters.md)  
 <span data-ttu-id="5736c-112">Décrit comment utiliser des paramètres d'entrée et de sortie.</span><span class="sxs-lookup"><span data-stu-id="5736c-112">Describes how to use input and output parameters.</span></span>  
  
 [<span data-ttu-id="5736c-113">Guide pratique pour Utilisez les procédures stockées mappées pour plusieurs formes de résultats</span><span class="sxs-lookup"><span data-stu-id="5736c-113">How to: Use Stored Procedures Mapped for Multiple Result Shapes</span></span>](../../../../../../docs/framework/data/adonet/sql/linq/how-to-use-stored-procedures-mapped-for-multiple-result-shapes.md)  
 <span data-ttu-id="5736c-114">Explique comment permettre le retour de plusieurs formes dans la même procédure stockée.</span><span class="sxs-lookup"><span data-stu-id="5736c-114">Describes how to provide for returns of multiple shapes in the same stored procedure.</span></span>  
  
 [<span data-ttu-id="5736c-115">Guide pratique pour Utiliser des procédures stockées mappées pour des formes de résultats séquentielles</span><span class="sxs-lookup"><span data-stu-id="5736c-115">How to: Use Stored Procedures Mapped for Sequential Result Shapes</span></span>](../../../../../../docs/framework/data/adonet/sql/linq/how-to-use-stored-procedures-mapped-for-sequential-result-shapes.md)  
 <span data-ttu-id="5736c-116">Explique comment permettre plusieurs formes lorsque la séquence de retour est connue.</span><span class="sxs-lookup"><span data-stu-id="5736c-116">Describes how to provide for multiple shapes where the return sequence is known.</span></span>  
  
 [<span data-ttu-id="5736c-117">Personnalisation d’opérations à l’aide de procédures stockées</span><span class="sxs-lookup"><span data-stu-id="5736c-117">Customizing Operations By Using Stored Procedures</span></span>](../../../../../../docs/framework/data/adonet/sql/linq/customizing-operations-by-using-stored-procedures.md)  
 <span data-ttu-id="5736c-118">Explique comment utiliser des procédures stockées pour implémenter les opérations d'insertion, de mise à jour et de suppression.</span><span class="sxs-lookup"><span data-stu-id="5736c-118">Describes how to use stored procedures to implement insert, update, and delete operations.</span></span>  
  
 [<span data-ttu-id="5736c-119">Personnalisation d’opérations à l’aide de procédures stockées uniquement</span><span class="sxs-lookup"><span data-stu-id="5736c-119">Customizing Operations by Using Stored Procedures Exclusively</span></span>](../../../../../../docs/framework/data/adonet/sql/linq/customizing-operations-by-using-stored-procedures-exclusively.md)  
 <span data-ttu-id="5736c-120">Explique comment utiliser uniquement des procédures stockées pour implémenter les opérations d'insertion, de mise à jour et de suppression.</span><span class="sxs-lookup"><span data-stu-id="5736c-120">Describes how to use nothing but stored procedures to implement insert, update, and delete operations.</span></span>  
  
## <a name="related-sections"></a><span data-ttu-id="5736c-121">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="5736c-121">Related Sections</span></span>  
 [<span data-ttu-id="5736c-122">Guide de programmation</span><span class="sxs-lookup"><span data-stu-id="5736c-122">Programming Guide</span></span>](../../../../../../docs/framework/data/adonet/sql/linq/programming-guide.md)  
 <span data-ttu-id="5736c-123">Fournit des informations sur la création et l'utilisation de votre modèle objet [!INCLUDE[vbtecdlinq](../../../../../../includes/vbtecdlinq-md.md)].</span><span class="sxs-lookup"><span data-stu-id="5736c-123">Provides information about how to create and use your [!INCLUDE[vbtecdlinq](../../../../../../includes/vbtecdlinq-md.md)] object model.</span></span>  
  
 [<span data-ttu-id="5736c-124">Procédure pas à pas : À l’aide de procédures stockées uniquement (Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="5736c-124">Walkthrough: Using Only Stored Procedures (Visual Basic)</span></span>](../../../../../../docs/framework/data/adonet/sql/linq/walkthrough-using-only-stored-procedures-visual-basic.md)  
 <span data-ttu-id="5736c-125">Inclut des procédures qui expliquent comment utiliser des procédures stockées dans Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="5736c-125">Includes procedures that illustrate how to use stored procedures in Visual Basic.</span></span>  
  
 [<span data-ttu-id="5736c-126">Procédure pas à pas : À l’aide de procédures stockées uniquement (C#)</span><span class="sxs-lookup"><span data-stu-id="5736c-126">Walkthrough: Using Only Stored Procedures (C#)</span></span>](../../../../../../docs/framework/data/adonet/sql/linq/walkthrough-using-only-stored-procedures-csharp.md)  
 <span data-ttu-id="5736c-127">Inclut des procédures qui expliquent comment utiliser des procédures stockées dans C#.</span><span class="sxs-lookup"><span data-stu-id="5736c-127">Includes procedures that illustrate how to use stored procedures in C#.</span></span>
