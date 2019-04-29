---
title: 'Procédure : Spécifier HandoffBehavior entre des animations de table de montage séquentiel'
ms.date: 03/30/2017
helpviewer_keywords:
- Storyboards [WPF], handoff behavior between animations
- animation [WPF], handoff behavior between
ms.assetid: 97bd6842-929b-49d9-813e-46553ae46472
ms.openlocfilehash: d7129d6a48bdf31dc4953bb450267ad3b38fdd17
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61651036"
---
# <a name="how-to-specify-handoffbehavior-between-storyboard-animations"></a>Procédure : Spécifier HandoffBehavior entre des animations de table de montage séquentiel
Cet exemple montre comment spécifier le comportement de transfert entre des animations de storyboard. Le <xref:System.Windows.Media.Animation.BeginStoryboard.HandoffBehavior%2A> propriété du <xref:System.Windows.Media.Animation.BeginStoryboard> spécifie comment les nouvelles animations interagissent avec les animations existantes qui sont déjà appliquées à une propriété.  
  
## <a name="example"></a>Exemple  
 L’exemple suivant crée deux boutons s’agrandissent lorsque le curseur de souris se déplace au-dessus d’eux et diminuent lorsque le curseur se déplace. Si vous placez la souris sur un bouton et ensuite supprimez rapidement le curseur, la deuxième animation sera appliquée avant que la première est terminée. C’est lorsque deux animations se chevauchent ainsi que vous pouvez voir la différence entre la <xref:System.Windows.Media.Animation.BeginStoryboard.HandoffBehavior%2A> les valeurs de <xref:System.Windows.Media.Animation.HandoffBehavior.Compose> et <xref:System.Windows.Media.Animation.HandoffBehavior.SnapshotAndReplace>. La valeur <xref:System.Windows.Media.Animation.HandoffBehavior.Compose> combine les animations qui se chevauche à l’origine d’une transition plus fluide entre les animations alors que la valeur <xref:System.Windows.Media.Animation.HandoffBehavior.SnapshotAndReplace> provoque la nouvelle animation remplacement immédiat de l’animation précédemment qui se chevauchent.  
  
 [!code-xaml[timingbehaviors_snip#HandoffBehaviorWholePage](~/samples/snippets/csharp/VS_Snippets_Wpf/timingbehaviors_snip/CSharp/HandoffBehaviorExample.xaml#handoffbehaviorwholepage)]  
  
## <a name="see-also"></a>Voir aussi

- <xref:System.Windows.Media.Animation.BeginStoryboard>
- <xref:System.Windows.Media.Animation.BeginStoryboard.HandoffBehavior%2A>
- [Vue d’ensemble de l’animation](animation-overview.md)
- [L’animation et minutage des rubriques de procédures](animation-and-timing-how-to-topics.md)
