---
title: Sécurisation des services et des clients
ms.date: 03/30/2017
helpviewer_keywords:
- message security [WCF]
ms.assetid: e681f3bd-0c09-4a58-b0e4-0ecbdf1aa6c7
ms.openlocfilehash: e455c7a48e1484d5acdcc5f6cdc9098997a3ba83
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61990936"
---
# <a name="securing-services-and-clients"></a><span data-ttu-id="8f938-102">Sécurisation des services et des clients</span><span class="sxs-lookup"><span data-stu-id="8f938-102">Securing Services and Clients</span></span>
<span data-ttu-id="8f938-103">Les informations contenues dans cette section se concentre sur la programmation de la sécurité dans Windows Communication Foundation (WCF).</span><span class="sxs-lookup"><span data-stu-id="8f938-103">The information in this section focuses on programming security in Windows Communication Foundation (WCF).</span></span> <span data-ttu-id="8f938-104">En général, l’opération inclut la sélection d’une liaison appropriée fournie par le système, la définition des propriétés de l’élément de sécurité, puis la définition des propriétés des comportements du service qui déterminent la manière dont les informations d’identification sont récupérées pour être utilisées par le service ou le client.</span><span class="sxs-lookup"><span data-stu-id="8f938-104">Generally, this includes selecting an appropriate system-provided binding, setting the properties of the security element, and then setting properties of the service behaviors that govern how credentials are retrieved for use by either the service or the client.</span></span> <span data-ttu-id="8f938-105">Ces techniques couvrent les exigences de sécurité de la plupart des utilisateurs pour la plupart des scénarios, comme indiqué dans [scénarios de sécurité courants](../../../../docs/framework/wcf/feature-details/common-security-scenarios.md).</span><span class="sxs-lookup"><span data-stu-id="8f938-105">These techniques cover the security requirements of most users for most scenarios, as shown in [Common Security Scenarios](../../../../docs/framework/wcf/feature-details/common-security-scenarios.md).</span></span> <span data-ttu-id="8f938-106">Si votre scénario requiert des fonctionnalités supplémentaires, consultez tout d’abord [fonctionnalités de sécurité avec les liaisons personnalisées](../../../../docs/framework/wcf/feature-details/security-capabilities-with-custom-bindings.md); si une solution n’est pas évident, consultez [extension de sécurité](../../../../docs/framework/wcf/extending/extending-security.md).</span><span class="sxs-lookup"><span data-stu-id="8f938-106">If your scenario requires more capabilities, first see [Security Capabilities with Custom Bindings](../../../../docs/framework/wcf/feature-details/security-capabilities-with-custom-bindings.md); if a solution is not apparent, see [Extending Security](../../../../docs/framework/wcf/extending/extending-security.md).</span></span> <span data-ttu-id="8f938-107">Si vous créez (ou interopération avec) un système qui utilise des revendications riches, consultez les rubriques de [autorisation](../../../../docs/framework/wcf/feature-details/authorization-in-wcf.md).</span><span class="sxs-lookup"><span data-stu-id="8f938-107">If you are creating (or interoperating with) a system that uses rich claims, see the topics in [Authorization](../../../../docs/framework/wcf/feature-details/authorization-in-wcf.md).</span></span>  
  
