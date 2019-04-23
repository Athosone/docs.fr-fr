---
title: 'Procédure : attacher un menu contextuel à un TreeNode à l’aide du concepteur'
ms.date: 03/30/2017
helpviewer_keywords:
- shortcut menus [Windows Forms], attaching to TreeNodes
- TreeNode [Windows Forms], attaching a shortcut menu using Designer
ms.assetid: 8e45e184-1313-4f8f-90ff-2cd5789b2268
ms.openlocfilehash: 9be633d14429bc2ceda1f0db2ff09252d55d5dd5
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59337446"
---
# <a name="how-to-attach-a-shortcut-menu-to-a-treenode-using-the-designer"></a>Procédure : attacher un menu contextuel à un TreeNode à l’aide du concepteur
Les formulaires Windows <xref:System.Windows.Forms.TreeView> contrôle affiche une hiérarchie de nœuds, similaires aux fichiers et dossiers affichés dans le volet gauche de la fonctionnalité de l’Explorateur Windows dans les systèmes d’exploitation Windows. En définissant le <xref:System.Windows.Forms.Control.ContextMenuStrip%2A> propriété, vous pouvez fournir des opérations contextuelles à l’utilisateur lorsqu’ils avec le bouton droit le <xref:System.Windows.Forms.TreeView> contrôle. En associant un <xref:System.Windows.Forms.ContextMenuStrip> composant individuels <xref:System.Windows.Forms.TreeNode> éléments, vous pouvez ajouter un niveau personnalisé de fonctionnalités de menu contextuel à votre <xref:System.Windows.Forms.TreeView> contrôles.  
  
> [!NOTE]
>  Les boîtes de dialogue et les commandes de menu qui s'affichent peuvent être différentes de celles qui sont décrites dans l'aide, en fonction de vos paramètres actifs ou de l'édition utilisée. Pour modifier vos paramètres, choisissez **Importation et exportation de paramètres** dans le menu **Outils** . Pour plus d’informations, consultez [Personnaliser l’IDE Visual Studio](/visualstudio/ide/personalizing-the-visual-studio-ide).  
  
### <a name="to-associate-a-shortcut-menu-with-a-treenode-at-design-time"></a>Pour associer un menu contextuel à un TreeNode au moment du design  
  
1. Ajouter un <xref:System.Windows.Forms.TreeView> le contrôle à votre formulaire et ajouter des nœuds à la <xref:System.Windows.Forms.TreeView> en fonction des besoins. Pour plus d'informations, voir [Procédure : Ajouter et supprimer des nœuds avec les Windows Forms contrôle TreeView](how-to-add-and-remove-nodes-with-the-windows-forms-treeview-control.md).  
  
2. Ajouter un <xref:System.Windows.Forms.ContextMenuStrip> à votre formulaire, puis ajoutez les éléments de menu au menu contextuel qui représentent des opérations au niveau du nœud vous souhaitez rendre disponible au moment de l’exécution. Pour plus d'informations, voir [Procédure : Ajouter des éléments de Menu à un ContextMenuStrip](how-to-add-menu-items-to-a-contextmenustrip.md).  
  
3. Rouvrez le **TreeNode** boîte de dialogue pour le <xref:System.Windows.Forms.TreeView> contrôler, sélectionnez le nœud pour modifier et définir son <xref:System.Windows.Forms.ContextMenuStrip> propriété au menu contextuel que vous avez ajouté.  
  
4. Lorsque cette propriété est définie, le menu contextuel s’affichera lorsque vous cliquez sur le nœud.  
  
     En outre, vous devez écrire du code pour gérer le <xref:System.Windows.Forms.ToolStripItem.Click> événements pour ces éléments de menu.  
  
## <a name="see-also"></a>Voir aussi

- [TreeView, contrôle](treeview-control-windows-forms.md)
- [Vue d’ensemble du contrôle TreeView](treeview-control-overview-windows-forms.md)
- [ContextMenuStrip, contrôle](contextmenustrip-control.md)
