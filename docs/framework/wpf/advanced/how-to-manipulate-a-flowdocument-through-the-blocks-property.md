---
title: 'Procédure : Manipuler un FlowDocument avec la propriété Blocks'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- 'documents [WPF], manipulating FlowDocuments through Blocks property [WPF], , '
- ', '
ms.assetid: cbb7291e-3f1b-433e-9e16-f4d93ced14e8
ms.openlocfilehash: c307d85bf24e2d8a20226856181e0758758d40c0
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62051505"
---
# <a name="how-to-manipulate-a-flowdocument-through-the-blocks-property"></a><span data-ttu-id="ad9c0-102">Procédure : Manipuler un FlowDocument avec la propriété Blocks</span><span class="sxs-lookup"><span data-stu-id="ad9c0-102">How to: Manipulate a FlowDocument through the Blocks Property</span></span>
<span data-ttu-id="ad9c0-103">Ces exemples illustrent certaines des opérations plus courantes qui peuvent être effectuées sur un <xref:System.Windows.Documents.FlowDocument> via la <xref:System.Windows.Documents.FlowDocument.Blocks%2A> propriété.</span><span class="sxs-lookup"><span data-stu-id="ad9c0-103">These examples demonstrate some of the more common operations that can be performed on a <xref:System.Windows.Documents.FlowDocument> through the <xref:System.Windows.Documents.FlowDocument.Blocks%2A> property.</span></span>  
  
