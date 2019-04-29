---
title: Transactions de workflow
ms.date: 03/30/2017
ms.assetid: 6081fb02-c0f2-483d-97b8-f3b7dc03011d
ms.openlocfilehash: 17e4b712f5b6955ab777168d60d8a28e8b0ebd63
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61670194"
---
# <a name="workflow-transactions"></a><span data-ttu-id="507c3-102">Transactions de workflow</span><span class="sxs-lookup"><span data-stu-id="507c3-102">Workflow Transactions</span></span>

[!INCLUDE[wf1](../../../includes/wf1-md.md)] <span data-ttu-id="507c3-103">offre une prise en charge pour participer aux transactions <xref:System.Transactions> en utilisant l'activité <xref:System.Activities.Statements.TransactionScope> pour étendre une unité traitée de travail.</span><span class="sxs-lookup"><span data-stu-id="507c3-103">provides support for participating in <xref:System.Transactions> transactions by using the <xref:System.Activities.Statements.TransactionScope> activity to scope a transacted unit of work.</span></span> <span data-ttu-id="507c3-104">Alors que le <xref:System.Transactions.TransactionScope?displayProperty=nameWithType> doit être terminé explicitement, l'activité <xref:System.Activities.Statements.TransactionScope?displayProperty=nameWithType> appelle implicitement la transaction une fois cette dernière terminée.</span><span class="sxs-lookup"><span data-stu-id="507c3-104">While the <xref:System.Transactions.TransactionScope?displayProperty=nameWithType> must be explicitly completed the <xref:System.Activities.Statements.TransactionScope?displayProperty=nameWithType> activity implicitly calls complete on the transaction upon successful completion.</span></span> <span data-ttu-id="507c3-105">Toute activité contenue dans l’élément <xref:System.Activities.Statements.TransactionScope.Body%2A> de l’activité <xref:System.Activities.Statements.TransactionScope> participe à la transaction.</span><span class="sxs-lookup"><span data-stu-id="507c3-105">Any activities that are contained in the <xref:System.Activities.Statements.TransactionScope.Body%2A> of the <xref:System.Activities.Statements.TransactionScope> activity participate in the transaction.</span></span> <span data-ttu-id="507c3-106">WF peut transférer des transactions dans un workflow en faisant appel à l’activité <xref:System.ServiceModel.Activities.TransactedReceiveScope>.</span><span class="sxs-lookup"><span data-stu-id="507c3-106">WF can to flow transactions into a workflow through the use of the <xref:System.ServiceModel.Activities.TransactedReceiveScope> activity.</span></span> <span data-ttu-id="507c3-107">Comme l'activité <xref:System.Activities.Statements.TransactionScope>, toute activité contenue dans le <xref:System.ServiceModel.Activities.TransactedReceiveScope.Body%2A> participe à la transaction.</span><span class="sxs-lookup"><span data-stu-id="507c3-107">Like the <xref:System.Activities.Statements.TransactionScope> activity, any activity contained in the <xref:System.ServiceModel.Activities.TransactedReceiveScope.Body%2A> participates in the transaction.</span></span> <span data-ttu-id="507c3-108">WF vérifie que les activités dépendant de <xref:System.Transactions.Transaction.Current%2A?displayProperty=nameWithType> utilisent à la fois <xref:System.Activities.Statements.TransactionScope> et <xref:System.ServiceModel.Activities.TransactedReceiveScope>.</span><span class="sxs-lookup"><span data-stu-id="507c3-108">WF ensures that activities dependent on <xref:System.Transactions.Transaction.Current%2A?displayProperty=nameWithType> works with both <xref:System.Activities.Statements.TransactionScope> and <xref:System.ServiceModel.Activities.TransactedReceiveScope>.</span></span> <span data-ttu-id="507c3-109">Si les activités fournies par le système ne remplissent pas toutes les conditions, les activités personnalisées peuvent être construites à l’aide du <xref:System.Activities.RuntimeTransactionHandle> afin d’activer un flux avancé et des scénarios de contrôle de transaction.</span><span class="sxs-lookup"><span data-stu-id="507c3-109">If the system-provided activities do not address all requirements, custom activities can be built using the <xref:System.Activities.RuntimeTransactionHandle> to enable advanced flow and transaction control scenarios.</span></span>  
  
<span data-ttu-id="507c3-110">Dans l’exemple suivant, un flux de travail est composé d’un <xref:System.Activities.Statements.Sequence> activité qui contient les activités enfants, y compris un <xref:System.Activities.Statements.TransactionScope> activité.</span><span class="sxs-lookup"><span data-stu-id="507c3-110">In the following example, a workflow is constructed consisting of a <xref:System.Activities.Statements.Sequence> activity that contains child activities including a <xref:System.Activities.Statements.TransactionScope> activity.</span></span> <span data-ttu-id="507c3-111">Les activités <xref:System.Activities.Statements.TransactionScope.Body%2A> du <xref:System.Activities.Statements.TransactionScope> s'exécutent sous la transaction initialisée par l'activité <xref:System.Activities.Statements.TransactionScope>.</span><span class="sxs-lookup"><span data-stu-id="507c3-111">The <xref:System.Activities.Statements.TransactionScope.Body%2A> activities of the <xref:System.Activities.Statements.TransactionScope> execute under the transaction initialized by the <xref:System.Activities.Statements.TransactionScope> activity.</span></span>  
  
```csharp  
static Activity ScenarioOne()  
{  
    return new Sequence  
    {  
        Activities =  
        {  
            new WriteLine { Text = "    Begin workflow" },  
  
            new TransactionScope  
            {  
                Body = new Sequence  
                {  
                    Activities =   
                    {  
                        new WriteLine { Text = "    Begin TransactionScope" },  
  
                        new PrintTransactionId(),  
  
                        new TransactionScopeTest(),  
  
                        new WriteLine { Text = "    End TransactionScope" },  
                    },  
                },  
            },  
  
            new WriteLine { Text = "    End workflow" },  
        }  
    };  
}  
```  
  
<span data-ttu-id="507c3-112">Pour plus d’informations, consultez Utilisation <xref:System.ServiceModel.Activities.TransactedReceiveScope>, consultez [Transactions circulant vers et depuis des Services de Workflow](../wcf/feature-details/flowing-transactions-into-and-out-of-workflow-services.md).</span><span class="sxs-lookup"><span data-stu-id="507c3-112">For more information, see about using <xref:System.ServiceModel.Activities.TransactedReceiveScope>, see [Flowing Transactions into and out of Workflow Services](../wcf/feature-details/flowing-transactions-into-and-out-of-workflow-services.md).</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="507c3-113">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="507c3-113">See also</span></span>

- <xref:System.Activities.Statements.TransactionScope>
- <xref:System.Transactions.TransactionScope>
- <xref:System.Transactions.Transaction.Current%2A?displayProperty=nameWithType>
