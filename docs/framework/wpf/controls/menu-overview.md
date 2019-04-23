---
title: Vue d'ensemble de Menu
ms.date: 03/30/2017
helpviewer_keywords:
- Menu control [WPF]
- controls [WPF], Menu
ms.assetid: 67df6de5-db96-4c71-b752-af90729a6537
ms.openlocfilehash: a3250cfd3fd651cb4ed3c4fd6975f5b5c89195f9
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59166372"
---
# <a name="menu-overview"></a>Vue d'ensemble de Menu
Le <xref:System.Windows.Controls.Menu> classe vous permet d’organiser les éléments associés aux commandes et gestionnaires d’événements dans un ordre hiérarchique. Chaque <xref:System.Windows.Controls.Menu> élément contient une collection de <xref:System.Windows.Controls.MenuItem> éléments.  

<a name="menu_control"></a>   
## <a name="menu-control"></a>Contrôle Menu  
 Le <xref:System.Windows.Controls.Menu> contrôle présente une liste des éléments qui spécifient des commandes ou des options pour une application. En règle générale, en cliquant sur un <xref:System.Windows.Controls.MenuItem> ouvre un sous-menu ou entraîne l’application à exécuter une commande.  
  
<a name="creating_menus"></a>   
## <a name="creating-menus"></a>Création de menus  
 L’exemple suivant crée un <xref:System.Windows.Controls.Menu> à manipuler du texte dans un <xref:System.Windows.Controls.TextBox>. Le <xref:System.Windows.Controls.Menu> contient <xref:System.Windows.Controls.MenuItem> objets qui utilisent le <xref:System.Windows.Controls.MenuItem.Command%2A>, <xref:System.Windows.Controls.MenuItem.IsCheckable%2A>, et <xref:System.Windows.Controls.HeaderedItemsControl.Header%2A> propriétés et le <xref:System.Windows.Controls.MenuItem.Checked>, <xref:System.Windows.Controls.MenuItem.Unchecked>, et <xref:System.Windows.Controls.MenuItem.Click> événements.  
  
 [!code-xaml[MenuItemCommandsAndEvents#1](~/samples/snippets/csharp/VS_Snippets_Wpf/MenuItemCommandsAndEvents/CSharp/Window1.xaml#1)]  
  
 [!code-csharp[MenuItemCommandsAndEvents#2](~/samples/snippets/csharp/VS_Snippets_Wpf/MenuItemCommandsAndEvents/CSharp/Window1.xaml.cs#2)]
 [!code-vb[MenuItemCommandsAndEvents#2](~/samples/snippets/visualbasic/VS_Snippets_Wpf/MenuItemCommandsAndEvents/VisualBasic/Window1.xaml.vb#2)]  
  
<a name="menus_with_shortcutkeys"></a>   
## <a name="menuitems-with-keyboard-shortcuts"></a>MenuItems avec raccourcis clavier  
 Raccourcis clavier sont des combinaisons de caractères qui peuvent être entrés avec le clavier pour appeler <xref:System.Windows.Controls.Menu> commandes. Par exemple, le raccourci clavier de la **copie** est CTRL+C. Il existe deux propriétés à utiliser avec les raccourcis clavier et les éléments de menu :<xref:System.Windows.Controls.MenuItem.InputGestureText%2A> ou <xref:System.Windows.Controls.MenuItem.Command%2A>.  
  
<a name="menus_inputgesturetext"></a>   
### <a name="inputgesturetext"></a>InputGestureText  
 L’exemple suivant montre comment utiliser le <xref:System.Windows.Controls.MenuItem.InputGestureText%2A> propriété à attribuer le texte de raccourci clavier à <xref:System.Windows.Controls.MenuItem> contrôles. Cette opération ne fait que placer le raccourci clavier dans l’élément de menu.  Il n’associe pas la commande avec le <xref:System.Windows.Controls.MenuItem>. L’application doit gérer l’entrée de l’utilisateur pour exécuter l’action.  
  
 [!code-xaml[MenuEvent#6](~/samples/snippets/csharp/VS_Snippets_Wpf/MenuEvent/CSharp/Pane1.xaml#6)]  
  
<a name="menus_commands"></a>   
### <a name="command"></a>Commande  
 L’exemple suivant montre comment utiliser le <xref:System.Windows.Controls.MenuItem.Command%2A> propriété à associer le **Open** et **enregistrer** commandes avec <xref:System.Windows.Controls.MenuItem> contrôles. Non seulement la propriété de la commande associer une commande avec un <xref:System.Windows.Controls.MenuItem>, mais elle fournit également le texte de mouvement d’entrée à utiliser comme un raccourci.  
  
 [!code-xaml[MenuEvent#8](~/samples/snippets/csharp/VS_Snippets_Wpf/MenuEvent/CSharp/Pane1.xaml#8)]  
  
 Le <xref:System.Windows.Controls.MenuItem> classe a également un <xref:System.Windows.Controls.MenuItem.CommandTarget%2A> propriété qui spécifie l’élément où la commande se produit. Si <xref:System.Windows.Controls.MenuItem.CommandTarget%2A> n’est pas défini, l’élément qui a le focus clavier reçoit la commande. Pour plus d’informations sur les commandes, consultez [Vue d’ensemble des commandes](../advanced/commanding-overview.md).  
  
<a name="menu_styling"></a>   
## <a name="menu-styling"></a>Styles de menu  
 Avec les styles de contrôle, vous pouvez modifier considérablement l’apparence et le comportement de <xref:System.Windows.Controls.Menu> contrôles sans devoir écrire un contrôle personnalisé. Outre la définition des propriétés visuelles, vous pouvez également appliquer un <xref:System.Windows.Style> aux parties individuelles d’un contrôle, modifier le comportement de parties du contrôle via les propriétés, ou ajouter des parties supplémentaires ou modifier la disposition d’un contrôle. Les exemples suivants illustrent plusieurs façons d’ajouter un <xref:System.Windows.Style> à un <xref:System.Windows.Controls.Menu> contrôle.  
  
 Le premier exemple de code définit un <xref:System.Windows.Style> appelée `Simple` qui montre comment utiliser les paramètres système actuels dans votre style. Le code assigne la couleur du pinceau `MenuHighlightBrush` comme couleur d’arrière-plan du menu et celle du pinceau `MenuTextBrush` comme couleur de premier plan du menu. Notez que vous utilisez des clés de ressource pour assigner les pinceaux.  
  
 [!code-xaml[MenuStylesSnippet#1](~/samples/snippets/csharp/VS_Snippets_Wpf/MenuStylesSnippet/CS/app.xaml#1)]  
  
 L’exemple suivant utilise <xref:System.Windows.Trigger> les éléments qui vous permettent de modifier l’apparence d’un <xref:System.Windows.Controls.MenuItem> en réponse aux événements qui se produisent sur le <xref:System.Windows.Controls.Menu>. Lorsque vous déplacez la souris sur le <xref:System.Windows.Controls.Menu>, la couleur de premier plan et les caractéristiques de police des éléments de menu Modifier.  
  
 [!code-xaml[MenuStylesSnippet#2](~/samples/snippets/csharp/VS_Snippets_Wpf/MenuStylesSnippet/CS/app.xaml#2)]  
  
## <a name="see-also"></a>Voir aussi

- [Exemple de galerie de contrôles WPF](https://go.microsoft.com/fwlink/?LinkID=160053)
