---
title: Élément <cryptographySettings>
ms.date: 03/30/2017
f1_keywords:
- http://schemas.microsoft.com/.NetConfiguration/v2.0#configuration/mscorlib/cryptographySettings
- http://schemas.microsoft.com/.NetConfiguration/v2.0#cryptographySettings
helpviewer_keywords:
- cryptographySettings element
- <cryptographySettings> element
ms.assetid: 6201b7da-bcb7-49f7-b9f5-ba1fe05573b9
ms.openlocfilehash: ec3a5a73caa901a21e22dbec7500af9153e01ef4
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61705218"
---
# <a name="cryptographysettings-element"></a><span data-ttu-id="d3e4f-102">\<cryptographySettings > élément</span><span class="sxs-lookup"><span data-stu-id="d3e4f-102">\<cryptographySettings> Element</span></span>
<span data-ttu-id="d3e4f-103">Contient des paramètres de chiffrement.</span><span class="sxs-lookup"><span data-stu-id="d3e4f-103">Contains cryptography settings.</span></span>  
  
 <span data-ttu-id="d3e4f-104">\<configuration></span><span class="sxs-lookup"><span data-stu-id="d3e4f-104">\<configuration></span></span>  
<span data-ttu-id="d3e4f-105">\<mscorlib></span><span class="sxs-lookup"><span data-stu-id="d3e4f-105">\<mscorlib></span></span>  
<span data-ttu-id="d3e4f-106">\<cryptographySettings></span><span class="sxs-lookup"><span data-stu-id="d3e4f-106">\<cryptographySettings></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="d3e4f-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="d3e4f-107">Syntax</span></span>  
  
