---
title: 'Procédure : afficher manuellement les graphismes mis en mémoire tampon'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- flicker [Windows Forms], reducing by manually rendering graphics
- graphics [Windows Forms], rendering
ms.assetid: 5192295e-bd8e-45f7-8bd6-5c4f6bd21e61
ms.openlocfilehash: 48dd1d76a42661df6ba642c032c991be4d6a2900
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61756583"
---
# <a name="how-to-manually-render-buffered-graphics"></a><span data-ttu-id="66e39-102">Procédure : afficher manuellement les graphismes mis en mémoire tampon</span><span class="sxs-lookup"><span data-stu-id="66e39-102">How to: Manually Render Buffered Graphics</span></span>
<span data-ttu-id="66e39-103">Si vous gérez vos propres graphismes mis en mémoire tampon, vous devez pouvoir créer et restituer des mémoires tampon de graphiques.</span><span class="sxs-lookup"><span data-stu-id="66e39-103">If you are managing your own buffered graphics, you will need to be able to create and render graphics buffers.</span></span> <span data-ttu-id="66e39-104">Vous pouvez créer des instances de la classe <xref:System.Drawing.BufferedGraphics> associée aux surfaces de dessin sur votre écran en appelant la méthode <xref:System.Drawing.BufferedGraphicsContext.Allocate%2A>.</span><span class="sxs-lookup"><span data-stu-id="66e39-104">You can create instances of the <xref:System.Drawing.BufferedGraphics> class that is associated with drawing surfaces on your screen by calling the <xref:System.Drawing.BufferedGraphicsContext.Allocate%2A> method.</span></span> <span data-ttu-id="66e39-105">Cette méthode crée une instance de <xref:System.Drawing.BufferedGraphics> associée à une surface de rendu particulière, comme un formulaire ou un contrôle.</span><span class="sxs-lookup"><span data-stu-id="66e39-105">This method creates a <xref:System.Drawing.BufferedGraphics> instance that is associated with a particular rendering surface, such as a form or control.</span></span> <span data-ttu-id="66e39-106">Après avoir créé une instance de <xref:System.Drawing.BufferedGraphics>, vous pouvez dessiner des graphismes dans la mémoire tampon qu'elle représente par le biais de la propriété <xref:System.Drawing.BufferedGraphics.Graphics%2A>.</span><span class="sxs-lookup"><span data-stu-id="66e39-106">After you have created a <xref:System.Drawing.BufferedGraphics> instance, you can draw graphics to the buffer it represents through the <xref:System.Drawing.BufferedGraphics.Graphics%2A> property.</span></span> <span data-ttu-id="66e39-107">Après avoir effectué toutes les opérations graphiques, vous pouvez copier le contenu de la mémoire tampon à l'écran en appelant la méthode <xref:System.Drawing.BufferedGraphics.Render%2A>.</span><span class="sxs-lookup"><span data-stu-id="66e39-107">After you have performed all graphics operations, you can copy the contents of the buffer to the screen by calling the <xref:System.Drawing.BufferedGraphics.Render%2A> method.</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="66e39-108">Si vous effectuez votre propre rendu, la consommation de mémoire augmentera, bien que cette augmentation puisse être très légère.</span><span class="sxs-lookup"><span data-stu-id="66e39-108">If you perform your own rendering, memory consumption will increase, though the increase may only be slight.</span></span>  
  
### <a name="to-manually-display-buffered-graphics"></a><span data-ttu-id="66e39-109">Pour afficher manuellement des graphismes mis en mémoire tampon</span><span class="sxs-lookup"><span data-stu-id="66e39-109">To manually display buffered graphics</span></span>  
  
1. <span data-ttu-id="66e39-110">Obtenez une référence à une instance de la classe <xref:System.Drawing.BufferedGraphicsContext>.</span><span class="sxs-lookup"><span data-stu-id="66e39-110">Obtain a reference to an instance of the <xref:System.Drawing.BufferedGraphicsContext> class.</span></span> <span data-ttu-id="66e39-111">Pour plus d'informations, voir [Procédure : Gérer manuellement des graphiques mis en mémoire tampon](how-to-manually-manage-buffered-graphics.md).</span><span class="sxs-lookup"><span data-stu-id="66e39-111">For more information, see [How to: Manually Manage Buffered Graphics](how-to-manually-manage-buffered-graphics.md).</span></span>  
  
