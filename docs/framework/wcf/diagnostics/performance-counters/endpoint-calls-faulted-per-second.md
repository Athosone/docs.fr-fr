---
title: 'Point de terminaison : Appels ayant renvoyé une erreur par seconde'
ms.date: 03/30/2017
ms.assetid: 9840fc0a-0e4d-4638-96fd-40e3ab9e4667
ms.openlocfilehash: f425d95868a9ba5bc3c2f2291db2bc414b1918e2
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59122224"
---
# <a name="endpoint-calls-faulted-per-second"></a><span data-ttu-id="2920f-102">Point de terminaison : Appels ayant renvoyé une erreur par seconde</span><span class="sxs-lookup"><span data-stu-id="2920f-102">Endpoint: Calls Faulted Per Second</span></span>
<span data-ttu-id="2920f-103">Nom du compteur : Appels erronés par seconde.</span><span class="sxs-lookup"><span data-stu-id="2920f-103">Counter Name: Calls Faulted Per Second.</span></span>  
  
## <a name="description"></a><span data-ttu-id="2920f-104">Description</span><span class="sxs-lookup"><span data-stu-id="2920f-104">Description</span></span>  
 <span data-ttu-id="2920f-105">Nombre d'appels qui ont retourné des erreurs à ce point de terminaison en une seconde.</span><span class="sxs-lookup"><span data-stu-id="2920f-105">Number of calls that have returned faults to this endpoint in a second.</span></span>  
  
 <span data-ttu-id="2920f-106">Ce compteur est de type de compteur de performances [PERF_COUNTER_COUNTER](https://go.microsoft.com/fwlink/?LinkID=94649), dont la valeur est calculée à l’aide de la formule suivante.</span><span class="sxs-lookup"><span data-stu-id="2920f-106">This counter is of performance counter type [PERF_COUNTER_COUNTER](https://go.microsoft.com/fwlink/?LinkID=94649), whose value is calculated using the following formula.</span></span>  
  
 <span data-ttu-id="2920f-107">(N 1 - N 0 ) / ( (D 1 -D 0 ) / F)</span><span class="sxs-lookup"><span data-stu-id="2920f-107">(N 1 - N 0 ) / ( (D 1 -D 0 ) / F)</span></span>  
  
 <span data-ttu-id="2920f-108">Dans les applications Windows Communication Foundation (WCF), les méthodes de service communiquent des informations d’erreur de traitement à l’aide de messages d’erreur SOAP.</span><span class="sxs-lookup"><span data-stu-id="2920f-108">In Windows Communication Foundation (WCF) applications, service methods communicate processing error information using SOAP fault messages.</span></span> <span data-ttu-id="2920f-109">Les erreurs SOAP sont des types de message inclus dans les métadonnées d'une opération de service et créent, par conséquent, un contrat d'erreur permettant aux clients d'améliorer la fiabilité ou l'interactivité de leur exécution.</span><span class="sxs-lookup"><span data-stu-id="2920f-109">SOAP faults are message types that are included in the metadata for a service operation and therefore create a fault contract that clients can use to make their execution more robust or interactive.</span></span> <span data-ttu-id="2920f-110">Les erreurs SOAP étant exprimées aux clients dans un format XML, elles sont très interopérables.</span><span class="sxs-lookup"><span data-stu-id="2920f-110">Since SOAP faults are expressed to clients in XML form, they are highly interoperable.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="2920f-111">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="2920f-111">See also</span></span>

- [<span data-ttu-id="2920f-112">Spécification et gestion des erreurs dans les contrats et les services</span><span class="sxs-lookup"><span data-stu-id="2920f-112">Specifying and Handling Faults in Contracts and Services</span></span>](../../../../../docs/framework/wcf/specifying-and-handling-faults-in-contracts-and-services.md)
