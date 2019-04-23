---
title: System.ServiceModel.TxFailedToNegotiateOleTx
ms.date: 03/30/2017
ms.assetid: 3f0f0b4b-a1ad-4704-8329-455daf54892d
ms.openlocfilehash: 2de1aa51d58d9d86f953e027fd3f7f172e3887d3
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59097562"
---
# <a name="systemservicemodeltxfailedtonegotiateoletx"></a><span data-ttu-id="e3589-102">System.ServiceModel.TxFailedToNegotiateOleTx</span><span class="sxs-lookup"><span data-stu-id="e3589-102">System.ServiceModel.TxFailedToNegotiateOleTx</span></span>
<span data-ttu-id="e3589-103">La négociation du protocole OleTransactions n'a pas pu se terminer pour le contexte de coordination spécifié.</span><span class="sxs-lookup"><span data-stu-id="e3589-103">The OleTransactions protocol negotiation failed to complete for the specified coordination context.</span></span>  
  
## <a name="description"></a><span data-ttu-id="e3589-104">Description</span><span class="sxs-lookup"><span data-stu-id="e3589-104">Description</span></span>  
 <span data-ttu-id="e3589-105">Tracé lorsqu'une transaction entrante avec des informations OleTx ne peut pas utiliser les informations OleTx jointes, et a recours à l'utilisation de WS-AT à la place.</span><span class="sxs-lookup"><span data-stu-id="e3589-105">Traced when an incoming transaction with OleTx information is unable to use the attached OleTx information, and will fall-back to using WS-AT instead.</span></span>  
  
## <a name="troubleshooting"></a><span data-ttu-id="e3589-106">Résolution des problèmes</span><span class="sxs-lookup"><span data-stu-id="e3589-106">Troubleshooting</span></span>  
 <span data-ttu-id="e3589-107">Indique un problème potentiel avec la communication de MSDTC RPC entre les ordinateurs.</span><span class="sxs-lookup"><span data-stu-id="e3589-107">Indicates a potential problem with MSDTC RPC communication between the machines.</span></span> <span data-ttu-id="e3589-108">Si beaucoup de ces suivis apparaissent dans le journal, il peut s'ensuivre une baisse radicale des performances.</span><span class="sxs-lookup"><span data-stu-id="e3589-108">If many of these traces appear in the log, a drastic decrease in performance can result.</span></span>  <span data-ttu-id="e3589-109">Si OleTx n'est pas souhaité, affectez la valeur 0 à `OleTxUpgradeEnabled` dans la configuration du registre WS-AT.</span><span class="sxs-lookup"><span data-stu-id="e3589-109">If OleTx is not desired, set `OleTxUpgradeEnabled` to 0 in the WS-AT registry configuration.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="e3589-110">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e3589-110">See also</span></span>

- [<span data-ttu-id="e3589-111">Suivi</span><span class="sxs-lookup"><span data-stu-id="e3589-111">Tracing</span></span>](../../../../../docs/framework/wcf/diagnostics/tracing/index.md)
- [<span data-ttu-id="e3589-112">Utilisation du suivi pour résoudre les problèmes posés par votre application</span><span class="sxs-lookup"><span data-stu-id="e3589-112">Using Tracing to Troubleshoot Your Application</span></span>](../../../../../docs/framework/wcf/diagnostics/tracing/using-tracing-to-troubleshoot-your-application.md)
- [<span data-ttu-id="e3589-113">Administration et diagnostics</span><span class="sxs-lookup"><span data-stu-id="e3589-113">Administration and Diagnostics</span></span>](../../../../../docs/framework/wcf/diagnostics/index.md)
