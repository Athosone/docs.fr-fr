---
title: 'Procédure : Mettre un Freezable en lecture seule'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- Freezable objects [WPF], making read-only
ms.assetid: 6c544b7d-d3c9-4736-aa90-4b8728234ccb
ms.openlocfilehash: 9b7102db4de0df7183355e50e3b372eac30d81b3
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59191436"
---
# <a name="how-to-make-a-freezable-read-only"></a><span data-ttu-id="5308a-102">Procédure : Mettre un Freezable en lecture seule</span><span class="sxs-lookup"><span data-stu-id="5308a-102">How to: Make a Freezable Read-Only</span></span>
<span data-ttu-id="5308a-103">Cet exemple montre comment rendre un <xref:System.Windows.Freezable> en lecture seule en appelant son <xref:System.Windows.Freezable.Freeze%2A> (méthode).</span><span class="sxs-lookup"><span data-stu-id="5308a-103">This example shows how to make a <xref:System.Windows.Freezable> read-only by calling its <xref:System.Windows.Freezable.Freeze%2A> method.</span></span>  
  
 <span data-ttu-id="5308a-104">Vous ne pouvez pas figer un <xref:System.Windows.Freezable> objet si l’une des conditions suivantes est `true` sur l’objet :</span><span class="sxs-lookup"><span data-stu-id="5308a-104">You cannot freeze a <xref:System.Windows.Freezable> object if any one of the following conditions is `true` about the object:</span></span>  
  
-   <span data-ttu-id="5308a-105">Il a animé ou propriétés liées aux données.</span><span class="sxs-lookup"><span data-stu-id="5308a-105">It has animated or data bound properties.</span></span>  
  
-   <span data-ttu-id="5308a-106">Il possède des propriétés qui sont définies par une ressource dynamique.</span><span class="sxs-lookup"><span data-stu-id="5308a-106">It has properties that are set by a dynamic resource.</span></span> <span data-ttu-id="5308a-107">Pour plus d’informations sur les ressources dynamiques, consultez le [XAML ressources](xaml-resources.md).</span><span class="sxs-lookup"><span data-stu-id="5308a-107">For more information about dynamic resources, see the [XAML Resources](xaml-resources.md).</span></span>  
  
-   <span data-ttu-id="5308a-108">Il contient <xref:System.Windows.Freezable> sous-objets qui ne peut pas être figés.</span><span class="sxs-lookup"><span data-stu-id="5308a-108">It contains <xref:System.Windows.Freezable> sub-objects that cannot be frozen.</span></span>  
  
 <span data-ttu-id="5308a-109">Si ces conditions sont `false` pour votre <xref:System.Windows.Freezable> objet et que vous ne souhaitez pas modifier, envisagez de geler pour profiter des avantages de performances.</span><span class="sxs-lookup"><span data-stu-id="5308a-109">If these conditions are `false` for your <xref:System.Windows.Freezable> object and you do not intend to modify it, consider freezing it to gain performance benefits.</span></span>  
  
## <a name="example"></a><span data-ttu-id="5308a-110">Exemple</span><span class="sxs-lookup"><span data-stu-id="5308a-110">Example</span></span>  
 <span data-ttu-id="5308a-111">L’exemple suivant se fige un <xref:System.Windows.Media.SolidColorBrush>, qui est un type de <xref:System.Windows.Freezable> objet.</span><span class="sxs-lookup"><span data-stu-id="5308a-111">The following example freezes a <xref:System.Windows.Media.SolidColorBrush>, which is a type of <xref:System.Windows.Freezable> object.</span></span>  
  
 [!code-csharp[freezablesample_procedural#FreezeExample1](~/samples/snippets/csharp/VS_Snippets_Wpf/freezablesample_procedural/CSharp/freezablesample.cs#freezeexample1)]
 [!code-vb[freezablesample_procedural#FreezeExample1](~/samples/snippets/visualbasic/VS_Snippets_Wpf/freezablesample_procedural/visualbasic/freezablesample.vb#freezeexample1)]  
  
 <span data-ttu-id="5308a-112">Pour plus d’informations sur <xref:System.Windows.Freezable> , voir la [vue d’ensemble des objets Freezable](freezable-objects-overview.md).</span><span class="sxs-lookup"><span data-stu-id="5308a-112">For more information about <xref:System.Windows.Freezable> objects, see the [Freezable Objects Overview](freezable-objects-overview.md).</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="5308a-113">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="5308a-113">See also</span></span>

- <xref:System.Windows.Freezable>
- <xref:System.Windows.Freezable.CanFreeze%2A>
- <xref:System.Windows.Freezable.Freeze%2A>
- [<span data-ttu-id="5308a-114">Vue d’ensemble des objets Freezable</span><span class="sxs-lookup"><span data-stu-id="5308a-114">Freezable Objects Overview</span></span>](freezable-objects-overview.md)
- [<span data-ttu-id="5308a-115">Rubriques de guide pratique</span><span class="sxs-lookup"><span data-stu-id="5308a-115">How-to Topics</span></span>](base-elements-how-to-topics.md)
