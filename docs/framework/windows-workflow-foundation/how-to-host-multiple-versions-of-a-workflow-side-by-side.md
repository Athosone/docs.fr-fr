---
title: 'Procédure : héberger plusieurs versions d’un workflow côte à côte'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
ms.assetid: 09c575df-e0a3-4f3b-9e01-a7ac59d65287
ms.openlocfilehash: 061a8c7b73903b763de27e614e9b3067777afe58
ms.sourcegitcommit: 89fcad7e816c12eb1299128481183f01c73f2c07
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/24/2019
ms.locfileid: "63809460"
---
# <a name="how-to-host-multiple-versions-of-a-workflow-side-by-side"></a>Procédure : héberger plusieurs versions d’un workflow côte à côte

`WorkflowIdentity` permet aux développeurs d'applications de workflow d'associer un nom et une version à une définition de workflow, et d'associer ces informations à une instance persistante de workflow. Ces informations d'identité peuvent être utilisées par les développeurs d'applications de workflow pour activer des scénarios tels que l'exécution côte à côte de plusieurs versions d'une définition de workflow, et fournir la base d'autres fonctionnalités telles que la mise à jour dynamique. Cette étape du didacticiel explique comment utiliser `WorkflowIdentity` pour héberger plusieurs versions de workflow en même temps.

