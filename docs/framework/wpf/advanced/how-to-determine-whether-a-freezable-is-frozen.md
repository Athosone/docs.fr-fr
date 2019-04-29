---
title: 'Procédure : Déterminer si un Freezable est gelé'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- Freezable objects [WPF], determining if frozen
ms.assetid: 92e58baa-ee12-4a9e-ac3a-ca458807a8b2
ms.openlocfilehash: 6a63862d35f2c40289ea6445eb3dab8a2abe4a61
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61776231"
---
# <a name="how-to-determine-whether-a-freezable-is-frozen"></a><span data-ttu-id="7d82d-102">Procédure : Déterminer si un Freezable est gelé</span><span class="sxs-lookup"><span data-stu-id="7d82d-102">How to: Determine Whether a Freezable Is Frozen</span></span>
<span data-ttu-id="7d82d-103">Cet exemple montre comment déterminer si un <xref:System.Windows.Freezable> objet est figé.</span><span class="sxs-lookup"><span data-stu-id="7d82d-103">This example shows how to determine whether a <xref:System.Windows.Freezable> object is frozen.</span></span> <span data-ttu-id="7d82d-104">Si vous essayez de modifier un objet figé <xref:System.Windows.Freezable> de l’objet, elle lève une <xref:System.InvalidOperationException>.</span><span class="sxs-lookup"><span data-stu-id="7d82d-104">If you try to modify a frozen <xref:System.Windows.Freezable> object, it throws an <xref:System.InvalidOperationException>.</span></span> <span data-ttu-id="7d82d-105">Pour éviter de lever cette exception, utilisez la <xref:System.Windows.Freezable.IsFrozen%2A> propriété de la <xref:System.Windows.Freezable> objet afin de déterminer si elle est figée.</span><span class="sxs-lookup"><span data-stu-id="7d82d-105">To avoid throwing this exception, use the <xref:System.Windows.Freezable.IsFrozen%2A> property of the <xref:System.Windows.Freezable> object to determine whether it is frozen.</span></span>  
  
## <a name="example"></a><span data-ttu-id="7d82d-106">Exemple</span><span class="sxs-lookup"><span data-stu-id="7d82d-106">Example</span></span>  
 <span data-ttu-id="7d82d-107">L’exemple suivant se fige un <xref:System.Windows.Media.SolidColorBrush> , puis le teste à l’aide de la <xref:System.Windows.Freezable.IsFrozen%2A> propriété afin de déterminer si elle est figée.</span><span class="sxs-lookup"><span data-stu-id="7d82d-107">The following example freezes a <xref:System.Windows.Media.SolidColorBrush> and then tests it by using the <xref:System.Windows.Freezable.IsFrozen%2A> property to determine whether it is frozen.</span></span>  
  
 [!code-csharp[freezablesample_procedural#CheckIsFrozenExample](~/samples/snippets/csharp/VS_Snippets_Wpf/freezablesample_procedural/CSharp/freezablesample.cs#checkisfrozenexample)]
 [!code-vb[freezablesample_procedural#CheckIsFrozenExample](~/samples/snippets/visualbasic/VS_Snippets_Wpf/freezablesample_procedural/visualbasic/freezablesample.vb#checkisfrozenexample)]  
  
 <span data-ttu-id="7d82d-108">Pour plus d’informations sur <xref:System.Windows.Freezable> , voir la [vue d’ensemble des objets Freezable](freezable-objects-overview.md).</span><span class="sxs-lookup"><span data-stu-id="7d82d-108">For more information about <xref:System.Windows.Freezable> objects, see the [Freezable Objects Overview](freezable-objects-overview.md).</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="7d82d-109">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="7d82d-109">See also</span></span>

- <xref:System.Windows.Freezable>
- <xref:System.Windows.Freezable.IsFrozen%2A>
- [<span data-ttu-id="7d82d-110">Vue d’ensemble des objets Freezable</span><span class="sxs-lookup"><span data-stu-id="7d82d-110">Freezable Objects Overview</span></span>](freezable-objects-overview.md)
- [<span data-ttu-id="7d82d-111">Rubriques de guide pratique</span><span class="sxs-lookup"><span data-stu-id="7d82d-111">How-to Topics</span></span>](base-elements-how-to-topics.md)
