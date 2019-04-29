---
title: <customCookieHandler>
ms.date: 03/30/2017
ms.assetid: a03b153d-5ec6-4915-9031-6f0c3fd348be
author: BrucePerlerMS
ms.openlocfilehash: 0129c63fe17b63889a77ea1a56c0d7e657def859
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61791727"
---
# <a name="customcookiehandler"></a><span data-ttu-id="0a0ec-101">\<customCookieHandler></span><span class="sxs-lookup"><span data-stu-id="0a0ec-101">\<customCookieHandler></span></span>
<span data-ttu-id="0a0ec-102">Définit le type de gestionnaire de cookie personnalisé.</span><span class="sxs-lookup"><span data-stu-id="0a0ec-102">Sets the custom cookie handler type.</span></span> <span data-ttu-id="0a0ec-103">Cet élément peut uniquement être présent si la `mode` attribut de la `<cookieHandler>` élément est « Custom ».</span><span class="sxs-lookup"><span data-stu-id="0a0ec-103">This element may only be present if the `mode` attribute of the `<cookieHandler>` element is "Custom".</span></span> <span data-ttu-id="0a0ec-104">Le type personnalisé doit être dérivé du <xref:System.IdentityModel.Services.CookieHandler> classe.</span><span class="sxs-lookup"><span data-stu-id="0a0ec-104">The custom type must be derived from the <xref:System.IdentityModel.Services.CookieHandler> class.</span></span>  
  
 <span data-ttu-id="0a0ec-105">\<system.identityModel.services></span><span class="sxs-lookup"><span data-stu-id="0a0ec-105">\<system.identityModel.services></span></span>  
<span data-ttu-id="0a0ec-106">\<federationConfiguration></span><span class="sxs-lookup"><span data-stu-id="0a0ec-106">\<federationConfiguration></span></span>  
<span data-ttu-id="0a0ec-107">\<cookieHandler></span><span class="sxs-lookup"><span data-stu-id="0a0ec-107">\<cookieHandler></span></span>  
<span data-ttu-id="0a0ec-108">\<customCookieHandler></span><span class="sxs-lookup"><span data-stu-id="0a0ec-108">\<customCookieHandler></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="0a0ec-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="0a0ec-109">Syntax</span></span>  
  
