---
title: 'Procédure : Rechercher une horloge de façon synchrone'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- clocks [WPF], seeking synchronously
- seeking clocks synchronously [WPF]
ms.assetid: e5b7529b-b7d0-40d2-9e1d-fa4b5e736e96
ms.openlocfilehash: 9b6b1f5523effc56ccd9ddaa4f478e1d3a20ada8
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61651257"
---
# <a name="how-to-seek-a-clock-synchronously"></a>Procédure : Rechercher une horloge de façon synchrone
Utilisez le <xref:System.Windows.Media.Animation.ClockController.SeekAlignedToLastTick%2A> méthode pour rechercher une horloge à un point spécifique de façon synchrone. L’exemple suivant illustre les deux le <xref:System.Windows.Media.Animation.ClockController.Seek%2A> et <xref:System.Windows.Media.Animation.ClockController.SeekAlignedToLastTick%2A> méthodes d’un <xref:System.Windows.Media.Animation.ClockController>.  
  
 Cet exemple montre comment rechercher un <xref:System.Windows.Media.Animation.Clock>; pour obtenir un exemple montrant comment rechercher un storyboard, consultez [rechercher un Storyboard de façon synchrone](how-to-seek-a-storyboard-synchronously.md) .  
  
## <a name="example"></a>Exemple  
 [!code-csharp[ClockController_procedural_snip#ClockControllerSeekExample](~/samples/snippets/csharp/VS_Snippets_Wpf/ClockController_procedural_snip/CSharp/SeekAlignedToLastTickExample.cs#clockcontrollerseekexample)]
 [!code-vb[ClockController_procedural_snip#ClockControllerSeekExample](~/samples/snippets/visualbasic/VS_Snippets_Wpf/ClockController_procedural_snip/visualbasic/seekalignedtolasttickexample.vb#clockcontrollerseekexample)]
