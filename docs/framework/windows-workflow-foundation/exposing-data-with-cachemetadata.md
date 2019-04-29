---
title: Exposition de données avec CacheMetadata
ms.date: 03/30/2017
ms.assetid: 34832f23-e93b-40e6-a80b-606a855a00d9
ms.openlocfilehash: a044c896e56541ee954fc33853376eb8293c6ede
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61945702"
---
# <a name="exposing-data-with-cachemetadata"></a><span data-ttu-id="a6f8b-102">Exposition de données avec CacheMetadata</span><span class="sxs-lookup"><span data-stu-id="a6f8b-102">Exposing data with CacheMetadata</span></span>

<span data-ttu-id="a6f8b-103">Avant d'exécuter une activité, le runtime du workflow obtient toutes les informations nécessaires sur l'activité afin de gérer son exécution.</span><span class="sxs-lookup"><span data-stu-id="a6f8b-103">Before executing an activity, the workflow runtime obtains all of the information about the activity that it needs in order to maintain its execution.</span></span> <span data-ttu-id="a6f8b-104">Le runtime de workflow obtient ces informations pendant l'exécution de la méthode <xref:System.Activities.Activity.CacheMetadata%2A>.</span><span class="sxs-lookup"><span data-stu-id="a6f8b-104">The workflow runtime gets this information during the execution of the <xref:System.Activities.Activity.CacheMetadata%2A> method.</span></span> <span data-ttu-id="a6f8b-105">L'implémentation par défaut de cette méthode fournit au runtime tous les arguments publics, variables et activités enfants exposés par l'activité lors de son exécution ; si l'activité a besoin de fournir plus d'informations au runtime (telles que les membres privés ou les activités à planifier par l'activité), cette méthode peut être substituée pour les fournir.</span><span class="sxs-lookup"><span data-stu-id="a6f8b-105">The default implementation of this method provides the runtime with all of the public arguments, variables, and child activities exposed by the activity at the time it is executed; if the activity needs to give more information to the runtime than this (such as private members, or activities to be scheduled by the activity), this method can be overridden to provide it.</span></span>

## <a name="default-cachemetadata-behavior"></a><span data-ttu-id="a6f8b-106">Comportement par défaut de CacheMetadata</span><span class="sxs-lookup"><span data-stu-id="a6f8b-106">Default CacheMetadata behavior</span></span>

<span data-ttu-id="a6f8b-107">L'implémentation par défaut de <xref:System.Activities.NativeActivity.CacheMetadata%2A> pour les activités qui dérivent de <xref:System.Activities.NativeActivity> traite les types de méthode suivants comme suit :</span><span class="sxs-lookup"><span data-stu-id="a6f8b-107">The default implementation of <xref:System.Activities.NativeActivity.CacheMetadata%2A> for activities that derive from <xref:System.Activities.NativeActivity> processes the following method types in the following ways:</span></span>

- <span data-ttu-id="a6f8b-108"><xref:System.Activities.InArgument%601>, <xref:System.Activities.OutArgument%601>, ou <xref:System.Activities.InOutArgument%601> (arguments génériques) : Ces arguments sont exposés au runtime en tant qu’arguments avec un nom et le type correspondent au propriété exposée nom et type, la direction de l’argument approprié, et certaines données de validation.</span><span class="sxs-lookup"><span data-stu-id="a6f8b-108"><xref:System.Activities.InArgument%601>, <xref:System.Activities.OutArgument%601>, or <xref:System.Activities.InOutArgument%601> (generic arguments): These arguments are exposed to the runtime as arguments with a name and type equal to the exposed property name and type, the appropriate argument direction, and some validation data.</span></span>

- <span data-ttu-id="a6f8b-109"><xref:System.Activities.Variable> ou une sous-classe : Ces membres sont exposés au runtime en tant que variables publiques.</span><span class="sxs-lookup"><span data-stu-id="a6f8b-109"><xref:System.Activities.Variable> or any subclass thereof: These members are exposed to the runtime as public variables.</span></span>

