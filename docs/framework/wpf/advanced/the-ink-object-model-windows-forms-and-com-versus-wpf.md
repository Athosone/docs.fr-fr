---
title: 'Le modèle objet encre : Windows Forms et COM comparé à WPF'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- enabling ink [WPF]
- InkCanvas control [WPF]
- ink object model [WPF]
- tablet pen [WPF], events [WPF]
- ink [WPF], enabling
- events [WPF], tablet pen
ms.assetid: 577835be-b145-4226-8570-1d309e9b3901
ms.openlocfilehash: 68003943041fe0ba405eff1236c43a8e7e9c2b71
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62051674"
---
# <a name="the-ink-object-model-windows-forms-and-com-versus-wpf"></a>Le modèle objet encre : Windows Forms et COM comparé à WPF

Il existe essentiellement trois plateformes qui prennent en charge de l’encre numérique : la plateforme Tablet PC Windows Forms, la plateforme Tablet PC COM et la plateforme Windows Presentation Foundation (WPF).  Le partage de plateformes Windows Forms et COM est un modèle objet semblable, mais le modèle objet pour la [!INCLUDE[TLA2#tla_wpf](../../../../includes/tla2sharptla-wpf-md.md)] plateforme est sensiblement différent.  Cette rubrique décrit les différences de façon générale afin que les développeurs qui ont travaillé avec un modèle objet peuvent de mieux comprendre l’autre.  
  
## <a name="enabling-ink-in-an-application"></a>L’activation de l’encre dans une Application  
 Les trois plateformes fournissent des objets et des contrôles qui permettent à une application recevoir l’entrée d’un stylet.  Les Windows Forms et les plateformes de COM fournis avec [Microsoft.Ink.InkPicture](https://docs.microsoft.com/previous-versions/dotnet/netframework-3.5/ms583740(v=vs.90)), [Microsoft.Ink.InkEdit](https://docs.microsoft.com/previous-versions/dotnet/netframework-3.5/ms552265(v=vs.90)), [Microsoft.Ink.InkOverlay](https://docs.microsoft.com/previous-versions/dotnet/netframework-3.5/ms552322(v=vs.90)) et [ Microsoft.Ink.InkCollector](https://docs.microsoft.com/previous-versions/dotnet/netframework-3.5/ms583683(v=vs.90)) classes.  [Microsoft.Ink.InkPicture](https://docs.microsoft.com/previous-versions/dotnet/netframework-3.5/ms583740(v=vs.90)) et [Microsoft.Ink.InkEdit](https://docs.microsoft.com/previous-versions/dotnet/netframework-3.5/ms552265(v=vs.90)) sont des contrôles que vous pouvez ajouter à une application pour collecter l’encre.  Le [Microsoft.Ink.InkOverlay](https://docs.microsoft.com/previous-versions/dotnet/netframework-3.5/ms552322(v=vs.90)) et [Microsoft.Ink.InkCollector](https://docs.microsoft.com/previous-versions/dotnet/netframework-3.5/ms583683(v=vs.90)) peuvent être attachés à une fenêtre existante pour activer l’encre windows et des contrôles personnalisés.  
  
 La plateforme WPF inclut le <xref:System.Windows.Controls.InkCanvas> contrôle.  Vous pouvez ajouter un <xref:System.Windows.Controls.InkCanvas> à votre application et commencer à collecter l’encre immédiatement. Avec la <xref:System.Windows.Controls.InkCanvas>, l’utilisateur peut copier, sélectionner et redimensionner l’encre.  Vous pouvez ajouter d’autres contrôles à la <xref:System.Windows.Controls.InkCanvas>, et l’utilisateur peut écrire à la main sur ces contrôles.  Vous pouvez créer un contrôle personnalisé prenant en charge de l’encre en ajoutant un <xref:System.Windows.Controls.InkPresenter> et en collectant ses points de stylet.  
  
 Le tableau suivant répertorie les emplacements pour en savoir plus sur l’activation de l’encre dans une application :  
  
|Pour ce faire...|Sur la plateforme WPF...|Sur les plateformes de formulaires/COM Windows...|  
|-----------------|--------------------------|------------------------------------------|  
|Ajouter un contrôle prenant en charge de l’encre à une application|Consultez [mise en route avec l’encre](getting-started-with-ink.md).|Consultez [automatique revendications forment exemple](/windows/desktop/tablet/auto-claims-form-sample)|  
|Activer l’encre sur un contrôle personnalisé|Consultez [création d’une entrée manuscrite contrôle Input](creating-an-ink-input-control.md).|Consultez [exemple de Presse-papiers de l’encre](/windows/desktop/tablet/ink-clipboard-sample).|  
  
## <a name="ink-data"></a>Données d’entrée manuscrite  
 Sur les Windows Forms et COM plateformes, [Microsoft.Ink.InkCollector](https://docs.microsoft.com/previous-versions/dotnet/netframework-3.5/ms583683(v=vs.90)), [Microsoft.Ink.InkOverlay](https://docs.microsoft.com/previous-versions/dotnet/netframework-3.5/ms552322(v=vs.90)), [Microsoft.Ink.InkEdit](https://docs.microsoft.com/previous-versions/dotnet/netframework-3.5/ms552265(v=vs.90)), et [ Microsoft.Ink.InkPicture](https://docs.microsoft.com/previous-versions/dotnet/netframework-3.5/ms583740(v=vs.90)) exposent chacun un [Microsoft.Ink.Ink](https://docs.microsoft.com/previous-versions/dotnet/netframework-3.5/ms583670(v=vs.90)) objet. Le [Microsoft.Ink.Ink](https://docs.microsoft.com/previous-versions/dotnet/netframework-3.5/ms583670(v=vs.90)) objet contient les données pour un ou plusieurs [Microsoft.Ink.Stroke](https://docs.microsoft.com/previous-versions/dotnet/netframework-3.5/ms552692(v=vs.90)) objets et expose des méthodes et propriétés pour gérer et manipuler ces traits communes.  Le [Microsoft.Ink.Ink](https://docs.microsoft.com/previous-versions/dotnet/netframework-3.5/ms583670(v=vs.90)) objet gère la durée de vie des traits qu’il contient ; le [Microsoft.Ink.Ink](https://docs.microsoft.com/previous-versions/dotnet/netframework-3.5/ms583670(v=vs.90)) objet crée et supprime les traits qu’il possède.  Chaque [Microsoft.Ink.Stroke](https://docs.microsoft.com/previous-versions/dotnet/netframework-3.5/ms552692(v=vs.90)) a un identificateur qui est unique au sein de son parent [Microsoft.Ink.Ink](https://docs.microsoft.com/previous-versions/dotnet/netframework-3.5/ms583670(v=vs.90)) objet.  
  
 Sur la plateforme WPF, la <xref:System.Windows.Ink.Stroke?displayProperty=nameWithType> classe possède et gère sa propre durée de vie. Un groupe de <xref:System.Windows.Ink.Stroke> objets peuvent être collectés dans un <xref:System.Windows.Ink.StrokeCollection>, qui fournit des opérations de gestion de données méthodes pour l’encre courants tels que d’accès au test, effacement, la transformation et la sérialisation de l’encre. Un <xref:System.Windows.Ink.Stroke> peut appartenir à zéro, un ou plusieurs <xref:System.Windows.Ink.StrokeCollection> objets à n’importe quelle donnent le temps.  Au lieu d’avoir un [Microsoft.Ink.Ink](https://docs.microsoft.com/previous-versions/dotnet/netframework-3.5/ms583670(v=vs.90)) objet, le <xref:System.Windows.Controls.InkCanvas> et <xref:System.Windows.Controls.InkPresenter> contiennent un <xref:System.Windows.Ink.StrokeCollection?displayProperty=nameWithType>.  
  
 La paire d’illustrations suivante compare les modèles d’objet de données d’encre.  Sur les Windows Forms et COM plateformes, les [Microsoft.Ink.Ink](https://docs.microsoft.com/previous-versions/dotnet/netframework-3.5/ms583670(v=vs.90)) objet contraint la durée de vie de la [Microsoft.Ink.Stroke](https://docs.microsoft.com/previous-versions/dotnet/netframework-3.5/ms552692(v=vs.90)) objets et les paquets de stylet appartiennent aux traits individuels.  Deux ou plusieurs traits peuvent référencer le même [Microsoft.Ink.DrawingAttributes](https://docs.microsoft.com/previous-versions/dotnet/netframework-3.5/ms583636(v=vs.90)) de l’objet, comme indiqué dans l’illustration suivante.  
  
 ![Diagramme du modèle d’objet manuscrit pour COM&#47;Winforms. ](./media/ink-inkownsstrokes.png "Ink_InkOwnsStrokes")  
  
 Sur le [!INCLUDE[TLA2#tla_winclient](../../../../includes/tla2sharptla-winclient-md.md)], chaque <xref:System.Windows.Ink.Stroke?displayProperty=nameWithType> est un objet du common language runtime qui existe tant que quelque chose a une référence à celui-ci.  Chaque <xref:System.Windows.Ink.Stroke> références un <xref:System.Windows.Input.StylusPointCollection> et <xref:System.Windows.Ink.DrawingAttributes?displayProperty=nameWithType> objet, qui sont également des objets common language runtime.  
  
 ![Diagramme du modèle d’objet manuscrit pour WPF. ](./media/ink-wpfinkobjectmodel.png "Ink_WPFInkObjectModel")  
  
 Le tableau suivant compare la façon d’accomplir certaines tâches courantes sur les [!INCLUDE[TLA2#tla_wpf](../../../../includes/tla2sharptla-wpf-md.md)] plateforme et les plateformes Windows Forms et COM.  
  
|Tâche|Windows Presentation Foundation|COM et Windows Forms|  
|----------|-------------------------------------|---------------------------|  
|Enregistrer l’encre|<xref:System.Windows.Ink.StrokeCollection.Save%2A>|[Microsoft.Ink.Ink.Save](https://docs.microsoft.com/previous-versions/dotnet/netframework-3.5/ms571335(v=vs.90))|  
|Charger l’encre|Créer un <xref:System.Windows.Ink.StrokeCollection> avec la <xref:System.Windows.Ink.StrokeCollection.%23ctor%2A> constructeur.|[Microsoft.Ink.Ink.Load](https://docs.microsoft.com/previous-versions/dotnet/netframework-3.5/ms569609(v=vs.90))|  
|Test de positionnement|<xref:System.Windows.Ink.StrokeCollection.HitTest%2A>|[Microsoft.Ink.Ink.HitTest](https://docs.microsoft.com/previous-versions/dotnet/netframework-3.5/ms571330(v=vs.90))|  
|Copier l’entrée manuscrite|<xref:System.Windows.Controls.InkCanvas.CopySelection%2A>|[Microsoft.Ink.Ink.ClipboardCopy](https://docs.microsoft.com/previous-versions/dotnet/netframework-3.5/ms571316(v=vs.90))|  
|Collez l’encre|<xref:System.Windows.Controls.InkCanvas.Paste%2A>|[Microsoft.Ink.Ink.ClipboardPaste](https://docs.microsoft.com/previous-versions/dotnet/netframework-3.5/ms571318(v=vs.90))|  
|Propriétés personnalisées d’accès sur une collection de traits|<xref:System.Windows.Ink.StrokeCollection.AddPropertyData%2A> (les propriétés sont stockées en interne et accessibles via <xref:System.Windows.Ink.StrokeCollection.AddPropertyData%2A>, <xref:System.Windows.Ink.StrokeCollection.RemovePropertyData%2A>, et <xref:System.Windows.Ink.StrokeCollection.ContainsPropertyData%2A>)|Utilisez [Microsoft.Ink.Ink.ExtendedProperties](https://docs.microsoft.com/previous-versions/dotnet/netframework-3.5/ms582214(v=vs.90))|  
  
### <a name="sharing-ink-between-platforms"></a>Partage d’encre entre les plateformes  
 Bien que les plateformes aient des modèles objet différents pour les données de l’encre, il est très facile de partager les données entre les plateformes. Les exemples suivants enregistrent l’encre à partir d’une application Windows Forms et chargent l’encre dans une application Windows Presentation Foundation.  
  
 [!code-csharp[WinFormWPFInk#UsingWinforms](~/samples/snippets/csharp/VS_Snippets_Wpf/WinformWPFInk/CSharp/Program.cs#usingwinforms)]
 [!code-vb[WinFormWPFInk#UsingWinforms](~/samples/snippets/visualbasic/VS_Snippets_Wpf/WinformWPFInk/VisualBasic/Module1.vb#usingwinforms)]  
[!code-csharp[WinFormWPFInk#SaveWinforms](~/samples/snippets/csharp/VS_Snippets_Wpf/WinformWPFInk/CSharp/Program.cs#savewinforms)]
[!code-vb[WinFormWPFInk#SaveWinforms](~/samples/snippets/visualbasic/VS_Snippets_Wpf/WinformWPFInk/VisualBasic/Module1.vb#savewinforms)]  
  
 [!code-csharp[WinFormWPFInk#UsingWPF](~/samples/snippets/csharp/VS_Snippets_Wpf/WinformWPFInk/CSharp/Program.cs#usingwpf)]
 [!code-vb[WinFormWPFInk#UsingWPF](~/samples/snippets/visualbasic/VS_Snippets_Wpf/WinformWPFInk/VisualBasic/Module1.vb#usingwpf)]  
[!code-csharp[WinFormWPFInk#LoadWPF](~/samples/snippets/csharp/VS_Snippets_Wpf/WinformWPFInk/CSharp/Program.cs#loadwpf)]
[!code-vb[WinFormWPFInk#LoadWPF](~/samples/snippets/visualbasic/VS_Snippets_Wpf/WinformWPFInk/VisualBasic/Module1.vb#loadwpf)]  
  
 Les exemples suivants enregistrent l’encre à partir d’une application Windows Presentation Foundation et chargent l’encre dans une application Windows Forms.  
  
 [!code-csharp[WinFormWPFInk#UsingWPF](~/samples/snippets/csharp/VS_Snippets_Wpf/WinformWPFInk/CSharp/Program.cs#usingwpf)]
 [!code-vb[WinFormWPFInk#UsingWPF](~/samples/snippets/visualbasic/VS_Snippets_Wpf/WinformWPFInk/VisualBasic/Module1.vb#usingwpf)]  
[!code-csharp[WinFormWPFInk#SaveWPF](~/samples/snippets/csharp/VS_Snippets_Wpf/WinformWPFInk/CSharp/Program.cs#savewpf)]
[!code-vb[WinFormWPFInk#SaveWPF](~/samples/snippets/visualbasic/VS_Snippets_Wpf/WinformWPFInk/VisualBasic/Module1.vb#savewpf)]  
  
 [!code-csharp[WinFormWPFInk#UsingWinforms](~/samples/snippets/csharp/VS_Snippets_Wpf/WinformWPFInk/CSharp/Program.cs#usingwinforms)]
 [!code-vb[WinFormWPFInk#UsingWinforms](~/samples/snippets/visualbasic/VS_Snippets_Wpf/WinformWPFInk/VisualBasic/Module1.vb#usingwinforms)]  
[!code-csharp[WinFormWPFInk#LoadWinforms](~/samples/snippets/csharp/VS_Snippets_Wpf/WinformWPFInk/CSharp/Program.cs#loadwinforms)]
[!code-vb[WinFormWPFInk#LoadWinforms](~/samples/snippets/visualbasic/VS_Snippets_Wpf/WinformWPFInk/VisualBasic/Module1.vb#loadwinforms)]
## <a name="events-from-the-tablet-pen"></a>Événements du stylet  

 Le [Microsoft.Ink.InkOverlay](https://docs.microsoft.com/previous-versions/dotnet/netframework-3.5/ms552322(v=vs.90)), [Microsoft.Ink.InkCollector](https://docs.microsoft.com/previous-versions/dotnet/netframework-3.5/ms583683(v=vs.90)), et [Microsoft.Ink.InkPicture](https://docs.microsoft.com/previous-versions/dotnet/netframework-3.5/ms583740(v=vs.90)) sur les Windows Forms et COM plateformes recevoir des événements lorsque l’utilisateur entrées du stylo de données. Le [Microsoft.Ink.InkOverlay](https://docs.microsoft.com/previous-versions/dotnet/netframework-3.5/ms552322(v=vs.90)) ou [Microsoft.Ink.InkCollector](https://docs.microsoft.com/previous-versions/dotnet/netframework-3.5/ms583683(v=vs.90)) est attaché à une fenêtre ou un contrôle et peuvent s’abonner aux événements déclenchés par les données d’entrée de tablette. Le thread sur lequel ces événements se produit dépend si les événements sont déclenchés avec un stylet, une souris, ou par programme. Pour plus d’informations sur les threads par rapport à ces événements, consultez [considérations générales de Threading](/windows/desktop/tablet/general-threading-considerations) et [des Threads qui permettre déclencher un événement](/windows/desktop/tablet/threads-on-which-an-event-can-fire).  
  
 Sur la plateforme Windows Presentation Foundation, la <xref:System.Windows.UIElement> classe a des événements pour l’entrée du stylet. Cela signifie que chaque contrôle expose l’ensemble des événements de stylet.  Les événements de stylet ont des événements de tunneling/propagation paires et sont toujours effectuées sur le thread d’application.  Pour plus d’informations, consultez [vue d’ensemble des événements routés](routed-events-overview.md).  
  
 Le schéma suivant compare les modèles d’objet pour les classes qui déclenchent des événements de stylet. Le modèle objet Windows Presentation Foundation affiche uniquement les événements de propagation, pas les équivalents d’événements de tunneling.  
  
 ![Diagramme des événements de stylet dans WPF par rapport à Winforms. ](./media/ink-stylusevents.png "Ink_StylusEvents")  
  
## <a name="pen-data"></a>Données de stylet  
 Les trois plateformes vous permettent d’intercepter et de manipuler les données qui provient d’un stylet.  Sur les Windows Forms et les plateformes de COM, ceci est obtenue en créant un [Microsoft.StylusInput.RealTimeStylus](https://docs.microsoft.com/previous-versions/dotnet/netframework-3.5/ms585724(v=vs.90)), attachement d’une fenêtre ou un contrôle à celui-ci et la création d’une classe qui implémente le [ Microsoft.StylusInput.IStylusSyncPlugin](https://docs.microsoft.com/previous-versions/dotnet/netframework-3.5/ms575201(v=vs.90)) ou [Microsoft.StylusInput.IStylusAsyncPlugin](https://docs.microsoft.com/previous-versions/dotnet/netframework-3.5/ms575194(v=vs.90)) interface. Le plug-in personnalisé est ensuite ajouté à la collection de plug-in de la [Microsoft.StylusInput.RealTimeStylus](https://docs.microsoft.com/previous-versions/dotnet/netframework-3.5/ms585724(v=vs.90)). Pour plus d’informations sur ce modèle objet, consultez [Architecture de the StylusInput APIs](/windows/desktop/tablet/architecture-of-the-stylusinput-apis).  
  
 Sur le [!INCLUDE[TLA2#tla_wpf](../../../../includes/tla2sharptla-wpf-md.md)] plateforme, le <xref:System.Windows.UIElement> classe expose une collection de plug-ins, similaires dans la conception pour la [Microsoft.StylusInput.RealTimeStylus](https://docs.microsoft.com/previous-versions/dotnet/netframework-3.5/ms585724(v=vs.90)).  Pour intercepter les données de stylet, créez une classe qui hérite de <xref:System.Windows.Input.StylusPlugIns.StylusPlugIn> et ajouter cet objet à la <xref:System.Windows.UIElement.StylusPlugIns%2A> collection de la <xref:System.Windows.UIElement>. Pour plus d’informations sur cette interaction, consultez [interception d’entrée à partir du stylet](intercepting-input-from-the-stylus.md).  
  
 Sur toutes les plateformes, un pool de threads reçoit les données de l’encre via des événements de stylet et l’envoie au thread d’application.  Pour plus d’informations concernant les threads sur les plateformes COM et Windows, consultez [Threading Considerations for the StylusInput APIs](/windows/desktop/tablet/threading-considerations-for-the-stylusinput-apis).  Pour plus d’informations concernant les threads sur le logiciel de présentation de Windows, consultez [le modèle de thread de l’encre](the-ink-threading-model.md).  
  
 L’illustration suivante compare les modèles d’objet pour les classes qui reçoivent des données de stylet sur le pool de threads de stylet.  
  
 ![Diagramme de la StylusPlugin modèle WPF par rapport à Winforms. ](./media/ink-stylusplugins.png "Ink_StylusPlugins")
