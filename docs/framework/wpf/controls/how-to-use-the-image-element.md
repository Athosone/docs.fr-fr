---
title: 'Procédure : Utiliser l’élément Image'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- controls [WPF], Image
- Image control [WPF]
- rendering images [WPF]
ms.assetid: 5b92e74b-1b56-4756-ac64-d5e9e08d9854
ms.openlocfilehash: 967159894e25721bdf380f851712e91d76088f87
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61696272"
---
# <a name="how-to-use-the-image-element"></a>Procédure : Utiliser l’élément Image
Cet exemple montre comment inclure des images dans une application à l’aide de la <xref:System.Windows.Controls.Image> élément.  
  
## <a name="example"></a>Exemple  
 L’exemple suivant montre comment afficher une image de 200 pixels de large. Dans cet exemple en [!INCLUDE[TLA#tla_xaml](../../../../includes/tlasharptla-xaml-md.md)], la syntaxe d’attribut et la syntaxe de balise de propriété sont utilisées pour définir l’image. Pour plus d’informations sur les syntaxes d’attribut et de propriété, consultez [Vue d’ensemble des propriétés de dépendance](../advanced/dependency-properties-overview.md). Un <xref:System.Windows.Media.Imaging.BitmapImage> est utilisé pour définir les données de l’image source et est définie explicitement pour l’exemple de syntaxe de balise de propriété. En outre, le <xref:System.Windows.Media.Imaging.BitmapImage.DecodePixelWidth%2A> de la <xref:System.Windows.Media.Imaging.BitmapImage> est défini sur la même largeur que le <xref:System.Windows.FrameworkElement.Width%2A> de la <xref:System.Windows.Controls.Image>. Cela garantit que la quantité minimale de mémoire est utilisée pour le rendu de l’image.  
  
> [!NOTE]
>  En règle générale, si vous souhaitez spécifier la taille d’un rendu d’image, spécifiez uniquement le <xref:System.Windows.FrameworkElement.Width%2A> ou <xref:System.Windows.FrameworkElement.Height%2A> mais pas les deux. Si vous ne spécifiez qu’un seul de ces paramètres, les proportions de l’image sont conservées. Dans le cas contraire, l’image peut apparaître étirée ou déformée. Pour contrôler l’image d’étirement de comportement, utilisez le <xref:System.Windows.Controls.Image.Stretch%2A> et <xref:System.Windows.Controls.Image.StretchDirection%2A> propriétés.  
  
> [!NOTE]
>  Lorsque vous spécifiez la taille d’une image avec soit <xref:System.Windows.FrameworkElement.Width%2A> ou <xref:System.Windows.FrameworkElement.Height%2A>, vous devez également définir soit <xref:System.Windows.Media.Imaging.BitmapImage.DecodePixelWidth%2A> ou <xref:System.Windows.Media.Imaging.BitmapImage.DecodePixelHeight%2A> à la même taille.  
  
 Le <xref:System.Windows.Controls.Image.Stretch%2A> propriété détermine la manière dont la source de l’image est étirée pour remplir l’élément image. Pour plus d’informations, consultez l’énumération <xref:System.Windows.Media.Stretch>.  
  
 [!code-xaml[ImageElementExample_snip#ImageSimpleExampleInlineMarkup](~/samples/snippets/csharp/VS_Snippets_Wpf/ImageElementExample_snip/CSharp/ImageSimpleExample.xaml#imagesimpleexampleinlinemarkup)]  
  
## <a name="example"></a>Exemple  
 L’exemple suivant montre comment afficher une image de 200 pixels de large à l’aide de code.  
  
> [!NOTE]
>  Paramètre <xref:System.Windows.Media.Imaging.BitmapImage> propriétés doivent être effectuées au sein d’un <xref:System.Windows.Media.Imaging.BitmapImage.BeginInit%2A> et <xref:System.Windows.Media.Imaging.BitmapImage.EndInit%2A> bloc.  
  
 [!code-csharp[ImageElementExample_snip#ImageSimpleExampleInlineCode1](~/samples/snippets/csharp/VS_Snippets_Wpf/ImageElementExample_snip/CSharp/ImageSimpleExample.xaml.cs#imagesimpleexampleinlinecode1)]
 [!code-vb[ImageElementExample_snip#ImageSimpleExampleInlineCode1](~/samples/snippets/visualbasic/VS_Snippets_Wpf/ImageElementExample_snip/VB/ImageSimpleExample.xaml.vb#imagesimpleexampleinlinecode1)]  
  
## <a name="see-also"></a>Voir aussi

- [Vue d’ensemble de la création d’images](../graphics-multimedia/imaging-overview.md)
