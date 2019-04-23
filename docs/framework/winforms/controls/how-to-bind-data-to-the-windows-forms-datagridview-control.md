---
title: 'Procédure : Lier des données au contrôle Windows Forms DataGridView'
ms.date: 02/08/2019
dev_langs:
- csharp
- vb
helpviewer_keywords:
- data binding [Windows Forms], grids
- data binding [Windows Forms], DataGridView control
- DataGridView control [Windows Forms], data binding
ms.assetid: 1660f69c-5711-45d2-abc1-e25bc6779124
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: e147109a64687177f201ad1e312fab56ea61d604
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59160068"
---
# <a name="how-to-bind-data-to-the-windows-forms-datagridview-control"></a><span data-ttu-id="79841-102">Procédure : Lier des données au contrôle Windows Forms DataGridView</span><span class="sxs-lookup"><span data-stu-id="79841-102">How to: Bind data to the Windows Forms DataGridView control</span></span>

<span data-ttu-id="79841-103">Le <xref:System.Windows.Forms.DataGridView> contrôle prend en charge le modèle de liaison de données Windows Forms standard, il peut être lié à une variété de sources de données.</span><span class="sxs-lookup"><span data-stu-id="79841-103">The <xref:System.Windows.Forms.DataGridView> control supports the standard Windows Forms data binding model, so it can bind to a variety of data sources.</span></span> <span data-ttu-id="79841-104">En règle générale, vous liez à un <xref:System.Windows.Forms.BindingSource> qui gère l’interaction avec la source de données.</span><span class="sxs-lookup"><span data-stu-id="79841-104">Usually, you bind to a <xref:System.Windows.Forms.BindingSource> that manages the interaction with the data source.</span></span> <span data-ttu-id="79841-105">Le <xref:System.Windows.Forms.BindingSource> peut être toute source de données Windows Forms, qui vous donne une grande souplesse lors du choix ou de modification de l’emplacement de vos données.</span><span class="sxs-lookup"><span data-stu-id="79841-105">The <xref:System.Windows.Forms.BindingSource> can be any Windows Forms data source, which gives you great flexibility when choosing or modifying your data's location.</span></span> <span data-ttu-id="79841-106">Pour plus d’informations sur les sources de données le <xref:System.Windows.Forms.DataGridView> contrôle prend en charge, consultez le [vue d’ensemble du contrôle DataGridView](datagridview-control-overview-windows-forms.md).</span><span class="sxs-lookup"><span data-stu-id="79841-106">For more information about data sources the <xref:System.Windows.Forms.DataGridView> control supports, see the [DataGridView control overview](datagridview-control-overview-windows-forms.md).</span></span>  

<span data-ttu-id="79841-107">Visual Studio propose une prise en charge complète de la liaison de données pour le contrôle DataGridView.</span><span class="sxs-lookup"><span data-stu-id="79841-107">Visual Studio has extensive support for data binding to the DataGridView control.</span></span> <span data-ttu-id="79841-108">Pour plus d'informations, voir [Procédure : Lier des données au contrôle DataGridView de Windows Forms à l’aide du concepteur](bind-data-to-the-datagrid-using-the-designer.md).</span><span class="sxs-lookup"><span data-stu-id="79841-108">For more information, see [How to: Bind data to the Windows Forms DataGridView control using the Designer](bind-data-to-the-datagrid-using-the-designer.md).</span></span>  

<span data-ttu-id="79841-109">Pour vous connecter à un contrôle DataGridView à des données :</span><span class="sxs-lookup"><span data-stu-id="79841-109">To connect a DataGridView control to data:</span></span>

1. <span data-ttu-id="79841-110">Implémenter une méthode pour gérer les détails de la récupération des données.</span><span class="sxs-lookup"><span data-stu-id="79841-110">Implement a method to handle the details of retrieving the data.</span></span> <span data-ttu-id="79841-111">Le code suivant exemple implémente un `GetData` méthode qui initialise un <xref:System.Data.SqlClient.SqlDataAdapter>et l’utilise pour remplir un <xref:System.Data.DataTable>.</span><span class="sxs-lookup"><span data-stu-id="79841-111">The following code example implements a `GetData` method that initializes a <xref:System.Data.SqlClient.SqlDataAdapter>, and uses it to populate a <xref:System.Data.DataTable>.</span></span> <span data-ttu-id="79841-112">Il lie ensuite le <xref:System.Data.DataTable> à la <xref:System.Windows.Forms.BindingSource>.</span><span class="sxs-lookup"><span data-stu-id="79841-112">It then binds the <xref:System.Data.DataTable> to the <xref:System.Windows.Forms.BindingSource>.</span></span> 

2. <span data-ttu-id="79841-113">Dans le formulaire <xref:System.Windows.Forms.Form.Load> Gestionnaire d’événements, liez le <xref:System.Windows.Forms.DataGridView> le contrôle à la <xref:System.Windows.Forms.BindingSource>et appelez le `GetData` méthode pour récupérer les données.</span><span class="sxs-lookup"><span data-stu-id="79841-113">In the form's <xref:System.Windows.Forms.Form.Load> event handler, bind the <xref:System.Windows.Forms.DataGridView> control to the <xref:System.Windows.Forms.BindingSource>, and call the `GetData` method to retrieve the data.</span></span>  

