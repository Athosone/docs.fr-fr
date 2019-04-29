---
title: 'Procédure : Animer l’épaisseur d’une bordure à l’aide d’images clés'
ms.date: 03/30/2017
helpviewer_keywords:
- animation [WPF], border thickness with key frames
- key frames [WPF], animating border thickness with
- border thickness [WPF], animating with key frames
ms.assetid: 3a9cb463-0a63-407d-aae7-3fbb1a559947
ms.openlocfilehash: 101fd077bf125faadbd9a0186c2282e4b20ee78f
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61699030"
---
# <a name="how-to-animate-the-thickness-of-a-border-by-using-key-frames"></a><span data-ttu-id="b6fbb-102">Procédure : Animer l’épaisseur d’une bordure à l’aide d’images clés</span><span class="sxs-lookup"><span data-stu-id="b6fbb-102">How to: Animate the Thickness of a Border by Using Key Frames</span></span>
<span data-ttu-id="b6fbb-103">Cet exemple montre comment animer la <xref:System.Windows.Controls.Control.BorderThickness%2A> propriété d’un <xref:System.Windows.Controls.Border>.</span><span class="sxs-lookup"><span data-stu-id="b6fbb-103">This example shows how to animate the <xref:System.Windows.Controls.Control.BorderThickness%2A> property of a <xref:System.Windows.Controls.Border>.</span></span>  
  
## <a name="example"></a><span data-ttu-id="b6fbb-104">Exemple</span><span class="sxs-lookup"><span data-stu-id="b6fbb-104">Example</span></span>  
 <span data-ttu-id="b6fbb-105">L’exemple suivant utilise le <xref:System.Windows.Media.Animation.ThicknessAnimationUsingKeyFrames> classe pour animer la <xref:System.Windows.Controls.Control.BorderThickness%2A> propriété d’un <xref:System.Windows.Controls.Border>.</span><span class="sxs-lookup"><span data-stu-id="b6fbb-105">The following example uses the <xref:System.Windows.Media.Animation.ThicknessAnimationUsingKeyFrames> class to animate the <xref:System.Windows.Controls.Control.BorderThickness%2A> property of a <xref:System.Windows.Controls.Border>.</span></span> <span data-ttu-id="b6fbb-106">Cette animation utilise trois images clés de la manière suivante :</span><span class="sxs-lookup"><span data-stu-id="b6fbb-106">This animation uses three key frames in the following manner:</span></span>  
  
1. <span data-ttu-id="b6fbb-107">Pendant la première demi-seconde, elle utilise une instance de la <xref:System.Windows.Media.Animation.LinearThicknessKeyFrame> classe pour augmenter progressivement l’épaisseur de la bordure.</span><span class="sxs-lookup"><span data-stu-id="b6fbb-107">During the first half second, uses an instance of the <xref:System.Windows.Media.Animation.LinearThicknessKeyFrame> class to gradually increase the thickness of the border.</span></span> <span data-ttu-id="b6fbb-108">L’exemple utilise <xref:System.Windows.Media.Animation.LinearThicknessKeyFrame> pour créer une augmentation linéaire fluide entre les valeurs.</span><span class="sxs-lookup"><span data-stu-id="b6fbb-108">The example uses <xref:System.Windows.Media.Animation.LinearThicknessKeyFrame> to create a smooth linear increase between values.</span></span>  
  
2. <span data-ttu-id="b6fbb-109">À la fin de la prochaine demi-seconde, elle utilise une instance de la <xref:System.Windows.Media.Animation.DiscreteThicknessKeyFrame> classe pour augmenter soudainement l’épaisseur de la bordure.</span><span class="sxs-lookup"><span data-stu-id="b6fbb-109">At the end of the next half second, uses an instance of the <xref:System.Windows.Media.Animation.DiscreteThicknessKeyFrame> class to suddenly increase the thickness of the border.</span></span> <span data-ttu-id="b6fbb-110">Les images clés discrètes comme celles dérivées de <xref:System.Windows.Media.Animation.DiscreteThicknessKeyFrame> créent des changements soudains entre les valeurs, autrement dit, le déplacement de l’animation est saccadé.</span><span class="sxs-lookup"><span data-stu-id="b6fbb-110">Discrete key frames like those derived from <xref:System.Windows.Media.Animation.DiscreteThicknessKeyFrame> create sudden jumps between values, that is, the movement of the animation is jerky.</span></span>  
  
3. <span data-ttu-id="b6fbb-111">Pendant les deux dernières secondes, utilise une instance de la <xref:System.Windows.Media.Animation.SplineThicknessKeyFrame> classe pour diminuer l’épaisseur de la bordure.</span><span class="sxs-lookup"><span data-stu-id="b6fbb-111">During the final two seconds, uses an instance of the <xref:System.Windows.Media.Animation.SplineThicknessKeyFrame> class to decrease the thickness of the border.</span></span> <span data-ttu-id="b6fbb-112">Images clés spline comme celles dérivées de <xref:System.Windows.Media.Animation.SplineThicknessKeyFrame> créent une transition variable entre des valeurs en fonction de la <xref:System.Windows.Media.Animation.SplineThicknessKeyFrame.KeySpline%2A> propriété.</span><span class="sxs-lookup"><span data-stu-id="b6fbb-112">Spline key frames like those derived from <xref:System.Windows.Media.Animation.SplineThicknessKeyFrame> create a variable transition between values according to the values of the <xref:System.Windows.Media.Animation.SplineThicknessKeyFrame.KeySpline%2A> property.</span></span> <span data-ttu-id="b6fbb-113">Dans cette image clé, l’animation commence lentement, puis accélère de façon exponentielle jusqu’à la fin du segment temporel.</span><span class="sxs-lookup"><span data-stu-id="b6fbb-113">In this key frame, the animation starts off slow and speeds up exponentially toward the end of the time segment.</span></span>  
  
 [!code-xaml[keyframes_snip#ThicknessAnimationUsingKeyFramesWholePage](~/samples/snippets/xaml/VS_Snippets_Wpf/keyframes_snip/XAML/ThicknessAnimationUsingKeyFramesExample.xaml#thicknessanimationusingkeyframeswholepage)]  
  
 <span data-ttu-id="b6fbb-114">Pour l’exemple complet, consultez la page [Animation d’image clé, exemple](https://go.microsoft.com/fwlink/?LinkID=160012).</span><span class="sxs-lookup"><span data-stu-id="b6fbb-114">For the complete sample, see [KeyFrame Animation Sample](https://go.microsoft.com/fwlink/?LinkID=160012).</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="b6fbb-115">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b6fbb-115">See also</span></span>

- <xref:System.Windows.Media.Animation.LinearThicknessKeyFrame>
- <xref:System.Windows.Media.Animation.DiscreteThicknessKeyFrame>
- <xref:System.Windows.Media.Animation.SplineThicknessKeyFrame>
- [<span data-ttu-id="b6fbb-116">Vue d'ensemble des animations d'image clé</span><span class="sxs-lookup"><span data-stu-id="b6fbb-116">Key-Frame Animations Overview</span></span>](key-frame-animations-overview.md)
- [<span data-ttu-id="b6fbb-117">Guides pratiques relatifs aux images clés</span><span class="sxs-lookup"><span data-stu-id="b6fbb-117">Key-Frame How-to Topics</span></span>](key-frame-animation-how-to-topics.md)
- [<span data-ttu-id="b6fbb-118">Animer une valeur BorderThickness</span><span class="sxs-lookup"><span data-stu-id="b6fbb-118">Animate a BorderThickness Value</span></span>](../controls/how-to-animate-a-borderthickness-value.md)
