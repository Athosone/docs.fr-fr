---
title: Restriction de la surface de dessin dans GDI+
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- GDI+, clipping
- clipping [Windows Forms], using GDI+
- GDI+, restricting drawing surface
ms.assetid: 8b5f71d9-d2f0-4540-9c41-740f90fd4c26
ms.openlocfilehash: d0508166f905b45789ce638b03d0747dd6fa904e
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59074958"
---
# <a name="restricting-the-drawing-surface-in-gdi"></a>Restriction de la surface de dessin dans GDI+
Le découpage consiste à restreindre le dessin à un rectangle ou une région. L’illustration suivante montre la chaîne « Hello » attachée à une région en forme de cœur.  
  
 ![Surface de dessin restreinte](./media/aboutgdip02-art30.gif "AboutGdip02_Art30")  
  
## <a name="clipping-with-regions"></a>Découpage avec des régions  
 Régions peuvent être construites à partir de chemins d’accès et les chemins peuvent contenir des contours des chaînes, vous pouvez donc utiliser texte avec contour pour le découpage. L’illustration suivante montre un ensemble de points de suspension concentriques découpé à l’intérieur d’une chaîne de texte.  
  
 ![Surface de dessin restreinte](./media/aboutgdip02-art31.gif "AboutGdip02_Art31")  
  
 Pour dessiner avec un découpage, créez un <xref:System.Drawing.Graphics> de l’objet, définissez son <xref:System.Drawing.Graphics.Clip%2A> propriété, puis appelez les méthodes de dessin de même <xref:System.Drawing.Graphics> objet :  
  
 [!code-csharp[LinesCurvesAndShapes#91](~/samples/snippets/csharp/VS_Snippets_Winforms/LinesCurvesAndShapes/CS/Class1.cs#91)]
 [!code-vb[LinesCurvesAndShapes#91](~/samples/snippets/visualbasic/VS_Snippets_Winforms/LinesCurvesAndShapes/VB/Class1.vb#91)]  
  
## <a name="see-also"></a>Voir aussi

- <xref:System.Drawing.Graphics?displayProperty=nameWithType>
- <xref:System.Drawing.Region?displayProperty=nameWithType>
- [Lignes, courbes et formes](lines-curves-and-shapes.md)
- [Utilisation de régions](using-regions.md)