## <a name="example"></a><span data-ttu-id="79841-114">Exemple</span><span class="sxs-lookup"><span data-stu-id="79841-114">Example</span></span>

<span data-ttu-id="79841-115">Cet exemple de code complet récupère des données à partir d’une base de données pour remplir un contrôle DataGridView dans un formulaire Windows.</span><span class="sxs-lookup"><span data-stu-id="79841-115">This complete code example retrieves data from a database to populate a DataGridView control in a Windows form.</span></span> <span data-ttu-id="79841-116">Le formulaire comporte également des boutons pour recharger les données et soumettre des modifications à la base de données.</span><span class="sxs-lookup"><span data-stu-id="79841-116">The form also has buttons to reload data and submit changes to the database.</span></span>  

<span data-ttu-id="79841-117">Cet exemple nécessite :</span><span class="sxs-lookup"><span data-stu-id="79841-117">This example requires:</span></span> 

- <span data-ttu-id="79841-118">Accès à une base de données exemple Northwind SQL Server.</span><span class="sxs-lookup"><span data-stu-id="79841-118">Access to a Northwind SQL Server sample database.</span></span> <span data-ttu-id="79841-119">Pour plus d’informations sur l’installation de la base de données Northwind, consultez [obtenir les bases de données d’exemple pour obtenir des exemples de code ADO.NET](../../data/adonet/sql/linq/downloading-sample-databases.md).</span><span class="sxs-lookup"><span data-stu-id="79841-119">For more information about installing the Northwind sample database, see [Get the sample databases for ADO.NET code samples](../../data/adonet/sql/linq/downloading-sample-databases.md).</span></span> 

- <span data-ttu-id="79841-120">Références aux assemblys System, System.Windows.Forms, System.Data et System.Xml.</span><span class="sxs-lookup"><span data-stu-id="79841-120">References to the System, System.Windows.Forms, System.Data, and System.Xml assemblies.</span></span>  

<span data-ttu-id="79841-121">Pour générer et exécuter cet exemple, collez le code dans le *Form1* fichier de code dans un nouveau projet Windows Forms.</span><span class="sxs-lookup"><span data-stu-id="79841-121">To build and run this example, paste the code into the *Form1* code file in a new Windows Forms project.</span></span> <span data-ttu-id="79841-122">Pour plus d’informations sur la génération à partir de la C# ou ligne de commande de Visual Basic, consultez [de ligne de commande avec csc.exe](../../../csharp/language-reference/compiler-options/command-line-building-with-csc-exe.md) ou [construire à partir de la ligne de commande](../../../visual-basic/reference/command-line-compiler/building-from-the-command-line.md).</span><span class="sxs-lookup"><span data-stu-id="79841-122">For information about building from the C# or Visual Basic command line, see [Command-line building with csc.exe](../../../csharp/language-reference/compiler-options/command-line-building-with-csc-exe.md) or [Build from the command line](../../../visual-basic/reference/command-line-compiler/building-from-the-command-line.md).</span></span>  
  
<span data-ttu-id="79841-123">Remplir le `connectionString` variable dans l’exemple avec les valeurs pour votre connexion de base de données exemple Northwind SQL Server.</span><span class="sxs-lookup"><span data-stu-id="79841-123">Populate the `connectionString` variable in the example with the values for your Northwind SQL Server sample database connection.</span></span> <span data-ttu-id="79841-124">L’authentification Windows, également appelée sécurité intégrée, est un moyen plus sûr pour vous connecter à la base de données que le stockage d’un mot de passe dans la chaîne de connexion.</span><span class="sxs-lookup"><span data-stu-id="79841-124">Windows Authentication, also called integrated security, is a more secure way to connect to the database than storing a password in the connection string.</span></span> <span data-ttu-id="79841-125">Pour plus d’informations sur la sécurité de connexion, consultez [protéger les informations de connexion](../../data/adonet/protecting-connection-information.md).</span><span class="sxs-lookup"><span data-stu-id="79841-125">For more information about connection security, see [Protect connection information](../../data/adonet/protecting-connection-information.md).</span></span>  

[!code-csharp[System.Windows.Forms.DataGridViewBoundEditable](~/samples/snippets/csharp/VS_Snippets_Winforms/System.Windows.Forms.DataGridViewBoundEditable/CS/datagridviewboundeditable.cs)]
[!code-vb[System.Windows.Forms.DataGridViewBoundEditable](~/samples/snippets/visualbasic/VS_Snippets_Winforms/System.Windows.Forms.DataGridViewBoundEditable/VB/datagridviewboundeditable.vb)]  
  
## <a name="see-also"></a><span data-ttu-id="79841-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="79841-126">See also</span></span>

- <xref:System.Windows.Forms.DataGridView>
- <xref:System.Windows.Forms.DataGridView.DataSource%2A?displayProperty=nameWithType>
- <xref:System.Windows.Forms.BindingSource>
- [<span data-ttu-id="79841-127">Afficher des données dans le contrôle Windows Forms DataGridView</span><span class="sxs-lookup"><span data-stu-id="79841-127">Display data in the Windows Forms DataGridView control</span></span>](displaying-data-in-the-windows-forms-datagridview-control.md)
- [<span data-ttu-id="79841-128">Protéger les informations de connexion</span><span class="sxs-lookup"><span data-stu-id="79841-128">Protect connection information</span></span>](../../data/adonet/protecting-connection-information.md)
