---
title: 'Procédure : exécuter des opérations glisser-déplacer entre des applications'
ms.date: 03/30/2017
helpviewer_keywords:
- drag and drop [Windows Forms], between applications
ms.assetid: fa347436-2b12-4dd6-8507-59d7241f6a06
ms.openlocfilehash: 9aac3a0efd6359c25a6972f0e0b52dd489ec31db
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59327527"
---
# <a name="how-to-perform-drag-and-drop-operations-between-applications"></a><span data-ttu-id="710b2-102">Procédure : exécuter des opérations glisser-déplacer entre des applications</span><span class="sxs-lookup"><span data-stu-id="710b2-102">How to: Perform Drag-and-Drop Operations Between Applications</span></span>
<span data-ttu-id="710b2-103">L’exécution d’opérations de glisser-déposer entre applications revient à activer cette action dans une application, du moment que les deux applications concernées respectent le "contrat" établi entre les propriétés <xref:System.Windows.Forms.DragEventArgs.AllowedEffect%2A> et <xref:System.Windows.Forms.DragEventArgs.Effect%2A>.</span><span class="sxs-lookup"><span data-stu-id="710b2-103">Performing drag-and-drop operations between applications is no different than enabling this action within an application, as long as both applications involved behave according to the "contract" established between the <xref:System.Windows.Forms.DragEventArgs.AllowedEffect%2A> and <xref:System.Windows.Forms.DragEventArgs.Effect%2A> properties.</span></span>  
  
 <span data-ttu-id="710b2-104">Dans la procédure suivante, vous allez utiliser une application Windows que vous aurez créée, ainsi que le traitement de texte WordPad fourni avec le système d'exploitation Windows pour effectuer des opérations de glisser-déplacer entre applications.</span><span class="sxs-lookup"><span data-stu-id="710b2-104">In the following procedure, you will use a Windows-based application you create and the WordPad word processor that is included with the Windows operating system to perform drag-and-drop operations between applications.</span></span> <span data-ttu-id="710b2-105">WordPad possède un ensemble d'effets autorisés pour le texte faisant l'objet du glisser-déplacer. L'application Windows pour laquelle vous allez écrire du code utilisera ces effets pour que les opérations de glisser-déplacer se déroulent correctement.</span><span class="sxs-lookup"><span data-stu-id="710b2-105">WordPad has a certain set of allowed effects for text being dragged and dropped; the Windows-based application you will write code for will work with these effects so that drag-and-drop operations may be completed successfully.</span></span>  
  
### <a name="to-perform-a-drag-and-drop-procedure-between-applications"></a><span data-ttu-id="710b2-106">Pour effectuer une opération de glisser-déplacer entre applications</span><span class="sxs-lookup"><span data-stu-id="710b2-106">To perform a drag-and-drop procedure between applications</span></span>  
  
1. <span data-ttu-id="710b2-107">Créez une application Windows Forms.</span><span class="sxs-lookup"><span data-stu-id="710b2-107">Create a new Windows Forms application.</span></span>  
  
2. <span data-ttu-id="710b2-108">Ajoutez un contrôle <xref:System.Windows.Forms.TextBox> à votre formulaire.</span><span class="sxs-lookup"><span data-stu-id="710b2-108">Add a <xref:System.Windows.Forms.TextBox> control to your form.</span></span>  
  
3. <span data-ttu-id="710b2-109">Configurez le contrôle <xref:System.Windows.Forms.TextBox> pour recevoir les données déposées.</span><span class="sxs-lookup"><span data-stu-id="710b2-109">Configure the <xref:System.Windows.Forms.TextBox> control to receive dropped data.</span></span>  
  
     <span data-ttu-id="710b2-110">Pour plus d’informations, consultez [Procédure pas à pas : Exécution d’une opération de glisser-déplacer dans les Windows Forms](walkthrough-performing-a-drag-and-drop-operation-in-windows-forms.md).</span><span class="sxs-lookup"><span data-stu-id="710b2-110">For more information, see [Walkthrough: Performing a Drag-and-Drop Operation in Windows Forms](walkthrough-performing-a-drag-and-drop-operation-in-windows-forms.md).</span></span>  
  
