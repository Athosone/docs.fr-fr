---
title: 'Procédure pas à pas : exécution d’une opération en arrière-plan'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- background tasks
- forms [Windows Forms], multithreading
- forms [Windows Forms], background operations
- background threads
- BackgroundWorker class [Windows Forms], examples
- threading [Windows Forms], background operations
- background operations
ms.assetid: 1b9a4e0a-f134-48ff-a1be-c461446a31ba
ms.openlocfilehash: c1881ffa1c6fca546b086efea59d2263af853949
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61792169"
---
# <a name="walkthrough-running-an-operation-in-the-background"></a><span data-ttu-id="77cd6-102">Procédure pas à pas : exécution d’une opération en arrière-plan</span><span class="sxs-lookup"><span data-stu-id="77cd6-102">Walkthrough: Running an Operation in the Background</span></span>
<span data-ttu-id="77cd6-103">Si vous avez une opération qui prendra un certain temps et que vous ne souhaitez pas causer de retards dans votre interface utilisateur, vous pouvez utiliser la classe <xref:System.ComponentModel.BackgroundWorker> pour exécuter l'opération sur un autre thread.</span><span class="sxs-lookup"><span data-stu-id="77cd6-103">If you have an operation that will take a long time to complete, and you do not want to cause delays in your user interface, you can use the <xref:System.ComponentModel.BackgroundWorker> class to run the operation on another thread.</span></span>  
  
 <span data-ttu-id="77cd6-104">Pour obtenir une liste complète du code utilisé dans cet exemple, consultez [Comment : exécuter une opération en arrière-plan](how-to-run-an-operation-in-the-background.md).</span><span class="sxs-lookup"><span data-stu-id="77cd6-104">For a complete listing of the code used in this example, see [How to: Run an Operation in the Background](how-to-run-an-operation-in-the-background.md).</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="77cd6-105">Les boîtes de dialogue et les commandes de menu qui s'affichent peuvent être différentes de celles qui sont décrites dans l'aide, en fonction de vos paramètres actifs ou de l'édition utilisée.</span><span class="sxs-lookup"><span data-stu-id="77cd6-105">The dialog boxes and menu commands you see might differ from those described in Help depending on your active settings or edition.</span></span> <span data-ttu-id="77cd6-106">Pour modifier vos paramètres, choisissez **Importation et exportation de paramètres** dans le menu **Outils** .</span><span class="sxs-lookup"><span data-stu-id="77cd6-106">To change your settings, choose **Import and Export Settings** on the **Tools** menu.</span></span> <span data-ttu-id="77cd6-107">Pour plus d’informations, consultez [Personnaliser l’IDE Visual Studio](/visualstudio/ide/personalizing-the-visual-studio-ide).</span><span class="sxs-lookup"><span data-stu-id="77cd6-107">For more information, see [Personalize the Visual Studio IDE](/visualstudio/ide/personalizing-the-visual-studio-ide).</span></span>  
  
### <a name="to-run-an-operation-in-the-background"></a><span data-ttu-id="77cd6-108">Pour exécuter une opération en arrière-plan</span><span class="sxs-lookup"><span data-stu-id="77cd6-108">To run an operation in the background</span></span>  
  
1. <span data-ttu-id="77cd6-109">Avec votre formulaire actif dans le Concepteur de formulaires Windows, faites glisser deux <xref:System.Windows.Forms.Button> des contrôles de la **boîte à outils** le formulaire, puis définissez le `Name` et <xref:System.Windows.Forms.Control.Text%2A> propriétés des boutons conformément au tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="77cd6-109">With your form active in the Windows Forms Designer, drag two <xref:System.Windows.Forms.Button> controls from the **Toolbox** to the form, and then set the `Name` and <xref:System.Windows.Forms.Control.Text%2A> properties of the buttons according to the following table.</span></span>  
  
    |<span data-ttu-id="77cd6-110">Bouton</span><span class="sxs-lookup"><span data-stu-id="77cd6-110">Button</span></span>|<span data-ttu-id="77cd6-111">Nom</span><span class="sxs-lookup"><span data-stu-id="77cd6-111">Name</span></span>|<span data-ttu-id="77cd6-112">Texte</span><span class="sxs-lookup"><span data-stu-id="77cd6-112">Text</span></span>|  
    |------------|----------|----------|  
    |`button1`|`startBtn`|<span data-ttu-id="77cd6-113">**Démarrer**</span><span class="sxs-lookup"><span data-stu-id="77cd6-113">**Start**</span></span>|  
    |`button2`|`cancelBtn`|<span data-ttu-id="77cd6-114">**Annuler**</span><span class="sxs-lookup"><span data-stu-id="77cd6-114">**Cancel**</span></span>|  
  
