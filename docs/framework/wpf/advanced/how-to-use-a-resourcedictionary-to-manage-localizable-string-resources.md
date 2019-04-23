---
title: 'Procédure : Utiliser un ResourceDictionary pour gérer des ressources de type chaîne localisables'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- resources [WPF], packaging string resources
- packaging string resources [WPF]
- ResourceDictionary [WPF]
- localization [WPF], packaging string resources
ms.assetid: 19e7d9a5-20df-4ad3-b157-fe6515902e5e
ms.openlocfilehash: b56a307ed31fc8f7573215eac70350ac5e4b9de1
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59772113"
---
# <a name="how-to-use-a-resourcedictionary-to-manage-localizable-string-resources"></a>Procédure : Utiliser un ResourceDictionary pour gérer des ressources de type chaîne localisables
Cet exemple montre comment utiliser un <xref:System.Windows.ResourceDictionary> pour empaqueter des ressources de type chaîne localisables pour les applications Windows Presentation Foundation (WPF).  
  
### <a name="to-use-a-resourcedictionary-to-manage-localizable-string-resources"></a>Pour utiliser un ResourceDictionary pour gérer des ressources de type chaîne localisables  
  
1. Créer un <xref:System.Windows.ResourceDictionary> qui contient les chaînes que vous souhaitez localiser. Le code suivant fournit un exemple.  
  
     [!code-xaml[StringLocalizationSample#StringResourceDictionary](~/samples/snippets/csharp/VS_Snippets_Wpf/StringLocalizationSample/CSharp/StringResources.xaml#stringresourcedictionary)]  
  
     Ce code définit une ressource de chaîne, `localizedMessage`, de type <xref:System.String>, à partir de la <xref:System> espace de noms dans mscorlib.dll.  
  
2. Ajouter le <xref:System.Windows.ResourceDictionary> à votre application, en utilisant le code suivant.  
  
     [!code-xaml[StringLocalizationSample#ReferencingStringResourceDictionary](~/samples/snippets/csharp/VS_Snippets_Wpf/StringLocalizationSample/CSharp/App.xaml#referencingstringresourcedictionary)]  
  
3. Utiliser la ressource de chaîne à partir du balisage, à l’aide de [!INCLUDE[TLA#tla_xaml](../../../../includes/tlasharptla-xaml-md.md)] comme suit.  
  
     [!code-xaml[StringLocalizationSample#GetLocalizedResourceFromMarkup](~/samples/snippets/csharp/VS_Snippets_Wpf/StringLocalizationSample/CSharp/MainWindow.xaml#getlocalizedresourcefrommarkup)]  
  
4. Utilisez la ressource de chaîne à partir du code-behind, à l’aide de code semblable au suivant.  
  
     [!code-csharp[StringLocalizationSample#GetLocalizedResourceFromCode](~/samples/snippets/csharp/VS_Snippets_Wpf/StringLocalizationSample/CSharp/MainWindow.xaml.cs#getlocalizedresourcefromcode)]
     [!code-vb[StringLocalizationSample#GetLocalizedResourceFromCode](~/samples/snippets/visualbasic/VS_Snippets_Wpf/StringLocalizationSample/VisualBasic/MainWindow.xaml.vb#getlocalizedresourcefromcode)]  
  
5. Localisez l’application. Pour plus d’informations, consultez [localiser une Application](how-to-localize-an-application.md).
