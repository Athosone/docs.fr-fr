---
title: 'Procédure : créer une interface utilisateur à plusieurs volets avec Windows Forms'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- SplitContainer control [Windows Forms], examples
- ListView control [Windows Forms], examples
- RichTextBox control [Windows Forms], examples
- Panel control [Windows Forms], examples
- TreeView control [Windows Forms], examples
- Splitter control [Windows Forms], examples
ms.assetid: e79f6bcc-3740-4d1e-b46a-c5594d9b7327
ms.openlocfilehash: 8650ba3b8011e50779080e31d94727609f2d08f1
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59315152"
---
# <a name="how-to-create-a-multipane-user-interface-with-windows-forms"></a><span data-ttu-id="16f4f-102">Procédure : créer une interface utilisateur à plusieurs volets avec Windows Forms</span><span class="sxs-lookup"><span data-stu-id="16f4f-102">How to: Create a Multipane User Interface with Windows Forms</span></span>
<span data-ttu-id="16f4f-103">Dans la procédure suivante, vous allez créer une interface utilisateur à plusieurs volets semblable à celle utilisée dans Microsoft Outlook, avec un **dossier** liste, un **Messages** volet et un **aperçu** volet.</span><span class="sxs-lookup"><span data-stu-id="16f4f-103">In the following procedure, you will create a multipane user interface that is similar to the one used in Microsoft Outlook, with a **Folder** list, a **Messages** pane, and a **Preview** pane.</span></span> <span data-ttu-id="16f4f-104">Cette disposition est obtenue principalement en ancrant les contrôles dans le formulaire.</span><span class="sxs-lookup"><span data-stu-id="16f4f-104">This arrangement is achieved chiefly through docking controls with the form.</span></span>  
  
 <span data-ttu-id="16f4f-105">Lorsque vous ancrez un contrôle, vous déterminez le bord du conteneur parent auquel un contrôle est attaché.</span><span class="sxs-lookup"><span data-stu-id="16f4f-105">When you dock a control, you determine which edge of the parent container a control is fastened to.</span></span> <span data-ttu-id="16f4f-106">Par conséquent, si vous définissez la <xref:System.Windows.Forms.SplitContainer.Dock%2A> propriété <xref:System.Windows.Forms.DockStyle.Right>, le bord droit du contrôle sera ancré sur le bord droit de son contrôle parent.</span><span class="sxs-lookup"><span data-stu-id="16f4f-106">Thus, if you set the <xref:System.Windows.Forms.SplitContainer.Dock%2A> property to <xref:System.Windows.Forms.DockStyle.Right>, the right edge of the control will be docked to the right edge of its parent control.</span></span> <span data-ttu-id="16f4f-107">En outre, le bord du contrôle ancré est redimensionné pour correspondre à celle de son contrôle conteneur.</span><span class="sxs-lookup"><span data-stu-id="16f4f-107">Additionally, the docked edge of the control is resized to match that of its container control.</span></span> <span data-ttu-id="16f4f-108">Pour plus d’informations sur la façon dont <xref:System.Windows.Forms.SplitContainer.Dock%2A> fonctionne de la propriété, consultez [Comment : Ancrer des contrôles aux Windows Forms](how-to-dock-controls-on-windows-forms.md).</span><span class="sxs-lookup"><span data-stu-id="16f4f-108">For more information about how the <xref:System.Windows.Forms.SplitContainer.Dock%2A> property works, see [How to: Dock Controls on Windows Forms](how-to-dock-controls-on-windows-forms.md).</span></span>  
  
 <span data-ttu-id="16f4f-109">Cette procédure se concentre sur la disposition du <xref:System.Windows.Forms.SplitContainer> et d’autres contrôles sur le formulaire, et non sur l’ajout de fonctionnalités pour que l’application ressemble à Microsoft Outlook.</span><span class="sxs-lookup"><span data-stu-id="16f4f-109">This procedure focuses on arranging the <xref:System.Windows.Forms.SplitContainer> and the other controls on the form, not on adding functionality to make the application mimic Microsoft Outlook.</span></span>  
  
 <span data-ttu-id="16f4f-110">Pour créer cette interface utilisateur, vous placez tous les contrôles dans un <xref:System.Windows.Forms.SplitContainer> contrôle, qui contient un <xref:System.Windows.Forms.TreeView> contrôle dans le volet gauche.</span><span class="sxs-lookup"><span data-stu-id="16f4f-110">To create this user interface, you place all the controls within a <xref:System.Windows.Forms.SplitContainer> control, which contains a <xref:System.Windows.Forms.TreeView> control in the left-hand panel.</span></span> <span data-ttu-id="16f4f-111">Le volet de droite de la <xref:System.Windows.Forms.SplitContainer> contrôle contient une seconde <xref:System.Windows.Forms.SplitContainer> contrôler avec un <xref:System.Windows.Forms.ListView> contrôle ci-dessus un <xref:System.Windows.Forms.RichTextBox> contrôle.</span><span class="sxs-lookup"><span data-stu-id="16f4f-111">The right-hand panel of the <xref:System.Windows.Forms.SplitContainer> control contains a second <xref:System.Windows.Forms.SplitContainer> control with a <xref:System.Windows.Forms.ListView> control above a <xref:System.Windows.Forms.RichTextBox> control.</span></span> <span data-ttu-id="16f4f-112">Ces <xref:System.Windows.Forms.SplitContainer> les contrôles permettent un redimensionnement indépendant des autres contrôles sur le formulaire.</span><span class="sxs-lookup"><span data-stu-id="16f4f-112">These <xref:System.Windows.Forms.SplitContainer> controls enable independent resizing of the other controls on the form.</span></span> <span data-ttu-id="16f4f-113">Vous pouvez adapter les techniques de cette procédure pour les interfaces utilisateur personnalisées de métier de votre choix.</span><span class="sxs-lookup"><span data-stu-id="16f4f-113">You can adapt the techniques in this procedure to craft custom user interfaces of your own.</span></span>  
  
