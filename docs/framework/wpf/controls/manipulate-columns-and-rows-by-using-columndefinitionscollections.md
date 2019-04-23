---
title: 'Procédure : Manipuler des colonnes et des lignes à l’aide de ColumnDefinitionsCollections et RowDefinitionsCollections'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- controls [WPF], Grid class
- Grid control [WPF], ColumnDefinitionCollection class
- Grid control [WPF], RowDefinitionCollection class
ms.assetid: bfc7160a-45f2-4e17-9961-df414dfb13c5
ms.openlocfilehash: f316cced076223edba1d39c9cfb21b9a504b9eee
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/22/2019
ms.locfileid: "59978274"
---
# <a name="how-to-manipulate-columns-and-rows-by-using-columndefinitionscollections-and-rowdefinitionscollections"></a><span data-ttu-id="60de7-102">Procédure : Manipuler des colonnes et des lignes à l’aide de ColumnDefinitionsCollections et RowDefinitionsCollections</span><span class="sxs-lookup"><span data-stu-id="60de7-102">How to: Manipulate Columns and Rows by Using ColumnDefinitionsCollections and RowDefinitionsCollections</span></span>
<span data-ttu-id="60de7-103">Cet exemple montre comment utiliser les méthodes dans le <xref:System.Windows.Controls.ColumnDefinitionCollection> et <xref:System.Windows.Controls.RowDefinitionCollection> classes pour effectuer des actions comme ajouter, effacer ou compter le contenu de lignes ou colonnes.</span><span class="sxs-lookup"><span data-stu-id="60de7-103">This example shows how to use the methods in the <xref:System.Windows.Controls.ColumnDefinitionCollection> and <xref:System.Windows.Controls.RowDefinitionCollection> classes to perform actions like adding, clearing, or counting the contents of rows or columns.</span></span> <span data-ttu-id="60de7-104">Par exemple, vous pouvez <xref:System.Windows.Controls.ColumnDefinitionCollection.Add%2A>, <xref:System.Windows.Controls.ColumnDefinitionCollection.Clear%2A>, ou <xref:System.Windows.Controls.ColumnDefinitionCollection.Count%2A> les éléments qui sont inclus dans un <xref:System.Windows.Controls.ColumnDefinition> ou <xref:System.Windows.Controls.RowDefinition>.</span><span class="sxs-lookup"><span data-stu-id="60de7-104">For example, you can <xref:System.Windows.Controls.ColumnDefinitionCollection.Add%2A>, <xref:System.Windows.Controls.ColumnDefinitionCollection.Clear%2A>, or <xref:System.Windows.Controls.ColumnDefinitionCollection.Count%2A> the items that are included in a <xref:System.Windows.Controls.ColumnDefinition> or <xref:System.Windows.Controls.RowDefinition>.</span></span>  
  
## <a name="example"></a><span data-ttu-id="60de7-105">Exemple</span><span class="sxs-lookup"><span data-stu-id="60de7-105">Example</span></span>  
 <span data-ttu-id="60de7-106">L’exemple suivant crée un <xref:System.Windows.Controls.Grid> élément avec un <xref:System.Windows.FrameworkElement.Name%2A> de `grid1`.</span><span class="sxs-lookup"><span data-stu-id="60de7-106">The following example creates a <xref:System.Windows.Controls.Grid> element with a <xref:System.Windows.FrameworkElement.Name%2A> of `grid1`.</span></span> <span data-ttu-id="60de7-107">Le <xref:System.Windows.Controls.Grid> contient un <xref:System.Windows.Controls.StackPanel> contenant <xref:System.Windows.Controls.Button> éléments, chacun étant contrôlé par une méthode de collection différente.</span><span class="sxs-lookup"><span data-stu-id="60de7-107">The <xref:System.Windows.Controls.Grid> contains a <xref:System.Windows.Controls.StackPanel> that holds <xref:System.Windows.Controls.Button> elements, each controlled by a different collection method.</span></span> <span data-ttu-id="60de7-108">Lorsque vous cliquez sur un <xref:System.Windows.Controls.Button>, il active un appel de méthode dans le fichier code-behind.</span><span class="sxs-lookup"><span data-stu-id="60de7-108">When you click a <xref:System.Windows.Controls.Button>, it activates a method call in the code-behind file.</span></span>  
  
 [!code-xaml[ColumnDefinitionsGrid#1](~/samples/snippets/csharp/VS_Snippets_Wpf/ColumnDefinitionsGrid/CSharp/Window1.xaml#1)]  
  
 <span data-ttu-id="60de7-109">Cet exemple définit une série de méthodes personnalisées, correspondant chacune à un <xref:System.Windows.Controls.Primitives.ButtonBase.Click> événement dans le [!INCLUDE[TLA#tla_xaml](../../../../includes/tlasharptla-xaml-md.md)] fichier.</span><span class="sxs-lookup"><span data-stu-id="60de7-109">This example defines a series of custom methods, each corresponding to a <xref:System.Windows.Controls.Primitives.ButtonBase.Click> event in the [!INCLUDE[TLA#tla_xaml](../../../../includes/tlasharptla-xaml-md.md)] file.</span></span> <span data-ttu-id="60de7-110">Vous pouvez modifier le nombre de colonnes et lignes dans le <xref:System.Windows.Controls.Grid> de plusieurs façons, qui comprend l’ajout ou suppression des lignes et des colonnes ; et en comptant le nombre total de lignes et colonnes.</span><span class="sxs-lookup"><span data-stu-id="60de7-110">You can change the number of columns and rows in the <xref:System.Windows.Controls.Grid> in several ways, which includes adding or removing rows and columns; and counting the total number of rows and columns.</span></span> <span data-ttu-id="60de7-111">Pour empêcher <xref:System.ArgumentOutOfRangeException> et <xref:System.ArgumentException> exceptions, vous pouvez utiliser la fonctionnalité de vérification des erreurs qui le <xref:System.Windows.Controls.ColumnDefinitionCollection.RemoveRange%2A> fournit de la méthode.</span><span class="sxs-lookup"><span data-stu-id="60de7-111">To prevent <xref:System.ArgumentOutOfRangeException> and <xref:System.ArgumentException> exceptions, you can use the error-checking functionality that the <xref:System.Windows.Controls.ColumnDefinitionCollection.RemoveRange%2A> method provides.</span></span>  
  
 [!code-csharp[ColumnDefinitionsGrid#2](~/samples/snippets/csharp/VS_Snippets_Wpf/ColumnDefinitionsGrid/CSharp/Window1.xaml.cs#2)]
 [!code-vb[ColumnDefinitionsGrid#2](~/samples/snippets/visualbasic/VS_Snippets_Wpf/ColumnDefinitionsGrid/VisualBasic/Window1.xaml.vb#2)]  
  
## <a name="see-also"></a><span data-ttu-id="60de7-112">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="60de7-112">See also</span></span>

- <xref:System.Windows.Controls.Grid>
- <xref:System.Windows.Controls.ColumnDefinitionCollection>
- <xref:System.Windows.Controls.RowDefinitionCollection>
