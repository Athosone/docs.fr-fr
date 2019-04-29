---
title: <mtomMessageEncoding>
ms.date: 03/30/2017
ms.assetid: 7865d171-cd1e-430a-8421-39cc13541d1b
ms.openlocfilehash: 61b23957c56bad81598dd65b0dd68f7b44d329e5
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61772383"
---
# <a name="mtommessageencoding"></a><span data-ttu-id="e98d3-101">\<mtomMessageEncoding></span><span class="sxs-lookup"><span data-stu-id="e98d3-101">\<mtomMessageEncoding></span></span>
<span data-ttu-id="e98d3-102">Spécifie l'encodage et le suivi des versions de message utilisés pour les messages basés sur MTOM (Message Transmission Optimization Mechanism).</span><span class="sxs-lookup"><span data-stu-id="e98d3-102">Specifies the encoding and message versioning used for SOAP Message Transmission Optimization Mechanism (MTOM) based messages.</span></span>  
  
 <span data-ttu-id="e98d3-103">\<system.serviceModel></span><span class="sxs-lookup"><span data-stu-id="e98d3-103">\<system.serviceModel></span></span>  
<span data-ttu-id="e98d3-104">\<bindings></span><span class="sxs-lookup"><span data-stu-id="e98d3-104">\<bindings></span></span>  
<span data-ttu-id="e98d3-105">\<customBinding></span><span class="sxs-lookup"><span data-stu-id="e98d3-105">\<customBinding></span></span>  
<span data-ttu-id="e98d3-106">\<binding></span><span class="sxs-lookup"><span data-stu-id="e98d3-106">\<binding></span></span>  
<span data-ttu-id="e98d3-107">\<mtomMessageEncoding></span><span class="sxs-lookup"><span data-stu-id="e98d3-107">\<mtomMessageEncoding></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="e98d3-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="e98d3-108">Syntax</span></span>  
  
