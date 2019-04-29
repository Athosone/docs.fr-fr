---
title: 'Procédure : créer une session sécurisée'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- security [WCF], creating a session
ms.assetid: b6f42b5a-bbf7-45cf-b917-7ec9fa7ae110
ms.openlocfilehash: 4464100012fe9b3e1f0e8743707b1dc9a477c3d9
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61787866"
---
# <a name="how-to-create-a-secure-session"></a><span data-ttu-id="05dcc-102">Procédure : créer une session sécurisée</span><span class="sxs-lookup"><span data-stu-id="05dcc-102">How to: Create a Secure Session</span></span>
<span data-ttu-id="05dcc-103">À l’exception de la [ \<basicHttpBinding >](../../../../docs/framework/configure-apps/file-schema/wcf/basichttpbinding.md) de liaison, les liaisons fournies par le système dans Windows Communication Foundation (WCF) utilisent automatiquement des sessions sécurisées lorsque la sécurité de message est activée.</span><span class="sxs-lookup"><span data-stu-id="05dcc-103">With the exception of the [\<basicHttpBinding>](../../../../docs/framework/configure-apps/file-schema/wcf/basichttpbinding.md) binding, the system-provided bindings in Windows Communication Foundation (WCF) automatically use secure sessions when message security is enabled.</span></span>  
  
 <span data-ttu-id="05dcc-104">Par défaut, les sessions sécurisées ne survivent pas à un serveur web recyclé.</span><span class="sxs-lookup"><span data-stu-id="05dcc-104">By default, secure sessions do not survive a Web server that is recycled.</span></span> <span data-ttu-id="05dcc-105">Lorsqu'une session sécurisée est établie, le client et le service mettent en cache la clé associée à la session sécurisée.</span><span class="sxs-lookup"><span data-stu-id="05dcc-105">When a secure session is established, the client and the service cache the key that is associated with the secure session.</span></span> <span data-ttu-id="05dcc-106">Lorsque les messages sont échangés, seul un identificateur de la clé mise en cache est échangé.</span><span class="sxs-lookup"><span data-stu-id="05dcc-106">As the messages are exchanged, only an identifier to the cached key is exchanged.</span></span> <span data-ttu-id="05dcc-107">Si le serveur web est recyclé, le cache est également recyclé, de sorte que le serveur web ne peut pas récupérer la clé mise en cache pour l’identificateur.</span><span class="sxs-lookup"><span data-stu-id="05dcc-107">If the Web server is recycled, the cache is also recycled, such that the Web server cannot retrieve the cached key for the identifier.</span></span> <span data-ttu-id="05dcc-108">Si cela arrive, une exception est retournée au client.</span><span class="sxs-lookup"><span data-stu-id="05dcc-108">If this happens, an exception is thrown back to the client.</span></span> <span data-ttu-id="05dcc-109">Les sessions sécurisées qui utilisent un jeton de contexte de sécurité avec état peuvent survivre au recyclage d'un serveur Web.</span><span class="sxs-lookup"><span data-stu-id="05dcc-109">Secure sessions that use a stateful security context token (SCT) can survive a Web server being recycled.</span></span> <span data-ttu-id="05dcc-110">Pour plus d’informations sur l’utilisation de SCT avec état dans une session sécurisée, consultez [Comment : Créer un contexte de sécurité jeton pour une Session sécurisée](../../../../docs/framework/wcf/feature-details/how-to-create-a-security-context-token-for-a-secure-session.md).</span><span class="sxs-lookup"><span data-stu-id="05dcc-110">For more information about using a stateful SCT in a secure session, see [How to: Create a Security Context Token for a Secure Session](../../../../docs/framework/wcf/feature-details/how-to-create-a-security-context-token-for-a-secure-session.md).</span></span>  
  
### <a name="to-specify-that-a-service-uses-secure-sessions-by-using-one-of-the-system-provided-bindings"></a><span data-ttu-id="05dcc-111">Pour spécifier qu’un service utilise des sessions sécurisées à l’aide de l’une des liaisons fournies par le système</span><span class="sxs-lookup"><span data-stu-id="05dcc-111">To specify that a service uses secure sessions by using one of the system-provided bindings</span></span>  
  