- <span data-ttu-id="a6f8b-110"><xref:System.Activities.Activity> ou une sous-classe : Ces membres sont exposés au runtime en tant qu’activités enfants publiques.</span><span class="sxs-lookup"><span data-stu-id="a6f8b-110"><xref:System.Activities.Activity> or any subclass thereof: These members are exposed to the runtime as public child activities.</span></span> <span data-ttu-id="a6f8b-111">Le comportement par défaut peut être implémenté explicitement en appelant <xref:System.Activities.ActivityMetadata.AddImportedChild%2A>, en passant l’activité enfant.</span><span class="sxs-lookup"><span data-stu-id="a6f8b-111">The default behavior can be implemented explicitly by calling <xref:System.Activities.ActivityMetadata.AddImportedChild%2A>, passing in the child activity.</span></span>

- <span data-ttu-id="a6f8b-112"><xref:System.Activities.ActivityDelegate> ou une sous-classe : Ces membres sont exposés au runtime en tant que délégués publics.</span><span class="sxs-lookup"><span data-stu-id="a6f8b-112"><xref:System.Activities.ActivityDelegate> or any subclass thereof: These members are exposed to the runtime as public delegates.</span></span>

- <span data-ttu-id="a6f8b-113"><xref:System.Collections.ICollection> de type <xref:System.Activities.Variable>: Tous les éléments dans la collection sont exposés au runtime en tant que variables publiques.</span><span class="sxs-lookup"><span data-stu-id="a6f8b-113"><xref:System.Collections.ICollection> of type <xref:System.Activities.Variable>: All elements in the collection are exposed to the runtime as public variables.</span></span>

- <span data-ttu-id="a6f8b-114"><xref:System.Collections.ICollection> de type <xref:System.Activities.Activity>: Tous les éléments dans la collection sont exposés au runtime en tant qu’enfants publics.</span><span class="sxs-lookup"><span data-stu-id="a6f8b-114"><xref:System.Collections.ICollection> of type <xref:System.Activities.Activity>: All elements in the collection are exposed to the runtime as public children.</span></span>

- <span data-ttu-id="a6f8b-115"><xref:System.Collections.ICollection> de type <xref:System.Activities.ActivityDelegate>: Tous les éléments dans la collection sont exposés au runtime en tant que délégués publics.</span><span class="sxs-lookup"><span data-stu-id="a6f8b-115"><xref:System.Collections.ICollection> of type <xref:System.Activities.ActivityDelegate>: All elements in the collection are exposed to the runtime as public delegates.</span></span>

<span data-ttu-id="a6f8b-116">Le <xref:System.Activities.Activity.CacheMetadata%2A> pour les activités qui dérivent de <xref:System.Activities.Activity>, <xref:System.Workflow.Activities.CodeActivity> et <xref:System.Activities.AsyncCodeActivity> fonctionnent également comme ci-dessus, à l'exception des différences suivantes :</span><span class="sxs-lookup"><span data-stu-id="a6f8b-116">The <xref:System.Activities.Activity.CacheMetadata%2A> for activities that derive from <xref:System.Activities.Activity>, <xref:System.Workflow.Activities.CodeActivity>, and <xref:System.Activities.AsyncCodeActivity> also function as above, except for the following differences:</span></span>

- <span data-ttu-id="a6f8b-117">Les classes qui dérivent de <xref:System.Activities.Activity> ne peuvent pas planifier des activités enfants ou des délégués, ces pourquoi ces membres sont exposés comme des enfants importés et des délégués ; les</span><span class="sxs-lookup"><span data-stu-id="a6f8b-117">Classes that derive from <xref:System.Activities.Activity> cannot schedule child activities or delegates, so such members are exposed as imported children and delegates; the</span></span>

- <span data-ttu-id="a6f8b-118">classes qui dérivent de <xref:System.Activities.CodeActivity> et <xref:System.Activities.AsyncCodeActivity> ne prennent pas en charge les variables, les enfants ou les délégués, c'est pourquoi seuls les arguments seront exposés.</span><span class="sxs-lookup"><span data-stu-id="a6f8b-118">Classes that derive from <xref:System.Activities.CodeActivity> and <xref:System.Activities.AsyncCodeActivity> do not support variables, children, or delegates, so only arguments will be exposed.</span></span>

## <a name="overriding-cachemetadata-to-provide-information-to-the-runtime"></a><span data-ttu-id="a6f8b-119">Substitution de CacheMetadata pour fournir des informations au runtime</span><span class="sxs-lookup"><span data-stu-id="a6f8b-119">Overriding CacheMetadata to provide information to the runtime</span></span>

