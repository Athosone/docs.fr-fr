---
title: 'Procédure : générer automatiquement des colonnes dans un contrôle DataGridView Windows Forms lié à des données'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- data grids [Windows Forms], autogenerating columns
- columns [Windows Forms], autogenerating
- DataGridView control [Windows Forms], data-bound columns
ms.assetid: 699f6f9e-6aa5-4811-902b-6a2c57dec7d6
ms.openlocfilehash: 4490a24047f5cce1328d68c529783a1d7692ff32
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59165995"
---
# <a name="how-to-autogenerate-columns-in-a-data-bound-windows-forms-datagridview-control"></a><span data-ttu-id="aeccb-102">Procédure : générer automatiquement des colonnes dans un contrôle DataGridView Windows Forms lié à des données</span><span class="sxs-lookup"><span data-stu-id="aeccb-102">How to: Autogenerate Columns in a Data-Bound Windows Forms DataGridView Control</span></span>
<span data-ttu-id="aeccb-103">L’exemple de code suivant montre comment afficher des colonnes à partir d’une source de données liées dans un <xref:System.Windows.Forms.DataGridView> contrôle.</span><span class="sxs-lookup"><span data-stu-id="aeccb-103">The following code example demonstrates how to display columns from a bound data source in a <xref:System.Windows.Forms.DataGridView> control.</span></span> <span data-ttu-id="aeccb-104">Lorsque le <xref:System.Windows.Forms.DataGridView.AutoGenerateColumns%2A> valeur de propriété est `true` (la valeur par défaut), un <xref:System.Windows.Forms.DataGridViewColumn> est créé pour chaque colonne dans la table de source de données.</span><span class="sxs-lookup"><span data-stu-id="aeccb-104">When the <xref:System.Windows.Forms.DataGridView.AutoGenerateColumns%2A> property value is `true` (the default), a <xref:System.Windows.Forms.DataGridViewColumn> is created for each column in the data source table.</span></span>  
  
 <span data-ttu-id="aeccb-105">Si le <xref:System.Windows.Forms.DataGridView> contrôle possède déjà des colonnes lorsque vous définissez le <xref:System.Windows.Forms.DataGridViewComboBoxColumn.DataSource%2A> propriété, la limite existante colonnes sont comparées aux colonnes dans la source de données et conservées chaque fois qu’il existe une correspondance.</span><span class="sxs-lookup"><span data-stu-id="aeccb-105">If the <xref:System.Windows.Forms.DataGridView> control already has columns when you set the <xref:System.Windows.Forms.DataGridViewComboBoxColumn.DataSource%2A> property, the existing bound columns are compared to the columns in the data source and preserved whenever there is a match.</span></span> <span data-ttu-id="aeccb-106">Des colonnes indépendantes sont toujours conservés.</span><span class="sxs-lookup"><span data-stu-id="aeccb-106">Unbound columns are always preserved.</span></span> <span data-ttu-id="aeccb-107">Les colonnes dépendantes pour lesquelles il n’existe aucune correspondance dans la source de données sont supprimées.</span><span class="sxs-lookup"><span data-stu-id="aeccb-107">Bound columns for which there is no match in the data source are removed.</span></span> <span data-ttu-id="aeccb-108">Colonnes de la source de données pour lequel il n’existe aucune correspondance dans le contrôle de génèrent de nouveaux <xref:System.Windows.Forms.DataGridViewColumn> objets, qui sont ajoutés à la fin de la <xref:System.Windows.Forms.DataGridView.Columns%2A> collection.</span><span class="sxs-lookup"><span data-stu-id="aeccb-108">Columns in the data source for which there is no match in the control generate new <xref:System.Windows.Forms.DataGridViewColumn> objects, which are added to the end of the <xref:System.Windows.Forms.DataGridView.Columns%2A> collection.</span></span>  
  
## <a name="example"></a><span data-ttu-id="aeccb-109">Exemple</span><span class="sxs-lookup"><span data-stu-id="aeccb-109">Example</span></span>  
 [!code-csharp[System.Windows.Forms.DataGridViewMisc#020](~/samples/snippets/csharp/VS_Snippets_Winforms/System.Windows.Forms.DataGridViewMisc/CS/datagridviewmisc.cs#020)]
 [!code-vb[System.Windows.Forms.DataGridViewMisc#020](~/samples/snippets/visualbasic/VS_Snippets_Winforms/System.Windows.Forms.DataGridViewMisc/VB/datagridviewmisc.vb#020)]  
  
## <a name="compiling-the-code"></a><span data-ttu-id="aeccb-110">Compilation du code</span><span class="sxs-lookup"><span data-stu-id="aeccb-110">Compiling the Code</span></span>  
 <span data-ttu-id="aeccb-111">Cet exemple nécessite :</span><span class="sxs-lookup"><span data-stu-id="aeccb-111">This example requires:</span></span>  
  
-   <span data-ttu-id="aeccb-112">un contrôle <xref:System.Windows.Forms.DataGridView> nommé `customersDataGridView` ;</span><span class="sxs-lookup"><span data-stu-id="aeccb-112">A <xref:System.Windows.Forms.DataGridView> control named `customersDataGridView`.</span></span>  
  
-   <span data-ttu-id="aeccb-113">Un <xref:System.Data.DataSet> objet nommé `customersDataSet` qui a une table nommée `Customers`.</span><span class="sxs-lookup"><span data-stu-id="aeccb-113">A <xref:System.Data.DataSet> object named `customersDataSet` that has a table named `Customers`.</span></span>  
  
-   <span data-ttu-id="aeccb-114">des références aux assemblys <xref:System?displayProperty=nameWithType>, <xref:System.Windows.Forms?displayProperty=nameWithType>, <xref:System.Data?displayProperty=nameWithType> et <xref:System.Xml?displayProperty=nameWithType>.</span><span class="sxs-lookup"><span data-stu-id="aeccb-114">References to the <xref:System?displayProperty=nameWithType>, <xref:System.Windows.Forms?displayProperty=nameWithType>, <xref:System.Data?displayProperty=nameWithType>, and <xref:System.Xml?displayProperty=nameWithType> assemblies.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="aeccb-115">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="aeccb-115">See also</span></span>

- <xref:System.Windows.Forms.DataGridView>
- <xref:System.Windows.Forms.DataGridView.AutoGenerateColumns%2A?displayProperty=nameWithType>
- [<span data-ttu-id="aeccb-116">Affichage des données dans le contrôle DataGridView Windows Forms</span><span class="sxs-lookup"><span data-stu-id="aeccb-116">Displaying Data in the Windows Forms DataGridView Control</span></span>](displaying-data-in-the-windows-forms-datagridview-control.md)
- [<span data-ttu-id="aeccb-117">Guide pratique pour Supprimer les colonnes générées automatiquement à partir d’un contrôle de DataGridView Windows Forms</span><span class="sxs-lookup"><span data-stu-id="aeccb-117">How to: Remove Autogenerated Columns from a Windows Forms DataGridView Control</span></span>](remove-autogenerated-columns-from-a-wf-datagridview-control.md)
