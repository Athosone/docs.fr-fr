---
title: 'Procédure : déplacer des ToolStripMenuItems'
ms.date: 03/30/2017
helpviewer_keywords:
- ToolStripMenuItems [Windows Forms], moving
- menus [Windows Forms], arranging items
- ToolStripMenuItems [Windows Forms], dragging and dropping
- menu items [Windows Forms], moving
- menu items [Windows Forms], cutting and pasting
- menu items [Windows Forms], dragging and dropping
- MenuStrip control [Windows Forms], arranging items
- ToolStripMenuItems [Windows Forms], cutting and pasting
ms.assetid: cab9e03e-4edd-4c25-b3e3-bd1edc602bd9
ms.openlocfilehash: 2203511e91254c270c59b5d298dd87a5b3737109
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59308353"
---
# <a name="how-to-move-toolstripmenuitems"></a>Procédure : déplacer des ToolStripMenuItems
Au moment du design, vous pouvez déplacer l’intégralité de menus de niveau supérieur et leurs éléments de menu à un autre emplacement le <xref:System.Windows.Forms.MenuStrip>. Vous pouvez également déplacer des éléments de menu individuels entre des menus de niveau supérieur ou modifier la position des éléments de menu dans un menu.  
  
> [!NOTE]
>  Les boîtes de dialogue et les commandes de menu qui s'affichent peuvent être différentes de celles qui sont décrites dans l'aide, en fonction de vos paramètres actifs ou de l'édition utilisée. Pour modifier vos paramètres, choisissez **Importation et exportation de paramètres** dans le menu **Outils** . Pour plus d’informations, consultez [Personnaliser l’IDE Visual Studio](/visualstudio/ide/personalizing-the-visual-studio-ide).  
  
### <a name="to-move-a-top-level-menu-and-its-menu-items-to-another-top-level-location"></a>Pour déplacer un menu de niveau supérieur et ses éléments de menu à un autre emplacement de niveau supérieur  
  
1. Cliquez et maintenez le bouton gauche de la souris sur le menu que vous souhaitez déplacer.  
  
2. Faites glisser le point d’insertion dans le menu de niveau supérieur qui se trouve avant le nouvel emplacement prévu et relâchez le bouton gauche de la souris.  
  
     Le menu sélectionné se déplace vers la droite du point d’insertion.  
  
### <a name="to-move-a-top-level-menu-and-its-menu-items-to-a-drop-down-location"></a>Pour déplacer un menu de niveau supérieur et ses éléments de menu à un emplacement de la liste déroulante  
  
1. Cliquez sur le menu que vous souhaitez déplacer et appuyez sur CTRL + X, ou le menu contextuel et sélectionnez **couper** dans le menu contextuel.  
  
2. Dans le menu de niveau supérieur de destination, cliquez sur l’élément de menu au-dessus du nouvel emplacement prévu et appuyez sur CTRL + V, ou cliquez sur l’élément de menu au-dessus du nouvel emplacement prévu et sélectionnez **coller** dans le menu contextuel.  
  
     Le menu que vous coupez est inséré après l’élément de menu sélectionné.  
  
### <a name="to-move-a-menu-item-within-a-menu-using-the-items-collection-editor"></a>Pour déplacer un élément de menu dans un menu à l’aide de l’éditeur de collections Items  
  
1. Cliquez sur le menu qui contient l’élément de menu que vous souhaitez déplacer.  
  
2. Dans le menu contextuel, choisissez **modifier les DropDownItems**.  
  
3. Dans le **éditeur de collections Items**, cliquez sur l’élément de menu que vous souhaitez déplacer.  
  
4. Cliquez sur les touches de direction haut et bas pour déplacer l’élément de menu dans le menu.  
  
5. Cliquez sur **OK**.  
  
### <a name="to-move-a-menu-item-within-a-menu-using-the-keyboard"></a>Pour déplacer un élément de menu dans un menu à l’aide du clavier  
  
1. Maintenez la touche ALT enfoncée.  
  
2. Cliquez et maintenez le bouton gauche de la souris sur l’élément de menu que vous souhaitez déplacer.  
  
3. Faites glisser l’élément de menu vers le nouvel emplacement et relâchez le bouton gauche de la souris.  
  
### <a name="to-move-a-menu-item-to-another-menu"></a>Pour déplacer un élément de menu vers un autre menu  
  
1. Cliquez sur l’élément de menu que vous souhaitez déplacer et appuyez sur CTRL + X, ou l’élément de menu, sélectionnez **couper** dans le menu contextuel.  
  
2. Cliquez sur le menu qui contiendra l’élément de menu que vous coupez.  
  
3. Cliquez sur l’élément de menu qui se trouve avant le nouvel emplacement prévu et appuyez sur CTRL + V ou cliquez sur l’élément de menu qui se trouve avant le nouvel emplacement prévu et sélectionnez **coller** dans le menu contextuel.  
  
     L’élément de menu que vous coupez est inséré après l’élément de menu sélectionné.  
  
## <a name="see-also"></a>Voir aussi

- <xref:System.Windows.Forms.MenuStrip>
- <xref:System.Windows.Forms.ToolStripMenuItem>
- [Vue d'ensemble du contrôle MenuStrip](menustrip-control-overview-windows-forms.md)