```xml  
<mtomMessageEncoding maxBufferSize="Integer"
                     maxReadPoolSize="Integer"
                     maxWritePoolSize="Integer"
                     messageVersion="Soap11Addressing1/Soap12Addressing10"
                     writeEncoding="UnicodeFffeTextEncoding/Utf16TextEncoding/Utf8TextEncoding" />
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="e98d3-109">Attributs et éléments</span><span class="sxs-lookup"><span data-stu-id="e98d3-109">Attributes and Elements</span></span>  
 <span data-ttu-id="e98d3-110">Les sections suivantes décrivent des attributs, des éléments enfants et des éléments parents.</span><span class="sxs-lookup"><span data-stu-id="e98d3-110">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="e98d3-111">Attributs</span><span class="sxs-lookup"><span data-stu-id="e98d3-111">Attributes</span></span>  
  
|<span data-ttu-id="e98d3-112">Attribut</span><span class="sxs-lookup"><span data-stu-id="e98d3-112">Attribute</span></span>|<span data-ttu-id="e98d3-113">Description</span><span class="sxs-lookup"><span data-stu-id="e98d3-113">Description</span></span>|  
|---------------|-----------------|  
|<span data-ttu-id="e98d3-114">maxBufferSize</span><span class="sxs-lookup"><span data-stu-id="e98d3-114">maxBufferSize</span></span>|<span data-ttu-id="e98d3-115">Entier qui spécifie la taille maximale de la mémoire tampon qui peut être utilisée.</span><span class="sxs-lookup"><span data-stu-id="e98d3-115">An integer that specifies the maximum size of the buffer that can be used.</span></span>|  
|<span data-ttu-id="e98d3-116">maxReadPoolSize</span><span class="sxs-lookup"><span data-stu-id="e98d3-116">maxReadPoolSize</span></span>|<span data-ttu-id="e98d3-117">Entier qui spécifie combien de messages peuvent être lus de manière simultanée sans allouer de nouveaux lecteurs.</span><span class="sxs-lookup"><span data-stu-id="e98d3-117">An integer that specifies how many messages can be read simultaneously without allocating new readers.</span></span> <span data-ttu-id="e98d3-118">Des pools plus volumineux permettent au système d'être plus tolérant aux pics d'activité au prix d'une plage de travail plus volumineuse.</span><span class="sxs-lookup"><span data-stu-id="e98d3-118">Larger pool sizes make the system more tolerant to activity spikes at the cost of a larger working set.</span></span> <span data-ttu-id="e98d3-119">La valeur par défaut est 64.</span><span class="sxs-lookup"><span data-stu-id="e98d3-119">The default is 64.</span></span>|  
|<span data-ttu-id="e98d3-120">maxWritePoolSize</span><span class="sxs-lookup"><span data-stu-id="e98d3-120">maxWritePoolSize</span></span>|<span data-ttu-id="e98d3-121">Entier qui spécifie combien de messages peuvent être envoyés simultanément sans allouer de nouveaux enregistreurs.</span><span class="sxs-lookup"><span data-stu-id="e98d3-121">An integer that specifies how many messages can be sent simultaneously without allocating new writers.</span></span> <span data-ttu-id="e98d3-122">Des pools plus volumineux permettent au système d'être plus tolérant aux pics d'activité au prix d'une plage de travail plus volumineuse.</span><span class="sxs-lookup"><span data-stu-id="e98d3-122">Larger pool sizes make the system more tolerant to activity spikes at the cost of a larger working set.</span></span> <span data-ttu-id="e98d3-123">La valeur par défaut est 16.</span><span class="sxs-lookup"><span data-stu-id="e98d3-123">The default is 16.</span></span>|  
|<span data-ttu-id="e98d3-124">messageVersion</span><span class="sxs-lookup"><span data-stu-id="e98d3-124">messageVersion</span></span>|<span data-ttu-id="e98d3-125">Spécifie la version SOAP des messages envoyés à l'aide de la liaison.</span><span class="sxs-lookup"><span data-stu-id="e98d3-125">Specifies the SOAP version of the messages sent using the binding.</span></span> <span data-ttu-id="e98d3-126">Les valeurs valides sont les suivantes :</span><span class="sxs-lookup"><span data-stu-id="e98d3-126">Valid values are</span></span><br /><br /> <span data-ttu-id="e98d3-127">-   Soap11Addressing1</span><span class="sxs-lookup"><span data-stu-id="e98d3-127">-   Soap11Addressing1</span></span><br /><span data-ttu-id="e98d3-128">-Soap12Addressing10</span><span class="sxs-lookup"><span data-stu-id="e98d3-128">-   Soap12Addressing10</span></span><br /><br /> <span data-ttu-id="e98d3-129">La valeur par défaut est Soap12Addressing10.</span><span class="sxs-lookup"><span data-stu-id="e98d3-129">The default is Soap12Addressing10.</span></span> <span data-ttu-id="e98d3-130">Cet attribut est de type <xref:System.ServiceModel.Channels.MessageVersion>.</span><span class="sxs-lookup"><span data-stu-id="e98d3-130">This attribute is of type <xref:System.ServiceModel.Channels.MessageVersion>.</span></span>|  
|<span data-ttu-id="e98d3-131">writeEncoding</span><span class="sxs-lookup"><span data-stu-id="e98d3-131">writeEncoding</span></span>|<span data-ttu-id="e98d3-132">Spécifie l'encodage de jeu de caractères à utiliser pour l'émission de messages sur la liaison.</span><span class="sxs-lookup"><span data-stu-id="e98d3-132">Specifies the character set encoding to be used for emitting messages on the binding.</span></span> <span data-ttu-id="e98d3-133">Les valeurs valides sont les suivantes :</span><span class="sxs-lookup"><span data-stu-id="e98d3-133">Valid values are</span></span><br /><br /> <span data-ttu-id="e98d3-134">-   UnicodeFffeTextEncoding: Codage Unicode BigEndian</span><span class="sxs-lookup"><span data-stu-id="e98d3-134">-   UnicodeFffeTextEncoding: Unicode BigEndian encoding</span></span><br /><span data-ttu-id="e98d3-135">-   Utf16TextEncoding: Encodage Unicode</span><span class="sxs-lookup"><span data-stu-id="e98d3-135">-   Utf16TextEncoding: Unicode encoding</span></span><br /><span data-ttu-id="e98d3-136">-   Utf8TextEncoding: codage 8 bits</span><span class="sxs-lookup"><span data-stu-id="e98d3-136">-   Utf8TextEncoding: 8-bit encoding</span></span><br /><br /> <span data-ttu-id="e98d3-137">La valeur par défaut est Utf8TextEncoding.</span><span class="sxs-lookup"><span data-stu-id="e98d3-137">The default is Utf8TextEncoding.</span></span> <span data-ttu-id="e98d3-138">Cet attribut est de type <xref:System.Text.Encoding>.</span><span class="sxs-lookup"><span data-stu-id="e98d3-138">This attribute is of type <xref:System.Text.Encoding>.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="e98d3-139">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="e98d3-139">Child Elements</span></span>  
  
|<span data-ttu-id="e98d3-140">Élément</span><span class="sxs-lookup"><span data-stu-id="e98d3-140">Element</span></span>|<span data-ttu-id="e98d3-141">Description</span><span class="sxs-lookup"><span data-stu-id="e98d3-141">Description</span></span>|  
|-------------|-----------------|  
|<span data-ttu-id="e98d3-142">[\<readerQuotas>](https://docs.microsoft.com/previous-versions/dotnet/netframework-4.0/ms731325(v=vs.100))</span><span class="sxs-lookup"><span data-stu-id="e98d3-142">[\<readerQuotas>](https://docs.microsoft.com/previous-versions/dotnet/netframework-4.0/ms731325(v=vs.100))</span></span>|<span data-ttu-id="e98d3-143">Définit les contraintes sur la complexité des messages SOAP pouvant être traités par les points de terminaison configurés avec cette liaison.</span><span class="sxs-lookup"><span data-stu-id="e98d3-143">Defines the constraints on the complexity of SOAP messages that can be processed by endpoints configured with this binding.</span></span> <span data-ttu-id="e98d3-144">Cet élément est de type <xref:System.ServiceModel.Configuration.XmlDictionaryReaderQuotasElement>.</span><span class="sxs-lookup"><span data-stu-id="e98d3-144">This element is of type <xref:System.ServiceModel.Configuration.XmlDictionaryReaderQuotasElement>.</span></span>|  
  
### <a name="parent-elements"></a><span data-ttu-id="e98d3-145">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="e98d3-145">Parent Elements</span></span>  
  
|<span data-ttu-id="e98d3-146">Élément</span><span class="sxs-lookup"><span data-stu-id="e98d3-146">Element</span></span>|<span data-ttu-id="e98d3-147">Description</span><span class="sxs-lookup"><span data-stu-id="e98d3-147">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="e98d3-148">\<binding></span><span class="sxs-lookup"><span data-stu-id="e98d3-148">\<binding></span></span>](../../../../../docs/framework/misc/binding.md)|<span data-ttu-id="e98d3-149">Définit toutes les fonctions de liaison d’une liaison personnalisée.</span><span class="sxs-lookup"><span data-stu-id="e98d3-149">Defines all binding capabilities of the custom binding.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="e98d3-150">Notes</span><span class="sxs-lookup"><span data-stu-id="e98d3-150">Remarks</span></span>  
 <span data-ttu-id="e98d3-151">L'encodage est le processus de transformation d'un message en une séquence d'octets.</span><span class="sxs-lookup"><span data-stu-id="e98d3-151">Encoding is the process of transforming a message into a sequence of bytes.</span></span> <span data-ttu-id="e98d3-152">Le décodage est le processus inverse.</span><span class="sxs-lookup"><span data-stu-id="e98d3-152">Decoding is the reverse process.</span></span> <span data-ttu-id="e98d3-153">Windows Communication Foundation (WCF) inclut trois types d’encodage des messages SOAP : Texte, binaire et Message Transmission Optimization Mechanism (MTOM).</span><span class="sxs-lookup"><span data-stu-id="e98d3-153">Windows Communication Foundation (WCF) includes three types of encoding for SOAP messages: Text, Binary and Message Transmission Optimization Mechanism (MTOM).</span></span>  
  
 <span data-ttu-id="e98d3-154">L'élément `MtomMessageEncoding` spécifie l'encodage de caractères et le contrôle de version de message, ainsi que d'autres paramètres utilisés pour un message encodé avec MTOM (Message Transmission Optimization Mechanism).</span><span class="sxs-lookup"><span data-stu-id="e98d3-154">The `MtomMessageEncoding` element specifies the character encoding and message versioning and other settings used for messages using a Message Transmission Optimization Mechanism (MTOM) encoding.</span></span> <span data-ttu-id="e98d3-155">MTOM est une technologie efficace de transmission de données binaires dans les messages WCF.</span><span class="sxs-lookup"><span data-stu-id="e98d3-155">MTOM is an efficient technology for transmitting binary data in WCF messages.</span></span> <span data-ttu-id="e98d3-156">L'encodeur MTOM tente de créer un équilibre entre rendement et interopérabilité.</span><span class="sxs-lookup"><span data-stu-id="e98d3-156">The MTOM encoder attempts to create a balance between efficiency and interoperability.</span></span> <span data-ttu-id="e98d3-157">L'encodage MTOM transmet la plupart des données XML sous forme textuelle, mais optimise les blocs de données binaires volumineux en les transmettant tels quels, sans conversion au format base64 encodé.</span><span class="sxs-lookup"><span data-stu-id="e98d3-157">The MTOM encoding transmits most XML in textual form, but optimizes large blocks of binary data by transmitting them as-is, without conversion to their base64 encoded format.</span></span>  
  
## <a name="example"></a><span data-ttu-id="e98d3-158">Exemple</span><span class="sxs-lookup"><span data-stu-id="e98d3-158">Example</span></span>  
  
```xml  
<mtomMessageEncoding maxReadPoolSize="211"
                     maxWritePoolSize="2132"
                     messageVersion="Soap11Addressing10"
                     textEncoding="utf-8" />
