---
title: 'Procédure : Personnaliser la taille du curseur sur une barre de défilement'
ms.date: 03/30/2017
helpviewer_keywords:
- ScrollBar control [WPF]
- customizing thumb size [WPF]
- thumb size [WPF]
ms.assetid: fa32b866-5ca1-4e73-85e7-2ac64b80d194
ms.openlocfilehash: 60ae7c4e95801036c5deb0c485645297509b830c
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59207277"
---
# <a name="how-to-customize-the-thumb-size-on-a-scrollbar"></a><span data-ttu-id="3a3d9-102">Procédure : Personnaliser la taille du curseur sur une barre de défilement</span><span class="sxs-lookup"><span data-stu-id="3a3d9-102">How to: Customize the Thumb Size on a ScrollBar</span></span>
<span data-ttu-id="3a3d9-103">Cette rubrique explique comment définir le <xref:System.Windows.Controls.Primitives.Thumb> d’un <xref:System.Windows.Controls.Primitives.ScrollBar> à une taille fixe et comment spécifier une taille minimale pour le <xref:System.Windows.Controls.Primitives.Thumb> d’un <xref:System.Windows.Controls.Primitives.ScrollBar>.</span><span class="sxs-lookup"><span data-stu-id="3a3d9-103">This topic explains how to set the <xref:System.Windows.Controls.Primitives.Thumb> of a <xref:System.Windows.Controls.Primitives.ScrollBar> to a fixed size and how to specify a minimum size for the <xref:System.Windows.Controls.Primitives.Thumb> of a <xref:System.Windows.Controls.Primitives.ScrollBar>.</span></span>  
  
## <a name="example"></a><span data-ttu-id="3a3d9-104">Exemple</span><span class="sxs-lookup"><span data-stu-id="3a3d9-104">Example</span></span>  
  
## <a name="description"></a><span data-ttu-id="3a3d9-105">Description</span><span class="sxs-lookup"><span data-stu-id="3a3d9-105">Description</span></span>  
 <span data-ttu-id="3a3d9-106">L’exemple suivant crée un <xref:System.Windows.Controls.Primitives.ScrollBar> qui a un <xref:System.Windows.Controls.Primitives.Thumb> avec une taille fixe.</span><span class="sxs-lookup"><span data-stu-id="3a3d9-106">The following example creates a <xref:System.Windows.Controls.Primitives.ScrollBar> that has a <xref:System.Windows.Controls.Primitives.Thumb> with a fixed size.</span></span> <span data-ttu-id="3a3d9-107">L’exemple définit le <xref:System.Windows.Controls.Primitives.Track.ViewportSize%2A> propriété de la <xref:System.Windows.Controls.Primitives.Thumb> à <xref:System.Double.NaN> et définit la hauteur de la <xref:System.Windows.Controls.Primitives.Thumb>.</span><span class="sxs-lookup"><span data-stu-id="3a3d9-107">The example sets the <xref:System.Windows.Controls.Primitives.Track.ViewportSize%2A> property of the <xref:System.Windows.Controls.Primitives.Thumb> to <xref:System.Double.NaN> and sets the height of the <xref:System.Windows.Controls.Primitives.Thumb>.</span></span>  <span data-ttu-id="3a3d9-108">Pour créer un horizontal <xref:System.Windows.Controls.Primitives.ScrollBar> avec un <xref:System.Windows.Controls.Primitives.Thumb> qui a une largeur fixe, la valeur de la largeur de la <xref:System.Windows.Controls.Primitives.Thumb>.</span><span class="sxs-lookup"><span data-stu-id="3a3d9-108">To create a horizontal <xref:System.Windows.Controls.Primitives.ScrollBar> with a <xref:System.Windows.Controls.Primitives.Thumb> that has a fixed width, set the width of the <xref:System.Windows.Controls.Primitives.Thumb>.</span></span>  
  
## <a name="code"></a><span data-ttu-id="3a3d9-109">Code</span><span class="sxs-lookup"><span data-stu-id="3a3d9-109">Code</span></span>  
 [!code-xaml[ScrollBarCustomThumbSize#1](~/samples/snippets/csharp/VS_Snippets_Wpf/ScrollBarCustomThumbSize/CS/Window1.xaml#1)]  
  
## <a name="description"></a><span data-ttu-id="3a3d9-110">Description</span><span class="sxs-lookup"><span data-stu-id="3a3d9-110">Description</span></span>  
 <span data-ttu-id="3a3d9-111">L’exemple suivant crée un <xref:System.Windows.Controls.Primitives.ScrollBar> qui a un <xref:System.Windows.Controls.Primitives.Thumb> avec une taille minimale.</span><span class="sxs-lookup"><span data-stu-id="3a3d9-111">The following example creates a <xref:System.Windows.Controls.Primitives.ScrollBar> that has a <xref:System.Windows.Controls.Primitives.Thumb> with a minimum size.</span></span> <span data-ttu-id="3a3d9-112">L’exemple définit la valeur de <xref:System.Windows.SystemParameters.VerticalScrollBarButtonHeightKey%2A>.</span><span class="sxs-lookup"><span data-stu-id="3a3d9-112">The example sets the value of <xref:System.Windows.SystemParameters.VerticalScrollBarButtonHeightKey%2A>.</span></span> <span data-ttu-id="3a3d9-113">Pour créer un horizontal <xref:System.Windows.Controls.Primitives.ScrollBar> avec un <xref:System.Windows.Controls.Primitives.Thumb> qui a une largeur minimale, définissez le <xref:System.Windows.SystemParameters.HorizontalScrollBarButtonWidthKey%2A>.</span><span class="sxs-lookup"><span data-stu-id="3a3d9-113">To create a horizontal <xref:System.Windows.Controls.Primitives.ScrollBar> with a <xref:System.Windows.Controls.Primitives.Thumb> that has a minimum width, set the <xref:System.Windows.SystemParameters.HorizontalScrollBarButtonWidthKey%2A>.</span></span>  
  
## <a name="code"></a><span data-ttu-id="3a3d9-114">Code</span><span class="sxs-lookup"><span data-stu-id="3a3d9-114">Code</span></span>  
 [!code-xaml[ScrollBarCustomThumbSize#2](~/samples/snippets/csharp/VS_Snippets_Wpf/ScrollBarCustomThumbSize/CS/Window1.xaml#2)]  
  
## <a name="see-also"></a><span data-ttu-id="3a3d9-115">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="3a3d9-115">See also</span></span>

- [<span data-ttu-id="3a3d9-116">Styles et modèles ScrollBar</span><span class="sxs-lookup"><span data-stu-id="3a3d9-116">ScrollBar Styles and Templates</span></span>](scrollbar-styles-and-templates.md)
