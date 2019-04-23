---
title: 'Procédure : Implémenter ICommandSource'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- ICommandSource interfaces [WPF], implementing
ms.assetid: 7452dd39-6e11-44bf-806a-31d87f3772ac
ms.openlocfilehash: 218a17f221598ac29213bd28a0f04adb16bc933b
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59107365"
---
# <a name="how-to-implement-icommandsource"></a>Procédure : Implémenter ICommandSource
Cet exemple montre comment créer une source de commande en implémentant <xref:System.Windows.Input.ICommandSource>.  Une source de commande est un objet qui sait comment appeler une commande.  Le <xref:System.Windows.Input.ICommandSource> interface expose trois membres : <xref:System.Windows.Input.ICommandSource.Command%2A>, <xref:System.Windows.Input.ICommandSource.CommandParameter%2A>, et <xref:System.Windows.Input.ICommandSource.CommandTarget%2A>.  <xref:System.Windows.Input.ICommandSource.Command%2A> est la commande qui sera appelée. Le <xref:System.Windows.Input.ICommandSource.CommandParameter%2A> est un type de données défini par l’utilisateur qui est passé à partir de la source de commande à la méthode qui gère la commande. Le <xref:System.Windows.Input.ICommandSource.CommandTarget%2A> est l’objet qui est en cours d’exécution sur la commande.  
  
 Dans cet exemple, une classe est créée qui sous-classe la <xref:System.Windows.Controls.Slider> contrôle et implémente <xref:System.Windows.Input.ICommandSource>.  
  
