---
title: 'Procédure : mettre les colonnes en lecture seule dans le contrôle DataGridView Windows Forms à l’aide du concepteur'
ms.date: 03/30/2017
helpviewer_keywords:
- Windows Forms, columns
- DataGridView control [Windows Forms], read-only columns
- data [Windows Forms], displaying
- columns [Windows Forms], read-only
ms.assetid: b4ef7a75-ab33-4ee3-b2cf-201530e454e9
ms.openlocfilehash: a735b9bef9f9e3488941e05b2aa9444e6ecdc4b8
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59320078"
---
# <a name="how-to-make-columns-read-only-in-the-windows-forms-datagridview-control-using-the-designer"></a>Procédure : mettre les colonnes en lecture seule dans le contrôle DataGridView Windows Forms à l’aide du concepteur
Par défaut, les utilisateurs peuvent modifier des données texte et numériques affichées dans les formulaires Windows <xref:System.Windows.Forms.DataGridView> contrôle. Si vous souhaitez afficher les données qui ne sont pas conçues pour modification, vous devez vous les colonnes qui contiennent les données en lecture seule. Pour plus d’informations sur la façon de rendre le contrôle entièrement en lecture seule, consultez [Comment : Empêcher l’ajout de ligne et de suppression dans les Windows Forms DataGridView Control à l’aide du concepteur](prevent-row-addition-and-deletion-in-the-datagrid-using-the-designer.md).  
  
 La procédure suivante nécessite un **Windows Application** projet avec un formulaire contenant un <xref:System.Windows.Forms.DataGridView> contrôle. Pour plus d’informations sur la configuration d’un tel projet, consultez [Comment : Créer un projet d’application Windows Forms](/visualstudio/ide/step-1-create-a-windows-forms-application-project) et [Comment : Ajouter des contrôles aux Windows Forms](how-to-add-controls-to-windows-forms.md).  
  
> [!NOTE]
>  Les boîtes de dialogue et les commandes de menu qui s'affichent peuvent être différentes de celles qui sont décrites dans l'aide, en fonction de vos paramètres actifs ou de l'édition utilisée. Pour modifier vos paramètres, choisissez **Importation et exportation de paramètres** dans le menu **Outils** . Pour plus d’informations, consultez [Personnaliser l’IDE Visual Studio](/visualstudio/ide/personalizing-the-visual-studio-ide).  
  
### <a name="to-make-a-column-read-only-by-using-the-designer"></a>Pour définir une colonne en lecture seule à l’aide du Concepteur  
  
1. Cliquez sur le glyphe de balise active (![glyphe de balise active](./media/vs-winformsmttagglyph.gif "VS_WinFormSmtTagGlyph")) dans le coin supérieur droit de la <xref:System.Windows.Forms.DataGridView> contrôler, puis sélectionnez **modifier les colonnes**.  
  
2. Sélectionnez une colonne dans la **colonnes sélectionnées** liste.  
  
3. Dans le **propriétés de la colonne** grille, définissez la <xref:System.Windows.Forms.DataGridViewColumn.ReadOnly%2A> propriété `true`.  
  
    > [!NOTE]
    >  Vous pouvez également effectuer une colonne en lecture seule lorsque vous l’ajoutez en sélectionnant le **en lecture seule** case à cocher dans la **ajouter une colonne** boîte de dialogue.  
  
## <a name="see-also"></a>Voir aussi

- <xref:System.Windows.Forms.DataGridView>
- <xref:System.Windows.Forms.DataGridViewColumn.ReadOnly%2A?displayProperty=nameWithType>
- [Guide pratique pour Ajouter et supprimer des colonnes dans le contrôle de DataGridView Windows Forms à l’aide du Concepteur](add-and-remove-columns-in-the-datagrid-using-the-designer.md)
- [Guide pratique pour Empêcher l’ajout de ligne et la suppression dans le contrôle de DataGridView Windows Forms à l’aide du Concepteur](prevent-row-addition-and-deletion-in-the-datagrid-using-the-designer.md)
- [Guide pratique pour Créer un projet Application Windows Forms](/visualstudio/ide/step-1-create-a-windows-forms-application-project)
- [Guide pratique pour Ajouter des contrôles aux Windows Forms](how-to-add-controls-to-windows-forms.md)
