---
title: 'Procédure : Redimensionner un canevas à l’aide d’un curseur'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- resizing Canvas control [WPF]
- controls [WPF], Thumb
- controls [WPF], Canvas
- Thumb control [WPF]
- Canvas control [WPF]
ms.assetid: 7dc9f435-726c-4d4d-be41-eb24cfe17bef
ms.openlocfilehash: 14942157429b029147d47e2f88428c56e66523d1
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61770745"
---
# <a name="how-to-resize-a-canvas-by-using-a-thumb"></a><span data-ttu-id="b4bd3-102">Procédure : Redimensionner un canevas à l’aide d’un curseur</span><span class="sxs-lookup"><span data-stu-id="b4bd3-102">How to: Resize a Canvas by Using a Thumb</span></span>
<span data-ttu-id="b4bd3-103">Cet exemple montre comment utiliser un <xref:System.Windows.Controls.Primitives.Thumb> contrôle pour redimensionner un <xref:System.Windows.Controls.Canvas> contrôle.</span><span class="sxs-lookup"><span data-stu-id="b4bd3-103">This example shows how to use a <xref:System.Windows.Controls.Primitives.Thumb> control to resize a <xref:System.Windows.Controls.Canvas> control.</span></span>  
  
## <a name="example"></a><span data-ttu-id="b4bd3-104">Exemple</span><span class="sxs-lookup"><span data-stu-id="b4bd3-104">Example</span></span>  
 <span data-ttu-id="b4bd3-105">Le <xref:System.Windows.Controls.Primitives.Thumb> contrôle fournit des fonctionnalités de glissement qui peuvent être utilisée pour déplacer ou redimensionner des contrôles en surveillant le <xref:System.Windows.Controls.Primitives.Thumb.DragStarted>, <xref:System.Windows.Controls.Primitives.Thumb.DragDelta> et <xref:System.Windows.Controls.Primitives.Thumb.DragCompleted> événements de la <xref:System.Windows.Controls.Primitives.Thumb>.</span><span class="sxs-lookup"><span data-stu-id="b4bd3-105">The <xref:System.Windows.Controls.Primitives.Thumb> control provides drag functionality that can be used to move or resize controls by monitoring the <xref:System.Windows.Controls.Primitives.Thumb.DragStarted>, <xref:System.Windows.Controls.Primitives.Thumb.DragDelta> and <xref:System.Windows.Controls.Primitives.Thumb.DragCompleted> events of the <xref:System.Windows.Controls.Primitives.Thumb>.</span></span>  
  
 <span data-ttu-id="b4bd3-106">L’utilisateur commence une opération glisser en appuyant sur le bouton gauche de la souris lorsque le pointeur de la souris est en pause sur le <xref:System.Windows.Controls.Primitives.Thumb> contrôle.</span><span class="sxs-lookup"><span data-stu-id="b4bd3-106">The user begins a drag operation by pressing the left mouse button when the mouse pointer is paused on the <xref:System.Windows.Controls.Primitives.Thumb> control.</span></span> <span data-ttu-id="b4bd3-107">L’opération glisser se poursuit aussi longtemps que le bouton gauche de la souris est enfoncé.</span><span class="sxs-lookup"><span data-stu-id="b4bd3-107">The drag operation continues as long as the left mouse button remains pressed.</span></span> <span data-ttu-id="b4bd3-108">Pendant l’opération glisser, la <xref:System.Windows.Controls.Primitives.Thumb.DragDelta> peut se produire plusieurs fois.</span><span class="sxs-lookup"><span data-stu-id="b4bd3-108">During the drag operation, the <xref:System.Windows.Controls.Primitives.Thumb.DragDelta> can occur more than once.</span></span> <span data-ttu-id="b4bd3-109">Chaque fois qu’il se produit, le <xref:System.Windows.Controls.Primitives.DragDeltaEventArgs> classe fournit la modification de la position qui correspond à la modification de la position de la souris.</span><span class="sxs-lookup"><span data-stu-id="b4bd3-109">Each time it occurs, the <xref:System.Windows.Controls.Primitives.DragDeltaEventArgs> class provides the change in position that corresponds to the change in mouse position.</span></span> <span data-ttu-id="b4bd3-110">Lorsque l’utilisateur relâche le bouton gauche de la souris, l’opération glisser est terminée.</span><span class="sxs-lookup"><span data-stu-id="b4bd3-110">When the user releases the left mouse button, the drag operation is finished.</span></span> <span data-ttu-id="b4bd3-111">L’opération glisser fournit uniquement les nouvelles coordonnées ; elle ne repositionne pas automatiquement le <xref:System.Windows.Controls.Primitives.Thumb>.</span><span class="sxs-lookup"><span data-stu-id="b4bd3-111">The drag operation only provides new coordinates; it does not automatically reposition the <xref:System.Windows.Controls.Primitives.Thumb>.</span></span>  
  
 <span data-ttu-id="b4bd3-112">L’exemple suivant montre un <xref:System.Windows.Controls.Primitives.Thumb> contrôle qui est l’élément enfant d’un <xref:System.Windows.Controls.Canvas> contrôle.</span><span class="sxs-lookup"><span data-stu-id="b4bd3-112">The following example shows a <xref:System.Windows.Controls.Primitives.Thumb> control that is the child element of a <xref:System.Windows.Controls.Canvas> control.</span></span> <span data-ttu-id="b4bd3-113">Le Gestionnaire d’événements pour son <xref:System.Windows.Controls.Primitives.Thumb.DragDelta> événement fournit la logique pour déplacer le <xref:System.Windows.Controls.Primitives.Thumb> et redimensionner le <xref:System.Windows.Controls.Canvas>.</span><span class="sxs-lookup"><span data-stu-id="b4bd3-113">The event handler for its <xref:System.Windows.Controls.Primitives.Thumb.DragDelta> event provides the logic to move the <xref:System.Windows.Controls.Primitives.Thumb> and resize the <xref:System.Windows.Controls.Canvas>.</span></span> <span data-ttu-id="b4bd3-114">Les gestionnaires d’événements pour le <xref:System.Windows.Controls.Primitives.Thumb.DragStarted> et <xref:System.Windows.Controls.Primitives.Thumb.DragCompleted> événement modifier la couleur de la <xref:System.Windows.Controls.Primitives.Thumb> pendant une opération glisser.</span><span class="sxs-lookup"><span data-stu-id="b4bd3-114">The event handlers for the <xref:System.Windows.Controls.Primitives.Thumb.DragStarted> and <xref:System.Windows.Controls.Primitives.Thumb.DragCompleted> event change the color of the <xref:System.Windows.Controls.Primitives.Thumb> during a drag operation.</span></span> <span data-ttu-id="b4bd3-115">L’exemple suivant définit la <xref:System.Windows.Controls.Primitives.Thumb>.</span><span class="sxs-lookup"><span data-stu-id="b4bd3-115">The following example defines the <xref:System.Windows.Controls.Primitives.Thumb>.</span></span>  
  
 [!code-xaml[Thumb#thumb](~/samples/snippets/csharp/VS_Snippets_Wpf/Thumb/CSharp/Pane1.xaml#thumb)]  
  
 <span data-ttu-id="b4bd3-116">L’exemple suivant montre le <xref:System.Windows.Controls.Primitives.Thumb.DragDelta> Gestionnaire d’événements qui déplace les <xref:System.Windows.Controls.Primitives.Thumb> et redimensionne le <xref:System.Windows.Controls.Canvas> en réponse à un mouvement de souris.</span><span class="sxs-lookup"><span data-stu-id="b4bd3-116">The following example shows the <xref:System.Windows.Controls.Primitives.Thumb.DragDelta> event handler that moves the <xref:System.Windows.Controls.Primitives.Thumb> and resizes the <xref:System.Windows.Controls.Canvas> in response to a mouse movement.</span></span>  
  
 [!code-csharp[Thumb#2](~/samples/snippets/csharp/VS_Snippets_Wpf/Thumb/CSharp/Pane1.xaml.cs#2)]  
  
 <span data-ttu-id="b4bd3-117">L’exemple suivant montre le <xref:System.Windows.Controls.Primitives.Thumb.DragStarted> Gestionnaire d’événements.</span><span class="sxs-lookup"><span data-stu-id="b4bd3-117">The following example shows the <xref:System.Windows.Controls.Primitives.Thumb.DragStarted> event handler.</span></span>  
  
 [!code-csharp[Thumb#DragStartedHandler](~/samples/snippets/csharp/VS_Snippets_Wpf/Thumb/CSharp/Pane1.xaml.cs#dragstartedhandler)]
 [!code-vb[Thumb#DragStartedHandler](~/samples/snippets/visualbasic/VS_Snippets_Wpf/Thumb/VisualBasic/Pane1.xaml.vb#dragstartedhandler)]  
  
 <span data-ttu-id="b4bd3-118">L’exemple suivant montre le <xref:System.Windows.Controls.Primitives.Thumb.DragCompleted> Gestionnaire d’événements.</span><span class="sxs-lookup"><span data-stu-id="b4bd3-118">The following example shows the <xref:System.Windows.Controls.Primitives.Thumb.DragCompleted> event handler.</span></span>  
  
 [!code-csharp[Thumb#DragCompletedHandler](~/samples/snippets/csharp/VS_Snippets_Wpf/Thumb/CSharp/Pane1.xaml.cs#dragcompletedhandler)]
 [!code-vb[Thumb#DragCompletedHandler](~/samples/snippets/visualbasic/VS_Snippets_Wpf/Thumb/VisualBasic/Pane1.xaml.vb#dragcompletedhandler)]  
  
 <span data-ttu-id="b4bd3-119">Pour obtenir un exemple complet, consultez [exemple de fonctionnalité de glisser Thumb](https://go.microsoft.com/fwlink/?LinkID=160042).</span><span class="sxs-lookup"><span data-stu-id="b4bd3-119">For the complete sample, see [Thumb Drag Functionality Sample](https://go.microsoft.com/fwlink/?LinkID=160042).</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="b4bd3-120">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b4bd3-120">See also</span></span>

- <xref:System.Windows.Controls.Primitives.Thumb>
- <xref:System.Windows.Controls.Primitives.Thumb.DragStarted>
- <xref:System.Windows.Controls.Primitives.Thumb.DragDelta>
- <xref:System.Windows.Controls.Primitives.Thumb.DragCompleted>
