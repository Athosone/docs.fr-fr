---
title: 'Procédure : sélectionner du texte dans le contrôle TextBox Windows Forms'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
- cpp
helpviewer_keywords:
- TextBox control [Windows Forms], selecting text programmatically
- text boxes [Windows Forms], selecting text programmatically
- text [Windows Forms], selecting in text boxes programmatically
ms.assetid: 8c591546-6a01-45c7-8e03-f78431f903b1
ms.openlocfilehash: 3bb1245cd47084935d632ff345a32058db6074e1
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62013294"
---
# <a name="how-to-select-text-in-the-windows-forms-textbox-control"></a><span data-ttu-id="c8048-102">Procédure : sélectionner du texte dans le contrôle TextBox Windows Forms</span><span class="sxs-lookup"><span data-stu-id="c8048-102">How to: Select Text in the Windows Forms TextBox Control</span></span>
<span data-ttu-id="c8048-103">Vous pouvez sélectionner le texte par programmation dans les formulaires Windows <xref:System.Windows.Forms.TextBox> contrôle.</span><span class="sxs-lookup"><span data-stu-id="c8048-103">You can select text programmatically in the Windows Forms <xref:System.Windows.Forms.TextBox> control.</span></span> <span data-ttu-id="c8048-104">Par exemple, si vous créez une fonction qui recherche du texte pour une chaîne particulière, vous pouvez sélectionner le texte afin d’alerter visuellement le lecteur de position de la chaîne trouvée.</span><span class="sxs-lookup"><span data-stu-id="c8048-104">For example, if you create a function that searches text for a particular string, you can select the text to visually alert the reader of the found string's position.</span></span>  
  
### <a name="to-select-text-programmatically"></a><span data-ttu-id="c8048-105">Pour sélectionner le texte par programmation</span><span class="sxs-lookup"><span data-stu-id="c8048-105">To select text programmatically</span></span>  
  
1. <span data-ttu-id="c8048-106">Définir le <xref:System.Windows.Forms.TextBoxBase.SelectionStart%2A> propriété vers le début du texte que vous souhaitez sélectionner.</span><span class="sxs-lookup"><span data-stu-id="c8048-106">Set the <xref:System.Windows.Forms.TextBoxBase.SelectionStart%2A> property to the beginning of the text you want to select.</span></span>  
  
     <span data-ttu-id="c8048-107">Le <xref:System.Windows.Forms.TextBoxBase.SelectionStart%2A> propriété est un nombre qui indique le point d’insertion dans la chaîne de texte, 0 étant la position la plus à gauche.</span><span class="sxs-lookup"><span data-stu-id="c8048-107">The <xref:System.Windows.Forms.TextBoxBase.SelectionStart%2A> property is a number that indicates the insertion point within the string of text, with 0 being the left-most position.</span></span> <span data-ttu-id="c8048-108">Si la <xref:System.Windows.Forms.TextBoxBase.SelectionStart%2A> est définie sur une valeur égale ou supérieure au nombre de caractères dans la zone de texte, le point d’insertion est placé après le dernier caractère.</span><span class="sxs-lookup"><span data-stu-id="c8048-108">If the <xref:System.Windows.Forms.TextBoxBase.SelectionStart%2A> property is set to a value equal to or greater than the number of characters in the text box, the insertion point is placed after the last character.</span></span>  
  
2. <span data-ttu-id="c8048-109">Définir le <xref:System.Windows.Forms.TextBoxBase.SelectionLength%2A> propriété à la longueur du texte que vous souhaitez sélectionner.</span><span class="sxs-lookup"><span data-stu-id="c8048-109">Set the <xref:System.Windows.Forms.TextBoxBase.SelectionLength%2A> property to the length of the text you want to select.</span></span>  
  
     <span data-ttu-id="c8048-110">Le <xref:System.Windows.Forms.TextBoxBase.SelectionLength%2A> propriété est une valeur numérique qui définit la largeur du point d’insertion.</span><span class="sxs-lookup"><span data-stu-id="c8048-110">The <xref:System.Windows.Forms.TextBoxBase.SelectionLength%2A> property is a numeric value that sets the width of the insertion point.</span></span> <span data-ttu-id="c8048-111">Définition de la <xref:System.Windows.Forms.TextBoxBase.SelectionLength%2A> par un nombre supérieur à 0 ce nombre de caractères à sélectionner, en commençant à partir du point d’insertion actuel.</span><span class="sxs-lookup"><span data-stu-id="c8048-111">Setting the <xref:System.Windows.Forms.TextBoxBase.SelectionLength%2A> to a number greater than 0 causes that number of characters to be selected, starting from the current insertion point.</span></span>  
  
