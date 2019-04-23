---
title: 'Procédure : Animer une géométrie rectangle à l’aide d’images clés'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- key frames [WPF], animating RectangleGeometry objects with
- RectangleGeometry objects [WPF], animating with key frames
- animation [WPF], RectangleGeometry objects with key frames
ms.assetid: a8b45ceb-0e32-4ba1-928f-df6d30db17c6
ms.openlocfilehash: 03953b79127ffceeb49e4ece2070d09f382448a5
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59311342"
---
# <a name="how-to-animate-a-rectangle-geometry-by-using-key-frames"></a>Procédure : Animer une géométrie rectangle à l’aide d’images clés
Cet exemple montre comment animer la <xref:System.Windows.Media.RectangleGeometry.Rect%2A> propriété d’un <xref:System.Windows.Media.RectangleGeometry> à l’aide d’images clés.  
  
## <a name="example"></a>Exemple  
 L’exemple suivant utilise le <xref:System.Windows.Media.Animation.RectAnimationUsingKeyFrames> classe pour animer la <xref:System.Windows.Media.RectangleGeometry.Rect%2A> propriété d’un <xref:System.Windows.Media.RectangleGeometry>. Cette animation utilise trois images clés de la manière suivante :  
  
1. Pendant les deux premières secondes, utilise une instance de la <xref:System.Windows.Media.Animation.LinearRectKeyFrame> classe pour animer un changement graduel de position, la largeur et hauteur d’un rectangle. Images clés linéaires comme <xref:System.Windows.Media.Animation.LinearRectKeyFrame> créent une transition linéaire fluide entre les valeurs.  
  
2. Lors de la fin de la prochaine demi-seconde, elle utilise une instance de la <xref:System.Windows.Media.Animation.DiscreteRectKeyFrame> classe pour réduire soudainement la hauteur du rectangle. Images clés discrètes comme <xref:System.Windows.Media.Animation.DiscreteRectKeyFrame> créent des changements soudains entre les valeurs, autrement dit, la diminution de la hauteur se produit rapidement et n’est pas subtile.  
  
3. Pendant les deux dernières secondes, utilise une instance de la <xref:System.Windows.Media.Animation.SplineRectKeyFrame> classe pour modifier le rectangle à sa taille et sa position d’origine. Les images clés spline comme <xref:System.Windows.Media.Animation.SplineRectKeyFrame> créent une transition variable entre des valeurs en fonction de la <xref:System.Windows.Media.Animation.SplineRectKeyFrame.KeySpline%2A> propriété. Dans cet exemple, le changement commence lentement, puis accélère de façon exponentielle jusqu’à la fin du segment temporel.  
  
 [!code-csharp[keyframes_snip#RectAnimationUsingKeyFramesWholePage](~/samples/snippets/csharp/VS_Snippets_Wpf/keyframes_snip/CSharp/RectAnimationUsingKeyFramesExample.cs#rectanimationusingkeyframeswholepage)]
 [!code-vb[keyframes_snip#RectAnimationUsingKeyFramesWholePage](~/samples/snippets/visualbasic/VS_Snippets_Wpf/keyframes_snip/visualbasic/rectanimationusingkeyframesexample.vb#rectanimationusingkeyframeswholepage)]
 [!code-xaml[keyframes_snip#RectAnimationUsingKeyFramesWholePage](~/samples/snippets/xaml/VS_Snippets_Wpf/keyframes_snip/XAML/RectAnimationUsingKeyFramesExample.xaml#rectanimationusingkeyframeswholepage)]  
  
 Pour l’exemple complet, consultez la page [Animation d’image clé, exemple](https://go.microsoft.com/fwlink/?LinkID=160012).  
  
## <a name="see-also"></a>Voir aussi

- <xref:System.Windows.Media.RectangleGeometry>
- <xref:System.Windows.Media.RectangleGeometry.Rect%2A>
- <xref:System.Windows.Media.Animation.RectAnimationUsingKeyFrames>
- [Vue d'ensemble des animations d'image clé](key-frame-animations-overview.md)
- [Guides pratiques relatifs aux images clés](key-frame-animation-how-to-topics.md)
