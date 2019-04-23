---
title: 'Procédure : lier le contrôle DataGrid Windows Forms à une source de données'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
- cpp
helpviewer_keywords:
- datasets [Windows Forms], binding to DataGrid control
- data binding [Windows Forms], DataGrid control
- DataGrid control [Windows Forms], data binding
- bound controls [Windows Forms], DataGrid control
- Windows Forms controls, data binding
- bound controls [Windows Forms]
- data-bound controls [Windows Forms], DataGrid
ms.assetid: 128cdb07-dfd3-4d60-9d6a-902847667c36
ms.openlocfilehash: 920a93894cc126f85bc6b618efbe6e9cedea4881
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59332571"
---
# <a name="how-to-bind-the-windows-forms-datagrid-control-to-a-data-source"></a><span data-ttu-id="0b7f4-102">Procédure : lier le contrôle DataGrid Windows Forms à une source de données</span><span class="sxs-lookup"><span data-stu-id="0b7f4-102">How to: Bind the Windows Forms DataGrid Control to a Data Source</span></span>
> [!NOTE]
>  <span data-ttu-id="0b7f4-103">Le contrôle <xref:System.Windows.Forms.DataGridView> remplace le contrôle <xref:System.Windows.Forms.DataGrid> et lui ajoute des fonctionnalités ; toutefois, le contrôle <xref:System.Windows.Forms.DataGrid> est conservé pour la compatibilité descendante et l'utilisation future si tel est votre choix.</span><span class="sxs-lookup"><span data-stu-id="0b7f4-103">The <xref:System.Windows.Forms.DataGridView> control replaces and adds functionality to the <xref:System.Windows.Forms.DataGrid> control; however, the <xref:System.Windows.Forms.DataGrid> control is retained for both backward compatibility and future use, if you choose.</span></span> <span data-ttu-id="0b7f4-104">Pour plus d’informations, consultez [Différences entre les contrôles DataGridView et DataGrid Windows Forms](differences-between-the-windows-forms-datagridview-and-datagrid-controls.md).</span><span class="sxs-lookup"><span data-stu-id="0b7f4-104">For more information, see [Differences Between the Windows Forms DataGridView and DataGrid Controls](differences-between-the-windows-forms-datagridview-and-datagrid-controls.md).</span></span>  
  
 <span data-ttu-id="0b7f4-105">Les formulaires Windows <xref:System.Windows.Forms.DataGrid> contrôle est spécifiquement conçu pour afficher des informations à partir d’une source de données.</span><span class="sxs-lookup"><span data-stu-id="0b7f4-105">The Windows Forms <xref:System.Windows.Forms.DataGrid> control is specifically designed to display information from a data source.</span></span> <span data-ttu-id="0b7f4-106">Vous liez le contrôle au moment de l’exécution en appelant le <xref:System.Windows.Forms.DataGrid.SetDataBinding%2A> (méthode).</span><span class="sxs-lookup"><span data-stu-id="0b7f4-106">You bind the control at run time by calling the <xref:System.Windows.Forms.DataGrid.SetDataBinding%2A> method.</span></span> <span data-ttu-id="0b7f4-107">Bien que vous pouvez afficher des données à partir de diverses sources de données, les sources les plus courantes sont les vues de données et des jeux de données.</span><span class="sxs-lookup"><span data-stu-id="0b7f4-107">Although you can display data from a variety of data sources, the most typical sources are datasets and data views.</span></span>  
  
### <a name="to-data-bind-the-datagrid-control-programmatically"></a><span data-ttu-id="0b7f4-108">Lier aux données du contrôle DataGrid par programme</span><span class="sxs-lookup"><span data-stu-id="0b7f4-108">To data-bind the DataGrid control programmatically</span></span>  
  
