---
title: 'Procédure : aligner du texte dessiné'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- text [Windows Forms], aligning
- Windows Forms, aligning drawn text
ms.assetid: 83c10a81-1a90-4b5c-98aa-2c6c4b280079
ms.openlocfilehash: 0e77e4d8eeb9d7a07115b89525ac80074afeb6e8
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61937811"
---
# <a name="how-to-align-drawn-text"></a><span data-ttu-id="92bce-102">Procédure : aligner du texte dessiné</span><span class="sxs-lookup"><span data-stu-id="92bce-102">How to: Align Drawn Text</span></span>
<span data-ttu-id="92bce-103">Lorsque vous effectuez un dessin personnalisé, vous souhaiterez souvent centrer le texte dessiné sur un formulaire ou contrôle.</span><span class="sxs-lookup"><span data-stu-id="92bce-103">When you perform custom drawing, you may often want to center drawn text on a form or control.</span></span> <span data-ttu-id="92bce-104">Vous pouvez facilement aligner le texte dessiné avec la <xref:System.Drawing.Graphics.DrawString%2A> ou <xref:System.Windows.Forms.TextRenderer.DrawText%2A> méthodes en créant l’objet de mise en forme correcte et en définissant les indicateurs de format approprié.</span><span class="sxs-lookup"><span data-stu-id="92bce-104">You can easily align text drawn with the <xref:System.Drawing.Graphics.DrawString%2A> or <xref:System.Windows.Forms.TextRenderer.DrawText%2A> methods by creating the correct formatting object and setting the appropriate format flags.</span></span>  
  
### <a name="to-draw-centered-text-with-gdi-drawstring"></a><span data-ttu-id="92bce-105">Pour dessiner un texte centré avec GDI + (DrawString)</span><span class="sxs-lookup"><span data-stu-id="92bce-105">To draw centered text with GDI+ (DrawString)</span></span>  
  
1. <span data-ttu-id="92bce-106">Utilisez un <xref:System.Drawing.StringFormat> avec le bon <xref:System.Drawing.Graphics.DrawString%2A> méthode pour spécifier le texte centré.</span><span class="sxs-lookup"><span data-stu-id="92bce-106">Use a <xref:System.Drawing.StringFormat> with the appropriate <xref:System.Drawing.Graphics.DrawString%2A> method to specify centered text.</span></span>  
  
     [!code-csharp[System.Drawing.AlignDrawnText#10](~/samples/snippets/csharp/VS_Snippets_Winforms/System.Drawing.AlignDrawnText/CS/Form1.cs#10)]
     [!code-vb[System.Drawing.AlignDrawnText#10](~/samples/snippets/visualbasic/VS_Snippets_Winforms/System.Drawing.AlignDrawnText/VB/Form1.vb#10)]  
  
### <a name="to-draw-centered-text-with-gdi-drawtext"></a><span data-ttu-id="92bce-107">Pour dessiner un texte centré avec GDI (DrawText)</span><span class="sxs-lookup"><span data-stu-id="92bce-107">To draw centered text with GDI (DrawText)</span></span>  
  
1. <span data-ttu-id="92bce-108">Utilisez le <xref:System.Windows.Forms.TextFormatFlags> énumération pour habiller ainsi que centrer verticalement et horizontalement le texte avec le bon <xref:System.Windows.Forms.TextRenderer.DrawText%2A> (méthode).</span><span class="sxs-lookup"><span data-stu-id="92bce-108">Use the <xref:System.Windows.Forms.TextFormatFlags> enumeration for wrapping as well as vertically and horizontally centering text with the appropriate <xref:System.Windows.Forms.TextRenderer.DrawText%2A> method.</span></span>  
  
     [!code-csharp[System.Drawing.AlignDrawnText#20](~/samples/snippets/csharp/VS_Snippets_Winforms/System.Drawing.AlignDrawnText/CS/Form1.cs#20)]
     [!code-vb[System.Drawing.AlignDrawnText#20](~/samples/snippets/visualbasic/VS_Snippets_Winforms/System.Drawing.AlignDrawnText/VB/Form1.vb#20)]  
  
## <a name="compiling-the-code"></a><span data-ttu-id="92bce-109">Compilation du code</span><span class="sxs-lookup"><span data-stu-id="92bce-109">Compiling the Code</span></span>  
 <span data-ttu-id="92bce-110">Les exemples de code précédents sont conçus pour une utilisation avec Windows Forms, et ils nécessitent <xref:System.Windows.Forms.PaintEventArgs> `e`, qui est un paramètre de <xref:System.Windows.Forms.PaintEventHandler>.</span><span class="sxs-lookup"><span data-stu-id="92bce-110">The preceding code examples are designed for use with Windows Forms, and they require <xref:System.Windows.Forms.PaintEventArgs>`e`, which is a parameter of <xref:System.Windows.Forms.PaintEventHandler>.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="92bce-111">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="92bce-111">See also</span></span>

- [<span data-ttu-id="92bce-112">Guide pratique pour Dessiner du texte avec GDI</span><span class="sxs-lookup"><span data-stu-id="92bce-112">How to: Draw Text with GDI</span></span>](how-to-draw-text-with-gdi.md)
- [<span data-ttu-id="92bce-113">Utilisation de polices et de texte</span><span class="sxs-lookup"><span data-stu-id="92bce-113">Using Fonts and Text</span></span>](using-fonts-and-text.md)
- [<span data-ttu-id="92bce-114">Guide pratique pour Construire des familles de polices et des polices</span><span class="sxs-lookup"><span data-stu-id="92bce-114">How to: Construct Font Families and Fonts</span></span>](how-to-construct-font-families-and-fonts.md)
