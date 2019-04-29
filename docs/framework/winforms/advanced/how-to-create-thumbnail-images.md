---
title: 'Procédure : créer des images miniatures'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- thumbnail images [Windows Forms], creating
- images [Windows Forms], creating thumbnails
ms.assetid: e956242a-1e5b-4217-a3cf-5f3fb45d00ba
ms.openlocfilehash: b9afbac85dee90938e2bd55ebe19d3b02c0d66d5
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61937634"
---
# <a name="how-to-create-thumbnail-images"></a><span data-ttu-id="29871-102">Procédure : créer des images miniatures</span><span class="sxs-lookup"><span data-stu-id="29871-102">How to: Create Thumbnail Images</span></span>
<span data-ttu-id="29871-103">Une image miniature est une version réduite d’une image.</span><span class="sxs-lookup"><span data-stu-id="29871-103">A thumbnail image is a small version of an image.</span></span> <span data-ttu-id="29871-104">Vous pouvez créer une image miniature en appelant le <xref:System.Drawing.Image.GetThumbnailImage%2A> méthode d’un <xref:System.Drawing.Image> objet.</span><span class="sxs-lookup"><span data-stu-id="29871-104">You can create a thumbnail image by calling the <xref:System.Drawing.Image.GetThumbnailImage%2A> method of an <xref:System.Drawing.Image> object.</span></span>  
  
## <a name="example"></a><span data-ttu-id="29871-105">Exemple</span><span class="sxs-lookup"><span data-stu-id="29871-105">Example</span></span>  
 <span data-ttu-id="29871-106">L’exemple suivant construit un <xref:System.Drawing.Image> objet à partir d’un fichier JPG.</span><span class="sxs-lookup"><span data-stu-id="29871-106">The following example constructs an <xref:System.Drawing.Image> object from a JPG file.</span></span> <span data-ttu-id="29871-107">L’image d’origine a une largeur de 640 pixels et une hauteur de 479 pixels.</span><span class="sxs-lookup"><span data-stu-id="29871-107">The original image has a width of 640 pixels and a height of 479 pixels.</span></span> <span data-ttu-id="29871-108">Le code crée une image miniature qui a une largeur de 100 pixels et une hauteur de 100 pixels.</span><span class="sxs-lookup"><span data-stu-id="29871-108">The code creates a thumbnail image that has a width of 100 pixels and a height of 100 pixels.</span></span>  
  
 <span data-ttu-id="29871-109">L’illustration suivante montre l’image miniature.</span><span class="sxs-lookup"><span data-stu-id="29871-109">The following illustration shows the thumbnail image.</span></span>  
  
 <span data-ttu-id="29871-110">![Image miniature](./media/thumbnail1.png "Thumbnail1")</span><span class="sxs-lookup"><span data-stu-id="29871-110">![Thumbnail Image](./media/thumbnail1.png "Thumbnail1")</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="29871-111">Dans cet exemple, une méthode de rappel est déclarée mais jamais utilisée.</span><span class="sxs-lookup"><span data-stu-id="29871-111">In this example, a callback method is declared, but never used.</span></span> <span data-ttu-id="29871-112">Cela prend en charge toutes les versions de GDI +.</span><span class="sxs-lookup"><span data-stu-id="29871-112">This supports all versions of GDI+.</span></span>  
  
 [!code-csharp[System.Drawing.WorkingWithImages#71](~/samples/snippets/csharp/VS_Snippets_Winforms/System.Drawing.WorkingWithImages/CS/Class1.cs#71)]
 [!code-vb[System.Drawing.WorkingWithImages#71](~/samples/snippets/visualbasic/VS_Snippets_Winforms/System.Drawing.WorkingWithImages/VB/Class1.vb#71)]  
  
## <a name="compiling-the-code"></a><span data-ttu-id="29871-113">Compilation du code</span><span class="sxs-lookup"><span data-stu-id="29871-113">Compiling the Code</span></span>  
 <span data-ttu-id="29871-114">L’exemple précédent est conçu pour une utilisation avec Windows Forms et nécessite <xref:System.Windows.Forms.PaintEventArgs> `e`, qui est un paramètre de la <xref:System.Windows.Forms.Control.Paint> Gestionnaire d’événements.</span><span class="sxs-lookup"><span data-stu-id="29871-114">The preceding example is designed for use with Windows Forms, and it requires <xref:System.Windows.Forms.PaintEventArgs> `e`, which is a parameter of the <xref:System.Windows.Forms.Control.Paint> event handler.</span></span> <span data-ttu-id="29871-115">Pour exécuter l’exemple, procédez comme suit :</span><span class="sxs-lookup"><span data-stu-id="29871-115">To run the example, follow these steps:</span></span>  
  
1. <span data-ttu-id="29871-116">Créez une application Windows Forms.</span><span class="sxs-lookup"><span data-stu-id="29871-116">Create a new Windows Forms application.</span></span>  
  
2. <span data-ttu-id="29871-117">Ajoutez l’exemple de code au formulaire.</span><span class="sxs-lookup"><span data-stu-id="29871-117">Add the example code to the form.</span></span>  
  
3. <span data-ttu-id="29871-118">Créez un gestionnaire pour le formulaire <xref:System.Windows.Forms.Control.Paint> événement</span><span class="sxs-lookup"><span data-stu-id="29871-118">Create a handler for the form's <xref:System.Windows.Forms.Control.Paint> event</span></span>  
  
4. <span data-ttu-id="29871-119">Dans le <xref:System.Windows.Forms.Control.Paint> gestionnaire, appelez le `GetThumbnail` (méthode) et passez `e` pour <xref:System.Windows.Forms.PaintEventArgs>.</span><span class="sxs-lookup"><span data-stu-id="29871-119">In the <xref:System.Windows.Forms.Control.Paint> handler, call the `GetThumbnail` method and pass `e` for <xref:System.Windows.Forms.PaintEventArgs>.</span></span>  
  
5. <span data-ttu-id="29871-120">Rechercher un fichier image que vous souhaitez faire une miniature.</span><span class="sxs-lookup"><span data-stu-id="29871-120">Find an image file that you want to make a thumbnail of.</span></span>  
  
6. <span data-ttu-id="29871-121">Dans le `GetThumbnail` (méthode), spécifiez le chemin d’accès et le nom à votre image de fichier.</span><span class="sxs-lookup"><span data-stu-id="29871-121">In the `GetThumbnail` method, specify the path and file name to your image.</span></span>  
  
7. <span data-ttu-id="29871-122">Appuyez sur F5 pour exécuter l’exemple.</span><span class="sxs-lookup"><span data-stu-id="29871-122">Press F5 to run the example.</span></span>  
  
     <span data-ttu-id="29871-123">Une image miniature de 100 par 100 s’affiche sur le formulaire.</span><span class="sxs-lookup"><span data-stu-id="29871-123">A 100 by 100 thumbnail image appears on the form.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="29871-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="29871-124">See also</span></span>

- [<span data-ttu-id="29871-125">Images, bitmaps et métafichiers</span><span class="sxs-lookup"><span data-stu-id="29871-125">Images, Bitmaps, and Metafiles</span></span>](images-bitmaps-and-metafiles.md)
- [<span data-ttu-id="29871-126">Utilisation des images, bitmaps, icônes et métafichiers</span><span class="sxs-lookup"><span data-stu-id="29871-126">Working with Images, Bitmaps, Icons, and Metafiles</span></span>](working-with-images-bitmaps-icons-and-metafiles.md)
