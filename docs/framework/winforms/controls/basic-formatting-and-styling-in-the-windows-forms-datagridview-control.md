---
title: Mises en forme et styles de base dans le contrôle DataGridView Windows Forms
ms.date: 03/30/2017
helpviewer_keywords:
- DataGridView control [Windows Forms], formatting and styling
- data grids [Windows Forms], formatting
ms.assetid: b9b90836-1f56-4aa9-8db8-edc78fe830e8
ms.openlocfilehash: 5e967c1bbe54095cc11e48b014600158da7fe6a3
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62011682"
---
# <a name="basic-formatting-and-styling-in-the-windows-forms-datagridview-control"></a><span data-ttu-id="d5edb-102">Mises en forme et styles de base dans le contrôle DataGridView Windows Forms</span><span class="sxs-lookup"><span data-stu-id="d5edb-102">Basic Formatting and Styling in the Windows Forms DataGridView Control</span></span>
<span data-ttu-id="d5edb-103">Le `DataGridView` contrôle vous permet de définir l’apparence de base des cellules et le format d’affichage des valeurs de cellule.</span><span class="sxs-lookup"><span data-stu-id="d5edb-103">The `DataGridView` control makes it easy to define the basic appearance of cells and the display formatting of cell values.</span></span> <span data-ttu-id="d5edb-104">Vous pouvez définir d’apparence et de mise en forme de styles pour les cellules individuelles, pour les cellules des colonnes spécifiques et des lignes ou pour toutes les cellules dans le contrôle en définissant les propriétés de la `DataGridViewCellStyle` objets accédés par divers `DataGridView` propriétés du contrôle.</span><span class="sxs-lookup"><span data-stu-id="d5edb-104">You can define appearance and formatting styles for individual cells, for cells in specific columns and rows, or for all cells in the control by setting the properties of the `DataGridViewCellStyle` objects accessed through various `DataGridView` control properties.</span></span> <span data-ttu-id="d5edb-105">En outre, vous pouvez modifier ces styles dynamiquement en fonction de facteurs tels que la valeur de cellule en gérant le `CellFormatting` événement.</span><span class="sxs-lookup"><span data-stu-id="d5edb-105">Additionally, you can modify these styles dynamically based on factors such as the cell value by handling the `CellFormatting` event.</span></span>  
  
## <a name="in-this-section"></a><span data-ttu-id="d5edb-106">Dans cette section</span><span class="sxs-lookup"><span data-stu-id="d5edb-106">In This Section</span></span>  
 [<span data-ttu-id="d5edb-107">Guide pratique pour Modifier la bordure et les Styles de quadrillage dans le contrôle de DataGridView Windows Forms</span><span class="sxs-lookup"><span data-stu-id="d5edb-107">How to: Change the Border and Gridline Styles in the Windows Forms DataGridView Control</span></span>](change-the-border-and-gridline-styles-in-the-datagrid.md)  
 <span data-ttu-id="d5edb-108">Explique comment définir `DataGridView` propriétés qui définissent l’apparence de la bordure du contrôle et les lignes de la limite entre les cellules.</span><span class="sxs-lookup"><span data-stu-id="d5edb-108">Describes how to set `DataGridView` properties that define the appearance of the control border and the boundary lines between cells.</span></span>  
  
 [<span data-ttu-id="d5edb-109">Styles de cellules dans le contrôle DataGridView Windows Forms</span><span class="sxs-lookup"><span data-stu-id="d5edb-109">Cell Styles in the Windows Forms DataGridView Control</span></span>](cell-styles-in-the-windows-forms-datagridview-control.md)  
 <span data-ttu-id="d5edb-110">Décrit la `DataGridViewCellStyle` classe et la façon dont les propriétés de ce type interagissent pour définir l’affichent des cellules dans le contrôle.</span><span class="sxs-lookup"><span data-stu-id="d5edb-110">Describes the `DataGridViewCellStyle` class and how properties of that type interact to define how cells are displayed in the control.</span></span>  
  
 [<span data-ttu-id="d5edb-111">Guide pratique pour Définir des Styles de cellules par défaut pour le contrôle de DataGridView Windows Forms</span><span class="sxs-lookup"><span data-stu-id="d5edb-111">How to: Set Default Cell Styles for the Windows Forms DataGridView Control</span></span>](how-to-set-default-cell-styles-for-the-windows-forms-datagridview-control.md)  
 <span data-ttu-id="d5edb-112">Décrit comment utiliser `DataGridViewCellStyle` propriétés pour définir l’apparence par défaut des cellules dans des lignes et colonnes et dans l’ensemble du contrôle.</span><span class="sxs-lookup"><span data-stu-id="d5edb-112">Describes how to use `DataGridViewCellStyle` properties to define the default appearance of cells in specific rows and columns and in the entire control.</span></span>  
  
 [<span data-ttu-id="d5edb-113">Guide pratique pour Format des données dans les Windows Forms DataGridView Control</span><span class="sxs-lookup"><span data-stu-id="d5edb-113">How to: Format Data in the Windows Forms DataGridView Control</span></span>](how-to-format-data-in-the-windows-forms-datagridview-control.md)  
 <span data-ttu-id="d5edb-114">Décrit comment mettre en forme les valeurs d’affichage de cellule à l’aide de `DataGridViewCellStyle` propriétés.</span><span class="sxs-lookup"><span data-stu-id="d5edb-114">Describes how to format cell display values using `DataGridViewCellStyle` properties.</span></span>  
  
 [<span data-ttu-id="d5edb-115">Guide pratique pour Définir des Styles de police et couleur dans le contrôle DataGridView Windows Forms</span><span class="sxs-lookup"><span data-stu-id="d5edb-115">How to: Set Font and Color Styles in the Windows Forms DataGridView Control</span></span>](how-to-set-font-and-color-styles-in-the-windows-forms-datagridview-control.md)  
 <span data-ttu-id="d5edb-116">Décrit comment utiliser le `DefaultCellStyle` propriété à définir base afficher les caractéristiques pour toutes les cellules dans le contrôle.</span><span class="sxs-lookup"><span data-stu-id="d5edb-116">Describes how to use the `DefaultCellStyle` property to set basic display characteristics for all cells in the control.</span></span>  
  
 [<span data-ttu-id="d5edb-117">Guide pratique pour Définir les Styles de ligne en alternance pour le contrôle de DataGridView Windows Forms</span><span class="sxs-lookup"><span data-stu-id="d5edb-117">How to: Set Alternating Row Styles for the Windows Forms DataGridView Control</span></span>](how-to-set-alternating-row-styles-for-the-windows-forms-datagridview-control.md)  
 <span data-ttu-id="d5edb-118">Décrit comment créer un effet de livre dans le contrôle à l’aide de lignes en alternance qui sont affichent différemment.</span><span class="sxs-lookup"><span data-stu-id="d5edb-118">Describes how to create a ledger-like effect in the control using alternating rows that are displayed differently.</span></span>  
  
 [<span data-ttu-id="d5edb-119">Guide pratique pour Utiliser le modèle de ligne pour personnaliser les lignes dans le contrôle de DataGridView Windows Forms</span><span class="sxs-lookup"><span data-stu-id="d5edb-119">How to: Use the Row Template to Customize Rows in the Windows Forms DataGridView Control</span></span>](use-the-row-template-to-customize-rows-in-the-datagrid.md)  
 <span data-ttu-id="d5edb-120">Décrit comment utiliser le `RowTemplate` propriété pour définir les propriétés de ligne qui seront utilisées pour toutes les lignes dans le contrôle.</span><span class="sxs-lookup"><span data-stu-id="d5edb-120">Describes how to use the `RowTemplate` property to set row properties that will be used for all rows in the control.</span></span>  
  
