---
title: Microsoft.Transactions.TransactionBridge.CoordinatorStateMachineFinished
ms.date: 03/30/2017
ms.assetid: 16cb428d-d886-4789-a961-6fded4b0dbba
ms.openlocfilehash: bffaed4976d82202eaea9ce50f6d389548fdabfd
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59144824"
---
# <a name="microsofttransactionstransactionbridgecoordinatorstatemachinefinished"></a><span data-ttu-id="dbb11-102">Microsoft.Transactions.TransactionBridge.CoordinatorStateMachineFinished</span><span class="sxs-lookup"><span data-stu-id="dbb11-102">Microsoft.Transactions.TransactionBridge.CoordinatorStateMachineFinished</span></span>
<span data-ttu-id="dbb11-103">La machine à états pour un enrôlement de coordinateur est passée à l'état Finished.</span><span class="sxs-lookup"><span data-stu-id="dbb11-103">The state machine for a coordinator enlistment has entered the finished state.</span></span>  
  
## <a name="description"></a><span data-ttu-id="dbb11-104">Description</span><span class="sxs-lookup"><span data-stu-id="dbb11-104">Description</span></span>  
 <span data-ttu-id="dbb11-105">Suivi lorsque le gestionnaire de transactions local croit qu’un enrôlement de coordinateur supérieur a terminé le traitement 2PC.</span><span class="sxs-lookup"><span data-stu-id="dbb11-105">Traced when the local Transaction Manager believes a superior coordinator enlistment has completed 2pc processing.</span></span> <span data-ttu-id="dbb11-106">Le résultat peut être Committed, Aborted ou Forgotten.</span><span class="sxs-lookup"><span data-stu-id="dbb11-106">The outcome for the enlistment can be Committed or Aborted or Forgotten.</span></span> <span data-ttu-id="dbb11-107">Suivi également lorsque le gestionnaire de transaction local vote ReadOnly pendant la préparation.</span><span class="sxs-lookup"><span data-stu-id="dbb11-107">It is also traced if the local Transaction Manager votes ReadOnly during Prepare.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="dbb11-108">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="dbb11-108">See also</span></span>

- [<span data-ttu-id="dbb11-109">Suivi</span><span class="sxs-lookup"><span data-stu-id="dbb11-109">Tracing</span></span>](../../../../../docs/framework/wcf/diagnostics/tracing/index.md)
- [<span data-ttu-id="dbb11-110">Utilisation du suivi pour résoudre les problèmes posés par votre application</span><span class="sxs-lookup"><span data-stu-id="dbb11-110">Using Tracing to Troubleshoot Your Application</span></span>](../../../../../docs/framework/wcf/diagnostics/tracing/using-tracing-to-troubleshoot-your-application.md)
- [<span data-ttu-id="dbb11-111">Administration et diagnostics</span><span class="sxs-lookup"><span data-stu-id="dbb11-111">Administration and Diagnostics</span></span>](../../../../../docs/framework/wcf/diagnostics/index.md)
