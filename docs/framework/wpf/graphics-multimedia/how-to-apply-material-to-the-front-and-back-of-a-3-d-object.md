---
title: 'Procédure : Appliquer un matériau à l’avant et l’arrière d’un objet 3D'
ms.date: 03/30/2017
helpviewer_keywords:
- 3-D objects [WPF], applying Material class
- Material class [WPF], applying to both sides of 3-D object
- classes [WPF], Material
ms.assetid: d93c8ad6-4939-4d29-9544-4d16d98093c1
ms.openlocfilehash: 1d3f6a0622b5e0ccccf14af99782bb78dfe87ccb
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59168049"
---
# <a name="how-to-apply-material-to-the-front-and-back-of-a-3-d-object"></a><span data-ttu-id="dc0f0-102">Procédure : Appliquer un matériau à l’avant et l’arrière d’un objet 3D</span><span class="sxs-lookup"><span data-stu-id="dc0f0-102">How to: Apply Material to the Front and Back of a 3-D Object</span></span>
<span data-ttu-id="dc0f0-103">L’exemple suivant montre comment appliquer un <xref:System.Windows.Media.Media3D.Material> de l’objet à l’avant et arrière 3D et animer l’objet pour afficher les deux côtés de l’objet.</span><span class="sxs-lookup"><span data-stu-id="dc0f0-103">The following example shows how to apply a <xref:System.Windows.Media.Media3D.Material> to the front and back of a 3-D object and animate the object to show both sides of the object.</span></span> <span data-ttu-id="dc0f0-104">Le <xref:System.Windows.Media.Media3D.GeometryModel3D.Material%2A> propriété d’un <xref:System.Windows.Media.Media3D.GeometryModel3D> est utilisé pour appliquer une croix rouge <xref:System.Windows.Media.Brush> à la face avant de l’objet et le <xref:System.Windows.Media.Media3D.GeometryModel3D.BackMaterial%2A> propriété du <xref:System.Windows.Media.Media3D.GeometryModel3D> est utilisé pour appliquer un bleu <xref:System.Windows.Media.Brush> à l’arrière de l’objet.</span><span class="sxs-lookup"><span data-stu-id="dc0f0-104">The <xref:System.Windows.Media.Media3D.GeometryModel3D.Material%2A> property of a <xref:System.Windows.Media.Media3D.GeometryModel3D> is used to apply a red <xref:System.Windows.Media.Brush> to the front side of the object and the <xref:System.Windows.Media.Media3D.GeometryModel3D.BackMaterial%2A> property of the <xref:System.Windows.Media.Media3D.GeometryModel3D> is used to apply a blue <xref:System.Windows.Media.Brush> to the back side of the object.</span></span> <span data-ttu-id="dc0f0-105">Le code ci-dessous montre l’application des matériaux à l’objet :</span><span class="sxs-lookup"><span data-stu-id="dc0f0-105">The code below shows the application of the materials to the object:</span></span>  
  
 [!code-xaml[Animation3DGallery_snip#BackMaterialAnimationExampleInline1](~/samples/snippets/csharp/VS_Snippets_Wpf/Animation3DGallery_snip/CS/BackMaterialAnimationExample.xaml#backmaterialanimationexampleinline1)]  
  
## <a name="example"></a><span data-ttu-id="dc0f0-106">Exemple</span><span class="sxs-lookup"><span data-stu-id="dc0f0-106">Example</span></span>  
 <span data-ttu-id="dc0f0-107">Le code suivant montre l’exemple complet.</span><span class="sxs-lookup"><span data-stu-id="dc0f0-107">The following code shows the entire sample.</span></span>  
  
 [!code-xaml[Animation3DGallery_snip#BackMaterialAnimationExampleWholePage](~/samples/snippets/csharp/VS_Snippets_Wpf/Animation3DGallery_snip/CS/BackMaterialAnimationExample.xaml#backmaterialanimationexamplewholepage)]  
  
## <a name="see-also"></a><span data-ttu-id="dc0f0-108">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="dc0f0-108">See also</span></span>

- [<span data-ttu-id="dc0f0-109">Créer une scène 3D</span><span class="sxs-lookup"><span data-stu-id="dc0f0-109">Create a 3-D Scene</span></span>](how-to-create-a-3-d-scene.md)
- [<span data-ttu-id="dc0f0-110">Vue d’ensemble des graphiques 3D</span><span class="sxs-lookup"><span data-stu-id="dc0f0-110">3-D Graphics Overview</span></span>](3-d-graphics-overview.md)
- [<span data-ttu-id="dc0f0-111">Animer les propriétés de matériel dans une scène 3D</span><span class="sxs-lookup"><span data-stu-id="dc0f0-111">Animate Material Properties in a 3-D Scene</span></span>](how-to-animate-material-properties-in-a-3-d-scene.md)
- [<span data-ttu-id="dc0f0-112">Appliquer un matériau émissif à un objet 3D</span><span class="sxs-lookup"><span data-stu-id="dc0f0-112">Apply Emissive Material to a 3-D Object</span></span>](how-to-apply-emissive-material-to-a-3-d-object.md)
