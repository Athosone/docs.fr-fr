---
title: Vue d'ensemble du contrôle NumericUpDown (Windows Forms)
ms.date: 03/30/2017
f1_keywords:
- NumericUpDown
helpviewer_keywords:
- numeric spin button control [Windows Forms], Windows Forms
- NumericUpDown control [Windows Forms], about NumericUpDown control
- spin button control [Windows Forms], Windows Forms
ms.assetid: cff3cf30-4d46-4381-87df-37bfe83c71c5
ms.openlocfilehash: 218eb685e546acac76a18450612a1601ab87276b
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59109874"
---
# <a name="numericupdown-control-overview-windows-forms"></a>Vue d'ensemble du contrôle NumericUpDown (Windows Forms)
Le <xref:System.Windows.Forms.NumericUpDown> contrôle se présente comme une combinaison d’une zone de texte et une paire de flèches sur lesquelles l’utilisateur peut cliquer pour ajuster une valeur. Le contrôle affiche et définit une valeur numérique unique à partir d’une liste de choix de valeurs numériques fixe. L’utilisateur peut augmenter et diminuer le nombre en cliquant sur le haut et bas flèches, en appuyant sur les touches de direction haut et bas, ou en tapant un nombre dans la partie zone de texte du contrôle. En cliquant sur la touche de direction haut déplace le numéro de la valeur maximale ; en cliquant sur la touche de direction bas déplace le nombre vers le minimum.  
  
 En raison de ses fonctionnalités polyvalentes, ce contrôle est par exemple, un choix évident, si vous souhaitez créer un contrôle de volume pour une application de lecteur de musique. Le <xref:System.Windows.Forms.NumericUpDown> contrôle est utilisé dans de nombreuses applications du Panneau de configuration Windows.  
  
## <a name="key-properties-and-methods"></a>Méthodes et propriétés de clé  
 Les nombres affichés dans la zone de texte du contrôle peuvent être dans différents formats, y compris hexadécimales. Pour plus d'informations, voir [Procédure : Définissez le Format pour les Windows Forms contrôle NumericUpDown](how-to-set-the-format-for-the-windows-forms-numericupdown-control.md). Les principales propriétés du contrôle sont <xref:System.Windows.Forms.NumericUpDown.Value%2A>, <xref:System.Windows.Forms.NumericUpDown.Maximum%2A> (valeur par défaut 100), <xref:System.Windows.Forms.NumericUpDown.Minimum%2A> (valeur par défaut 0), et <xref:System.Windows.Forms.NumericUpDown.Increment%2A> (valeur par défaut 1). Le <xref:System.Windows.Forms.NumericUpDown.Value%2A> propriété définit le nombre actuellement sélectionné dans le contrôle. Le <xref:System.Windows.Forms.NumericUpDown.Increment%2A> propriété définit la durée que le nombre est ajusté par quand l’utilisateur clique sur un haut ou flèche vers le bas. Lorsque le focus se déplace hors du contrôle, toute valeur entrée est validée en fonction les valeurs numériques minimales et maximales. Vous pouvez augmenter la vitesse de déplacement du contrôle à travers les nombres, lorsque l’utilisateur clique en permanence le haut ou flèche bas, avec le <xref:System.Windows.Forms.NumericUpDown.Accelerations%2A> propriété. Les principales méthodes du contrôle sont <xref:System.Windows.Forms.NumericUpDown.UpButton%2A> et <xref:System.Windows.Forms.NumericUpDown.DownButton%2A>.  
  
## <a name="see-also"></a>Voir aussi

- <xref:System.Windows.Forms.NumericUpDown>
- [NumericUpDown, contrôle](numericupdown-control-windows-forms.md)
- [Guide pratique pour Définir le Format pour le contrôle NumericUpDown Windows Forms](how-to-set-the-format-for-the-windows-forms-numericupdown-control.md)
- [TextBox, contrôle](textbox-control-windows-forms.md)
