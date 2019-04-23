---
title: 'Procédure : ajouter et supprimer des éléments avec le contrôle ListView Windows Forms à l’aide du concepteur'
ms.date: 03/30/2017
helpviewer_keywords:
- ListView control [Windows Forms], populating
- ListView control [Windows Forms], adding list items
ms.assetid: 217611ee-fd11-4d39-9a54-a37c3e781be1
ms.openlocfilehash: 6e08a7013242b0dbb433e288c4f8d788cb4e143b
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59343842"
---
# <a name="how-to-add-and-remove-items-with-the-windows-forms-listview-control-using-the-designer"></a><span data-ttu-id="950ed-102">Procédure : ajouter et supprimer des éléments avec le contrôle ListView Windows Forms à l’aide du concepteur</span><span class="sxs-lookup"><span data-stu-id="950ed-102">How to: Add and Remove Items with the Windows Forms ListView Control Using the Designer</span></span>
<span data-ttu-id="950ed-103">Le processus d’ajout d’un élément à un formulaire Windows <xref:System.Windows.Forms.ListView> contrôle se compose principalement de la spécification de l’élément et lui assigner des propriétés.</span><span class="sxs-lookup"><span data-stu-id="950ed-103">The process of adding an item to a Windows Forms <xref:System.Windows.Forms.ListView> control consists primarily of specifying the item and assigning properties to it.</span></span> <span data-ttu-id="950ed-104">Ajouter ou supprimer des éléments de liste peut être effectuée à tout moment.</span><span class="sxs-lookup"><span data-stu-id="950ed-104">Adding or removing list items can be done at any time.</span></span>  
  
 <span data-ttu-id="950ed-105">La procédure suivante nécessite un **Windows Application** projet avec un formulaire contenant un <xref:System.Windows.Forms.ListView> contrôle.</span><span class="sxs-lookup"><span data-stu-id="950ed-105">The following procedure requires a **Windows Application** project with a form containing a <xref:System.Windows.Forms.ListView> control.</span></span> <span data-ttu-id="950ed-106">Pour plus d’informations sur la configuration d’un tel projet, consultez [Comment : Créer un projet d’application Windows Forms](/visualstudio/ide/step-1-create-a-windows-forms-application-project) et [Comment : Ajouter des contrôles aux Windows Forms](how-to-add-controls-to-windows-forms.md).</span><span class="sxs-lookup"><span data-stu-id="950ed-106">For information about setting up such a project, see [How to: Create a Windows Forms application project](/visualstudio/ide/step-1-create-a-windows-forms-application-project) and [How to: Add Controls to Windows Forms](how-to-add-controls-to-windows-forms.md).</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="950ed-107">Les boîtes de dialogue et les commandes de menu qui s'affichent peuvent être différentes de celles qui sont décrites dans l'aide, en fonction de vos paramètres actifs ou de l'édition utilisée.</span><span class="sxs-lookup"><span data-stu-id="950ed-107">The dialog boxes and menu commands you see might differ from those described in Help depending on your active settings or edition.</span></span> <span data-ttu-id="950ed-108">Pour modifier vos paramètres, choisissez **Importation et exportation de paramètres** dans le menu **Outils** .</span><span class="sxs-lookup"><span data-stu-id="950ed-108">To change your settings, choose **Import and Export Settings** on the **Tools** menu.</span></span> <span data-ttu-id="950ed-109">Pour plus d’informations, consultez [Personnaliser l’IDE Visual Studio](/visualstudio/ide/personalizing-the-visual-studio-ide).</span><span class="sxs-lookup"><span data-stu-id="950ed-109">For more information, see [Personalize the Visual Studio IDE](/visualstudio/ide/personalizing-the-visual-studio-ide).</span></span>  
  
### <a name="to-add-or-remove-items-using-the-designer"></a><span data-ttu-id="950ed-110">Pour ajouter ou supprimer des éléments à l’aide du Concepteur</span><span class="sxs-lookup"><span data-stu-id="950ed-110">To add or remove items using the designer</span></span>  
  
