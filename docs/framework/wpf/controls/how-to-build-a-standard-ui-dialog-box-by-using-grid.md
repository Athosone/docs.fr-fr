---
title: 'Procédure : Générer une boîte de dialogue d’interface utilisateur standard à l’aide d’une grille'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- dialog boxes [WPF], creating
- Grid control [WPF], creating [WPF], dialog box
ms.assetid: d6ac3d51-844b-4d29-96d8-81a696a7b960
ms.openlocfilehash: 0ade908e92e552017acb9ba242ccba2c28c3c995
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59149524"
---
# <a name="how-to-build-a-standard-ui-dialog-box-by-using-grid"></a><span data-ttu-id="60671-102">Procédure : Générer une boîte de dialogue d’interface utilisateur standard à l’aide d’une grille</span><span class="sxs-lookup"><span data-stu-id="60671-102">How to: Build a Standard UI Dialog Box by Using Grid</span></span>
<span data-ttu-id="60671-103">Cet exemple montre comment créer une norme [!INCLUDE[TLA#tla_ui](../../../../includes/tlasharptla-ui-md.md)] boîte de dialogue à l’aide de la <xref:System.Windows.Controls.Grid> élément.</span><span class="sxs-lookup"><span data-stu-id="60671-103">This example shows how to create a standard [!INCLUDE[TLA#tla_ui](../../../../includes/tlasharptla-ui-md.md)] dialog box by using the <xref:System.Windows.Controls.Grid> element.</span></span>  
  
## <a name="example"></a><span data-ttu-id="60671-104">Exemple</span><span class="sxs-lookup"><span data-stu-id="60671-104">Example</span></span>  
 <span data-ttu-id="60671-105">L’exemple suivant crée une boîte de dialogue similaire à la **exécuter** boîte de dialogue dans le [!INCLUDE[TLA#tla_mswin](../../../../includes/tlasharptla-mswin-md.md)] système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="60671-105">The following example creates a dialog box like the **Run** dialog box in the [!INCLUDE[TLA#tla_mswin](../../../../includes/tlasharptla-mswin-md.md)] operating system.</span></span>  
  
 <span data-ttu-id="60671-106">L’exemple crée un <xref:System.Windows.Controls.Grid> et utilise le <xref:System.Windows.Controls.ColumnDefinition> et <xref:System.Windows.Controls.RowDefinition> classes pour définir les cinq colonnes et quatre lignes.</span><span class="sxs-lookup"><span data-stu-id="60671-106">The example creates a <xref:System.Windows.Controls.Grid> and uses the <xref:System.Windows.Controls.ColumnDefinition> and <xref:System.Windows.Controls.RowDefinition> classes to define five columns and four rows.</span></span>  
  
 <span data-ttu-id="60671-107">L’exemple ajoute et positionne un <xref:System.Windows.Controls.Image>, `RunIcon.png`, pour représenter l’image qui se trouve dans la boîte de dialogue.</span><span class="sxs-lookup"><span data-stu-id="60671-107">The example then adds and positions an <xref:System.Windows.Controls.Image>, `RunIcon.png`, to represent the image that is found in the dialog box.</span></span> <span data-ttu-id="60671-108">L’image est placée dans la première colonne et ligne de la <xref:System.Windows.Controls.Grid> (le coin supérieur droit).</span><span class="sxs-lookup"><span data-stu-id="60671-108">The image is placed in the first column and row of the <xref:System.Windows.Controls.Grid> (the upper-left corner).</span></span>  
  
 <span data-ttu-id="60671-109">Ensuite, l’exemple ajoute un <xref:System.Windows.Controls.TextBlock> élément à la première colonne, qui couvre les colonnes restantes de la première ligne.</span><span class="sxs-lookup"><span data-stu-id="60671-109">Next, the example adds a <xref:System.Windows.Controls.TextBlock> element to the first column, which spans the remaining columns of the first row.</span></span> <span data-ttu-id="60671-110">Il ajoute un autre <xref:System.Windows.Controls.TextBlock> élément à la deuxième ligne dans la première colonne, pour représenter le **Open** zone de texte.</span><span class="sxs-lookup"><span data-stu-id="60671-110">It adds another <xref:System.Windows.Controls.TextBlock> element to the second row in the first column, to represent the **Open** text box.</span></span> <span data-ttu-id="60671-111">Un <xref:System.Windows.Controls.TextBlock> suit, ce qui représente la zone de saisie de données.</span><span class="sxs-lookup"><span data-stu-id="60671-111">A <xref:System.Windows.Controls.TextBlock> follows, which represents the data entry area.</span></span>  
  
 <span data-ttu-id="60671-112">Enfin, l’exemple ajoute trois <xref:System.Windows.Controls.Button> à la dernière ligne, les éléments qui représentent le **OK**, **Annuler**, et **Parcourir** événements.</span><span class="sxs-lookup"><span data-stu-id="60671-112">Finally, the example adds three <xref:System.Windows.Controls.Button> elements to the final row, which represent the **OK**, **Cancel**, and **Browse** events.</span></span>  
  
 [!code-csharp[GridRunDialog#1](~/samples/snippets/csharp/VS_Snippets_Wpf/GridRunDialog/CSharp/window1.xaml.cs#1)]
 [!code-vb[GridRunDialog#1](~/samples/snippets/visualbasic/VS_Snippets_Wpf/GridRunDialog/VisualBasic/grid_vb.vb#1)]  
  
## <a name="see-also"></a><span data-ttu-id="60671-113">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="60671-113">See also</span></span>

- <xref:System.Windows.Controls.Grid>
- <xref:System.Windows.GridUnitType>
- [<span data-ttu-id="60671-114">Vue d’ensemble de Panel</span><span class="sxs-lookup"><span data-stu-id="60671-114">Panels Overview</span></span>](panels-overview.md)
- [<span data-ttu-id="60671-115">Rubriques de guide pratique</span><span class="sxs-lookup"><span data-stu-id="60671-115">How-to Topics</span></span>](grid-how-to-topics.md)
