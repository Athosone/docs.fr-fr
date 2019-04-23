---
title: 'Procédure : Appliquer un style à une ligne dans un ListView implémentant un GridView'
ms.date: 03/30/2017
helpviewer_keywords:
- GridView controls [WPF], styling rows
- styling rows in ListViews implementing GridViews [WPF]
- ListView controls [WPF], styling rows with GridViews
ms.assetid: 2e406ba2-70a0-4e62-841f-0934859de76e
ms.openlocfilehash: 9af8d10c7db2d3bbe8b9443402cbb1cfeaa7edb3
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59091458"
---
# <a name="how-to-style-a-row-in-a-listview-that-implements-a-gridview"></a><span data-ttu-id="50f9e-102">Procédure : Appliquer un style à une ligne dans un ListView implémentant un GridView</span><span class="sxs-lookup"><span data-stu-id="50f9e-102">How to: Style a Row in a ListView That Implements a GridView</span></span>
<span data-ttu-id="50f9e-103">Cet exemple montre comment appliquer un style une ligne dans un <xref:System.Windows.Controls.ListView> contrôle qui implémente un <xref:System.Windows.Controls.GridView> <xref:System.Windows.Controls.ListView.View%2A> mode.</span><span class="sxs-lookup"><span data-stu-id="50f9e-103">This example shows how to style a row in a <xref:System.Windows.Controls.ListView> control that implements a <xref:System.Windows.Controls.GridView><xref:System.Windows.Controls.ListView.View%2A> mode.</span></span>  
  