### <a name="to-create-an-outlook-style-user-interface-programmatically"></a><span data-ttu-id="16f4f-114">Pour créer une interface utilisateur de type Outlook par programmation</span><span class="sxs-lookup"><span data-stu-id="16f4f-114">To create an Outlook-style user interface programmatically</span></span>  
  
1. <span data-ttu-id="16f4f-115">Dans un formulaire, déclarez chaque contrôle constituant votre interface utilisateur.</span><span class="sxs-lookup"><span data-stu-id="16f4f-115">Within a form, declare each control that comprises your user interface.</span></span> <span data-ttu-id="16f4f-116">Pour cet exemple, utilisez le <xref:System.Windows.Forms.TreeView>, <xref:System.Windows.Forms.ListView>, <xref:System.Windows.Forms.SplitContainer>, et <xref:System.Windows.Forms.RichTextBox> contrôles pour reproduire l’interface utilisateur de Microsoft Outlook.</span><span class="sxs-lookup"><span data-stu-id="16f4f-116">For this example, use the <xref:System.Windows.Forms.TreeView>, <xref:System.Windows.Forms.ListView>, <xref:System.Windows.Forms.SplitContainer>, and <xref:System.Windows.Forms.RichTextBox> controls to mimic the Microsoft Outlook user interface.</span></span>  
  
    ```vb  
    Private WithEvents treeView1 As System.Windows.Forms.TreeView  
    Private WithEvents listView1 As System.Windows.Forms.ListView  
    Private WithEvents richTextBox1 As System.Windows.Forms.RichTextBox  
    Private WithEvents splitContainer1 As _  
        System.Windows.Forms.SplitContainer  
    Private WithEvents splitContainer2 As _  
        System.Windows.Forms.SplitContainer  
    ```  
  
    ```csharp  
    private System.Windows.Forms.TreeView treeView1;  
    private System.Windows.Forms.ListView listView1;  
    private System.Windows.Forms.RichTextBox richTextBox1;  
    private System.Windows.Forms. SplitContainer splitContainer2;  
    private System.Windows.Forms. SplitContainer splitContainer1;  
    ```  
  
