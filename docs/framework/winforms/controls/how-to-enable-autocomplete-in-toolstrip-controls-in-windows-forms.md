---
title: 'Procédure : Activer la saisie semi-automatique dans les contrôles ToolStrip dans les Windows Forms'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- AutoComplete [Windows Forms], examples
- toolbars [Windows Forms], AutoComplete
- examples [Windows Forms], toolbars
- AutoComplete [Windows Forms], enabling in toolbars
- ToolStripComboBox class [Windows Forms], examples
- ToolStrip control [Windows Forms], AutoComplete
ms.assetid: fd66d085-1af1-45d4-930a-cde944da2e16
ms.openlocfilehash: d7919bf87444ef6c4a64ee236356e762da14853f
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61941477"
---
# <a name="how-to-enable-autocomplete-in-toolstrip-controls-in-windows-forms"></a><span data-ttu-id="3109a-102">Procédure : Activer la saisie semi-automatique dans les contrôles ToolStrip dans les Windows Forms</span><span class="sxs-lookup"><span data-stu-id="3109a-102">How to: Enable AutoComplete in ToolStrip Controls in Windows Forms</span></span>
<span data-ttu-id="3109a-103">La procédure suivante combine un <xref:System.Windows.Forms.ToolStripLabel> avec un <xref:System.Windows.Forms.ToolStripComboBox> qui peut être déplacé vers le bas pour afficher une liste d’éléments, tels que récemment visité les sites Web.</span><span class="sxs-lookup"><span data-stu-id="3109a-103">The following procedure combines a <xref:System.Windows.Forms.ToolStripLabel> with a <xref:System.Windows.Forms.ToolStripComboBox> that can be dropped down to show a list of items, such as recently visited Web sites.</span></span> <span data-ttu-id="3109a-104">Si l’utilisateur tape un caractère qui correspond au premier caractère d’un des éléments dans la liste, l’élément est immédiatement affiché.</span><span class="sxs-lookup"><span data-stu-id="3109a-104">If the user types a character that matches the first character of one of the items in the list, the item is immediately displayed.</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="3109a-105">La saisie semi-automatique fonctionne avec `ToolStrip` contrôles de la même façon qu’il fonctionne avec les contrôles traditionnels, tels que <xref:System.Windows.Forms.ComboBox> et <xref:System.Windows.Forms.TextBox>.</span><span class="sxs-lookup"><span data-stu-id="3109a-105">Automatic completion works with `ToolStrip` controls in the same way that it works with traditional controls such as <xref:System.Windows.Forms.ComboBox> and <xref:System.Windows.Forms.TextBox>.</span></span>  
  
### <a name="to-enable-autocomplete-in-a-toolstrip-control"></a><span data-ttu-id="3109a-106">Pour activer la saisie semi-automatique dans un contrôle ToolStrip</span><span class="sxs-lookup"><span data-stu-id="3109a-106">To enable AutoComplete in a ToolStrip control</span></span>  
  
1. <span data-ttu-id="3109a-107">Créer un <xref:System.Windows.Forms.ToolStrip> contrôler et ajouter des éléments.</span><span class="sxs-lookup"><span data-stu-id="3109a-107">Create a <xref:System.Windows.Forms.ToolStrip> control and add items to it.</span></span>  
  
    ```vb  
    ToolStrip1 = New System.Windows.Forms.ToolStrip  
    ToolStrip1.Items.AddRange(New System.Windows.Forms.ToolStripItem()_  
        {ToolStripLabel1, ToolStripComboBox1})  
    ```  
  
    ```csharp  
    toolStrip1 = new System.Windows.Forms.ToolStrip();  
    toolStrip1.Items.AddRange(new System.Windows.Forms.ToolStripItem[]   
        {toolStripLabel1, toolStripComboBox1});  
    ```  
  