4. <span data-ttu-id="710b2-111">Exécutez votre application Windows et pendant que celle-ci s'exécute, exécutez WordPad.</span><span class="sxs-lookup"><span data-stu-id="710b2-111">Run your Windows-based application, and while the application is running, run WordPad.</span></span>  
  
     <span data-ttu-id="710b2-112">WordPad est un éditeur de texte installé par Windows qui permet les opérations de glisser-déplacer.</span><span class="sxs-lookup"><span data-stu-id="710b2-112">WordPad is a text editor installed by Windows that allows drag-and-drop operations.</span></span> <span data-ttu-id="710b2-113">Il est accessible en appuyant sur la **Démarrer** bouton, en sélectionnant **exécuter**, puis en tapant `WordPad` dans la zone de texte de la **exécuter** boîte de dialogue et en cliquant sur **OK**.</span><span class="sxs-lookup"><span data-stu-id="710b2-113">It is accessible by pressing the **Start** button, selecting **Run**, and then typing `WordPad` into the text box of the **Run** dialog box and clicking **OK**.</span></span>  
  
5. <span data-ttu-id="710b2-114">Une fois que WordPad est ouvert, tapez une chaîne de texte.</span><span class="sxs-lookup"><span data-stu-id="710b2-114">Once WordPad is open, type a string of text into it.</span></span>  
  
6. <span data-ttu-id="710b2-115">À l'aide de la souris, sélectionnez le texte, puis faites glisser le texte sélectionné vers le contrôle <xref:System.Windows.Forms.TextBox> dans votre application Windows.</span><span class="sxs-lookup"><span data-stu-id="710b2-115">Using the mouse, select the text, and then drag the selected text over to the <xref:System.Windows.Forms.TextBox> control in your Windows-based application.</span></span>  
  
     <span data-ttu-id="710b2-116">Notez que quand vous placez la souris sur le contrôle <xref:System.Windows.Forms.TextBox> (et déclenchez donc l'événement <xref:System.Windows.Forms.Control.DragEnter>), le curseur se transforme et vous pouvez placer le texte sélectionné dans le contrôle <xref:System.Windows.Forms.TextBox>.</span><span class="sxs-lookup"><span data-stu-id="710b2-116">Observe that when you mouse over the <xref:System.Windows.Forms.TextBox> control (and, consequently, raise the <xref:System.Windows.Forms.Control.DragEnter> event), the cursor changes, and you can drop the selected text into the <xref:System.Windows.Forms.TextBox> control.</span></span>  
  
     <span data-ttu-id="710b2-117">En outre, vous pouvez configurer le contrôle <xref:System.Windows.Forms.TextBox> pour permettre le glisser-déplacer des chaînes de texte dans WordPad.</span><span class="sxs-lookup"><span data-stu-id="710b2-117">Additionally, you can configure your <xref:System.Windows.Forms.TextBox> control to allow text strings to be dragged and dropped into WordPad.</span></span> <span data-ttu-id="710b2-118">Pour plus d’informations, consultez [Procédure pas à pas : Exécution d’une opération de glisser-déplacer dans les Windows Forms](walkthrough-performing-a-drag-and-drop-operation-in-windows-forms.md).</span><span class="sxs-lookup"><span data-stu-id="710b2-118">For more information, see [Walkthrough: Performing a Drag-and-Drop Operation in Windows Forms](walkthrough-performing-a-drag-and-drop-operation-in-windows-forms.md).</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="710b2-119">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="710b2-119">See also</span></span>

- [<span data-ttu-id="710b2-120">Guide pratique pour Ajouter des données dans le Presse-papiers</span><span class="sxs-lookup"><span data-stu-id="710b2-120">How to: Add Data to the Clipboard</span></span>](how-to-add-data-to-the-clipboard.md)
- [<span data-ttu-id="710b2-121">Guide pratique pour Récupérer des données à partir du Presse-papiers</span><span class="sxs-lookup"><span data-stu-id="710b2-121">How to: Retrieve Data from the Clipboard</span></span>](how-to-retrieve-data-from-the-clipboard.md)
- [<span data-ttu-id="710b2-122">Opérations glisser-déposer et prise en charge du Presse-papiers</span><span class="sxs-lookup"><span data-stu-id="710b2-122">Drag-and-Drop Operations and Clipboard Support</span></span>](drag-and-drop-operations-and-clipboard-support.md)
