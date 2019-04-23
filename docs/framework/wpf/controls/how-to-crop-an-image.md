---
title: 'Procédure : Rogner une image'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- images [WPF], cropping
- cropping images [WPF]
ms.assetid: c6bba109-c6e7-4cf8-bfe6-9cf8d01bb4fc
ms.openlocfilehash: e672c7e24ec4db2d6424fa0b611cb1c135cf8eec
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59195551"
---
# <a name="how-to-crop-an-image"></a><span data-ttu-id="b3db9-102">Procédure : Rogner une image</span><span class="sxs-lookup"><span data-stu-id="b3db9-102">How to: Crop an Image</span></span>
<span data-ttu-id="b3db9-103">Cet exemple montre comment rogner une image à l’aide <xref:System.Windows.Media.Imaging.CroppedBitmap>.</span><span class="sxs-lookup"><span data-stu-id="b3db9-103">This example shows how to crop an image using <xref:System.Windows.Media.Imaging.CroppedBitmap>.</span></span>  
  
 <span data-ttu-id="b3db9-104"><xref:System.Windows.Media.Imaging.CroppedBitmap> est principalement utilisée lors de l’encodage d’une version d’une image rognée à enregistrer dans un fichier.</span><span class="sxs-lookup"><span data-stu-id="b3db9-104"><xref:System.Windows.Media.Imaging.CroppedBitmap> is primarily used when encoding a cropped version of an image to save out to a file.</span></span> <span data-ttu-id="b3db9-105">Pour rogner une image à des fins d’affichage, consultez le [Comment : Créer une zone de découpage](https://docs.microsoft.com/previous-versions/dotnet/netframework-3.5/ms746710(v=vs.90)) rubrique.</span><span class="sxs-lookup"><span data-stu-id="b3db9-105">To crop an image for display purposes see the [How to: Create a Clip Region](https://docs.microsoft.com/previous-versions/dotnet/netframework-3.5/ms746710(v=vs.90)) topic.</span></span>  
  
## <a name="example"></a><span data-ttu-id="b3db9-106">Exemple</span><span class="sxs-lookup"><span data-stu-id="b3db9-106">Example</span></span>  
 <span data-ttu-id="b3db9-107">Ce qui suit [!INCLUDE[TLA#tla_xaml](../../../../includes/tlasharptla-xaml-md.md)] définit les ressources utilisées dans les exemples ci-dessous.</span><span class="sxs-lookup"><span data-stu-id="b3db9-107">The following [!INCLUDE[TLA#tla_xaml](../../../../includes/tlasharptla-xaml-md.md)] defines resources used within the samples below.</span></span>  
  
 [!code-xaml[imageelementexample#CroppedXAML1](~/samples/snippets/csharp/VS_Snippets_Wpf/ImageElementExample/CSharp/CroppedImageExample.xaml#croppedxaml1)]  
  
 <span data-ttu-id="b3db9-108">L’exemple suivant crée une image à l’aide un <xref:System.Windows.Media.Imaging.CroppedBitmap> comme source.</span><span class="sxs-lookup"><span data-stu-id="b3db9-108">The following example creates an image using a <xref:System.Windows.Media.Imaging.CroppedBitmap> as its source.</span></span>  
  
 [!code-xaml[imageelementexample#CroppedXAML2](~/samples/snippets/csharp/VS_Snippets_Wpf/ImageElementExample/CSharp/CroppedImageExample.xaml#croppedxaml2)]  
  
 [!code-csharp[imageelementexample#CroppedCSharp1](~/samples/snippets/csharp/VS_Snippets_Wpf/ImageElementExample/CSharp/CroppedImageExample.xaml.cs#croppedcsharp1)]
 [!code-vb[imageelementexample#CroppedCSharp1](~/samples/snippets/visualbasic/VS_Snippets_Wpf/ImageElementExample/VB/CroppedImageExample.xaml.vb#croppedcsharp1)]  
  
 <span data-ttu-id="b3db9-109">Le <xref:System.Windows.Media.Imaging.CroppedBitmap> peut également être utilisé comme source d’un autre <xref:System.Windows.Media.Imaging.CroppedBitmap>, chaînant le rognage.</span><span class="sxs-lookup"><span data-stu-id="b3db9-109">The <xref:System.Windows.Media.Imaging.CroppedBitmap> can also be used as the source of another <xref:System.Windows.Media.Imaging.CroppedBitmap>, chaining the cropping.</span></span> <span data-ttu-id="b3db9-110">Notez que le <xref:System.Windows.Media.Imaging.CroppedBitmap.SourceRect%2A> utilise les valeurs par rapport à la bitmap source rogné et pas l’image initiale.</span><span class="sxs-lookup"><span data-stu-id="b3db9-110">Note that the <xref:System.Windows.Media.Imaging.CroppedBitmap.SourceRect%2A> uses values that are relative to the source cropped bitmap and not the initial image.</span></span>  
  
 [!code-xaml[imageelementexample#CroppedXAML3](~/samples/snippets/csharp/VS_Snippets_Wpf/ImageElementExample/CSharp/CroppedImageExample.xaml#croppedxaml3)]  
  
 [!code-csharp[imageelementexample#CroppedCSharp2](~/samples/snippets/csharp/VS_Snippets_Wpf/ImageElementExample/CSharp/CroppedImageExample.xaml.cs#croppedcsharp2)]
 [!code-vb[imageelementexample#CroppedCSharp2](~/samples/snippets/visualbasic/VS_Snippets_Wpf/ImageElementExample/VB/CroppedImageExample.xaml.vb#croppedcsharp2)]  
  
## <a name="see-also"></a><span data-ttu-id="b3db9-111">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b3db9-111">See also</span></span>

- <span data-ttu-id="b3db9-112">[Guide pratique pour Créer une zone de découpage](https://docs.microsoft.com/previous-versions/dotnet/netframework-3.5/ms746710(v=vs.90))</span><span class="sxs-lookup"><span data-stu-id="b3db9-112">[How to: Create a Clip Region](https://docs.microsoft.com/previous-versions/dotnet/netframework-3.5/ms746710(v=vs.90))</span></span>
