---
title: Reconnaissance d'écriture manuscrite
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- handwriting recognition [WPF]
- recognition of handwriting [WPF]
ms.assetid: f4e8576d-e731-4bac-9818-22e2ae636636
ms.openlocfilehash: 417af272514ac9ce68c8faa72339f2befc2dd7c1
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61923381"
---
# <a name="handwriting-recognition"></a>Reconnaissance d'écriture manuscrite
Cette section présente les notions de base de la reconnaissance relative à l’encre numérique dans la plateforme WPF.  
  
## <a name="recognition-solutions"></a>Solutions de reconnaissance  
 L’exemple suivant montre comment reconnaître de l’encre à l’aide de la classe [Microsoft.Ink.InkCollector](https://docs.microsoft.com/previous-versions/dotnet/netframework-3.5/ms583683(v=vs.90)).  
  
> [!NOTE]
>  Cet exemple nécessite que les modules de reconnaissance d’écriture manuscrite soient installés sur le système.  
  
 Créez un projet d’application WPF dans Visual Studio, intitulé **InkRecognition**. Remplacez le contenu du fichier Window1.xaml par le code XAML suivant. Ce code restitue l’interface utilisateur de l’application.  
  
 [!code-xaml[InkRecognition#1](~/samples/snippets/csharp/VS_Snippets_Wpf/InkRecognition/CSharp/Window1.xaml#1)]  
  
 Ajoutez une référence à l’assembly Microsoft Annotations, Microsoft.Ink.dll, qui se trouve dans \Program Files\Common Files\Microsoft Shared\Ink. Remplacez le contenu du fichier code-behind par le code suivant.  
  
 [!code-csharp[InkRecognition#2](~/samples/snippets/csharp/VS_Snippets_Wpf/InkRecognition/CSharp/Window1.xaml.cs#2)]
 [!code-vb[InkRecognition#2](~/samples/snippets/visualbasic/VS_Snippets_Wpf/InkRecognition/VisualBasic/Window1.xaml.vb#2)]  
  
## <a name="see-also"></a>Voir aussi

- [Microsoft.Ink.InkCollector](https://docs.microsoft.com/previous-versions/dotnet/netframework-3.5/ms583683(v=vs.90))
