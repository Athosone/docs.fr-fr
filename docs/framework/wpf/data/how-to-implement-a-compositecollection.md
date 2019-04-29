---
title: 'Procédure : Implémenter une classe CompositeCollection'
ms.date: 03/30/2017
helpviewer_keywords:
- data binding [WPF], CompositeCollection class
ms.assetid: 0d8fc84c-7920-427f-8ad7-d55ca656c170
ms.openlocfilehash: 8361c2bfa9c125aeadf0a62ca86af1855e5c3dbc
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61931674"
---
# <a name="how-to-implement-a-compositecollection"></a><span data-ttu-id="5ca9d-102">Procédure : Implémenter une classe CompositeCollection</span><span class="sxs-lookup"><span data-stu-id="5ca9d-102">How to: Implement a CompositeCollection</span></span>
## <a name="example"></a><span data-ttu-id="5ca9d-103">Exemple</span><span class="sxs-lookup"><span data-stu-id="5ca9d-103">Example</span></span>  
 <span data-ttu-id="5ca9d-104">L’exemple suivant montre comment afficher plusieurs collections et éléments comme une liste à l’aide la <xref:System.Windows.Data.CompositeCollection> classe.</span><span class="sxs-lookup"><span data-stu-id="5ca9d-104">The following example shows how to display multiple collections and items as one list using the <xref:System.Windows.Data.CompositeCollection> class.</span></span> <span data-ttu-id="5ca9d-105">Dans cet exemple, `GreekGods` est un <xref:System.Collections.ObjectModel.ObservableCollection%601> de `GreekGod` des objets personnalisés.</span><span class="sxs-lookup"><span data-stu-id="5ca9d-105">In this example, `GreekGods` is an <xref:System.Collections.ObjectModel.ObservableCollection%601> of `GreekGod` custom objects.</span></span> <span data-ttu-id="5ca9d-106">Modèles de données sont définies afin que `GreekGod` objets et `GreekHero` objets apparaissent avec un OR et une couleur de premier plan cyan, respectivement.</span><span class="sxs-lookup"><span data-stu-id="5ca9d-106">Data templates are defined so that `GreekGod` objects and `GreekHero` objects appear with a gold and a cyan foreground color respectively.</span></span>  
  
 [!code-xaml[CompositeCollections#1](~/samples/snippets/csharp/VS_Snippets_Wpf/CompositeCollections/CS/Window1.xaml#1)]  
  
## <a name="see-also"></a><span data-ttu-id="5ca9d-107">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="5ca9d-107">See also</span></span>

- <xref:System.Windows.Data.CollectionContainer>
- <xref:System.Windows.Controls.ItemsControl.ItemsSource%2A>
- <xref:System.Windows.Data.XmlDataProvider>
- <xref:System.Windows.DataTemplate>
- [<span data-ttu-id="5ca9d-108">Vue d’ensemble de la liaison de données</span><span class="sxs-lookup"><span data-stu-id="5ca9d-108">Data Binding Overview</span></span>](data-binding-overview.md)
- [<span data-ttu-id="5ca9d-109">Rubriques de guide pratique</span><span class="sxs-lookup"><span data-stu-id="5ca9d-109">How-to Topics</span></span>](data-binding-how-to-topics.md)
