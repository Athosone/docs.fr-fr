---
title: 'Procédure : afficher des icônes pour le contrôle ListView Windows Forms'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- ListView control [Windows Forms], displaying icons
- icons [Windows Forms], displaying for ListView controls
- lists [Windows Forms], displaying icons
- ImageList component [Windows Forms], with ListView control
- list views [Windows Forms], displaying icons
ms.assetid: 9d577542-8595-429b-99e5-078770ec9d35
ms.openlocfilehash: 8e4ae744eecbe894767114179dd63651828b191b
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59318609"
---
# <a name="how-to-display-icons-for-the-windows-forms-listview-control"></a><span data-ttu-id="84428-102">Procédure : afficher des icônes pour le contrôle ListView Windows Forms</span><span class="sxs-lookup"><span data-stu-id="84428-102">How to: Display Icons for the Windows Forms ListView Control</span></span>
<span data-ttu-id="84428-103">Les formulaires Windows <xref:System.Windows.Forms.ListView> contrôle peut afficher des icônes à partir de trois listes d’images.</span><span class="sxs-lookup"><span data-stu-id="84428-103">The Windows Forms <xref:System.Windows.Forms.ListView> control can display icons from three image lists.</span></span> <span data-ttu-id="84428-104">Les vues de liste, les détails et SmallIcon affichent des images à partir de la liste d’images spécifié dans le <xref:System.Windows.Forms.ListView.SmallImageList%2A> propriété.</span><span class="sxs-lookup"><span data-stu-id="84428-104">The List, Details, and SmallIcon views display images from the image list specified in the <xref:System.Windows.Forms.ListView.SmallImageList%2A> property.</span></span> <span data-ttu-id="84428-105">La vue LargeIcon affiche des images à partir de la liste d’images spécifié dans le <xref:System.Windows.Forms.ListView.LargeImageList%2A> propriété.</span><span class="sxs-lookup"><span data-stu-id="84428-105">The LargeIcon view displays images from the image list specified in the <xref:System.Windows.Forms.ListView.LargeImageList%2A> property.</span></span> <span data-ttu-id="84428-106">Un affichage de liste peut également afficher un ensemble supplémentaire d’icônes, défini le <xref:System.Windows.Forms.ListView.StateImageList%2A> propriété, en regard des petites ou grandes icônes.</span><span class="sxs-lookup"><span data-stu-id="84428-106">A list view can also display an additional set of icons, set in the <xref:System.Windows.Forms.ListView.StateImageList%2A> property, next to the large or small icons.</span></span> <span data-ttu-id="84428-107">Pour plus d’informations sur les listes d’images, consultez [composant ImageList](imagelist-component-windows-forms.md) et [Comment : Ajouter ou supprimer des Images avec les Windows Forms composant ImageList](how-to-add-or-remove-images-with-the-windows-forms-imagelist-component.md).</span><span class="sxs-lookup"><span data-stu-id="84428-107">For more information about image lists, see [ImageList Component](imagelist-component-windows-forms.md) and [How to: Add or Remove Images with the Windows Forms ImageList Component](how-to-add-or-remove-images-with-the-windows-forms-imagelist-component.md).</span></span>  
  
### <a name="to-display-images-in-a-list-view"></a><span data-ttu-id="84428-108">Pour afficher des images dans une vue liste</span><span class="sxs-lookup"><span data-stu-id="84428-108">To display images in a list view</span></span>  
  