- <span data-ttu-id="05dcc-112">Configurez un service pour utiliser une liaison fournie par le système qui prend en charge la sécurité de message.</span><span class="sxs-lookup"><span data-stu-id="05dcc-112">Configure a service to use a system-provided binding that supports message security.</span></span>  
  
     <span data-ttu-id="05dcc-113">À l’exception de la [ \<basicHttpBinding >](../../../../docs/framework/configure-apps/file-schema/wcf/basichttpbinding.md) liaison, lorsque les liaisons fournies par le système sont configurés pour utiliser la sécurité de message, WCF automatiquement utilise des sessions sécurisées.</span><span class="sxs-lookup"><span data-stu-id="05dcc-113">With the exception of the [\<basicHttpBinding>](../../../../docs/framework/configure-apps/file-schema/wcf/basichttpbinding.md) binding, when the system-provided bindings are configured to use message security, WCF automatically uses secure sessions.</span></span> <span data-ttu-id="05dcc-114">Le tableau suivant répertorie les liaisons fournies par le système qui prennent en charge la sécurité de message et indique si la sécurité de message est le mécanisme de sécurité par défaut.</span><span class="sxs-lookup"><span data-stu-id="05dcc-114">The following table lists the system-provided bindings that support message security and whether message security is the default security mechanism.</span></span>  
  
    |<span data-ttu-id="05dcc-115">Liaison fournie par le système</span><span class="sxs-lookup"><span data-stu-id="05dcc-115">System-provided binding</span></span>|<span data-ttu-id="05dcc-116">Élément de configuration</span><span class="sxs-lookup"><span data-stu-id="05dcc-116">Configuration element</span></span>|<span data-ttu-id="05dcc-117">Sécurité de message activée par défaut</span><span class="sxs-lookup"><span data-stu-id="05dcc-117">Message security on by default</span></span>|  
    |------------------------------|---------------------------|------------------------------------|  
    |<xref:System.ServiceModel.BasicHttpBinding>|[<span data-ttu-id="05dcc-118">\<basicHttpBinding></span><span class="sxs-lookup"><span data-stu-id="05dcc-118">\<basicHttpBinding></span></span>](../../../../docs/framework/configure-apps/file-schema/wcf/basichttpbinding.md)|<span data-ttu-id="05dcc-119">Non</span><span class="sxs-lookup"><span data-stu-id="05dcc-119">No</span></span>|  
    |<xref:System.ServiceModel.WSHttpBinding>|[<span data-ttu-id="05dcc-120">\<wsHttpBinding></span><span class="sxs-lookup"><span data-stu-id="05dcc-120">\<wsHttpBinding></span></span>](../../../../docs/framework/configure-apps/file-schema/wcf/wshttpbinding.md)|<span data-ttu-id="05dcc-121">Oui</span><span class="sxs-lookup"><span data-stu-id="05dcc-121">Yes</span></span>|  
    |<xref:System.ServiceModel.WSDualHttpBinding>|[<span data-ttu-id="05dcc-122">\<wsDualHttpBinding></span><span class="sxs-lookup"><span data-stu-id="05dcc-122">\<wsDualHttpBinding></span></span>](../../../../docs/framework/configure-apps/file-schema/wcf/wsdualhttpbinding.md)|<span data-ttu-id="05dcc-123">Oui</span><span class="sxs-lookup"><span data-stu-id="05dcc-123">Yes</span></span>|  
    |<xref:System.ServiceModel.WSFederationHttpBinding>|[<span data-ttu-id="05dcc-124">\<wsFederationHttpBinding></span><span class="sxs-lookup"><span data-stu-id="05dcc-124">\<wsFederationHttpBinding></span></span>](../../../../docs/framework/configure-apps/file-schema/wcf/wsfederationhttpbinding.md)|<span data-ttu-id="05dcc-125">Oui</span><span class="sxs-lookup"><span data-stu-id="05dcc-125">Yes</span></span>|  
    |<xref:System.ServiceModel.NetTcpBinding>|[<span data-ttu-id="05dcc-126">\<netTcpBinding></span><span class="sxs-lookup"><span data-stu-id="05dcc-126">\<netTcpBinding></span></span>](../../../../docs/framework/configure-apps/file-schema/wcf/nettcpbinding.md)|<span data-ttu-id="05dcc-127">Non</span><span class="sxs-lookup"><span data-stu-id="05dcc-127">No</span></span>|  
    |<xref:System.ServiceModel.NetMsmqBinding>|[<span data-ttu-id="05dcc-128">\<netMsmqBinding></span><span class="sxs-lookup"><span data-stu-id="05dcc-128">\<netMsmqBinding></span></span>](../../../../docs/framework/configure-apps/file-schema/wcf/netmsmqbinding.md)|<span data-ttu-id="05dcc-129">Non</span><span class="sxs-lookup"><span data-stu-id="05dcc-129">No</span></span>|  
  
     <span data-ttu-id="05dcc-130">L’exemple de code suivant utilise la configuration pour spécifier une liaison nommée `wsHttpBinding_Calculator` qui utilise le [ \<wsHttpBinding >](../../../../docs/framework/configure-apps/file-schema/wcf/wshttpbinding.md), la sécurité de message et sécuriser des sessions.</span><span class="sxs-lookup"><span data-stu-id="05dcc-130">The following code example uses configuration to specify a binding named `wsHttpBinding_Calculator` that uses the [\<wsHttpBinding>](../../../../docs/framework/configure-apps/file-schema/wcf/wshttpbinding.md), message security, and secure sessions.</span></span>  
  
    ```xml  
    <bindings>  
      <WSHttpBinding>  
       <binding name = "wsHttpBinding_Calculator">  
         <security mode="Message">  
           <message clientCredentialType="Windows"/>  
         </security>  
        </binding>  
      </WSHttpBinding>  
    </bindings>  
    ```  
  
     <span data-ttu-id="05dcc-131">L’exemple de code suivant spécifie que le [ \<wsHttpBinding >](../../../../docs/framework/configure-apps/file-schema/wcf/wshttpbinding.md), la sécurité de message et sécuriser les sessions sont utilisées pour sécuriser la `secureCalculator` service.</span><span class="sxs-lookup"><span data-stu-id="05dcc-131">The following code example specifies that the [\<wsHttpBinding>](../../../../docs/framework/configure-apps/file-schema/wcf/wshttpbinding.md), message security, and secure sessions are used to secure the `secureCalculator` service.</span></span>  
  
     [!code-csharp[c_CreateSecureSession#1](../../../../samples/snippets/csharp/VS_Snippets_CFX/c_createsecuresession/cs/secureservice.cs#1)]
     [!code-vb[c_CreateSecureSession#1](../../../../samples/snippets/visualbasic/VS_Snippets_CFX/c_createsecuresession/vb/secureservice.vb#1)]  
  
    > [!NOTE]
    >  <span data-ttu-id="05dcc-132">Sessions sécurisées peuvent être désactivées pour le [ \<wsHttpBinding >](../../../../docs/framework/configure-apps/file-schema/wcf/wshttpbinding.md) en définissant le `establishSecurityContext` attribut `false`.</span><span class="sxs-lookup"><span data-stu-id="05dcc-132">Secure sessions can be turned off for the [\<wsHttpBinding>](../../../../docs/framework/configure-apps/file-schema/wcf/wshttpbinding.md) by setting the `establishSecurityContext` attribute to `false`.</span></span> <span data-ttu-id="05dcc-133">Pour les autres liaisons fournies par le système, les sessions sécurisées peuvent être désactivées uniquement en créant une liaison personnalisée.</span><span class="sxs-lookup"><span data-stu-id="05dcc-133">For the other system-provided bindings, secure sessions can only be turned off by creating a custom binding.</span></span>  
  
### <a name="to-specify-that-a-service-uses-secure-sessions-by-using-a-custom-binding"></a><span data-ttu-id="05dcc-134">Pour spécifier qu'un service utilise des sessions sécurisées à l'aide d'une liaison personnalisée</span><span class="sxs-lookup"><span data-stu-id="05dcc-134">To specify that a service uses secure sessions by using a custom binding</span></span>  
  
- <span data-ttu-id="05dcc-135">Créez une liaison personnalisée qui spécifie que les messages SOAP sont protégés par une session sécurisée.</span><span class="sxs-lookup"><span data-stu-id="05dcc-135">Create a custom binding that specifies that SOAP messages are protected by a secure session.</span></span>  
  
     <span data-ttu-id="05dcc-136">Pour plus d’informations sur la création d’une liaison personnalisée, consultez [Comment : Personnaliser une liaison fournie par le système](../../../../docs/framework/wcf/extending/how-to-customize-a-system-provided-binding.md).</span><span class="sxs-lookup"><span data-stu-id="05dcc-136">For more information about creating a custom binding, see [How to: Customize a System-Provided Binding](../../../../docs/framework/wcf/extending/how-to-customize-a-system-provided-binding.md).</span></span>  
  
     <span data-ttu-id="05dcc-137">L’exemple de code suivant utilise la configuration pour spécifier une liaison personnalisée à laquelle les messages font appel dans une session sécurisée.</span><span class="sxs-lookup"><span data-stu-id="05dcc-137">The following code example uses configuration to specify a custom binding that messages using a secure session.</span></span>  
  
    ```xml  
    <bindings>  
      <!-- configure a custom binding -->  
      <customBinding>  
        <binding name="customBinding_Calculator">  
          <security authenticationMode="SecureConversation" />  
          <secureConversationBootstrap authenticationMode="SspiNegotiated" />  
          <textMessageEncoding messageVersion="Soap12WSAddressing10" writeEncoding="utf-8"/>  
          <httpTransport/>  
        </binding>  
      </customBinding>  
    </bindings>  
    ```  
  
     <span data-ttu-id="05dcc-138">L’exemple de code suivant crée une liaison personnalisée qui utilise le mode d’authentification <xref:System.ServiceModel.Configuration.AuthenticationMode.MutualCertificate> pour démarrer une session sécurisée.</span><span class="sxs-lookup"><span data-stu-id="05dcc-138">The following code example creates a custom binding that uses the <xref:System.ServiceModel.Configuration.AuthenticationMode.MutualCertificate> authentication mode to bootstrap a secure session.</span></span>  
  
     [!code-csharp[c_CreateSecureSession#2](../../../../samples/snippets/csharp/VS_Snippets_CFX/c_createsecuresession/cs/secureservice.cs#2)]
     [!code-vb[c_CreateSecureSession#2](../../../../samples/snippets/visualbasic/VS_Snippets_CFX/c_createsecuresession/vb/secureservice.vb#2)]  
  
## <a name="see-also"></a><span data-ttu-id="05dcc-139">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="05dcc-139">See also</span></span>

- [<span data-ttu-id="05dcc-140">Vue d’ensemble des liaisons WCF</span><span class="sxs-lookup"><span data-stu-id="05dcc-140">WCF Bindings Overview</span></span>](../../../../docs/framework/wcf/bindings-overview.md)
