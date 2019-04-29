---
title: 'Procédure : disposer une forme en mosaïque avec une image'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- texture brushes [Windows Forms], tiling images with
- images [Windows Forms], filling shapes with
- shapes [Windows Forms], tiling with images
- bitmaps [Windows Forms], filling shapes with
ms.assetid: 6d407891-6e5c-4495-a546-3da5604e9fb8
ms.openlocfilehash: ad7b8737a63028e533cadfa6db56b063eb943f22
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61954931"
---
# <a name="how-to-tile-a-shape-with-an-image"></a><span data-ttu-id="99c6b-102">Procédure : disposer une forme en mosaïque avec une image</span><span class="sxs-lookup"><span data-stu-id="99c6b-102">How to: Tile a Shape with an Image</span></span>
<span data-ttu-id="99c6b-103">Tout comme les vignettes peuvent être placés à côté des autres pour couvrir un étage, rectangulaires images peuvent être placés en regard de chacun des autres sur fill (mosaïque) une forme.</span><span class="sxs-lookup"><span data-stu-id="99c6b-103">Just as tiles can be placed next to each other to cover a floor, rectangular images can be placed next to each other to fill (tile) a shape.</span></span> <span data-ttu-id="99c6b-104">Pour disposer en mosaïque à l’intérieur d’une forme, utilisez un pinceau de la texture.</span><span class="sxs-lookup"><span data-stu-id="99c6b-104">To tile the interior of a shape, use a texture brush.</span></span> <span data-ttu-id="99c6b-105">Lorsque vous construisez un <xref:System.Drawing.TextureBrush> de l’objet, un des arguments que vous passez au constructeur est un <xref:System.Drawing.Image> objet.</span><span class="sxs-lookup"><span data-stu-id="99c6b-105">When you construct a <xref:System.Drawing.TextureBrush> object, one of the arguments you pass to the constructor is an <xref:System.Drawing.Image> object.</span></span> <span data-ttu-id="99c6b-106">Lorsque vous utilisez le pinceau de texture pour peindre l’intérieur d’une forme, la forme est remplie avec les copies répétées de cette image.</span><span class="sxs-lookup"><span data-stu-id="99c6b-106">When you use the texture brush to paint the interior of a shape, the shape is filled with repeated copies of this image.</span></span>  
  
 <span data-ttu-id="99c6b-107">La propriété de mode de retour à la ligne de la <xref:System.Drawing.TextureBrush> objet détermine comment l’image est orienté comme il est répété dans une grille rectangulaire.</span><span class="sxs-lookup"><span data-stu-id="99c6b-107">The wrap mode property of the <xref:System.Drawing.TextureBrush> object determines how the image is oriented as it is repeated in a rectangular grid.</span></span> <span data-ttu-id="99c6b-108">Vous pouvez effectuer toutes les vignettes dans la grille ont la même orientation, ou vous pouvez rendre une image de retournement d’une position à l’autre.</span><span class="sxs-lookup"><span data-stu-id="99c6b-108">You can make all the tiles in the grid have the same orientation, or you can make the image flip from one grid position to the next.</span></span> <span data-ttu-id="99c6b-109">La rotation peut être horizontale, verticale ou les deux.</span><span class="sxs-lookup"><span data-stu-id="99c6b-109">The flipping can be horizontal, vertical, or both.</span></span> <span data-ttu-id="99c6b-110">Les exemples suivants illustrent une mosaïque avec différents types de rotation.</span><span class="sxs-lookup"><span data-stu-id="99c6b-110">The following examples demonstrate tiling with different types of flipping.</span></span>  
  
### <a name="to-tile-an-image"></a><span data-ttu-id="99c6b-111">À la vignette d’une image</span><span class="sxs-lookup"><span data-stu-id="99c6b-111">To tile an image</span></span>  
  
