---
title: 'Procédure : Peindre une zone avec une vidéo'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- painting with a video [WPF]
- video [WPF], painting with
- brushes [WPF], painting with a video
ms.assetid: 04dd6600-4a6e-4b43-a93e-21cce7dfbcb8
ms.openlocfilehash: be09d1310847cd7214ea795a704c25d994f07b7a
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61921730"
---
# <a name="how-to-paint-an-area-with-a-video"></a>Procédure : Peindre une zone avec une vidéo
Cet exemple montre comment peindre une zone avec le média. Pour peindre une zone avec un média consiste à utiliser un <xref:System.Windows.Controls.MediaElement> avec un <xref:System.Windows.Media.VisualBrush>. Utiliser le <xref:System.Windows.Controls.MediaElement> pour charger et lire le média, puis utilisez-le pour définir le <xref:System.Windows.Media.VisualBrush.Visual%2A> propriété de la <xref:System.Windows.Media.VisualBrush>. Vous pouvez ensuite utiliser le <xref:System.Windows.Media.VisualBrush> pour peindre une zone avec le média chargé.  
  
## <a name="example"></a>Exemple  
 L’exemple suivant utilise un <xref:System.Windows.Controls.MediaElement> et un <xref:System.Windows.Media.VisualBrush> pour peindre le <xref:System.Windows.Controls.TextBlock.Foreground%2A> d’un <xref:System.Windows.Controls.TextBlock> contrôle avec la vidéo. Cet exemple définit le <xref:System.Windows.Controls.MediaElement.IsMuted%2A> propriété de la <xref:System.Windows.Controls.MediaElement> à `true` afin qu’il ne produise aucun son.  
  
 [!code-csharp[Visualbrush_markup_snip#GraphicsMMVideoAsTextBackgroundInline](~/samples/snippets/csharp/VS_Snippets_Wpf/visualbrush_markup_snip/CSharp/PaintWithVideoExample.cs#graphicsmmvideoastextbackgroundinline)]
 [!code-vb[Visualbrush_markup_snip#GraphicsMMVideoAsTextBackgroundInline](~/samples/snippets/visualbasic/VS_Snippets_Wpf/visualbrush_markup_snip/visualbasic/paintwithvideoexample.vb#graphicsmmvideoastextbackgroundinline)]
 [!code-xaml[Visualbrush_markup_snip#GraphicsMMVideoAsTextBackgroundInline](~/samples/snippets/xaml/VS_Snippets_Wpf/visualbrush_markup_snip/XAML/PaintWithVideoExample.xaml#graphicsmmvideoastextbackgroundinline)]  
  
## <a name="example"></a>Exemple  
 Étant donné que <xref:System.Windows.Media.VisualBrush> hérite le <xref:System.Windows.Media.TileBrush> (classe), il fournit plusieurs modes de mosaïque. En définissant le <xref:System.Windows.Media.TileBrush.TileMode%2A> propriété d’un <xref:System.Windows.Media.VisualBrush> à <xref:System.Windows.Media.TileMode.Tile> et en définissant son <xref:System.Windows.Media.TileBrush.Viewport%2A> propriété à une valeur inférieure à la zone que vous peignez, vous pouvez créer un modèle en mosaïque.  
  
 L’exemple suivant est identique à l’exemple précédent, à ceci près que le <xref:System.Windows.Media.VisualBrush> génère un modèle à partir de la vidéo.  
  
 [!code-csharp[Visualbrush_markup_snip#GraphicsMMVideoAsTextBackgroundTiledInline](~/samples/snippets/csharp/VS_Snippets_Wpf/visualbrush_markup_snip/CSharp/PaintWithVideoExample.cs#graphicsmmvideoastextbackgroundtiledinline)]
 [!code-vb[Visualbrush_markup_snip#GraphicsMMVideoAsTextBackgroundTiledInline](~/samples/snippets/visualbasic/VS_Snippets_Wpf/visualbrush_markup_snip/visualbasic/paintwithvideoexample.vb#graphicsmmvideoastextbackgroundtiledinline)]
 [!code-xaml[Visualbrush_markup_snip#GraphicsMMVideoAsTextBackgroundTiledInline](~/samples/snippets/xaml/VS_Snippets_Wpf/visualbrush_markup_snip/XAML/PaintWithVideoExample.xaml#graphicsmmvideoastextbackgroundtiledinline)]  
  
 Pour plus d’informations sur l’ajout d’un fichier de contenu, tel qu’un fichier multimédia, à votre application, consultez [ressource d’Application WPF, de contenu et de fichiers de données](../app-development/wpf-application-resource-content-and-data-files.md). Lorsque vous ajoutez un fichier multimédia, vous devez l’ajouter en tant qu’un fichier de contenu, et non comme un fichier de ressources.  
  
## <a name="see-also"></a>Voir aussi

- <xref:System.Windows.Media.VisualBrush>
- [Peinture avec des images, des dessins et des objets visuels](painting-with-images-drawings-and-visuals.md)
- [Vue d’ensemble de TileBrush](tilebrush-overview.md)
- [Vue d’ensemble multimédia](multimedia-overview.md)
