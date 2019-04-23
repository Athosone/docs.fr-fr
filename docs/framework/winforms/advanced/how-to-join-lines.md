---
title: 'Procédure : joindre des lignes'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- miter line join style
- bevel line join style
- line join
- drawing [Windows Forms], joining lines
- GraphicsPath object
- round line join style
- lines [Windows Forms], joining
- graphics [Windows Forms], joining lines
ms.assetid: 9fc480c2-3c75-4fd1-8ab5-296a99e820e2
ms.openlocfilehash: 445d7f12f57137c6b06a074eeaf0574eb027a723
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59174913"
---
# <a name="how-to-join-lines"></a>Procédure : joindre des lignes
Une jointure de la ligne est la zone commune qui est formée par deux lignes dont les extrémités se rencontrent ou se chevauchent. [!INCLUDE[ndptecgdiplus](../../../../includes/ndptecgdiplus-md.md)] fournit trois styles de jonction de ligne : angle aigu, en biseau et arrondie. Style de ligne de jointure est une propriété de la <xref:System.Drawing.Pen> classe. Lorsque vous spécifiez un style de jointure de ligne pour un <xref:System.Drawing.Pen> que jointure style sera appliqué à toutes les lignes connectées dans un objet <xref:System.Drawing.Drawing2D.GraphicsPath> objet dessiné à l’aide de ce stylet.  
  
 L’illustration suivante montre les résultats de l’exemple de jointure de ligne en relief.  
  
 ![Illustration des lignes jointes.](./media/how-to-join-lines/joined-beveled-lines.gif)  
  
## <a name="example"></a>Exemple  
 Vous pouvez spécifier le style de ligne de jointure à l’aide de la <xref:System.Drawing.Pen.LineJoin%2A> propriété de la <xref:System.Drawing.Pen> classe. L’exemple montre une jointure de lignes biseautée entre une ligne horizontale et une ligne verticale. Dans le code suivant, la valeur <xref:System.Drawing.Drawing2D.LineJoin.Bevel> affectée à la <xref:System.Drawing.Pen.LineJoin%2A> propriété est un membre de la <xref:System.Drawing.Drawing2D.LineJoin> énumération. Les autres membres de la <xref:System.Drawing.Drawing2D.LineJoin> énumération sont <xref:System.Drawing.Drawing2D.LineJoin.Miter> et <xref:System.Drawing.Drawing2D.LineJoin.Round>.  
  
 [!code-csharp[System.Drawing.UsingAPen#31](~/samples/snippets/csharp/VS_Snippets_Winforms/System.Drawing.UsingAPen/CS/Class1.cs#31)]
 [!code-vb[System.Drawing.UsingAPen#31](~/samples/snippets/visualbasic/VS_Snippets_Winforms/System.Drawing.UsingAPen/VB/Class1.vb#31)]  
  
## <a name="compiling-the-code"></a>Compilation du code  
 L’exemple précédent est conçu pour une utilisation avec Windows Forms et nécessite <xref:System.Windows.Forms.PaintEventArgs> `e`, qui est un paramètre de la <xref:System.Windows.Forms.Control.Paint> Gestionnaire d’événements.  
  
## <a name="see-also"></a>Voir aussi

- [Utilisation d'un stylet pour dessiner des lignes et des formes](using-a-pen-to-draw-lines-and-shapes.md)
