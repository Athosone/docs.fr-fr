---
title: 'Tâche 3 : créer les volets Toolbox et PropertyGrid'
ms.date: 03/30/2017
ms.assetid: 72c1546a-eed5-4f0f-a616-719a163414f4
ms.openlocfilehash: 15e5b4ea08b6bc243484b6963c1c06f448bb985b
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61641538"
---
# <a name="task-3-create-the-toolbox-and-propertygrid-panes"></a><span data-ttu-id="f4e1b-102">Tâche 3 : créer les volets Toolbox et PropertyGrid</span><span class="sxs-lookup"><span data-stu-id="f4e1b-102">Task 3: Create the Toolbox and PropertyGrid Panes</span></span>
<span data-ttu-id="f4e1b-103">Dans cette tâche, vous allez créer le **boîte à outils** et **PropertyGrid** volets et les ajouter à la réhébergé [!INCLUDE[wfd1](../../../includes/wfd1-md.md)].</span><span class="sxs-lookup"><span data-stu-id="f4e1b-103">In this task, you will create the **Toolbox** and **PropertyGrid** panes and add them to the rehosted [!INCLUDE[wfd1](../../../includes/wfd1-md.md)].</span></span>  
  
 <span data-ttu-id="f4e1b-104">Pour référence, le code qui doit être dans le fichier MainWindow.xaml.cs après avoir effectué les trois tâches dans le [réhébergement du Concepteur de flux de travail](rehosting-the-workflow-designer.md) série de rubriques est fourni à la fin de cette rubrique.</span><span class="sxs-lookup"><span data-stu-id="f4e1b-104">For reference, the code that should be in the MainWindow.xaml.cs file after completing the three tasks in the [Rehosting the Workflow Designer](rehosting-the-workflow-designer.md) series of topics is provided at the end of this topic.</span></span>  
  
### <a name="to-create-the-toolbox-and-add-it-to-the-grid"></a><span data-ttu-id="f4e1b-105">Pour créer la boîte à outils et l'ajouter à la grille</span><span class="sxs-lookup"><span data-stu-id="f4e1b-105">To create the Toolbox and add it to the grid</span></span>  
  
1. <span data-ttu-id="f4e1b-106">Ouvrez le projet hostingapplication que vous avez obtenu en suivant la procédure décrite dans [tâche 2 : Héberger le Concepteur de flux de travail](task-2-host-the-workflow-designer.md).</span><span class="sxs-lookup"><span data-stu-id="f4e1b-106">Open the HostingApplication project you obtained by following the procedure described in [Task 2: Host the Workflow Designer](task-2-host-the-workflow-designer.md).</span></span>  
  
2. <span data-ttu-id="f4e1b-107">Dans le **l’Explorateur de solutions** volet, cliquez sur le fichier MainWindow.xaml et sélectionnez **afficher le Code**.</span><span class="sxs-lookup"><span data-stu-id="f4e1b-107">In the **Solution Explorer** pane, right-click the MainWindow.xaml file and select **View Code**.</span></span>  
  
3. <span data-ttu-id="f4e1b-108">Ajouter un `GetToolboxControl` méthode à la `MainWindow` classe qui crée un <xref:System.Activities.Presentation.Toolbox.ToolboxControl>, ajoute un nouveau **boîte à outils** catégorie à la **boîte à outils**et assigne le <xref:System.Activities.Statements.Assign> et <xref:System.Activities.Statements.Sequence> types d’activités à cette catégorie.</span><span class="sxs-lookup"><span data-stu-id="f4e1b-108">Add a `GetToolboxControl` method to the `MainWindow` class that creates a <xref:System.Activities.Presentation.Toolbox.ToolboxControl>, adds a new **Toolbox** category to the **Toolbox**, and assigns the <xref:System.Activities.Statements.Assign> and <xref:System.Activities.Statements.Sequence> activity types to that category.</span></span>  
  
    ```csharp  
    private ToolboxControl GetToolboxControl()  
    {  
        // Create the ToolBoxControl.  
        ToolboxControl ctrl = new ToolboxControl();  
  
        // Create a category.  
        ToolboxCategory category = new ToolboxCategory("category1");  
  
        // Create Toolbox items.  
        ToolboxItemWrapper tool1 =   
            new ToolboxItemWrapper("System.Activities.Statements.Assign",   
            typeof(Assign).Assembly.FullName, null, "Assign");  
  
        ToolboxItemWrapper tool2 = new ToolboxItemWrapper("System.Activities.Statements.Sequence",   
            typeof(Sequence).Assembly.FullName, null, "Sequence");  
  
        // Add the Toolbox items to the category.  
        category.Add(tool1);  
        category.Add(tool2);  
  
        // Add the category to the ToolBox control.  
        ctrl.Categories.Add(category);  
        return ctrl;  
    }  
    ```  
  