```  
  
## <a name="see-also"></a><span data-ttu-id="e98d3-159">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e98d3-159">See also</span></span>

- <xref:System.ServiceModel.Configuration.MtomMessageEncodingElement>
- <xref:System.ServiceModel.Channels.CustomBinding>
- <xref:System.ServiceModel.Channels.MessageEncodingBindingElement>
- <xref:System.ServiceModel.Channels.MtomMessageEncodingBindingElement>
- [<span data-ttu-id="e98d3-160">Encodage de message</span><span class="sxs-lookup"><span data-stu-id="e98d3-160">Message Encoding</span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/message-encoding.md)
- [<span data-ttu-id="e98d3-161">Sélection d’un encodeur de message</span><span class="sxs-lookup"><span data-stu-id="e98d3-161">Choosing a Message Encoder</span></span>](../../../../../docs/framework/wcf/feature-details/choosing-a-message-encoder.md)
- [<span data-ttu-id="e98d3-162">Liaisons</span><span class="sxs-lookup"><span data-stu-id="e98d3-162">Bindings</span></span>](../../../../../docs/framework/wcf/bindings.md)
- [<span data-ttu-id="e98d3-163">Extension de liaisons</span><span class="sxs-lookup"><span data-stu-id="e98d3-163">Extending Bindings</span></span>](../../../../../docs/framework/wcf/extending/extending-bindings.md)
- [<span data-ttu-id="e98d3-164">Liaisons personnalisées</span><span class="sxs-lookup"><span data-stu-id="e98d3-164">Custom Bindings</span></span>](../../../../../docs/framework/wcf/extending/custom-bindings.md)
- [<span data-ttu-id="e98d3-165">\<customBinding></span><span class="sxs-lookup"><span data-stu-id="e98d3-165">\<customBinding></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/custombinding.md)
