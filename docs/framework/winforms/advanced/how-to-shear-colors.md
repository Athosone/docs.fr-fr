---
title: 'Procédure : incliner des couleurs'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- colors [Windows Forms], transforming with color matrices
- colors [Windows Forms], shearing
ms.assetid: 0a424171-5b8b-45c4-afef-e9720a6c3e22
ms.openlocfilehash: bf645cf88c4905cd5cf47c2a6c7af088fa428c8a
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59076241"
---
# <a name="how-to-shear-colors"></a>Procédure : incliner des couleurs
L’inclinaison augmente ou diminue d’un composant de couleur d’un montant proportionnel à un autre composant de couleur. Par exemple, considérez la transformation où le composant rouge est augmenté par la moitié de la valeur du composant bleu. Sous une transformation de ce type, la couleur (0,2, 0,5, 1) deviendrait (0,7, 0,5, 1). Le nouveau composant rouge est 0,2 + (1/2)(1) = 0,7.  
  
## <a name="example"></a>Exemple  
 L’exemple suivant construit un <xref:System.Drawing.Image> objet à partir du fichier ColorBars4.bmp. Le code applique ensuite la transformation d’inclinaison décrite dans le paragraphe précédent à chaque pixel de l’image.  
  
 L’illustration suivante montre l’image d’origine sur la gauche et l’image inclinée sur la droite : 
  
 ![Deux des carrés avec rayures colorée côté à côte illustrant l’image d’origine et l’image inclinée.](./media/how-to-shear-colors/original-image-sheared-image.png)  
  
 Le tableau suivant répertorie les vecteurs de couleur pour les quatre barres avant et après la transformation d’inclinaison.  
  
|D'origine|Inclinée|  
|--------------|-------------|  
|(0, 0, 1, 1)|(0.5, 0, 1, 1)|  
|(0.5, 1, 0.5, 1)|(0.75, 1, 0.5, 1)|  
|(1, 1, 0, 1)|(1, 1, 0, 1)|  
|(0.4, 0.4, 0.4, 1)|(0.6, 0.4, 0.4, 1)|  
  
 [!code-csharp[System.Drawing.Misc3#9](~/samples/snippets/csharp/VS_Snippets_Winforms/System.Drawing.Misc3/CS/Form1.cs#9)]
 [!code-vb[System.Drawing.Misc3#9](~/samples/snippets/visualbasic/VS_Snippets_Winforms/System.Drawing.Misc3/VB/Form1.vb#9)]  
  
## <a name="compiling-the-code"></a>Compilation du code  
 L'exemple précédent est conçu pour une utilisation avec Windows Forms et nécessite <xref:System.Windows.Forms.PaintEventArgs>`e`, qui est un paramètre du gestionnaire d'événements <xref:System.Windows.Forms.Control.Paint>. Remplacez `ColorBars.bmp` avec un nom de l’image et le chemin d’accès valide sur votre système.  
  
## <a name="see-also"></a>Voir aussi

- <xref:System.Drawing.Imaging.ColorMatrix>
- <xref:System.Drawing.Imaging.ImageAttributes>
- [Graphiques et dessins dans Windows Forms](graphics-and-drawing-in-windows-forms.md)
- [Recoloriage des images](recoloring-images.md)