```xml  
<system.identityModel.services>  
  <federationConfiguration>  
    <cookieHandler mode="Custom">  
      <customCookieHandler type="MyNamespace.MyCustomCookieHandler, MyAssembly" >  
      </customCookieHandler>  
    </cookieHandler>  
  </federationConfiguration>  
</system.identityModel.services>  
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="0a0ec-110">Attributs et éléments</span><span class="sxs-lookup"><span data-stu-id="0a0ec-110">Attributes and Elements</span></span>  
 <span data-ttu-id="0a0ec-111">Les sections suivantes décrivent des attributs, des éléments enfants et des éléments parents.</span><span class="sxs-lookup"><span data-stu-id="0a0ec-111">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="0a0ec-112">Attributs</span><span class="sxs-lookup"><span data-stu-id="0a0ec-112">Attributes</span></span>  
  
|<span data-ttu-id="0a0ec-113">Attribut</span><span class="sxs-lookup"><span data-stu-id="0a0ec-113">Attribute</span></span>|<span data-ttu-id="0a0ec-114">Description</span><span class="sxs-lookup"><span data-stu-id="0a0ec-114">Description</span></span>|  
|---------------|-----------------|  
|<span data-ttu-id="0a0ec-115">type</span><span class="sxs-lookup"><span data-stu-id="0a0ec-115">type</span></span>|<span data-ttu-id="0a0ec-116">Spécifie un type personnalisé qui dérive de la <xref:System.IdentityModel.Services.CookieHandler> classe.</span><span class="sxs-lookup"><span data-stu-id="0a0ec-116">Specifies a custom type that derives from the <xref:System.IdentityModel.Services.CookieHandler> class.</span></span> <span data-ttu-id="0a0ec-117">Pour plus d’informations sur la façon de spécifier le `type` d’attribut, consultez [références de Type personnalisé](../../../../../docs/framework/configure-apps/file-schema/windows-workflow-foundation/index.md).</span><span class="sxs-lookup"><span data-stu-id="0a0ec-117">For more information about how to specify the `type` attribute, see [Custom Type References](../../../../../docs/framework/configure-apps/file-schema/windows-workflow-foundation/index.md).</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="0a0ec-118">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="0a0ec-118">Child Elements</span></span>  
 <span data-ttu-id="0a0ec-119">Aucun.</span><span class="sxs-lookup"><span data-stu-id="0a0ec-119">None</span></span>  
  
### <a name="parent-elements"></a><span data-ttu-id="0a0ec-120">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="0a0ec-120">Parent Elements</span></span>  
  
|<span data-ttu-id="0a0ec-121">Élément</span><span class="sxs-lookup"><span data-stu-id="0a0ec-121">Element</span></span>|<span data-ttu-id="0a0ec-122">Description</span><span class="sxs-lookup"><span data-stu-id="0a0ec-122">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="0a0ec-123">\<cookieHandler></span><span class="sxs-lookup"><span data-stu-id="0a0ec-123">\<cookieHandler></span></span>](../../../../../docs/framework/configure-apps/file-schema/windows-identity-foundation/cookiehandler.md)|<span data-ttu-id="0a0ec-124">Configure le <xref:System.IdentityModel.Services.CookieHandler> qui le <xref:System.IdentityModel.Services.SessionAuthenticationModule> utilise pour lire et écrire des cookies.</span><span class="sxs-lookup"><span data-stu-id="0a0ec-124">Configures the <xref:System.IdentityModel.Services.CookieHandler> that the <xref:System.IdentityModel.Services.SessionAuthenticationModule> uses to read and write cookies.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="0a0ec-125">Notes</span><span class="sxs-lookup"><span data-stu-id="0a0ec-125">Remarks</span></span>  
 <span data-ttu-id="0a0ec-126">Lorsque vous spécifiez un gestionnaire de cookie personnalisé en définissant le `mode` attribut de la `<cookieHandler>` élément « Personnalisé », vous devez spécifier le type du Gestionnaire de cookie personnalisé en incluant un `<customCookieHandler>` élément enfant qui fait référence au type de gestionnaire de cookie.</span><span class="sxs-lookup"><span data-stu-id="0a0ec-126">When you specify a custom cookie handler by setting the `mode` attribute of the `<cookieHandler>` element to "Custom", you must specify the type of the custom cookie handler by including a `<customCookieHandler>` child element that references the cookie handler type.</span></span> <span data-ttu-id="0a0ec-127">Cet élément ne peut pas être spécifié lorsque le `mode` attribut a la valeur « Chunked » ou « Default ».</span><span class="sxs-lookup"><span data-stu-id="0a0ec-127">This element cannot be specified when the `mode` attribute is set to "Chunked" or "Default".</span></span> <span data-ttu-id="0a0ec-128">Gestionnaires de cookie personnalisé doivent dériver de la <xref:System.IdentityModel.Services.CookieHandler> classe.</span><span class="sxs-lookup"><span data-stu-id="0a0ec-128">Custom cookie handlers must derive from the <xref:System.IdentityModel.Services.CookieHandler> class.</span></span>  
  
 <span data-ttu-id="0a0ec-129">Le `<customCookieHandler>` élément est représenté par la <xref:System.IdentityModel.Configuration.CustomTypeElement> classe.</span><span class="sxs-lookup"><span data-stu-id="0a0ec-129">The `<customCookieHandler>` element is represented by the <xref:System.IdentityModel.Configuration.CustomTypeElement> class.</span></span>  
  
## <a name="example"></a><span data-ttu-id="0a0ec-130">Exemple</span><span class="sxs-lookup"><span data-stu-id="0a0ec-130">Example</span></span>  
 <span data-ttu-id="0a0ec-131">L’exemple suivant configure le module SAM pour utiliser un gestionnaire de cookie personnalisé de type `MyNamespace.MyCustomCookieHandler`.</span><span class="sxs-lookup"><span data-stu-id="0a0ec-131">The following example configures the SAM to use a custom cookie handler of type `MyNamespace.MyCustomCookieHandler`.</span></span>  
  
```xml  
<cookieHandler mode="Custom">  
    <customCookieHandler type="MyNamespace.MyCustomCookieHandler, MyAssembly" />  
</cookieHandler>  
```  
  
## <a name="see-also"></a><span data-ttu-id="0a0ec-132">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0a0ec-132">See also</span></span>

- <xref:System.IdentityModel.Services.CookieHandler>
