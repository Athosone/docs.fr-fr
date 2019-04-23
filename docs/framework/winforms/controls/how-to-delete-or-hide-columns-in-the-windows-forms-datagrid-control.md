---
title: 'Procédure : supprimer ou masquer des colonnes dans le contrôle DataGrid Windows Forms'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- data grids [Windows Forms], deleting columns
- DataGrid control [Windows Forms], deleting columns
- data grids [Windows Forms], hiding columns
- columns [Windows Forms], hiding
- columns [Windows Forms], deleting in data grids
- DataGrid control [Windows Forms], hiding columns
ms.assetid: bcd0dd96-6687-4c48-b0e1-d5287b93ac91
ms.openlocfilehash: d3f1f013cbb5e41c997014f556602b01bab62914
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59297510"
---
# <a name="how-to-delete-or-hide-columns-in-the-windows-forms-datagrid-control"></a><span data-ttu-id="d5a05-102">Procédure : supprimer ou masquer des colonnes dans le contrôle DataGrid Windows Forms</span><span class="sxs-lookup"><span data-stu-id="d5a05-102">How to: Delete or Hide Columns in the Windows Forms DataGrid Control</span></span>
> [!NOTE]
>  <span data-ttu-id="d5a05-103">Le contrôle <xref:System.Windows.Forms.DataGridView> remplace le contrôle <xref:System.Windows.Forms.DataGrid> et lui ajoute des fonctionnalités ; toutefois, le contrôle <xref:System.Windows.Forms.DataGrid> est conservé pour la compatibilité descendante et l'utilisation future si tel est votre choix.</span><span class="sxs-lookup"><span data-stu-id="d5a05-103">The <xref:System.Windows.Forms.DataGridView> control replaces and adds functionality to the <xref:System.Windows.Forms.DataGrid> control; however, the <xref:System.Windows.Forms.DataGrid> control is retained for both backward compatibility and future use, if you choose.</span></span> <span data-ttu-id="d5a05-104">Pour plus d’informations, consultez [Différences entre les contrôles DataGridView et DataGrid Windows Forms](differences-between-the-windows-forms-datagridview-and-datagrid-controls.md).</span><span class="sxs-lookup"><span data-stu-id="d5a05-104">For more information, see [Differences Between the Windows Forms DataGridView and DataGrid Controls](differences-between-the-windows-forms-datagridview-and-datagrid-controls.md).</span></span>  
  
 <span data-ttu-id="d5a05-105">Vous pouvez par programmation supprimer ou masquer des colonnes dans les formulaires Windows <xref:System.Windows.Forms.DataGrid> contrôle à l’aide des propriétés et méthodes de la <xref:System.Windows.Forms.GridColumnStylesCollection> et <xref:System.Windows.Forms.DataGridColumnStyle> objets (qui sont membres de la <xref:System.Windows.Forms.DataGridTableStyle> classe).</span><span class="sxs-lookup"><span data-stu-id="d5a05-105">You can programmatically delete or hide columns in the Windows Forms <xref:System.Windows.Forms.DataGrid> control by using the properties and methods of the <xref:System.Windows.Forms.GridColumnStylesCollection> and <xref:System.Windows.Forms.DataGridColumnStyle> objects (which are members of the <xref:System.Windows.Forms.DataGridTableStyle> class).</span></span>  
  
 <span data-ttu-id="d5a05-106">Les colonnes supprimées ou masquées existent toujours dans la source de données est lié à la grille et accessible par programme.</span><span class="sxs-lookup"><span data-stu-id="d5a05-106">The deleted or hidden columns still exist in the data source the grid is bound to, and can still be accessed programmatically.</span></span> <span data-ttu-id="d5a05-107">Ils sont simplement n’est plus visibles dans la grille de données.</span><span class="sxs-lookup"><span data-stu-id="d5a05-107">They are just no longer visible in the datagrid.</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="d5a05-108">Si votre application n’accède pas à certaines colonnes de données, et que vous ne souhaitez pas les afficher dans la grille de données, il n’est probablement pas nécessaire pour les inclure dans la source de données en premier lieu.</span><span class="sxs-lookup"><span data-stu-id="d5a05-108">If your application does not access certain columns of data, and you do not want them displayed in the datagrid, then it is probably not necessary to include them in the data source in the first place.</span></span>  
  
