---
title: Implémentation d'un proxy de découverte
ms.date: 03/30/2017
ms.assetid: dda20e79-8df3-438e-a281-69d779d978ec
ms.openlocfilehash: 5d9296d8ba70d4c9e8d8339fa3a032d9c4c62826
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62047059"
---
# <a name="implementing-a-discovery-proxy"></a><span data-ttu-id="eccc3-102">Implémentation d'un proxy de découverte</span><span class="sxs-lookup"><span data-stu-id="eccc3-102">Implementing a Discovery Proxy</span></span>
<span data-ttu-id="eccc3-103">Cette section décrit les étapes nécessaires pour implémenter un proxy de découverte.</span><span class="sxs-lookup"><span data-stu-id="eccc3-103">This section describes the steps required to implement a discovery proxy.</span></span> <span data-ttu-id="eccc3-104">Un proxy de découverte est un service autonome qui contient un référentiel de services.</span><span class="sxs-lookup"><span data-stu-id="eccc3-104">A discovery proxy is a standalone service that contains a repository of services.</span></span> <span data-ttu-id="eccc3-105">Les clients peuvent interroger un proxy de découverte pour trouver les services détectables que le proxy connaît.</span><span class="sxs-lookup"><span data-stu-id="eccc3-105">Clients can query a discovery proxy to find discoverable services that the proxy is aware of.</span></span> <span data-ttu-id="eccc3-106">La manière dont un proxy est rempli avec des services incombe à l'implémenteur.</span><span class="sxs-lookup"><span data-stu-id="eccc3-106">How a proxy is populated with services is up to the implementer.</span></span> <span data-ttu-id="eccc3-107">Par exemple, un proxy de découverte peut se connecter à un référentiel de services existants et rendre cette information détectable, un administrateur peut utiliser une API de gestion pour ajouter des services détectables à un proxy, ou un proxy de découverte peut utiliser les fonctionnalités d'annonce pour mettre à jour son cache interne.</span><span class="sxs-lookup"><span data-stu-id="eccc3-107">For example, a discovery proxy can connect to an existing service repository and make that information discoverable, an administrator can use a management API to add discoverable services to a proxy, or a discovery proxy can use the announcement functionality to update its internal cache.</span></span>  
  
 <span data-ttu-id="eccc3-108">L'implémentation WCF fournit des classes de base qui vous permettent de générer facilement un proxy.</span><span class="sxs-lookup"><span data-stu-id="eccc3-108">The WCF implementation provides base classes that allow you to easily build a proxy.</span></span> <span data-ttu-id="eccc3-109">Vous pouvez utiliser ces API pour générer un en-tête du proxy de découverte sur votre base de données de référentiel existante.</span><span class="sxs-lookup"><span data-stu-id="eccc3-109">You can utilize these APIs to build a Discovery Proxy on top of your existing repository.</span></span>  
  
 <span data-ttu-id="eccc3-110">Le proxy de découverte implémenté dans cet exemple est identique à n'importe quel autre service WCF, en ce sens que vous pouvez également rendre le proxy de découverte détectable et faire localiser ses points de terminaison par les clients.</span><span class="sxs-lookup"><span data-stu-id="eccc3-110">The discovery proxy implemented here is like any other WCF services, in that you can also make the discovery proxy discoverable and have the clients locate its endpoints.</span></span>  
  
## <a name="in-this-section"></a><span data-ttu-id="eccc3-111">Dans cette section</span><span class="sxs-lookup"><span data-stu-id="eccc3-111">In This Section</span></span>  
 [<span data-ttu-id="eccc3-112">Guide pratique pour Implémenter un Proxy de découverte</span><span class="sxs-lookup"><span data-stu-id="eccc3-112">How to: Implement a Discovery Proxy</span></span>](../../../../docs/framework/wcf/feature-details/how-to-implement-a-discovery-proxy.md)  
 <span data-ttu-id="eccc3-113">Décrit comment implémenter un proxy de découverte.</span><span class="sxs-lookup"><span data-stu-id="eccc3-113">Describes how to implement a discovery proxy.</span></span>  
  
 [<span data-ttu-id="eccc3-114">Guide pratique pour Implémenter un Service détectable qui s’enregistre avec le Proxy de découverte</span><span class="sxs-lookup"><span data-stu-id="eccc3-114">How to: Implement a Discoverable Service that Registers with the Discovery Proxy</span></span>](../../../../docs/framework/wcf/feature-details/discoverable-service-that-registers-with-the-discovery-proxy.md)  
 <span data-ttu-id="eccc3-115">Décrit comment implémenter un service WCF détectable qui s’enregistre avec le proxy de découverte.</span><span class="sxs-lookup"><span data-stu-id="eccc3-115">Describes how to implement a discoverable WCF service that registers with the discovery proxy.</span></span>  
  
 [<span data-ttu-id="eccc3-116">Guide pratique pour Implémenter une Application cliente qui utilise le Proxy de découverte pour rechercher un Service</span><span class="sxs-lookup"><span data-stu-id="eccc3-116">How to: Implement a Client Application that Uses the Discovery Proxy to Find a Service</span></span>](../../../../docs/framework/wcf/feature-details/client-app-discovery-proxy-to-find-a-service.md)  
 <span data-ttu-id="eccc3-117">Décrit comment implémenter une application cliente WCF qui utilise le proxy de découverte pour rechercher un service.</span><span class="sxs-lookup"><span data-stu-id="eccc3-117">Describes how to implement a WCF client application that uses the discovery proxy to search for a service.</span></span>  
  
 [<span data-ttu-id="eccc3-118">Guide pratique pour Tester le Proxy de découverte</span><span class="sxs-lookup"><span data-stu-id="eccc3-118">How to: Test the Discovery Proxy</span></span>](../../../../docs/framework/wcf/feature-details/how-to-test-the-discovery-proxy.md)  
 <span data-ttu-id="eccc3-119">Décrit comment tester le code écrit dans les trois rubriques précédentes.</span><span class="sxs-lookup"><span data-stu-id="eccc3-119">Describes how to test the code written in the previous three topics.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="eccc3-120">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="eccc3-120">See also</span></span>

- [<span data-ttu-id="eccc3-121">Découverte WCF</span><span class="sxs-lookup"><span data-stu-id="eccc3-121">WCF Discovery</span></span>](../../../../docs/framework/wcf/feature-details/wcf-discovery.md)
- [<span data-ttu-id="eccc3-122">Guide pratique pour Ajouter par programmation la détectabilité à un Service WCF et un Client</span><span class="sxs-lookup"><span data-stu-id="eccc3-122">How to: Programmatically Add Discoverability to a WCF Service and Client</span></span>](../../../../docs/framework/wcf/feature-details/how-to-programmatically-add-discoverability-to-a-wcf-service-and-client.md)