3. <span data-ttu-id="c8048-112">(Facultatif) Accéder au texte sélectionné via la <xref:System.Windows.Forms.TextBoxBase.SelectedText%2A> propriété.</span><span class="sxs-lookup"><span data-stu-id="c8048-112">(Optional) Access the selected text through the <xref:System.Windows.Forms.TextBoxBase.SelectedText%2A> property.</span></span>  
  
     <span data-ttu-id="c8048-113">Le code ci-dessous sélectionne le contenu d’un texte boîte lorsque le contrôle <xref:System.Windows.Forms.Control.Enter> événement se produit.</span><span class="sxs-lookup"><span data-stu-id="c8048-113">The code below selects the contents of a text box when the control's <xref:System.Windows.Forms.Control.Enter> event occurs.</span></span> <span data-ttu-id="c8048-114">Cet exemple vérifie si la zone de texte a une valeur pour le <xref:System.Windows.Forms.TextBox.Text%2A> propriété qui n’est pas `null` ou une chaîne vide.</span><span class="sxs-lookup"><span data-stu-id="c8048-114">This example checks if the text box has a value for the <xref:System.Windows.Forms.TextBox.Text%2A> property that is not `null` or an empty string.</span></span> <span data-ttu-id="c8048-115">Lorsque la zone de texte reçoit le focus, le texte actuel dans la zone de texte est sélectionné.</span><span class="sxs-lookup"><span data-stu-id="c8048-115">When the text box receives the focus, the current text in the text box is selected.</span></span> <span data-ttu-id="c8048-116">Le `TextBox1_Enter` Gestionnaire d’événements doit être lié au contrôle ; pour plus d’informations, consultez [Comment : Créer des gestionnaires d’événements en cours d’exécution pour les Windows Forms](../how-to-create-event-handlers-at-run-time-for-windows-forms.md).</span><span class="sxs-lookup"><span data-stu-id="c8048-116">The `TextBox1_Enter` event handler must be bound to the control; for more information, see [How to: Create Event Handlers at Run Time for Windows Forms](../how-to-create-event-handlers-at-run-time-for-windows-forms.md).</span></span>  
  
     <span data-ttu-id="c8048-117">Pour tester cet exemple, appuyez sur la touche Tab jusqu'à ce que la zone de texte a le focus.</span><span class="sxs-lookup"><span data-stu-id="c8048-117">To test this example, press the Tab key until the text box has the focus.</span></span> <span data-ttu-id="c8048-118">Si vous cliquez dans la zone de texte, le texte est désélectionné.</span><span class="sxs-lookup"><span data-stu-id="c8048-118">If you click in the text box, the text is unselected.</span></span>  
  
    ```vb  
    Private Sub TextBox1_Enter(ByVal sender As Object, ByVal e As System.EventArgs) Handles TextBox1.Enter  
       If (Not String.IsNullOrEmpty(TextBox1.Text)) Then  
          TextBox1.SelectionStart = 0  
          TextBox1.SelectionLength = TextBox1.Text.Length  
       End If  
    End Sub  
    ```  
  
    ```csharp  
    private void textBox1_Enter(object sender, System.EventArgs e){  
       if (!String.IsNullOrEmpty(textBox1.Text))  
       {  
          textBox1.SelectionStart = 0;  
          textBox1.SelectionLength = textBox1.Text.Length;  
       }  
    }  
    ```  
  
    ```cpp  
    private:  
       void textBox1_Enter(System::Object ^ sender,  
          System::EventArgs ^ e) {  
       if (!System::String::IsNullOrEmpty(textBox1->Text))  
       {  
          textBox1->SelectionStart = 0;  
          textBox1->SelectionLength = textBox1->Text->Length;  
       }  
    }  
    ```  
  
## <a name="see-also"></a><span data-ttu-id="c8048-119">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c8048-119">See also</span></span>

- <xref:System.Windows.Forms.TextBox>
- [<span data-ttu-id="c8048-120">Vue d’ensemble du contrôle TextBox</span><span class="sxs-lookup"><span data-stu-id="c8048-120">TextBox Control Overview</span></span>](textbox-control-overview-windows-forms.md)
- [<span data-ttu-id="c8048-121">Guide pratique pour Contrôler le Point d’Insertion dans un contrôle de zone de texte Windows Forms</span><span class="sxs-lookup"><span data-stu-id="c8048-121">How to: Control the Insertion Point in a Windows Forms TextBox Control</span></span>](how-to-control-the-insertion-point-in-a-windows-forms-textbox-control.md)
- [<span data-ttu-id="c8048-122">Guide pratique pour Créer une zone de texte mot de passe avec le contrôle de zone de texte Windows Forms</span><span class="sxs-lookup"><span data-stu-id="c8048-122">How to: Create a Password Text Box with the Windows Forms TextBox Control</span></span>](how-to-create-a-password-text-box-with-the-windows-forms-textbox-control.md)
- [<span data-ttu-id="c8048-123">Guide pratique pour Créer une zone de texte en lecture seule</span><span class="sxs-lookup"><span data-stu-id="c8048-123">How to: Create a Read-Only Text Box</span></span>](how-to-create-a-read-only-text-box-windows-forms.md)
- [<span data-ttu-id="c8048-124">Guide pratique pour Placez des guillemets doubles dans une chaîne</span><span class="sxs-lookup"><span data-stu-id="c8048-124">How to: Put Quotation Marks in a String</span></span>](how-to-put-quotation-marks-in-a-string-windows-forms.md)
- [<span data-ttu-id="c8048-125">Guide pratique pour Afficher plusieurs lignes dans le contrôle de zone de texte Windows Forms</span><span class="sxs-lookup"><span data-stu-id="c8048-125">How to: View Multiple Lines in the Windows Forms TextBox Control</span></span>](how-to-view-multiple-lines-in-the-windows-forms-textbox-control.md)
- [<span data-ttu-id="c8048-126">TextBox, contrôle</span><span class="sxs-lookup"><span data-stu-id="c8048-126">TextBox Control</span></span>](textbox-control-windows-forms.md)
