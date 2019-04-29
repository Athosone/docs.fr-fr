---
title: 'Procédure : Reconnaître les mouvements d’application'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- application gestures [WPF], recognizing
- gestures [WPF], recognizing
ms.assetid: d58b740f-5192-4a3e-af59-7aa162e6ca15
ms.openlocfilehash: 647e7c9c1d785cebfdc362dc48511d865f3945dc
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61768431"
---
# <a name="how-to-recognize-application-gestures"></a>Procédure : Reconnaître les mouvements d’application
L’exemple suivant montre comment effacer l’encre lorsqu’un utilisateur apporte une <xref:System.Windows.Ink.ApplicationGesture.ScratchOut> de mouvements sur un <xref:System.Windows.Controls.InkCanvas>. Cet exemple suppose un <xref:System.Windows.Controls.InkCanvas>, appelé `inkCanvas1`, est déclaré dans le fichier XAML.  
  
## <a name="example"></a>Exemple  
 [!code-csharp[HowToRecognizeGestures#1](~/samples/snippets/csharp/VS_Snippets_Wpf/HowToRecognizeGestures/CSharp/Window1.xaml.cs#1)]
 [!code-vb[HowToRecognizeGestures#1](~/samples/snippets/visualbasic/VS_Snippets_Wpf/HowToRecognizeGestures/VisualBasic/Window1.xaml.vb#1)]  
  
## <a name="see-also"></a>Voir aussi

- <xref:System.Windows.Ink.ApplicationGesture>
- <xref:System.Windows.Controls.InkCanvas>
- <xref:System.Windows.Controls.InkCanvas.Gesture>
