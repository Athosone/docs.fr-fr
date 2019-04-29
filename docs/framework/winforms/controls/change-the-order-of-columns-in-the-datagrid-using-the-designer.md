---
title: 'Procédure : modifier l’ordre des colonnes dans le contrôle DataGridView Windows Forms à l’aide du concepteur'
ms.date: 03/30/2017
helpviewer_keywords:
- columns [Windows Forms], order of
- DataGridView control [Windows Forms], column order
- Windows Forms, columns
- data [Windows Forms], displaying
ms.assetid: 7fe52a98-75d6-448c-97a5-65ca2c568c1a
ms.openlocfilehash: cb8aeb30e12f7af18b475fd7707fa9d2ede6a299
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61939085"
---
# <a name="how-to-change-the-order-of-columns-in-the-windows-forms-datagridview-control-using-the-designer"></a><span data-ttu-id="4b89c-102">Procédure : modifier l’ordre des colonnes dans le contrôle DataGridView Windows Forms à l’aide du concepteur</span><span class="sxs-lookup"><span data-stu-id="4b89c-102">How to: Change the Order of Columns in the Windows Forms DataGridView Control Using the Designer</span></span>
<span data-ttu-id="4b89c-103">Lorsque vous liez un formulaire Windows <xref:System.Windows.Forms.DataGridView> contrôle à une source de données, l’ordre d’affichage des colonnes générées automatiquement est dicté par la source de données.</span><span class="sxs-lookup"><span data-stu-id="4b89c-103">When you bind a Windows Forms <xref:System.Windows.Forms.DataGridView> control to a data source, the display order of the automatically generated columns is dictated by the data source.</span></span> <span data-ttu-id="4b89c-104">Si cette commande n’est pas ce que vous préférez, vous pouvez modifier l’ordre des colonnes à l’aide du concepteur.</span><span class="sxs-lookup"><span data-stu-id="4b89c-104">If this order is not what you prefer, you can change the order of the columns using the designer.</span></span> <span data-ttu-id="4b89c-105">Vous pouvez également ajouter des colonnes indépendantes au contrôle et modifier leur ordre d’affichage.</span><span class="sxs-lookup"><span data-stu-id="4b89c-105">You may also want to add unbound columns to the control and change their display order.</span></span> <span data-ttu-id="4b89c-106">Pour plus d’informations sur la façon de modifier l’ordre des colonnes par programmation, consultez [Comment : Modifier l’ordre des colonnes dans le contrôle de DataGridView Windows Forms](how-to-change-the-order-of-columns-in-the-windows-forms-datagridview-control.md).</span><span class="sxs-lookup"><span data-stu-id="4b89c-106">For information about how to change the column order programmatically, see [How to: Change the Order of Columns in the Windows Forms DataGridView Control](how-to-change-the-order-of-columns-in-the-windows-forms-datagridview-control.md).</span></span>  
  
 <span data-ttu-id="4b89c-107">La procédure suivante nécessite un **Windows Application** projet avec un formulaire contenant un <xref:System.Windows.Forms.DataGridView> contrôle.</span><span class="sxs-lookup"><span data-stu-id="4b89c-107">The following procedure requires a **Windows Application** project with a form containing a <xref:System.Windows.Forms.DataGridView> control.</span></span> <span data-ttu-id="4b89c-108">Pour plus d’informations sur la configuration d’un tel projet, consultez [Comment : Créer un projet d’application Windows Forms](/visualstudio/ide/step-1-create-a-windows-forms-application-project) et [Comment : Ajouter des contrôles aux Windows Forms](how-to-add-controls-to-windows-forms.md).</span><span class="sxs-lookup"><span data-stu-id="4b89c-108">For information about setting up such a project, see [How to: Create a Windows Forms application project](/visualstudio/ide/step-1-create-a-windows-forms-application-project) and [How to: Add Controls to Windows Forms](how-to-add-controls-to-windows-forms.md).</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="4b89c-109">Les boîtes de dialogue et les commandes de menu qui s'affichent peuvent être différentes de celles qui sont décrites dans l'aide, en fonction de vos paramètres actifs ou de l'édition utilisée.</span><span class="sxs-lookup"><span data-stu-id="4b89c-109">The dialog boxes and menu commands you see might differ from those described in Help depending on your active settings or edition.</span></span> <span data-ttu-id="4b89c-110">Pour modifier vos paramètres, choisissez **Importation et exportation de paramètres** dans le menu **Outils** .</span><span class="sxs-lookup"><span data-stu-id="4b89c-110">To change your settings, choose **Import and Export Settings** on the **Tools** menu.</span></span> <span data-ttu-id="4b89c-111">Pour plus d’informations, consultez [personnaliser l’IDE de Visual Studio](/visualstudio/ide/personalizing-the-visual-studio-ide)</span><span class="sxs-lookup"><span data-stu-id="4b89c-111">For more information, see [Personalize the Visual Studio IDE](/visualstudio/ide/personalizing-the-visual-studio-ide)</span></span>  
  