1. <span data-ttu-id="0b7f4-109">Écrire du code pour remplir le dataset.</span><span class="sxs-lookup"><span data-stu-id="0b7f4-109">Write code to fill the dataset.</span></span>  
  
     <span data-ttu-id="0b7f4-110">Si la source de données est un jeu de données ou une vue de données basée sur une table de dataset, ajoutez le code au formulaire pour remplir le dataset.</span><span class="sxs-lookup"><span data-stu-id="0b7f4-110">If the data source is a dataset or a data view based on a dataset table, add code to the form to fill the dataset.</span></span>  
  
     <span data-ttu-id="0b7f4-111">Le code exact que vous utilisez dépend où le jeu de données est l’obtention de données.</span><span class="sxs-lookup"><span data-stu-id="0b7f4-111">The exact code you use depends on where the dataset is getting data.</span></span> <span data-ttu-id="0b7f4-112">Si le jeu de données est rempli directement à partir d’une base de données, vous appelez généralement la `Fill` méthode d’un adaptateur de données, comme dans l’exemple suivant, qui remplit un dataset nommé `DsCategories1`:</span><span class="sxs-lookup"><span data-stu-id="0b7f4-112">If the dataset is being populated directly from a database, you typically call the `Fill` method of a data adapter, as in the following example, which populates a dataset called `DsCategories1`:</span></span>  
  
    ```vb  
    sqlDataAdapter1.Fill(DsCategories1)  
    ```  
  
    ```csharp  
    sqlDataAdapter1.Fill(DsCategories1);  
    ```  
  
    ```cpp  
    sqlDataAdapter1->Fill(dsCategories1);  
    ```  
  
     <span data-ttu-id="0b7f4-113">Si le jeu de données est remplie à partir d’un service Web XML, vous en général, créez une instance du service dans votre code, puis appelez une de ses méthodes pour retourner un jeu de données.</span><span class="sxs-lookup"><span data-stu-id="0b7f4-113">If the dataset is being filled from an XML Web service, you typically create an instance of the service in your code and then call one of its methods to return a dataset.</span></span> <span data-ttu-id="0b7f4-114">Vous permet ensuite de fusionner le jeu de données à partir du service Web XML dans votre jeu de données local.</span><span class="sxs-lookup"><span data-stu-id="0b7f4-114">You then merge the dataset from the XML Web service into your local dataset.</span></span> <span data-ttu-id="0b7f4-115">L’exemple suivant montre comment vous pouvez créer une instance d’un service Web XML appelé `CategoriesService`, appelez sa `GetCategories` (méthode) et fusion, le jeu de données résultant dans un jeu de données local appelé `DsCategories1`:</span><span class="sxs-lookup"><span data-stu-id="0b7f4-115">The following example shows how you can create an instance of an XML Web service called `CategoriesService`, call its `GetCategories` method, and merge the resulting dataset into a local dataset called `DsCategories1`:</span></span>  
  
    ```vb  
    Dim ws As New MyProject.localhost.CategoriesService()  
    ws.Credentials = System.Net.CredentialCache.DefaultCredentials  
    DsCategories1.Merge(ws.GetCategories())  
    ```  
  
    ```csharp  
    MyProject.localhost.CategoriesService ws = new MyProject.localhost.CategoriesService();  
    ws.Credentials = System.Net.CredentialCache.DefaultCredentials;  
    DsCategories1.Merge(ws.GetCategories());  
    ```  
  
    ```cpp  
    MyProject::localhost::CategoriesService^ ws =   
       new MyProject::localhost::CategoriesService();  
    ws->Credentials = System::Net::CredentialCache::DefaultCredentials;  
    dsCategories1->Merge(ws->GetCategories());  
    ```  
  
