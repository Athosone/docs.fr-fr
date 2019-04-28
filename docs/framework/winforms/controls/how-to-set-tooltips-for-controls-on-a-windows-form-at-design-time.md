---
title: 'Procédure : définir des info-bulles pour des contrôles dans un formulaire Windows au moment du design'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
- cpp
helpviewer_keywords:
- tooltips [Windows Forms], for controls
- examples [Windows Forms], tooltips
ms.assetid: c4b60637-4c0a-44c2-a103-f66dff887936
ms.openlocfilehash: cc8f8c620516a943d6d70187e19b72f5a2a99888
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62013073"
---
# <a name="how-to-set-tooltips-for-controls-on-a-windows-form-at-design-time"></a>Procédure : définir des info-bulles pour des contrôles dans un formulaire Windows au moment du design
Vous pouvez définir un <xref:System.Windows.Forms.ToolTip> chaîne dans le code ou dans le Concepteur de formulaires Windows. Pour plus d’informations sur la <xref:System.Windows.Forms.ToolTip> composant, consultez [vue d’ensemble du composant ToolTip](tooltip-component-overview-windows-forms.md).  
  
> [!NOTE]
>  Les boîtes de dialogue et les commandes de menu qui s'affichent peuvent être différentes de celles qui sont décrites dans l'aide, en fonction de vos paramètres actifs ou de l'édition utilisée. Pour modifier vos paramètres, choisissez **Importation et exportation de paramètres** dans le menu **Outils** . Pour plus d’informations, consultez [Personnaliser l’IDE Visual Studio](/visualstudio/ide/personalizing-the-visual-studio-ide).  
  
### <a name="to-set-a-tooltip-programmatically"></a>Pour définir une info-bulle par programmation  
  
1. Ajoutez le contrôle qui affiche l’info-bulle.  
  
2. Utilisez le <xref:System.Windows.Forms.ToolTip.SetToolTip%2A> méthode de la <xref:System.Windows.Forms.ToolTip> composant.  
  
    ```vb  
    ' In this example, Button1 is the control to display the ToolTip.  
    ToolTip1.SetToolTip(Button1, "Save changes")  
    ```  
  
    ```csharp  
    // In this example, button1 is the control to display the ToolTip.  
    toolTip1.SetToolTip(button1, "Save changes");  
    ```  
  
    ```cpp  
    // In this example, button1 is the control to display the ToolTip.  
    toolTip1->SetToolTip(button1, "Save changes");  
    ```  
  
### <a name="to-set-a-tooltip-in-the-designer"></a>Pour définir une info-bulle dans le Concepteur  
  
1. Ajoutez un composant <xref:System.Windows.Forms.ToolTip> au formulaire.  
  
2. Sélectionnez le contrôle qui affiche l’info-bulle, ou ajoutez-le au formulaire.  
  
3. Dans le **propriétés** fenêtre, définissez la **info-bulle sur ToolTip1** valeur à une chaîne de texte appropriée.  

### <a name="to-remove-a-tooltip-programmatically"></a>Pour supprimer une info-bulle par programme  
  
1. Utilisez le <xref:System.Windows.Forms.ToolTip.SetToolTip%2A> méthode de la <xref:System.Windows.Forms.ToolTip> composant.  
  
    ```vb  
    ' In this example, Button1 is the control displaying the ToolTip.  
    ToolTip1.SetToolTip(Button1, Nothing)  
    ```  
  
    ```csharp  
    // In this example, button1 is the control displaying the ToolTip.  
    toolTip1.SetToolTip(button1, null);  
    ```  
  
    ```cpp  
    // In this example, button1 is the control displaying the ToolTip.  
    toolTip1->SetToolTip(button1, NULL);  
    ```  
  
### <a name="to-remove-a-tooltip-in-the-designer"></a>Pour supprimer une info-bulle dans le Concepteur  
  
1. Sélectionnez le contrôle qui affiche l’info-bulle.  
  
2. Dans le **propriétés** fenêtre, supprimez le texte dans le **info-bulle sur ToolTip1**.  

## <a name="see-also"></a>Voir aussi

- [Vue d’ensemble du composant ToolTip](tooltip-component-overview-windows-forms.md)
- [Guide pratique pour Modifier la durée avant affichage du composant ToolTip Windows Forms](how-to-change-the-delay-of-the-windows-forms-tooltip-component.md)
- [ToolTip, composant](tooltip-component-windows-forms.md)
