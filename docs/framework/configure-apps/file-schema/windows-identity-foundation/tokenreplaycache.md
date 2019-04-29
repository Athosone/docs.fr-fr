---
title: <tokenReplayCache>
ms.date: 03/30/2017
ms.assetid: 1572ab23-6933-41b5-bfb4-0c4548145500
author: BrucePerlerMS
ms.openlocfilehash: 1567c669b5e682a7a771d7bedc95a8effa474e36
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61790505"
---
# <a name="tokenreplaycache"></a><span data-ttu-id="29c33-101">\<tokenReplayCache></span><span class="sxs-lookup"><span data-stu-id="29c33-101">\<tokenReplayCache></span></span>
<span data-ttu-id="29c33-102">Inscrit un cache de relecture de jetons avec un service ou une collection de gestionnaires de jetons de sécurité.</span><span class="sxs-lookup"><span data-stu-id="29c33-102">Registers a token replay cache with a service or a security token handler collection.</span></span>  
  
 <span data-ttu-id="29c33-103">\<system.identityModel></span><span class="sxs-lookup"><span data-stu-id="29c33-103">\<system.identityModel></span></span>  
<span data-ttu-id="29c33-104">\<identityConfiguration></span><span class="sxs-lookup"><span data-stu-id="29c33-104">\<identityConfiguration></span></span>  
<span data-ttu-id="29c33-105">\<caches></span><span class="sxs-lookup"><span data-stu-id="29c33-105">\<caches></span></span>  
<span data-ttu-id="29c33-106">\<tokenReplayCache></span><span class="sxs-lookup"><span data-stu-id="29c33-106">\<tokenReplayCache></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="29c33-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="29c33-107">Syntax</span></span>  
  
```xml  
<system.identityModel>  
  <identityConfiguration>  
    <caches>  
      <tokenReplayCache type=xs:string>  
      </tokenReplayCache>  
    </caches>  
  </identityConfiguration>  
</system.identityModel>  
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="29c33-108">Attributs et éléments</span><span class="sxs-lookup"><span data-stu-id="29c33-108">Attributes and Elements</span></span>  
 <span data-ttu-id="29c33-109">Les sections suivantes décrivent des attributs, des éléments enfants et des éléments parents.</span><span class="sxs-lookup"><span data-stu-id="29c33-109">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="29c33-110">Attributs</span><span class="sxs-lookup"><span data-stu-id="29c33-110">Attributes</span></span>  
  
|<span data-ttu-id="29c33-111">Attribut</span><span class="sxs-lookup"><span data-stu-id="29c33-111">Attribute</span></span>|<span data-ttu-id="29c33-112">Description</span><span class="sxs-lookup"><span data-stu-id="29c33-112">Description</span></span>|  
|---------------|-----------------|  
|<span data-ttu-id="29c33-113">type</span><span class="sxs-lookup"><span data-stu-id="29c33-113">type</span></span>|<span data-ttu-id="29c33-114">Un type qui dérive de la <xref:System.IdentityModel.Tokens.TokenReplayCache> classe.</span><span class="sxs-lookup"><span data-stu-id="29c33-114">A type that derives from the <xref:System.IdentityModel.Tokens.TokenReplayCache> class.</span></span> <span data-ttu-id="29c33-115">Pour plus d’informations sur la façon de spécifier une personnalisée `type`, consultez [références de Type personnalisé].</span><span class="sxs-lookup"><span data-stu-id="29c33-115">For more information about how to specify a custom `type`, see [Custom Type References].</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="29c33-116">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="29c33-116">Child Elements</span></span>  
 <span data-ttu-id="29c33-117">Aucun.</span><span class="sxs-lookup"><span data-stu-id="29c33-117">None</span></span>  
  
### <a name="parent-elements"></a><span data-ttu-id="29c33-118">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="29c33-118">Parent Elements</span></span>  
  
|<span data-ttu-id="29c33-119">Élément</span><span class="sxs-lookup"><span data-stu-id="29c33-119">Element</span></span>|<span data-ttu-id="29c33-120">Description</span><span class="sxs-lookup"><span data-stu-id="29c33-120">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="29c33-121">\<caches></span><span class="sxs-lookup"><span data-stu-id="29c33-121">\<caches></span></span>](../../../../../docs/framework/configure-apps/file-schema/windows-identity-foundation/caches.md)|<span data-ttu-id="29c33-122">Inscrit le met en cache utilisé par un service ou une collection de gestionnaires de jetons de sécurité.</span><span class="sxs-lookup"><span data-stu-id="29c33-122">Registers the caches used by a service or a security token handler collection.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="29c33-123">Notes</span><span class="sxs-lookup"><span data-stu-id="29c33-123">Remarks</span></span>  
 <span data-ttu-id="29c33-124">Le cache de relecture de jetons est utilisé pour détecter les jetons relus.</span><span class="sxs-lookup"><span data-stu-id="29c33-124">The token replay cache is used to detect replayed tokens.</span></span> <span data-ttu-id="29c33-125">Détection de relecture de jetons est activée par le [ \<tokenReplayDetection >](../../../../../docs/framework/configure-apps/file-schema/windows-identity-foundation/tokenreplaydetection.md) élément, qui spécifie également l’heure d’expiration maximal pour les jetons.</span><span class="sxs-lookup"><span data-stu-id="29c33-125">Token replay detection is enabled by the [\<tokenReplayDetection>](../../../../../docs/framework/configure-apps/file-schema/windows-identity-foundation/tokenreplaydetection.md) element, which also specifies the maximum expiration time for tokens.</span></span>  
  
## <a name="example"></a><span data-ttu-id="29c33-126">Exemple</span><span class="sxs-lookup"><span data-stu-id="29c33-126">Example</span></span>  
 <span data-ttu-id="29c33-127">Le code XML suivant illustre la configuration d’un cache personnalisé pour détecter les jetons relus.</span><span class="sxs-lookup"><span data-stu-id="29c33-127">The following XML shows the configuration of a custom cache for detecting replayed tokens.</span></span>  
  
```xml  
<caches>  
  <tokenReplayCache type="MyCacheLibrary.MyTokenReplayCache, MyCacheLibrary">  
  </tokenReplayCache>  
</caches>  
```  
  
## <a name="see-also"></a><span data-ttu-id="29c33-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="29c33-128">See also</span></span>

- <xref:System.IdentityModel.Tokens.TokenReplayCache>
- [<span data-ttu-id="29c33-129">\<tokenReplayDetection></span><span class="sxs-lookup"><span data-stu-id="29c33-129">\<tokenReplayDetection></span></span>](../../../../../docs/framework/configure-apps/file-schema/windows-identity-foundation/tokenreplaydetection.md)
