---
title: 'Procédure : Définir les propriétés Height d’un élément'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- height properties [WPF]
- Panel control [WPF], height properties of elements
ms.assetid: 5ab9e781-dbb8-469a-a3c8-cf38ce312647
ms.openlocfilehash: fb655630336c3b69afdc726a2e3c5a2cb8838667
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59221585"
---
# <a name="how-to-set-the-height-properties-of-an-element"></a><span data-ttu-id="2c95e-102">Procédure : Définir les propriétés Height d’un élément</span><span class="sxs-lookup"><span data-stu-id="2c95e-102">How to: Set the Height Properties of an Element</span></span>
## <a name="example"></a><span data-ttu-id="2c95e-103">Exemple</span><span class="sxs-lookup"><span data-stu-id="2c95e-103">Example</span></span>  
 <span data-ttu-id="2c95e-104">Cet exemple montre visuellement les différences de rendu de comportement entre les quatre propriétés associées à la hauteur dans [!INCLUDE[TLA#tla_winclient](../../../../includes/tlasharptla-winclient-md.md)].</span><span class="sxs-lookup"><span data-stu-id="2c95e-104">This example visually shows the differences in rendering behavior among the four height-related properties in [!INCLUDE[TLA#tla_winclient](../../../../includes/tlasharptla-winclient-md.md)].</span></span>  
  
 <span data-ttu-id="2c95e-105">Le <xref:System.Windows.FrameworkElement> classe expose quatre propriétés qui décrivent les caractéristiques de hauteur d’un élément.</span><span class="sxs-lookup"><span data-stu-id="2c95e-105">The <xref:System.Windows.FrameworkElement> class exposes four properties that describe the height characteristics of an element.</span></span> <span data-ttu-id="2c95e-106">Ces quatre propriétés peuvent entrer en conflit, et quand ils le font, la valeur prioritaire est déterminée comme suit : le <xref:System.Windows.FrameworkElement.MinHeight%2A> valeur est prioritaire sur la <xref:System.Windows.FrameworkElement.MaxHeight%2A> valeur, qui à son tour est prioritaire sur la <xref:System.Windows.FrameworkElement.Height%2A> valeur.</span><span class="sxs-lookup"><span data-stu-id="2c95e-106">These four properties can conflict, and when they do, the value that takes precedence is determined as follows: the <xref:System.Windows.FrameworkElement.MinHeight%2A> value takes precedence over the <xref:System.Windows.FrameworkElement.MaxHeight%2A> value, which in turn takes precedence over the <xref:System.Windows.FrameworkElement.Height%2A> value.</span></span> <span data-ttu-id="2c95e-107">Une quatrième propriété <xref:System.Windows.FrameworkElement.ActualHeight%2A>, est en lecture seule et signale la hauteur réelle, telle que déterminée par les interactions avec le processus de disposition.</span><span class="sxs-lookup"><span data-stu-id="2c95e-107">A fourth property, <xref:System.Windows.FrameworkElement.ActualHeight%2A>, is read-only, and reports the actual height as determined by interactions with the layout process.</span></span>  
  
 <span data-ttu-id="2c95e-108">Ce qui suit [!INCLUDE[TLA#tla_xaml](../../../../includes/tlasharptla-xaml-md.md)] exemples dessinent un <xref:System.Windows.Shapes.Rectangle> élément (`rect1`) en tant qu’enfant de <xref:System.Windows.Controls.Canvas>.</span><span class="sxs-lookup"><span data-stu-id="2c95e-108">The following [!INCLUDE[TLA#tla_xaml](../../../../includes/tlasharptla-xaml-md.md)] examples draw a <xref:System.Windows.Shapes.Rectangle> element (`rect1`) as a child of <xref:System.Windows.Controls.Canvas>.</span></span> <span data-ttu-id="2c95e-109">Vous pouvez modifier les propriétés height d’un <xref:System.Windows.Shapes.Rectangle> à l’aide d’une série de <xref:System.Windows.Controls.ListBox> éléments qui représentent les valeurs de propriété <xref:System.Windows.FrameworkElement.MinHeight%2A>, <xref:System.Windows.FrameworkElement.MaxHeight%2A>, et <xref:System.Windows.FrameworkElement.Height%2A>.</span><span class="sxs-lookup"><span data-stu-id="2c95e-109">You can change the height properties of a <xref:System.Windows.Shapes.Rectangle> by using a series of <xref:System.Windows.Controls.ListBox> elements that represent the property values of <xref:System.Windows.FrameworkElement.MinHeight%2A>, <xref:System.Windows.FrameworkElement.MaxHeight%2A>, and <xref:System.Windows.FrameworkElement.Height%2A>.</span></span> <span data-ttu-id="2c95e-110">De cette manière, la priorité de chaque propriété est affichée visuellement.</span><span class="sxs-lookup"><span data-stu-id="2c95e-110">In this manner, the precedence of each property is visually displayed.</span></span>  
  
 [!code-xaml[HeightMinHeightMaxHeight#1](~/samples/snippets/csharp/VS_Snippets_Wpf/HeightMinHeightMaxHeight/CSharp/Window1.xaml#1)]  
[!code-xaml[HeightMinHeightMaxHeight#2](~/samples/snippets/csharp/VS_Snippets_Wpf/HeightMinHeightMaxHeight/CSharp/Window1.xaml#2)]  
  
 <span data-ttu-id="2c95e-111">Les exemples de code-behind suivant gèrent les événements qui le <xref:System.Windows.Controls.Primitives.Selector.SelectionChanged> déclenche des événements.</span><span class="sxs-lookup"><span data-stu-id="2c95e-111">The following code-behind examples handle the events that the <xref:System.Windows.Controls.Primitives.Selector.SelectionChanged> event raises.</span></span> <span data-ttu-id="2c95e-112">Chaque gestionnaire extrait l’entrée de la <xref:System.Windows.Controls.ListBox>, analyse la valeur comme un <xref:System.Double>et applique la valeur à la propriété associées à la hauteur spécifiée.</span><span class="sxs-lookup"><span data-stu-id="2c95e-112">Each handler takes the input from the <xref:System.Windows.Controls.ListBox>, parses the value as a <xref:System.Double>, and applies the value to the specified height-related property.</span></span> <span data-ttu-id="2c95e-113">Les valeurs de hauteur sont également converties en une chaîne et écrites dans différents <xref:System.Windows.Controls.TextBlock> éléments (la définition de ces éléments n’est pas affichée dans le XAML sélectionné).</span><span class="sxs-lookup"><span data-stu-id="2c95e-113">The height values are also converted to a string and written to various <xref:System.Windows.Controls.TextBlock> elements (definition of those elements is not shown in the selected XAML).</span></span>  
  
 [!code-csharp[HeightMinHeightMaxHeight#3](~/samples/snippets/csharp/VS_Snippets_Wpf/HeightMinHeightMaxHeight/CSharp/Window1.xaml.cs#3)]
 [!code-vb[HeightMinHeightMaxHeight#3](~/samples/snippets/visualbasic/VS_Snippets_Wpf/HeightMinHeightMaxHeight/VisualBasic/Window1.xaml.vb#3)]  
  
 <span data-ttu-id="2c95e-114">Pour obtenir un exemple complet, consultez [propriétés Height, exemple](https://go.microsoft.com/fwlink/?LinkID=159993).</span><span class="sxs-lookup"><span data-stu-id="2c95e-114">For the complete sample, see [Height Properties Sample](https://go.microsoft.com/fwlink/?LinkID=159993).</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="2c95e-115">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="2c95e-115">See also</span></span>

- <xref:System.Windows.FrameworkElement>
- <xref:System.Windows.Controls.ListBox>
- <xref:System.Windows.FrameworkElement.ActualHeight%2A>
- <xref:System.Windows.FrameworkElement.MaxHeight%2A>
- <xref:System.Windows.FrameworkElement.MinHeight%2A>
- <xref:System.Windows.FrameworkElement.Height%2A>
- [<span data-ttu-id="2c95e-116">Définir les propriétés Width d’un élément</span><span class="sxs-lookup"><span data-stu-id="2c95e-116">Set the Width Properties of an Element</span></span>](how-to-set-the-width-properties-of-an-element.md)
- [<span data-ttu-id="2c95e-117">Vue d’ensemble de Panel</span><span class="sxs-lookup"><span data-stu-id="2c95e-117">Panels Overview</span></span>](panels-overview.md)
- [<span data-ttu-id="2c95e-118">Exemple de propriétés de hauteur</span><span class="sxs-lookup"><span data-stu-id="2c95e-118">Height Properties Sample</span></span>](https://go.microsoft.com/fwlink/?LinkID=159993)
