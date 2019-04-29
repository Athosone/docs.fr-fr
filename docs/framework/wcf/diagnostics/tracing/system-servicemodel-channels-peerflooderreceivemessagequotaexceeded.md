---
title: System.ServiceModel.Channels.PeerFlooderReceiveMessageQuotaExceeded
ms.date: 03/30/2017
ms.assetid: b8371d0a-843e-440b-b86a-6996db131cb0
ms.openlocfilehash: 0ca3d198ce225221348ac7b405ea91ad215cd298
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61950642"
---
# <a name="systemservicemodelchannelspeerflooderreceivemessagequotaexceeded"></a><span data-ttu-id="cadf9-102">System.ServiceModel.Channels.PeerFlooderReceiveMessageQuotaExceeded</span><span class="sxs-lookup"><span data-stu-id="cadf9-102">System.ServiceModel.Channels.PeerFlooderReceiveMessageQuotaExceeded</span></span>
<span data-ttu-id="cadf9-103">Le taux de réception entrant des messages est trop élevé.</span><span class="sxs-lookup"><span data-stu-id="cadf9-103">The inbound receive rate of messages is too high.</span></span>  
  
## <a name="description"></a><span data-ttu-id="cadf9-104">Description</span><span class="sxs-lookup"><span data-stu-id="cadf9-104">Description</span></span>  
 <span data-ttu-id="cadf9-105">Ce suivi se produit lors de la tentative de traitement des messages entrants.</span><span class="sxs-lookup"><span data-stu-id="cadf9-105">This trace occurs when attempting to process inbound messages.</span></span> <span data-ttu-id="cadf9-106">Un message n'a pas pu être transmis à un voisin spécifique en raison du dépassement du quota défini pour ce voisin.</span><span class="sxs-lookup"><span data-stu-id="cadf9-106">A message could not be forwarded to a specific neighbor because the quota set for that neighbor has been exceeded.</span></span> <span data-ttu-id="cadf9-107">Ce cas se produit lorsqu’un voisin qui ne répond pas ne peut pas effacer un backlog avec messages en attente pour ce voisin.</span><span class="sxs-lookup"><span data-stu-id="cadf9-107">This occurs when an unresponsive neighbor fails to clear a backlog of messages pending for that neighbor.</span></span>  
  
## <a name="troubleshooting"></a><span data-ttu-id="cadf9-108">Résolution des problèmes</span><span class="sxs-lookup"><span data-stu-id="cadf9-108">Troubleshooting</span></span>  
 <span data-ttu-id="cadf9-109">Réduisez le taux auquel les messages sont envoyés dans la maille.</span><span class="sxs-lookup"><span data-stu-id="cadf9-109">Reduce the rate at which messages are sent within the mesh.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="cadf9-110">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="cadf9-110">See also</span></span>

- [<span data-ttu-id="cadf9-111">Suivi</span><span class="sxs-lookup"><span data-stu-id="cadf9-111">Tracing</span></span>](../../../../../docs/framework/wcf/diagnostics/tracing/index.md)
- [<span data-ttu-id="cadf9-112">Utilisation du suivi pour résoudre les problèmes posés par votre application</span><span class="sxs-lookup"><span data-stu-id="cadf9-112">Using Tracing to Troubleshoot Your Application</span></span>](../../../../../docs/framework/wcf/diagnostics/tracing/using-tracing-to-troubleshoot-your-application.md)
- [<span data-ttu-id="cadf9-113">Administration et diagnostics</span><span class="sxs-lookup"><span data-stu-id="cadf9-113">Administration and Diagnostics</span></span>](../../../../../docs/framework/wcf/diagnostics/index.md)
