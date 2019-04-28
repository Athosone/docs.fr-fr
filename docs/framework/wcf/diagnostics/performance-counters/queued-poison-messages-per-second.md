---
title: Messages incohérents en file d'attente par seconde
ms.date: 03/30/2017
ms.assetid: d193fdd1-02f1-44a0-906e-f632a8f574c3
ms.openlocfilehash: d4c921b105dfd1c1a364d2c86f54ab920078dd4a
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61916147"
---
# <a name="queued-poison-messages-per-second"></a><span data-ttu-id="73912-102">Messages incohérents en file d'attente par seconde</span><span class="sxs-lookup"><span data-stu-id="73912-102">Queued Poison Messages Per Second</span></span>
<span data-ttu-id="73912-103">Nom du compteur : Messages incohérents en file d’attente par seconde.</span><span class="sxs-lookup"><span data-stu-id="73912-103">Counter Name: Queued Poison Messages Per Second.</span></span>  
  
## <a name="description"></a><span data-ttu-id="73912-104">Description</span><span class="sxs-lookup"><span data-stu-id="73912-104">Description</span></span>  
 <span data-ttu-id="73912-105">Nombre de messages vers ce service marqués comme incohérents par le transport de mise en file d'attente par seconde.</span><span class="sxs-lookup"><span data-stu-id="73912-105">Number of messages that are marked poisoned by the queued transport at this service in a second.</span></span>  
  
 <span data-ttu-id="73912-106">Ce compteur est de type de compteur de performances [PERF_COUNTER_COUNTER](https://go.microsoft.com/fwlink/?LinkID=94649), dont la valeur est calculée à l’aide de la formule suivante.</span><span class="sxs-lookup"><span data-stu-id="73912-106">This counter is of performance counter type [PERF_COUNTER_COUNTER](https://go.microsoft.com/fwlink/?LinkID=94649), whose value is calculated using the following formula.</span></span>  
  
 <span data-ttu-id="73912-107">(N 1 - N 0 ) / ( (D 1 -D 0 ) / F)</span><span class="sxs-lookup"><span data-stu-id="73912-107">(N 1 - N 0 ) / ( (D 1 -D 0 ) / F)</span></span>
