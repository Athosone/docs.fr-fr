---
title: 'Procédure : Créer une image bitmap à partir d’un visuel'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- bitmaps [WPF], rendering from visuals
- visuals [WPF], rendering to bitmaps
ms.assetid: 103fc7f5-7306-4026-9d61-2005e79959f3
ms.openlocfilehash: a622d99f7c477f8654526ed399f1eb37288682fe
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59189875"
---
# <a name="how-to-create-a-bitmap-from-a-visual"></a><span data-ttu-id="2b195-102">Procédure : Créer une image bitmap à partir d’un visuel</span><span class="sxs-lookup"><span data-stu-id="2b195-102">How to: Create a Bitmap from a Visual</span></span>
<span data-ttu-id="2b195-103">Cet exemple montre comment vous pouvez créer une image bitmap à partir d’un <xref:System.Windows.Media.Visual>.</span><span class="sxs-lookup"><span data-stu-id="2b195-103">This example shows how you can create a bitmap from a <xref:System.Windows.Media.Visual>.</span></span> <span data-ttu-id="2b195-104">Un <xref:System.Windows.Media.DrawingVisual> est rendue avec <xref:System.Windows.Media.FormattedText>.</span><span class="sxs-lookup"><span data-stu-id="2b195-104">A <xref:System.Windows.Media.DrawingVisual> is rendered with <xref:System.Windows.Media.FormattedText>.</span></span> <span data-ttu-id="2b195-105">Le <xref:System.Windows.Media.Visual> est ensuite rendu dans le <xref:System.Windows.Media.Imaging.RenderTargetBitmap> création d’une bitmap d’un texte donné.</span><span class="sxs-lookup"><span data-stu-id="2b195-105">The <xref:System.Windows.Media.Visual> is then rendered to the <xref:System.Windows.Media.Imaging.RenderTargetBitmap> creating a bitmap of the given text.</span></span>  
  
## <a name="example"></a><span data-ttu-id="2b195-106">Exemple</span><span class="sxs-lookup"><span data-stu-id="2b195-106">Example</span></span>  
 [!code-csharp[ImagingSnippetGallery_procedural_snip#CreateRTBImage](~/samples/snippets/csharp/VS_Snippets_Wpf/ImagingSnippetGallery_procedural_snip/CSharp/RenderTargetBitmapExample.cs#creatertbimage)]
 [!code-vb[ImagingSnippetGallery_procedural_snip#CreateRTBImage](~/samples/snippets/visualbasic/VS_Snippets_Wpf/ImagingSnippetGallery_procedural_snip/VB/RenderTargetBitmapExample.vb#creatertbimage)]  
  
## <a name="see-also"></a><span data-ttu-id="2b195-107">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="2b195-107">See also</span></span>

- <xref:System.Windows.Media.DrawingContext>
- [<span data-ttu-id="2b195-108">Vue d’ensemble de la création d’images</span><span class="sxs-lookup"><span data-stu-id="2b195-108">Imaging Overview</span></span>](imaging-overview.md)
- [<span data-ttu-id="2b195-109">Vue d’ensemble des objets de dessin</span><span class="sxs-lookup"><span data-stu-id="2b195-109">Drawing Objects Overview</span></span>](drawing-objects-overview.md)
- [<span data-ttu-id="2b195-110">Utilisation d’objets DrawingVisual</span><span class="sxs-lookup"><span data-stu-id="2b195-110">Using DrawingVisual Objects</span></span>](using-drawingvisual-objects.md)
