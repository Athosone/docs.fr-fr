---
title: <specifiedPickupDirectory>, élément (paramètres réseau)
ms.date: 03/30/2017
f1_keywords:
- http://schemas.microsoft.com/.NetConfiguration/v2.0#specifiedPickupDirectory
- http://schemas.microsoft.com/.NetConfiguration/v2.0#configuration/system.net/mailSettings/smtp/specifiedPickupDirectory
helpviewer_keywords:
- specifiedPickupDirectory element
- <specifiedPickupDirectory> element
ms.assetid: 0121f49d-bff2-4bc6-af06-f1628dcd61f1
ms.openlocfilehash: a459fee557285935c383dcfaf512c8a8a9aea570
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59099272"
---
# <a name="specifiedpickupdirectory-element-network-settings"></a><span data-ttu-id="391da-102">\<specifiedPickupDirectory >, élément (paramètres réseau)</span><span class="sxs-lookup"><span data-stu-id="391da-102">\<specifiedPickupDirectory> Element (Network Settings)</span></span>
<span data-ttu-id="391da-103">Configure le répertoire local pour un serveur SMTP Simple Mail Transport Protocol ().</span><span class="sxs-lookup"><span data-stu-id="391da-103">Configures the local directory for a Simple Mail Transport Protocol (SMTP) server.</span></span>  
  
 <span data-ttu-id="391da-104">\<configuration></span><span class="sxs-lookup"><span data-stu-id="391da-104">\<configuration></span></span>  
<span data-ttu-id="391da-105">\<system.net></span><span class="sxs-lookup"><span data-stu-id="391da-105">\<system.net></span></span>  
<span data-ttu-id="391da-106">\<mailSettings></span><span class="sxs-lookup"><span data-stu-id="391da-106">\<mailSettings></span></span>  
<span data-ttu-id="391da-107">\<smtp></span><span class="sxs-lookup"><span data-stu-id="391da-107">\<smtp></span></span>  
<span data-ttu-id="391da-108">\<specifiedPickupDirectory></span><span class="sxs-lookup"><span data-stu-id="391da-108">\<specifiedPickupDirectory></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="391da-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="391da-109">Syntax</span></span>  
  
```xml  
<specifiedPickupDirectory  
  pickupDirectoryLocation="directory"   
/>  
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="391da-110">Attributs et éléments</span><span class="sxs-lookup"><span data-stu-id="391da-110">Attributes and Elements</span></span>  
 <span data-ttu-id="391da-111">Les sections suivantes décrivent des attributs, des éléments enfants et des éléments parents.</span><span class="sxs-lookup"><span data-stu-id="391da-111">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="391da-112">Attributs</span><span class="sxs-lookup"><span data-stu-id="391da-112">Attributes</span></span>  
  
|<span data-ttu-id="391da-113">Attribut</span><span class="sxs-lookup"><span data-stu-id="391da-113">Attribute</span></span>|<span data-ttu-id="391da-114">Description</span><span class="sxs-lookup"><span data-stu-id="391da-114">Description</span></span>|  
|---------------|-----------------|  
|`pickupDirectoryLocation`|<span data-ttu-id="391da-115">Le répertoire dans lequel les applications enregistrent e-mail pour un traitement ultérieur par le serveur SMTP.</span><span class="sxs-lookup"><span data-stu-id="391da-115">The directory where applications save email for later processing by the SMTP server.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="391da-116">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="391da-116">Child Elements</span></span>  
 <span data-ttu-id="391da-117">Aucun.</span><span class="sxs-lookup"><span data-stu-id="391da-117">None.</span></span>  
  
### <a name="parent-elements"></a><span data-ttu-id="391da-118">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="391da-118">Parent Elements</span></span>  
  
|<span data-ttu-id="391da-119">Élément</span><span class="sxs-lookup"><span data-stu-id="391da-119">Element</span></span>|<span data-ttu-id="391da-120">Description</span><span class="sxs-lookup"><span data-stu-id="391da-120">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="391da-121">\<SMTP >, élément (paramètres réseau)</span><span class="sxs-lookup"><span data-stu-id="391da-121">\<smtp> Element (Network Settings)</span></span>](../../../../../docs/framework/configure-apps/file-schema/network/smtp-element-network-settings.md)|<span data-ttu-id="391da-122">Configure les options d’envoi du courrier SMTP Simple Mail Transport Protocol ().</span><span class="sxs-lookup"><span data-stu-id="391da-122">Configures Simple Mail Transport Protocol (SMTP) mail sending options.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="391da-123">Notes</span><span class="sxs-lookup"><span data-stu-id="391da-123">Remarks</span></span>  
 <span data-ttu-id="391da-124">Le `specifiedPickupDirectory` attribut définit le répertoire dans lequel les applications enregistrent les messages électroniques à traiter par le serveur SMTP.</span><span class="sxs-lookup"><span data-stu-id="391da-124">The `specifiedPickupDirectory` attribute sets the directory where applications save mail messages to be processed by the SMTP server.</span></span>  
  
## <a name="example"></a><span data-ttu-id="391da-125">Exemple</span><span class="sxs-lookup"><span data-stu-id="391da-125">Example</span></span>  
 <span data-ttu-id="391da-126">L’exemple suivant indique c:\maildrop comme répertoire de collecte de messagerie.</span><span class="sxs-lookup"><span data-stu-id="391da-126">The following example specifies c:\maildrop as the mail pickup directory.</span></span>  
  
```xml  
<configuration>  
  <system.net>  
    <mailSettings>  
      <smtp deliveryMethod="SpecifiedPickupDirectory">  
        <specifiedPickupDirectory  
          pickupDirectoryLocation="c:\maildrop"  
        />  
      </smtp>  
    </mailSettings>  
  </system.net>  
</configuration>  
```  
  
## <a name="see-also"></a><span data-ttu-id="391da-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="391da-127">See also</span></span>

- <xref:System.Net.Mail.SmtpClient?displayProperty=nameWithType>
- <xref:System.Net.Configuration.SmtpSection?displayProperty=nameWithType>
- <xref:System.Net.Configuration.SmtpSpecifiedPickupDirectoryElement?displayProperty=nameWithType>
- [<span data-ttu-id="391da-128">Schéma des paramètres réseau</span><span class="sxs-lookup"><span data-stu-id="391da-128">Network Settings Schema</span></span>](../../../../../docs/framework/configure-apps/file-schema/network/index.md)