```xml  
      <cryptographySettings>   
</cryptographySettings>  
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="d3e4f-108">Attributs et éléments</span><span class="sxs-lookup"><span data-stu-id="d3e4f-108">Attributes and Elements</span></span>  
 <span data-ttu-id="d3e4f-109">Les sections suivantes décrivent des attributs, des éléments enfants et des éléments parents.</span><span class="sxs-lookup"><span data-stu-id="d3e4f-109">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="d3e4f-110">Attributs</span><span class="sxs-lookup"><span data-stu-id="d3e4f-110">Attributes</span></span>  
 <span data-ttu-id="d3e4f-111">Aucun.</span><span class="sxs-lookup"><span data-stu-id="d3e4f-111">None.</span></span>  
  
### <a name="child-elements"></a><span data-ttu-id="d3e4f-112">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="d3e4f-112">Child Elements</span></span>  
  
|<span data-ttu-id="d3e4f-113">Élément</span><span class="sxs-lookup"><span data-stu-id="d3e4f-113">Element</span></span>|<span data-ttu-id="d3e4f-114">Description</span><span class="sxs-lookup"><span data-stu-id="d3e4f-114">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="d3e4f-115">\<cryptoNameMapping></span><span class="sxs-lookup"><span data-stu-id="d3e4f-115">\<cryptoNameMapping></span></span>](../../../../../docs/framework/configure-apps/file-schema/cryptography/cryptonamemapping-element.md)|<span data-ttu-id="d3e4f-116">Contient des mappages de classes à des noms conviviaux.</span><span class="sxs-lookup"><span data-stu-id="d3e4f-116">Contains mappings of classes to friendly names.</span></span>|  
|[<span data-ttu-id="d3e4f-117">\<oidMap></span><span class="sxs-lookup"><span data-stu-id="d3e4f-117">\<oidMap></span></span>](../../../../../docs/framework/configure-apps/file-schema/cryptography/oidmap-element.md)|<span data-ttu-id="d3e4f-118">Contient des mappages d’identificateur (OID) d’objet ASN.1 aux classes.</span><span class="sxs-lookup"><span data-stu-id="d3e4f-118">Contains ASN.1 object identifier (OID) mappings to classes.</span></span>|  
  
### <a name="parent-elements"></a><span data-ttu-id="d3e4f-119">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="d3e4f-119">Parent Elements</span></span>  
  
|<span data-ttu-id="d3e4f-120">Élément</span><span class="sxs-lookup"><span data-stu-id="d3e4f-120">Element</span></span>|<span data-ttu-id="d3e4f-121">Description</span><span class="sxs-lookup"><span data-stu-id="d3e4f-121">Description</span></span>|  
|-------------|-----------------|  
|`configuration`|<span data-ttu-id="d3e4f-122">Élément racine de chaque fichier de configuration utilisé par le Common Language Runtime et les applications .NET Framework.</span><span class="sxs-lookup"><span data-stu-id="d3e4f-122">The root element in every configuration file used by the common language runtime and .NET Framework applications.</span></span>|  
|`mscorlib`|<span data-ttu-id="d3e4f-123">Contient le `cryptographySettings` élément.</span><span class="sxs-lookup"><span data-stu-id="d3e4f-123">Contains the `cryptographySettings` element.</span></span>|  
  
## <a name="example"></a><span data-ttu-id="d3e4f-124">Exemple</span><span class="sxs-lookup"><span data-stu-id="d3e4f-124">Example</span></span>  
 <span data-ttu-id="d3e4f-125">L’exemple suivant montre comment utiliser le  **\<cryptographySettings >** élément qui contient les mappages des noms de chiffrement et les mappages d’OID.</span><span class="sxs-lookup"><span data-stu-id="d3e4f-125">The following example shows how use the **\<cryptographySettings>** element to contain cryptography name mappings and OID mappings.</span></span> <span data-ttu-id="d3e4f-126">Cet exemple configure l’exécution afin que <xref:System.Security.Cryptography.HashAlgorithm.Create%2A?displayProperty=nameWithType> retourne un `MyHashClass` objet et le `MyCryptoClass` classe correspond à l’OID 1.3.36.2.1.</span><span class="sxs-lookup"><span data-stu-id="d3e4f-126">This example configures the runtime so that <xref:System.Security.Cryptography.HashAlgorithm.Create%2A?displayProperty=nameWithType> returns a `MyHashClass` object and the `MyCryptoClass` class maps to the object identifier 1.3.36.2.1.</span></span>  
  
```xml  
<configuration>  
   <mscorlib>  
      <cryptographySettings>  
         <cryptoNameMapping>  
            <cryptoClasses>  
               <cryptoClass   MyHash="MyHashClass, MyAssembly  
                  Culture=neutral, PublicKeyToken=a5d015c7d5a0b012,  
                  Version=1.0.0.0"/>  
               <cryptoClass   MyCrypto="MyCryptoClass, MyAssembly  
                  Culture=neutral, PublicKeyToken=a5d015c7d5a0b012,  
                  Version=1.0.0.0"/>  
            </cryptoClasses>  
            <nameEntry name="System.Security.Cryptography.HashAlgorithm"  
                       class="MyHash"/>  
         </cryptoNameMapping>  
         <oidMap>  
            <oidEntry OID="1.3.36.3.2.1"   name="MyCryptoClass"/>  
         </oidMap>  
      </cryptographySettings>  
   </mscorlib>  
</configuration>  
```  
  
## <a name="see-also"></a><span data-ttu-id="d3e4f-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d3e4f-127">See also</span></span>

- [<span data-ttu-id="d3e4f-128">Schéma des fichiers de configuration</span><span class="sxs-lookup"><span data-stu-id="d3e4f-128">Configuration File Schema</span></span>](../../../../../docs/framework/configure-apps/file-schema/index.md)
- [<span data-ttu-id="d3e4f-129">Schéma des paramètres de chiffrement</span><span class="sxs-lookup"><span data-stu-id="d3e4f-129">Cryptography Settings Schema</span></span>](../../../../../docs/framework/configure-apps/file-schema/cryptography/index.md)
- [<span data-ttu-id="d3e4f-130">Cryptographic Services</span><span class="sxs-lookup"><span data-stu-id="d3e4f-130">Cryptographic Services</span></span>](../../../../../docs/standard/security/cryptographic-services.md)
