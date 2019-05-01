---
title: 'Procédure : Résoudre des conflits en remplaçant des valeurs de bases de données'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
ms.assetid: fd6db0b8-c29c-48ff-b768-31d28e7a148c
ms.openlocfilehash: 7b8d7cf8ab2335c064062ed3ab4072d81e8042fe
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62033655"
---
# <a name="how-to-resolve-conflicts-by-overwriting-database-values"></a><span data-ttu-id="2988a-102">Procédure : Résoudre des conflits en remplaçant des valeurs de bases de données</span><span class="sxs-lookup"><span data-stu-id="2988a-102">How to: Resolve Conflicts by Overwriting Database Values</span></span>
<span data-ttu-id="2988a-103">Pour harmoniser des différences entre des valeurs de base de données attendues et réelles avant d'essayer de renvoyer vos modifications, vous pouvez utiliser <xref:System.Data.Linq.RefreshMode.KeepCurrentValues> pour remplacer les valeurs de la base de données.</span><span class="sxs-lookup"><span data-stu-id="2988a-103">To reconcile differences between expected and actual database values before you try to resubmit your changes, you can use <xref:System.Data.Linq.RefreshMode.KeepCurrentValues> to overwrite database values.</span></span> <span data-ttu-id="2988a-104">Pour plus d’informations, consultez [d’accès concurrentiel optimiste : Vue d’ensemble](../../../../../../docs/framework/data/adonet/sql/linq/optimistic-concurrency-overview.md).</span><span class="sxs-lookup"><span data-stu-id="2988a-104">For more information, see [Optimistic Concurrency: Overview](../../../../../../docs/framework/data/adonet/sql/linq/optimistic-concurrency-overview.md).</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="2988a-105">Dans tous les cas, l'enregistrement sur le client est actualisé lors de la récupération des données mises à jour de la base de données.</span><span class="sxs-lookup"><span data-stu-id="2988a-105">In all cases, the record on the client is first refreshed by retrieving the updated data from the database.</span></span> <span data-ttu-id="2988a-106">Cette action permet de s'assurer que la prochaine tentative de mise à jour n'échouera pas sur les mêmes vérifications d'accès concurrentiel.</span><span class="sxs-lookup"><span data-stu-id="2988a-106">This action makes sure that the next update try will not fail on the same concurrency checks.</span></span>  
  
## <a name="example"></a><span data-ttu-id="2988a-107">Exemple</span><span class="sxs-lookup"><span data-stu-id="2988a-107">Example</span></span>  
 <span data-ttu-id="2988a-108">Dans ce scénario, une exception <xref:System.Data.Linq.ChangeConflictException> est levée lorsque User1 tente de soumettre des modifications, car User2 a modifié entre-temps les colonnes Assistant et Department.</span><span class="sxs-lookup"><span data-stu-id="2988a-108">In this scenario, an <xref:System.Data.Linq.ChangeConflictException> exception is thrown when User1 tries to submit changes, because User2 has in the meantime changed the Assistant and Department columns.</span></span> <span data-ttu-id="2988a-109">Le tableau suivant présente la situation.</span><span class="sxs-lookup"><span data-stu-id="2988a-109">The following table shows the situation.</span></span>  
  