2. <span data-ttu-id="66e39-112">Créez une instance de la classe <xref:System.Drawing.BufferedGraphics> en appelant la méthode <xref:System.Drawing.BufferedGraphicsContext.Allocate%2A>, comme indiqué dans l'exemple de code suivant.</span><span class="sxs-lookup"><span data-stu-id="66e39-112">Create an instance of the <xref:System.Drawing.BufferedGraphics> class by calling the <xref:System.Drawing.BufferedGraphicsContext.Allocate%2A> method, as shown in the following code example.</span></span>  
  
     [!code-csharp[System.Windows.Forms.LegacyBufferedGraphics#21](~/samples/snippets/csharp/VS_Snippets_Winforms/System.Windows.Forms.LegacyBufferedGraphics/CS/Class1.cs#21)]
     [!code-vb[System.Windows.Forms.LegacyBufferedGraphics#21](~/samples/snippets/visualbasic/VS_Snippets_Winforms/System.Windows.Forms.LegacyBufferedGraphics/VB/Class1.vb#21)]  
  
3. <span data-ttu-id="66e39-113">Dessinez des graphismes dans la mémoire tampon de graphiques en définissant la propriété <xref:System.Drawing.BufferedGraphics.Graphics%2A>.</span><span class="sxs-lookup"><span data-stu-id="66e39-113">Draw graphics to the graphics buffer by setting the <xref:System.Drawing.BufferedGraphics.Graphics%2A> property.</span></span> <span data-ttu-id="66e39-114">Exemple :</span><span class="sxs-lookup"><span data-stu-id="66e39-114">For example:</span></span>  
  
     [!code-csharp[System.Windows.Forms.LegacyBufferedGraphics#22](~/samples/snippets/csharp/VS_Snippets_Winforms/System.Windows.Forms.LegacyBufferedGraphics/CS/Class1.cs#22)]
     [!code-vb[System.Windows.Forms.LegacyBufferedGraphics#22](~/samples/snippets/visualbasic/VS_Snippets_Winforms/System.Windows.Forms.LegacyBufferedGraphics/VB/Class1.vb#22)]  
  
4. <span data-ttu-id="66e39-115">Quand vous avez terminé toutes vos opérations de dessin dans la mémoire tampon de graphiques, appelez la méthode <xref:System.Drawing.BufferedGraphics.Render%2A> pour restituer la mémoire tampon, soit sur la surface de dessin associée à cette mémoire tampon, soit sur une surface de dessin spécifiée, comme illustré dans l'exemple de code suivant.</span><span class="sxs-lookup"><span data-stu-id="66e39-115">When you have completed all of your drawing operations to the graphics buffer, call the <xref:System.Drawing.BufferedGraphics.Render%2A> method to render the buffer, either to the drawing surface associated with that buffer, or to a specified drawing surface, as shown in the following code example.</span></span>  
  
     [!code-csharp[System.Windows.Forms.LegacyBufferedGraphics#23](~/samples/snippets/csharp/VS_Snippets_Winforms/System.Windows.Forms.LegacyBufferedGraphics/CS/Class1.cs#23)]
     [!code-vb[System.Windows.Forms.LegacyBufferedGraphics#23](~/samples/snippets/visualbasic/VS_Snippets_Winforms/System.Windows.Forms.LegacyBufferedGraphics/VB/Class1.vb#23)]  
  
5. <span data-ttu-id="66e39-116">Quand vous avez terminé d'afficher les graphismes, appelez la méthode `Dispose` sur l'instance de <xref:System.Drawing.BufferedGraphics> pour libérer les ressources système.</span><span class="sxs-lookup"><span data-stu-id="66e39-116">After you are finished rendering graphics, call the `Dispose` method on the <xref:System.Drawing.BufferedGraphics> instance to free system resources.</span></span>  
  
     [!code-csharp[System.Windows.Forms.LegacyBufferedGraphics#24](~/samples/snippets/csharp/VS_Snippets_Winforms/System.Windows.Forms.LegacyBufferedGraphics/CS/Class1.cs#24)]
     [!code-vb[System.Windows.Forms.LegacyBufferedGraphics#24](~/samples/snippets/visualbasic/VS_Snippets_Winforms/System.Windows.Forms.LegacyBufferedGraphics/VB/Class1.vb#24)]  
  
## <a name="see-also"></a><span data-ttu-id="66e39-117">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="66e39-117">See also</span></span>

- <xref:System.Drawing.BufferedGraphicsContext>
- <xref:System.Drawing.BufferedGraphics>
- [<span data-ttu-id="66e39-118">Graphiques mis deux fois en mémoire tampon</span><span class="sxs-lookup"><span data-stu-id="66e39-118">Double Buffered Graphics</span></span>](double-buffered-graphics.md)
- [<span data-ttu-id="66e39-119">Guide pratique pour Gérer manuellement des graphiques mis en mémoire tampon</span><span class="sxs-lookup"><span data-stu-id="66e39-119">How to: Manually Manage Buffered Graphics</span></span>](how-to-manually-manage-buffered-graphics.md)