### <a name="to-delete-a-column-from-the-datagrid-programmatically"></a><span data-ttu-id="d5a05-109">Pour supprimer une colonne à partir de la grille de données par programmation</span><span class="sxs-lookup"><span data-stu-id="d5a05-109">To delete a column from the DataGrid programmatically</span></span>  
  
1. <span data-ttu-id="d5a05-110">Dans la zone de déclarations de votre formulaire, déclarez une nouvelle instance de la <xref:System.Windows.Forms.DataGridTableStyle> classe.</span><span class="sxs-lookup"><span data-stu-id="d5a05-110">In the declarations area of your form, declare a new instance of the <xref:System.Windows.Forms.DataGridTableStyle> class.</span></span>  
  
2. <span data-ttu-id="d5a05-111">Définir le <xref:System.Windows.Forms.DataGridTableStyle.MappingName%2A?displayProperty=nameWithType> propriété à la table dans votre source de données que vous souhaitez appliquer le style.</span><span class="sxs-lookup"><span data-stu-id="d5a05-111">Set the <xref:System.Windows.Forms.DataGridTableStyle.MappingName%2A?displayProperty=nameWithType> property to the table in your data source that you want to apply the style to.</span></span> <span data-ttu-id="d5a05-112">L’exemple suivant utilise le <xref:System.Windows.Forms.DataGrid.DataMember%2A?displayProperty=nameWithType> propriété, qu’il considère est déjà défini.</span><span class="sxs-lookup"><span data-stu-id="d5a05-112">The following example uses the <xref:System.Windows.Forms.DataGrid.DataMember%2A?displayProperty=nameWithType> property, which it assumes is already set.</span></span>  
  
3. <span data-ttu-id="d5a05-113">Ajoutez la nouvelle <xref:System.Windows.Forms.DataGridTableStyle> objet à la collection de styles de table de la grille de données.</span><span class="sxs-lookup"><span data-stu-id="d5a05-113">Add the new <xref:System.Windows.Forms.DataGridTableStyle> object to the datagrid's table styles collection.</span></span>  
  
4. <span data-ttu-id="d5a05-114">Appelez le <xref:System.Windows.Forms.GridColumnStylesCollection.RemoveAt%2A> méthode de la <xref:System.Windows.Forms.DataGrid>de <xref:System.Windows.Forms.DataGridTableStyle.GridColumnStyles%2A> collection, en spécifiant l’index de colonne de la colonne à supprimer.</span><span class="sxs-lookup"><span data-stu-id="d5a05-114">Call the <xref:System.Windows.Forms.GridColumnStylesCollection.RemoveAt%2A> method of the <xref:System.Windows.Forms.DataGrid>'s <xref:System.Windows.Forms.DataGridTableStyle.GridColumnStyles%2A> collection, specifying the column index of the column to delete.</span></span>  
  
    ```vb  
    ' Declare a new DataGridTableStyle in the  
    ' declarations area of your form.  
    Dim ts As DataGridTableStyle = New DataGridTableStyle()  
  
    Sub DeleteColumn()  
       ' Set the DataGridTableStyle.MappingName property  
       ' to the table in the data source to map to.  
       ts.MappingName = DataGrid1.DataMember  
  
       ' Add it to the datagrid's TableStyles collection  
       DataGrid1.TableStyles.Add(ts)  
  
       ' Delete the first column (index 0)  
       DataGrid1.TableStyles(0).GridColumnStyles.RemoveAt(0)  
    End Sub  
    ```  
  
    ```csharp  
    // Declare a new DataGridTableStyle in the  
    // declarations area of your form.  
    DataGridTableStyle ts = new DataGridTableStyle();  
  
    private void deleteColumn()  
    {  
       // Set the DataGridTableStyle.MappingName property  
       // to the table in the data source to map to.  
       ts.MappingName = dataGrid1.DataMember;  
  
       // Add it to the datagrid's TableStyles collection  
       dataGrid1.TableStyles.Add(ts);  
  
       // Delete the first column (index 0)  
       dataGrid1.TableStyles[0].GridColumnStyles.RemoveAt(0);  
    }  
    ```  
  
### <a name="to-hide-a-column-in-the-datagrid-programmatically"></a><span data-ttu-id="d5a05-115">Pour masquer une colonne dans la grille de données par programmation</span><span class="sxs-lookup"><span data-stu-id="d5a05-115">To hide a column in the DataGrid programmatically</span></span>  
  