2. <span data-ttu-id="16f4f-117">Créer une procédure qui définit votre interface utilisateur.</span><span class="sxs-lookup"><span data-stu-id="16f4f-117">Create a procedure that defines your user interface.</span></span> <span data-ttu-id="16f4f-118">Le code suivant définit les propriétés afin que le formulaire ressemble à l’interface utilisateur dans Microsoft Outlook.</span><span class="sxs-lookup"><span data-stu-id="16f4f-118">The following code sets the properties so that the form will resemble the user interface in Microsoft Outlook.</span></span> <span data-ttu-id="16f4f-119">Toutefois, à l’aide d’autres contrôles ou les ancrant différemment, il est tout aussi facile de créer d’autres interfaces utilisateur qui sont tout aussi souples.</span><span class="sxs-lookup"><span data-stu-id="16f4f-119">However, by using other controls or docking them differently, it is just as easy to create other user interfaces that are equally flexible.</span></span>  
  
    ```vb  
    Public Sub CreateOutlookUI()  
        ' Create an instance of each control being used.  
        Me.components = New System.ComponentModel.Container()  
        Me.treeView1 = New System.Windows.Forms.TreeView()  
        Me.listView1 = New System.Windows.Forms.ListView()  
        Me.richTextBox1 = New System.Windows.Forms.RichTextBox()  
        Me.splitContainer1 = New System.Windows.Forms.SplitContainer()  
        Me.splitContainer2= New System.Windows.Forms. SplitContainer()  
  
        ' Should you develop this into a working application,  
        ' use the AddHandler method to hook up event procedures here.  
  
        ' Set properties of TreeView control.  
        ' Use the With statement to avoid repetitive code.  
        With Me.treeView1  
            .Dock = System.Windows.Forms.DockStyle.Fill  
            .TabIndex = 0  
            .Nodes.Add("treeView")  
        End With  
  
    ' Set properties of ListView control.  
       With Me.listView1  
          .Dock = System.Windows.Forms.DockStyle.Top  
          .TabIndex = 2  
          .Items.Add("listView")  
       End With  
  
    ' Set properties of RichTextBox control.  
       With Me.richTextBox1  
          .Dock = System.Windows.Forms.DockStyle.Fill  
          .TabIndex = 3  
          .Text = "richTextBox1"  
       End With  
  
        ' Set properties of the first SplitContainer control.  
        With Me.splitContainer1  
            .Dock = System.Windows.Forms.DockStyle.Fill  
            .TabIndex = 1  
            .SplitterWidth = 4  
            .SplitterDistance = 150  
            .Orientation = Orientation.Horizontal  
            .Panel1.Controls.Add(Me.listView1)  
            .Panel2.Controls.Add(Me.richTextBox1)  
    End With  
  
        ' Set properties of the second SplitContainer control.  
        With Me.splitContainer2  
            .Dock = System.Windows.Forms.DockStyle.Fill  
            .TabIndex = 4  
            .SplitterWidth = 4  
            .SplitterDistance = 100  
            .Panel1.Controls.Add(Me.treeView1)  
            .Panel2.Controls.Add(Me.SplitContainer1)  
    End With  
  
    ' Add the main SplitContainer control to the form.  
        Me.Controls.Add(Me.splitContainer2)  
        Me.Text = "Intricate UI Example"  
    End Sub  
    ```  
  
    ```csharp  
    public void createOutlookUI()  
    {  
        // Create an instance of each control being used.  
        treeView1 = new System.Windows.Forms.TreeView();  
        listView1 = new System.Windows.Forms.ListView();  
        richTextBox1 = new System.Windows.Forms.RichTextBox();  
        splitContainer2 = new System.Windows.Forms.SplitContainer();  
        splitContainer1 = new System.Windows.Forms.SplitContainer();  
  
        // Insert code here to hook up event methods.  
  
        // Set properties of TreeView control.  
        treeView1.Dock = System.Windows.Forms.DockStyle.Fill;  
        treeView1.TabIndex = 0;  
        treeView1.Nodes.Add("treeView");  
  
        // Set properties of ListView control.  
        listView1.Dock = System.Windows.Forms.DockStyle.Top;  
        listView1.TabIndex = 2;  
        listView1.Items.Add("listView");  
  
        // Set properties of RichTextBox control.  
        richTextBox1.Dock = System.Windows.Forms.DockStyle.Fill;  
        richTextBox1.TabIndex = 3;  
        richTextBox1.Text = "richTextBox1";  
  
        // Set properties of first SplitContainer control.  
        splitContainer1.Dock = System.Windows.Forms.DockStyle.Fill;  
        splitContainer2.TabIndex = 1;  
        splitContainer2.SplitterWidth = 4;  
        splitContainer2.SplitterDistance = 150;  
        splitContainer2.Orientation = Orientation.Horizontal;  
        splitContainer2.Panel1.Controls.Add(this.listView1);  
        splitContainer2.Panel1.Controls.Add(this.richTextBox1);  
  
        // Set properties of second SplitContainer control.  
        splitContainer2.Dock = System.Windows.Forms.DockStyle.Fill;  
        splitContainer2.TabIndex = 4;  
        splitContainer2.SplitterWidth = 4;  
        splitContainer2.SplitterDistance = 100;  
        splitContainer2.Panel1.Controls.Add(this.treeView1);  
        splitContainer2.Panel1.Controls.Add(this.splitContainer1);  
  
        // Add the main SplitContainer control to the form.  
        this.Controls.Add(this.splitContainer2);  
        this.Text = "Intricate UI Example";  
    }  
    ```  
  
3. <span data-ttu-id="16f4f-120">Dans Visual Basic, ajoutez un appel à la procédure que vous venez de créer dans le `New()` procédure.</span><span class="sxs-lookup"><span data-stu-id="16f4f-120">In Visual Basic, add a call to the procedure you just created in the `New()` procedure.</span></span> <span data-ttu-id="16f4f-121">Dans Visual C#, ajoutez cette ligne de code au constructeur pour la classe de formulaire.</span><span class="sxs-lookup"><span data-stu-id="16f4f-121">In Visual C#, add this line of code to the constructor for the form class.</span></span>  
  
    ```vb  
    ' Add this to the New procedure.  
    CreateOutlookUI()  
    ```  
  
    ```csharp  
    // Add this to the form class's constructor.  
    createOutlookUI();  
    ```  
  
## <a name="see-also"></a><span data-ttu-id="16f4f-122">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="16f4f-122">See also</span></span>

- <xref:System.Windows.Forms.SplitContainer>
- [<span data-ttu-id="16f4f-123">SplitContainer, contrôle</span><span class="sxs-lookup"><span data-stu-id="16f4f-123">SplitContainer Control</span></span>](splitcontainer-control-windows-forms.md)
- [<span data-ttu-id="16f4f-124">Guide pratique pour Créer une Interface utilisateur à plusieurs volets avec des formulaires Windows à l’aide du Concepteur</span><span class="sxs-lookup"><span data-stu-id="16f4f-124">How to: Create a Multipane User Interface with Windows Forms Using the Designer</span></span>](create-a-multipane-user-interface-with-wf-using-the-designer.md)
