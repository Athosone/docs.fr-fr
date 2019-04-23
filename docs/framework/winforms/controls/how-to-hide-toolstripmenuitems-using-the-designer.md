---
title: 'Procédure : masquer des ToolStripMenuItems à l’aide du concepteur'
ms.date: 03/30/2017
helpviewer_keywords:
- ToolStripMenuItems [Windows Forms], hiding menu items in designer
- MenuStrip control [Windows Forms], hiding menu items in designer
- menu items [Windows Forms], hiding
ms.assetid: 8f1b057e-3d8a-4f11-88df-935f7b29a836
ms.openlocfilehash: 31c597a0e2cbf41484f19c8d4179823e9fb929ba
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59317673"
---
# <a name="how-to-hide-toolstripmenuitems-using-the-designer"></a><span data-ttu-id="2f8d7-102">Procédure : masquer des ToolStripMenuItems à l’aide du concepteur</span><span class="sxs-lookup"><span data-stu-id="2f8d7-102">How to: Hide ToolStripMenuItems Using the Designer</span></span>
<span data-ttu-id="2f8d7-103">Masquage d’éléments de menu est un moyen de contrôler l’interface utilisateur (IU) de votre application et de restreindre les commandes de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="2f8d7-103">Hiding menu items is a way to control the user interface (UI) of your application and restrict user commands.</span></span> <span data-ttu-id="2f8d7-104">Souvent, vous devez masquer un menu quand tous les éléments de menu sur ce dernier ne sont pas disponibles.</span><span class="sxs-lookup"><span data-stu-id="2f8d7-104">Often, you will want to hide an entire menu when all of the menu items on it are unavailable.</span></span> <span data-ttu-id="2f8d7-105">Cela est moins distrait pour l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="2f8d7-105">This presents fewer distractions for the user.</span></span> <span data-ttu-id="2f8d7-106">En outre, vous souhaiterez peut-être cacher et désactiver le menu ou un élément de menu, comme simple masquage n’empêche pas l’utilisateur d’accéder à une commande de menu à l’aide d’une touche de raccourci.</span><span class="sxs-lookup"><span data-stu-id="2f8d7-106">Furthermore, you might want to both hide and disable the menu or menu item, as hiding alone does not prevent the user from accessing a menu command by using a shortcut key.</span></span> <span data-ttu-id="2f8d7-107">Pour plus d’informations sur la désactivation des éléments de menu, consultez [Comment : Désactiver des ToolStripMenuItems à l’aide du concepteur](how-to-disable-toolstripmenuitems-using-the-designer.md).</span><span class="sxs-lookup"><span data-stu-id="2f8d7-107">For more information on disabling menu items, see [How to: Disable ToolStripMenuItems Using the Designer](how-to-disable-toolstripmenuitems-using-the-designer.md).</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="2f8d7-108">Les boîtes de dialogue et les commandes de menu qui s'affichent peuvent être différentes de celles qui sont décrites dans l'aide, en fonction de vos paramètres actifs ou de l'édition utilisée.</span><span class="sxs-lookup"><span data-stu-id="2f8d7-108">The dialog boxes and menu commands you see might differ from those described in Help depending on your active settings or edition.</span></span> <span data-ttu-id="2f8d7-109">Pour modifier vos paramètres, choisissez **Importation et exportation de paramètres** dans le menu **Outils** .</span><span class="sxs-lookup"><span data-stu-id="2f8d7-109">To change your settings, choose **Import and Export Settings** on the **Tools** menu.</span></span> <span data-ttu-id="2f8d7-110">Pour plus d’informations, consultez [Personnaliser l’IDE Visual Studio](/visualstudio/ide/personalizing-the-visual-studio-ide).</span><span class="sxs-lookup"><span data-stu-id="2f8d7-110">For more information, see [Personalize the Visual Studio IDE](/visualstudio/ide/personalizing-the-visual-studio-ide).</span></span>  
  
### <a name="to-hide-a-top-level-menu-and-its-submenu-items"></a><span data-ttu-id="2f8d7-111">Pour masquer un menu de niveau supérieur et ses éléments de sous-menu</span><span class="sxs-lookup"><span data-stu-id="2f8d7-111">To hide a top-level menu and its submenu items</span></span>  
  
