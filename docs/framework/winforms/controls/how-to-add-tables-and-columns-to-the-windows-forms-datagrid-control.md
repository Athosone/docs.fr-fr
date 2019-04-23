---
title: 'Procédure : ajouter des tables et des colonnes au contrôle DataGrid Windows Forms'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
- cpp
helpviewer_keywords:
- columns [Windows Forms], adding to DataGrid control
- tables [Windows Forms], adding to DataGrid control
- DataGrid control [Windows Forms], adding tables and columns
ms.assetid: 2fe661b9-aa06-49b9-a314-a0d3cbfdcb4d
ms.openlocfilehash: cc364f3609f8041378b0b03b8e1bc8f312fade18
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59319909"
---
# <a name="how-to-add-tables-and-columns-to-the-windows-forms-datagrid-control"></a><span data-ttu-id="e4bf2-102">Procédure : ajouter des tables et des colonnes au contrôle DataGrid Windows Forms</span><span class="sxs-lookup"><span data-stu-id="e4bf2-102">How to: Add Tables and Columns to the Windows Forms DataGrid Control</span></span>
> [!NOTE]
>  <span data-ttu-id="e4bf2-103">Le contrôle <xref:System.Windows.Forms.DataGridView> remplace le contrôle <xref:System.Windows.Forms.DataGrid> et lui ajoute des fonctionnalités ; toutefois, le contrôle <xref:System.Windows.Forms.DataGrid> est conservé pour la compatibilité descendante et l'utilisation future si tel est votre choix.</span><span class="sxs-lookup"><span data-stu-id="e4bf2-103">The <xref:System.Windows.Forms.DataGridView> control replaces and adds functionality to the <xref:System.Windows.Forms.DataGrid> control; however, the <xref:System.Windows.Forms.DataGrid> control is retained for both backward compatibility and future use, if you choose.</span></span> <span data-ttu-id="e4bf2-104">Pour plus d’informations, consultez [Différences entre les contrôles DataGridView et DataGrid Windows Forms](differences-between-the-windows-forms-datagridview-and-datagrid-controls.md).</span><span class="sxs-lookup"><span data-stu-id="e4bf2-104">For more information, see [Differences Between the Windows Forms DataGridView and DataGrid Controls](differences-between-the-windows-forms-datagridview-and-datagrid-controls.md).</span></span>  
  
 <span data-ttu-id="e4bf2-105">Vous pouvez afficher des données dans les formulaires Windows <xref:System.Windows.Forms.DataGrid> contrôle dans les tables et colonnes en créant **DataGridTableStyle** objets et en les ajoutant à la **GridTableStylesCollection** objet, qui est accessible via la <xref:System.Windows.Forms.DataGrid> du contrôle **TableStyles** propriété.</span><span class="sxs-lookup"><span data-stu-id="e4bf2-105">You can display data in the Windows Forms <xref:System.Windows.Forms.DataGrid> control in tables and columns by creating **DataGridTableStyle** objects and adding them to the **GridTableStylesCollection** object, which is accessed through the <xref:System.Windows.Forms.DataGrid> control's **TableStyles** property.</span></span> <span data-ttu-id="e4bf2-106">Chaque style de table affiche le contenu de toute table de données spécifiée dans le **DataGridTableStyle** l’objet **MappingName** propriété.</span><span class="sxs-lookup"><span data-stu-id="e4bf2-106">Each table style displays the contents of whatever data table is specified in the **DataGridTableStyle** object's **MappingName** property.</span></span> <span data-ttu-id="e4bf2-107">Par défaut, un style de table sans style de colonne spécifié affiche toutes les colonnes des table de données.</span><span class="sxs-lookup"><span data-stu-id="e4bf2-107">By default, a table style with no column styles specified will display all the columns within that data table.</span></span> <span data-ttu-id="e4bf2-108">Vous pouvez limiter les colonnes de la table s’affichent en ajoutant **DataGridColumnStyle** des objets sur le **GridColumnStylesCollection** objet, qui est accessible via la  **GridColumnStyles** propriété de chaque **DataGridTableStyle** objet.</span><span class="sxs-lookup"><span data-stu-id="e4bf2-108">You can restrict which columns from the table appear by adding **DataGridColumnStyle** objects to the **GridColumnStylesCollection** object, which is accessed through the **GridColumnStyles** property of each **DataGridTableStyle** object.</span></span>  
  
### <a name="to-add-a-table-and-column-to-a-datagrid-programmatically"></a><span data-ttu-id="e4bf2-109">Pour ajouter par programmation une table et une colonne à un contrôle DataGrid</span><span class="sxs-lookup"><span data-stu-id="e4bf2-109">To add a table and column to a DataGrid programmatically</span></span>  
  