||<span data-ttu-id="2988a-110">Responsable</span><span class="sxs-lookup"><span data-stu-id="2988a-110">Manager</span></span>|<span data-ttu-id="2988a-111">Assistant</span><span class="sxs-lookup"><span data-stu-id="2988a-111">Assistant</span></span>|<span data-ttu-id="2988a-112">Department</span><span class="sxs-lookup"><span data-stu-id="2988a-112">Department</span></span>|  
|------|-------------|---------------|----------------|  
|<span data-ttu-id="2988a-113">État de la base de données d'origine lors d'une interrogation par User1 et User2.</span><span class="sxs-lookup"><span data-stu-id="2988a-113">Original database state when queried by User1 and User2.</span></span>|<span data-ttu-id="2988a-114">Alfreds</span><span class="sxs-lookup"><span data-stu-id="2988a-114">Alfreds</span></span>|<span data-ttu-id="2988a-115">Maria</span><span class="sxs-lookup"><span data-stu-id="2988a-115">Maria</span></span>|<span data-ttu-id="2988a-116">Sales</span><span class="sxs-lookup"><span data-stu-id="2988a-116">Sales</span></span>|  
|<span data-ttu-id="2988a-117">User1 s'apprête à soumettre ces modifications.</span><span class="sxs-lookup"><span data-stu-id="2988a-117">User1 prepares to submit these changes.</span></span>|<span data-ttu-id="2988a-118">Alfred</span><span class="sxs-lookup"><span data-stu-id="2988a-118">Alfred</span></span>||<span data-ttu-id="2988a-119">Marketing</span><span class="sxs-lookup"><span data-stu-id="2988a-119">Marketing</span></span>|  
|<span data-ttu-id="2988a-120">User2 a déjà soumis ces modifications.</span><span class="sxs-lookup"><span data-stu-id="2988a-120">User2 has already submitted these changes.</span></span>||<span data-ttu-id="2988a-121">Mary</span><span class="sxs-lookup"><span data-stu-id="2988a-121">Mary</span></span>|<span data-ttu-id="2988a-122">Service</span><span class="sxs-lookup"><span data-stu-id="2988a-122">Service</span></span>|  
  
 <span data-ttu-id="2988a-123">User1 décide de résoudre ce conflit en remplaçant des valeurs de base de données par les valeurs de membre client actuelles.</span><span class="sxs-lookup"><span data-stu-id="2988a-123">User1 decides to resolve this conflict by overwriting database values with the current client member values.</span></span>  
  
 <span data-ttu-id="2988a-124">Lorsque User1 résout le conflit à l'aide de <xref:System.Data.Linq.RefreshMode.KeepCurrentValues>, le résultat dans la base de données se présente comme dans le tableau suivant :</span><span class="sxs-lookup"><span data-stu-id="2988a-124">When User1 resolves the conflict by using <xref:System.Data.Linq.RefreshMode.KeepCurrentValues>, the result in the database is as in following table:</span></span>  
  
||<span data-ttu-id="2988a-125">Responsable</span><span class="sxs-lookup"><span data-stu-id="2988a-125">Manager</span></span>|<span data-ttu-id="2988a-126">Assistant</span><span class="sxs-lookup"><span data-stu-id="2988a-126">Assistant</span></span>|<span data-ttu-id="2988a-127">Department</span><span class="sxs-lookup"><span data-stu-id="2988a-127">Department</span></span>|  
|------|-------------|---------------|----------------|  
|<span data-ttu-id="2988a-128">Nouvel état après résolution du conflit.</span><span class="sxs-lookup"><span data-stu-id="2988a-128">New state after conflict resolution.</span></span>|<span data-ttu-id="2988a-129">Alfred</span><span class="sxs-lookup"><span data-stu-id="2988a-129">Alfred</span></span><br /><br /> <span data-ttu-id="2988a-130">(de User1)</span><span class="sxs-lookup"><span data-stu-id="2988a-130">(from User1)</span></span>|<span data-ttu-id="2988a-131">Maria</span><span class="sxs-lookup"><span data-stu-id="2988a-131">Maria</span></span><br /><br /> <span data-ttu-id="2988a-132">(d'origine)</span><span class="sxs-lookup"><span data-stu-id="2988a-132">(original)</span></span>|<span data-ttu-id="2988a-133">Marketing</span><span class="sxs-lookup"><span data-stu-id="2988a-133">Marketing</span></span><br /><br /> <span data-ttu-id="2988a-134">(de User1)</span><span class="sxs-lookup"><span data-stu-id="2988a-134">(from User1)</span></span>|  
  
 <span data-ttu-id="2988a-135">L'exemple suivant montre comment remplacer des valeurs de base de données par des valeurs de membre client actuelles.</span><span class="sxs-lookup"><span data-stu-id="2988a-135">The following example code shows how to overwrite database values with the current client member values.</span></span> <span data-ttu-id="2988a-136">Aucune inspection ni aucune gestion personnalisée des conflits de membres individuels n'est effectuée.</span><span class="sxs-lookup"><span data-stu-id="2988a-136">(No inspection or custom handling of individual member conflicts occurs.)</span></span>  
  
 [!code-csharp[System.Data.Linq.RefreshMode#2](../../../../../../samples/snippets/csharp/VS_Snippets_Data/system.data.linq.refreshmode/cs/program.cs#2)]
 [!code-vb[System.Data.Linq.RefreshMode#2](../../../../../../samples/snippets/visualbasic/VS_Snippets_Data/system.data.linq.refreshmode/vb/module1.vb#2)]  
  
## <a name="see-also"></a><span data-ttu-id="2988a-137">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="2988a-137">See also</span></span>

- [<span data-ttu-id="2988a-138">Guide pratique pour Gérer les conflits de changement</span><span class="sxs-lookup"><span data-stu-id="2988a-138">How to: Manage Change Conflicts</span></span>](../../../../../../docs/framework/data/adonet/sql/linq/how-to-manage-change-conflicts.md)
