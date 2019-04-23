---
title: 'Procédure : Personnaliser la taille du curseur sur une barre de défilement'
ms.date: 03/30/2017
helpviewer_keywords:
- ScrollBar control [WPF]
- customizing thumb size [WPF]
- thumb size [WPF]
ms.assetid: fa32b866-5ca1-4e73-85e7-2ac64b80d194
ms.openlocfilehash: 60ae7c4e95801036c5deb0c485645297509b830c
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59207277"
---
# <a name="how-to-customize-the-thumb-size-on-a-scrollbar"></a>Procédure : Personnaliser la taille du curseur sur une barre de défilement
Cette rubrique explique comment définir le <xref:System.Windows.Controls.Primitives.Thumb> d’un <xref:System.Windows.Controls.Primitives.ScrollBar> à une taille fixe et comment spécifier une taille minimale pour le <xref:System.Windows.Controls.Primitives.Thumb> d’un <xref:System.Windows.Controls.Primitives.ScrollBar>.  
  
## <a name="example"></a>Exemple  
  
## <a name="description"></a>Description  
 L’exemple suivant crée un <xref:System.Windows.Controls.Primitives.ScrollBar> qui a un <xref:System.Windows.Controls.Primitives.Thumb> avec une taille fixe. L’exemple définit le <xref:System.Windows.Controls.Primitives.Track.ViewportSize%2A> propriété de la <xref:System.Windows.Controls.Primitives.Thumb> à <xref:System.Double.NaN> et définit la hauteur de la <xref:System.Windows.Controls.Primitives.Thumb>.  Pour créer un horizontal <xref:System.Windows.Controls.Primitives.ScrollBar> avec un <xref:System.Windows.Controls.Primitives.Thumb> qui a une largeur fixe, la valeur de la largeur de la <xref:System.Windows.Controls.Primitives.Thumb>.  
  
## <a name="code"></a>Code  
 [!code-xaml[ScrollBarCustomThumbSize#1](~/samples/snippets/csharp/VS_Snippets_Wpf/ScrollBarCustomThumbSize/CS/Window1.xaml#1)]  
  
## <a name="description"></a>Description  
 L’exemple suivant crée un <xref:System.Windows.Controls.Primitives.ScrollBar> qui a un <xref:System.Windows.Controls.Primitives.Thumb> avec une taille minimale. L’exemple définit la valeur de <xref:System.Windows.SystemParameters.VerticalScrollBarButtonHeightKey%2A>. Pour créer un horizontal <xref:System.Windows.Controls.Primitives.ScrollBar> avec un <xref:System.Windows.Controls.Primitives.Thumb> qui a une largeur minimale, définissez le <xref:System.Windows.SystemParameters.HorizontalScrollBarButtonWidthKey%2A>.  
  
## <a name="code"></a>Code  
 [!code-xaml[ScrollBarCustomThumbSize#2](~/samples/snippets/csharp/VS_Snippets_Wpf/ScrollBarCustomThumbSize/CS/Window1.xaml#2)]  
  
## <a name="see-also"></a>Voir aussi

- [Styles et modèles ScrollBar](scrollbar-styles-and-templates.md)
