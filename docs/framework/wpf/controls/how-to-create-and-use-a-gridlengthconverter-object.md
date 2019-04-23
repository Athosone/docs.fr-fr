---
title: 'Procédure : Créer et utiliser un objet GridLengthConverter'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- Grid control [WPF], creating [WPF], GridLengthConverter objects
ms.assetid: 5ab75911-e36a-4825-80e4-081c57e8e182
ms.openlocfilehash: 498d2b9c531f391f4cbeb1478469a99d381deec7
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59770765"
---
# <a name="how-to-create-and-use-a-gridlengthconverter-object"></a><span data-ttu-id="69247-102">Procédure : Créer et utiliser un objet GridLengthConverter</span><span class="sxs-lookup"><span data-stu-id="69247-102">How to: Create and Use a GridLengthConverter Object</span></span>
## <a name="example"></a><span data-ttu-id="69247-103">Exemple</span><span class="sxs-lookup"><span data-stu-id="69247-103">Example</span></span>  
 <span data-ttu-id="69247-104">L’exemple suivant montre comment créer et utiliser une instance de <xref:System.Windows.GridLengthConverter>.</span><span class="sxs-lookup"><span data-stu-id="69247-104">The following example shows how to create and use an instance of <xref:System.Windows.GridLengthConverter>.</span></span> <span data-ttu-id="69247-105">L’exemple définit une méthode personnalisée nommée `changeCol`, qui passe le <xref:System.Windows.Controls.ListBoxItem> à un <xref:System.Windows.GridLengthConverter> qui convertit le <xref:System.Windows.Controls.ContentControl.Content%2A> d’un <xref:System.Windows.Controls.ListBoxItem> à une instance de <xref:System.Windows.GridLength>.</span><span class="sxs-lookup"><span data-stu-id="69247-105">The example defines a custom method called `changeCol`, which passes the <xref:System.Windows.Controls.ListBoxItem> to a <xref:System.Windows.GridLengthConverter> that converts the <xref:System.Windows.Controls.ContentControl.Content%2A> of a <xref:System.Windows.Controls.ListBoxItem> to an instance of <xref:System.Windows.GridLength>.</span></span> <span data-ttu-id="69247-106">La valeur convertie est ensuite passée comme valeur de la <xref:System.Windows.Controls.ColumnDefinition.Width%2A> propriété de la <xref:System.Windows.Controls.ColumnDefinition> élément.</span><span class="sxs-lookup"><span data-stu-id="69247-106">The converted value is then passed back as the value of the <xref:System.Windows.Controls.ColumnDefinition.Width%2A> property of the <xref:System.Windows.Controls.ColumnDefinition> element.</span></span>  
  
 <span data-ttu-id="69247-107">L’exemple définit également une deuxième méthode personnalisée, appelée `changeColVal`.</span><span class="sxs-lookup"><span data-stu-id="69247-107">The example also defines a second custom method, called `changeColVal`.</span></span> <span data-ttu-id="69247-108">Cette méthode personnalisée convertit le <xref:System.Windows.Controls.Primitives.RangeBase.Value%2A> d’un <xref:System.Windows.Controls.Slider> à un <xref:System.String> puis passe cette valeur à la <xref:System.Windows.Controls.ColumnDefinition> en tant que le <xref:System.Windows.Controls.ColumnDefinition.Width%2A> de l’élément.</span><span class="sxs-lookup"><span data-stu-id="69247-108">This custom method converts the <xref:System.Windows.Controls.Primitives.RangeBase.Value%2A> of a <xref:System.Windows.Controls.Slider> to a <xref:System.String> and then passes that value back to the <xref:System.Windows.Controls.ColumnDefinition> as the <xref:System.Windows.Controls.ColumnDefinition.Width%2A> of the element.</span></span>  
  
 <span data-ttu-id="69247-109">Notez que distinct [!INCLUDE[TLA#tla_xaml](../../../../includes/tlasharptla-xaml-md.md)] fichier définit le contenu d’un <xref:System.Windows.Controls.ListBoxItem>.</span><span class="sxs-lookup"><span data-stu-id="69247-109">Note that a separate [!INCLUDE[TLA#tla_xaml](../../../../includes/tlasharptla-xaml-md.md)] file defines the contents of a <xref:System.Windows.Controls.ListBoxItem>.</span></span>  
  
 [!code-csharp[gridlengthConverterGrid#1](~/samples/snippets/csharp/VS_Snippets_Wpf/gridlengthConverterGrid/CSharp/Window1.xaml.cs#1)]
 [!code-vb[gridlengthConverterGrid#1](~/samples/snippets/visualbasic/VS_Snippets_Wpf/gridlengthConverterGrid/VisualBasic/Window1.xaml.vb#1)]  
  
## <a name="see-also"></a><span data-ttu-id="69247-110">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="69247-110">See also</span></span>

- <xref:System.Windows.GridLengthConverter>
- <xref:System.Windows.GridLength>
