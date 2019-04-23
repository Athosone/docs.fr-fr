---
title: 'Procédure : Animer la position et la direction de la caméra d’une scène 3D'
ms.date: 03/30/2017
helpviewer_keywords:
- animation [WPF], camera position in 3-D scenes
- camera direction [WPF], animating in 3-D scenes
- 3-D scenes [WPF], animating camera position
- 3-D scenes [WPF], animating camera direction
- camera position [WPF], animating in 3-D scenes
- animation [WPF], camera direction in 3-D scenes
ms.assetid: 480224b7-a5e5-4165-ba7f-ef760ddff94a
ms.openlocfilehash: b64263a495ffe845a76317aad8f5b4a14e11b31e
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59146001"
---
# <a name="how-to-animate-camera-position-and-direction-in-a-3d-scene"></a><span data-ttu-id="ac354-102">Procédure : Animer la position et la direction de la caméra d’une scène 3D</span><span class="sxs-lookup"><span data-stu-id="ac354-102">How to: Animate Camera Position and Direction in a 3D Scene</span></span>
<span data-ttu-id="ac354-103">L’exemple suivant montre comment animer la position d’une caméra et animer la direction qu’il pointe dans une scène 3D.</span><span class="sxs-lookup"><span data-stu-id="ac354-103">The following example shows how to animate the position of a camera and animate the direction it is pointing in a 3D scene.</span></span> <span data-ttu-id="ac354-104">Pour cela, à l’aide de <xref:System.Windows.Media.Animation.Point3DAnimation> et <xref:System.Windows.Media.Animation.Vector3DAnimation> pour animer la <xref:System.Windows.Media.Media3D.ProjectionCamera.Position%2A> et <xref:System.Windows.Media.Media3D.ProjectionCamera.LookDirection%2A> propriétés respectivement de la <xref:System.Windows.Media.Media3D.PerspectiveCamera>.</span><span class="sxs-lookup"><span data-stu-id="ac354-104">This is done by using <xref:System.Windows.Media.Animation.Point3DAnimation> and <xref:System.Windows.Media.Animation.Vector3DAnimation> to animate the <xref:System.Windows.Media.Media3D.ProjectionCamera.Position%2A> and <xref:System.Windows.Media.Media3D.ProjectionCamera.LookDirection%2A> properties respectively of the <xref:System.Windows.Media.Media3D.PerspectiveCamera>.</span></span> <span data-ttu-id="ac354-105">Vous pouvez utiliser une animation comme suit pour modifier l’affichage du spectateur d’une scène en réponse à un événement.</span><span class="sxs-lookup"><span data-stu-id="ac354-105">You might use an animation like this to change the onlooker's view of a scene in response to an event.</span></span>  
  
## <a name="example"></a><span data-ttu-id="ac354-106">Exemple</span><span class="sxs-lookup"><span data-stu-id="ac354-106">Example</span></span>  
 [!code-xaml[Animation3DGallery_snip#PointVector3DAnimationExampleWholePage](~/samples/snippets/csharp/VS_Snippets_Wpf/Animation3DGallery_snip/CS/PointVector3DAnimationExample.xaml#pointvector3danimationexamplewholepage)]  
  
## <a name="see-also"></a><span data-ttu-id="ac354-107">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ac354-107">See also</span></span>

- <xref:System.Windows.Media.Animation.Vector3DAnimation>
- <xref:System.Windows.Media.Animation.Point3DAnimation>
- [<span data-ttu-id="ac354-108">Animer la position et la direction de la caméra à l’aide d’images clés</span><span class="sxs-lookup"><span data-stu-id="ac354-108">Animate Camera Position and Direction Using Key Frames</span></span>](how-to-animate-camera-position-and-direction-using-key-frames.md)
- [<span data-ttu-id="ac354-109">Vue d’ensemble des graphiques 3D</span><span class="sxs-lookup"><span data-stu-id="ac354-109">3-D Graphics Overview</span></span>](3-d-graphics-overview.md)
