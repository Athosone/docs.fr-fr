---
title: 'Procédure : Créer un mode d’affichage personnalisé pour un ListView'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- ListView controls [WPF], creating custom View mode
ms.assetid: 71077349-eeb9-4344-ab29-b5df96df3314
ms.openlocfilehash: de11250a2e7529fba3b262e42b6714262738fa90
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59092888"
---
# <a name="how-to-create-a-custom-view-mode-for-a-listview"></a>Procédure : Créer un mode d’affichage personnalisé pour un ListView
Cet exemple montre comment créer un personnalisé <xref:System.Windows.Controls.ListView.View%2A> mode pour un <xref:System.Windows.Controls.ListView> contrôle.  
  
## <a name="example"></a>Exemple  
 Vous devez utiliser le <xref:System.Windows.Controls.ViewBase> classe lorsque vous créez un affichage personnalisé pour le <xref:System.Windows.Controls.ListView> contrôle. L’exemple suivant montre un mode d’affichage qui est appelé `PlainView`, qui est dérivée de la <xref:System.Windows.Controls.ViewBase> classe.  
  
 [!code-csharp[ListViewCustomView#PlainView](~/samples/snippets/csharp/VS_Snippets_Wpf/ListViewCustomView/CSharp/PlainView.cs#plainview)]
 [!code-vb[ListViewCustomView#PlainView](~/samples/snippets/visualbasic/VS_Snippets_Wpf/ListViewCustomView/visualbasic/plainview.vb#plainview)]  
  
 Pour appliquer un style à la vue personnalisée, utilisez la <xref:System.Windows.Style> classe. L’exemple suivant définit un <xref:System.Windows.Style> pour la `PlainView` mode d’affichage. Dans l’exemple précédent, ce style est défini comme valeur de la <xref:System.Windows.Controls.ViewBase.DefaultStyleKey%2A> propriété est définie pour `PlainView`.  
  
 [!code-xaml[ListViewCustomView#PlainViewStyle](~/samples/snippets/csharp/VS_Snippets_Wpf/ListViewCustomView/CSharp/Themes/Generic.xaml#plainviewstyle)]  
  
 Pour définir la disposition des données dans un mode d’affichage personnalisé, définissez un <xref:System.Windows.DataTemplate> objet. L’exemple suivant définit un <xref:System.Windows.DataTemplate> qui peut être utilisé pour afficher des données dans le `PlainView` mode d’affichage.  
  
 [!code-xaml[ListViewCustomView#PlainViewDataTemplate](~/samples/snippets/csharp/VS_Snippets_Wpf/ListViewCustomView/CSharp/Window1.xaml#plainviewdatatemplate)]  
  
 L’exemple suivant montre comment définir un <xref:System.Windows.ResourceKey> pour le `PlainView` mode d’affichage qui utilise le <xref:System.Windows.DataTemplate> qui est définie dans l’exemple précédent.  
  
 [!code-xaml[ListViewCustomView#PlainViewtileView](~/samples/snippets/csharp/VS_Snippets_Wpf/ListViewCustomView/CSharp/Window1.xaml#plainviewtileview)]  
  
 Un <xref:System.Windows.Controls.ListView> contrôle peut utiliser une vue personnalisée si vous définissez le <xref:System.Windows.Controls.ListView.View%2A> propriété à la clé de ressource. L’exemple suivant montre comment spécifier `PlainView` en tant que le mode d’affichage pour un <xref:System.Windows.Controls.ListView>.  
  
 [!code-csharp[ListViewCustomView#ListViewtileViewmode](~/samples/snippets/csharp/VS_Snippets_Wpf/ListViewCustomView/CSharp/Window1.xaml.cs#listviewtileviewmode)]
 [!code-vb[ListViewCustomView#ListViewtileViewmode](~/samples/snippets/visualbasic/VS_Snippets_Wpf/ListViewCustomView/visualbasic/window1.xaml.vb#listviewtileviewmode)]  
  
 Pour obtenir un exemple complet, consultez [ListView avec plusieurs vues (C#)](https://github.com/dotnet/samples/tree/master/snippets/csharp/VS_Snippets_Wpf/ListViewCustomView/CSharp) ou [ListView avec plusieurs Views(Visual Basic)](https://github.com/dotnet/samples/tree/master/snippets/visualbasic/VS_Snippets_Wpf/ListViewCustomView/visualbasic).  
  
## <a name="see-also"></a>Voir aussi

- <xref:System.Windows.Controls.ListView>
- <xref:System.Windows.Controls.GridView>
- [Rubriques de guide pratique](listview-how-to-topics.md)
- [Vue d’ensemble de ListView](listview-overview.md)
- [Vue d’ensemble de GridView](gridview-overview.md)