## <a name="reference"></a><span data-ttu-id="d5edb-121">Référence</span><span class="sxs-lookup"><span data-stu-id="d5edb-121">Reference</span></span>  
 <xref:System.Windows.Forms.DataGridView>  
 <span data-ttu-id="d5edb-122">Fournit une documentation de référence pour le contrôle <xref:System.Windows.Forms.DataGridView>.</span><span class="sxs-lookup"><span data-stu-id="d5edb-122">Provides reference documentation for the <xref:System.Windows.Forms.DataGridView> control.</span></span>  
  
 <xref:System.Windows.Forms.DataGridViewCellStyle>  
 <span data-ttu-id="d5edb-123">Fournit la documentation de référence pour la <xref:System.Windows.Forms.DataGridViewCellStyle> classe.</span><span class="sxs-lookup"><span data-stu-id="d5edb-123">Provides reference documentation for the <xref:System.Windows.Forms.DataGridViewCellStyle> class.</span></span>  
  
 <xref:System.Windows.Forms.DataGridView.CellFormatting>  
 <span data-ttu-id="d5edb-124">Fournit la documentation de référence pour le <xref:System.Windows.Forms.DataGridView.CellFormatting> événement.</span><span class="sxs-lookup"><span data-stu-id="d5edb-124">Provides reference documentation for the <xref:System.Windows.Forms.DataGridView.CellFormatting> event.</span></span>  
  
 <xref:System.Windows.Forms.DataGridView.RowTemplate%2A>  
 <span data-ttu-id="d5edb-125">Fournit la documentation de référence pour le <xref:System.Windows.Forms.DataGridView.RowTemplate%2A> propriété.</span><span class="sxs-lookup"><span data-stu-id="d5edb-125">Provides reference documentation for the <xref:System.Windows.Forms.DataGridView.RowTemplate%2A> property.</span></span>  
  
## <a name="related-sections"></a><span data-ttu-id="d5edb-126">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="d5edb-126">Related Sections</span></span>  
 [<span data-ttu-id="d5edb-127">Personnalisation du contrôle DataGridView Windows Forms</span><span class="sxs-lookup"><span data-stu-id="d5edb-127">Customizing the Windows Forms DataGridView Control</span></span>](customizing-the-windows-forms-datagridview-control.md)  
 <span data-ttu-id="d5edb-128">Fournit des rubriques qui décrivent la peinture personnalisée des cellules et des lignes <xref:System.Windows.Forms.DataGridView> et la création de types de lignes, de colonnes et de cellules dérivés.</span><span class="sxs-lookup"><span data-stu-id="d5edb-128">Provides topics that describe custom painting <xref:System.Windows.Forms.DataGridView> cells and rows, and creating derived cell, column, and row types.</span></span>  
  
 [<span data-ttu-id="d5edb-129">Fonctionnalités de base liées aux colonnes, lignes et cellules dans le contrôle DataGridView Windows Forms</span><span class="sxs-lookup"><span data-stu-id="d5edb-129">Basic Column, Row, and Cell Features in the Windows Forms DataGridView Control</span></span>](basic-column-row-and-cell-features-wf-datagridview-control.md)  
 <span data-ttu-id="d5edb-130">Fournit des rubriques qui décrivent couramment utilisé des propriétés de cellule, ligne et colonne.</span><span class="sxs-lookup"><span data-stu-id="d5edb-130">Provides topics that describe commonly used cell, row, and column properties.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="d5edb-131">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d5edb-131">See also</span></span>

- [<span data-ttu-id="d5edb-132">DataGridView, contrôle</span><span class="sxs-lookup"><span data-stu-id="d5edb-132">DataGridView Control</span></span>](datagridview-control-windows-forms.md)