2. <span data-ttu-id="77cd6-115">Ouvrir le **boîte à outils**, cliquez sur le **composants** onglet, puis faites glisser le <xref:System.ComponentModel.BackgroundWorker> composant vers votre formulaire.</span><span class="sxs-lookup"><span data-stu-id="77cd6-115">Open the **Toolbox**, click the **Components** tab, and then drag the <xref:System.ComponentModel.BackgroundWorker> component onto your form.</span></span>  
  
     <span data-ttu-id="77cd6-116">Le `backgroundWorker1` composant apparaît dans le **barre d’état du composant**.</span><span class="sxs-lookup"><span data-stu-id="77cd6-116">The `backgroundWorker1` component appears in the **Component Tray**.</span></span>  
  
3. <span data-ttu-id="77cd6-117">Dans la fenêtre **Propriétés** , définissez la propriété <xref:System.ComponentModel.BackgroundWorker.WorkerSupportsCancellation%2A> sur `true`.</span><span class="sxs-lookup"><span data-stu-id="77cd6-117">In the **Properties** window, set the <xref:System.ComponentModel.BackgroundWorker.WorkerSupportsCancellation%2A> property to `true`.</span></span>  
  
4. <span data-ttu-id="77cd6-118">Dans le **propriétés** fenêtre, cliquez sur le **événements** bouton, puis double-cliquez sur le <xref:System.ComponentModel.BackgroundWorker.DoWork> et <xref:System.ComponentModel.BackgroundWorker.RunWorkerCompleted> événements pour créer des gestionnaires d’événements.</span><span class="sxs-lookup"><span data-stu-id="77cd6-118">In the **Properties** window, click on the **Events** button, and then double-click the <xref:System.ComponentModel.BackgroundWorker.DoWork> and <xref:System.ComponentModel.BackgroundWorker.RunWorkerCompleted> events to create event handlers.</span></span>  
  
5. <span data-ttu-id="77cd6-119">Insérez votre code du temps dans le <xref:System.ComponentModel.BackgroundWorker.DoWork> Gestionnaire d’événements.</span><span class="sxs-lookup"><span data-stu-id="77cd6-119">Insert your time-consuming code into the <xref:System.ComponentModel.BackgroundWorker.DoWork> event handler.</span></span>  
  
6. <span data-ttu-id="77cd6-120">Extraire tous les paramètres requis par l’opération à partir de la <xref:System.ComponentModel.DoWorkEventArgs.Argument%2A> propriété de le <xref:System.ComponentModel.DoWorkEventArgs> paramètre.</span><span class="sxs-lookup"><span data-stu-id="77cd6-120">Extract any parameters required by the operation from the <xref:System.ComponentModel.DoWorkEventArgs.Argument%2A> property of the <xref:System.ComponentModel.DoWorkEventArgs> parameter.</span></span>  
  
