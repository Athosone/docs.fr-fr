---
title: Utilisation d'extensions d'activité
ms.date: 03/30/2017
ms.assetid: 500eb96a-c009-4247-b6b5-b36faffdf715
ms.openlocfilehash: e524f7e7127eb215be85b0c317474eee70830c2b
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61669509"
---
# <a name="using-activity-extensions"></a><span data-ttu-id="cc038-102">Utilisation d'extensions d'activité</span><span class="sxs-lookup"><span data-stu-id="cc038-102">Using Activity Extensions</span></span>
<span data-ttu-id="cc038-103">Les activités peuvent interagir avec les extensions d’application de workflow qui permettent à l’hôte de fournir des fonctionnalités supplémentaires qui ne sont pas explicitement modélisées dans le workflow.</span><span class="sxs-lookup"><span data-stu-id="cc038-103">Activities can interact with workflow application extensions that allow the host to provide additional functionality that is not explicitly modeled in the workflow.</span></span>  <span data-ttu-id="cc038-104">Cette rubrique explique comment créer et utiliser une extension pour compter le nombre de fois où l'activité s'exécute.</span><span class="sxs-lookup"><span data-stu-id="cc038-104">This topic describes how to create and use an extension to count the number of times the activity executes.</span></span>

### <a name="to-use-an-activity-extension-to-count-executions"></a><span data-ttu-id="cc038-105">Pour utiliser une extension d’activité pour compter les exécutions</span><span class="sxs-lookup"><span data-stu-id="cc038-105">To use an activity extension to count executions</span></span>

1. <span data-ttu-id="cc038-106">Ouvrez Visual Studio 2010.</span><span class="sxs-lookup"><span data-stu-id="cc038-106">Open Visual Studio 2010.</span></span> <span data-ttu-id="cc038-107">Sélectionnez **nouveau**, **projet**.</span><span class="sxs-lookup"><span data-stu-id="cc038-107">Select **New**, **Project**.</span></span> <span data-ttu-id="cc038-108">Sous le **Visual C#** nœud, sélectionnez **Workflow**.</span><span class="sxs-lookup"><span data-stu-id="cc038-108">Under the **Visual C#** node, select **Workflow**.</span></span>  <span data-ttu-id="cc038-109">Sélectionnez **Application Console de Workflow** à partir de la liste des modèles.</span><span class="sxs-lookup"><span data-stu-id="cc038-109">Select **Workflow Console Application** from the list of templates.</span></span> <span data-ttu-id="cc038-110">Attribuez un nom au projet `Extensions`.</span><span class="sxs-lookup"><span data-stu-id="cc038-110">Name the project `Extensions`.</span></span> <span data-ttu-id="cc038-111">Cliquez sur **OK** pour créer le projet.</span><span class="sxs-lookup"><span data-stu-id="cc038-111">Click **OK** to create the project.</span></span>

2. <span data-ttu-id="cc038-112">Ajouter un `using` instruction dans le fichier Program.cs pour le **System.Collections.Generic** espace de noms.</span><span class="sxs-lookup"><span data-stu-id="cc038-112">Add a `using` statement in the Program.cs file for the **System.Collections.Generic** namespace.</span></span>

    ```
    using System.Collections.Generic;
    ```

3. <span data-ttu-id="cc038-113">Dans le fichier Program.cs, créez une classe nommée **ExecutionCountExtension**.</span><span class="sxs-lookup"><span data-stu-id="cc038-113">In the Program.cs file, create a new class named **ExecutionCountExtension**.</span></span> <span data-ttu-id="cc038-114">Le code suivant crée une extension de workflow qui assure le suivi des ID d’instance lors de son **inscrire** méthode est appelée.</span><span class="sxs-lookup"><span data-stu-id="cc038-114">The following code creates a workflow extension that tracks instance IDs when its **Register** method is called.</span></span>

    ```
    // This extension collects a list of workflow Ids
    public class ExecutionCountExtension
    {
        IList<Guid> instances = new List<Guid>();

        public int ExecutionCount
        {
            get
            {
                return this.instances.Count;
            }
        }

        public IEnumerable<Guid> InstanceIds
        {
            get
            {
                return this.instances;
            }
        }

        public void Register(Guid activityInstanceId)
        {
            if (!this.instances.Contains<Guid>(activityInstanceId))
            {
                instances.Add(activityInstanceId);
            }
        }
    }
    ```

4. <span data-ttu-id="cc038-115">Créer une activité qui consomme le **ExecutionCountExtension**.</span><span class="sxs-lookup"><span data-stu-id="cc038-115">Create an activity that consumes the **ExecutionCountExtension**.</span></span> <span data-ttu-id="cc038-116">Le code suivant définit une activité qui Récupère le **ExecutionCountExtension** objet à partir du runtime et appelle son **inscrire** méthode lorsque l’activité s’exécute.</span><span class="sxs-lookup"><span data-stu-id="cc038-116">The following code defines an activity that retrieves the **ExecutionCountExtension** object from the runtime and calls its **Register** method when the activity executes.</span></span>

    ```
    // Activity that consumes an extension provided by the host. If the extension is available
    // in the context, it will invoke (in this case, registers the Id of the executing workflow)
    public class MyActivity: CodeActivity
    {
        protected override void Execute(CodeActivityContext context)
        {
            ExecutionCountExtension ext = context.GetExtension<ExecutionCountExtension>();
            if (ext != null)
            {
                ext.Register(context.WorkflowInstanceId);
            }

        }
    }
    ```

5. <span data-ttu-id="cc038-117">Implémentez l’activité dans le **Main** méthode du fichier program.cs.</span><span class="sxs-lookup"><span data-stu-id="cc038-117">Implement the activity in the **Main** method of the program.cs file.</span></span> <span data-ttu-id="cc038-118">Le code suivant contient les méthodes pour générer deux workflows distincts, exécuter plusieurs fois chaque workflow et afficher les données résultantes contenues dans l’extension.</span><span class="sxs-lookup"><span data-stu-id="cc038-118">The following code contains methods to generate two different workflows, execute each workflow several times, and display the resulting data that is contained in the extension.</span></span>

    ```
    class Program
    {
        // Creates a workflow that uses the activity that consumes the extension
        static Activity CreateWorkflow1()
        {
            return new Sequence
            {
                Activities =
                {
                    new MyActivity()
                }
            };
        }

        // Creates a workflow that uses two instances of the activity that consumes the extension
        static Activity CreateWorkflow2()
        {
            return new Sequence
            {
                Activities =
                {
                    new MyActivity(),
                    new MyActivity()
                }
            };
        }

        static void Main(string[] args)
        {
            // create the extension
            ExecutionCountExtension executionCountExt = new ExecutionCountExtension();

            // configure the first invoker and execute 3 times
            WorkflowInvoker invoker = new WorkflowInvoker(CreateWorkflow1());
            invoker.Extensions.Add(executionCountExt);
            invoker.Invoke();
            invoker.Invoke();
            invoker.Invoke();

            // configure the second invoker and execute 2 times
            WorkflowInvoker invoker2 = new WorkflowInvoker(CreateWorkflow2());
            invoker2.Extensions.Add(executionCountExt);
            invoker2.Invoke();
            invoker2.Invoke();

            // show the data in the extension
            Console.WriteLine("Executed {0} times", executionCountExt.ExecutionCount);
            executionCountExt.InstanceIds.ToList().ForEach(i => Console.WriteLine("...{0}", i));
        }
    }
    ```