4. <span data-ttu-id="f4e1b-109">Ajouter une privée `AddToolbox` méthode à la `MainWindow` classe place le **boîte à outils** dans la colonne de gauche sur la grille.</span><span class="sxs-lookup"><span data-stu-id="f4e1b-109">Add a private `AddToolbox` method to the `MainWindow` class that places the **Toolbox** in the left column on the grid.</span></span>  
  
    ```csharp  
    private void AddToolBox()  
    {  
        ToolboxControl tc = GetToolboxControl();  
        Grid.SetColumn(tc, 0);  
        grid1.Children.Add(tc);  
    }  
    ```  
  
5. <span data-ttu-id="f4e1b-110">Ajoutez un appel à la méthode `AddToolBox` dans le constructeur de classe `MainWindow()`, comme illustré dans le code suivant.</span><span class="sxs-lookup"><span data-stu-id="f4e1b-110">Add a call to the `AddToolBox` method in the `MainWindow()` class constructor as shown in the following code.</span></span>  
  
    ```csharp  
    public MainWindow()  
    {  
        InitializeComponent();  
        this.RegisterMetadata();  
        this.AddDesigner();  
  
        this.AddToolBox();  
    }  
    ```  
  
6. <span data-ttu-id="f4e1b-111">Appuyez sur F5 pour générer et exécuter votre solution.</span><span class="sxs-lookup"><span data-stu-id="f4e1b-111">Press F5 to build and run your solution.</span></span> <span data-ttu-id="f4e1b-112">Le **boîte à outils** contenant le <xref:System.Activities.Statements.Assign> et <xref:System.Activities.Statements.Sequence> activités doivent être affichées.</span><span class="sxs-lookup"><span data-stu-id="f4e1b-112">The **Toolbox** containing the <xref:System.Activities.Statements.Assign> and <xref:System.Activities.Statements.Sequence> activities should be displayed.</span></span>  
  
### <a name="to-create-the-propertygrid"></a><span data-ttu-id="f4e1b-113">Pour créer PropertyGrid</span><span class="sxs-lookup"><span data-stu-id="f4e1b-113">To create the PropertyGrid</span></span>  
  
1. <span data-ttu-id="f4e1b-114">Dans le **l’Explorateur de solutions** volet, cliquez sur le fichier MainWindow.xaml et sélectionnez **afficher le Code**.</span><span class="sxs-lookup"><span data-stu-id="f4e1b-114">In the **Solution Explorer** pane, right-click the MainWindow.xaml file and select **View Code**.</span></span>  
  
2. <span data-ttu-id="f4e1b-115">Ajouter le `AddPropertyInspector` méthode à la `MainWindow` classe pour placer le **PropertyGrid** volet dans la colonne la plus à droite sur la grille.</span><span class="sxs-lookup"><span data-stu-id="f4e1b-115">Add the `AddPropertyInspector` method to the `MainWindow` class to place the **PropertyGrid** pane in the rightmost column on the grid.</span></span>  
  
    ```csharp  
    private void AddPropertyInspector()  
    {  
        Grid.SetColumn(wd.PropertyInspectorView, 2);  
        grid1.Children.Add(wd.PropertyInspectorView);              
    }  
    ```  
  
3. <span data-ttu-id="f4e1b-116">Ajoutez un appel à la méthode `AddPropertyInspector` dans le constructeur de classe `MainWindow()`, comme illustré dans le code suivant.</span><span class="sxs-lookup"><span data-stu-id="f4e1b-116">Add a call to the `AddPropertyInspector` method in the `MainWindow()` class constructor as shown in the following code.</span></span>  
  
    ```csharp  
    public MainWindow()  
    {  
        InitializeComponent();  
        this.RegisterMetadata();  
        this.AddDesigner();  
        this.AddToolBox();  
  
        this.AddPropertyInspector();   
    }  
    ```  
  
4. <span data-ttu-id="f4e1b-117">Pour générer et exécuter la solution, appuyez sur F5.</span><span class="sxs-lookup"><span data-stu-id="f4e1b-117">Press F5 to build and run the solution.</span></span> <span data-ttu-id="f4e1b-118">Le **boîte à outils**, zone de conception de flux de travail, et **PropertyGrid** volets doivent tous être affichés, et lorsque vous faites glisser un <xref:System.Activities.Statements.Assign> activité ou un <xref:System.Activities.Statements.Sequence> activité sur la zone de conception, le grille des propriétés doit mettre à jour en fonction de l’activité en surbrillance.</span><span class="sxs-lookup"><span data-stu-id="f4e1b-118">The **Toolbox**, workflow design canvas, and **PropertyGrid** panes should all be displayed, and when you drag an <xref:System.Activities.Statements.Assign> activity or a <xref:System.Activities.Statements.Sequence> activity onto the design canvas, the property grid should update depending on the highlighted activity.</span></span>  
  
