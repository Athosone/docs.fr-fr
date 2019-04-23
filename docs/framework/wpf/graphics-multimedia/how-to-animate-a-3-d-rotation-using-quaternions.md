---
title: 'Procédure : Animer une rotation 3D à l’aide de quaternions'
ms.date: 03/30/2017
helpviewer_keywords:
- quaternions [WPF]
- animation [WPF], 3-D translations [WPF], with quaternions
- 3-D translations [WPF], animating [WPF], with quaternions
ms.assetid: adca9cb1-066b-4de8-abbb-6b4007579ee7
ms.openlocfilehash: d994ac2ae67fd366f27f123d5bd15f14d5ac7abe
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59183220"
---
# <a name="how-to-animate-a-3-d-rotation-using-quaternions"></a>Procédure : Animer une rotation 3D à l’aide de quaternions
Cet exemple montre comment animer une rotation d’un objet 3D à l’aide de quaternions.  
  
 Le code ci-dessous montre un <xref:System.Windows.Media.Media3D.QuaternionRotation3D> utilisé comme valeur pour le <xref:System.Windows.Media.Media3D.RotateTransform3D.Rotation%2A> propriété d’un <xref:System.Windows.Media.Media3D.RotateTransform3D>.  
  
 [!code-xaml[Animation3DGallery_snip#QuaternionAnimationExampleInline1](~/samples/snippets/csharp/VS_Snippets_Wpf/Animation3DGallery_snip/CS/QuaternionAnimationExample.xaml#quaternionanimationexampleinline1)]  
  
 Cela <xref:System.Windows.Media.Media3D.QuaternionRotation3D> est animée avec un <xref:System.Windows.Media.Animation.QuaternionAnimation> au sein d’un <xref:System.Windows.Media.Animation.Storyboard> en utilisant le code ci-dessous.  
  
 [!code-xaml[Animation3DGallery_snip#QuaternionAnimationExampleInline2](~/samples/snippets/csharp/VS_Snippets_Wpf/Animation3DGallery_snip/CS/QuaternionAnimationExample.xaml#quaternionanimationexampleinline2)]  
  
## <a name="example"></a>Exemple  
 Le code suivant montre l’exemple complet.  
  
 [!code-xaml[Animation3DGallery_snip#QuaternionAnimationExampleWholePage](~/samples/snippets/csharp/VS_Snippets_Wpf/Animation3DGallery_snip/CS/QuaternionAnimationExample.xaml#quaternionanimationexamplewholepage)]  
  
## <a name="see-also"></a>Voir aussi

- [Vue d’ensemble de l’animation](animation-overview.md)
- [Créer une scène 3D](how-to-create-a-3-d-scene.md)
- [Vue d’ensemble des graphiques 3D](3-d-graphics-overview.md)
- [Vue d’ensemble des transformations](transforms-overview.md)
- [Animer une rotation 3D à l’aide de storyboards](how-to-animate-a-3-d-rotation-using-storyboards.md)
- [Animer une rotation 3D à l’aide de Rotation3DAnimation](how-to-animate-a-3-d-rotation-using-rotation3danimation.md)
