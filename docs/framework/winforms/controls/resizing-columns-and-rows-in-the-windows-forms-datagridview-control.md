---
title: Redimensionnement des colonnes et des lignes dans le contrôle DataGridView Windows Forms
ms.date: 03/30/2017
helpviewer_keywords:
- DataGridView control [Windows Forms], sizing rows and columns
- columns [Windows Forms], resizing in grids
- data grids [Windows Forms], resizing columns and rows
ms.assetid: 7532764d-e5c1-4943-a08b-6377a722d3b6
ms.openlocfilehash: e1fa2d57cfb2cd374d691fe03a0e0bdbd3ad7141
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61903186"
---
# <a name="resizing-columns-and-rows-in-the-windows-forms-datagridview-control"></a><span data-ttu-id="8ea9c-102">Redimensionnement des colonnes et des lignes dans le contrôle DataGridView Windows Forms</span><span class="sxs-lookup"><span data-stu-id="8ea9c-102">Resizing Columns and Rows in the Windows Forms DataGridView Control</span></span>
<span data-ttu-id="8ea9c-103">Le `DataGridView` contrôle fournit de nombreuses options permettant de personnaliser le comportement de dimensionnement de ses colonnes et de lignes.</span><span class="sxs-lookup"><span data-stu-id="8ea9c-103">The `DataGridView` control provides numerous options for customizing the sizing behavior of its columns and rows.</span></span> <span data-ttu-id="8ea9c-104">En règle générale, `DataGridView` cellules ne se redimensionnent pas en fonction de leur contenu.</span><span class="sxs-lookup"><span data-stu-id="8ea9c-104">Typically, `DataGridView` cells do not resize based on their contents.</span></span> <span data-ttu-id="8ea9c-105">Au lieu de cela, elles tronquent toute valeur d’affichage qui est supérieure à la cellule.</span><span class="sxs-lookup"><span data-stu-id="8ea9c-105">Instead, they clip any display value that is larger than the cell.</span></span> <span data-ttu-id="8ea9c-106">Si le contenu peut être affiché sous forme de chaîne, la cellule l’affiche dans une info-bulle.</span><span class="sxs-lookup"><span data-stu-id="8ea9c-106">If the content can be displayed as a string, the cell displays it in a ToolTip.</span></span>  
  
 <span data-ttu-id="8ea9c-107">Par défaut, les utilisateurs peuvent faire glisser de ligne, colonne et les séparateurs d’en-têtes avec la souris pour afficher plus d’informations.</span><span class="sxs-lookup"><span data-stu-id="8ea9c-107">By default, users can drag row, column, and header dividers with the mouse to show more information.</span></span> <span data-ttu-id="8ea9c-108">Les utilisateurs peuvent également double-cliquer sur un séparateur pour redimensionner automatiquement la bande de ligne, colonne ou en-tête associée, en fonction de son contenu.</span><span class="sxs-lookup"><span data-stu-id="8ea9c-108">Users can also double-click a divider to automatically resize the associated row, column, or header band based on its contents.</span></span>  
  
 <span data-ttu-id="8ea9c-109">Le `DataGridView` contrôle fournit des propriétés, méthodes et événements qui vous permettent de personnaliser ou de désactiver tous ces comportements dirigé par l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="8ea9c-109">The `DataGridView` control provides properties, methods, and events that enable you to customize or disable all of these user-directed behaviors.</span></span> <span data-ttu-id="8ea9c-110">En outre, vous pouvez redimensionner par programme les lignes, colonnes et en-têtes en fonction de leur contenu, ou vous pouvez les configurer pour se redimensionnent automatiquement lorsque leur contenu change.</span><span class="sxs-lookup"><span data-stu-id="8ea9c-110">Additionally, you can programmatically resize rows, columns, and headers to fit their contents, or you can configure them to automatically resize themselves whenever their contents change.</span></span> <span data-ttu-id="8ea9c-111">Vous pouvez également configurer des colonnes pour diviser automatiquement la largeur disponible du contrôle dans des proportions que vous spécifiez.</span><span class="sxs-lookup"><span data-stu-id="8ea9c-111">You can also configure columns to automatically divide the available width of the control in proportions that you specify.</span></span>  
  
