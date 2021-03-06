---
title: 'Procédure : exécuter un workflow'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
ms.assetid: f814ff82-fe2b-4614-aebb-b768c3e61179
ms.openlocfilehash: 06ac34f5ba5d95bd9f000a35036cf288d3c8f7f7
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61779156"
---
# <a name="how-to-run-a-workflow"></a>Procédure : exécuter un workflow
Cette rubrique est la suite du didacticiel le Guide de mise en route de Windows Workflow Foundation et explique comment créer un hôte de workflow et exécuter le workflow défini dans le précédent [Comment : Créer un flux de travail](how-to-create-a-workflow.md) rubrique.

> [!NOTE]
>  Chaque rubrique du didacticiel de mise en route dépend des rubriques précédentes. Pour terminer cette rubrique, vous devez tout d’abord effectuer [Comment : Créer une activité](how-to-create-an-activity.md) et [Comment : Créer un flux de travail](how-to-create-a-workflow.md).

> [!NOTE]
>  Pour télécharger une version complète du didacticiel, consultez [Windows Workflow Foundation (WF45) - Getting Started Tutorial](https://go.microsoft.com/fwlink/?LinkID=248976)(Windows Workflow Foundation (WF45) - Didacticiel de mise en route).  
  
### <a name="to-create-the-workflow-host-project"></a>Pour créer le projet d'hôte du workflow  
  
1. Ouvrez la solution à partir de la précédente [Comment : Créer une activité](how-to-create-an-activity.md) rubrique à l’aide de Visual Studio 2012.  
  
2. Dans l' **Explorateur de solutions** , cliquez avec le bouton droit sur la solution **WF45GettingStartedTutorial** , puis sélectionnez **Ajouter**, **Nouveau projet**.  
  
    > [!TIP]
    >  Si la fenêtre **Explorateur de solutions** n'est pas affichée, sélectionnez **Explorateur de solutions** dans le menu **Affichage** .

3. Dans le nœud **Installé** , sélectionnez **Visual C#**, **Workflow** (ou **Visual Basic**, **Workflow**).

    > [!NOTE]
    >  En fonction du langage de programmation qui est configuré comme langage principal dans Visual Studio, le nœud **Visual C#** ou **Visual Basic** peut se trouver sous le nœud **Autres langages** dans le nœud **Installé** .

     Dans la liste déroulante de la version du .NET Framework, vérifiez que **.NET Framework 4.5** est sélectionné. Dans la liste **Workflow** , sélectionnez **Application console de workflow** . Dans la zone `NumberGuessWorkflowHost` Nom **, tapez** et cliquez sur **OK**. Une application de workflow de démarrage est ainsi créée, ainsi qu'un support d'hébergement de workflow de base. Le code d'hébergement de base est modifié et sert à exécuter l'application de workflow.

4. Cliquez avec le bouton droit sur le projet **NumberGuessWorkflowHost** récemment ajouté dans l' **Explorateur de solutions** , puis sélectionnez **Ajouter une référence**. Dans la liste **Ajouter une référence** , sélectionnez **Solution** , activez la case à cocher en regard de **NumberGuessWorkflowActivities**, puis cliquez sur **OK**.

5. Cliquez avec le bouton droit sur **Workflow1.xaml** dans l' **Explorateur de solutions** et choisissez **Supprimer**. Pour confirmer, cliquez sur **OK** .

### <a name="to-modify-the-workflow-hosting-code"></a>Pour modifier le code d'hébergement de workflow

1. Double-cliquez sur **Program.cs** ou sur **Module1.vb** dans l' **Explorateur de solutions** pour afficher le code.

    > [!TIP]
    >  Si la fenêtre **Explorateur de solutions** n'est pas affichée, sélectionnez **Explorateur de solutions** dans le menu **Affichage** .

     Étant donné que ce projet a été créé à l'aide du modèle **Application console de workflow** , **Program.cs** ou **Module1.vb** contient le code d'hébergement de workflow de base suivant.

    ```vb
    ' Create and cache the workflow definition
    Activity workflow1 = new Workflow1()
    WorkflowInvoker.Invoke(workflow1)
    ```

    ```csharp
    // Create and cache the workflow definition
    Activity workflow1 = new Workflow1();
    WorkflowInvoker.Invoke(workflow1);
    ```

     Ce code d'hébergement généré utilise <xref:System.Activities.WorkflowInvoker>. <xref:System.Activities.WorkflowInvoker> offre un moyen simple pour appeler un workflow comme s'il s'agissait d'un appel de méthode et ne peut être utilisé que pour les workflows qui n'utilisent pas la persistance. <xref:System.Activities.WorkflowApplication> fournit un modèle plus riche pour exécuter des workflows, qui inclut la notification des événements de cycle de vie, le contrôle d'exécution, la modification de signet et la persistance. Cet exemple utilise des signets et <xref:System.Activities.WorkflowApplication> est utilisé pour l'hébergement du workflow. Ajoutez l'instruction `using` ou **Imports** suivante dans la partie supérieure de **Program.cs** ou **Module1.vb** sous les instructions **using** ou **Imports** existantes.

    ```vb
    Imports NumberGuessWorkflowActivities
    Imports System.Threading
    ```

    ```csharp
    using NumberGuessWorkflowActivities;
    using System.Threading;
    ```

     Remplacez les lignes de code qui utilisent <xref:System.Activities.WorkflowInvoker> par le code d'hébergement <xref:System.Activities.WorkflowApplication> de base suivant. Cet exemple de code d'hébergement montre les étapes de base pour l'hébergement et l'appel d'un workflow, mais ne contient pas encore les fonctionnalités pour exécuter avec succès le workflow à partir de cette rubrique. Au cours des étapes suivantes, le code de base est modifié et des fonctionnalités supplémentaires sont ajoutées jusqu'à ce que l'application soit terminée.

    > [!NOTE]
    >  Remplacez `Workflow1` dans ces exemples par `FlowchartNumberGuessWorkflow`, `SequentialNumberGuessWorkflow`, ou `StateMachineNumberGuessWorkflow`, en fonction du workflow que vous avez finalisé dans le précédent [Comment : Créer un flux de travail](how-to-create-a-workflow.md) étape. Si vous ne substituez pas `Workflow1` , vous obtiendrez des erreurs de build lors de la génération ou de l'exécution du workflow.

     [!code-csharp[CFX_WF_GettingStarted#4](~/samples/snippets/csharp/VS_Snippets_CFX/cfx_wf_gettingstarted/cs/extrasnippets.cs#4)]
     [!code-vb[CFX_WF_GettingStarted#4](~/samples/snippets/visualbasic/VS_Snippets_CFX/cfx_wf_gettingstarted/vb/extrasnippets.vb#4)]

     Ce code crée un <xref:System.Activities.WorkflowApplication>, s'abonne à trois événements de cycle de vie du workflow, démarre le workflow avec un appel à la méthode <xref:System.Activities.WorkflowApplication.Run%2A>, puis attend que le workflow soit terminé. Lorsque le workflow est terminé, le <xref:System.Threading.AutoResetEvent> est défini et l'application hôte se termine.

### <a name="to-set-input-arguments-of-a-workflow"></a>Pour définir des arguments d'entrée d'un workflow

1. Ajoutez l'instruction suivante dans la partie supérieure de **Program.cs** ou **Module1.vb** sous les instructions `using` ou `Imports` existantes.

     [!code-csharp[CFX_WF_GettingStarted#5](~/samples/snippets/csharp/VS_Snippets_CFX/cfx_wf_gettingstarted/cs/program.cs#5)]
     [!code-vb[CFX_WF_GettingStarted#5](~/samples/snippets/visualbasic/VS_Snippets_CFX/cfx_wf_gettingstarted/vb/module1.vb#5)]

2. Remplacez la ligne de code qui crée le <xref:System.Activities.WorkflowApplication> par le code suivant qui crée et passe un dictionnaire de paramètres au workflow lorsqu'il est créé.

    > [!NOTE]
    >  Remplacez `Workflow1` dans ces exemples par `FlowchartNumberGuessWorkflow`, `SequentialNumberGuessWorkflow`, ou `StateMachineNumberGuessWorkflow`, en fonction du workflow que vous avez finalisé dans le précédent [Comment : Créer un flux de travail](how-to-create-a-workflow.md) étape. Si vous ne substituez pas `Workflow1` , vous obtiendrez des erreurs de build lors de la génération ou de l'exécution du workflow.

     [!code-csharp[CFX_WF_GettingStarted#6](~/samples/snippets/csharp/VS_Snippets_CFX/cfx_wf_gettingstarted/cs/program.cs#6)]
     [!code-vb[CFX_WF_GettingStarted#6](~/samples/snippets/visualbasic/VS_Snippets_CFX/cfx_wf_gettingstarted/vb/module1.vb#6)]

     Ce dictionnaire contient un élément avec une clé de `MaxNumber`. Les clés du dictionnaire d'entrée correspondent aux arguments d'entrée sur l'activité racine du workflow. `MaxNumber` est utilisé par le workflow pour déterminer la limite supérieure pour le nombre généré de manière aléatoire.

### <a name="to-retrieve-output-arguments-of-a-workflow"></a>Pour récupérer des arguments de sortie d'un workflow

1. Modifiez le gestionnaire <xref:System.Activities.WorkflowApplication.Completed%2A> pour récupérer et afficher le nombre de tours utilisé par le workflow.

     [!code-csharp[CFX_WF_GettingStarted#7](~/samples/snippets/csharp/VS_Snippets_CFX/cfx_wf_gettingstarted/cs/program.cs#7)]
     [!code-vb[CFX_WF_GettingStarted#7](~/samples/snippets/visualbasic/VS_Snippets_CFX/cfx_wf_gettingstarted/vb/module1.vb#7)]

### <a name="to-resume-a-bookmark"></a>Pour reprendre un signet

1. Ajoutez le code suivant en haut de la méthode `Main` , juste après la déclaration <xref:System.Threading.AutoResetEvent> existante.

     [!code-csharp[CFX_WF_GettingStarted#8](~/samples/snippets/csharp/VS_Snippets_CFX/cfx_wf_gettingstarted/cs/program.cs#8)]
     [!code-vb[CFX_WF_GettingStarted#8](~/samples/snippets/visualbasic/VS_Snippets_CFX/cfx_wf_gettingstarted/vb/module1.vb#8)]

2. Ajoutez le gestionnaire <xref:System.Activities.WorkflowApplication.Idle%2A> suivant, juste en dessous des trois gestionnaires de cycle de vie du workflow existants dans `Main`.

     [!code-csharp[CFX_WF_GettingStarted#9](~/samples/snippets/csharp/VS_Snippets_CFX/cfx_wf_gettingstarted/cs/program.cs#9)]
     [!code-vb[CFX_WF_GettingStarted#9](~/samples/snippets/visualbasic/VS_Snippets_CFX/cfx_wf_gettingstarted/vb/module1.vb#9)]

     Chaque fois que le workflow devient inactif en attendant l’estimation suivante, ce gestionnaire est appelé et le `idleAction` <xref:System.Threading.AutoResetEvent> est défini. Le code de l'étape suivante utilise `idleEvent` et `syncEvent` pour déterminer si le workflow attend l'estimation suivante ou s'il est terminé.

    > [!NOTE]
    >  Dans cet exemple, l'application hôte utilise des événements à réinitialisation automatique dans les gestionnaires <xref:System.Activities.WorkflowApplication.Completed%2A> et <xref:System.Activities.WorkflowApplication.Idle%2A> pour synchroniser l'application hôte avec la progression du workflow. Il n'est pas nécessaire de bloquer et d'attendre que le workflow devienne inactif avant de reprendre un signet mais, dans cet exemple, les événements de synchronisation sont nécessaires afin que l'hôte sache si le workflow est terminé ou s'il attend une ou plusieurs autres entrées d'utilisateur à l'aide de <xref:System.Activities.Bookmark>. Pour plus d’informations, consultez [signets](bookmarks.md).

3. Supprimez l'appel à `WaitOne`et remplacez-le par du code pour recueillir l'entrée de l'utilisateur et reprendre le <xref:System.Activities.Bookmark>.

     Supprimez la ligne de code suivante.

     [!code-csharp[CFX_WF_GettingStarted#10](~/samples/snippets/csharp/VS_Snippets_CFX/cfx_wf_gettingstarted/cs/extrasnippets.cs#10)]
     [!code-vb[CFX_WF_GettingStarted#10](~/samples/snippets/visualbasic/VS_Snippets_CFX/cfx_wf_gettingstarted/vb/extrasnippets.vb#10)]

     Remplacez-la par l'exemple suivant.

     [!code-csharp[CFX_WF_GettingStarted#11](~/samples/snippets/csharp/VS_Snippets_CFX/cfx_wf_gettingstarted/cs/program.cs#11)]
     [!code-vb[CFX_WF_GettingStarted#11](~/samples/snippets/visualbasic/VS_Snippets_CFX/cfx_wf_gettingstarted/vb/module1.vb#11)]

## <a name="BKMK_ToRunTheApplication"></a> Pour générer et exécuter l'application

1. Cliquez avec le bouton droit sur **NumberGuessWorkflowHost** dans l' **Explorateur de solutions** , puis sélectionnez **Définir comme projet de démarrage**.

2. Appuyez sur Ctrl+F5 pour générer et exécuter l'application. Essayez de deviner le nombre en aussi peu de tours que possible.

     Pour essayer l'application avec un des autres styles de workflow, remplacez `Workflow1` dans le code qui crée le <xref:System.Activities.WorkflowApplication> par `FlowchartNumberGuessWorkflow`, `SequentialNumberGuessWorkflow`, ou `StateMachineNumberGuessWorkflow`, en fonction du style de workflow souhaité.

     [!code-csharp[CFX_WF_GettingStarted#6](~/samples/snippets/csharp/VS_Snippets_CFX/cfx_wf_gettingstarted/cs/program.cs#6)]
     [!code-vb[CFX_WF_GettingStarted#6](~/samples/snippets/visualbasic/VS_Snippets_CFX/cfx_wf_gettingstarted/vb/module1.vb#6)]

     Pour savoir comment ajouter la persistance à une application de workflow, consultez la rubrique suivante, [Comment : Créer et exécuter un Long en cours d’exécution du flux de travail](how-to-create-and-run-a-long-running-workflow.md).

## <a name="example"></a>Exemple
 L'exemple suivant constitue l'intégralité du code de la méthode `Main` .

> [!NOTE]
>  Remplacez `Workflow1` dans ces exemples par `FlowchartNumberGuessWorkflow`, `SequentialNumberGuessWorkflow`, ou `StateMachineNumberGuessWorkflow`, en fonction du workflow que vous avez finalisé dans le précédent [Comment : Créer un flux de travail](how-to-create-a-workflow.md) étape. Si vous ne substituez pas `Workflow1` , vous obtiendrez des erreurs de build lors de la génération ou de l'exécution du workflow.

 [!code-csharp[CFX_WF_GettingStarted#12](~/samples/snippets/csharp/VS_Snippets_CFX/cfx_wf_gettingstarted/cs/program.cs#12)]
 [!code-vb[CFX_WF_GettingStarted#12](~/samples/snippets/visualbasic/VS_Snippets_CFX/cfx_wf_gettingstarted/vb/module1.vb#12)]

## <a name="see-also"></a>Voir aussi

- <xref:System.Activities.WorkflowApplication>
- <xref:System.Activities.Bookmark>
- [Programmation Windows Workflow Foundation](programming.md)
- [Didacticiel Bien démarrer](getting-started-tutorial.md)
- [Guide pratique pour Créer un flux de travail](how-to-create-a-workflow.md)
- [Guide pratique pour Créer et exécuter un Long en cours d’exécution du flux de travail](how-to-create-and-run-a-long-running-workflow.md)
- [Attente d’une entrée dans un workflow](waiting-for-input-in-a-workflow.md)
- [Hébergement de workflows](hosting-workflows.md)