- <span data-ttu-id="99c6b-112">Cet exemple utilise l’image 75 × 75 suivante à la vignette d’un rectangle 200 × 200.</span><span class="sxs-lookup"><span data-stu-id="99c6b-112">This example uses the following 75×75 image to tile a 200×200 rectangle.</span></span>  
  
 <span data-ttu-id="99c6b-113">![Vignette 1](./media/tile1.gif "tile1")</span><span class="sxs-lookup"><span data-stu-id="99c6b-113">![Tile 1](./media/tile1.gif "tile1")</span></span>  
  
- <span data-ttu-id="99c6b-114">L’illustration suivante montre la façon dont le rectangle est affichée en mosaïque avec l’image.</span><span class="sxs-lookup"><span data-stu-id="99c6b-114">The following illustration shows how the rectangle is tiled with the image.</span></span> <span data-ttu-id="99c6b-115">Notez que toutes les vignettes ont la même orientation ; Il n’existe aucun retournement.</span><span class="sxs-lookup"><span data-stu-id="99c6b-115">Note that all tiles have the same orientation; there is no flipping.</span></span>  
  
 <span data-ttu-id="99c6b-116">![Vignette 2](./media/tile2.gif "tile2")</span><span class="sxs-lookup"><span data-stu-id="99c6b-116">![Tile 2](./media/tile2.gif "tile2")</span></span>  
  
 [!code-csharp[System.Drawing.UsingABrush#31](~/samples/snippets/csharp/VS_Snippets_Winforms/System.Drawing.UsingABrush/CS/Class1.cs#31)]
 [!code-vb[System.Drawing.UsingABrush#31](~/samples/snippets/visualbasic/VS_Snippets_Winforms/System.Drawing.UsingABrush/VB/Class1.vb#31)]  
  
### <a name="to-flip-an-image-horizontally-while-tiling"></a><span data-ttu-id="99c6b-117">Pour faire pivoter une image horizontalement lors de la disposition en mosaïque</span><span class="sxs-lookup"><span data-stu-id="99c6b-117">To flip an image horizontally while tiling</span></span>  
  
- <span data-ttu-id="99c6b-118">Cet exemple utilise la même image 75 × 75 pour remplir un rectangle 200 × 200.</span><span class="sxs-lookup"><span data-stu-id="99c6b-118">This example uses the same 75×75 image to fill a 200×200 rectangle.</span></span> <span data-ttu-id="99c6b-119">Le mode habillage est défini pour retourner l’image horizontalement.</span><span class="sxs-lookup"><span data-stu-id="99c6b-119">The wrap mode is set to flip the image horizontally.</span></span> <span data-ttu-id="99c6b-120">L’illustration suivante montre la façon dont le rectangle est affichée en mosaïque avec l’image.</span><span class="sxs-lookup"><span data-stu-id="99c6b-120">The following illustration shows how the rectangle is tiled with the image.</span></span> <span data-ttu-id="99c6b-121">Notez que lorsque vous déplacez à partir d’une vignette à l’autre dans une ligne donnée, l’image est retournée horizontalement.</span><span class="sxs-lookup"><span data-stu-id="99c6b-121">Note that as you move from one tile to the next in a given row, the image is flipped horizontally.</span></span>  
  
 <span data-ttu-id="99c6b-122">![Vignette 3](./media/tile3.gif "tile3")</span><span class="sxs-lookup"><span data-stu-id="99c6b-122">![Tile 3](./media/tile3.gif "tile3")</span></span>  
  
 [!code-csharp[System.Drawing.UsingABrush#32](~/samples/snippets/csharp/VS_Snippets_Winforms/System.Drawing.UsingABrush/CS/Class1.cs#32)]
 [!code-vb[System.Drawing.UsingABrush#32](~/samples/snippets/visualbasic/VS_Snippets_Winforms/System.Drawing.UsingABrush/VB/Class1.vb#32)]  
  
### <a name="to-flip-an-image-vertically-while-tiling"></a><span data-ttu-id="99c6b-123">Pour faire pivoter une image verticalement lors de la disposition en mosaïque</span><span class="sxs-lookup"><span data-stu-id="99c6b-123">To flip an image vertically while tiling</span></span>  
  
- <span data-ttu-id="99c6b-124">Cet exemple utilise la même image 75 × 75 pour remplir un rectangle 200 × 200.</span><span class="sxs-lookup"><span data-stu-id="99c6b-124">This example uses the same 75×75 image to fill a 200×200 rectangle.</span></span> <span data-ttu-id="99c6b-125">Le mode habillage est défini pour retourner l’image verticalement.</span><span class="sxs-lookup"><span data-stu-id="99c6b-125">The wrap mode is set to flip the image vertically.</span></span>  
  
     [!code-csharp[System.Drawing.UsingABrush#33](~/samples/snippets/csharp/VS_Snippets_Winforms/System.Drawing.UsingABrush/CS/Class1.cs#33)]
     [!code-vb[System.Drawing.UsingABrush#33](~/samples/snippets/visualbasic/VS_Snippets_Winforms/System.Drawing.UsingABrush/VB/Class1.vb#33)]  
  
### <a name="to-flip-an-image-horizontally-and-vertically-while-tiling"></a><span data-ttu-id="99c6b-126">Pour faire pivoter une image horizontalement et verticalement mosaïque</span><span class="sxs-lookup"><span data-stu-id="99c6b-126">To flip an image horizontally and vertically while tiling</span></span>  
  
- <span data-ttu-id="99c6b-127">Cet exemple utilise la même image 75 × 75 à la vignette d’un rectangle 200 × 200.</span><span class="sxs-lookup"><span data-stu-id="99c6b-127">This example uses the same 75×75 image to tile a 200×200 rectangle.</span></span> <span data-ttu-id="99c6b-128">Le mode habillage est défini pour retourner l’image horizontalement et verticalement.</span><span class="sxs-lookup"><span data-stu-id="99c6b-128">The wrap mode is set to flip the image both horizontally and vertically.</span></span> <span data-ttu-id="99c6b-129">L’illustration suivante montre la façon dont le rectangle est affichée en mosaïque par l’image.</span><span class="sxs-lookup"><span data-stu-id="99c6b-129">The following illustration shows how the rectangle is tiled by the image.</span></span> <span data-ttu-id="99c6b-130">Notez que lorsque vous déplacez à partir d’une vignette à l’autre dans une ligne donnée, l’image est retournée horizontalement, et lorsque vous passez d’une image à la suivante dans une colonne donnée, l’image est retournée verticalement.</span><span class="sxs-lookup"><span data-stu-id="99c6b-130">Note that as you move from one tile to the next in a given row, the image is flipped horizontally, and as you move from one tile to the next in a given column, the image is flipped vertically.</span></span>  
  
 <span data-ttu-id="99c6b-131">![Vignette 5](./media/tile5.gif "tile5")</span><span class="sxs-lookup"><span data-stu-id="99c6b-131">![Tile 5](./media/tile5.gif "tile5")</span></span>  
  
 [!code-csharp[System.Drawing.UsingABrush#34](~/samples/snippets/csharp/VS_Snippets_Winforms/System.Drawing.UsingABrush/CS/Class1.cs#34)]
 [!code-vb[System.Drawing.UsingABrush#34](~/samples/snippets/visualbasic/VS_Snippets_Winforms/System.Drawing.UsingABrush/VB/Class1.vb#34)]  
  
## <a name="see-also"></a><span data-ttu-id="99c6b-132">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="99c6b-132">See also</span></span>

- [<span data-ttu-id="99c6b-133">Utilisation d'un pinceau pour remplir des formes</span><span class="sxs-lookup"><span data-stu-id="99c6b-133">Using a Brush to Fill Shapes</span></span>](using-a-brush-to-fill-shapes.md)
