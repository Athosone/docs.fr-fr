---
title: Sessions fiables
ms.date: 03/30/2017
f1_keywords:
- Windows Communication Foundation, sessions and instances
- WCF, sessions and instances
- sessions and instances [WCF]
helpviewer_keywords:
- instances [WCF]
- sessions [WCF]
ms.assetid: 143951b3-3aa0-4540-b4b7-d33e77e874a1
ms.openlocfilehash: 9a2cd06c4c5a73d9fb5c4c7f09632e10c3eb0d87
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61991157"
---
# <a name="reliable-sessions"></a><span data-ttu-id="dc269-102">Sessions fiables</span><span class="sxs-lookup"><span data-stu-id="dc269-102">Reliable Sessions</span></span>

<span data-ttu-id="dc269-103">Cette section décrit quelles un Windows Communication Foundation (WCF) est de la session fiable, à quoi il sert, comment et quand utiliser, quelles configurations de liaison prennent en charge et des pointeurs sur les meilleures pratiques.</span><span class="sxs-lookup"><span data-stu-id="dc269-103">This section describes what a Windows Communication Foundation (WCF) reliable session is, what it's used for, how and when to use one, what binding configurations support it, and pointers on best practices.</span></span> <span data-ttu-id="dc269-104">Le tableau suivant résume les détails sur les points essentiels et les rubriques connexes de cette section.</span><span class="sxs-lookup"><span data-stu-id="dc269-104">The following table summarizes details about the essential points and related topics in this section.</span></span>

<span data-ttu-id="dc269-105">La session fiable WCF fournit des fonctionnalités en vous assurant que les messages envoyés entre les points de terminaison sont transférés via des intermédiaires SOAP ou de transport et sont remis une seule fois et, éventuellement, dans le même ordre que celui dans lequel ils ont été envoyés.</span><span class="sxs-lookup"><span data-stu-id="dc269-105">The reliable session WCF provides features ensuring that messages sent between endpoints are transferred across SOAP or transport intermediaries and are delivered only once and, optionally, in the same order in which they were sent.</span></span>

<span data-ttu-id="dc269-106">Pour utiliser une session fiable avec une application WCF, utilisez une des liaisons fournies par le système dans WCF qui prennent en charge une session fiable par défaut ou en tant qu’option ou créer votre propre liaison personnalisée qui prend en charge de la session.</span><span class="sxs-lookup"><span data-stu-id="dc269-106">To use a reliable session with a WCF application, either use one of the system-provided bindings in WCF that support a reliable session by default or as an option, or create your own custom binding that supports the session.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="dc269-107">Dans cette section</span><span class="sxs-lookup"><span data-stu-id="dc269-107">In This Section</span></span>

<span data-ttu-id="dc269-108">[Vue d’ensemble des Sessions fiables](../../../../docs/framework/wcf/feature-details/reliable-sessions-overview.md) décrit des sessions fiables, quand les utiliser, les différentes liaisons qui prennent en charge des sessions fiables, et leur fonctionnement.</span><span class="sxs-lookup"><span data-stu-id="dc269-108">[Reliable Sessions Overview](../../../../docs/framework/wcf/feature-details/reliable-sessions-overview.md) Describes reliable sessions, when to use them, the different bindings that support reliable sessions, and how they work.</span></span>

<span data-ttu-id="dc269-109">[Guide pratique pour Exchange Messages au sein d’une Session fiable](../../../../docs/framework/wcf/feature-details/how-to-exchange-messages-within-a-reliable-session.md) décrit comment créer une session fiable sur HTTP à l’aide d’une liaison personnalisée spécifiée dans la configuration.</span><span class="sxs-lookup"><span data-stu-id="dc269-109">[How to: Exchange Messages Within a Reliable Session](../../../../docs/framework/wcf/feature-details/how-to-exchange-messages-within-a-reliable-session.md) Describes how to create a reliable session over HTTP using a custom binding specified in the configuration.</span></span>

<span data-ttu-id="dc269-110">[Guide pratique pour Sécuriser des Messages au sein de Sessions fiables](../../../../docs/framework/wcf/feature-details/how-to-secure-messages-within-reliable-sessions.md) explique comment sécuriser une session fiable.</span><span class="sxs-lookup"><span data-stu-id="dc269-110">[How to: Secure Messages within Reliable Sessions](../../../../docs/framework/wcf/feature-details/how-to-secure-messages-within-reliable-sessions.md) Describes how to secure a reliable session.</span></span>

<span data-ttu-id="dc269-111">[Guide pratique pour Créer une liaison Session fiable personnalisée avec le protocole HTTPS](../../../../docs/framework/wcf/feature-details/how-to-create-a-custom-reliable-session-binding-with-https.md) décrit comment créer une session fiable sur HTTPS.</span><span class="sxs-lookup"><span data-stu-id="dc269-111">[How to: Create a Custom Reliable Session Binding with HTTPS](../../../../docs/framework/wcf/feature-details/how-to-create-a-custom-reliable-session-binding-with-https.md) Describes how to create a reliable session over HTTPS.</span></span>

<span data-ttu-id="dc269-112">[Meilleures pratiques pour les Sessions fiables](../../../../docs/framework/wcf/feature-details/best-practices-for-reliable-sessions.md) décrit quelques-unes des meilleures pratiques associées à l’aide d’une session fiable.</span><span class="sxs-lookup"><span data-stu-id="dc269-112">[Best Practices for Reliable Sessions](../../../../docs/framework/wcf/feature-details/best-practices-for-reliable-sessions.md) Describes some of the best practices associated with using a reliable session.</span></span>

## <a name="reference"></a><span data-ttu-id="dc269-113">Référence</span><span class="sxs-lookup"><span data-stu-id="dc269-113">Reference</span></span>

<xref:System.ServiceModel.ReliableSession>

## <a name="see-also"></a><span data-ttu-id="dc269-114">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="dc269-114">See also</span></span>

- [<span data-ttu-id="dc269-115">Files d’attente et sessions fiables</span><span class="sxs-lookup"><span data-stu-id="dc269-115">Queues and Reliable Sessions</span></span>](../../../../docs/framework/wcf/feature-details/queues-and-reliable-sessions.md)
- [<span data-ttu-id="dc269-116">Sessions, instanciation et accès concurrentiel</span><span class="sxs-lookup"><span data-stu-id="dc269-116">Sessions, Instancing, and Concurrency</span></span>](../../../../docs/framework/wcf/feature-details/sessions-instancing-and-concurrency.md)