## <a name="example"></a><span data-ttu-id="f4e1b-119">Exemple</span><span class="sxs-lookup"><span data-stu-id="f4e1b-119">Example</span></span>  
 <span data-ttu-id="f4e1b-120">Le fichier MainWindow.xaml.cs doit maintenant contenir le code suivant.</span><span class="sxs-lookup"><span data-stu-id="f4e1b-120">The MainWindow.xaml.cs file should now contain the following code.</span></span>  
  
```  
using System;  
using System.Collections.Generic;  
using System.Linq;  
using System.Text;  
using System.Windows;  
using System.Windows.Controls;  
using System.Windows.Data;  
using System.Windows.Documents;  
using System.Windows.Input;  
using System.Windows.Media;  
using System.Windows.Media.Imaging;  
using System.Windows.Navigation;  
using System.Windows.Shapes;  
//dlls added  
using System.Activities;  
using System.Activities.Core.Presentation;  
using System.Activities.Presentation;  
using System.Activities.Presentation.Metadata;  
using System.Activities.Presentation.Toolbox;  
using System.Activities.Statements;  
using System.ComponentModel;  
  
namespace HostingApplication  
{  
    /// <summary>  
    /// Interaction logic for MainWindow.xaml  
    /// </summary>  
    public partial class MainWindow : Window  
    {  
        private WorkflowDesigner wd;  
  
        public MainWindow()  
        {  
            InitializeComponent();  
            RegisterMetadata();  
            AddDesigner();  
            this.AddToolBox();  
            this.AddPropertyInspector();  
        }  
  
        private void AddDesigner()  
        {  
            //Create an instance of WorkflowDesigner class.  
            this.wd = new WorkflowDesigner();  
  
            //Place the designer canvas in the middle column of the grid.  
            Grid.SetColumn(this.wd.View, 1);  
  
            //Load a new Sequence as default.  
            this.wd.Load(new Sequence());  
  
            //Add the designer canvas to the grid.  
            grid1.Children.Add(this.wd.View);  
        }  
  
        private void RegisterMetadata()  
        {  
            DesignerMetadata dm = new DesignerMetadata();  
            dm.Register();  
        }  
  
        private ToolboxControl GetToolboxControl()  
        {  
            // Create the ToolBoxControl.  
            ToolboxControl ctrl = new ToolboxControl();  
  
            // Create a category.  
            ToolboxCategory category = new ToolboxCategory("category1");  
  
            // Create Toolbox items.  
            ToolboxItemWrapper tool1 =  
                new ToolboxItemWrapper("System.Activities.Statements.Assign",  
                typeof(Assign).Assembly.FullName, null, "Assign");  
  
            ToolboxItemWrapper tool2 = new ToolboxItemWrapper("System.Activities.Statements.Sequence",  
                typeof(Sequence).Assembly.FullName, null, "Sequence");  
  
            // Add the Toolbox items to the category.  
            category.Add(tool1);  
            category.Add(tool2);  
  
            // Add the category to the ToolBox control.  
            ctrl.Categories.Add(category);  
            return ctrl;  
        }  
  
        private void AddToolBox()  
        {  
            ToolboxControl tc = GetToolboxControl();  
            Grid.SetColumn(tc, 0);  
            grid1.Children.Add(tc);  
        }  
  
        private void AddPropertyInspector()  
        {  
            Grid.SetColumn(wd.PropertyInspectorView, 2);  
            grid1.Children.Add(wd.PropertyInspectorView);  
        }  
  
    }  
}  
```  
  
## <a name="see-also"></a><span data-ttu-id="f4e1b-121">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f4e1b-121">See also</span></span>

- [<span data-ttu-id="f4e1b-122">Réhébergement du concepteur de flux de travail</span><span class="sxs-lookup"><span data-stu-id="f4e1b-122">Rehosting the Workflow Designer</span></span>](rehosting-the-workflow-designer.md)
- [<span data-ttu-id="f4e1b-123">Tâche 1 : Créer une nouvelle Application Windows Presentation Foundation</span><span class="sxs-lookup"><span data-stu-id="f4e1b-123">Task 1: Create a New Windows Presentation Foundation Application</span></span>](task-1-create-a-new-wpf-app.md)
- [<span data-ttu-id="f4e1b-124">Tâche 2 : Héberger le Concepteur de flux de travail</span><span class="sxs-lookup"><span data-stu-id="f4e1b-124">Task 2: Host the Workflow Designer</span></span>](task-2-host-the-workflow-designer.md)
