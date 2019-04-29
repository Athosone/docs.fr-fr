---
title: <serviceCertificate>
ms.date: 03/30/2017
ms.assetid: 42c7f291-2ec3-43c5-8872-35897ff3c660
author: BrucePerlerMS
ms.openlocfilehash: 328d074f9edc5ddf871308a7e3d694bf94adea78
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61793820"
---
# <a name="servicecertificate"></a><span data-ttu-id="af22b-101">\<serviceCertificate></span><span class="sxs-lookup"><span data-stu-id="af22b-101">\<serviceCertificate></span></span>
<span data-ttu-id="af22b-102">Configure le certificat X.509 qui est utilisé pour chiffrer et déchiffrer les jetons.</span><span class="sxs-lookup"><span data-stu-id="af22b-102">Configures the X.509 certificate that is used to encrypt and decrypt tokens.</span></span>  
  
 <span data-ttu-id="af22b-103">\<system.identityModel.services></span><span class="sxs-lookup"><span data-stu-id="af22b-103">\<system.identityModel.services></span></span>  
<span data-ttu-id="af22b-104">\<federationConfiguration></span><span class="sxs-lookup"><span data-stu-id="af22b-104">\<federationConfiguration></span></span>  
<span data-ttu-id="af22b-105">\<serviceCertificate></span><span class="sxs-lookup"><span data-stu-id="af22b-105">\<serviceCertificate></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="af22b-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="af22b-106">Syntax</span></span>  
  
```xml  
<system.identityModel.services>  
  <federationConfiguration>  
    <serviceCertificate>  
    </serviceCertificate>  
  </federationConfiguration>  
</system.identityModel.services>  
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="af22b-107">Attributs et éléments</span><span class="sxs-lookup"><span data-stu-id="af22b-107">Attributes and Elements</span></span>  
 <span data-ttu-id="af22b-108">Les sections suivantes décrivent des attributs, des éléments enfants et des éléments parents.</span><span class="sxs-lookup"><span data-stu-id="af22b-108">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="af22b-109">Attributs</span><span class="sxs-lookup"><span data-stu-id="af22b-109">Attributes</span></span>  
 <span data-ttu-id="af22b-110">Aucun.</span><span class="sxs-lookup"><span data-stu-id="af22b-110">None</span></span>  
  
### <a name="child-elements"></a><span data-ttu-id="af22b-111">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="af22b-111">Child Elements</span></span>  
  
|<span data-ttu-id="af22b-112">Élément</span><span class="sxs-lookup"><span data-stu-id="af22b-112">Element</span></span>|<span data-ttu-id="af22b-113">Description</span><span class="sxs-lookup"><span data-stu-id="af22b-113">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="af22b-114">\<certificateReference></span><span class="sxs-lookup"><span data-stu-id="af22b-114">\<certificateReference></span></span>](../../../../../docs/framework/configure-apps/file-schema/windows-identity-foundation/certificatereference.md)|<span data-ttu-id="af22b-115">Spécifie les paramètres qui sont utilisés pour rechercher et valider le certificat X.509 dans un magasin de certificats.</span><span class="sxs-lookup"><span data-stu-id="af22b-115">Specifies settings that are used to find and validate an X.509 certificate in a certificate store.</span></span>|  
  
### <a name="parent-elements"></a><span data-ttu-id="af22b-116">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="af22b-116">Parent Elements</span></span>  
  
|<span data-ttu-id="af22b-117">Élément</span><span class="sxs-lookup"><span data-stu-id="af22b-117">Element</span></span>|<span data-ttu-id="af22b-118">Description</span><span class="sxs-lookup"><span data-stu-id="af22b-118">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="af22b-119">\<federationConfiguration></span><span class="sxs-lookup"><span data-stu-id="af22b-119">\<federationConfiguration></span></span>](../../../../../docs/framework/configure-apps/file-schema/windows-identity-foundation/federationconfiguration.md)|<span data-ttu-id="af22b-120">Contient les paramètres qui configurent le <xref:System.IdentityModel.Services.WSFederationAuthenticationModule> (WSFAM) et le <xref:System.IdentityModel.Services.SessionAuthenticationModule> (SAM).</span><span class="sxs-lookup"><span data-stu-id="af22b-120">Contains the settings that configure the <xref:System.IdentityModel.Services.WSFederationAuthenticationModule> (WSFAM) and the <xref:System.IdentityModel.Services.SessionAuthenticationModule> (SAM).</span></span>|  
  
## <a name="example"></a><span data-ttu-id="af22b-121">Exemple</span><span class="sxs-lookup"><span data-stu-id="af22b-121">Example</span></span>  
 <span data-ttu-id="af22b-122">Le code XML suivant illustre l’utilisation de la \<serviceCertificate > élément.</span><span class="sxs-lookup"><span data-stu-id="af22b-122">The following XML shows the use of the \<serviceCertificate> element.</span></span> <span data-ttu-id="af22b-123">Le code XML provient de la `CustomToken` exemple.</span><span class="sxs-lookup"><span data-stu-id="af22b-123">The XML is taken from the `CustomToken` sample.</span></span>  
  
```xml  
<serviceCertificate>  
  <certificateReference x509FindType="FindBySubjectName" findValue="localhost" storeLocation="LocalMachine" storeName="My"/>  
</serviceCertificate>  
```