## <a name="example"></a>Exemple  
 [!INCLUDE[TLA2#tla_winclient](../../../../includes/tla2sharptla-winclient-md.md)] fournit un certain nombre de classes qui implémentent <xref:System.Windows.Input.ICommandSource>, tel que <xref:System.Windows.Controls.Button>, <xref:System.Windows.Controls.MenuItem>, et <xref:System.Windows.Controls.ListBoxItem>.  Une source de commande définit comment appeler une commande.   <xref:System.Windows.Controls.Button> et <xref:System.Windows.Controls.MenuItem> appeler une commande lorsque vous cliquez dessus.  Un <xref:System.Windows.Controls.ListBoxItem> appelle une commande lorsque double-clique dessus. Ces classes ne deviennent une commande source quand leur <xref:System.Windows.Input.ICommandSource.Command%2A> propriété est définie.  
  
 Pour cet exemple, nous appellerons la commande lorsque le curseur est déplacé, ou plus précisément, lorsque le <xref:System.Windows.Controls.Primitives.RangeBase.Value%2A> propriété est modifiée.  
  
 Voici la définition de classe.  
  
 [!code-csharp[ImplementICommandSource#ImplementICommandSourceClassDefinition](~/samples/snippets/csharp/VS_Snippets_Wpf/ImplementICommandSource/CSharp/CommandSlider.cs#implementicommandsourceclassdefinition)]
 [!code-vb[ImplementICommandSource#ImplementICommandSourceClassDefinition](~/samples/snippets/visualbasic/VS_Snippets_Wpf/ImplementICommandSource/visualbasic/commandslider.vb#implementicommandsourceclassdefinition)]  
  
 L’étape suivante consiste à implémenter le <xref:System.Windows.Input.ICommandSource> membres.  Dans cet exemple, les propriétés sont implémentées comme <xref:System.Windows.DependencyProperty> objets.  Ainsi, les propriétés à utiliser la liaison de données.  Pour plus d’informations sur la <xref:System.Windows.DependencyProperty> de classe, consultez le [vue d’ensemble des propriétés de dépendance](dependency-properties-overview.md).  Pour plus d’informations sur la liaison de données, consultez le [vue d’ensemble de la liaison de données](../data/data-binding-overview.md).  
  
 Uniquement la <xref:System.Windows.Input.ICommandSource.Command%2A> propriété est indiquée ici.  
  
 [!code-csharp[ImplementICommandSource#ImplementICommandSourceCommandPropertyDefinition](~/samples/snippets/csharp/VS_Snippets_Wpf/ImplementICommandSource/CSharp/CommandSlider.cs#implementicommandsourcecommandpropertydefinition)]
 [!code-vb[ImplementICommandSource#ImplementICommandSourceCommandPropertyDefinition](~/samples/snippets/visualbasic/VS_Snippets_Wpf/ImplementICommandSource/visualbasic/commandslider.vb#implementicommandsourcecommandpropertydefinition)]  
  
 Voici le <xref:System.Windows.DependencyProperty> modifier le rappel.  
  
 [!code-csharp[ImplementICommandSource#ImplementICommandSourceCommandChanged](~/samples/snippets/csharp/VS_Snippets_Wpf/ImplementICommandSource/CSharp/CommandSlider.cs#implementicommandsourcecommandchanged)]
 [!code-vb[ImplementICommandSource#ImplementICommandSourceCommandChanged](~/samples/snippets/visualbasic/VS_Snippets_Wpf/ImplementICommandSource/visualbasic/commandslider.vb#implementicommandsourcecommandchanged)]  
  
 L’étape suivante consiste à ajouter et supprimer la commande qui est associée à la source de commande.  Le <xref:System.Windows.Input.ICommandSource.Command%2A> propriété ne peut pas être remplacée simplement une nouvelle commande est ajoutée, car les gestionnaires d’événements associés à la commande précédente, le cas échéant, doivent être supprimés en premier.  
  
 [!code-csharp[ImplementICommandSource#ImplementICommandSourceHookUnHookCommands](~/samples/snippets/csharp/VS_Snippets_Wpf/ImplementICommandSource/CSharp/CommandSlider.cs#implementicommandsourcehookunhookcommands)]
 [!code-vb[ImplementICommandSource#ImplementICommandSourceHookUnHookCommands](~/samples/snippets/visualbasic/VS_Snippets_Wpf/ImplementICommandSource/visualbasic/commandslider.vb#implementicommandsourcehookunhookcommands)]  
  
 La dernière étape consiste à créer la logique pour le <xref:System.Windows.Input.ICommand.CanExecuteChanged> gestionnaire et le <xref:System.Windows.Input.ICommand.Execute%2A> (méthode).  
  
 Le <xref:System.Windows.Input.ICommand.CanExecuteChanged> événements informe la source de commande que la capacité de la commande à exécuter sur la cible de commande actuelle a peut-être changé.  Lorsqu’une source de commande reçoit cet événement, elle appelle généralement la <xref:System.Windows.Input.ICommand.CanExecute%2A> méthode sur la commande.  Si la commande ne peut pas s’exécuter sur la cible de commande actuelle, la source de commande est généralement désactivée.  Si la commande peut s’exécuter sur la cible de commande actuelle, la source de commande permettra généralement lui-même.  
  
 [!code-csharp[ImplementICommandSource#ImplementICommandCanExecuteChanged](~/samples/snippets/csharp/VS_Snippets_Wpf/ImplementICommandSource/CSharp/CommandSlider.cs#implementicommandcanexecutechanged)]
 [!code-vb[ImplementICommandSource#ImplementICommandCanExecuteChanged](~/samples/snippets/visualbasic/VS_Snippets_Wpf/ImplementICommandSource/visualbasic/commandslider.vb#implementicommandcanexecutechanged)]  
  
 La dernière étape est la <xref:System.Windows.Input.ICommand.Execute%2A> (méthode).  Si la commande est un <xref:System.Windows.Input.RoutedCommand>, le <xref:System.Windows.Input.RoutedCommand> <xref:System.Windows.Input.RoutedCommand.Execute%2A> méthode est appelée ; sinon, le <xref:System.Windows.Input.ICommand> <xref:System.Windows.Input.ICommand.Execute%2A> méthode est appelée.  
  
 [!code-csharp[ImplementICommandSource#ImplementICommandExecute](~/samples/snippets/csharp/VS_Snippets_Wpf/ImplementICommandSource/CSharp/CommandSlider.cs#implementicommandexecute)]
 [!code-vb[ImplementICommandSource#ImplementICommandExecute](~/samples/snippets/visualbasic/VS_Snippets_Wpf/ImplementICommandSource/visualbasic/commandslider.vb#implementicommandexecute)]  
  
## <a name="see-also"></a>Voir aussi

- <xref:System.Windows.Input.ICommandSource>
- <xref:System.Windows.Input.ICommand>
- <xref:System.Windows.Input.RoutedCommand>
- [Vue d’ensemble des commandes](commanding-overview.md)
