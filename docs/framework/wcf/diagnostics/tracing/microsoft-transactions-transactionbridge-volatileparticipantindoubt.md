---
title: Microsoft.Transactions.TransactionBridge.VolatileParticipantInDoubt
ms.date: 03/30/2017
ms.assetid: 3e8fc825-9f22-47e7-9c16-d64ef291c932
ms.openlocfilehash: 9434f2f902a50a37fb3efee22fd3b18b33af9129
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59138968"
---
# <a name="microsofttransactionstransactionbridgevolatileparticipantindoubt"></a><span data-ttu-id="7c001-102">Microsoft.Transactions.TransactionBridge.VolatileParticipantInDoubt</span><span class="sxs-lookup"><span data-stu-id="7c001-102">Microsoft.Transactions.TransactionBridge.VolatileParticipantInDoubt</span></span>
<span data-ttu-id="7c001-103">Le service du protocole WS-AT a reçu un message Prepared ou Replay d'un participant volatil non reconnu.</span><span class="sxs-lookup"><span data-stu-id="7c001-103">The WS-AT protocol service received a Prepared or Replay message from an unrecognized volatile participant.</span></span> <span data-ttu-id="7c001-104">Une faute a été renvoyée au participant, qui déclarera que le résultat de la transaction est douteux.</span><span class="sxs-lookup"><span data-stu-id="7c001-104">A fault was returned to the participant, declares that the transaction's outcome is in doubt.</span></span>  
  
## <a name="description"></a><span data-ttu-id="7c001-105">Description</span><span class="sxs-lookup"><span data-stu-id="7c001-105">Description</span></span>  
 <span data-ttu-id="7c001-106">Suivi généré lorsque le gestionnaire de transactions local reçoit un message Prepared ou Replay d’une inscription volatile qu’il a déjà oubliée.</span><span class="sxs-lookup"><span data-stu-id="7c001-106">Traced when the local Transaction Manager receives a Prepared or Replay message from a Volatile enlistment that it has already forgotten.</span></span>  
  
## <a name="troubleshooting"></a><span data-ttu-id="7c001-107">Résolution des problèmes</span><span class="sxs-lookup"><span data-stu-id="7c001-107">Troubleshooting</span></span>  
 <span data-ttu-id="7c001-108">Recherchez les causes potentielles de retard des messages qui viennent du participant volatil.</span><span class="sxs-lookup"><span data-stu-id="7c001-108">Investigate potential causes of late messages coming from the Volatile participant.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="7c001-109">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="7c001-109">See also</span></span>

- [<span data-ttu-id="7c001-110">Suivi</span><span class="sxs-lookup"><span data-stu-id="7c001-110">Tracing</span></span>](../../../../../docs/framework/wcf/diagnostics/tracing/index.md)
- [<span data-ttu-id="7c001-111">Utilisation du suivi pour résoudre les problèmes posés par votre application</span><span class="sxs-lookup"><span data-stu-id="7c001-111">Using Tracing to Troubleshoot Your Application</span></span>](../../../../../docs/framework/wcf/diagnostics/tracing/using-tracing-to-troubleshoot-your-application.md)
- [<span data-ttu-id="7c001-112">Administration et diagnostics</span><span class="sxs-lookup"><span data-stu-id="7c001-112">Administration and Diagnostics</span></span>](../../../../../docs/framework/wcf/diagnostics/index.md)
