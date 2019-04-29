---
title: 'Procédure : modifier le type d’une colonne DataGridView Windows Forms à l’aide du concepteur'
ms.date: 03/30/2017
helpviewer_keywords:
- Windows Forms, columns
- columns [Windows Forms], types
- DataGridView control [Windows Forms], changing column type
- data [Windows Forms], displaying
ms.assetid: 7f994d45-600d-4190-a187-35803214b40c
ms.openlocfilehash: e87017f3698bc88a123d8a0ba0df5dbe2b7bbfd9
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61939020"
---
# <a name="how-to-change-the-type-of-a-windows-forms-datagridview-column-using-the-designer"></a><span data-ttu-id="179e4-102">Procédure : modifier le type d’une colonne DataGridView Windows Forms à l’aide du concepteur</span><span class="sxs-lookup"><span data-stu-id="179e4-102">How to: Change the Type of a Windows Forms DataGridView Column Using the Designer</span></span>
<span data-ttu-id="179e4-103">Parfois vous souhaitez modifier le type d’une colonne qui a déjà été ajouté à un formulaire Windows <xref:System.Windows.Forms.DataGridView> contrôle.</span><span class="sxs-lookup"><span data-stu-id="179e4-103">Sometimes you will want to change the type of a column that has already been added to a Windows Forms <xref:System.Windows.Forms.DataGridView> control.</span></span> <span data-ttu-id="179e4-104">Par exemple, vous souhaiterez modifier les types de certaines des colonnes qui sont générés automatiquement lorsque vous liez le contrôle à une source de données.</span><span class="sxs-lookup"><span data-stu-id="179e4-104">For example, you may want to modify the types of some of the columns that are generated automatically when you bind the control to a data source.</span></span> <span data-ttu-id="179e4-105">Cela est utile lorsque la table que vous affichez a des colonnes contenant des clés étrangères aux lignes dans une table associée.</span><span class="sxs-lookup"><span data-stu-id="179e4-105">This is useful when the table you display has columns containing foreign keys to rows in a related table.</span></span> <span data-ttu-id="179e4-106">Dans ce cas, vous souhaiterez remplacer les colonnes de zone de texte qui affichent ces clés étrangères avec des colonnes de zone de liste déroulante qui affichent des valeurs plus significatives à partir de la table associée.</span><span class="sxs-lookup"><span data-stu-id="179e4-106">In this case, you may want to replace the text box columns that display these foreign keys with combo box columns that display more meaningful values from the related table.</span></span>  
  
 <span data-ttu-id="179e4-107">La procédure suivante nécessite un **Windows Application** projet avec un formulaire contenant un <xref:System.Windows.Forms.DataGridView> contrôle.</span><span class="sxs-lookup"><span data-stu-id="179e4-107">The following procedure requires a **Windows Application** project with a form containing a <xref:System.Windows.Forms.DataGridView> control.</span></span> <span data-ttu-id="179e4-108">Pour plus d’informations sur la configuration d’un tel projet, consultez [Comment : Créer un projet d’application Windows Forms](/visualstudio/ide/step-1-create-a-windows-forms-application-project) et [Comment : Ajouter des contrôles aux Windows Forms](how-to-add-controls-to-windows-forms.md).</span><span class="sxs-lookup"><span data-stu-id="179e4-108">For information about setting up such a project, see [How to: Create a Windows Forms application project](/visualstudio/ide/step-1-create-a-windows-forms-application-project) and [How to: Add Controls to Windows Forms](how-to-add-controls-to-windows-forms.md).</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="179e4-109">Les boîtes de dialogue et les commandes de menu qui s'affichent peuvent être différentes de celles qui sont décrites dans l'aide, en fonction de vos paramètres actifs ou de l'édition utilisée.</span><span class="sxs-lookup"><span data-stu-id="179e4-109">The dialog boxes and menu commands you see might differ from those described in Help depending on your active settings or edition.</span></span> <span data-ttu-id="179e4-110">Pour modifier vos paramètres, choisissez **Importation et exportation de paramètres** dans le menu **Outils** .</span><span class="sxs-lookup"><span data-stu-id="179e4-110">To change your settings, choose **Import and Export Settings** on the **Tools** menu.</span></span> <span data-ttu-id="179e4-111">Pour plus d’informations, consultez [Personnaliser l’IDE Visual Studio](/visualstudio/ide/personalizing-the-visual-studio-ide).</span><span class="sxs-lookup"><span data-stu-id="179e4-111">For more information, see [Personalize the Visual Studio IDE](/visualstudio/ide/personalizing-the-visual-studio-ide).</span></span>  
  
### <a name="to-change-the-type-of-a-column-using-the-designer"></a><span data-ttu-id="179e4-112">Pour modifier le type d’une colonne à l’aide du Concepteur</span><span class="sxs-lookup"><span data-stu-id="179e4-112">To change the type of a column using the designer</span></span>  
  
1. <span data-ttu-id="179e4-113">Cliquez sur le glyphe de balise active (![glyphe de balise active](./media/vs-winformsmttagglyph.gif "VS_WinFormSmtTagGlyph")) dans le coin supérieur droit de la <xref:System.Windows.Forms.DataGridView> contrôler, puis sélectionnez **modifier les colonnes**.</span><span class="sxs-lookup"><span data-stu-id="179e4-113">Click the smart tag glyph (![Smart Tag Glyph](./media/vs-winformsmttagglyph.gif "VS_WinFormSmtTagGlyph")) on the upper-right corner of the <xref:System.Windows.Forms.DataGridView> control, and then select **Edit Columns**.</span></span>  
  
2. <span data-ttu-id="179e4-114">Sélectionnez une colonne dans la **colonnes sélectionnées** liste.</span><span class="sxs-lookup"><span data-stu-id="179e4-114">Select a column from the **Selected Columns** list.</span></span>  
  
3. <span data-ttu-id="179e4-115">Dans le **propriétés de la colonne** grille, définissez la `ColumnType` propriété vers le nouveau type de colonne.</span><span class="sxs-lookup"><span data-stu-id="179e4-115">In the **Column Properties** grid, set the `ColumnType` property to the new column type.</span></span>  
  
    > [!NOTE]
    >  <span data-ttu-id="179e4-116">Le `ColumnType` propriété est une propriété de conception uniquement au moment qui indique la classe qui représente le type de colonne.</span><span class="sxs-lookup"><span data-stu-id="179e4-116">The `ColumnType` property is a design-time-only property that indicates the class representing the column type.</span></span> <span data-ttu-id="179e4-117">Il n’est pas une propriété réelle définie dans une classe de la colonne.</span><span class="sxs-lookup"><span data-stu-id="179e4-117">It is not an actual property defined in a column class.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="179e4-118">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="179e4-118">See also</span></span>

- <xref:System.Windows.Forms.DataGridView>
- <xref:System.Windows.Forms.DataGridViewColumn>
- [<span data-ttu-id="179e4-119">Guide pratique pour Créer un projet Application Windows Forms</span><span class="sxs-lookup"><span data-stu-id="179e4-119">How to: Create a Windows Forms application project</span></span>](/visualstudio/ide/step-1-create-a-windows-forms-application-project)
- [<span data-ttu-id="179e4-120">Guide pratique pour Ajouter des contrôles aux Windows Forms</span><span class="sxs-lookup"><span data-stu-id="179e4-120">How to: Add Controls to Windows Forms</span></span>](how-to-add-controls-to-windows-forms.md)