1. <span data-ttu-id="950ed-111">Sélectionnez le contrôle <xref:System.Windows.Forms.ListView>.</span><span class="sxs-lookup"><span data-stu-id="950ed-111">Select the <xref:System.Windows.Forms.ListView> control.</span></span>  
  
2. <span data-ttu-id="950ed-112">Dans le **propriétés** fenêtre, cliquez sur le **points de suspension** (![d’écran de VisualStudioEllipsesButton](../media/vbellipsesbutton.png "vbEllipsesButton")) situé en regard le <xref:System.Windows.Forms.ListView.Items%2A> propriété.</span><span class="sxs-lookup"><span data-stu-id="950ed-112">In the **Properties** window, click the **Ellipsis** (![VisualStudioEllipsesButton screenshot](../media/vbellipsesbutton.png "vbEllipsesButton")) button next to the <xref:System.Windows.Forms.ListView.Items%2A> property.</span></span>  
  
     <span data-ttu-id="950ed-113">Le **éditeur de collections ListViewItem** s’affiche.</span><span class="sxs-lookup"><span data-stu-id="950ed-113">The **ListViewItem Collection Editor** appears.</span></span>  
  
3. <span data-ttu-id="950ed-114">Pour ajouter un élément, cliquez sur le **ajouter** bouton.</span><span class="sxs-lookup"><span data-stu-id="950ed-114">To add an item, click the **Add** button.</span></span> <span data-ttu-id="950ed-115">Vous pouvez ensuite définir les propriétés du nouvel élément, tel que le <xref:System.Windows.Forms.ListView.Text%2A> et <xref:System.Windows.Forms.ListViewItem.ImageIndex%2A> propriétés.</span><span class="sxs-lookup"><span data-stu-id="950ed-115">You can then set properties of the new item, such as the <xref:System.Windows.Forms.ListView.Text%2A> and <xref:System.Windows.Forms.ListViewItem.ImageIndex%2A> properties.</span></span>  
  
4. <span data-ttu-id="950ed-116">Pour supprimer un élément, sélectionnez-le et cliquez sur le **supprimer** bouton.</span><span class="sxs-lookup"><span data-stu-id="950ed-116">To remove an item, select it and click the **Remove** button.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="950ed-117">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="950ed-117">See also</span></span>

- [<span data-ttu-id="950ed-118">Vue d’ensemble du contrôle ListView</span><span class="sxs-lookup"><span data-stu-id="950ed-118">ListView Control Overview</span></span>](listview-control-overview-windows-forms.md)
- [<span data-ttu-id="950ed-119">Guide pratique pour Ajouter des colonnes au contrôle ListView Windows Forms</span><span class="sxs-lookup"><span data-stu-id="950ed-119">How to: Add Columns to the Windows Forms ListView Control</span></span>](how-to-add-columns-to-the-windows-forms-listview-control.md)
- [<span data-ttu-id="950ed-120">Guide pratique pour Afficher des sous-éléments en colonnes avec le contrôle ListView Windows Forms</span><span class="sxs-lookup"><span data-stu-id="950ed-120">How to: Display Subitems in Columns with the Windows Forms ListView Control</span></span>](how-to-display-subitems-in-columns-with-the-windows-forms-listview-control.md)
- [<span data-ttu-id="950ed-121">Guide pratique pour Afficher des icônes pour le contrôle ListView Windows Forms</span><span class="sxs-lookup"><span data-stu-id="950ed-121">How to: Display Icons for the Windows Forms ListView Control</span></span>](how-to-display-icons-for-the-windows-forms-listview-control.md)
- [<span data-ttu-id="950ed-122">Guide pratique pour Ajouter des informations personnalisées à un contrôle TreeView ou ListView (Windows Forms)</span><span class="sxs-lookup"><span data-stu-id="950ed-122">How to: Add Custom Information to a TreeView or ListView Control (Windows Forms)</span></span>](add-custom-information-to-a-treeview-or-listview-control-wf.md)
- [<span data-ttu-id="950ed-123">Guide pratique pour Grouper des éléments dans un contrôle de ListView Windows Forms</span><span class="sxs-lookup"><span data-stu-id="950ed-123">How to: Group Items in a Windows Forms ListView Control</span></span>](how-to-group-items-in-a-windows-forms-listview-control.md)