2. <span data-ttu-id="0b7f4-116">Appelez le <xref:System.Windows.Forms.DataGrid> du contrôle <xref:System.Windows.Forms.DataGrid.SetDataBinding%2A> méthode, en lui passant la source de données et un membre de données.</span><span class="sxs-lookup"><span data-stu-id="0b7f4-116">Call the <xref:System.Windows.Forms.DataGrid> control's <xref:System.Windows.Forms.DataGrid.SetDataBinding%2A> method, passing it the data source and a data member.</span></span> <span data-ttu-id="0b7f4-117">Si vous n’avez pas besoin de transmettre explicitement un membre de données, passez une chaîne vide.</span><span class="sxs-lookup"><span data-stu-id="0b7f4-117">If you do not need to explicitly pass a data member, pass an empty string.</span></span>  
  
    > [!NOTE]
    >  <span data-ttu-id="0b7f4-118">Si vous liez la grille pour la première fois, vous pouvez définir le contrôle <xref:System.Windows.Forms.DataGrid.DataSource%2A> et <xref:System.Windows.Forms.DataGrid.DataMember%2A> propriétés.</span><span class="sxs-lookup"><span data-stu-id="0b7f4-118">If you are binding the grid for the first time, you can set the control's <xref:System.Windows.Forms.DataGrid.DataSource%2A> and <xref:System.Windows.Forms.DataGrid.DataMember%2A> properties.</span></span> <span data-ttu-id="0b7f4-119">Toutefois, vous ne pouvez pas réinitialiser ces propriétés une fois qu’elles ont été définies.</span><span class="sxs-lookup"><span data-stu-id="0b7f4-119">However, you cannot reset these properties once they have been set.</span></span> <span data-ttu-id="0b7f4-120">Par conséquent, il est recommandé de toujours utiliser le <xref:System.Windows.Forms.DataGrid.SetDataBinding%2A> (méthode).</span><span class="sxs-lookup"><span data-stu-id="0b7f4-120">Therefore, it is recommended that you always use the <xref:System.Windows.Forms.DataGrid.SetDataBinding%2A> method.</span></span>  
  
     <span data-ttu-id="0b7f4-121">L’exemple suivant montre comment vous pouvez lier par programmation à la table Customers dans un dataset nommé `DsCustomers1`:</span><span class="sxs-lookup"><span data-stu-id="0b7f4-121">The following example shows how you can programmatically bind to the Customers table in a dataset called `DsCustomers1`:</span></span>  
  
    ```vb  
    DataGrid1.SetDataBinding(DsCustomers1, "Customers")  
    ```  
  
    ```csharp  
    DataGrid1.SetDataBinding(DsCustomers1, "Customers");  
    ```  
  
    ```cpp  
    dataGrid1->SetDataBinding(dsCustomers1, "Customers");  
    ```  
  
     <span data-ttu-id="0b7f4-122">Si la table Customers est la seule table dans le jeu de données, vous pourriez également lier à la grille de cette façon :</span><span class="sxs-lookup"><span data-stu-id="0b7f4-122">If the Customers table is the only table in the dataset, you could alternatively bind the grid this way:</span></span>  
  
    ```vb  
    DataGrid1.SetDataBinding(DsCustomers1, "")  
    ```  
  
    ```csharp  
    DataGrid1.SetDataBinding(DsCustomers1, "");  
    ```  
  
    ```cpp  
    dataGrid1->SetDataBinding(dsCustomers1, "");  
    ```  
  
3. <span data-ttu-id="0b7f4-123">(Facultatif) Ajouter les styles de table approprié et les styles de colonne à la grille.</span><span class="sxs-lookup"><span data-stu-id="0b7f4-123">(Optional) Add the appropriate table styles and column styles to the grid.</span></span> <span data-ttu-id="0b7f4-124">S’il n’y a aucun style de tableau, vous verrez la table, mais avec la mise en forme minimale et toutes les colonnes visibles.</span><span class="sxs-lookup"><span data-stu-id="0b7f4-124">If there are no table styles, you will see the table, but with minimal formatting and with all columns visible.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="0b7f4-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0b7f4-125">See also</span></span>

- [<span data-ttu-id="0b7f4-126">Vue d’ensemble du contrôle DataGrid</span><span class="sxs-lookup"><span data-stu-id="0b7f4-126">DataGrid Control Overview</span></span>](datagrid-control-overview-windows-forms.md)
- [<span data-ttu-id="0b7f4-127">Guide pratique pour Ajouter des Tables et des colonnes au contrôle DataGrid Windows Forms</span><span class="sxs-lookup"><span data-stu-id="0b7f4-127">How to: Add Tables and Columns to the Windows Forms DataGrid Control</span></span>](how-to-add-tables-and-columns-to-the-windows-forms-datagrid-control.md)
- [<span data-ttu-id="0b7f4-128">DataGrid, contrôle</span><span class="sxs-lookup"><span data-stu-id="0b7f4-128">DataGrid Control</span></span>](datagrid-control-windows-forms.md)
- [<span data-ttu-id="0b7f4-129">Liaison de données Windows Forms</span><span class="sxs-lookup"><span data-stu-id="0b7f4-129">Windows Forms Data Binding</span></span>](../windows-forms-data-binding.md)
