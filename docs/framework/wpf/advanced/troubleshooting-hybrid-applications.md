---
title: Dépannage des applications hybrides
ms.date: 03/30/2017
helpviewer_keywords:
- overlapping controls [WPF]
- Windows Forms [WPF], interoperability with
- Windows Forms [WPF], WPF interoperation
- interoperability [WPF], Windows Forms
- hybrid applications [WPF interoperability]
- message loops [WPF]
ms.assetid: f440c23f-fa5d-4d5a-852f-ba61150e6405
ms.openlocfilehash: 707e77ac69878c1c7fb8e975c1f90ad657228d1a
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59079668"
---
# <a name="troubleshooting-hybrid-applications"></a>Dépannage des applications hybrides
<a name="introduction"></a> Cette rubrique répertorie certains problèmes courants qui peuvent se produire lors de la création d’applications hybrides qui utilisent à la fois les technologies [!INCLUDE[TLA2#tla_winclient](../../../../includes/tla2sharptla-winclient-md.md)] et [!INCLUDE[TLA#tla_winforms](../../../../includes/tlasharptla-winforms-md.md)].  

<a name="overlapping_controls"></a>   
## <a name="overlapping-controls"></a>Chevauchement de contrôles  
 Les contrôles peuvent ne pas se chevaucher comme escompté. [!INCLUDE[TLA#tla_winforms](../../../../includes/tlasharptla-winforms-md.md)] utilise un HWND distinct pour chaque contrôle. [!INCLUDE[TLA2#tla_winclient](../../../../includes/tla2sharptla-winclient-md.md)] utilise un HWND pour tout le contenu d’une page. Cette différence d’implémentation provoque des comportements de chevauchement inattendus.  
  
 Un contrôle [!INCLUDE[TLA#tla_winforms](../../../../includes/tlasharptla-winforms-md.md)] hébergé dans [!INCLUDE[TLA2#tla_winclient](../../../../includes/tla2sharptla-winclient-md.md)] apparaît toujours par-dessus le contenu [!INCLUDE[TLA2#tla_winclient](../../../../includes/tla2sharptla-winclient-md.md)].  
  
 [!INCLUDE[TLA2#tla_winclient](../../../../includes/tla2sharptla-winclient-md.md)] contenu hébergé dans un <xref:System.Windows.Forms.Integration.ElementHost> contrôle s’affiche à l’ordre de plan le <xref:System.Windows.Forms.Integration.ElementHost> contrôle. Il est possible de se chevaucher <xref:System.Windows.Forms.Integration.ElementHost> contrôles, mais hébergé [!INCLUDE[TLA2#tla_winclient](../../../../includes/tla2sharptla-winclient-md.md)] contenu ne pas combiner ou interagir.  
  
<a name="child_property"></a>   
## <a name="child-property"></a>Propriété enfant  
 Le <xref:System.Windows.Forms.Integration.WindowsFormsHost> et <xref:System.Windows.Forms.Integration.ElementHost> classes peuvent héberger uniquement un seul contrôle ou élément enfant. Pour héberger plusieurs contrôles ou éléments, vous devez utiliser un conteneur comme contenu enfant. Par exemple, vous pouvez ajouter [!INCLUDE[TLA#tla_winforms](../../../../includes/tlasharptla-winforms-md.md)] contrôles bouton et case à cocher pour un <xref:System.Windows.Forms.Panel?displayProperty=nameWithType> contrôler, puis assigner le panneau à un <xref:System.Windows.Forms.Integration.WindowsFormsHost> du contrôle <xref:System.Windows.Forms.Integration.WindowsFormsHost.Child%2A> propriété. Toutefois, vous ne peut pas ajouter séparément les contrôles de bouton et la case à cocher au même <xref:System.Windows.Forms.Integration.WindowsFormsHost> contrôle.  
  
<a name="scaling"></a>   
## <a name="scaling"></a>Mise à l'échelle  
 [!INCLUDE[TLA2#tla_winclient](../../../../includes/tla2sharptla-winclient-md.md)] et [!INCLUDE[TLA#tla_winforms](../../../../includes/tlasharptla-winforms-md.md)] ont des modèles de mise à l’échelle différents. Certaines transformations de mise à l’échelle [!INCLUDE[TLA2#tla_winclient](../../../../includes/tla2sharptla-winclient-md.md)] sont significatives pour les contrôles [!INCLUDE[TLA#tla_winforms](../../../../includes/tlasharptla-winforms-md.md)], mais d’autres ne le sont pas. Par exemple, la mise à l’échelle d’un contrôle [!INCLUDE[TLA#tla_winforms](../../../../includes/tlasharptla-winforms-md.md)] à la valeur 0 fonctionnera, mais si vous essayez de mettre à l’échelle le même contrôle à une valeur différente de zéro, la taille du contrôle reste 0. Pour plus d’informations, consultez [Considérations sur la disposition de l’élément WindowsFormsHost](layout-considerations-for-the-windowsformshost-element.md).  
  
<a name="adapter"></a>   
## <a name="adapter"></a>Adaptateur  
 Il peut y avoir confusion lorsque vous utilisez le <xref:System.Windows.Forms.Integration.WindowsFormsHost> et <xref:System.Windows.Forms.Integration.ElementHost> des classes, car elles comprennent un conteneur masqué. À la fois le <xref:System.Windows.Forms.Integration.WindowsFormsHost> et <xref:System.Windows.Forms.Integration.ElementHost> classes ont un conteneur masqué, appelé un *adaptateur*, qu’ils utilisent pour héberger le contenu. Pour le <xref:System.Windows.Forms.Integration.WindowsFormsHost> élément, l’adaptateur dérive de la <xref:System.Windows.Forms.ContainerControl?displayProperty=nameWithType> classe. Pour le <xref:System.Windows.Forms.Integration.ElementHost> contrôle, l’adaptateur dérive de la <xref:System.Windows.Controls.DockPanel> élément. Quand vous voyez des références à l’adaptateur dans d’autres rubriques d’interopérabilité, c’est de ce conteneur qu’il est question.  
  
<a name="nesting"></a>   
## <a name="nesting"></a>Imbrication  
 L’imbrication d’un <xref:System.Windows.Forms.Integration.WindowsFormsHost> élément à l’intérieur d’un <xref:System.Windows.Forms.Integration.ElementHost> contrôle n’est pas pris en charge. L’imbrication d’un <xref:System.Windows.Forms.Integration.ElementHost> contrôler à l’intérieur d’un <xref:System.Windows.Forms.Integration.WindowsFormsHost> élément n’est pas également pris en charge.  
  
<a name="focus"></a>   
## <a name="focus"></a>Focus  
 Le focus fonctionne différemment dans [!INCLUDE[TLA2#tla_winclient](../../../../includes/tla2sharptla-winclient-md.md)] et [!INCLUDE[TLA#tla_winforms](../../../../includes/tlasharptla-winforms-md.md)], ce qui signifie que des problèmes de focus peuvent se produire dans une application hybride. Par exemple, si vous avez le focus à l’intérieur d’un <xref:System.Windows.Forms.Integration.WindowsFormsHost> élément et vous soit réduire et restaurer la page ou afficher une boîte de dialogue modale, focus à l’intérieur du <xref:System.Windows.Forms.Integration.WindowsFormsHost> élément peut-être être perdu. Le <xref:System.Windows.Forms.Integration.WindowsFormsHost> élément a encore le focus, mais pas le contrôle qu’il contient.  
  
 La validation des données est également affectée par le focus. La validation fonctionne un <xref:System.Windows.Forms.Integration.WindowsFormsHost> élément, mais il ne fonctionne pas comme vous le déplacez hors du <xref:System.Windows.Forms.Integration.WindowsFormsHost> élément, ou entre deux différents <xref:System.Windows.Forms.Integration.WindowsFormsHost> éléments.  
  
<a name="property_mapping"></a>   
## <a name="property-mapping"></a>Mappage de propriétés  
 Certains mappages de propriétés nécessitent une interprétation approfondie pour lier des implémentations différentes entre les technologies [!INCLUDE[TLA2#tla_winclient](../../../../includes/tla2sharptla-winclient-md.md)] et [!INCLUDE[TLA#tla_winforms](../../../../includes/tlasharptla-winforms-md.md)]. Les mappages de propriétés permettent à votre code de réagir aux changements de polices, de couleurs et d’autres propriétés. En général, les mappages de propriétés écoutent soit des événements *Property*Changed, soit des appels On*Property*Changed, et définissent des propriétés appropriées sur le contrôle enfant ou son adaptateur. Pour plus d’informations, consultez [Mappage de propriétés Windows Forms et WPF](windows-forms-and-wpf-property-mapping.md).  
  
<a name="layoutrelated_properties_on_hosted_content"></a>   
## <a name="layout-related-properties-on-hosted-content"></a>Propriétés de disposition sur le contenu hébergé  
 Lorsque le <xref:System.Windows.Forms.Integration.WindowsFormsHost.Child%2A?displayProperty=nameWithType> ou <xref:System.Windows.Forms.Integration.ElementHost.Child%2A?displayProperty=nameWithType> propriété est assignée, plusieurs propriétés relatives à la disposition sur le contenu hébergé sont définies automatiquement. La modification de ces propriétés peut provoquer des comportements de disposition inattendus.  
  
 Votre contenu hébergé est ancré pour remplir le <xref:System.Windows.Forms.Integration.WindowsFormsHost> et <xref:System.Windows.Forms.Integration.ElementHost> parent. Pour activer ce comportement de remplissage, plusieurs propriétés sont définies quand vous définissez la propriété enfant. Le tableau suivant répertorie les propriétés de contenu définis par le <xref:System.Windows.Forms.Integration.ElementHost> et <xref:System.Windows.Forms.Integration.WindowsFormsHost> classes.  
  
|Classe hôte|Propriétés de contenu|  
|----------------|------------------------|  
|<xref:System.Windows.Forms.Integration.ElementHost>|<xref:System.Windows.FrameworkElement.Height%2A><br /><br /> <xref:System.Windows.FrameworkElement.Width%2A><br /><br /> <xref:System.Windows.FrameworkElement.Margin%2A><br /><br /> <xref:System.Windows.FrameworkElement.VerticalAlignment%2A><br /><br /> <xref:System.Windows.FrameworkElement.HorizontalAlignment%2A>|  
|<xref:System.Windows.Forms.Integration.WindowsFormsHost>|<xref:System.Windows.Forms.Control.Margin%2A><br /><br /> <xref:System.Windows.Forms.Control.Dock%2A><br /><br /> <xref:System.Windows.Forms.Control.AutoSize%2A><br /><br /> <xref:System.Windows.Forms.Control.Location%2A><br /><br /> <xref:System.Windows.Forms.Control.MaximumSize%2A>|  
  
 Ne définissez pas ces propriétés directement sur le contenu hébergé. Pour plus d’informations, consultez [Considérations sur la disposition de l’élément WindowsFormsHost](layout-considerations-for-the-windowsformshost-element.md).  
  
<a name="navigation_applications"></a>   
## <a name="navigation-applications"></a>Applications de navigation  
 Les applications de navigation peuvent ne pas tenir à jour l’état utilisateur. Le <xref:System.Windows.Forms.Integration.WindowsFormsHost> élément recrée ses contrôles lorsqu’il est utilisé dans une application de navigation. Recréez les contrôles enfants se produit quand l’utilisateur navigue en dehors de la page d’hébergement la <xref:System.Windows.Forms.Integration.WindowsFormsHost> élément et retourne ensuite à ce dernier. Tout contenu qui a été tapé par l’utilisateur sera perdu.  
  
<a name="message_loop_interoperation"></a>   
## <a name="message-loop-interoperation"></a>Interopérabilité des boucles de messages  
 Quand vous travaillez avec des boucles de messages [!INCLUDE[TLA#tla_winforms](../../../../includes/tlasharptla-winforms-md.md)], les messages peuvent ne pas être traités comme prévu. Le <xref:System.Windows.Forms.Integration.WindowsFormsHost.EnableWindowsFormsInterop%2A> méthode est appelée par le <xref:System.Windows.Forms.Integration.WindowsFormsHost> constructeur. Cette méthode ajoute un filtre de messages à la boucle de message [!INCLUDE[TLA2#tla_winclient](../../../../includes/tla2sharptla-winclient-md.md)]. Ce filtre appelle le <xref:System.Windows.Forms.Control.PreProcessMessage%2A?displayProperty=nameWithType> méthode si une <xref:System.Windows.Forms.Control?displayProperty=nameWithType> était la cible du message et traduit/distribue le message.  
  
 Si vous affichez un <xref:System.Windows.Window> dans un [!INCLUDE[TLA#tla_winforms](../../../../includes/tlasharptla-winforms-md.md)] boucle de message avec <xref:System.Windows.Forms.Application.Run%2A?displayProperty=nameWithType>, vous ne pouvez pas taper quoi que ce soit, sauf si vous appelez le <xref:System.Windows.Forms.Integration.ElementHost.EnableModelessKeyboardInterop%2A> (méthode). Le <xref:System.Windows.Forms.Integration.ElementHost.EnableModelessKeyboardInterop%2A> méthode prend un <xref:System.Windows.Window> et ajoute un <xref:System.Windows.Forms.IMessageFilter?displayProperty=nameWithType>, qui redirige les messages liés à la clé pour le [!INCLUDE[TLA2#tla_winclient](../../../../includes/tla2sharptla-winclient-md.md)] boucle de message. Pour plus d’informations, consultez [Architecture d’entrée pour l’interopérabilité entre Windows Forms et WPF](windows-forms-and-wpf-interoperability-input-architecture.md).  
  
<a name="opacity_and_layering"></a>   
## <a name="opacity-and-layering"></a>Opacité et superposition  
 Le <xref:System.Windows.Interop.HwndHost> classe ne prend pas en charge la superposition. Cela signifie que la configuration du <xref:System.Windows.UIElement.Opacity%2A> propriété sur le <xref:System.Windows.Forms.Integration.WindowsFormsHost> élément n’a aucun effet et aucune fusion n’aura lieu avec d’autres [!INCLUDE[TLA2#tla_winclient](../../../../includes/tla2sharptla-winclient-md.md)] windows qui ont <xref:System.Windows.Window.AllowsTransparency%2A> défini sur `true`.  
  
<a name="dispose"></a>   
## <a name="dispose"></a>Suppression  
 Le fait de ne pas supprimer correctement les classes peut entraîner une fuite des ressources. Dans vos applications hybrides, vérifiez que le <xref:System.Windows.Forms.Integration.WindowsFormsHost> et <xref:System.Windows.Forms.Integration.ElementHost> classes sont supprimés, ou vous pouvez provoquer une fuite de ressources. [!INCLUDE[TLA#tla_winforms](../../../../includes/tlasharptla-winforms-md.md)] Supprime <xref:System.Windows.Forms.Integration.ElementHost> contrôle le moment où son non modale <xref:System.Windows.Forms.Form> parents se ferme. [!INCLUDE[TLA2#tla_winclient](../../../../includes/tla2sharptla-winclient-md.md)] Supprime <xref:System.Windows.Forms.Integration.WindowsFormsHost> éléments lorsque votre application s’arrête. Il est possible d’afficher un <xref:System.Windows.Forms.Integration.WindowsFormsHost> élément dans un <xref:System.Windows.Window> dans un [!INCLUDE[TLA#tla_winforms](../../../../includes/tlasharptla-winforms-md.md)] boucle de message. Dans ce cas, votre code peut ne pas être averti que votre application s’arrête.  
  
<a name="enabling_visual_styles"></a>   
## <a name="enabling-visual-styles"></a>Activation des styles visuels  
 Les styles visuels [!INCLUDE[TLA#tla_winxp](../../../../includes/tlasharptla-winxp-md.md)] sur un contrôle [!INCLUDE[TLA#tla_winforms](../../../../includes/tlasharptla-winforms-md.md)] peuvent ne pas être activés. Le <xref:System.Windows.Forms.Application.EnableVisualStyles%2A?displayProperty=nameWithType> méthode est appelée dans le modèle pour un [!INCLUDE[TLA#tla_winforms](../../../../includes/tlasharptla-winforms-md.md)] application. Bien que cette méthode ne soit pas appelée par défaut, si vous utilisez [!INCLUDE[TLA2#tla_visualstu](../../../../includes/tla2sharptla-visualstu-md.md)] pour créer un projet, vous obtiendrez des styles visuels [!INCLUDE[TLA#tla_winxp](../../../../includes/tlasharptla-winxp-md.md)] pour les contrôles, si la version 6.0 de Comctl32.dll est disponible. Vous devez appeler la <xref:System.Windows.Forms.Application.EnableVisualStyles%2A> méthode avant que les handles soient créés sur le thread. Pour plus d'informations, voir [Procédure : Activer des Styles visuels dans une Application hybride](how-to-enable-visual-styles-in-a-hybrid-application.md).  
  
<a name="licensed_controls"></a>   
## <a name="licensed-controls"></a>Contrôles sous licence  
 Les contrôles [!INCLUDE[TLA#tla_winforms](../../../../includes/tlasharptla-winforms-md.md)] sous licence qui présentent à l’utilisateur des informations de licence dans un message peuvent provoquer un comportement inattendu pour une application hybride. Certains contrôles sous licence affichent une boîte de dialogue en réponse à la création de handle. Par exemple, un contrôle sous licence peut informer l’utilisateur qu’une licence est nécessaire ou que l’utilisateur n’a plus le droit qu’à trois utilisations du contrôle.  
  
 Le <xref:System.Windows.Forms.Integration.WindowsFormsHost> élément dérive de la <xref:System.Windows.Interop.HwndHost> classe et les handle du contrôle enfant est créée à l’intérieur de la <xref:System.Windows.Forms.Integration.WindowsFormsHost.BuildWindowCore%2A> (méthode). Le <xref:System.Windows.Interop.HwndHost> classe n’autorise pas les messages à traiter dans le <xref:System.Windows.Forms.Integration.WindowsFormsHost.BuildWindowCore%2A> (méthode), mais l’affichage d’une boîte de dialogue provoque l’envoi de messages. Pour activer ce scénario de licence, appelez le <xref:System.Windows.Forms.Control.CreateControl%2A?displayProperty=nameWithType> méthode sur le contrôle avant de l’affecter en tant que le <xref:System.Windows.Forms.Integration.WindowsFormsHost> enfant de l’élément.  
  
<a name="wpf_designer"></a>   
## <a name="wpf-designer"></a>Concepteur WPF  
 Vous pouvez concevoir votre contenu WPF à l’aide du [!INCLUDE[wpfdesigner_current_long](../../../../includes/wpfdesigner-current-long-md.md)]. Les sections suivantes décrivent certains problèmes courants qui peuvent se produire lors de la création d’applications hybrides avec le [!INCLUDE[wpfdesigner_current_short](../../../../includes/wpfdesigner-current-short-md.md)].  
  
### <a name="backcolortransparent-is-ignored-at-design-time"></a>BackColorTransparent est ignoré au moment du design  
 Le <xref:System.Windows.Forms.Integration.ElementHost.BackColorTransparent%2A> propriété ne peut pas fonctionner comme prévu au moment du design.  
  
 Si un contrôle WPF n’est pas sur un parent visible, le runtime WPF ignore la <xref:System.Windows.Forms.Integration.ElementHost.BackColorTransparent%2A> valeur. La raison qui <xref:System.Windows.Forms.Integration.ElementHost.BackColorTransparent%2A> peut être ignoré est parce que <xref:System.Windows.Forms.Integration.ElementHost> objet est créé dans une fonction <xref:System.AppDomain>. Toutefois, lorsque vous exécutez l’application, <xref:System.Windows.Forms.Integration.ElementHost.BackColorTransparent%2A> ne fonctionne pas comme prévu.  
  
### <a name="design-time-error-list-appears-when-the-obj-folder-is-deleted"></a>La liste d’erreurs au moment du design apparaît quand le dossier obj est supprimé  
 Si vous supprimez le dossier obj, la liste d’erreurs au moment du design s’affiche.  
  
 Lorsque vous concevez à l’aide de <xref:System.Windows.Forms.Integration.ElementHost>, le Concepteur de formulaires Windows utilise des fichiers générés dans le dossier Debug ou Release dans le dossier obj de votre projet. Si vous supprimez ces fichiers, la liste d’erreurs au moment du design apparaît. Pour résoudre ce problème, regénérez votre projet. Pour plus d’informations, consultez [Erreurs au moment du design dans le Concepteur Windows Forms](../../winforms/controls/design-time-errors-in-the-windows-forms-designer.md).  
  
<a name="elementhost_and_ime"></a>   
## <a name="elementhost-and-ime"></a>ElementHost et IME  
 Les contrôles WPF hébergés dans un <xref:System.Windows.Forms.Integration.ElementHost> ne gèrent pas la <xref:System.Windows.Forms.Control.ImeMode%2A> propriété. Modifications apportées à <xref:System.Windows.Forms.Control.ImeMode%2A> sera ignorée par les contrôles hébergés.  
  
## <a name="see-also"></a>Voir aussi

- <xref:System.Windows.Forms.Integration.ElementHost>
- <xref:System.Windows.Forms.Integration.WindowsFormsHost>
- [Interopérabilité dans le Concepteur WPF](https://docs.microsoft.com/previous-versions/visualstudio/visual-studio-2010/bb628658(v=vs.100))
- [Architecture d’entrée pour l’interopérabilité entre Windows Forms et WPF](windows-forms-and-wpf-interoperability-input-architecture.md)
- [Guide pratique pour Activer des Styles visuels dans une Application hybride](how-to-enable-visual-styles-in-a-hybrid-application.md)
- [Considérations sur la disposition de l’élément WindowsFormsHost](layout-considerations-for-the-windowsformshost-element.md)
- [Mappage de propriétés Windows Forms et WPF](windows-forms-and-wpf-property-mapping.md)
- [Erreurs au moment du design dans le Concepteur Windows Forms](../../winforms/controls/design-time-errors-in-the-windows-forms-designer.md)
- [Migration et interopérabilité](migration-and-interoperability.md)
