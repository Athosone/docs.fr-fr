---
title: 'Procédure : redimensionner par programmation des cellules pour les adapter au contenu du contrôle DataGridView Windows Forms'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
- cpp
helpviewer_keywords:
- data grids [Windows Forms], resizing cells to fit content
- cells [Windows Forms], resizing to fit contents
- DataGridView control [Windows Forms], resizing cells
- grids [Windows Forms], resizing cells to fit content
ms.assetid: 63d770dc-b3f5-462b-901a-3125b2753792
ms.openlocfilehash: e8240d1d5ac9784bd33d65e4c79c3d5ac7595657
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62012540"
---
# <a name="how-to-programmatically-resize-cells-to-fit-content-in-the-windows-forms-datagridview-control"></a>Procédure : redimensionner par programmation des cellules pour les adapter au contenu du contrôle DataGridView Windows Forms
Vous pouvez utiliser les méthodes du contrôle <xref:System.Windows.Forms.DataGridView> pour redimensionner des lignes, des colonnes et des en-têtes pour qu'ils affichent leurs valeurs entières sans coupure. Vous pouvez utiliser ces méthodes pour redimensionner des éléments <xref:System.Windows.Forms.DataGridView> quand bon vous semble. En guise d'alternative, vous pouvez configurer le contrôle pour redimensionner automatiquement ces éléments chaque fois que le contenu est modifié. Toutefois, cette opération peut être inefficace quand vous travaillez avec grands jeux de données ou quand vos données changent fréquemment. Pour plus d’informations, consultez [les Options de dimensionnement dans le contrôle de DataGridView Windows Forms](sizing-options-in-the-windows-forms-datagridview-control.md).  
  
 En général, vous ajustez par programmation les éléments <xref:System.Windows.Forms.DataGridView> en fonction de leur contenu uniquement quand vous chargez de nouvelles données à partir d'une source de données ou quand l'utilisateur a modifié une valeur. Cela est utile pour optimiser les performances, mais aussi quand vous souhaitez permettre aux utilisateurs de redimensionner manuellement des lignes et des colonnes avec la souris.  
  
 L'exemple de code suivant illustre les options disponibles pour le redimensionnement par programmation.  
  
## <a name="example"></a>Exemple  
 [!code-cpp[System.Windows.Forms.DataGridView.ProgrammaticResizing#0](~/samples/snippets/cpp/VS_Snippets_Winforms/System.Windows.Forms.DataGridView.ProgrammaticResizing/CPP/programmaticsizing.cpp#0)]
 [!code-csharp[System.Windows.Forms.DataGridView.ProgrammaticResizing#0](~/samples/snippets/csharp/VS_Snippets_Winforms/System.Windows.Forms.DataGridView.ProgrammaticResizing/CS/programmaticsizing.cs#0)]
 [!code-vb[System.Windows.Forms.DataGridView.ProgrammaticResizing#0](~/samples/snippets/visualbasic/VS_Snippets_Winforms/System.Windows.Forms.DataGridView.ProgrammaticResizing/VB/programmaticsizing.vb#0)]  
  
## <a name="compiling-the-code"></a>Compilation du code  
 Cet exemple nécessite :  
  
- Références aux assemblys System, System.Drawing et System.Windows.Forms.  
  
 Pour plus d’informations sur la création de cet exemple à partir de la ligne de commande pour Visual Basic ou Visual c#, consultez [génération à partir de la ligne de commande](../../../visual-basic/reference/command-line-compiler/building-from-the-command-line.md) ou [de ligne de commande avec csc.exe](../../../csharp/language-reference/compiler-options/command-line-building-with-csc-exe.md). Vous pouvez également créer cet exemple dans Visual Studio en collant le code dans un nouveau projet.  
  
## <a name="see-also"></a>Voir aussi

- <xref:System.Windows.Forms.DataGridView>
- <xref:System.Windows.Forms.DataGridView.AutoResizeColumn%2A?displayProperty=nameWithType>
- <xref:System.Windows.Forms.DataGridView.AutoResizeColumns%2A?displayProperty=nameWithType>
- <xref:System.Windows.Forms.DataGridView.AutoResizeColumnHeadersHeight%2A?displayProperty=nameWithType>
- <xref:System.Windows.Forms.DataGridView.AutoResizeRow%2A?displayProperty=nameWithType>
- <xref:System.Windows.Forms.DataGridView.AutoResizeRows%2A?displayProperty=nameWithType>
- <xref:System.Windows.Forms.DataGridView.AutoResizeRowHeadersWidth%2A?displayProperty=nameWithType>
- <xref:System.Windows.Forms.DataGridViewAutoSizeRowMode>
- <xref:System.Windows.Forms.DataGridViewAutoSizeRowsMode>
- <xref:System.Windows.Forms.DataGridViewAutoSizeColumnMode>
- <xref:System.Windows.Forms.DataGridViewAutoSizeColumnsMode>
- <xref:System.Windows.Forms.DataGridViewColumnHeadersHeightSizeMode>
- <xref:System.Windows.Forms.DataGridViewRowHeadersWidthSizeMode>
- [Redimensionnement des colonnes et des lignes dans le contrôle DataGridView Windows Forms](resizing-columns-and-rows-in-the-windows-forms-datagridview-control.md)
- [Options de dimensionnement dans le contrôle DataGridView Windows Forms](sizing-options-in-the-windows-forms-datagridview-control.md)
- [Guide pratique pour Redimensionner automatiquement des cellules lorsque le contenu change dans le contrôle de DataGridView Windows Forms](automatically-resize-cells-when-content-changes-in-the-datagrid.md)