### <a name="to-change-the-column-order-using-the-designer"></a><span data-ttu-id="4b89c-112">Pour modifier l’ordre des colonnes à l’aide du Concepteur</span><span class="sxs-lookup"><span data-stu-id="4b89c-112">To change the column order using the designer</span></span>  
  
1. <span data-ttu-id="4b89c-113">Cliquez sur le glyphe de balise active (![glyphe de balise active](./media/vs-winformsmttagglyph.gif "VS_WinFormSmtTagGlyph")) dans le coin supérieur droit de la <xref:System.Windows.Forms.DataGridView> contrôler, puis sélectionnez **modifier les colonnes**.</span><span class="sxs-lookup"><span data-stu-id="4b89c-113">Click the smart tag glyph (![Smart Tag Glyph](./media/vs-winformsmttagglyph.gif "VS_WinFormSmtTagGlyph")) on the upper-right corner of the <xref:System.Windows.Forms.DataGridView> control, and then select **Edit Columns**.</span></span>  
  
2. <span data-ttu-id="4b89c-114">Sélectionnez une colonne dans la **colonnes sélectionnées** liste.</span><span class="sxs-lookup"><span data-stu-id="4b89c-114">Select a column from the **Selected Columns** list.</span></span>  
  
3. <span data-ttu-id="4b89c-115">Cliquez sur le haut ou bas à droite de la **colonnes sélectionnées** liste jusqu'à ce que la colonne sélectionnée soit dans la position souhaitée.</span><span class="sxs-lookup"><span data-stu-id="4b89c-115">Click the up or down arrow to the right of the **Selected Columns** list until the selected column is in the position you want.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="4b89c-116">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="4b89c-116">See also</span></span>

- <xref:System.Windows.Forms.DataGridView>
- [<span data-ttu-id="4b89c-117">Guide pratique pour Ajouter et supprimer des colonnes dans le contrôle de DataGridView Windows Forms à l’aide du Concepteur</span><span class="sxs-lookup"><span data-stu-id="4b89c-117">How to: Add and Remove Columns in the Windows Forms DataGridView Control Using the Designer</span></span>](add-and-remove-columns-in-the-datagrid-using-the-designer.md)
- [<span data-ttu-id="4b89c-118">Guide pratique pour Créer un projet Application Windows Forms</span><span class="sxs-lookup"><span data-stu-id="4b89c-118">How to: Create a Windows Forms application project</span></span>](/visualstudio/ide/step-1-create-a-windows-forms-application-project)
- [<span data-ttu-id="4b89c-119">Guide pratique pour Ajouter des contrôles aux Windows Forms</span><span class="sxs-lookup"><span data-stu-id="4b89c-119">How to: Add Controls to Windows Forms</span></span>](how-to-add-controls-to-windows-forms.md)