1. <span data-ttu-id="d5a05-116">Dans la zone de déclarations de votre formulaire, déclarez une nouvelle instance de la <xref:System.Windows.Forms.DataGridTableStyle> classe.</span><span class="sxs-lookup"><span data-stu-id="d5a05-116">In the declarations area of your form, declare a new instance of the <xref:System.Windows.Forms.DataGridTableStyle> class.</span></span>  
  
2. <span data-ttu-id="d5a05-117">Définir le <xref:System.Windows.Forms.DataGridTableStyle.MappingName%2A> propriété de la <xref:System.Windows.Forms.DataGridTableStyle> à la table dans votre source de données que vous souhaitez appliquer le style.</span><span class="sxs-lookup"><span data-stu-id="d5a05-117">Set the <xref:System.Windows.Forms.DataGridTableStyle.MappingName%2A> property of the <xref:System.Windows.Forms.DataGridTableStyle> to the table in your data source that you want to apply the style to.</span></span> <span data-ttu-id="d5a05-118">Le code suivant exemple utilise le <xref:System.Windows.Forms.DataGrid.DataMember%2A?displayProperty=nameWithType> propriété, qu’il considère est déjà défini.</span><span class="sxs-lookup"><span data-stu-id="d5a05-118">The following code example uses the <xref:System.Windows.Forms.DataGrid.DataMember%2A?displayProperty=nameWithType> property, which it assumes is already set.</span></span>  
  
3. <span data-ttu-id="d5a05-119">Ajoutez la nouvelle <xref:System.Windows.Forms.DataGridTableStyle> objet à la collection de styles de table de la grille de données.</span><span class="sxs-lookup"><span data-stu-id="d5a05-119">Add the new <xref:System.Windows.Forms.DataGridTableStyle> object to the datagrid's table styles collection.</span></span>  
  
4. <span data-ttu-id="d5a05-120">Masquer la colonne en définissant son `Width` propriété sur 0, qui spécifie l’index de colonne de la colonne à masquer.</span><span class="sxs-lookup"><span data-stu-id="d5a05-120">Hide the column by setting its `Width` property to 0, specifying the column index of the column to hide.</span></span>  
  
    ```vb  
    ' Declare a new DataGridTableStyle in the  
    ' declarations area of your form.  
    Dim ts As DataGridTableStyle = New DataGridTableStyle()  
  
    Sub HideColumn()  
       ' Set the DataGridTableStyle.MappingName property  
       ' to the table in the data source to map to.  
       ts.MappingName = DataGrid1.DataMember  
  
       ' Add it to the datagrid's TableStyles collection  
       DataGrid1.TableStyles.Add(ts)  
  
       ' Hide the first column (index 0)  
       DataGrid1.TableStyles(0).GridColumnStyles(0).Width = 0  
    End Sub  
    ```  
  
    ```csharp  
    // Declare a new DataGridTableStyle in the  
    // declarations area of your form.  
    DataGridTableStyle ts = new DataGridTableStyle();  
  
    private void hideColumn()  
    {  
       // Set the DataGridTableStyle.MappingName property  
       // to the table in the data source to map to.  
       ts.MappingName = dataGrid1.DataMember;  
  
       // Add it to the datagrid's TableStyles collection  
       dataGrid1.TableStyles.Add(ts);  
  
       // Hide the first column (index 0)  
       dataGrid1.TableStyles[0].GridColumnStyles[0].Width = 0;  
    }  
    ```  
  
## <a name="see-also"></a><span data-ttu-id="d5a05-121">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d5a05-121">See also</span></span>

- [<span data-ttu-id="d5a05-122">Guide pratique pour Modification des données affichées au moment de l’exécution dans le contrôle DataGrid Windows Forms</span><span class="sxs-lookup"><span data-stu-id="d5a05-122">How to: Change Displayed Data at Run Time in the Windows Forms DataGrid Control</span></span>](change-displayed-data-at-run-time-wf-datagrid-control.md)
- [<span data-ttu-id="d5a05-123">Guide pratique pour Ajouter des Tables et des colonnes au contrôle DataGrid Windows Forms</span><span class="sxs-lookup"><span data-stu-id="d5a05-123">How to: Add Tables and Columns to the Windows Forms DataGrid Control</span></span>](how-to-add-tables-and-columns-to-the-windows-forms-datagrid-control.md)