1. <span data-ttu-id="84428-109">Définissez la propriété appropriée :<xref:System.Windows.Forms.ListView.SmallImageList%2A>, <xref:System.Windows.Forms.ListView.LargeImageList%2A>, ou <xref:System.Windows.Forms.ListView.StateImageList%2A>— à l’objet existant <xref:System.Windows.Forms.ImageList> composant que vous souhaitez utiliser.</span><span class="sxs-lookup"><span data-stu-id="84428-109">Set the appropriate property—<xref:System.Windows.Forms.ListView.SmallImageList%2A>, <xref:System.Windows.Forms.ListView.LargeImageList%2A>, or <xref:System.Windows.Forms.ListView.StateImageList%2A>—to the existing <xref:System.Windows.Forms.ImageList> component you wish to use.</span></span>  
  
     <span data-ttu-id="84428-110">Ces propriétés peuvent être définies dans le concepteur avec la fenêtre Propriétés ou dans le code.</span><span class="sxs-lookup"><span data-stu-id="84428-110">These properties can be set in the designer with the Properties window, or in code.</span></span>  
  
     [!code-csharp[System.Windows.Forms.ListViewLegacyTopics#41](~/samples/snippets/csharp/VS_Snippets_Winforms/System.Windows.Forms.ListViewLegacyTopics/CS/Class1.cs#41)]
     [!code-vb[System.Windows.Forms.ListViewLegacyTopics#41](~/samples/snippets/visualbasic/VS_Snippets_Winforms/System.Windows.Forms.ListViewLegacyTopics/VB/Class1.vb#41)]  
  
2. <span data-ttu-id="84428-111">Définir le <xref:System.Windows.Forms.ListViewItem.ImageIndex%2A> ou <xref:System.Windows.Forms.ListViewItem.StateImageIndex%2A> propriété pour chaque élément de liste qui a une icône associée.</span><span class="sxs-lookup"><span data-stu-id="84428-111">Set the <xref:System.Windows.Forms.ListViewItem.ImageIndex%2A> or <xref:System.Windows.Forms.ListViewItem.StateImageIndex%2A> property for each list item that has an associated icon.</span></span>  
  
     <span data-ttu-id="84428-112">Ces propriétés peuvent être définies dans le code ou dans le **éditeur de collections ListViewItem**.</span><span class="sxs-lookup"><span data-stu-id="84428-112">These properties can be set in code, or within the **ListViewItem Collection Editor**.</span></span> <span data-ttu-id="84428-113">Pour ouvrir le **éditeur de collections ListViewItem**, cliquez sur le bouton de sélection (![d’écran de VisualStudioEllipsesButton](../media/vbellipsesbutton.png "vbEllipsesButton")) en regard de la <xref:System.Windows.Forms.ListView.Items%2A>propriété sur le **propriétés** fenêtre.</span><span class="sxs-lookup"><span data-stu-id="84428-113">To open the **ListViewItem Collection Editor**, click the ellipsis button (![VisualStudioEllipsesButton screenshot](../media/vbellipsesbutton.png "vbEllipsesButton")) next to the <xref:System.Windows.Forms.ListView.Items%2A> property on the **Properties** window.</span></span>  
  
     [!code-csharp[System.Windows.Forms.ListViewLegacyTopics#42](~/samples/snippets/csharp/VS_Snippets_Winforms/System.Windows.Forms.ListViewLegacyTopics/CS/Class1.cs#42)]
     [!code-vb[System.Windows.Forms.ListViewLegacyTopics#42](~/samples/snippets/visualbasic/VS_Snippets_Winforms/System.Windows.Forms.ListViewLegacyTopics/VB/Class1.vb#42)]  
  
## <a name="see-also"></a><span data-ttu-id="84428-114">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="84428-114">See also</span></span>

- [<span data-ttu-id="84428-115">Vue d’ensemble du contrôle ListView</span><span class="sxs-lookup"><span data-stu-id="84428-115">ListView Control Overview</span></span>](listview-control-overview-windows-forms.md)
- [<span data-ttu-id="84428-116">Guide pratique pour Ajouter et supprimer des éléments avec le contrôle ListView Windows Forms</span><span class="sxs-lookup"><span data-stu-id="84428-116">How to: Add and Remove Items with the Windows Forms ListView Control</span></span>](how-to-add-and-remove-items-with-the-windows-forms-listview-control.md)
- [<span data-ttu-id="84428-117">Guide pratique pour Ajouter des colonnes au contrôle ListView Windows Forms</span><span class="sxs-lookup"><span data-stu-id="84428-117">How to: Add Columns to the Windows Forms ListView Control</span></span>](how-to-add-columns-to-the-windows-forms-listview-control.md)
- [<span data-ttu-id="84428-118">Guide pratique pour Ajouter des informations personnalisées à un contrôle TreeView ou ListView (Windows Forms)</span><span class="sxs-lookup"><span data-stu-id="84428-118">How to: Add Custom Information to a TreeView or ListView Control (Windows Forms)</span></span>](add-custom-information-to-a-treeview-or-listview-control-wf.md)
- [<span data-ttu-id="84428-119">ImageList, composant</span><span class="sxs-lookup"><span data-stu-id="84428-119">ImageList Component</span></span>](imagelist-component-windows-forms.md)