> [!NOTE]
> Pour télécharger une version complète ou consulter une procédure pas à pas vidéo du didacticiel, consultez [Windows Workflow Foundation (WF45) - Getting Started Tutorial](https://go.microsoft.com/fwlink/?LinkID=248976).

## <a name="in-this-topic"></a>Dans cette rubrique

Dans cette étape du didacticiel, les activités `WriteLine` dans le workflow sont modifiées pour fournir des informations supplémentaires, et une nouvelle activité `WriteLine` est ajoutée. Une copie de l'assembly de workflow d'origine est enregistrée, et l'application hôte est mise à jour afin qu'elle puisse exécuter simultanément les workflows d'origine et mis à jour.

- [Pour effectuer une copie du projet NumberGuessWorkflowActivities](how-to-host-multiple-versions-of-a-workflow-side-by-side.md#BKMK_BackupCopy)

- [Pour mettre à jour les flux de travail](how-to-host-multiple-versions-of-a-workflow-side-by-side.md#BKMK_UpdateWorkflows)

    - [Pour mettre à jour le flux de travail StateMachine](how-to-host-multiple-versions-of-a-workflow-side-by-side.md#BKMK_UpdateStateMachine)

    - [Pour mettre à jour le workflow d’organigramme](how-to-host-multiple-versions-of-a-workflow-side-by-side.md#BKMK_UpdateFlowchart)

    - [Pour mettre à jour le workflow séquentiel](how-to-host-multiple-versions-of-a-workflow-side-by-side.md#BKMK_UpdateSequential)

- [Pour mettre à jour workflowversionmap de façon à inclure les versions précédentes de flux de travail](how-to-host-multiple-versions-of-a-workflow-side-by-side.md#BKMK_UpdateWorkflowVersionMap)

- [Pour générer et exécuter l’application](how-to-host-multiple-versions-of-a-workflow-side-by-side.md#BKMK_BuildAndRun)

> [!NOTE]
> Avant de suivre les étapes de cette rubrique, exécutez l'application, démarrez plusieurs workflows de chaque type et effectuez une ou deux propositions pour chacun. Ces workflows persistants sont utilisés dans cette étape et l’étape suivante, [Comment : Mettre à jour la définition d’une Instance de Workflow en cours d’exécution](how-to-update-the-definition-of-a-running-workflow-instance.md).

> [!NOTE]
> Chaque étape du didacticiel de mise en route dépend des étapes précédentes. Si vous n’avez pas effectué les étapes précédentes, vous pouvez télécharger une version terminée du didacticiel à partir de [Windows Workflow Foundation (WF45) - Getting Started Tutorial](https://go.microsoft.com/fwlink/?LinkID=248976).

### <a name="BKMK_BackupCopy"></a> Pour effectuer une copie du projet NumberGuessWorkflowActivities

1. Ouvrez le **WF45GettingStartedTutorial** solution dans Visual Studio 2012, si elle n’est pas ouverte.

2. Appuyez sur Ctrl+Maj+B pour générer la solution.

3. Fermer le **WF45GettingStartedTutorial** solution.

4. Ouvrez l’Explorateur Windows et accédez au répertoire dans lequel le fichier solution du didacticiel et les dossiers du projet sont situés.

5. Créez un dossier nommé **PreviousVersions** dans le même dossier que **NumberGuessWorkflowHost** et **NumberGuessWorkflowActivities**. Ce dossier est utilisé pour contenir les assemblys qui contiennent les différentes versions de workflow utilisées dans les étapes du didacticiel suivantes.

6. Accédez à la **NumberGuessWorkflowActivities\bin\debug** dossier (ou **bin\release** selon les paramètres du projet). Copie **NumberGuessWorkflowActivities.dll** et collez-la dans la **PreviousVersions** dossier.

7. Renommer **NumberGuessWorkflowActivities.dll** dans le **PreviousVersions** dossier **NumberGuessWorkflowActivities_v1.dll**.

    > [!NOTE]
    > Les étapes de cette rubrique illustrent une façon de gérer les assemblys utilisés pour contenir plusieurs versions de workflow. D'autres méthodes, telles que celles d'attribution de nom fort aux assemblys et d'inscription des assemblys dans le Global Assembly Cache peuvent également être utilisées.

8. Créez un dossier nommé **NumberGuessWorkflowActivities_du** dans le même dossier que **NumberGuessWorkflowHost**, **NumberGuessWorkflowActivities**et qui vient d’être ajouté **PreviousVersions** dossier, puis copiez tous les fichiers et sous-dossiers à partir de la **NumberGuessWorkflowActivities** dossier dans le nouvel  **NumberGuessWorkflowActivities_du** dossier. Cette copie de sauvegarde du projet pour la version initiale des activités est utilisée dans [Comment : Mettre à jour la définition d’une Instance de Workflow en cours d’exécution](how-to-update-the-definition-of-a-running-workflow-instance.md).

9. Ouvrez à nouveau le **WF45GettingStartedTutorial** solution dans Visual Studio 2012.

### <a name="BKMK_UpdateWorkflows"></a> Pour mettre à jour les flux de travail

 Dans cette section, les définitions de workflow sont mises à jour. Les deux activités `WriteLine` qui fournissent des commentaires sur la proposition de l'utilisateur sont mises à jour, et une nouvelle activité `WriteLine`, qui fournit des informations supplémentaires sur le jeu une fois que le nombre est deviné, est ajoutée.

#### <a name="BKMK_UpdateStateMachine"></a> Pour mettre à jour le flux de travail StateMachine

1. Dans **l’Explorateur de solutions**, sous le **NumberGuessWorkflowActivities** de projet, double-cliquez sur **StateMachineNumberGuessWorkflow.xaml**.

2. Double-cliquez sur le **Guess Incorrect** transition sur l’ordinateur d’état.

3. Mettez à jour la propriété `Text` de l'activité `WriteLine` située le plus à gauche dans l'activité `If`.

    ```vb
    Guess & " is too low."
    ```

    ```csharp
    Guess + " is too low."
    ```

4. Mettez à jour la propriété `Text` de l'activité `WriteLine` située le plus à droite dans l'activité `If`.

    ```vb
    Guess & " is too high."
    ```

    ```csharp
    Guess + " is too high."
    ```

5. Revenir à l’ensemble d’état en cliquant sur vue de la machine dans le Concepteur de flux de travail **StateMachine** dans la barre de navigation s’affichent en haut du Concepteur de workflow.

6. Double-cliquez sur le **Guess Correct** transition sur l’ordinateur d’état.

7. Faites glisser un **WriteLine** activité à partir de la **Primitives** section de la **boîte à outils** et déposez-la sur la **activité déposer l’Action ici** étiquette de la transition.

8. Dans la zone de propriété `Text`, tapez l'expression suivante :

    ```vb
    Guess & " is correct. You guessed it in " & Turns & " turns."
    ```

    ```csharp
    Guess + " is correct. You guessed it in " + Turns + " turns."
    ```

#### <a name="BKMK_UpdateFlowchart"></a> Pour mettre à jour le workflow d’organigramme

1. Dans **l’Explorateur de solutions**, sous le **NumberGuessWorkflowActivities** de projet, double-cliquez sur **FlowchartNumberGuessWorkflow.xaml**.

2. Mettez à jour la propriété `Text` de l'activité `WriteLine` située le plus à gauche.

    ```vb
    Guess & " is too low."
    ```

    ```csharp
    Guess + " is too low."
    ```

3. Mettez à jour la propriété `Text` de l'activité `WriteLine` située le plus à droite.

    ```vb
    Guess & " is too high."
    ```

    ```csharp
    Guess + " is too high."
    ```

4. Faites glisser un **WriteLine** activité à partir de la **Primitives** section de la **boîte à outils** et déposez-la sur le point de déplacement de la `True` action du premier `FlowDecision` . L'activité `WriteLine` est ajoutée à l'organigramme et liée à l'action `True` de `FlowDecision`.

5. Dans la zone de propriété `Text`, tapez l'expression suivante :

    ```vb
    Guess & " is correct. You guessed it in " & Turns & " turns."
    ```

    ```csharp
    Guess + " is correct. You guessed it in " + Turns + " turns."
    ```

#### <a name="BKMK_UpdateSequential"></a> Pour mettre à jour le workflow séquentiel

1. Dans **l’Explorateur de solutions**, sous le **NumberGuessWorkflowActivities** de projet, double-cliquez sur **SequentialNumberGuessWorkflow.xaml**.

2. Mettez à jour la propriété `Text` de l'activité `WriteLine` située le plus à gauche dans l'activité `If`.

    ```vb
    Guess & " is too low."
    ```

    ```csharp
    Guess + " is too low."
    ```

3. Mettez à jour la propriété `Text` de l'activité `WriteLine` située le plus à droite dans l'activité `If`.

    ```vb
    Guess & " is too high."
    ```

    ```csharp
    Guess + " is too high."
    ```

4. Faites glisser un **WriteLine** activité à partir de la **Primitives** section de la **boîte à outils** et déposez-la après le **DoWhile** activité afin que le  **WriteLine** est la dernière activité de la racine `Sequence` activité.

5. Dans la zone de propriété `Text`, tapez l'expression suivante :

    ```vb
    Guess & " is correct. You guessed it in " & Turns & " turns."
    ```

    ```csharp
    Guess + " is correct. You guessed it in " + Turns + " turns."
    ```

### <a name="BKMK_UpdateWorkflowVersionMap"></a> Pour mettre à jour workflowversionmap de façon à inclure les versions précédentes de flux de travail

1. Double-cliquez sur **WorkflowVersionMap.cs** (ou **WorkflowVersionMap.vb**) sous le **NumberGuessWorkflowHost** projet pour l’ouvrir.

2. Ajoutez les instructions `using` (ou `Imports`) suivantes au début du fichier avec les autres instructions `using` (ou `Imports`).

    ```vb
    Imports System.Reflection
    Imports System.IO
    ```

    ```csharp
    using System.Reflection;
    using System.IO;
    ```

3. Ajoutez trois nouvelles identités de workflow juste au-dessous des trois déclarations d'identité de workflow existantes. Ces nouvelles identités de workflow `v1` seront utilisées pour fournir la définition appropriée de workflow aux workflows démarrés avant que les mises à jour aient été effectuées.

    ```vb
    'Current version identities.
    Public StateMachineNumberGuessIdentity As WorkflowIdentity
    Public FlowchartNumberGuessIdentity As WorkflowIdentity
    Public SequentialNumberGuessIdentity As WorkflowIdentity

    'v1 Identities.
    Public StateMachineNumberGuessIdentity_v1 As WorkflowIdentity
    Public FlowchartNumberGuessIdentity_v1 As WorkflowIdentity
    Public SequentialNumberGuessIdentity_v1 As WorkflowIdentity
    ```

    ```csharp
    // Current version identities.
    static public WorkflowIdentity StateMachineNumberGuessIdentity;
    static public WorkflowIdentity FlowchartNumberGuessIdentity;
    static public WorkflowIdentity SequentialNumberGuessIdentity;

    // v1 identities.
    static public WorkflowIdentity StateMachineNumberGuessIdentity_v1;
    static public WorkflowIdentity FlowchartNumberGuessIdentity_v1;
    static public WorkflowIdentity SequentialNumberGuessIdentity_v1;
    ```

4. Dans le constructeur `WorkflowVersionMap`, mettez à jour la propriété `Version` des trois identités actuelles de workflow vers `2.0.0.0`.

    ```vb
    'Add the current workflow version identities.
    StateMachineNumberGuessIdentity = New WorkflowIdentity With
    {
        .Name = "StateMachineNumberGuessWorkflow",
        .Version = New Version(2, 0, 0, 0)
    }

    FlowchartNumberGuessIdentity = New WorkflowIdentity With
    {
        .Name = "FlowchartNumberGuessWorkflow",
        .Version = New Version(2, 0, 0, 0)
    }

    SequentialNumberGuessIdentity = New WorkflowIdentity With
    {
        .Name = "SequentialNumberGuessWorkflow",
        .Version = New Version(2, 0, 0, 0)
    }

    map.Add(StateMachineNumberGuessIdentity, New StateMachineNumberGuessWorkflow())
    map.Add(FlowchartNumberGuessIdentity, New FlowchartNumberGuessWorkflow())
    map.Add(SequentialNumberGuessIdentity, New SequentialNumberGuessWorkflow())
    ```

    ```csharp
    // Add the current workflow version identities.
    StateMachineNumberGuessIdentity = new WorkflowIdentity
    {
        Name = "StateMachineNumberGuessWorkflow",
        // Version = new Version(1, 0, 0, 0),
        Version = new Version(2, 0, 0, 0)
    };

    FlowchartNumberGuessIdentity = new WorkflowIdentity
    {
        Name = "FlowchartNumberGuessWorkflow",
        // Version = new Version(1, 0, 0, 0),
        Version = new Version(2, 0, 0, 0)
    };

    SequentialNumberGuessIdentity = new WorkflowIdentity
    {
        Name = "SequentialNumberGuessWorkflow",
        // Version = new Version(1, 0, 0, 0),
        Version = new Version(2, 0, 0, 0)
    };

    map.Add(StateMachineNumberGuessIdentity, new StateMachineNumberGuessWorkflow());
    map.Add(FlowchartNumberGuessIdentity, new FlowchartNumberGuessWorkflow());
    map.Add(SequentialNumberGuessIdentity, new SequentialNumberGuessWorkflow());
    ```

    Le code qui ajoute les versions actuelles des workflow au dictionnaire utilise les versions actuelles qui sont référencées dans le projet ainsi, le code qui initialise les définitions de workflow n'a pas besoin d'être mis à jour.

5. Ajoutez le code suivant dans le constructeur juste après le code qui ajoute les versions actuelles au dictionnaire.

    ```vb
    'Initialize the previous workflow version identities.
    StateMachineNumberGuessIdentity_v1 = New WorkflowIdentity With
    {
        .Name = "StateMachineNumberGuessWorkflow",
        .Version = New Version(1, 0, 0, 0)
    }

    FlowchartNumberGuessIdentity_v1 = New WorkflowIdentity With
    {
        .Name = "FlowchartNumberGuessWorkflow",
        .Version = New Version(1, 0, 0, 0)
    }

    SequentialNumberGuessIdentity_v1 = New WorkflowIdentity With
    {
        .Name = "SequentialNumberGuessWorkflow",
        .Version = New Version(1, 0, 0, 0)
    }
    ```

    ```csharp
    // Initialize the previous workflow version identities.
    StateMachineNumberGuessIdentity_v1 = new WorkflowIdentity
    {
        Name = "StateMachineNumberGuessWorkflow",
        Version = new Version(1, 0, 0, 0)
    };

    FlowchartNumberGuessIdentity_v1 = new WorkflowIdentity
    {
        Name = "FlowchartNumberGuessWorkflow",
        Version = new Version(1, 0, 0, 0)
    };

    SequentialNumberGuessIdentity_v1 = new WorkflowIdentity
    {
        Name = "SequentialNumberGuessWorkflow",
        Version = new Version(1, 0, 0, 0)
    };
    ```

    Ces identités de workflow sont associées aux versions initiales des définitions correspondantes de workflow.

6. Ensuite, chargez l'assembly qui contient la première version des définitions de workflow, puis créez et ajoutez des définitions correspondantes de workflow au dictionnaire.

    ```vb
    'Add the previous version workflow identities to the dictionary along with
    'the corresponding workflow definitions loaded from the v1 assembly.
    'Assembly.LoadFile requires an absolute path so convert this relative path
    'to an absolute path.
    Dim v1AssemblyPath As String = "..\..\..\PreviousVersions\NumberGuessWorkflowActivities_v1.dll"
    v1AssemblyPath = Path.GetFullPath(v1AssemblyPath)
    Dim v1Assembly As Assembly = Assembly.LoadFile(v1AssemblyPath)

    map.Add(StateMachineNumberGuessIdentity_v1,
        v1Assembly.CreateInstance("NumberGuessWorkflowActivities.StateMachineNumberGuessWorkflow"))

    map.Add(SequentialNumberGuessIdentity_v1,
        v1Assembly.CreateInstance("NumberGuessWorkflowActivities.SequentialNumberGuessWorkflow"))

    map.Add(FlowchartNumberGuessIdentity_v1,
        v1Assembly.CreateInstance("NumberGuessWorkflowActivities.FlowchartNumberGuessWorkflow"))
    ```

    ```csharp
    // Add the previous version workflow identities to the dictionary along with
    // the corresponding workflow definitions loaded from the v1 assembly.
    // Assembly.LoadFile requires an absolute path so convert this relative path
    // to an absolute path.
    string v1AssemblyPath = @"..\..\..\PreviousVersions\NumberGuessWorkflowActivities_v1.dll";
    v1AssemblyPath = Path.GetFullPath(v1AssemblyPath);
    Assembly v1Assembly = Assembly.LoadFile(v1AssemblyPath);

    map.Add(StateMachineNumberGuessIdentity_v1,
        v1Assembly.CreateInstance("NumberGuessWorkflowActivities.StateMachineNumberGuessWorkflow") as Activity);

    map.Add(SequentialNumberGuessIdentity_v1,
        v1Assembly.CreateInstance("NumberGuessWorkflowActivities.SequentialNumberGuessWorkflow") as Activity);

    map.Add(FlowchartNumberGuessIdentity_v1,
        v1Assembly.CreateInstance("NumberGuessWorkflowActivities.FlowchartNumberGuessWorkflow") as Activity);
    ```

    L'exemple suivant constitue l'intégralité de la classe `WorkflowVersionMap` mise à jour.

    ```vb
    Public Module WorkflowVersionMap
        Dim map As Dictionary(Of WorkflowIdentity, Activity)

        'Current version identities.
        Public StateMachineNumberGuessIdentity As WorkflowIdentity
        Public FlowchartNumberGuessIdentity As WorkflowIdentity
        Public SequentialNumberGuessIdentity As WorkflowIdentity

        'v1 Identities.
        Public StateMachineNumberGuessIdentity_v1 As WorkflowIdentity
        Public FlowchartNumberGuessIdentity_v1 As WorkflowIdentity
        Public SequentialNumberGuessIdentity_v1 As WorkflowIdentity

        Sub New()
            map = New Dictionary(Of WorkflowIdentity, Activity)

            'Add the current workflow version identities.
            StateMachineNumberGuessIdentity = New WorkflowIdentity With
            {
                .Name = "StateMachineNumberGuessWorkflow",
                .Version = New Version(2, 0, 0, 0)
            }

            FlowchartNumberGuessIdentity = New WorkflowIdentity With
            {
                .Name = "FlowchartNumberGuessWorkflow",
                .Version = New Version(2, 0, 0, 0)
            }

            SequentialNumberGuessIdentity = New WorkflowIdentity With
            {
                .Name = "SequentialNumberGuessWorkflow",
                .Version = New Version(2, 0, 0, 0)
            }

            map.Add(StateMachineNumberGuessIdentity, New StateMachineNumberGuessWorkflow())
            map.Add(FlowchartNumberGuessIdentity, New FlowchartNumberGuessWorkflow())
            map.Add(SequentialNumberGuessIdentity, New SequentialNumberGuessWorkflow())

            'Initialize the previous workflow version identities.
            StateMachineNumberGuessIdentity_v1 = New WorkflowIdentity With
            {
                .Name = "StateMachineNumberGuessWorkflow",
                .Version = New Version(1, 0, 0, 0)
            }

            FlowchartNumberGuessIdentity_v1 = New WorkflowIdentity With
            {
                .Name = "FlowchartNumberGuessWorkflow",
                .Version = New Version(1, 0, 0, 0)
            }

            SequentialNumberGuessIdentity_v1 = New WorkflowIdentity With
            {
                .Name = "SequentialNumberGuessWorkflow",
                .Version = New Version(1, 0, 0, 0)
            }

            'Add the previous version workflow identities to the dictionary along with
            'the corresponding workflow definitions loaded from the v1 assembly.
            'Assembly.LoadFile requires an absolute path so convert this relative path
            'to an absolute path.
            Dim v1AssemblyPath As String = "..\..\..\PreviousVersions\NumberGuessWorkflowActivities_v1.dll"
            v1AssemblyPath = Path.GetFullPath(v1AssemblyPath)
            Dim v1Assembly As Assembly = Assembly.LoadFile(v1AssemblyPath)

            map.Add(StateMachineNumberGuessIdentity_v1,
                v1Assembly.CreateInstance("NumberGuessWorkflowActivities.StateMachineNumberGuessWorkflow"))

            map.Add(SequentialNumberGuessIdentity_v1,
                v1Assembly.CreateInstance("NumberGuessWorkflowActivities.SequentialNumberGuessWorkflow"))

            map.Add(FlowchartNumberGuessIdentity_v1,
                v1Assembly.CreateInstance("NumberGuessWorkflowActivities.FlowchartNumberGuessWorkflow"))
        End Sub

        Public Function GetWorkflowDefinition(identity As WorkflowIdentity) As Activity
            Return map(identity)
        End Function

        Public Function GetIdentityDescription(identity As WorkflowIdentity) As String
            Return identity.ToString()
        End Function
    End Module
    ```

    ```csharp
    public static class WorkflowVersionMap
    {
        static Dictionary<WorkflowIdentity, Activity> map;

        // Current version identities.
        static public WorkflowIdentity StateMachineNumberGuessIdentity;
        static public WorkflowIdentity FlowchartNumberGuessIdentity;
        static public WorkflowIdentity SequentialNumberGuessIdentity;

        // v1 identities.
        static public WorkflowIdentity StateMachineNumberGuessIdentity_v1;
        static public WorkflowIdentity FlowchartNumberGuessIdentity_v1;
        static public WorkflowIdentity SequentialNumberGuessIdentity_v1;

        static WorkflowVersionMap()
        {
            map = new Dictionary<WorkflowIdentity, Activity>();

            // Add the current workflow version identities.
            StateMachineNumberGuessIdentity = new WorkflowIdentity
            {
                Name = "StateMachineNumberGuessWorkflow",
                // Version = new Version(1, 0, 0, 0),
                Version = new Version(2, 0, 0, 0)
            };

            FlowchartNumberGuessIdentity = new WorkflowIdentity
            {
                Name = "FlowchartNumberGuessWorkflow",
                // Version = new Version(1, 0, 0, 0),
                Version = new Version(2, 0, 0, 0)
            };

            SequentialNumberGuessIdentity = new WorkflowIdentity
            {
                Name = "SequentialNumberGuessWorkflow",
                // Version = new Version(1, 0, 0, 0),
                Version = new Version(2, 0, 0, 0)
            };

            map.Add(StateMachineNumberGuessIdentity, new StateMachineNumberGuessWorkflow());
            map.Add(FlowchartNumberGuessIdentity, new FlowchartNumberGuessWorkflow());
            map.Add(SequentialNumberGuessIdentity, new SequentialNumberGuessWorkflow());

            // Initialize the previous workflow version identities.
            StateMachineNumberGuessIdentity_v1 = new WorkflowIdentity
            {
                Name = "StateMachineNumberGuessWorkflow",
                Version = new Version(1, 0, 0, 0)
            };

            FlowchartNumberGuessIdentity_v1 = new WorkflowIdentity
            {
                Name = "FlowchartNumberGuessWorkflow",
                Version = new Version(1, 0, 0, 0)
            };

            SequentialNumberGuessIdentity_v1 = new WorkflowIdentity
            {
                Name = "SequentialNumberGuessWorkflow",
                Version = new Version(1, 0, 0, 0)
            };

            // Add the previous version workflow identities to the dictionary along with
            // the corresponding workflow definitions loaded from the v1 assembly.
            // Assembly.LoadFile requires an absolute path so convert this relative path
            // to an absolute path.
            string v1AssemblyPath = @"..\..\..\PreviousVersions\NumberGuessWorkflowActivities_v1.dll";
            v1AssemblyPath = Path.GetFullPath(v1AssemblyPath);
            Assembly v1Assembly = Assembly.LoadFile(v1AssemblyPath);

            map.Add(StateMachineNumberGuessIdentity_v1,
                v1Assembly.CreateInstance("NumberGuessWorkflowActivities.StateMachineNumberGuessWorkflow") as Activity);

            map.Add(SequentialNumberGuessIdentity_v1,
                v1Assembly.CreateInstance("NumberGuessWorkflowActivities.SequentialNumberGuessWorkflow") as Activity);

            map.Add(FlowchartNumberGuessIdentity_v1,
                v1Assembly.CreateInstance("NumberGuessWorkflowActivities.FlowchartNumberGuessWorkflow") as Activity);
        }

        public static Activity GetWorkflowDefinition(WorkflowIdentity identity)
        {
            return map[identity];
        }

        public static string GetIdentityDescription(WorkflowIdentity identity)
        {
            return identity.ToString();
        }
    }
    ```

### <a name="BKMK_BuildAndRun"></a> Pour générer et exécuter l'application

1. Appuyez sur Ctrl+Maj+B pour générer l'application, puis sur Ctrl+F5 pour démarrer.

2. Démarrer un nouveau flux de travail en cliquant sur **nouvelle partie**. La version du workflow s'affiche dans la fenêtre d'état et reflète la version mise à jour du `WorkflowIdentity` associé. Notez `InstanceId` de façon à afficher le fichier de suivi du workflow lorsqu'il se termine, puis entrez des propositions jusqu'à ce que le jeu soit terminé. Notez comment la proposition de l'utilisateur est affichée dans les informations affichées dans la fenêtre d'état basée sur les mises à jour dans les activités `WriteLine`.

    ```
    Please enter a number between 1 and 10
    5 is too high.
    Please enter a number between 1 and 10
    3 is too high.
    Please enter a number between 1 and 10
    1 is too low.
    Please enter a number between 1 and 10
    Congratulations, you guessed the number in 4 turns.
    ```

    > [!NOTE]
    > Le texte mis à jour à partir des activités `WriteLine` s'affiche, mais la sortie de l'activité finale `WriteLine` ajoutée dans cette rubrique ne s'affiche pas. Cela est dû au fait que la fenêtre d'état est mise à jour par le gestionnaire `PersistableIdle`. Étant donné que le workflow se termine et n'est pas inactif après l'activité finale, le gestionnaire `PersistableIdle` n'est pas appelé. Toutefois, un message similaire est affiché dans la fenêtre d'état par le gestionnaire `Completed`. Si vous le souhaitez, le code peut être ajouté au gestionnaire `Completed` pour extraire le texte de `StringWriter` et pour l'afficher dans la fenêtre d'état.

3. Ouvrez l’Explorateur Windows et accédez à la **NumberGuessWorkflowHost\bin\debug** dossier (ou **bin\release** selon les paramètres du projet) et ouvrez le fichier de suivi à l’aide du bloc-notes qui correspond pour le flux de travail terminé. Si vous n’avez pas effectué une note de la `InstanceId`, vous pouvez identifier le fichier de suivi approprié à l’aide de la **Date de modification** informations dans l’Explorateur Windows.

    ```
    Please enter a number between 1 and 10
    5 is too high.
    Please enter a number between 1 and 10
    3 is too high.
    Please enter a number between 1 and 10
    1 is too low.
    Please enter a number between 1 and 10
    2 is correct. You guessed it in 4 turns.
    ```

    La sortie mise à jour `WriteLine` est contenue dans le fichier de trace, y compris la sortie `WriteLine` ajoutée dans cette rubrique.

4. Revenez à l'application d'estimation de nombre et sélectionnez l'un des workflows qui a été démarré avant que les mises à jour n'aient été effectuées. Vous pouvez identifier la version du workflow actuellement sélectionné en examinant les informations de version qui s'affichent sous la fenêtre d'état. Entrez des propositions et notez que les mises à jour d'état correspondent à la sortie d'activité `WriteLine` de la version antérieure, et n'incluez pas l'estimation de l'utilisateur. Cela est dû au fait que ces workflows utilisent la définition de workflow précédente qui n'a pas les mises à jour de `WriteLine`.

    Dans l’étape suivante, [Comment : Mettre à jour la définition d’une Instance de Workflow en cours d’exécution](how-to-update-the-definition-of-a-running-workflow-instance.md), l’exécution `v1` les instances de flux de travail sont mis à jour afin qu’ils contiennent les nouvelles fonctionnalités comme la `v2` instances.
