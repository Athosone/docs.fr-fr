---
title: System.ServiceModel.MessageClosedAgain
ms.date: 03/30/2017
ms.assetid: 24c274d4-65cd-4c91-9869-bc6eb34ef979
ms.openlocfilehash: a18355d55359df665d0e936ce95da34bf07aec6a
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61761505"
---
# <a name="systemservicemodelmessageclosedagain"></a><span data-ttu-id="62323-102">System.ServiceModel.MessageClosedAgain</span><span class="sxs-lookup"><span data-stu-id="62323-102">System.ServiceModel.MessageClosedAgain</span></span>
<span data-ttu-id="62323-103">System.ServiceModel.MessageClosedAgain</span><span class="sxs-lookup"><span data-stu-id="62323-103">System.ServiceModel.MessageClosedAgain</span></span>  
  
## <a name="description"></a><span data-ttu-id="62323-104">Description</span><span class="sxs-lookup"><span data-stu-id="62323-104">Description</span></span>  
 <span data-ttu-id="62323-105">Un message a de nouveau été fermé.</span><span class="sxs-lookup"><span data-stu-id="62323-105">A message was closed again.</span></span>  
  
 <span data-ttu-id="62323-106">Un message ne doit être fermé qu'une seule fois.</span><span class="sxs-lookup"><span data-stu-id="62323-106">A message should be closed only once.</span></span> <span data-ttu-id="62323-107">Si ce suivi est émis dans le code d’extension utilisateur, il indique que ce code ferme un message qui a déjà été fermé.</span><span class="sxs-lookup"><span data-stu-id="62323-107">If this trace is being emitted in user extension code, it indicates that the user extension code is closing a message that has already been closed.</span></span> <span data-ttu-id="62323-108">Si ce suivi est émis via le code produit, il indique que le code d’extension utilisateur peut éventuellement fermer un message trop tôt.</span><span class="sxs-lookup"><span data-stu-id="62323-108">If this trace is being emitted through product code, it indicates that the user extension code could potentially be closing a message too early.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="62323-109">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="62323-109">See also</span></span>

- [<span data-ttu-id="62323-110">Suivi</span><span class="sxs-lookup"><span data-stu-id="62323-110">Tracing</span></span>](../../../../../docs/framework/wcf/diagnostics/tracing/index.md)
- [<span data-ttu-id="62323-111">Utilisation du suivi pour résoudre les problèmes posés par votre application</span><span class="sxs-lookup"><span data-stu-id="62323-111">Using Tracing to Troubleshoot Your Application</span></span>](../../../../../docs/framework/wcf/diagnostics/tracing/using-tracing-to-troubleshoot-your-application.md)
- [<span data-ttu-id="62323-112">Administration et diagnostics</span><span class="sxs-lookup"><span data-stu-id="62323-112">Administration and Diagnostics</span></span>](../../../../../docs/framework/wcf/diagnostics/index.md)
