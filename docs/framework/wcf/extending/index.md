---
title: Extension de WCF
ms.date: 03/30/2017
helpviewer_keywords:
- WCF, extensibility
- extensibility [WCF]
- Windows Communication Foundation, extensibility
ms.assetid: c145e2f6-f402-41f5-8b5a-eee03978737b
ms.openlocfilehash: 24ad74f04a3ac31d0b0d0d87f0d74f88c0521f50
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61768717"
---
# <a name="extending-wcf"></a><span data-ttu-id="ee845-102">Extension de WCF</span><span class="sxs-lookup"><span data-stu-id="ee845-102">Extending WCF</span></span>
<span data-ttu-id="ee845-103">Windows Communication Foundation (WCF) permet de modifier et d’étendre des composants d’exécution pour contrôler avec précision et d’étendre les applications basées sur le service.</span><span class="sxs-lookup"><span data-stu-id="ee845-103">Windows Communication Foundation (WCF) allows you to modify and extend run time components to precisely control and extend service-based applications.</span></span> <span data-ttu-id="ee845-104">Les rubriques de cette section approfondissent le concept d'architecture d'extensibilité.</span><span class="sxs-lookup"><span data-stu-id="ee845-104">The topics in this section go in depth about the extensibility architecture.</span></span> <span data-ttu-id="ee845-105">Pour plus d’informations sur la programmation de base, consultez [programmation WCF de base](../../../../docs/framework/wcf/basic-wcf-programming.md).</span><span class="sxs-lookup"><span data-stu-id="ee845-105">For more information about basic programming, see [Basic WCF Programming](../../../../docs/framework/wcf/basic-wcf-programming.md).</span></span>  
  