1. <span data-ttu-id="e4bf2-110">Pour afficher des données dans la table, vous devez d’abord lier le <xref:System.Windows.Forms.DataGrid> contrôle à un jeu de données.</span><span class="sxs-lookup"><span data-stu-id="e4bf2-110">In order to display data in the table, you must first bind the <xref:System.Windows.Forms.DataGrid> control to a dataset.</span></span> <span data-ttu-id="e4bf2-111">Pour plus d'informations, voir [Procédure : Lier le contrôle DataGrid Windows Forms à une Source de données](how-to-bind-the-windows-forms-datagrid-control-to-a-data-source.md).</span><span class="sxs-lookup"><span data-stu-id="e4bf2-111">For more information, see [How to: Bind the Windows Forms DataGrid Control to a Data Source](how-to-bind-the-windows-forms-datagrid-control-to-a-data-source.md).</span></span>  
  
    > [!CAUTION]
    >  <span data-ttu-id="e4bf2-112">Lorsque vous spécifiez par programme des styles de colonne, vous devez toujours créer **DataGridColumnStyle** objets et les ajouter à la **GridColumnStylesCollection** objet avant d’ajouter  **DataGridTableStyle** des objets sur le **GridTableStylesCollection** objet.</span><span class="sxs-lookup"><span data-stu-id="e4bf2-112">When programmatically specifying column styles, always create **DataGridColumnStyle** objects and add them to the **GridColumnStylesCollection** object before adding **DataGridTableStyle** objects to the **GridTableStylesCollection** object.</span></span> <span data-ttu-id="e4bf2-113">Lorsque vous ajoutez un vide **DataGridTableStyle** objet à la collection, **DataGridColumnStyle** objets sont générés automatiquement pour vous.</span><span class="sxs-lookup"><span data-stu-id="e4bf2-113">When you add an empty **DataGridTableStyle** object to the collection, **DataGridColumnStyle** objects are automatically generated for you.</span></span> <span data-ttu-id="e4bf2-114">Par conséquent, une exception sera levée si vous essayez d’ajouter de nouveaux **DataGridColumnStyle** objets en double **MappingName** valeurs à la **GridColumnStylesCollection**objet.</span><span class="sxs-lookup"><span data-stu-id="e4bf2-114">Consequently, an exception will be thrown if you try to add new **DataGridColumnStyle** objects with duplicate **MappingName** values to the **GridColumnStylesCollection** object.</span></span>  
  
2. <span data-ttu-id="e4bf2-115">Déclarez un nouveau style de table et définissez son nom de mappage.</span><span class="sxs-lookup"><span data-stu-id="e4bf2-115">Declare a new table style and set its mapping name.</span></span>  
  
    ```vb  
    Dim ts1 As New DataGridTableStyle()  
    ts1.MappingName = "Customers"  
    ```  
  
    ```csharp  
    DataGridTableStyle ts1 = new DataGridTableStyle();  
    ts1.MappingName = "Customers";  
    ```  
  
    ```cpp  
    DataGridTableStyle* ts1 = new DataGridTableStyle();  
    ts1->MappingName = S"Customers";  
    ```  
  
3. <span data-ttu-id="e4bf2-116">Déclarez un nouveau style de colonne et définir son nom de mappage et d’autres propriétés.</span><span class="sxs-lookup"><span data-stu-id="e4bf2-116">Declare a new column style and set its mapping name and other properties.</span></span>  
  
    ```vb  
    Dim myDataCol As New DataGridBoolColumn()  
    myDataCol.HeaderText = "My New Column"  
    myDataCol.MappingName = "Current"  
    ```  
  
    ```csharp  
    DataGridBoolColumn myDataCol = new DataGridBoolColumn();  
    myDataCol.HeaderText = "My New Column";  
    myDataCol.MappingName = "Current";  
    ```  
  
    ```cpp  
    DataGridBoolColumn^ myDataCol = gcnew DataGridBoolColumn();  
    myDataCol->HeaderText = "My New Column";  
    myDataCol->MappingName = "Current";  
    ```  
  
4. <span data-ttu-id="e4bf2-117">Appelez le **ajouter** méthode de la **GridColumnStylesCollection** objet à ajouter la colonne au style de table</span><span class="sxs-lookup"><span data-stu-id="e4bf2-117">Call the **Add** method of the **GridColumnStylesCollection** object to add the column to the table style</span></span>  
  
    ```vb  
    ts1.GridColumnStyles.Add(myDataCol)  
    ```  
  
    ```csharp  
    ts1.GridColumnStyles.Add(myDataCol);  
    ```  
  
    ```cpp  
    ts1->GridColumnStyles->Add(myDataCol);  
    ```  
  
5. <span data-ttu-id="e4bf2-118">Appelez le **ajouter** méthode de la **GridTableStylesCollection** objet à ajouter le style de table à la grille de données.</span><span class="sxs-lookup"><span data-stu-id="e4bf2-118">Call the **Add** method of the **GridTableStylesCollection** object to add the table style to the data grid.</span></span>  
  
    ```vb  
    DataGrid1.TableStyles.Add(ts1)  
    ```  
  
    ```csharp  
    dataGrid1.TableStyles.Add(ts1);  
    ```  
  
    ```cpp  
    dataGrid1->TableStyles->Add(ts1);  
    ```  
  
## <a name="see-also"></a><span data-ttu-id="e4bf2-119">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e4bf2-119">See also</span></span>

- [<span data-ttu-id="e4bf2-120">DataGrid, contrôle</span><span class="sxs-lookup"><span data-stu-id="e4bf2-120">DataGrid Control</span></span>](datagrid-control-windows-forms.md)
- [<span data-ttu-id="e4bf2-121">Guide pratique pour Supprimer ou masquer des colonnes dans le contrôle DataGrid Windows Forms</span><span class="sxs-lookup"><span data-stu-id="e4bf2-121">How to: Delete or Hide Columns in the Windows Forms DataGrid Control</span></span>](how-to-delete-or-hide-columns-in-the-windows-forms-datagrid-control.md)
