---
title: 'Procédure : masquer les en-têtes de colonne dans le contrôle DataGridView Windows Forms'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- columns [Windows Forms], hiding column headers
- column headers [Windows Forms], hiding
- DataGridView control [Windows Forms], column headers
ms.assetid: e4ad5f68-50d2-4b9e-93ee-9d622423a8ab
ms.openlocfilehash: 85332bfdbb80e4c49bab1ff208228a88337fbb43
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61941282"
---
# <a name="how-to-hide-column-headers-in-the-windows-forms-datagridview-control"></a><span data-ttu-id="38463-102">Procédure : masquer les en-têtes de colonne dans le contrôle DataGridView Windows Forms</span><span class="sxs-lookup"><span data-stu-id="38463-102">How to: Hide Column Headers in the Windows Forms DataGridView Control</span></span>
<span data-ttu-id="38463-103">Parfois, vous souhaitez afficher un <xref:System.Windows.Forms.DataGridView> sans en-têtes de colonne.</span><span class="sxs-lookup"><span data-stu-id="38463-103">Sometimes you will want to display a <xref:System.Windows.Forms.DataGridView> without column headers.</span></span> <span data-ttu-id="38463-104">Dans le <xref:System.Windows.Forms.DataGridView> contrôle, le <xref:System.Windows.Forms.DataGridView.ColumnHeadersVisible%2A> valeur de propriété détermine si les en-têtes de colonnes sont affichés.</span><span class="sxs-lookup"><span data-stu-id="38463-104">In the <xref:System.Windows.Forms.DataGridView> control, the <xref:System.Windows.Forms.DataGridView.ColumnHeadersVisible%2A> property value determines whether the column headers are displayed.</span></span>  
  
### <a name="to-hide-the-column-headers"></a><span data-ttu-id="38463-105">Pour masquer les en-têtes de colonnes</span><span class="sxs-lookup"><span data-stu-id="38463-105">To hide the column headers</span></span>  
  
- <span data-ttu-id="38463-106">Affectez à la propriété <xref:System.Windows.Forms.DataGridView.ColumnHeadersVisible%2A?displayProperty=nameWithType> la valeur `false`.</span><span class="sxs-lookup"><span data-stu-id="38463-106">Set the <xref:System.Windows.Forms.DataGridView.ColumnHeadersVisible%2A?displayProperty=nameWithType> property to `false`.</span></span>  
  
     [!code-csharp[System.Windows.Forms.DataGridViewMisc#062](~/samples/snippets/csharp/VS_Snippets_Winforms/System.Windows.Forms.DataGridViewMisc/CS/datagridviewmisc.cs#062)]
     [!code-vb[System.Windows.Forms.DataGridViewMisc#062](~/samples/snippets/visualbasic/VS_Snippets_Winforms/System.Windows.Forms.DataGridViewMisc/VB/datagridviewmisc.vb#062)]  
  
## <a name="compiling-the-code"></a><span data-ttu-id="38463-107">Compilation du code</span><span class="sxs-lookup"><span data-stu-id="38463-107">Compiling the Code</span></span>  
 <span data-ttu-id="38463-108">Cet exemple nécessite :</span><span class="sxs-lookup"><span data-stu-id="38463-108">This example requires:</span></span>  
  
- <span data-ttu-id="38463-109">un contrôle <xref:System.Windows.Forms.DataGridView> nommé `dataGridView1` ;</span><span class="sxs-lookup"><span data-stu-id="38463-109">A <xref:System.Windows.Forms.DataGridView> control named `dataGridView1`.</span></span>  
  
- <span data-ttu-id="38463-110">des références aux assemblys <xref:System?displayProperty=nameWithType> et <xref:System.Windows.Forms?displayProperty=nameWithType>.</span><span class="sxs-lookup"><span data-stu-id="38463-110">References to the <xref:System?displayProperty=nameWithType> and <xref:System.Windows.Forms?displayProperty=nameWithType> assemblies.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="38463-111">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="38463-111">See also</span></span>

- <xref:System.Windows.Forms.DataGridView>
- <xref:System.Windows.Forms.DataGridView.ColumnHeadersVisible%2A?displayProperty=nameWithType>
- [<span data-ttu-id="38463-112">Fonctionnalités de base liées aux colonnes, lignes et cellules dans le contrôle DataGridView Windows Forms</span><span class="sxs-lookup"><span data-stu-id="38463-112">Basic Column, Row, and Cell Features in the Windows Forms DataGridView Control</span></span>](basic-column-row-and-cell-features-wf-datagridview-control.md)
