---
title: Autorisation dans WCF
ms.date: 03/30/2017
helpviewer_keywords:
- authorization [WCF]
- security [WCF], authorization
ms.assetid: 8ea0b552-af65-45b0-a157-c6c111b8ce5e
ms.openlocfilehash: 26aa445f3136fcb16e2eb9cdce6b245476297dfd
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59161359"
---
# <a name="authorization-in-wcf"></a><span data-ttu-id="b8363-102">Autorisation dans WCF</span><span class="sxs-lookup"><span data-stu-id="b8363-102">Authorization in WCF</span></span>
<span data-ttu-id="b8363-103">L'autorisation est le processus qui consiste à contrôler l'accès et les droits aux ressources, telles que les services ou fichiers.</span><span class="sxs-lookup"><span data-stu-id="b8363-103">Authorization is the process of controlling access and rights to resources, such as services or files.</span></span> <span data-ttu-id="b8363-104">Les rubriques de cette section vous montrent comment effectuer cette tâche de base dans Windows Communication Foundation (WCF) de plusieurs façons.</span><span class="sxs-lookup"><span data-stu-id="b8363-104">The topics in this section show you how to perform this basic task in Windows Communication Foundation (WCF) in a variety of ways.</span></span>  
  
## <a name="in-this-section"></a><span data-ttu-id="b8363-105">Dans cette section</span><span class="sxs-lookup"><span data-stu-id="b8363-105">In This Section</span></span>  
 [<span data-ttu-id="b8363-106">Mécanismes de contrôle d’accès</span><span class="sxs-lookup"><span data-stu-id="b8363-106">Access Control Mechanisms</span></span>](../../../../docs/framework/wcf/feature-details/access-control-mechanisms.md)  
 <span data-ttu-id="b8363-107">Fournit une brève description des mécanismes d’autorisation dans WCF et il utilise suggérée.</span><span class="sxs-lookup"><span data-stu-id="b8363-107">Provides a brief outline of the authorization mechanisms in WCF, and suggested uses.</span></span>  
  
 [<span data-ttu-id="b8363-108">Guide pratique pour Restreindre l’accès à la classe PrincipalPermissionAttribute</span><span class="sxs-lookup"><span data-stu-id="b8363-108">How to: Restrict Access with the PrincipalPermissionAttribute Class</span></span>](../../../../docs/framework/wcf/how-to-restrict-access-with-the-principalpermissionattribute-class.md)  
 <span data-ttu-id="b8363-109">Illustre le processus de limitation de l'accès à un service avec le <xref:System.Security.Permissions.PrincipalPermissionAttribute>.</span><span class="sxs-lookup"><span data-stu-id="b8363-109">Shows the process of restricting access to a service with the <xref:System.Security.Permissions.PrincipalPermissionAttribute>.</span></span>  
  
 [<span data-ttu-id="b8363-110">Guide pratique pour Utiliser le fournisseur de rôle ASP.NET avec un Service</span><span class="sxs-lookup"><span data-stu-id="b8363-110">How to: Use the ASP.NET Role Provider with a Service</span></span>](../../../../docs/framework/wcf/feature-details/how-to-use-the-aspnet-role-provider-with-a-service.md)  
 <span data-ttu-id="b8363-111">Décrit les différentes étapes de la configuration d'un service pour lui permettre d'utiliser la fonctionnalité de fournisseur de rôle de [!INCLUDE[vstecasp](../../../../includes/vstecasp-md.md)].</span><span class="sxs-lookup"><span data-stu-id="b8363-111">Walks through the configuration of a service to enable it to use the role provider feature of [!INCLUDE[vstecasp](../../../../includes/vstecasp-md.md)].</span></span>  
  
 [<span data-ttu-id="b8363-112">Guide pratique pour Utiliser le fournisseur de rôles du Gestionnaire d’autorisations ASP.NET avec un Service</span><span class="sxs-lookup"><span data-stu-id="b8363-112">How to: Use the ASP.NET Authorization Manager Role Provider with a Service</span></span>](../../../../docs/framework/wcf/feature-details/how-to-use-the-aspnet-authorization-manager-role-provider-with-a-service.md)  
 [!INCLUDE[vstecasp](../../../../includes/vstecasp-md.md)] <span data-ttu-id="b8363-113">peut utiliser le Gestionnaire d'autorisations pour gérer l'autorisation pour un site Web.</span><span class="sxs-lookup"><span data-stu-id="b8363-113">can use the Authorization Manager to manage authorization for a Web site.</span></span> <span data-ttu-id="b8363-114">WCF peut tirer parti de la même façon le [!INCLUDE[vstecasp](../../../../includes/vstecasp-md.md)]combinaison /Authorization Manager pour l’autorisation de clients.</span><span class="sxs-lookup"><span data-stu-id="b8363-114">WCF can similarly leverage the [!INCLUDE[vstecasp](../../../../includes/vstecasp-md.md)]/Authorization Manager combination for authorization of clients.</span></span>  
  
 [<span data-ttu-id="b8363-115">Gestion des revendications et autorisation avec le modèle d’identité</span><span class="sxs-lookup"><span data-stu-id="b8363-115">Managing Claims and Authorization with the Identity Model</span></span>](../../../../docs/framework/wcf/feature-details/managing-claims-and-authorization-with-the-identity-model.md)  
 <span data-ttu-id="b8363-116">Explique les principes de base de l'utilisation de l'infrastructure Modèle d'identité pour l'autorisation basée sur les revendications.</span><span class="sxs-lookup"><span data-stu-id="b8363-116">Explains the basics of using the Identity Model infrastructure for claims-based authorization.</span></span>  
  
 [<span data-ttu-id="b8363-117">Délégation et emprunt d’identité</span><span class="sxs-lookup"><span data-stu-id="b8363-117">Delegation and Impersonation</span></span>](../../../../docs/framework/wcf/feature-details/delegation-and-impersonation-with-wcf.md)  
 <span data-ttu-id="b8363-118">Explique la différence entre la délégation et l'emprunt d'identité.</span><span class="sxs-lookup"><span data-stu-id="b8363-118">Explains the difference between delegation and impersonation.</span></span>  
  
## <a name="reference"></a><span data-ttu-id="b8363-119">Référence</span><span class="sxs-lookup"><span data-stu-id="b8363-119">Reference</span></span>  
 <xref:System.ServiceModel.Security>  
  
 <xref:System.ServiceModel.Description.PrincipalPermissionMode>  
  
 <xref:System.ServiceModel.Description.ServiceAuthorizationBehavior>  
  
 <xref:System.Security.Permissions.PrincipalPermissionAttribute>  
  
## <a name="related-sections"></a><span data-ttu-id="b8363-120">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="b8363-120">Related Sections</span></span>  
 [<span data-ttu-id="b8363-121">Authentification</span><span class="sxs-lookup"><span data-stu-id="b8363-121">Authentication</span></span>](../../../../docs/framework/wcf/feature-details/authentication-in-wcf.md)  
  
## <a name="see-also"></a><span data-ttu-id="b8363-122">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b8363-122">See also</span></span>

- [<span data-ttu-id="b8363-123">Vue d’ensemble de la sécurité</span><span class="sxs-lookup"><span data-stu-id="b8363-123">Security Overview</span></span>](../../../../docs/framework/wcf/feature-details/security-overview.md)
- [<span data-ttu-id="b8363-124">Modèle de sécurité pour Windows Server AppFabric</span><span class="sxs-lookup"><span data-stu-id="b8363-124">Security Model for Windows Server App Fabric</span></span>](https://go.microsoft.com/fwlink/?LinkID=201279&clcid=0x409)
