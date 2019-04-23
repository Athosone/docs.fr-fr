---
title: 'Procédure : Peindre une zone avec une couleur unie'
ms.date: 03/30/2017
helpviewer_keywords:
- solid colors [WPF], painting with
- brushes [WPF], painting with solid colors
- painting [WPF], with solid colors
ms.assetid: 5d27d8a7-4bd7-4063-bdf3-2c5c0f19f9d3
ms.openlocfilehash: c85ba72c858d155f29875bb944824db1c44ffaab
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59086843"
---
# <a name="how-to-paint-an-area-with-a-solid-color"></a><span data-ttu-id="42de0-102">Procédure : Peindre une zone avec une couleur unie</span><span class="sxs-lookup"><span data-stu-id="42de0-102">How to: Paint an Area with a Solid Color</span></span>
<span data-ttu-id="42de0-103">Pour peindre une zone avec une couleur unie, vous pouvez utiliser un pinceau système prédéfini, tel que <xref:System.Windows.Media.Brushes.Red%2A> ou <xref:System.Windows.Media.Brushes.Blue%2A>, ou vous pouvez créer un nouveau <xref:System.Windows.Media.SolidColorBrush> et décrire sa <xref:System.Windows.Media.SolidColorBrush.Color%2A> à l’aide des valeurs alphabétiques, rouges, vert et bleus.</span><span class="sxs-lookup"><span data-stu-id="42de0-103">To paint an area with a solid color, you can use a predefined system brush, such as <xref:System.Windows.Media.Brushes.Red%2A> or <xref:System.Windows.Media.Brushes.Blue%2A>, or you can create a new <xref:System.Windows.Media.SolidColorBrush> and describe its <xref:System.Windows.Media.SolidColorBrush.Color%2A> using alpha, red, green, and blue values.</span></span> <span data-ttu-id="42de0-104">En XAML, vous pouvez également peindre une zone avec une couleur unie à l’aide de la notation hexadécimale.</span><span class="sxs-lookup"><span data-stu-id="42de0-104">In XAML, you may also paint an area with a solid color by using hexidecimal notation.</span></span>  
  
 <span data-ttu-id="42de0-105">Les exemples suivants utilisent chacune de ces techniques pour peindre un <xref:System.Windows.Shapes.Rectangle> bleu.</span><span class="sxs-lookup"><span data-stu-id="42de0-105">The following examples uses each of these techniques to paint a <xref:System.Windows.Shapes.Rectangle> blue.</span></span>  
  