1. <span data-ttu-id="2f8d7-112">Sélectionnez l’élément de menu de niveau supérieur et définissez son <xref:System.Windows.Forms.ToolStripItem.Visible%2A> ou <xref:System.Windows.Forms.ToolStripItem.Available%2A> propriété `false`.</span><span class="sxs-lookup"><span data-stu-id="2f8d7-112">Select the top-level menu item and set its <xref:System.Windows.Forms.ToolStripItem.Visible%2A> or <xref:System.Windows.Forms.ToolStripItem.Available%2A> property to `false`.</span></span>  
  
     <span data-ttu-id="2f8d7-113">Lorsque vous masquez l’élément de menu de niveau supérieur, tous les éléments de menu au sein de ce menu sont également masqués.</span><span class="sxs-lookup"><span data-stu-id="2f8d7-113">When you hide the top-level menu item, all menu items within that menu are also hidden.</span></span> <span data-ttu-id="2f8d7-114">Si vous cliquez quelque part autre que sur le <xref:System.Windows.Forms.MenuStrip> après avoir défini <xref:System.Windows.Forms.ToolStripItem.Visible%2A> à `false`, l’élément de menu de niveau supérieur entier et ses éléments de sous-menu disparaissent de votre formulaire, vous montrant ainsi l’effet de l’exécution de votre action.</span><span class="sxs-lookup"><span data-stu-id="2f8d7-114">If you click somewhere other than on the <xref:System.Windows.Forms.MenuStrip> after setting <xref:System.Windows.Forms.ToolStripItem.Visible%2A> to `false`, the entire top-level menu item and its submenu items disappear from your form, thus showing you the run-time effect of your action.</span></span> <span data-ttu-id="2f8d7-115">Pour afficher l’élément de menu de niveau supérieur masqué au moment du design, cliquez sur le <xref:System.Windows.Forms.MenuStrip> dans le **barre d’état du composant**, dans **structure du Document**, ou en haut de la grille des propriétés.</span><span class="sxs-lookup"><span data-stu-id="2f8d7-115">To display the hidden top-level menu item at design time, click on the <xref:System.Windows.Forms.MenuStrip> in the **Component Tray**, in **Document Outline**, or at the top of the property grid.</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="2f8d7-116">Vous allez masquer rarement un menu à l’exception de plusieurs menus enfants MDI (interface) de document dans un scénario de fusion.</span><span class="sxs-lookup"><span data-stu-id="2f8d7-116">You will rarely hide an entire menu except for multiple document interface (MDI) child menus in a merging scenario.</span></span>  
  
### <a name="to-hide-a-submenu-item"></a><span data-ttu-id="2f8d7-117">Pour masquer un élément de sous-menu</span><span class="sxs-lookup"><span data-stu-id="2f8d7-117">To hide a submenu item</span></span>  
  
1. <span data-ttu-id="2f8d7-118">Sélectionnez l’élément de sous-menu et définissez son <xref:System.Windows.Forms.ToolStripItem.Visible%2A> propriété `false`.</span><span class="sxs-lookup"><span data-stu-id="2f8d7-118">Select the submenu item and set its <xref:System.Windows.Forms.ToolStripItem.Visible%2A> property to `false`.</span></span>  
  
     <span data-ttu-id="2f8d7-119">Lorsque vous masquez un élément de sous-menu, il reste visible sur votre formulaire au moment du design afin que vous puissiez le sélectionner facilement pour les tâches ultérieures.</span><span class="sxs-lookup"><span data-stu-id="2f8d7-119">When you hide a submenu item, it remains visible on your form at design time so that you can easily select it for further work.</span></span> <span data-ttu-id="2f8d7-120">Il est en fait masqué au moment de l’exécution.</span><span class="sxs-lookup"><span data-stu-id="2f8d7-120">It will actually be hidden at run time.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="2f8d7-121">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="2f8d7-121">See also</span></span>

- <xref:System.Windows.Forms.ToolStripItem.Visible%2A>
- <xref:System.Windows.Forms.MenuStrip>
- <xref:System.Windows.Forms.ToolStripMenuItem.Enabled%2A>
- <xref:System.Windows.Forms.ToolStripItem.Available%2A>
- <xref:System.Windows.Forms.ToolStripMenuItem.Overflow%2A>
- [<span data-ttu-id="2f8d7-122">Vue d'ensemble du contrôle MenuStrip</span><span class="sxs-lookup"><span data-stu-id="2f8d7-122">MenuStrip Control Overview</span></span>](menustrip-control-overview-windows-forms.md)
- [<span data-ttu-id="2f8d7-123">Guide pratique pour Désactiver des ToolStripMenuItems à l’aide du Concepteur</span><span class="sxs-lookup"><span data-stu-id="2f8d7-123">How to: Disable ToolStripMenuItems Using the Designer</span></span>](how-to-disable-toolstripmenuitems-using-the-designer.md)