## <a name="example"></a><span data-ttu-id="ad9c0-104">Exemple</span><span class="sxs-lookup"><span data-stu-id="ad9c0-104">Example</span></span>  
 <span data-ttu-id="ad9c0-105">L’exemple suivant crée un nouveau <xref:System.Windows.Documents.FlowDocument> avant d’ajouter un nouveau <xref:System.Windows.Documents.Paragraph> élément à la <xref:System.Windows.Documents.FlowDocument>.</span><span class="sxs-lookup"><span data-stu-id="ad9c0-105">The following example creates a new <xref:System.Windows.Documents.FlowDocument> and then appends a new <xref:System.Windows.Documents.Paragraph> element to the <xref:System.Windows.Documents.FlowDocument>.</span></span>  
  
 [!code-csharp[FlowDocumentSnippets#_FlowDocumentBlocksAdd](~/samples/snippets/csharp/VS_Snippets_Wpf/FlowDocumentSnippets/CSharp/Window1.xaml.cs#_flowdocumentblocksadd)]
 [!code-vb[FlowDocumentSnippets#_FlowDocumentBlocksAdd](~/samples/snippets/visualbasic/VS_Snippets_Wpf/FlowDocumentSnippets/visualbasic/window1.xaml.vb#_flowdocumentblocksadd)]  
  
## <a name="example"></a><span data-ttu-id="ad9c0-106">Exemple</span><span class="sxs-lookup"><span data-stu-id="ad9c0-106">Example</span></span>  
 <span data-ttu-id="ad9c0-107">L’exemple suivant crée un nouveau <xref:System.Windows.Documents.Paragraph> élément et l’insère au début de la <xref:System.Windows.Documents.FlowDocument>.</span><span class="sxs-lookup"><span data-stu-id="ad9c0-107">The following example creates a new <xref:System.Windows.Documents.Paragraph> element and inserts it at the beginning of the <xref:System.Windows.Documents.FlowDocument>.</span></span>  
  
 [!code-csharp[FlowDocumentSnippets#_FlowDocumentBlocksInsert](~/samples/snippets/csharp/VS_Snippets_Wpf/FlowDocumentSnippets/CSharp/Window1.xaml.cs#_flowdocumentblocksinsert)]
 [!code-vb[FlowDocumentSnippets#_FlowDocumentBlocksInsert](~/samples/snippets/visualbasic/VS_Snippets_Wpf/FlowDocumentSnippets/visualbasic/window1.xaml.vb#_flowdocumentblocksinsert)]  
  
## <a name="example"></a><span data-ttu-id="ad9c0-108">Exemple</span><span class="sxs-lookup"><span data-stu-id="ad9c0-108">Example</span></span>  
 <span data-ttu-id="ad9c0-109">L’exemple suivant obtient le nombre de niveau supérieur <xref:System.Windows.Documents.Block> éléments contenus dans le <xref:System.Windows.Documents.FlowDocument>.</span><span class="sxs-lookup"><span data-stu-id="ad9c0-109">The following example gets the number of top-level <xref:System.Windows.Documents.Block> elements contained in the <xref:System.Windows.Documents.FlowDocument>.</span></span>  
  
 [!code-csharp[FlowDocumentSnippets#_FlowDocumentBlocksCount](~/samples/snippets/csharp/VS_Snippets_Wpf/FlowDocumentSnippets/CSharp/Window1.xaml.cs#_flowdocumentblockscount)]
 [!code-vb[FlowDocumentSnippets#_FlowDocumentBlocksCount](~/samples/snippets/visualbasic/VS_Snippets_Wpf/FlowDocumentSnippets/visualbasic/window1.xaml.vb#_flowdocumentblockscount)]  
  
## <a name="example"></a><span data-ttu-id="ad9c0-110">Exemple</span><span class="sxs-lookup"><span data-stu-id="ad9c0-110">Example</span></span>  
 <span data-ttu-id="ad9c0-111">L’exemple suivant supprime le dernier <xref:System.Windows.Documents.Block> élément dans le <xref:System.Windows.Documents.FlowDocument>.</span><span class="sxs-lookup"><span data-stu-id="ad9c0-111">The following example deletes the last <xref:System.Windows.Documents.Block> element in the <xref:System.Windows.Documents.FlowDocument>.</span></span>  
  
 [!code-csharp[FlowDocumentSnippets#_FlowDocumentBlocksRemoveLast](~/samples/snippets/csharp/VS_Snippets_Wpf/FlowDocumentSnippets/CSharp/Window1.xaml.cs#_flowdocumentblocksremovelast)]
 [!code-vb[FlowDocumentSnippets#_FlowDocumentBlocksRemoveLast](~/samples/snippets/visualbasic/VS_Snippets_Wpf/FlowDocumentSnippets/visualbasic/window1.xaml.vb#_flowdocumentblocksremovelast)]  
  
## <a name="example"></a><span data-ttu-id="ad9c0-112">Exemple</span><span class="sxs-lookup"><span data-stu-id="ad9c0-112">Example</span></span>  
 <span data-ttu-id="ad9c0-113">L’exemple suivant efface tout le contenu (<xref:System.Windows.Documents.Block> éléments) à partir de la <xref:System.Windows.Documents.FlowDocument>.</span><span class="sxs-lookup"><span data-stu-id="ad9c0-113">The following example clears all of the contents (<xref:System.Windows.Documents.Block> elements) from the <xref:System.Windows.Documents.FlowDocument>.</span></span>  
  
 [!code-csharp[FlowDocumentSnippets#_FlowDocumentBlocksClear](~/samples/snippets/csharp/VS_Snippets_Wpf/FlowDocumentSnippets/CSharp/Window1.xaml.cs#_flowdocumentblocksclear)]
 [!code-vb[FlowDocumentSnippets#_FlowDocumentBlocksClear](~/samples/snippets/visualbasic/VS_Snippets_Wpf/FlowDocumentSnippets/visualbasic/window1.xaml.vb#_flowdocumentblocksclear)]  
  
## <a name="see-also"></a><span data-ttu-id="ad9c0-114">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ad9c0-114">See also</span></span>

- [<span data-ttu-id="ad9c0-115">Manipuler les groupes de lignes d’un tableau avec la propriété RowGroups</span><span class="sxs-lookup"><span data-stu-id="ad9c0-115">Manipulate a Table's Row Groups through the RowGroups Property</span></span>](how-to-manipulate-table-row-groups-through-the-rowgroups-property.md)
- [<span data-ttu-id="ad9c0-116">Manipuler les colonnes d’un tableau avec la propriété Columns</span><span class="sxs-lookup"><span data-stu-id="ad9c0-116">Manipulate a Table's Columns through the Columns Property</span></span>](how-to-manipulate-table-columns-through-the-columns-property.md)
- [<span data-ttu-id="ad9c0-117">Manipuler les groupes de lignes d’un tableau avec la propriété RowGroups</span><span class="sxs-lookup"><span data-stu-id="ad9c0-117">Manipulate a Table's Row Groups through the RowGroups Property</span></span>](how-to-manipulate-table-row-groups-through-the-rowgroups-property.md)