## <a name="in-this-section"></a><span data-ttu-id="8ea9c-112">Dans cette section</span><span class="sxs-lookup"><span data-stu-id="8ea9c-112">In This Section</span></span>  
 [<span data-ttu-id="8ea9c-113">Options de dimensionnement dans le contrôle DataGridView Windows Forms</span><span class="sxs-lookup"><span data-stu-id="8ea9c-113">Sizing Options in the Windows Forms DataGridView Control</span></span>](sizing-options-in-the-windows-forms-datagridview-control.md)  
 <span data-ttu-id="8ea9c-114">Décrit les options de dimensionnement de lignes, des colonnes et des en-têtes.</span><span class="sxs-lookup"><span data-stu-id="8ea9c-114">Describes the options for sizing rows, columns, and headers.</span></span> <span data-ttu-id="8ea9c-115">Également fournit des détails sur les méthodes et propriétés relatives au dimensionnement et décrit les scénarios d’utilisation courants.</span><span class="sxs-lookup"><span data-stu-id="8ea9c-115">Also provides details on sizing-related properties and methods, and describes common usage scenarios.</span></span>  
  
 [<span data-ttu-id="8ea9c-116">Mode Remplissage des colonnes dans le contrôle DataGridView Windows Forms</span><span class="sxs-lookup"><span data-stu-id="8ea9c-116">Column Fill Mode in the Windows Forms DataGridView Control</span></span>](column-fill-mode-in-the-windows-forms-datagridview-control.md)  
 <span data-ttu-id="8ea9c-117">Décrit le mode de remplissage de colonne en détail et fournit du code de démonstration qui vous permettent de faire des essais avec le mode de remplissage de colonne et les autres modes.</span><span class="sxs-lookup"><span data-stu-id="8ea9c-117">Describes column fill mode in detail, and provides demonstration code that you can use to experiment with column fill mode and other modes.</span></span>  
  
 [<span data-ttu-id="8ea9c-118">Guide pratique pour Définir les Modes de redimensionnement du contrôle DataGridView Windows Forms</span><span class="sxs-lookup"><span data-stu-id="8ea9c-118">How to: Set the Sizing Modes of the Windows Forms DataGridView Control</span></span>](how-to-set-the-sizing-modes-of-the-windows-forms-datagridview-control.md)  
 <span data-ttu-id="8ea9c-119">Décrit comment configurer les modes de dimensionnement pour des objectifs communs.</span><span class="sxs-lookup"><span data-stu-id="8ea9c-119">Describes how to configure the sizing modes for common purposes.</span></span>  
  
 [<span data-ttu-id="8ea9c-120">Guide pratique pour Redimensionner par programme les cellules en fonction du contenu dans le contrôle de DataGridView Windows Forms</span><span class="sxs-lookup"><span data-stu-id="8ea9c-120">How to: Programmatically Resize Cells to Fit Content in the Windows Forms DataGridView Control</span></span>](programmatically-resize-cells-to-fit-content-in-the-datagrid.md)  
 <span data-ttu-id="8ea9c-121">Fournit du code de démonstration que vous pouvez utiliser pour expérimenter le redimensionnement par programmation.</span><span class="sxs-lookup"><span data-stu-id="8ea9c-121">Provides demonstration code that you can use to experiment with programmatic resizing.</span></span>  
  
 [<span data-ttu-id="8ea9c-122">Guide pratique pour Redimensionner automatiquement des cellules lorsque le contenu change dans le contrôle de DataGridView Windows Forms</span><span class="sxs-lookup"><span data-stu-id="8ea9c-122">How to: Automatically Resize Cells When Content Changes in the Windows Forms DataGridView Control</span></span>](automatically-resize-cells-when-content-changes-in-the-datagrid.md)  
 <span data-ttu-id="8ea9c-123">Fournit du code de démonstration qui vous permettent de faire des essais avec les modes de dimensionnement automatique.</span><span class="sxs-lookup"><span data-stu-id="8ea9c-123">Provides demonstration code that you can use to experiment with automatic sizing modes.</span></span>  
  
## <a name="reference"></a><span data-ttu-id="8ea9c-124">Référence</span><span class="sxs-lookup"><span data-stu-id="8ea9c-124">Reference</span></span>  
 <xref:System.Windows.Forms.DataGridView>  
 <span data-ttu-id="8ea9c-125">Fournit une documentation de référence pour le contrôle <xref:System.Windows.Forms.DataGridView>.</span><span class="sxs-lookup"><span data-stu-id="8ea9c-125">Provides reference documentation for the <xref:System.Windows.Forms.DataGridView> control.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="8ea9c-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="8ea9c-126">See also</span></span>

- [<span data-ttu-id="8ea9c-127">DataGridView, contrôle</span><span class="sxs-lookup"><span data-stu-id="8ea9c-127">DataGridView Control</span></span>](datagridview-control-windows-forms.md)