<span data-ttu-id="a6f8b-120">L'extrait de code suivant montre comment ajouter des informations sur les membres aux métadonnées d'une activité pendant l'exécution de la méthode <xref:System.Activities.Activity.CacheMetadata%2A>.</span><span class="sxs-lookup"><span data-stu-id="a6f8b-120">The following code snippet demonstrates how to add information about members to an activity’s metadata during the execution of the <xref:System.Activities.Activity.CacheMetadata%2A> method.</span></span> <span data-ttu-id="a6f8b-121">Notez que la base de la méthode est appelée pour mettre en cache toutes les données publiques sur l'activité.</span><span class="sxs-lookup"><span data-stu-id="a6f8b-121">Note that the base of the method is called to cache all public data about the activity.</span></span>

```csharp
protected override void CacheMetadata(NativeActivityMetadata metadata)
{
    base.CacheMetadata(metadata);
    metadata.AddImplementationChild(this._writeLine);
    metadata.AddVariable(this._myVariable);
    metadata.AddImplementationVariable(this._myImplementationVariable);

    RuntimeArgument argument = new RuntimeArgument("MyArgument", ArgumentDirection.In, typeof(SomeType));
    metadata.Bind(argument, this.SomeName);
    metadata.AddArgument(argument);
}
```

## <a name="using-cachemetadata-to-expose-implementation-children"></a><span data-ttu-id="a6f8b-122">Utilisation de CacheMetadata pour exposer les enfants de l'implémentation</span><span class="sxs-lookup"><span data-stu-id="a6f8b-122">Using CacheMetadata to expose implementation children</span></span>

<span data-ttu-id="a6f8b-123">Pour passer les données aux activités enfants qui doivent être planifiées par une activité à l'aide de variables, il est nécessaire d'ajouter les variables en tant que variables d'implémentation ; les valeurs des variables publiques ne peuvent pas être définies de cette façon.</span><span class="sxs-lookup"><span data-stu-id="a6f8b-123">In order to pass data to child activities that are to be scheduled by an activity using variables, it is necessary to add the variables as implementation variables; public variables cannot have their values set this way.</span></span> <span data-ttu-id="a6f8b-124">En effet, les activités sont conçues pour être exécutées plus comme des implémentations de fonctions (qui ont des paramètres), que comme des classes encapsulées (qui ont des propriétés).</span><span class="sxs-lookup"><span data-stu-id="a6f8b-124">The reason for this is that activities are intended to be executed more as implementations of functions (which have parameters), rather than encapsulated classes (which have properties).</span></span> <span data-ttu-id="a6f8b-125">Toutefois, il existe des situations dans lesquelles les arguments doivent être définis explicitement, comme lors de l’utilisation de <xref:System.Activities.NativeActivityContext.ScheduleActivity%2A>, puisque l’activité planifiée n’a pas accès aux arguments de l’activité parent comme une activité enfant.</span><span class="sxs-lookup"><span data-stu-id="a6f8b-125">However, there are situations in which the arguments must be explicitly set, such as when using <xref:System.Activities.NativeActivityContext.ScheduleActivity%2A>, since the scheduled activity doesn't have access to the parent activity's arguments in the way a child activity would.</span></span>

<span data-ttu-id="a6f8b-126">L’extrait de code suivant montre comment passer un argument d’une activité native à une activité planifiée à l’aide de <xref:System.Activities.Activity.CacheMetadata%2A>.</span><span class="sxs-lookup"><span data-stu-id="a6f8b-126">The following code snippet demonstrates how to pass an argument form a native activity into a scheduled activity using <xref:System.Activities.Activity.CacheMetadata%2A>.</span></span>

```csharp
public sealed class ChildActivity : NativeActivity
{
    public WriteLine _writeLine;
    public InArgument<string> Message { get; set; }
    private Variable<string> MessageVariable { get; set; }
    public ChildActivity()
    {
        MessageVariable = new Variable<string>();
        _writeLine = new WriteLine
        {
            Text = new InArgument<string>(MessageVariable),
        };
    }
    protected override void CacheMetadata(NativeActivityMetadata metadata)
    {
        base.CacheMetadata(metadata);
        metadata.AddImplementationVariable(this.MessageVariable);
        metadata.AddImplementationChild(this._writeLine);
    }
    protected override void Execute(NativeActivityContext context)
    {
        string configuredMessage = context.GetValue(Message);
        context.SetValue(MessageVariable, configuredMessage);
        context.ScheduleActivity(this._writeLine);
    }
}
```