2. <span data-ttu-id="3109a-108">Définir le <xref:System.Windows.Forms.ToolStripItem.Overflow%2A> propriété de l’étiquette et la zone de liste déroulante <xref:System.Windows.Forms.ToolStripItemOverflow.Never> afin que la liste soit toujours disponible, quel que soit la taille du formulaire.</span><span class="sxs-lookup"><span data-stu-id="3109a-108">Set the <xref:System.Windows.Forms.ToolStripItem.Overflow%2A> property of the label and the combo box to <xref:System.Windows.Forms.ToolStripItemOverflow.Never> so that the list is always available regardless of the form's size.</span></span>  
  
    ```vb  
    ToolStripLabel1.Overflow = _  
        System.Windows.Forms.ToolStripItemOverflow.Never  
    ToolStripComboBox1.Overflow = _  
        System.Windows.Forms.ToolStripItemOverflow.Never  
    ```  
  
    ```csharp  
    toolStripLabel1.Overflow = _  
        System.Windows.Forms.ToolStripItemOverflow.Never  
    toolStripComboBox1.Overflow = System.Windows.Forms.ToolStripItemOverflow.Never  
    ```  
  
3. <span data-ttu-id="3109a-109">Ajouter des mots à la collection d’éléments de la <xref:System.Windows.Forms.ToolStripComboBox> contrôle.</span><span class="sxs-lookup"><span data-stu-id="3109a-109">Add words to the Items collection of the <xref:System.Windows.Forms.ToolStripComboBox> control.</span></span>  
  
    ```vb  
    ToolStripComboBox1.Items.AddRange(New Object() {"First Item", _  
        "Second Item", "Third Item"})  
    ```  
  
    ```csharp  
    toolStripComboBox1.Items.AddRange(new object[] {"First item", "Second item", "Third item"});  
    ```  
  
4. <span data-ttu-id="3109a-110">Définir le <xref:System.Windows.Forms.ComboBox.AutoCompleteMode%2A> propriété de la zone de liste déroulante <xref:System.Windows.Forms.AutoCompleteMode.Append>.</span><span class="sxs-lookup"><span data-stu-id="3109a-110">Set the <xref:System.Windows.Forms.ComboBox.AutoCompleteMode%2A> property of the combo box to <xref:System.Windows.Forms.AutoCompleteMode.Append>.</span></span>  
  
    ```vb  
    ToolStripComboBox1.AutoCompleteMode = _  
        System.Windows.Forms.AutoCompleteMode.Append  
    ```  
  
    ```csharp  
    toolStripComboBox1.AutoCompleteMode = System.Windows.Forms.AutoCompleteMode.Append;  
    ```  
  
5. <span data-ttu-id="3109a-111">Définir le <xref:System.Windows.Forms.ComboBox.AutoCompleteSource%2A> propriété de la zone de liste déroulante <xref:System.Windows.Forms.AutoCompleteSource.ListItems>.</span><span class="sxs-lookup"><span data-stu-id="3109a-111">Set the <xref:System.Windows.Forms.ComboBox.AutoCompleteSource%2A> property of the combo box to <xref:System.Windows.Forms.AutoCompleteSource.ListItems>.</span></span>  
  
    ```vb  
    ToolStripComboBox1.AutoCompleteSource = _  
        System.Windows.Forms.AutoCompleteSource.ListItems  
    ```  
  
    ```csharp  
    toolStripComboBox1.AutoCompleteSource = System.Windows.Forms.AutoCompleteSource.ListItems;  
    ```  
  
## <a name="see-also"></a><span data-ttu-id="3109a-112">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="3109a-112">See also</span></span>

- <xref:System.Windows.Forms.ToolStrip>
- <xref:System.Windows.Forms.ToolStripLabel>
- <xref:System.Windows.Forms.ToolStripComboBox>
- <xref:System.Windows.Forms.ToolStripComboBox.AutoCompleteMode%2A>
- <xref:System.Windows.Forms.ToolStripComboBox.AutoCompleteSource%2A>
- [<span data-ttu-id="3109a-113">Vue d’ensemble du contrôle ToolStrip</span><span class="sxs-lookup"><span data-stu-id="3109a-113">ToolStrip Control Overview</span></span>](toolstrip-control-overview-windows-forms.md)
- [<span data-ttu-id="3109a-114">Architecture du contrôle ToolStrip</span><span class="sxs-lookup"><span data-stu-id="3109a-114">ToolStrip Control Architecture</span></span>](toolstrip-control-architecture.md)
- [<span data-ttu-id="3109a-115">Résumé de la technologie ToolStrip</span><span class="sxs-lookup"><span data-stu-id="3109a-115">ToolStrip Technology Summary</span></span>](toolstrip-technology-summary.md)
