---
title: 'Procédure : Faire en sorte qu’un objet suive le pointeur de la souris'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- following the mouse pointer (cursor)
- mouse pointer (cursor), making objects follow
- cursor (mouse pointer), making objects follow
ms.assetid: 50b20415-14bc-405c-baf3-2fb254fffde3
ms.openlocfilehash: b9b13b4eec3e42744ba2be6031ec841fb5f215e3
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59107313"
---
# <a name="how-to-make-an-object-follow-the-mouse-pointer"></a><span data-ttu-id="71b5c-102">Procédure : Faire en sorte qu’un objet suive le pointeur de la souris</span><span class="sxs-lookup"><span data-stu-id="71b5c-102">How to: Make an Object Follow the Mouse Pointer</span></span>
<span data-ttu-id="71b5c-103">Cet exemple montre comment modifier les dimensions d’un objet lorsque le pointeur de la souris se déplace sur l’écran.</span><span class="sxs-lookup"><span data-stu-id="71b5c-103">This example shows how to change the dimensions of an object when the mouse pointer moves on the screen.</span></span>  
  
 <span data-ttu-id="71b5c-104">L’exemple inclut un [!INCLUDE[TLA#tla_xaml](../../../../includes/tlasharptla-xaml-md.md)] fichier qui crée le [!INCLUDE[TLA#tla_ui](../../../../includes/tlasharptla-ui-md.md)] et un fichier code-behind qui crée le Gestionnaire d’événements.</span><span class="sxs-lookup"><span data-stu-id="71b5c-104">The example includes an [!INCLUDE[TLA#tla_xaml](../../../../includes/tlasharptla-xaml-md.md)] file that creates the [!INCLUDE[TLA#tla_ui](../../../../includes/tlasharptla-ui-md.md)] and a code-behind file that creates the event handler.</span></span>  
  
## <a name="example"></a><span data-ttu-id="71b5c-105">Exemple</span><span class="sxs-lookup"><span data-stu-id="71b5c-105">Example</span></span>  
 <span data-ttu-id="71b5c-106">Ce qui suit [!INCLUDE[TLA2#tla_titlexaml](../../../../includes/tla2sharptla-titlexaml-md.md)] crée le [!INCLUDE[TLA2#tla_ui](../../../../includes/tla2sharptla-ui-md.md)], qui se compose d’un <xref:System.Windows.Shapes.Ellipse> à l’intérieur d’un <xref:System.Windows.Controls.StackPanel>et attache le Gestionnaire d’événements pour le <xref:System.Windows.UIElement.MouseMove> événement.</span><span class="sxs-lookup"><span data-stu-id="71b5c-106">The following [!INCLUDE[TLA2#tla_titlexaml](../../../../includes/tla2sharptla-titlexaml-md.md)] creates the [!INCLUDE[TLA2#tla_ui](../../../../includes/tla2sharptla-ui-md.md)], which consists of an <xref:System.Windows.Shapes.Ellipse> inside of a <xref:System.Windows.Controls.StackPanel>, and attaches the event handler for the <xref:System.Windows.UIElement.MouseMove> event.</span></span>  
  
 [!code-xaml[mouseMoveWithPointer#MouseMoveWithPointerXAML](~/samples/snippets/csharp/VS_Snippets_Wpf/mouseMoveWithPointer/CSharp/Window1.xaml#mousemovewithpointerxaml)]  
  
 <span data-ttu-id="71b5c-107">Le code-behind suivant crée le <xref:System.Windows.UIElement.MouseMove> Gestionnaire d’événements.</span><span class="sxs-lookup"><span data-stu-id="71b5c-107">The following code behind creates the <xref:System.Windows.UIElement.MouseMove> event handler.</span></span>  <span data-ttu-id="71b5c-108">Lorsque le pointeur de la souris se déplace, la hauteur et la largeur de la <xref:System.Windows.Shapes.Ellipse> augmentent et diminuent.</span><span class="sxs-lookup"><span data-stu-id="71b5c-108">When the mouse pointer moves, the height and the width of the <xref:System.Windows.Shapes.Ellipse> are increased and decreased.</span></span>  
  
 [!code-csharp[mouseMoveWithPointer#MouseMovePointerGetPosition](~/samples/snippets/csharp/VS_Snippets_Wpf/mouseMoveWithPointer/CSharp/Window1.xaml.cs#mousemovepointergetposition)]
 [!code-vb[mouseMoveWithPointer#MouseMovePointerGetPosition](~/samples/snippets/visualbasic/VS_Snippets_Wpf/mouseMoveWithPointer/VisualBasic/Window1.xaml.vb#mousemovepointergetposition)]  
  
## <a name="see-also"></a><span data-ttu-id="71b5c-109">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="71b5c-109">See also</span></span>

- [<span data-ttu-id="71b5c-110">Vue d’ensemble des entrées</span><span class="sxs-lookup"><span data-stu-id="71b5c-110">Input Overview</span></span>](input-overview.md)