## <a name="example"></a><span data-ttu-id="42de0-106">Exemple</span><span class="sxs-lookup"><span data-stu-id="42de0-106">Example</span></span>  
 <span data-ttu-id="42de0-107">**Utilisation d’un pinceau prédéfini**</span><span class="sxs-lookup"><span data-stu-id="42de0-107">**Using a Predefined Brush**</span></span>  
  
 <span data-ttu-id="42de0-108">Dans l’exemple suivant utilise le pinceau prédéfini <xref:System.Windows.Media.Brushes.Blue%2A> pour peindre un rectangle en bleu.</span><span class="sxs-lookup"><span data-stu-id="42de0-108">In the following example uses the predefined brush <xref:System.Windows.Media.Brushes.Blue%2A> to paint a rectangle blue.</span></span>  
  
 [!code-xaml[brushsamples_snip#_graphicsmm_PredefinedBrush1](~/samples/snippets/csharp/VS_Snippets_Wpf/brushsamples_snip/CS/SolidColorBrushExample.xaml#_graphicsmm_predefinedbrush1)]  
  
 [!code-csharp[brushsamples_procedural_snip#_graphicsmm_PredefinedBrush1](~/samples/snippets/csharp/VS_Snippets_Wpf/brushsamples_procedural_snip/CSharp/SolidColorBrushExample.cs#_graphicsmm_predefinedbrush1)]  
  
 <span data-ttu-id="42de0-109">**Utilisation de la notation hexadécimale**</span><span class="sxs-lookup"><span data-stu-id="42de0-109">**Using Hexadecimal Notation**</span></span>  
  
 <span data-ttu-id="42de0-110">L’exemple suivant utilise une notation hexadécimale à 8 chiffres pour peindre un rectangle en bleu.</span><span class="sxs-lookup"><span data-stu-id="42de0-110">The next example uses 8-digit hexadecimal notation to paint a rectangle blue.</span></span>  
  
 [!code-xaml[brushsamples_snip#_graphicsmm_HexNotation8Digit1](~/samples/snippets/csharp/VS_Snippets_Wpf/brushsamples_snip/CS/SolidColorBrushExample.xaml#_graphicsmm_hexnotation8digit1)]  
  
 <span data-ttu-id="42de0-111">**Utilisation de valeurs ARGB**</span><span class="sxs-lookup"><span data-stu-id="42de0-111">**Using ARGB Values**</span></span>  
  
 <span data-ttu-id="42de0-112">L’exemple suivant crée un <xref:System.Windows.Media.SolidColorBrush> et décrit son <xref:System.Windows.Media.SolidColorBrush.Color%2A> ARGB à l’aide de valeurs pour la couleur bleue.</span><span class="sxs-lookup"><span data-stu-id="42de0-112">The next example creates a <xref:System.Windows.Media.SolidColorBrush> and describes its <xref:System.Windows.Media.SolidColorBrush.Color%2A> using the ARGB values for the color blue.</span></span>  
  
 [!code-xaml[brushsamples_snip#_graphicsmm_RgbNotation1](~/samples/snippets/csharp/VS_Snippets_Wpf/brushsamples_snip/CS/SolidColorBrushExample.xaml#_graphicsmm_rgbnotation1)]  
  
 [!code-csharp[brushsamples_procedural_snip#_graphicsmm_RgbNotation1](~/samples/snippets/csharp/VS_Snippets_Wpf/brushsamples_procedural_snip/CSharp/SolidColorBrushExample.cs#_graphicsmm_rgbnotation1)]  
  
 <span data-ttu-id="42de0-113">Pour d’autres façons de décrire la couleur, consultez la <xref:System.Windows.Media.Color> structure.</span><span class="sxs-lookup"><span data-stu-id="42de0-113">For other ways of describing color, see the <xref:System.Windows.Media.Color> structure.</span></span>  
  
 <span data-ttu-id="42de0-114">**Rubriques connexes**</span><span class="sxs-lookup"><span data-stu-id="42de0-114">**Related Topics**</span></span>  
  
 <span data-ttu-id="42de0-115">Pour plus d’informations sur <xref:System.Windows.Media.SolidColorBrush> et obtenir des exemples supplémentaires, consultez le [peinture avec des couleurs unies et vue d’ensemble des dégradés](painting-with-solid-colors-and-gradients-overview.md) vue d’ensemble.</span><span class="sxs-lookup"><span data-stu-id="42de0-115">For more information about <xref:System.Windows.Media.SolidColorBrush> and additional examples, see the [Painting with Solid Colors and Gradients Overview](painting-with-solid-colors-and-gradients-overview.md) overview.</span></span>  
  
 <span data-ttu-id="42de0-116">Cet exemple de code fait partie d’un exemple plus complet fourni pour la <xref:System.Windows.Media.SolidColorBrush> classe.</span><span class="sxs-lookup"><span data-stu-id="42de0-116">This code example is part of a larger example provided for the <xref:System.Windows.Media.SolidColorBrush> class.</span></span> <span data-ttu-id="42de0-117">Pour l’exemple complet, consultez [Exemples de pinceaux](https://go.microsoft.com/fwlink/?LinkID=159973).</span><span class="sxs-lookup"><span data-stu-id="42de0-117">For the complete sample, see the [Brushes Sample](https://go.microsoft.com/fwlink/?LinkID=159973).</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="42de0-118">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="42de0-118">See also</span></span>

- <xref:System.Windows.Media.Brushes>
