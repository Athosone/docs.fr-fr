---
title: 'Procédure : accéder à des éléments spécifiques dans un contrôle ComboBox, ListBox ou CheckedListBox Windows Forms'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
- cpp
helpviewer_keywords:
- ComboBox control [Windows Forms], accessing items
- ListBox control [Windows Forms], returning item information
- list boxes [Windows Forms], accessing items
- ListBox control [Windows Forms], accessing items
- combo boxes [Windows Forms], accessing items
- CheckedListBox control [Windows Forms], accessing items
ms.assetid: 1216742f-bcf9-4ff8-8a62-d7c9053c2b96
ms.openlocfilehash: fbdd9168fe286823db7cf066ae0f821b8db88ecb
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62011825"
---
# <a name="how-to-access-specific-items-in-a-windows-forms-combobox-listbox-or-checkedlistbox-control"></a><span data-ttu-id="8b2cd-102">Procédure : accéder à des éléments spécifiques dans un contrôle ComboBox, ListBox ou CheckedListBox Windows Forms</span><span class="sxs-lookup"><span data-stu-id="8b2cd-102">How to: Access Specific Items in a Windows Forms ComboBox, ListBox, or CheckedListBox Control</span></span>
<span data-ttu-id="8b2cd-103">Accès aux éléments d’une zone de liste déroulante Windows Forms, la zone de liste ou la zone de liste vérifiés est une tâche essentielle.</span><span class="sxs-lookup"><span data-stu-id="8b2cd-103">Accessing specific items in a Windows Forms combo box, list box, or checked list box is an essential task.</span></span> <span data-ttu-id="8b2cd-104">Il vous permet de déterminer par programme les nouveautés dans la liste, à n’importe quelle position donnée.</span><span class="sxs-lookup"><span data-stu-id="8b2cd-104">It enables you to programmatically determine what is in a list, at any given position.</span></span>  
  
### <a name="to-access-a-specific-item"></a><span data-ttu-id="8b2cd-105">Pour accéder à un élément spécifique</span><span class="sxs-lookup"><span data-stu-id="8b2cd-105">To access a specific item</span></span>  
  
1. <span data-ttu-id="8b2cd-106">Requête la `Items` collection à l’aide de l’index de l’élément spécifique :</span><span class="sxs-lookup"><span data-stu-id="8b2cd-106">Query the `Items` collection using the index of the specific item:</span></span>  
  
    ```vb  
    Private Function GetItemText(i As Integer) As String  
       ' Return the text of the item using the index:  
       Return ComboBox1.Items(i).ToString  
    End Function  
    ```  
  
    ```csharp  
    private string GetItemText(int i)  
    {  
       // Return the text of the item using the index:  
       return (comboBox1.Items[i].ToString());  
    }  
    ```  
  
    ```cpp  
    private:  
       String^ GetItemText(int i)  
       {  
          // Return the text of the item using the index:  
          return (comboBox1->Items->Item[i]->ToString());  
       }  
    ```  
  
## <a name="see-also"></a><span data-ttu-id="8b2cd-107">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="8b2cd-107">See also</span></span>

- <xref:System.Windows.Forms.ComboBox>
- <xref:System.Windows.Forms.ListBox>
- <xref:System.Windows.Forms.CheckedListBox>
- [<span data-ttu-id="8b2cd-108">Contrôles Windows Forms utilisés pour l’affichage de listes d’options</span><span class="sxs-lookup"><span data-stu-id="8b2cd-108">Windows Forms Controls Used to List Options</span></span>](windows-forms-controls-used-to-list-options.md)