## <a name="in-this-section"></a><span data-ttu-id="8f938-108">Dans cette section</span><span class="sxs-lookup"><span data-stu-id="8f938-108">In This Section</span></span>  
 [<span data-ttu-id="8f938-109">Programmation de la sécurité dans WCF</span><span class="sxs-lookup"><span data-stu-id="8f938-109">Programming WCF Security</span></span>](../../../../docs/framework/wcf/feature-details/programming-wcf-security.md)  
 <span data-ttu-id="8f938-110">Vue d'ensemble du modèle de programmation utilisé pour sécuriser des messages.</span><span class="sxs-lookup"><span data-stu-id="8f938-110">An overview of the programming model used to secure messages.</span></span>  
  
 [<span data-ttu-id="8f938-111">Vue d’ensemble de la sécurité de transport</span><span class="sxs-lookup"><span data-stu-id="8f938-111">Transport Security Overview</span></span>](../../../../docs/framework/wcf/feature-details/transport-security-overview.md)  
 <span data-ttu-id="8f938-112">Vue d'ensemble de la sécurisation des messages par le biais de la couche transport.</span><span class="sxs-lookup"><span data-stu-id="8f938-112">An overview of how to secure messages through the transport layer.</span></span>  
  
 [<span data-ttu-id="8f938-113">Sécurité de message</span><span class="sxs-lookup"><span data-stu-id="8f938-113">Message Security</span></span>](../../../../docs/framework/wcf/feature-details/message-security-in-wcf.md)  
 <span data-ttu-id="8f938-114">Récapitule les raisons d’utiliser la sécurité au niveau du message dans Windows Communication Foundation (WCF).</span><span class="sxs-lookup"><span data-stu-id="8f938-114">Summarizes reasons for using message-level security in Windows Communication Foundation (WCF).</span></span>  
  
 [<span data-ttu-id="8f938-115">Sessions sécurisées</span><span class="sxs-lookup"><span data-stu-id="8f938-115">Secure Sessions</span></span>](../../../../docs/framework/wcf/feature-details/secure-sessions.md)  
 <span data-ttu-id="8f938-116">Présentation des considérations nécessaires lors de la sécurisation d’une session WCF.</span><span class="sxs-lookup"><span data-stu-id="8f938-116">A discussion of the considerations required when securing a WCF session.</span></span>  
  
 [<span data-ttu-id="8f938-117">Utilisation des certificats</span><span class="sxs-lookup"><span data-stu-id="8f938-117">Working with Certificates</span></span>](../../../../docs/framework/wcf/feature-details/working-with-certificates.md)  
 <span data-ttu-id="8f938-118">Explication de quelques-unes des tâches courantes requises lors de l’utilisation de certificats X.509.</span><span class="sxs-lookup"><span data-stu-id="8f938-118">An explanation of some of the common tasks required when using X.509 certificates.</span></span>  
  
## <a name="reference"></a><span data-ttu-id="8f938-119">Référence</span><span class="sxs-lookup"><span data-stu-id="8f938-119">Reference</span></span>  
 <xref:System.ServiceModel>  
  
 <xref:System.ServiceModel.Channels>  
  
 <xref:System.ServiceModel.Security>  
  
## <a name="related-sections"></a><span data-ttu-id="8f938-120">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="8f938-120">Related Sections</span></span>  
 [<span data-ttu-id="8f938-121">Concepts relatifs à la sécurité</span><span class="sxs-lookup"><span data-stu-id="8f938-121">Security Concepts</span></span>](../../../../docs/framework/wcf/feature-details/security-concepts.md)  
  
 [<span data-ttu-id="8f938-122">Extension de la sécurité</span><span class="sxs-lookup"><span data-stu-id="8f938-122">Extending Security</span></span>](../../../../docs/framework/wcf/extending/extending-security.md)  
  
 [<span data-ttu-id="8f938-123">Scénarios de sécurité courants</span><span class="sxs-lookup"><span data-stu-id="8f938-123">Common Security Scenarios</span></span>](../../../../docs/framework/wcf/feature-details/common-security-scenarios.md)  
  
 [<span data-ttu-id="8f938-124">Liaisons et sécurité</span><span class="sxs-lookup"><span data-stu-id="8f938-124">Bindings and Security</span></span>](../../../../docs/framework/wcf/feature-details/bindings-and-security.md)  
  
 [<span data-ttu-id="8f938-125">Fonctionnalités de sécurité avec des liaisons personnalisées</span><span class="sxs-lookup"><span data-stu-id="8f938-125">Security Capabilities with Custom Bindings</span></span>](../../../../docs/framework/wcf/feature-details/security-capabilities-with-custom-bindings.md)  
  
 [<span data-ttu-id="8f938-126">Extension de la sécurité</span><span class="sxs-lookup"><span data-stu-id="8f938-126">Extending Security</span></span>](../../../../docs/framework/wcf/extending/extending-security.md)  
  
 [<span data-ttu-id="8f938-127">Autorisation</span><span class="sxs-lookup"><span data-stu-id="8f938-127">Authorization</span></span>](../../../../docs/framework/wcf/feature-details/authorization-in-wcf.md)  
  
## <a name="see-also"></a><span data-ttu-id="8f938-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="8f938-128">See also</span></span>

- [<span data-ttu-id="8f938-129">Programmation WCF de base</span><span class="sxs-lookup"><span data-stu-id="8f938-129">Basic WCF Programming</span></span>](../../../../docs/framework/wcf/basic-wcf-programming.md)
- [<span data-ttu-id="8f938-130">Modèle de sécurité pour Windows Server AppFabric</span><span class="sxs-lookup"><span data-stu-id="8f938-130">Security Model for Windows Server App Fabric</span></span>](https://go.microsoft.com/fwlink/?LinkID=201279&clcid=0x409)
