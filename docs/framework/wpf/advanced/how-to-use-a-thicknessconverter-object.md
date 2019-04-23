---
title: 'Procédure : Utiliser un objet ThicknessConverter'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- border thickness [WPF]
- ThicknessConverter objects [WPF]
ms.assetid: 52682194-d7fd-499c-8005-73fcc84e7b2c
ms.openlocfilehash: ebfb8642a01f6d602f4e5ffa58fde6a8ee0b4e1f
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59075949"
---
# <a name="how-to-use-a-thicknessconverter-object"></a><span data-ttu-id="bd625-102">Procédure : Utiliser un objet ThicknessConverter</span><span class="sxs-lookup"><span data-stu-id="bd625-102">How to: Use a ThicknessConverter Object</span></span>
## <a name="example"></a><span data-ttu-id="bd625-103">Exemple</span><span class="sxs-lookup"><span data-stu-id="bd625-103">Example</span></span>  
 <span data-ttu-id="bd625-104">Cet exemple montre comment créer une instance de <xref:System.Windows.ThicknessConverter> et l’utiliser pour modifier l’épaisseur d’une bordure.</span><span class="sxs-lookup"><span data-stu-id="bd625-104">This example shows how to create an instance of <xref:System.Windows.ThicknessConverter> and use it to change the thickness of a border.</span></span>  
  
 <span data-ttu-id="bd625-105">L’exemple définit une méthode personnalisée nommée `changeThickness`; cette méthode convertit d’abord le contenu d’un <xref:System.Windows.Controls.ListBoxItem>, tel que défini dans une fonction [!INCLUDE[TLA#tla_xaml](../../../../includes/tlasharptla-xaml-md.md)] fichier, à une instance de <xref:System.Windows.Thickness>et plus tard convertit le contenu dans un <xref:System.String>.</span><span class="sxs-lookup"><span data-stu-id="bd625-105">The example defines a custom method called `changeThickness`; this method first converts the contents of a <xref:System.Windows.Controls.ListBoxItem>, as defined in a separate [!INCLUDE[TLA#tla_xaml](../../../../includes/tlasharptla-xaml-md.md)] file, to an instance of <xref:System.Windows.Thickness>, and later converts the content into a <xref:System.String>.</span></span> <span data-ttu-id="bd625-106">Cette méthode passe le <xref:System.Windows.Controls.ListBoxItem> à un <xref:System.Windows.ThicknessConverter> objet, qui convertit le <xref:System.Windows.Controls.ContentControl.Content%2A> d’un <xref:System.Windows.Controls.ListBoxItem> à une instance de <xref:System.Windows.Thickness>.</span><span class="sxs-lookup"><span data-stu-id="bd625-106">This method passes the <xref:System.Windows.Controls.ListBoxItem> to a <xref:System.Windows.ThicknessConverter> object, which converts the <xref:System.Windows.Controls.ContentControl.Content%2A> of a <xref:System.Windows.Controls.ListBoxItem> to an instance of <xref:System.Windows.Thickness>.</span></span> <span data-ttu-id="bd625-107">Cette valeur est ensuite retournée comme la valeur de la <xref:System.Windows.Controls.Border.BorderThickness%2A> propriété de la <xref:System.Windows.Controls.Border>.</span><span class="sxs-lookup"><span data-stu-id="bd625-107">This value is then passed back as the value of the <xref:System.Windows.Controls.Border.BorderThickness%2A> property of the <xref:System.Windows.Controls.Border>.</span></span>  
  
 <span data-ttu-id="bd625-108">Cet exemple ne s’exécute pas.</span><span class="sxs-lookup"><span data-stu-id="bd625-108">This example does not run.</span></span>  
  
 [!code-csharp[ThicknessConverter#1](~/samples/snippets/csharp/VS_Snippets_Wpf/ThicknessConverter/CSharp/Window1.xaml.cs#1)]
 [!code-vb[ThicknessConverter#1](~/samples/snippets/visualbasic/VS_Snippets_Wpf/ThicknessConverter/VisualBasic/Window1.xaml.vb#1)]  
  
## <a name="see-also"></a><span data-ttu-id="bd625-109">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="bd625-109">See also</span></span>

- <xref:System.Windows.Thickness>
- <xref:System.Windows.ThicknessConverter>
- <xref:System.Windows.Controls.Border>
- <span data-ttu-id="bd625-110">[Guide pratique pour Modifier la propriété Margin](https://docs.microsoft.com/previous-versions/dotnet/netframework-3.5/ms750561(v=vs.90))</span><span class="sxs-lookup"><span data-stu-id="bd625-110">[How to: Change the Margin Property](https://docs.microsoft.com/previous-versions/dotnet/netframework-3.5/ms750561(v=vs.90))</span></span>
- <span data-ttu-id="bd625-111">[Guide pratique pour Convertir un ListBoxItem en un nouveau Type de données](https://docs.microsoft.com/previous-versions/dotnet/netframework-3.5/ms749147(v=vs.90))</span><span class="sxs-lookup"><span data-stu-id="bd625-111">[How to: Convert a ListBoxItem to a new Data Type](https://docs.microsoft.com/previous-versions/dotnet/netframework-3.5/ms749147(v=vs.90))</span></span>
- [<span data-ttu-id="bd625-112">Vue d’ensemble de Panel</span><span class="sxs-lookup"><span data-stu-id="bd625-112">Panels Overview</span></span>](../controls/panels-overview.md)
