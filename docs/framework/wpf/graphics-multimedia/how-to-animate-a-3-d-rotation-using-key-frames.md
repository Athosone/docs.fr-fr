---
title: 'Procédure : Animer une Rotation 3D à l’aide d’images clés'
ms.date: 03/30/2017
helpviewer_keywords:
- animation [WPF], 3-D translations [WPF], with key frames (Rotation3DAnimation)
- key frames [WPF], Rotation3DAnimation
- 3-D translations [WPF], animating [WPF], with key frames (Rotation3DAnimation)
ms.assetid: 6f671b95-7f30-4836-9a4f-aeb7dc30121f
ms.openlocfilehash: e72ec94f830f0f5001a77e7492aa1326a47b309d
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59297991"
---
# <a name="how-to-animate-a-3-d-rotation-using-key-frames"></a><span data-ttu-id="fe188-102">Procédure : Animer une Rotation 3D à l’aide d’images clés</span><span class="sxs-lookup"><span data-stu-id="fe188-102">How to: Animate a 3-D Rotation Using Key Frames</span></span>
<span data-ttu-id="fe188-103">Dans l’exemple suivant, <xref:System.Windows.Media.Animation.Rotation3DAnimationUsingKeyFrames> est utilisé pour faire pivoter un objet 3D pendant son axe de rotation s’anime en créant une « déviation ».</span><span class="sxs-lookup"><span data-stu-id="fe188-103">In the following example, <xref:System.Windows.Media.Animation.Rotation3DAnimationUsingKeyFrames> is used to make a 3D object rotate while its axis of rotation animates resulting in a "wobble".</span></span> <span data-ttu-id="fe188-104">Cette animation utilise les images clés suivantes :</span><span class="sxs-lookup"><span data-stu-id="fe188-104">This animation uses the following key frames:</span></span>  
  
1. <span data-ttu-id="fe188-105"><xref:System.Windows.Media.Animation.LinearRotation3DKeyFrame> permet de créer une interpolation linéaire fluide entre les valeurs.</span><span class="sxs-lookup"><span data-stu-id="fe188-105"><xref:System.Windows.Media.Animation.LinearRotation3DKeyFrame> is used to create a smooth, linear interpolation between values.</span></span>  
  
2. <span data-ttu-id="fe188-106"><xref:System.Windows.Media.Animation.DiscreteRotation3DKeyFrame> permet de créer des « sauts » soudains entre les valeurs (aucune interpolation).</span><span class="sxs-lookup"><span data-stu-id="fe188-106"><xref:System.Windows.Media.Animation.DiscreteRotation3DKeyFrame> is used to create sudden "jumps" between values (no interpolation).</span></span>  
  
3. <span data-ttu-id="fe188-107"><xref:System.Windows.Media.Animation.SplineRotation3DKeyFrame> permet de créer une transition variable entre des valeurs en fonction de la <xref:System.Windows.Media.Animation.SplineRotation3DKeyFrame.KeySpline%2A> propriété.</span><span class="sxs-lookup"><span data-stu-id="fe188-107"><xref:System.Windows.Media.Animation.SplineRotation3DKeyFrame> is used to create a variable transition between values depending on the <xref:System.Windows.Media.Animation.SplineRotation3DKeyFrame.KeySpline%2A> property.</span></span> <span data-ttu-id="fe188-108">Dans l’exemple ci-dessous, cette partie de l’animation commence lentement vers la fin du segment temporel, accélère de façon exponentielle.</span><span class="sxs-lookup"><span data-stu-id="fe188-108">In the example below, this part of the animation starts off slow but toward the end of the time segment, speeds up exponentially.</span></span>  
  
## <a name="example"></a><span data-ttu-id="fe188-109">Exemple</span><span class="sxs-lookup"><span data-stu-id="fe188-109">Example</span></span>  
 [!code-xaml[Animation3DGallery_snip#Rotation3DAnimationUsingKeyFramesExampleWholePage](~/samples/snippets/csharp/VS_Snippets_Wpf/Animation3DGallery_snip/CS/Rotation3DAnimationUsingKeyFramesExample.xaml#rotation3danimationusingkeyframesexamplewholepage)]  
  
## <a name="see-also"></a><span data-ttu-id="fe188-110">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="fe188-110">See also</span></span>

- [<span data-ttu-id="fe188-111">Vue d’ensemble des graphiques 3D</span><span class="sxs-lookup"><span data-stu-id="fe188-111">3-D Graphics Overview</span></span>](3-d-graphics-overview.md)
- [<span data-ttu-id="fe188-112">Vue d'ensemble des animations d'image clé</span><span class="sxs-lookup"><span data-stu-id="fe188-112">Key-Frame Animations Overview</span></span>](key-frame-animations-overview.md)
- [<span data-ttu-id="fe188-113">Animer une rotation 3D à l’aide de storyboards</span><span class="sxs-lookup"><span data-stu-id="fe188-113">Animate a 3-D Rotation Using Storyboards</span></span>](how-to-animate-a-3-d-rotation-using-storyboards.md)
- [<span data-ttu-id="fe188-114">Animer une rotation 3D à l’aide de Rotation3DAnimation</span><span class="sxs-lookup"><span data-stu-id="fe188-114">Animate a 3-D Rotation Using Rotation3DAnimation</span></span>](how-to-animate-a-3-d-rotation-using-rotation3danimation.md)
- [<span data-ttu-id="fe188-115">Animer une rotation 3D à l'aide de quaternions</span><span class="sxs-lookup"><span data-stu-id="fe188-115">Animate a 3-D Rotation Using Quaternions</span></span>](how-to-animate-a-3-d-rotation-using-quaternions.md)
- [<span data-ttu-id="fe188-116">Animer une rotation 3D à l’aide d’images clés (QuaternionAnimationUsingKeyFrames)</span><span class="sxs-lookup"><span data-stu-id="fe188-116">Animate a 3-D Rotation Using Key Frames (QuaternionAnimationUsingKeyFrames)</span></span>](animate-a-3-d-rotation-quaternionanimationusingkeyframes.md)
