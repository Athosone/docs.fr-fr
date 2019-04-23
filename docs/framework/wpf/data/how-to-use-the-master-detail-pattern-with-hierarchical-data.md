---
title: 'Procédure : Utiliser le modèle maître/détail avec des données hiérarchiques'
ms.date: 03/30/2017
helpviewer_keywords:
- data binding [WPF], Master-Detail data paradigm
- Master-Detail data paradigm
ms.assetid: 11429b9e-058d-4084-bfb6-2cf209c8ddf7
ms.openlocfilehash: e0bbb24b07fdc1c362e2be43d69d189defbc27a4
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59346182"
---
# <a name="how-to-use-the-master-detail-pattern-with-hierarchical-data"></a><span data-ttu-id="aa55f-102">Procédure : Utiliser le modèle maître/détail avec des données hiérarchiques</span><span class="sxs-lookup"><span data-stu-id="aa55f-102">How to: Use the Master-Detail Pattern with Hierarchical Data</span></span>
<span data-ttu-id="aa55f-103">Cet exemple montre comment implémenter le scénario maître / détail.</span><span class="sxs-lookup"><span data-stu-id="aa55f-103">This example shows how to implement the master-detail scenario.</span></span>  
  
## <a name="example"></a><span data-ttu-id="aa55f-104">Exemple</span><span class="sxs-lookup"><span data-stu-id="aa55f-104">Example</span></span>  
 <span data-ttu-id="aa55f-105">Dans cet exemple, `LeagueList` est une collection de `Leagues`.</span><span class="sxs-lookup"><span data-stu-id="aa55f-105">In this example, `LeagueList` is a collection of `Leagues`.</span></span> <span data-ttu-id="aa55f-106">Chaque `League` a un `Name` et une collection de `Divisions`et chaque `Division` a un nom et une collection de `Teams`.</span><span class="sxs-lookup"><span data-stu-id="aa55f-106">Each `League` has a `Name` and a collection of `Divisions`, and each `Division` has a name and a collection of `Teams`.</span></span> <span data-ttu-id="aa55f-107">Chaque `Team` a un nom d’équipe.</span><span class="sxs-lookup"><span data-stu-id="aa55f-107">Each `Team` has a team name.</span></span>  
  
 [!code-xaml[MasterDetail#HowTo1](~/samples/snippets/visualbasic/VS_Snippets_Wpf/MasterDetail/VisualBasic/Page1.xaml#howto1)]  
[!code-xaml[MasterDetail#HowTo2](~/samples/snippets/visualbasic/VS_Snippets_Wpf/MasterDetail/VisualBasic/Page1.xaml#howto2)]  
  
 <span data-ttu-id="aa55f-108">Voici une capture d’écran de l’exemple.</span><span class="sxs-lookup"><span data-stu-id="aa55f-108">The following is a screenshot of the example.</span></span> <span data-ttu-id="aa55f-109">Le `Divisions` <xref:System.Windows.Controls.ListBox> effectue automatiquement le suivi des sélections dans le `Leagues` <xref:System.Windows.Controls.ListBox> et afficher les données correspondantes.</span><span class="sxs-lookup"><span data-stu-id="aa55f-109">The `Divisions` <xref:System.Windows.Controls.ListBox> automatically tracks selections in the `Leagues` <xref:System.Windows.Controls.ListBox> and display the corresponding data.</span></span> <span data-ttu-id="aa55f-110">Le `Teams` <xref:System.Windows.Controls.ListBox> effectue le suivi des sélections dans les deux autres <xref:System.Windows.Controls.ListBox> contrôles.</span><span class="sxs-lookup"><span data-stu-id="aa55f-110">The `Teams` <xref:System.Windows.Controls.ListBox> tracks selections in the other two <xref:System.Windows.Controls.ListBox> controls.</span></span>  
  
 ![Capture d’écran montrant un maître&#45;exemple de scénario de détail.](./media/how-to-use-the-master-detail-pattern-with-hierarchical-data/databinding-master-detail-scenario.png)  
  
 <span data-ttu-id="aa55f-112">Les deux choses à noter dans cet exemple sont :</span><span class="sxs-lookup"><span data-stu-id="aa55f-112">The two things to notice in this example are:</span></span>  
  
1. <span data-ttu-id="aa55f-113">Les trois <xref:System.Windows.Controls.ListBox> lient des contrôles à la même source.</span><span class="sxs-lookup"><span data-stu-id="aa55f-113">The three <xref:System.Windows.Controls.ListBox> controls bind to the same source.</span></span> <span data-ttu-id="aa55f-114">Vous définissez le <xref:System.Windows.Data.Binding.Path%2A> propriété de la liaison pour spécifier le niveau de données que vous souhaitez le <xref:System.Windows.Controls.ListBox> à afficher.</span><span class="sxs-lookup"><span data-stu-id="aa55f-114">You set the <xref:System.Windows.Data.Binding.Path%2A> property of the binding to specify which level of data you want the <xref:System.Windows.Controls.ListBox> to display.</span></span>  
  
2. <span data-ttu-id="aa55f-115">Vous devez définir le <xref:System.Windows.Controls.Primitives.Selector.IsSynchronizedWithCurrentItem%2A> propriété `true` sur la <xref:System.Windows.Controls.ListBox> contrôles dont la sélection que vous effectuez le suivi.</span><span class="sxs-lookup"><span data-stu-id="aa55f-115">You must set the <xref:System.Windows.Controls.Primitives.Selector.IsSynchronizedWithCurrentItem%2A> property to `true` on the <xref:System.Windows.Controls.ListBox> controls of which the selection you are tracking.</span></span> <span data-ttu-id="aa55f-116">Définition de cette propriété garantit que l’élément sélectionné est toujours défini en tant que le <xref:System.Windows.Controls.ItemCollection.CurrentItem%2A>.</span><span class="sxs-lookup"><span data-stu-id="aa55f-116">Setting this property ensures that the selected item is always set as the <xref:System.Windows.Controls.ItemCollection.CurrentItem%2A>.</span></span> <span data-ttu-id="aa55f-117">Ou bien, si le <xref:System.Windows.Controls.ListBox> obtient ses données à partir d’un <xref:System.Windows.Data.CollectionViewSource>, il synchronise automatiquement sélection et la devise.</span><span class="sxs-lookup"><span data-stu-id="aa55f-117">Alternatively, if the <xref:System.Windows.Controls.ListBox> gets it data from a <xref:System.Windows.Data.CollectionViewSource>, it synchronizes selection and currency automatically.</span></span>  
  
 <span data-ttu-id="aa55f-118">La technique est légèrement différente lorsque vous utilisez [!INCLUDE[TLA2#tla_xml](../../../../includes/tla2sharptla-xml-md.md)] données.</span><span class="sxs-lookup"><span data-stu-id="aa55f-118">The technique is slightly different when you are using [!INCLUDE[TLA2#tla_xml](../../../../includes/tla2sharptla-xml-md.md)] data.</span></span> <span data-ttu-id="aa55f-119">Pour obtenir un exemple, consultez [utiliser le modèle maître / détail avec des données XML hiérarchiques](how-to-use-the-master-detail-pattern-with-hierarchical-xml-data.md).</span><span class="sxs-lookup"><span data-stu-id="aa55f-119">For an example, see [Use the Master-Detail Pattern with Hierarchical XML Data](how-to-use-the-master-detail-pattern-with-hierarchical-xml-data.md).</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="aa55f-120">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="aa55f-120">See also</span></span>

- <xref:System.Windows.HierarchicalDataTemplate>
- [<span data-ttu-id="aa55f-121">Effectuer une liaison à une collection et afficher des informations basées sur la sélection</span><span class="sxs-lookup"><span data-stu-id="aa55f-121">Bind to a Collection and Display Information Based on Selection</span></span>](how-to-bind-to-a-collection-and-display-information-based-on-selection.md)
- [<span data-ttu-id="aa55f-122">Vue d’ensemble de la liaison de données</span><span class="sxs-lookup"><span data-stu-id="aa55f-122">Data Binding Overview</span></span>](data-binding-overview.md)
- [<span data-ttu-id="aa55f-123">Vue d’ensemble des modèles de données</span><span class="sxs-lookup"><span data-stu-id="aa55f-123">Data Templating Overview</span></span>](data-templating-overview.md)
- [<span data-ttu-id="aa55f-124">Rubriques de guide pratique</span><span class="sxs-lookup"><span data-stu-id="aa55f-124">How-to Topics</span></span>](data-binding-how-to-topics.md)