7. <span data-ttu-id="77cd6-121">Assignez le résultat du calcul à la <xref:System.ComponentModel.DoWorkEventArgs.Result%2A> propriété de la <xref:System.ComponentModel.DoWorkEventArgs>.</span><span class="sxs-lookup"><span data-stu-id="77cd6-121">Assign the result of the computation to the <xref:System.ComponentModel.DoWorkEventArgs.Result%2A> property of the <xref:System.ComponentModel.DoWorkEventArgs>.</span></span>  
  
     <span data-ttu-id="77cd6-122">Il s’agit de va être disponible pour le <xref:System.ComponentModel.BackgroundWorker.RunWorkerCompleted> Gestionnaire d’événements.</span><span class="sxs-lookup"><span data-stu-id="77cd6-122">This is will be available to the <xref:System.ComponentModel.BackgroundWorker.RunWorkerCompleted> event handler.</span></span>  
  
     [!code-csharp[System.ComponentModel.BackgroundWorker.Example#2](~/samples/snippets/csharp/VS_Snippets_Winforms/System.ComponentModel.BackgroundWorker.Example/CS/Form1.cs#2)]
     [!code-vb[System.ComponentModel.BackgroundWorker.Example#2](~/samples/snippets/visualbasic/VS_Snippets_Winforms/System.ComponentModel.BackgroundWorker.Example/VB/Form1.vb#2)]  
  
8. <span data-ttu-id="77cd6-123">Insérer du code pour récupérer le résultat de votre opération dans le <xref:System.ComponentModel.BackgroundWorker.RunWorkerCompleted> Gestionnaire d’événements.</span><span class="sxs-lookup"><span data-stu-id="77cd6-123">Insert code for retrieving the result of your operation in the <xref:System.ComponentModel.BackgroundWorker.RunWorkerCompleted> event handler.</span></span>  
  
     [!code-csharp[System.ComponentModel.BackgroundWorker.Example#3](~/samples/snippets/csharp/VS_Snippets_Winforms/System.ComponentModel.BackgroundWorker.Example/CS/Form1.cs#3)]
     [!code-vb[System.ComponentModel.BackgroundWorker.Example#3](~/samples/snippets/visualbasic/VS_Snippets_Winforms/System.ComponentModel.BackgroundWorker.Example/VB/Form1.vb#3)]  
  
9. <span data-ttu-id="77cd6-124">Implémentez la méthode `TimeConsumingOperation`.</span><span class="sxs-lookup"><span data-stu-id="77cd6-124">Implement the `TimeConsumingOperation` method.</span></span>  
  
     [!code-csharp[System.ComponentModel.BackgroundWorker.Example#4](~/samples/snippets/csharp/VS_Snippets_Winforms/System.ComponentModel.BackgroundWorker.Example/CS/Form1.cs#4)]
     [!code-vb[System.ComponentModel.BackgroundWorker.Example#4](~/samples/snippets/visualbasic/VS_Snippets_Winforms/System.ComponentModel.BackgroundWorker.Example/VB/Form1.vb#4)]  
  
10. <span data-ttu-id="77cd6-125">Dans le Concepteur Windows Forms, double-cliquez sur `startButton` pour créer le <xref:System.Windows.Forms.Control.Click> Gestionnaire d’événements.</span><span class="sxs-lookup"><span data-stu-id="77cd6-125">In the Windows Forms Designer, double-click `startButton` to create the <xref:System.Windows.Forms.Control.Click> event handler.</span></span>  
  
11. <span data-ttu-id="77cd6-126">Appelez le <xref:System.ComponentModel.BackgroundWorker.RunWorkerAsync%2A> méthode dans le <xref:System.Windows.Forms.Control.Click> Gestionnaire d’événements pour `startButton`.</span><span class="sxs-lookup"><span data-stu-id="77cd6-126">Call the <xref:System.ComponentModel.BackgroundWorker.RunWorkerAsync%2A> method in the <xref:System.Windows.Forms.Control.Click> event handler for `startButton`.</span></span>  
  
     [!code-csharp[System.ComponentModel.BackgroundWorker.Example#5](~/samples/snippets/csharp/VS_Snippets_Winforms/System.ComponentModel.BackgroundWorker.Example/CS/Form1.cs#5)]
     [!code-vb[System.ComponentModel.BackgroundWorker.Example#5](~/samples/snippets/visualbasic/VS_Snippets_Winforms/System.ComponentModel.BackgroundWorker.Example/VB/Form1.vb#5)]  
  
12. <span data-ttu-id="77cd6-127">Dans le Concepteur Windows Forms, double-cliquez sur `cancelButton` pour créer le <xref:System.Windows.Forms.Control.Click> Gestionnaire d’événements.</span><span class="sxs-lookup"><span data-stu-id="77cd6-127">In the Windows Forms Designer, double-click `cancelButton` to create the <xref:System.Windows.Forms.Control.Click> event handler.</span></span>  
  
13. <span data-ttu-id="77cd6-128">Appelez le <xref:System.ComponentModel.BackgroundWorker.CancelAsync%2A> méthode dans le <xref:System.Windows.Forms.Control.Click> Gestionnaire d’événements pour `cancelButton`.</span><span class="sxs-lookup"><span data-stu-id="77cd6-128">Call the <xref:System.ComponentModel.BackgroundWorker.CancelAsync%2A> method in the <xref:System.Windows.Forms.Control.Click> event handler for `cancelButton`.</span></span>  
  
     [!code-csharp[System.ComponentModel.BackgroundWorker.Example#6](~/samples/snippets/csharp/VS_Snippets_Winforms/System.ComponentModel.BackgroundWorker.Example/CS/Form1.cs#6)]
     [!code-vb[System.ComponentModel.BackgroundWorker.Example#6](~/samples/snippets/visualbasic/VS_Snippets_Winforms/System.ComponentModel.BackgroundWorker.Example/VB/Form1.vb#6)]  
  
14. <span data-ttu-id="77cd6-129">En haut du fichier, importez les espaces de noms System.ComponentModel et System.Threading.</span><span class="sxs-lookup"><span data-stu-id="77cd6-129">At the top of the file, import the System.ComponentModel and System.Threading namespaces.</span></span>  
  
     [!code-csharp[System.ComponentModel.BackgroundWorker.Example#7](~/samples/snippets/csharp/VS_Snippets_Winforms/System.ComponentModel.BackgroundWorker.Example/CS/Form1.cs#7)]
     [!code-vb[System.ComponentModel.BackgroundWorker.Example#7](~/samples/snippets/visualbasic/VS_Snippets_Winforms/System.ComponentModel.BackgroundWorker.Example/VB/Form1.vb#7)]  
  
15. <span data-ttu-id="77cd6-130">Appuyez sur F6 pour générer la solution, puis appuyez sur CTRL + F5 pour exécuter l’application en dehors du débogueur.</span><span class="sxs-lookup"><span data-stu-id="77cd6-130">Press F6 to build the solution, and then press CTRL-F5 to run the application outside the debugger.</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="77cd6-131">Si vous appuyez sur F5 pour exécuter l’application sous le débogueur, l’exception est levée dans le `TimeConsumingOperation` méthode est interceptée et affichée par le débogueur.</span><span class="sxs-lookup"><span data-stu-id="77cd6-131">If you press F5 to run the application under the debugger, the exception raised in the `TimeConsumingOperation` method is caught and displayed by the debugger.</span></span> <span data-ttu-id="77cd6-132">Lorsque vous exécutez l’application en dehors du débogueur, le <xref:System.ComponentModel.BackgroundWorker> gère l’exception et met en cache dans le <xref:System.ComponentModel.AsyncCompletedEventArgs.Error%2A> propriété de la <xref:System.ComponentModel.RunWorkerCompletedEventArgs>.</span><span class="sxs-lookup"><span data-stu-id="77cd6-132">When you run the application outside the debugger, the <xref:System.ComponentModel.BackgroundWorker> handles the exception and caches it in the <xref:System.ComponentModel.AsyncCompletedEventArgs.Error%2A> property of the <xref:System.ComponentModel.RunWorkerCompletedEventArgs>.</span></span>  
  
1. <span data-ttu-id="77cd6-133">Cliquez sur le **Démarrer** bouton pour exécuter une opération asynchrone, puis cliquez sur le **Annuler** bouton pour arrêter une opération asynchrone en cours d’exécution.</span><span class="sxs-lookup"><span data-stu-id="77cd6-133">Click the **Start** button to run an asynchronous operation, and then click the **Cancel** button to stop a running asynchronous operation.</span></span>  
  
     <span data-ttu-id="77cd6-134">Le résultat de chaque opération est affiché dans un <xref:System.Windows.Forms.MessageBox>.</span><span class="sxs-lookup"><span data-stu-id="77cd6-134">The outcome of each operation is displayed in a <xref:System.Windows.Forms.MessageBox>.</span></span>  
  
## <a name="next-steps"></a><span data-ttu-id="77cd6-135">Étapes suivantes</span><span class="sxs-lookup"><span data-stu-id="77cd6-135">Next Steps</span></span>  
  
- <span data-ttu-id="77cd6-136">Implémenter un formulaire qui signale la progression au fur et une opération asynchrone.</span><span class="sxs-lookup"><span data-stu-id="77cd6-136">Implement a form that reports progress as an asynchronous operation proceeds.</span></span> <span data-ttu-id="77cd6-137">Pour plus d'informations, voir [Procédure : Implémenter un formulaire qui utilise une opération d’arrière-plan](how-to-implement-a-form-that-uses-a-background-operation.md).</span><span class="sxs-lookup"><span data-stu-id="77cd6-137">For more information, see [How to: Implement a Form That Uses a Background Operation](how-to-implement-a-form-that-uses-a-background-operation.md).</span></span>  
  
- <span data-ttu-id="77cd6-138">Implémentez une classe qui prend en charge le modèle asynchrone pour les composants.</span><span class="sxs-lookup"><span data-stu-id="77cd6-138">Implement a class that supports the Asynchronous Pattern for Components.</span></span> <span data-ttu-id="77cd6-139">Pour plus d’informations, consultez [implémenter le modèle asynchrone basé sur événement](../../../standard/asynchronous-programming-patterns/implementing-the-event-based-asynchronous-pattern.md).</span><span class="sxs-lookup"><span data-stu-id="77cd6-139">For more information, see [Implementing the Event-based Asynchronous Pattern](../../../standard/asynchronous-programming-patterns/implementing-the-event-based-asynchronous-pattern.md).</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="77cd6-140">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="77cd6-140">See also</span></span>

- <xref:System.ComponentModel.BackgroundWorker>
- <xref:System.ComponentModel.DoWorkEventArgs>
- [<span data-ttu-id="77cd6-141">Guide pratique pour implémenter un formulaire qui utilise une opération d’arrière-plan</span><span class="sxs-lookup"><span data-stu-id="77cd6-141">How to: Implement a Form That Uses a Background Operation</span></span>](how-to-implement-a-form-that-uses-a-background-operation.md)
- [<span data-ttu-id="77cd6-142">Guide pratique pour exécuter une opération en arrière-plan</span><span class="sxs-lookup"><span data-stu-id="77cd6-142">How to: Run an Operation in the Background</span></span>](how-to-run-an-operation-in-the-background.md)
- [<span data-ttu-id="77cd6-143">Composant BackgroundWorker</span><span class="sxs-lookup"><span data-stu-id="77cd6-143">BackgroundWorker Component</span></span>](backgroundworker-component.md)