## <a name="example"></a><span data-ttu-id="50f9e-104">Exemple</span><span class="sxs-lookup"><span data-stu-id="50f9e-104">Example</span></span>  
 <span data-ttu-id="50f9e-105">Vous pouvez appliquer un style une ligne dans un <xref:System.Windows.Controls.ListView> contrôle en définissant une <xref:System.Windows.Controls.ItemsControl.ItemContainerStyle%2A> sur la <xref:System.Windows.Controls.ListView> contrôle.</span><span class="sxs-lookup"><span data-stu-id="50f9e-105">You can style a row in a <xref:System.Windows.Controls.ListView> control by setting an <xref:System.Windows.Controls.ItemsControl.ItemContainerStyle%2A> on the <xref:System.Windows.Controls.ListView> control.</span></span> <span data-ttu-id="50f9e-106">Définir le style pour ses éléments sont représentés en tant que <xref:System.Windows.Controls.ListViewItem> objets.</span><span class="sxs-lookup"><span data-stu-id="50f9e-106">Set the style for its items that are represented as <xref:System.Windows.Controls.ListViewItem> objects.</span></span> <span data-ttu-id="50f9e-107">Le <xref:System.Windows.Controls.ItemsControl.ItemContainerStyle%2A> références le <xref:System.Windows.Controls.ControlTemplate> objets qui sont utilisés pour afficher le contenu de la ligne.</span><span class="sxs-lookup"><span data-stu-id="50f9e-107">The <xref:System.Windows.Controls.ItemsControl.ItemContainerStyle%2A> references the <xref:System.Windows.Controls.ControlTemplate> objects that are used to display the row content.</span></span>  
  
 <span data-ttu-id="50f9e-108">L’exemple complet, dont sont extraits les exemples suivants, affiche une collection d’informations sur des chansons, stockée dans une base de données [!INCLUDE[TLA2#tla_xml](../../../../includes/tla2sharptla-xml-md.md)].</span><span class="sxs-lookup"><span data-stu-id="50f9e-108">The complete sample, which the following examples are extracted from, displays a collection of song information that is stored in an [!INCLUDE[TLA2#tla_xml](../../../../includes/tla2sharptla-xml-md.md)] database.</span></span> <span data-ttu-id="50f9e-109">Chaque chanson de la base de données est associée à un champ d’évaluation. La valeur de ce champ spécifie comment afficher une ligne d’informations sur la chanson.</span><span class="sxs-lookup"><span data-stu-id="50f9e-109">Each song in the database has a rating field and the value of this field specifies how to display a row of song information.</span></span>  
  
 <span data-ttu-id="50f9e-110">L’exemple suivant montre comment définir <xref:System.Windows.Controls.ItemsControl.ItemContainerStyle%2A> pour le <xref:System.Windows.Controls.ListViewItem> les objets qui représentent les chansons de la collection.</span><span class="sxs-lookup"><span data-stu-id="50f9e-110">The following example shows how to define <xref:System.Windows.Controls.ItemsControl.ItemContainerStyle%2A> for the <xref:System.Windows.Controls.ListViewItem> objects that represent the songs in the song collection.</span></span> <span data-ttu-id="50f9e-111">Le <xref:System.Windows.Controls.ItemsControl.ItemContainerStyle%2A> références <xref:System.Windows.Controls.ControlTemplate> objets qui spécifient comment afficher une ligne d’informations sur la chanson.</span><span class="sxs-lookup"><span data-stu-id="50f9e-111">The <xref:System.Windows.Controls.ItemsControl.ItemContainerStyle%2A> references <xref:System.Windows.Controls.ControlTemplate> objects that specify how to display a row of song information.</span></span>  
  
 [!code-xaml[ListViewItemStyleSnippet#ItemContainerStyle](~/samples/snippets/csharp/VS_Snippets_Wpf/ListViewItemStyleSnippet/CS/Window1.xaml#itemcontainerstyle)]  
  
 <span data-ttu-id="50f9e-112">L’exemple suivant montre un <xref:System.Windows.Controls.ControlTemplate> qui ajoute la chaîne de texte `"Strongly Recommended"` à la ligne.</span><span class="sxs-lookup"><span data-stu-id="50f9e-112">The following example shows a <xref:System.Windows.Controls.ControlTemplate> that adds the text string `"Strongly Recommended"` to the row.</span></span> <span data-ttu-id="50f9e-113">Ce modèle est référencé dans le <xref:System.Windows.Controls.ItemsControl.ItemContainerStyle%2A> et s’affiche lorsque l’évaluation de la chanson a la valeur 5 (cinq).</span><span class="sxs-lookup"><span data-stu-id="50f9e-113">This template is referenced in the <xref:System.Windows.Controls.ItemsControl.ItemContainerStyle%2A> and displays when the song's rating has a value of 5 (five).</span></span> <span data-ttu-id="50f9e-114">Le <xref:System.Windows.Controls.ControlTemplate> inclut un <xref:System.Windows.Controls.GridViewRowPresenter> objet dispose le contenu de la ligne dans les colonnes comme défini par le <xref:System.Windows.Controls.GridView> mode d’affichage.</span><span class="sxs-lookup"><span data-stu-id="50f9e-114">The <xref:System.Windows.Controls.ControlTemplate> includes a <xref:System.Windows.Controls.GridViewRowPresenter> object that lays out the contents of the row in columns as defined by the <xref:System.Windows.Controls.GridView> view mode.</span></span>  
  
 [!code-xaml[ListViewItemStyleSnippet#ControlTemplate](~/samples/snippets/csharp/VS_Snippets_Wpf/ListViewItemStyleSnippet/CS/Window1.xaml#controltemplate)]  
  
 <span data-ttu-id="50f9e-115">L’exemple suivant définit <xref:System.Windows.Controls.GridView>.</span><span class="sxs-lookup"><span data-stu-id="50f9e-115">The following example defines <xref:System.Windows.Controls.GridView>.</span></span>  
  
 [!code-xaml[ListViewItemStyleSnippet#GridView](~/samples/snippets/csharp/VS_Snippets_Wpf/ListViewItemStyleSnippet/CS/Window1.xaml#gridview)]  
  
## <a name="see-also"></a><span data-ttu-id="50f9e-116">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="50f9e-116">See also</span></span>

- <xref:System.Windows.Controls.ListView>
- <xref:System.Windows.Controls.GridView>
- [<span data-ttu-id="50f9e-117">Rubriques de guide pratique</span><span class="sxs-lookup"><span data-stu-id="50f9e-117">How-to Topics</span></span>](listview-how-to-topics.md)
- [<span data-ttu-id="50f9e-118">Vue d’ensemble de ListView</span><span class="sxs-lookup"><span data-stu-id="50f9e-118">ListView Overview</span></span>](listview-overview.md)
- [<span data-ttu-id="50f9e-119">Application d’un style et création de modèles</span><span class="sxs-lookup"><span data-stu-id="50f9e-119">Styling and Templating</span></span>](styling-and-templating.md)
