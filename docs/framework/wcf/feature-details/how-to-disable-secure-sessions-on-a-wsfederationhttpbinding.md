---
title: 'Procédure : désactiver des sessions sécurisées sur un WSFederationHttpBinding'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- WCF, federation
- federation
ms.assetid: 675fa143-6a4e-4be3-8afc-673334ab55ec
ms.openlocfilehash: 38863cbfe457afd923c3c8238d8c12b4d451c67f
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61773085"
---
# <a name="how-to-disable-secure-sessions-on-a-wsfederationhttpbinding"></a><span data-ttu-id="7d7f9-102">Procédure : désactiver des sessions sécurisées sur un WSFederationHttpBinding</span><span class="sxs-lookup"><span data-stu-id="7d7f9-102">How to: Disable Secure Sessions on a WSFederationHttpBinding</span></span>
<span data-ttu-id="7d7f9-103">Certains services peuvent requérir des informations d'identification fédérées mais ne prennent pas en charge les sessions sécurisées.</span><span class="sxs-lookup"><span data-stu-id="7d7f9-103">Some services may require federated credentials but not support secure sessions.</span></span> <span data-ttu-id="7d7f9-104">Dans ce cas, vous devez désactiver la fonctionnalité de session sécurisée.</span><span class="sxs-lookup"><span data-stu-id="7d7f9-104">In that case, you must disable the secure session feature.</span></span> <span data-ttu-id="7d7f9-105">Contrairement à <xref:System.ServiceModel.WSHttpBinding>, la classe <xref:System.ServiceModel.WSFederationHttpBinding> n'offre aucun moyen de désactiver les sessions sécurisées lors de la communication avec un service.</span><span class="sxs-lookup"><span data-stu-id="7d7f9-105">Unlike the <xref:System.ServiceModel.WSHttpBinding>, the <xref:System.ServiceModel.WSFederationHttpBinding> class does not provide a way to disable secure sessions when communicating with a service.</span></span> <span data-ttu-id="7d7f9-106">À la place, vous devez créer une liaison personnalisée qui remplace les paramètres de session sécurisée par un démarrage.</span><span class="sxs-lookup"><span data-stu-id="7d7f9-106">Instead, you must create a custom binding that replaces the secure session settings with a bootstrap.</span></span>  
  
 <span data-ttu-id="7d7f9-107">Cette rubrique montre comment modifier les éléments de liaison contenus dans une <xref:System.ServiceModel.WSFederationHttpBinding> pour créer une liaison personnalisée.</span><span class="sxs-lookup"><span data-stu-id="7d7f9-107">This topic demonstrates how to modify the binding elements contained within a <xref:System.ServiceModel.WSFederationHttpBinding> to create a custom binding.</span></span> <span data-ttu-id="7d7f9-108">Le résultat est identique à <xref:System.ServiceModel.WSFederationHttpBinding> mais n'utilise pas de sessions sécurisées.</span><span class="sxs-lookup"><span data-stu-id="7d7f9-108">The result is identical to the <xref:System.ServiceModel.WSFederationHttpBinding> except that it does not use secure sessions.</span></span>  
  
### <a name="to-create-a-custom-federated-binding-without-secure-session"></a><span data-ttu-id="7d7f9-109">Pour créer une liaison fédérée personnalisée sans session sécurisée</span><span class="sxs-lookup"><span data-stu-id="7d7f9-109">To create a custom federated binding without secure session</span></span>  
  
1. <span data-ttu-id="7d7f9-110">Créez une instance de la classe <xref:System.ServiceModel.WSFederationHttpBinding> soit impérativement dans du code, soit en la chargeant à partir du fichier de configuration.</span><span class="sxs-lookup"><span data-stu-id="7d7f9-110">Create an instance of the <xref:System.ServiceModel.WSFederationHttpBinding> class either imperatively in code or by loading one from the configuration file.</span></span>  
  
2. <span data-ttu-id="7d7f9-111">Clonez la <xref:System.ServiceModel.WSFederationHttpBinding> dans une <xref:System.ServiceModel.Channels.CustomBinding>.</span><span class="sxs-lookup"><span data-stu-id="7d7f9-111">Clone the <xref:System.ServiceModel.WSFederationHttpBinding> into a <xref:System.ServiceModel.Channels.CustomBinding>.</span></span>  
  
3. <span data-ttu-id="7d7f9-112">Recherchez <xref:System.ServiceModel.Channels.SecurityBindingElement> dans <xref:System.ServiceModel.Channels.CustomBinding>.</span><span class="sxs-lookup"><span data-stu-id="7d7f9-112">Find the <xref:System.ServiceModel.Channels.SecurityBindingElement> in the <xref:System.ServiceModel.Channels.CustomBinding>.</span></span>  
  
4. <span data-ttu-id="7d7f9-113">Recherchez <xref:System.ServiceModel.Security.Tokens.SecureConversationSecurityTokenParameters> dans <xref:System.ServiceModel.Channels.SecurityBindingElement>.</span><span class="sxs-lookup"><span data-stu-id="7d7f9-113">Find the <xref:System.ServiceModel.Security.Tokens.SecureConversationSecurityTokenParameters> in the <xref:System.ServiceModel.Channels.SecurityBindingElement>.</span></span>  
  
5. <span data-ttu-id="7d7f9-114">Remplacez le <xref:System.ServiceModel.Channels.SecurityBindingElement> d’origine par l’élément de liaison de sécurité de démarrage des <xref:System.ServiceModel.Security.Tokens.SecureConversationSecurityTokenParameters>.</span><span class="sxs-lookup"><span data-stu-id="7d7f9-114">Replace the original <xref:System.ServiceModel.Channels.SecurityBindingElement> with the bootstrap security binding element from the <xref:System.ServiceModel.Security.Tokens.SecureConversationSecurityTokenParameters>.</span></span>  
  
## <a name="example"></a><span data-ttu-id="7d7f9-115">Exemple</span><span class="sxs-lookup"><span data-stu-id="7d7f9-115">Example</span></span>  
 <span data-ttu-id="7d7f9-116">L'exemple suivant permet de créer une liaison fédérée personnalisée sans session sécurisée.</span><span class="sxs-lookup"><span data-stu-id="7d7f9-116">This following example creates a custom federated binding without secure session.</span></span>  
  
 [!code-csharp[c_CustomFederationBinding#0](../../../../samples/snippets/csharp/VS_Snippets_CFX/c_customfederationbinding/cs/c_customfederationbinding.cs#0)]
 [!code-vb[c_CustomFederationBinding#0](../../../../samples/snippets/visualbasic/VS_Snippets_CFX/c_customfederationbinding/vb/c_customfederationbinding.vb#0)]  
  
## <a name="compiling-the-code"></a><span data-ttu-id="7d7f9-117">Compilation du code</span><span class="sxs-lookup"><span data-stu-id="7d7f9-117">Compiling the Code</span></span>  
  
- <span data-ttu-id="7d7f9-118">Pour compiler l'exemple de code, créez un projet qui référence l'assembly System.ServiceModel.dll.</span><span class="sxs-lookup"><span data-stu-id="7d7f9-118">To compile the code example, create a project that references the System.ServiceModel.dll assembly.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="7d7f9-119">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="7d7f9-119">See also</span></span>

- [<span data-ttu-id="7d7f9-120">Liaisons et sécurité</span><span class="sxs-lookup"><span data-stu-id="7d7f9-120">Bindings and Security</span></span>](../../../../docs/framework/wcf/feature-details/bindings-and-security.md)
