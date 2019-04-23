---
title: 'Tutoriel : hébergement d’objets visuels dans une application Win32'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- visual objects in Win32 code [WPF]
- Win32 code [WPF], visual objects in
- hosting [WPF], visual objects in Win32 code
ms.assetid: f0e1600c-3217-43d5-875d-1864fa7fe628
ms.openlocfilehash: b260f96246f0d9e5447b74a05e1396bfef176197
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59111460"
---
# <a name="tutorial-hosting-visual-objects-in-a-win32-application"></a>Tutoriel : hébergement d’objets visuels dans une application Win32
[!INCLUDE[TLA#tla_winclient](../../../../includes/tlasharptla-winclient-md.md)] propose un environnement de création d'applications élaboré. Toutefois, lorsque vous avez beaucoup investi dans [!INCLUDE[TLA#tla_win32](../../../../includes/tlasharptla-win32-md.md)] code, il peut être plus judicieux d’ajouter [!INCLUDE[TLA2#tla_winclient](../../../../includes/tla2sharptla-winclient-md.md)] fonctionnalités à votre application plutôt que de réécrire votre code. Prise en charge [!INCLUDE[TLA#tla_win32](../../../../includes/tlasharptla-win32-md.md)] et [!INCLUDE[TLA2#tla_winclient](../../../../includes/tla2sharptla-winclient-md.md)] sous-systèmes graphiques utilisés simultanément dans une application, [!INCLUDE[TLA2#tla_winclient](../../../../includes/tla2sharptla-winclient-md.md)] fournit un mécanisme pour héberger des objets dans un [!INCLUDE[TLA2#tla_win32](../../../../includes/tla2sharptla-win32-md.md)] fenêtre.  
  
 Ce didacticiel explique comment écrire un exemple d’application, [Test de positionnement avec interopérabilité Win32, exemple](https://go.microsoft.com/fwlink/?LinkID=159995), qui héberge [!INCLUDE[TLA2#tla_winclient](../../../../includes/tla2sharptla-winclient-md.md)] objets visuels dans un [!INCLUDE[TLA2#tla_win32](../../../../includes/tla2sharptla-win32-md.md)] fenêtre.  

<a name="requirements"></a>   
## <a name="requirements"></a>Configuration requise  
 Ce didacticiel suppose que vous avez des connaissances de base en matière de programmation [!INCLUDE[TLA2#tla_winclient](../../../../includes/tla2sharptla-winclient-md.md)] et [!INCLUDE[TLA2#tla_win32](../../../../includes/tla2sharptla-win32-md.md)]. Pour obtenir une présentation générale [!INCLUDE[TLA2#tla_winclient](../../../../includes/tla2sharptla-winclient-md.md)] programmation, consultez [procédure pas à pas : Ma première application de bureau WPF](../getting-started/walkthrough-my-first-wpf-desktop-application.md). Pour une introduction aux [!INCLUDE[TLA2#tla_win32](../../../../includes/tla2sharptla-win32-md.md)] programmation, consultez un des nombreux ouvrages sur le sujet, en particulier *Windows programmation* de Charles Petzold.  
  
> [!NOTE]
>  Ce didacticiel comprend plusieurs exemples de code tirés de l'exemple associé. Cependant, pour une meilleure lecture, il n'inclut pas la totalité de l'exemple de code. Pour l’exemple de code complet, consultez [Test de positionnement avec interopérabilité Win32, exemple](https://go.microsoft.com/fwlink/?LinkID=159995).  
  
<a name="creating_the_host_win32_window"></a>   
## <a name="creating-the-host-win32-window"></a>Création de la fenêtre Win32 hôte  
 La clé à l’hébergement [!INCLUDE[TLA2#tla_winclient](../../../../includes/tla2sharptla-winclient-md.md)] des objets dans un [!INCLUDE[TLA2#tla_win32](../../../../includes/tla2sharptla-win32-md.md)] fenêtre est la <xref:System.Windows.Interop.HwndSource> classe. Cette classe encapsule le [!INCLUDE[TLA2#tla_winclient](../../../../includes/tla2sharptla-winclient-md.md)] des objets dans un [!INCLUDE[TLA2#tla_win32](../../../../includes/tla2sharptla-win32-md.md)] fenêtre, ce qui leur permet d’être incorporé dans votre [!INCLUDE[TLA#tla_ui](../../../../includes/tlasharptla-ui-md.md)] comme une fenêtre enfant.  
  
 L’exemple suivant montre le code pour créer le <xref:System.Windows.Interop.HwndSource> de l’objet en tant que le [!INCLUDE[TLA2#tla_win32](../../../../includes/tla2sharptla-win32-md.md)] fenêtre du conteneur pour les objets visuels. Pour définir le style de fenêtre, de position et d’autres paramètres pour le [!INCLUDE[TLA2#tla_win32](../../../../includes/tla2sharptla-win32-md.md)] fenêtre, utilisez le <xref:System.Windows.Interop.HwndSourceParameters> objet.  
  
 [!code-csharp[VisualsHitTesting#101](~/samples/snippets/csharp/VS_Snippets_Wpf/VisualsHitTesting/CSharp/MyWindow.cs#101)]
 [!code-vb[VisualsHitTesting#101](~/samples/snippets/visualbasic/VS_Snippets_Wpf/VisualsHitTesting/VisualBasic/MyWindow.vb#101)]  
  
> [!NOTE]
>  La valeur de la <xref:System.Windows.Interop.HwndSourceParameters.ExtendedWindowStyle%2A> propriété ne peut pas être définie sur WS_EX_TRANSPARENT. Cela signifie que l’hôte [!INCLUDE[TLA2#tla_win32](../../../../includes/tla2sharptla-win32-md.md)] fenêtre ne peut pas être transparente. Pour cette raison, la couleur d’arrière-plan de l’hôte [!INCLUDE[TLA2#tla_win32](../../../../includes/tla2sharptla-win32-md.md)] fenêtre est définie sur la même couleur d’arrière-plan que sa fenêtre parente.  
  
<a name="adding_visual_objects_to_the_host_win32_window"></a>   
## <a name="adding-visual-objects-to-the-host-win32-window"></a>Ajout d’objets visuels à la fenêtre Win32 hôte  
 Une fois que vous avez créé un hôte [!INCLUDE[TLA2#tla_win32](../../../../includes/tla2sharptla-win32-md.md)] fenêtre de conteneur pour les objets visuels, vous pouvez ajouter des objets visuels à celui-ci. Vous devez vous assurer que toutes les transformations des objets visuels, tels que les animations, ne s’étendent pas au-delà des limites de l’hôte [!INCLUDE[TLA2#tla_win32](../../../../includes/tla2sharptla-win32-md.md)] fenêtre du rectangle englobant.  
  
 L’exemple suivant montre le code pour créer le <xref:System.Windows.Interop.HwndSource> de l’objet et ajouter des objets visuels.  
  
> [!NOTE]
>  Le <xref:System.Windows.Interop.HwndSource.RootVisual%2A> propriété de la <xref:System.Windows.Interop.HwndSource> objet est défini sur le premier objet visuel ajouté à l’hôte [!INCLUDE[TLA2#tla_win32](../../../../includes/tla2sharptla-win32-md.md)] fenêtre. L’objet visuel racine définit le nœud supérieur de l’arborescence des objets visuels. Tous les objets visuels suivants ajoutés à l’hôte [!INCLUDE[TLA2#tla_win32](../../../../includes/tla2sharptla-win32-md.md)] fenêtre sont ajoutés comme objets enfants.  
  
 [!code-csharp[VisualsHitTesting#100](~/samples/snippets/csharp/VS_Snippets_Wpf/VisualsHitTesting/CSharp/MyWindow.cs#100)]
 [!code-vb[VisualsHitTesting#100](~/samples/snippets/visualbasic/VS_Snippets_Wpf/VisualsHitTesting/VisualBasic/MyWindow.vb#100)]  
  
<a name="implementing_the_win32_message_filter"></a>   
## <a name="implementing-the-win32-message-filter"></a>Implémentation du filtre de messages Win32  
 L’hôte [!INCLUDE[TLA2#tla_win32](../../../../includes/tla2sharptla-win32-md.md)] fenêtre pour les objets visuels nécessite une procédure de filtre de messages de fenêtre à traiter les messages sont envoyés à la fenêtre à partir de la file d’attente de l’application. La procédure de fenêtre reçoit des messages à partir de la [!INCLUDE[TLA2#tla_win32](../../../../includes/tla2sharptla-win32-md.md)] système. Ces messages peuvent être des messages de gestion de fenêtre ou des messages de saisie. Vous pouvez choisir de gérer un message dans votre procédure de fenêtre ou de transférer le message au système de traitement par défaut.  
  
 Le <xref:System.Windows.Interop.HwndSource> objet que vous avez défini comme parent pour les objets visuels doit faire référence à la procédure de filtre de messages de fenêtre que vous fournissez. Lorsque vous créez le <xref:System.Windows.Interop.HwndSource> de l’objet, définissez le <xref:System.Windows.Interop.HwndSourceParameters.HwndSourceHook%2A> propriété à référencer la procédure de fenêtre.  
  
 [!code-csharp[VisualsHitTesting#102](~/samples/snippets/csharp/VS_Snippets_Wpf/VisualsHitTesting/CSharp/MyWindow.cs#102)]
 [!code-vb[VisualsHitTesting#102](~/samples/snippets/visualbasic/VS_Snippets_Wpf/VisualsHitTesting/VisualBasic/MyWindow.vb#102)]  
  
 L’exemple suivant montre le code permettant de gérer les messages lorsque les boutons gauche et droit de la souris sont relâchés. Position de frappe de la valeur de coordonnée de la souris se trouve dans la valeur de la `lParam` paramètre.  
  
 [!code-csharp[VisualsHitTesting#103](~/samples/snippets/csharp/VS_Snippets_Wpf/VisualsHitTesting/CSharp/MyWindow.cs#103)]
 [!code-vb[VisualsHitTesting#103](~/samples/snippets/visualbasic/VS_Snippets_Wpf/VisualsHitTesting/VisualBasic/MyWindow.vb#103)]  
  
<a name="processing_the_win32_messages"></a>   
## <a name="processing-the-win32-messages"></a>Traitement des messages Win32  
 Le code dans l’exemple suivant montre comment un test de positionnement est effectué sur la hiérarchie des objets visuels contenue dans l’hôte [!INCLUDE[TLA2#tla_win32](../../../../includes/tla2sharptla-win32-md.md)] fenêtre. Vous pouvez déterminer si un point se trouve dans la géométrie d’un objet visuel, à l’aide de la <xref:System.Windows.Media.VisualTreeHelper.HitTest%2A> méthode pour spécifier l’objet visuel racine et la valeur des coordonnées pour le test de positionnement. Dans ce cas, l’objet visuel racine est la valeur de la <xref:System.Windows.Interop.HwndSource.RootVisual%2A> propriété de la <xref:System.Windows.Interop.HwndSource> objet.  
  
 [!code-csharp[VisualsHitTesting#104](~/samples/snippets/csharp/VS_Snippets_Wpf/VisualsHitTesting/CSharp/MyCircle.cs#104)]
 [!code-vb[VisualsHitTesting#104](~/samples/snippets/visualbasic/VS_Snippets_Wpf/VisualsHitTesting/VisualBasic/MyCircle.vb#104)]  
  
 Pour plus d’informations sur le test de positionnement sur des objets visuels, consultez [test de positionnement dans la couche visuelle](hit-testing-in-the-visual-layer.md).  
  
## <a name="see-also"></a>Voir aussi

- <xref:System.Windows.Interop.HwndSource>
- [Test de positionnement avec interopérabilité Win32, exemple](https://go.microsoft.com/fwlink/?LinkID=159995)
- [Test de positionnement dans la couche visuelle](hit-testing-in-the-visual-layer.md)
