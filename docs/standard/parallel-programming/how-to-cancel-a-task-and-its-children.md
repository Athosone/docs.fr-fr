---
title: 'Procédure : annuler une tâche et ses enfants'
ms.date: 03/30/2017
ms.technology: dotnet-standard
dev_langs:
- csharp
- vb
helpviewer_keywords:
- tasks, how to cancel
ms.assetid: 08574301-8331-4719-ad50-9cf7f6ff3048
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 08e5712db60fb09b48d6be9f35737c9a884d1ce8
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59324472"
---
# <a name="how-to-cancel-a-task-and-its-children"></a>Procédure : annuler une tâche et ses enfants
Ces exemples montrent comment effectuer les tâches suivantes :  
  
1. Créer et lancer une tâche annulable  
  
2. Passer un jeton d’annulation à votre délégué d’utilisateur et éventuellement à l’instance de tâche  
  
3. Notifier et répondre à la demande d’annulation dans votre délégué d’utilisateur  
  
4. Éventuellement notifier sur le thread appelant que la tâche a été annulée  
  
 Le thread appelant ne force pas l’arrêt de la tâche. Il signale seulement que son annulation a été demandée. Si la tâche est déjà en cours d’exécution, il incombe au délégué d’utilisateur de notifier la demande et d’y répondre de façon appropriée. Si l’annulation a été demandée avant l’exécution de la tâche, le délégué d’utilisateur n’est jamais exécuté et l’objet de tâche passe à l’état Canceled.  
  
## <a name="example"></a>Exemple  
 Cet exemple montre comment arrêter une <xref:System.Threading.Tasks.Task> et ses enfants en réponse à une demande d’annulation. Il montre également que quand un délégué d’utilisateur se termine en levant une <xref:System.Threading.Tasks.TaskCanceledException>, le thread appelant peut éventuellement utiliser la méthode <xref:System.Threading.Tasks.Task.Wait%2A> ou <xref:System.Threading.Tasks.Task.WaitAll%2A>pour attendre la fin des tâches. Dans ce cas, vous devez utiliser un bloc `try/catch` pour gérer les exceptions sur le thread appelant.  
  
 [!code-csharp[TPL_Cancellation#04](../../../samples/snippets/csharp/VS_Snippets_Misc/tpl_cancellation/cs/cancel1.cs#04)]
 [!code-vb[TPL_Cancellation#04](../../../samples/snippets/visualbasic/VS_Snippets_Misc/tpl_cancellation/vb/cancel1.vb#04)]  
  
 La classe <xref:System.Threading.Tasks.Task?displayProperty=nameWithType> est entièrement intégrée au modèle d’annulation qui est basé sur les types <xref:System.Threading.CancellationTokenSource?displayProperty=nameWithType> et <xref:System.Threading.CancellationToken?displayProperty=nameWithType>. Pour plus d’informations, consultez [Annulation dans les threads managés](../../../docs/standard/threading/cancellation-in-managed-threads.md) et [Annulation de tâches](../../../docs/standard/parallel-programming/task-cancellation.md).  
  
## <a name="see-also"></a>Voir aussi

- <xref:System.Threading.CancellationTokenSource?displayProperty=nameWithType>
- <xref:System.Threading.CancellationToken?displayProperty=nameWithType>
- <xref:System.Threading.Tasks.Task?displayProperty=nameWithType>
- <xref:System.Threading.Tasks.Task%601?displayProperty=nameWithType>
- [Programmation asynchrone basée sur les tâches](../../../docs/standard/parallel-programming/task-based-asynchronous-programming.md)
- [Tâches enfants attachées et détachées](../../../docs/standard/parallel-programming/attached-and-detached-child-tasks.md)
- [Expressions lambda en PLINQ et dans la bibliothèque parallèle de tâches](../../../docs/standard/parallel-programming/lambda-expressions-in-plinq-and-tpl.md)
