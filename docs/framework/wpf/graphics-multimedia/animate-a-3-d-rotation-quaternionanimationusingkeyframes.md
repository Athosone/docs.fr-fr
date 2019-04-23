---
title: 'Procédure : Animer une rotation 3D à l’aide d’images clés (QuaternionAnimationUsingKeyFrames)'
ms.date: 03/30/2017
helpviewer_keywords:
- 3-D translations [WPF], animating [WPF], with key frames (QuaternionAnimationUsingKeyFrames)
- key frames [WPF], QuaternionAnimationUsingKeyFrames
- animation [WPF], 3-D translations [WPF], with key frames (QuaternionAnimationUsingKeyFrames)
ms.assetid: 09e5707b-7523-4a08-9aa7-bb13cbedccdf
ms.openlocfilehash: 87176df26405a69cb2c3d63620def0575b750b52
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59338018"
---
# <a name="how-to-animate-a-3-d-rotation-using-key-frames-quaternionanimationusingkeyframes"></a><span data-ttu-id="1501e-102">Procédure : Animer une rotation 3D à l’aide d’images clés (QuaternionAnimationUsingKeyFrames)</span><span class="sxs-lookup"><span data-stu-id="1501e-102">How to: Animate a 3-D Rotation Using Key Frames (QuaternionAnimationUsingKeyFrames)</span></span>
<span data-ttu-id="1501e-103">Dans l’exemple suivant, <xref:System.Windows.Media.Animation.QuaternionAnimationUsingKeyFrames> est utilisé pour faire pivoter un objet 3D.</span><span class="sxs-lookup"><span data-stu-id="1501e-103">In the following example, <xref:System.Windows.Media.Animation.QuaternionAnimationUsingKeyFrames> is used to make a 3D object rotate.</span></span> <span data-ttu-id="1501e-104">Cette animation utilise les images clés suivantes :</span><span class="sxs-lookup"><span data-stu-id="1501e-104">This animation uses the following key frames:</span></span>  
  
1. <span data-ttu-id="1501e-105"><xref:System.Windows.Media.Animation.LinearRotation3DKeyFrame> permet de créer une interpolation linéaire fluide entre les valeurs.</span><span class="sxs-lookup"><span data-stu-id="1501e-105"><xref:System.Windows.Media.Animation.LinearRotation3DKeyFrame> is used to create a smooth, linear interpolation between values.</span></span>  
  
2. <span data-ttu-id="1501e-106"><xref:System.Windows.Media.Animation.DiscreteRotation3DKeyFrame> permet de créer des « sauts » soudains entre les valeurs (aucune interpolation).</span><span class="sxs-lookup"><span data-stu-id="1501e-106"><xref:System.Windows.Media.Animation.DiscreteRotation3DKeyFrame> is used to create sudden "jumps" between values (no interpolation).</span></span>  
  
3. <span data-ttu-id="1501e-107"><xref:System.Windows.Media.Animation.SplineRotation3DKeyFrame> permet de créer une transition variable entre des valeurs en fonction de la <xref:System.Windows.Media.Animation.SplineRotation3DKeyFrame.KeySpline%2A> propriété.</span><span class="sxs-lookup"><span data-stu-id="1501e-107"><xref:System.Windows.Media.Animation.SplineRotation3DKeyFrame> is used to create a variable transition between values depending on the <xref:System.Windows.Media.Animation.SplineRotation3DKeyFrame.KeySpline%2A> property.</span></span> <span data-ttu-id="1501e-108">Dans l’exemple ci-dessous, cette partie de l’animation commence lentement vers la fin du segment temporel, accélère de façon exponentielle.</span><span class="sxs-lookup"><span data-stu-id="1501e-108">In the example below, this part of the animation starts off slow but toward the end of the time segment, speeds up exponentially.</span></span>  
  
## <a name="example"></a><span data-ttu-id="1501e-109">Exemple</span><span class="sxs-lookup"><span data-stu-id="1501e-109">Example</span></span>  
 [!code-xaml[Animation3DGallery_snip#QuaternionAnimationUsingKeyFramesExampleWholePage](~/samples/snippets/csharp/VS_Snippets_Wpf/Animation3DGallery_snip/CS/QuaternionAnimationUsingKeyFramesExample.xaml#quaternionanimationusingkeyframesexamplewholepage)]  
  
## <a name="see-also"></a><span data-ttu-id="1501e-110">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1501e-110">See also</span></span>

- [<span data-ttu-id="1501e-111">Animer une rotation 3D à l’aide de storyboards</span><span class="sxs-lookup"><span data-stu-id="1501e-111">Animate a 3-D Rotation Using Storyboards</span></span>](how-to-animate-a-3-d-rotation-using-storyboards.md)
- [<span data-ttu-id="1501e-112">Animer une rotation 3D à l’aide de Rotation3DAnimation</span><span class="sxs-lookup"><span data-stu-id="1501e-112">Animate a 3-D Rotation Using Rotation3DAnimation</span></span>](how-to-animate-a-3-d-rotation-using-rotation3danimation.md)
- [<span data-ttu-id="1501e-113">Animer une rotation 3D à l'aide de quaternions</span><span class="sxs-lookup"><span data-stu-id="1501e-113">Animate a 3-D Rotation Using Quaternions</span></span>](how-to-animate-a-3-d-rotation-using-quaternions.md)
- [<span data-ttu-id="1501e-114">Animer une rotation 3D à l’aide d’images clés (Rotation3DAnimationUsingKeyFrames)</span><span class="sxs-lookup"><span data-stu-id="1501e-114">Animate a 3-D Rotation Using Key Frames (Rotation3DAnimationUsingKeyFrames)</span></span>](how-to-animate-a-3-d-rotation-using-key-frames.md)
- [<span data-ttu-id="1501e-115">Vue d’ensemble des graphiques 3D</span><span class="sxs-lookup"><span data-stu-id="1501e-115">3-D Graphics Overview</span></span>](3-d-graphics-overview.md)
- [<span data-ttu-id="1501e-116">Vue d'ensemble des animations d'image clé</span><span class="sxs-lookup"><span data-stu-id="1501e-116">Key-Frame Animations Overview</span></span>](key-frame-animations-overview.md)