## <a name="in-this-section"></a><span data-ttu-id="ee845-106">Dans cette section</span><span class="sxs-lookup"><span data-stu-id="ee845-106">In This Section</span></span>  
 [<span data-ttu-id="ee845-107">Extension de ServiceHost et de la couche de modèle de service</span><span class="sxs-lookup"><span data-stu-id="ee845-107">Extending ServiceHost and the Service Model Layer</span></span>](../../../../docs/framework/wcf/extending/extending-servicehost-and-the-service-model-layer.md)  
 <span data-ttu-id="ee845-108">La couche du modèle de service est chargée d'extraire des messages entrants des canaux sous-jacents, de les traduire dans des appels de méthode dans le code d'application et de renvoyer les résultats à l'appelant.</span><span class="sxs-lookup"><span data-stu-id="ee845-108">The service model layer is responsible for pulling incoming messages out of the underlying channels, translating them into method invocations in application code, and sending the results back to the caller.</span></span>  <span data-ttu-id="ee845-109">Les extensions de modèle de service modifient ou implémentent l'exécution ou les fonctionnalités de comportement et de communication ainsi que des fonctionnalités de répartiteur, des comportements personnalisés, l'interception de messages et de paramètres et d'autres fonctionnalités d'extensibilité.</span><span class="sxs-lookup"><span data-stu-id="ee845-109">Service model extensions modify or implement execution or communication behavior and features involving dispatcher functionality, custom behaviors, message and parameter interception, and other extensibility functionality.</span></span>  
  
 [<span data-ttu-id="ee845-110">Extension de liaisons</span><span class="sxs-lookup"><span data-stu-id="ee845-110">Extending Bindings</span></span>](../../../../docs/framework/wcf/extending/extending-bindings.md)  
 <span data-ttu-id="ee845-111">Les liaisons sont des objets qui décrivent les détails de communication requis pour se connecter à un point de terminaison.</span><span class="sxs-lookup"><span data-stu-id="ee845-111">Bindings are objects that describe the communication details required to connect to an endpoint.</span></span> <span data-ttu-id="ee845-112">Les extensions de liaison ou les liaisons personnalisées implémentent les fonctionnalités de communication personnalisées requises pour prendre en charge des fonctionnalités de l’application.</span><span class="sxs-lookup"><span data-stu-id="ee845-112">Binding extensions or custom bindings implement custom communication functionality required to support application features.</span></span>  
  
 [<span data-ttu-id="ee845-113">Extension de la couche du canal</span><span class="sxs-lookup"><span data-stu-id="ee845-113">Extending the Channel Layer</span></span>](../../../../docs/framework/wcf/extending/extending-the-channel-layer.md)  
 <span data-ttu-id="ee845-114">La couche du canal repose sous la couche du modèle de service et est chargée de l'échange des messages entre les clients et les services.</span><span class="sxs-lookup"><span data-stu-id="ee845-114">The channel layer sits beneath the service model layer and is responsible for the exchange of messages between clients and services.</span></span> <span data-ttu-id="ee845-115">Les extensions de canal peuvent implémenter des nouvelles fonctionnalités de protocole, telles que la sécurité.</span><span class="sxs-lookup"><span data-stu-id="ee845-115">Channel extensions can implement new protocol functionality, such as security.</span></span> <span data-ttu-id="ee845-116">Les extensions de canal contiennent aussi des fonctionnalités, telles que l’implémentation d’un nouveau transport réseau pour transporter les messages SOAP.</span><span class="sxs-lookup"><span data-stu-id="ee845-116">Channel extensions also transport functionality, such as implementing a new network transport to carry SOAP messages.</span></span>  
  
 [<span data-ttu-id="ee845-117">Extension de la sécurité</span><span class="sxs-lookup"><span data-stu-id="ee845-117">Extending Security</span></span>](../../../../docs/framework/wcf/extending/extending-security.md)  
 <span data-ttu-id="ee845-118">Sécurité dans WCF se compose de transfert de sécurité (intégrité, confidentialité et authentification), contrôle d’accès (autorisation) et l’audit.</span><span class="sxs-lookup"><span data-stu-id="ee845-118">Security in WCF consists of transfer security (integrity, confidentiality, and authentication), access control (authorization) and auditing.</span></span> <span data-ttu-id="ee845-119">Les classes se trouvent dans le `IdentityModel` espace de noms sont utilisés par WCF pour le contrôle d’accès.</span><span class="sxs-lookup"><span data-stu-id="ee845-119">The classes found in the `IdentityModel` namespace are used by WCF for access control.</span></span> <span data-ttu-id="ee845-120">La maîtrise du fonctionnement de l'architecture de sécurité vous permet de créer des types de revendication personnalisée afin d'accommoder des systèmes de contrôle d'accès personnalisés.</span><span class="sxs-lookup"><span data-stu-id="ee845-120">Understanding the security architecture allows you to create custom claim types to accommodate custom access control systems.</span></span>  
  
 [<span data-ttu-id="ee845-121">Extension du système de métadonnées</span><span class="sxs-lookup"><span data-stu-id="ee845-121">Extending the Metadata System</span></span>](../../../../docs/framework/wcf/extending/extending-the-metadata-system.md)  
 <span data-ttu-id="ee845-122">Le système de métadonnées WCF est un groupe de classes et interfaces qui représentent les métadonnées requises pour implémenter des applications basées sur le service.</span><span class="sxs-lookup"><span data-stu-id="ee845-122">The WCF metadata system is a group of classes and interfaces that represent metadata required to implement service-based applications.</span></span> <span data-ttu-id="ee845-123">Modifiez ou étendez les classes ou implémentez et configurez les interfaces pour exporter et importer des métadonnées personnalisées telles que les extensions WSDL (Web Services Description Language) ou des assertions WS-PolicyAttachments personnalisées.</span><span class="sxs-lookup"><span data-stu-id="ee845-123">Modify or extend the classes or implement and configure the interfaces to export and import custom metadata such as Web Services Description Language (WSDL) extensions or custom WS-PolicyAttachments assertions.</span></span>  
  
 [<span data-ttu-id="ee845-124">Extension des encodeurs et des sérialiseurs</span><span class="sxs-lookup"><span data-stu-id="ee845-124">Extending Encoders and Serializers</span></span>](../../../../docs/framework/wcf/extending/extending-encoders-and-serializers.md)  
 <span data-ttu-id="ee845-125">Les encodeurs et les sérialiseurs traduisent les données d'un format à l'autre.</span><span class="sxs-lookup"><span data-stu-id="ee845-125">Encoders and serializers translate data from one form to another.</span></span> <span data-ttu-id="ee845-126">Les rubriques de cette section expliquent comment étendre les classes fournies pour satisfaire des exigences particulières.</span><span class="sxs-lookup"><span data-stu-id="ee845-126">The topics in this section discuss how to extend the supplied classes to meet special requirements.</span></span>  
  
## <a name="reference"></a><span data-ttu-id="ee845-127">Référence</span><span class="sxs-lookup"><span data-stu-id="ee845-127">Reference</span></span>  
 <xref:System.ServiceModel>  
  
 <xref:System.ServiceModel.Channels>  
  
 <xref:System.ServiceModel.Description>  
  
 <xref:System.IdentityModel.Claims>  
  
 <xref:System.IdentityModel.Policy>  
  
 <xref:System.IdentityModel.Selectors>  
  
 <xref:System.IdentityModel.Tokens>  
  
## <a name="related-sections"></a><span data-ttu-id="ee845-128">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="ee845-128">Related Sections</span></span>  
 [<span data-ttu-id="ee845-129">Programmation WCF de base</span><span class="sxs-lookup"><span data-stu-id="ee845-129">Basic WCF Programming</span></span>](../../../../docs/framework/wcf/basic-wcf-programming.md)  
  
 [<span data-ttu-id="ee845-130">Informations détaillées sur les fonctionnalités de WCF</span><span class="sxs-lookup"><span data-stu-id="ee845-130">WCF Feature Details</span></span>](../../../../docs/framework/wcf/feature-details/index.md)  
  
 [<span data-ttu-id="ee845-131">Conseils et bonnes pratiques</span><span class="sxs-lookup"><span data-stu-id="ee845-131">Guidelines and Best Practices</span></span>](../../../../docs/framework/wcf/guidelines-and-best-practices.md)
