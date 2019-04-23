---
title: 'Procédure : Utiliser la classe FontSizeConverter'
ms.date: 03/30/2017
helpviewer_keywords:
- FontSizeConverter objects [WPF]
- typography [WPF], FontSizeConverter objects
ms.assetid: 3b0592bd-7223-4860-a108-a5d72f3a9178
ms.openlocfilehash: f33a297ae07d5509d2b4d9a98636086ac433a57f
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/22/2019
ms.locfileid: "59979353"
---
# <a name="how-to-use-the-fontsizeconverter-class"></a><span data-ttu-id="80734-102">Procédure : Utiliser la classe FontSizeConverter</span><span class="sxs-lookup"><span data-stu-id="80734-102">How to: Use the FontSizeConverter Class</span></span>
## <a name="example"></a><span data-ttu-id="80734-103">Exemple</span><span class="sxs-lookup"><span data-stu-id="80734-103">Example</span></span>  
 <span data-ttu-id="80734-104">Cet exemple montre comment créer une instance de <xref:System.Windows.FontSizeConverter> et l’utiliser pour modifier une taille de police.</span><span class="sxs-lookup"><span data-stu-id="80734-104">This example shows how to create an instance of <xref:System.Windows.FontSizeConverter> and use it to change a font size.</span></span>  
  
 <span data-ttu-id="80734-105">L’exemple définit une méthode personnalisée nommée `changeSize` qui convertit le contenu d’un <xref:System.Windows.Controls.ListBoxItem>, tel que défini dans une fonction [!INCLUDE[TLA#tla_xaml](../../../../includes/tlasharptla-xaml-md.md)] fichier, à une instance de <xref:System.Double>et par la suite en un <xref:System.String>.</span><span class="sxs-lookup"><span data-stu-id="80734-105">The example defines a custom method called `changeSize` that converts the contents of a <xref:System.Windows.Controls.ListBoxItem>, as defined in a separate [!INCLUDE[TLA#tla_xaml](../../../../includes/tlasharptla-xaml-md.md)] file, to an instance of <xref:System.Double>, and later into a <xref:System.String>.</span></span> <span data-ttu-id="80734-106">Cette méthode passe le <xref:System.Windows.Controls.ListBoxItem> à un <xref:System.Windows.FontSizeConverter> objet, qui convertit le <xref:System.Windows.Controls.ContentControl.Content%2A> d’un <xref:System.Windows.Controls.ListBoxItem> à une instance de <xref:System.Double>.</span><span class="sxs-lookup"><span data-stu-id="80734-106">This method passes the <xref:System.Windows.Controls.ListBoxItem> to a <xref:System.Windows.FontSizeConverter> object, which converts the <xref:System.Windows.Controls.ContentControl.Content%2A> of a <xref:System.Windows.Controls.ListBoxItem> to an instance of <xref:System.Double>.</span></span> <span data-ttu-id="80734-107">Cette valeur est ensuite retournée comme la valeur de la <xref:System.Windows.Controls.TextBlock.FontSize%2A> propriété de la <xref:System.Windows.Controls.TextBlock> élément.</span><span class="sxs-lookup"><span data-stu-id="80734-107">This value is then passed back as the value of the <xref:System.Windows.Controls.TextBlock.FontSize%2A> property of the <xref:System.Windows.Controls.TextBlock> element.</span></span>  
  
 <span data-ttu-id="80734-108">Cet exemple définit également une deuxième méthode personnalisée qui est appelée `changeFamily`.</span><span class="sxs-lookup"><span data-stu-id="80734-108">This example also defines a second custom method that is called `changeFamily`.</span></span> <span data-ttu-id="80734-109">Cette méthode convertit le <xref:System.Windows.Controls.ContentControl.Content%2A> de la <xref:System.Windows.Controls.ListBoxItem> à un <xref:System.String>, puis passe cette valeur à la <xref:System.Windows.Controls.TextBlock.FontFamily%2A> propriété de la <xref:System.Windows.Controls.TextBlock> élément.</span><span class="sxs-lookup"><span data-stu-id="80734-109">This method converts the <xref:System.Windows.Controls.ContentControl.Content%2A> of the <xref:System.Windows.Controls.ListBoxItem> to a <xref:System.String>, and then passes that value to the <xref:System.Windows.Controls.TextBlock.FontFamily%2A> property of the <xref:System.Windows.Controls.TextBlock> element.</span></span>  
  
 <span data-ttu-id="80734-110">Cet exemple ne s’exécute pas.</span><span class="sxs-lookup"><span data-stu-id="80734-110">This example does not run.</span></span>  
  
 [!code-csharp[FontSizeConverter#1](~/samples/snippets/csharp/VS_Snippets_Wpf/FontSizeConverter/CSharp/Window1.xaml.cs#1)]  
  
## <a name="see-also"></a><span data-ttu-id="80734-111">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="80734-111">See also</span></span>

- <xref:System.Windows.FontSizeConverter>
