---
title: 'Procédure : Faire défiler le contenu à l’aide de l’interface IScrollInfo'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- ScrollViewer control [WPF], scrolling content
- scrolling content [WPF]
- IScrollInfo interface [WPF]
ms.assetid: d8700bef-a3f8-4c12-9de2-fc3b79f32cd3
ms.openlocfilehash: 6ebd8268e1358b45709885c07e6b096d5f806ebb
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62051245"
---
# <a name="how-to-scroll-content-by-using-the-iscrollinfo-interface"></a><span data-ttu-id="f26d4-102">Procédure : Faire défiler le contenu à l’aide de l’interface IScrollInfo</span><span class="sxs-lookup"><span data-stu-id="f26d4-102">How to: Scroll Content by Using the IScrollInfo Interface</span></span>
<span data-ttu-id="f26d4-103">Cet exemple montre comment faire défiler le contenu à l’aide de la <xref:System.Windows.Controls.Primitives.IScrollInfo> interface.</span><span class="sxs-lookup"><span data-stu-id="f26d4-103">This example shows how to scroll content by using the <xref:System.Windows.Controls.Primitives.IScrollInfo> interface.</span></span>  
  
## <a name="example"></a><span data-ttu-id="f26d4-104">Exemple</span><span class="sxs-lookup"><span data-stu-id="f26d4-104">Example</span></span>  
 <span data-ttu-id="f26d4-105">L’exemple suivant illustre les fonctionnalités de la <xref:System.Windows.Controls.Primitives.IScrollInfo> interface.</span><span class="sxs-lookup"><span data-stu-id="f26d4-105">The following example demonstrates the features of the <xref:System.Windows.Controls.Primitives.IScrollInfo> interface.</span></span> <span data-ttu-id="f26d4-106">L’exemple crée un <xref:System.Windows.Controls.StackPanel> élément [!INCLUDE[TLA#tla_xaml](../../../../includes/tlasharptla-xaml-md.md)] qui est imbriqué dans un parent <xref:System.Windows.Controls.ScrollViewer>.</span><span class="sxs-lookup"><span data-stu-id="f26d4-106">The example creates a <xref:System.Windows.Controls.StackPanel> element in [!INCLUDE[TLA#tla_xaml](../../../../includes/tlasharptla-xaml-md.md)] that is nested in a parent <xref:System.Windows.Controls.ScrollViewer>.</span></span> <span data-ttu-id="f26d4-107">Les éléments enfants de la <xref:System.Windows.Controls.StackPanel> peut défiler logiquement à l’aide des méthodes définies par le <xref:System.Windows.Controls.Primitives.IScrollInfo> interface et cast à l’instance de <xref:System.Windows.Controls.StackPanel> (`sp1`) dans le code.</span><span class="sxs-lookup"><span data-stu-id="f26d4-107">The child elements of the <xref:System.Windows.Controls.StackPanel> can be scrolled logically by using the methods defined by the <xref:System.Windows.Controls.Primitives.IScrollInfo> interface and cast to the instance of <xref:System.Windows.Controls.StackPanel> (`sp1`) in code.</span></span>  
  
 [!code-xaml[IScrollInfoMethods#2](~/samples/snippets/csharp/VS_Snippets_Wpf/IScrollInfoMethods/CSharp/Window1.xaml#2)]  
  
 <span data-ttu-id="f26d4-108">Chaque <xref:System.Windows.Controls.Button> dans le [!INCLUDE[TLA2#tla_xaml](../../../../includes/tla2sharptla-xaml-md.md)] fichier déclenche une méthode personnalisée associée qui contrôle le comportement de défilement dans <xref:System.Windows.Controls.StackPanel>.</span><span class="sxs-lookup"><span data-stu-id="f26d4-108">Each <xref:System.Windows.Controls.Button> in the [!INCLUDE[TLA2#tla_xaml](../../../../includes/tla2sharptla-xaml-md.md)] file triggers an associated custom method that controls scrolling behavior in <xref:System.Windows.Controls.StackPanel>.</span></span> <span data-ttu-id="f26d4-109">L’exemple suivant montre comment utiliser le <xref:System.Windows.Controls.Primitives.IScrollInfo.LineUp%2A> et <xref:System.Windows.Controls.Primitives.IScrollInfo.LineDown%2A> méthodes ; il indique également générique comment utiliser toutes les méthodes de positionnement qui le <xref:System.Windows.Controls.Primitives.IScrollInfo> classe définit.</span><span class="sxs-lookup"><span data-stu-id="f26d4-109">The following example shows how to use the <xref:System.Windows.Controls.Primitives.IScrollInfo.LineUp%2A> and <xref:System.Windows.Controls.Primitives.IScrollInfo.LineDown%2A> methods; it also generically shows how to use all the positioning methods that the <xref:System.Windows.Controls.Primitives.IScrollInfo> class defines.</span></span>  
  
 [!code-csharp[IScrollInfoMethods#3](~/samples/snippets/csharp/VS_Snippets_Wpf/IScrollInfoMethods/CSharp/Window1.xaml.cs#3)]
 [!code-vb[IScrollInfoMethods#3](~/samples/snippets/visualbasic/VS_Snippets_Wpf/IScrollInfoMethods/VisualBasic/Window1.xaml.vb#3)]  
  
## <a name="see-also"></a><span data-ttu-id="f26d4-110">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f26d4-110">See also</span></span>

- <xref:System.Windows.Controls.ScrollViewer>
- <xref:System.Windows.Controls.Primitives.IScrollInfo>
- <xref:System.Windows.Controls.StackPanel>
- [<span data-ttu-id="f26d4-111">Vue d’ensemble de ScrollViewer</span><span class="sxs-lookup"><span data-stu-id="f26d4-111">ScrollViewer Overview</span></span>](scrollviewer-overview.md)
- [<span data-ttu-id="f26d4-112">Rubriques de guide pratique</span><span class="sxs-lookup"><span data-stu-id="f26d4-112">How-to Topics</span></span>](scrollviewer-how-to-topics.md)
- [<span data-ttu-id="f26d4-113">Vue d’ensemble de Panel</span><span class="sxs-lookup"><span data-stu-id="f26d4-113">Panels Overview</span></span>](panels-overview.md)
