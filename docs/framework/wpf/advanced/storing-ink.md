---
title: Stockage de l'encre
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- ISF (Ink Serialized Format)
- storing ink [WPF]
- ink [WPF], storing
- retrieving ink [WPF]
- Ink Serialized Format (ISF)
ms.assetid: a3f6d16b-d682-4680-9965-907332b4d2b8
ms.openlocfilehash: 4089aa7942105c14eb628c75edb7f53ffacfaeb0
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62053368"
---
# <a name="storing-ink"></a>Stockage de l'encre
Le <xref:System.Windows.Ink.StrokeCollection.Save%2A> méthodes fournissent la prise en charge pour le stockage de l’encre en tant que Ink Serialized Format (ISF). Les constructeurs pour la <xref:System.Windows.Ink.StrokeCollection> classe fournit la prise en charge pour la lecture des données d’entrée manuscrite.  
  
## <a name="ink-storage-and-retrieval"></a>Stockage de l’encre et la récupération  
 Cette section explique comment stocker et récupérer l’encre dans le [!INCLUDE[TLA2#tla_winclient](../../../../includes/tla2sharptla-winclient-md.md)] plateforme.  
  
 L’exemple suivant implémente un gestionnaire d’événements de clic de bouton qui présente à l’utilisateur avec une boîte de dialogue d’enregistrement de fichier et enregistre l’encre à partir d’un <xref:System.Windows.Controls.InkCanvas> dans un fichier.  
  
 [!code-csharp[DigitalInkTopics#12](~/samples/snippets/csharp/VS_Snippets_Wpf/DigitalInkTopics/CSharp/Window1.xaml.cs#12)]
 [!code-vb[DigitalInkTopics#12](~/samples/snippets/visualbasic/VS_Snippets_Wpf/DigitalInkTopics/VisualBasic/Window1.xaml.vb#12)]  
  
 L’exemple suivant implémente un gestionnaire d’événements de clic de bouton qui présente à l’utilisateur avec une boîte de dialogue Ouvrir le fichier et lit l’encre à partir du fichier dans un <xref:System.Windows.Controls.InkCanvas> élément.  
  
 [!code-csharp[DigitalInkTopics#13](~/samples/snippets/csharp/VS_Snippets_Wpf/DigitalInkTopics/CSharp/Window1.xaml.cs#13)]
 [!code-vb[DigitalInkTopics#13](~/samples/snippets/visualbasic/VS_Snippets_Wpf/DigitalInkTopics/VisualBasic/Window1.xaml.vb#13)]  
  
## <a name="see-also"></a>Voir aussi

- <xref:System.Windows.Controls.InkCanvas>
- [Windows Presentation Foundation](../index.md)
