---
title: <system.identityModel.services>
ms.date: 03/30/2017
ms.assetid: fa1624dd-2d74-4ae3-942e-498cee261ac5
author: BrucePerlerMS
ms.openlocfilehash: 9728f3caee4dba367e4fc4a3e68213b1055cc3d1
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61793781"
---
# <a name="systemidentitymodelservices"></a><span data-ttu-id="179e5-102">\<system.identityModel.services></span><span class="sxs-lookup"><span data-stu-id="179e5-102">\<system.identityModel.services></span></span>
<span data-ttu-id="179e5-103">Section de configuration pour l’authentification à l’aide du protocole WS-Federation.</span><span class="sxs-lookup"><span data-stu-id="179e5-103">Configuration section for authentication using the WS-Federation protocol.</span></span>  
  
 <span data-ttu-id="179e5-104">\<system.identityModel.services></span><span class="sxs-lookup"><span data-stu-id="179e5-104">\<system.identityModel.services></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="179e5-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="179e5-105">Syntax</span></span>  
  
```xml  
<system.identityModel.services>  
  <federationConfiguration name=xs:string identityConfigurationName=xs:string>  
  </federationConfiguration>  
</system.identityModel.services>  
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="179e5-106">Attributs et éléments</span><span class="sxs-lookup"><span data-stu-id="179e5-106">Attributes and Elements</span></span>  
 <span data-ttu-id="179e5-107">Les sections suivantes décrivent des attributs, des éléments enfants et des éléments parents.</span><span class="sxs-lookup"><span data-stu-id="179e5-107">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="179e5-108">Attributs</span><span class="sxs-lookup"><span data-stu-id="179e5-108">Attributes</span></span>  
 <span data-ttu-id="179e5-109">Aucun.</span><span class="sxs-lookup"><span data-stu-id="179e5-109">None</span></span>  
  
### <a name="child-elements"></a><span data-ttu-id="179e5-110">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="179e5-110">Child Elements</span></span>  
  
|<span data-ttu-id="179e5-111">Élément</span><span class="sxs-lookup"><span data-stu-id="179e5-111">Element</span></span>|<span data-ttu-id="179e5-112">Description</span><span class="sxs-lookup"><span data-stu-id="179e5-112">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="179e5-113">\<federationConfiguration></span><span class="sxs-lookup"><span data-stu-id="179e5-113">\<federationConfiguration></span></span>](../../../../../docs/framework/configure-apps/file-schema/windows-identity-foundation/federationconfiguration.md)|<span data-ttu-id="179e5-114">Contient les paramètres qui configurent le <xref:System.IdentityModel.Services.WSFederationAuthenticationModule> (WSFAM) et le <xref:System.IdentityModel.Services.SessionAuthenticationModule> modules (SAM) HTTP.</span><span class="sxs-lookup"><span data-stu-id="179e5-114">Contains the settings that configure the <xref:System.IdentityModel.Services.WSFederationAuthenticationModule> (WSFAM) and the <xref:System.IdentityModel.Services.SessionAuthenticationModule> (SAM) HTTP modules.</span></span>|  
  
### <a name="parent-elements"></a><span data-ttu-id="179e5-115">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="179e5-115">Parent Elements</span></span>  
 <span data-ttu-id="179e5-116">Aucun.</span><span class="sxs-lookup"><span data-stu-id="179e5-116">None</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="179e5-117">Notes</span><span class="sxs-lookup"><span data-stu-id="179e5-117">Remarks</span></span>  
 <span data-ttu-id="179e5-118">Ajouter un `<system.identityModel.services>` section au fichier de configuration de votre application pour fournir des paramètres pour le SAM et le WSFAM.</span><span class="sxs-lookup"><span data-stu-id="179e5-118">Add a `<system.identityModel.services>` section to your application’s configuration file to provide settings for the SAM and WSFAM.</span></span>  
  
> [!IMPORTANT]
>  <span data-ttu-id="179e5-119">Lorsque vous utilisez le <xref:System.IdentityModel.Services.ClaimsPrincipalPermission> ou le <xref:System.IdentityModel.Services.ClaimsPrincipalPermissionAttribute> classe pour fournir un contrôle d’accès basé sur les revendications dans votre code, le Gestionnaire d’autorisation des revendications (<xref:System.Security.Claims.ClaimsAuthorizationManager>) et de la stratégie qui est utilisée pour prendre des décisions d’autorisation sont configurés via un `<identityConfiguration>` élément qui est implicitement ou explicitement référencé à partir d’un `<federationConfiguration>` élément dans cette section.</span><span class="sxs-lookup"><span data-stu-id="179e5-119">When using the <xref:System.IdentityModel.Services.ClaimsPrincipalPermission> or the <xref:System.IdentityModel.Services.ClaimsPrincipalPermissionAttribute> class to provide claims-based access control in your code, the claims authorization manager (<xref:System.Security.Claims.ClaimsAuthorizationManager>) and policy that is used to make authorization decisions are configured through an `<identityConfiguration>` element that is implicitly or explicitly referenced from a `<federationConfiguration>` element in this section.</span></span> <span data-ttu-id="179e5-120">Pour plus d’informations, consultez le **remarques** sous le [ \<federationConfiguration >](../../../../../docs/framework/configure-apps/file-schema/windows-identity-foundation/federationconfiguration.md) élément.</span><span class="sxs-lookup"><span data-stu-id="179e5-120">For more information, see the **Remarks** under the [\<federationConfiguration>](../../../../../docs/framework/configure-apps/file-schema/windows-identity-foundation/federationconfiguration.md) element.</span></span>  
  
 <span data-ttu-id="179e5-121">Le `<system.identityModel.services>` section est représentée par la <xref:System.IdentityModel.Services.Configuration.SystemIdentityModelServicesSection> classe.</span><span class="sxs-lookup"><span data-stu-id="179e5-121">The `<system.identityModel.services>` section is represented by the <xref:System.IdentityModel.Services.Configuration.SystemIdentityModelServicesSection> class.</span></span> <span data-ttu-id="179e5-122">La collection d’enfants `<federationConfiguration>` configurés dans la section des éléments est représenté par la <xref:System.IdentityModel.Services.Configuration.FederationConfigurationElementCollection> classe.</span><span class="sxs-lookup"><span data-stu-id="179e5-122">The collection of child `<federationConfiguration>` elements configured in the section is represented by the <xref:System.IdentityModel.Services.Configuration.FederationConfigurationElementCollection> class.</span></span>  
  
## <a name="example"></a><span data-ttu-id="179e5-123">Exemple</span><span class="sxs-lookup"><span data-stu-id="179e5-123">Example</span></span>  
 <span data-ttu-id="179e5-124">Le code XML suivant montre comment ajouter un `<system.identityModel.services>` section dans un fichier de configuration.</span><span class="sxs-lookup"><span data-stu-id="179e5-124">The following XML shows how to add a `<system.identityModel.services>` section to a configuration file.</span></span> <span data-ttu-id="179e5-125">Vous devez d’abord ajouter les déclarations de section à la fois pour le `<system.identityModel.services>` section et le `<system.identityModel>` sections.</span><span class="sxs-lookup"><span data-stu-id="179e5-125">You must first add section declarations for both the `<system.identityModel.services>` section and the `<system.identityModel>` sections.</span></span> <span data-ttu-id="179e5-126">(Lorsque vous ajoutez un `<system.identityModel.services>` section, vous devez également ajouter une déclaration pour le `<system.identityModel>` section pour vous assurer que la valeur par défaut `<identityConfiguration>` section peut être créée par le runtime si nécessaire.) Après ont ajouté les déclarations de section, vous pouvez configurer les paramètres de l’authentification fédérée sous le `<system.identityModel.services>` élément.</span><span class="sxs-lookup"><span data-stu-id="179e5-126">(When you add a `<system.identityModel.services>` section, you should also add a declaration for the `<system.identityModel>` section to ensure that a default `<identityConfiguration>` section can be created by the runtime if necessary.) After the section declarations have been added, you can configure federated authentication settings under the `<system.identityModel.services>` element.</span></span>  
  
```xml  
<configuration>  
  <configSections>  
    <section name="system.identityModel" type="System.IdentityModel.Configuration.SystemIdentityModelSection, System.IdentityModel, Version=4.0.0.0, Culture=neutral, PublicKeyToken=B77A5C561934E089" />  
    <section name="system.identityModel.services" type="System.IdentityModel.Services.Configuration.SystemIdentityModelServicesSection, System.IdentityModel.Services, Version=4.0.0.0, Culture=neutral, PublicKeyToken=B77A5C561934E089" />  
  </configSections>  
  
  <!-- Additional elements (not shown) -->  
  
  <system.identityModel.services>  
    <federationConfiguration>  
      <wsFederation passiveRedirectEnabled="true"   
        issuer="http://localhost:15839/wsFederationSTS/Issue"   
        realm="http://localhost:50969/" reply="http://localhost:50969/"   
        requireHttps="false"   
        signOutReply="http://localhost:50969/SignedOutPage.html"   
        signOutQueryString="Param1=value2&Param2=value2"   
        persistentCookiesOnPassiveRedirects="true" />  
      <cookieHandler requireSsl="false" />  
    </federationConfiguration>  
  </system.identityModel.services>  
  
</configuration>  
```
