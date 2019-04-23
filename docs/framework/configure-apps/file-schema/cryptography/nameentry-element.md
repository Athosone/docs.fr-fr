---
title: Élément <nameEntry>
ms.date: 03/30/2017
f1_keywords:
- http://schemas.microsoft.com/.NetConfiguration/v2.0#nameEntry
- http://schemas.microsoft.com/.NetConfiguration/v2.0#configuration/mscorlib/cryptographySettings/cryptoNameMapping/nameEntry
helpviewer_keywords:
- <nameEntry> element
- nameEntry element
ms.assetid: 7d7535e9-4b4a-4b8c-82e2-e40dff5a7821
ms.openlocfilehash: 97521ba9073820beeea62f5fc7cab480b5422fb0
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59225324"
---
# <a name="nameentry-element"></a><span data-ttu-id="4f2a8-102">\<nameEntry > élément</span><span class="sxs-lookup"><span data-stu-id="4f2a8-102">\<nameEntry> Element</span></span>
<span data-ttu-id="4f2a8-103">Mappe un nom de classe à un nom d’algorithme convivial, ce qui permet à une classe d’avoir plusieurs noms conviviaux.</span><span class="sxs-lookup"><span data-stu-id="4f2a8-103">Maps a class name to a friendly algorithm name, which allows one class to have many friendly names.</span></span>  
  
 <span data-ttu-id="4f2a8-104">\<configuration></span><span class="sxs-lookup"><span data-stu-id="4f2a8-104">\<configuration></span></span>  
<span data-ttu-id="4f2a8-105">\<mscorlib></span><span class="sxs-lookup"><span data-stu-id="4f2a8-105">\<mscorlib></span></span>  
<span data-ttu-id="4f2a8-106">\<cryptographySettings></span><span class="sxs-lookup"><span data-stu-id="4f2a8-106">\<cryptographySettings></span></span>  
<span data-ttu-id="4f2a8-107">\<cryptoNameMapping></span><span class="sxs-lookup"><span data-stu-id="4f2a8-107">\<cryptoNameMapping></span></span>  
<span data-ttu-id="4f2a8-108">\<nameEntry></span><span class="sxs-lookup"><span data-stu-id="4f2a8-108">\<nameEntry></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="4f2a8-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="4f2a8-109">Syntax</span></span>  
  
```xml  
<nameEntry name="friendly name" Class="class name" />  
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="4f2a8-110">Attributs et éléments</span><span class="sxs-lookup"><span data-stu-id="4f2a8-110">Attributes and Elements</span></span>  
 <span data-ttu-id="4f2a8-111">Les sections suivantes décrivent des attributs, des éléments enfants et des éléments parents.</span><span class="sxs-lookup"><span data-stu-id="4f2a8-111">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="4f2a8-112">Attributs</span><span class="sxs-lookup"><span data-stu-id="4f2a8-112">Attributes</span></span>  
  
|<span data-ttu-id="4f2a8-113">Attribut</span><span class="sxs-lookup"><span data-stu-id="4f2a8-113">Attribute</span></span>|<span data-ttu-id="4f2a8-114">Description</span><span class="sxs-lookup"><span data-stu-id="4f2a8-114">Description</span></span>|  
|---------------|-----------------|  
|<span data-ttu-id="4f2a8-115">**name**</span><span class="sxs-lookup"><span data-stu-id="4f2a8-115">**name**</span></span>|<span data-ttu-id="4f2a8-116">Attribut requis.</span><span class="sxs-lookup"><span data-stu-id="4f2a8-116">Required attribute.</span></span><br /><br /> <span data-ttu-id="4f2a8-117">Spécifie le nom convivial de l’algorithme qui implémente la classe de chiffrement.</span><span class="sxs-lookup"><span data-stu-id="4f2a8-117">Specifies the friendly name of the algorithm that the cryptography class implements.</span></span>|  
|<span data-ttu-id="4f2a8-118">**class**</span><span class="sxs-lookup"><span data-stu-id="4f2a8-118">**class**</span></span>|<span data-ttu-id="4f2a8-119">Attribut requis.</span><span class="sxs-lookup"><span data-stu-id="4f2a8-119">Required attribute.</span></span><br /><br /> <span data-ttu-id="4f2a8-120">Spécifie la valeur de la **nom** d’attribut dans le [ \<cryptoClass >](../../../../../docs/framework/configure-apps/file-schema/cryptography/cryptoclass-element.md) élément.</span><span class="sxs-lookup"><span data-stu-id="4f2a8-120">Specifies the value for the **name** attribute in the [\<cryptoClass>](../../../../../docs/framework/configure-apps/file-schema/cryptography/cryptoclass-element.md) element.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="4f2a8-121">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="4f2a8-121">Child Elements</span></span>  
 <span data-ttu-id="4f2a8-122">Aucun.</span><span class="sxs-lookup"><span data-stu-id="4f2a8-122">None.</span></span>  
  
### <a name="parent-elements"></a><span data-ttu-id="4f2a8-123">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="4f2a8-123">Parent Elements</span></span>  
  
|<span data-ttu-id="4f2a8-124">Élément</span><span class="sxs-lookup"><span data-stu-id="4f2a8-124">Element</span></span>|<span data-ttu-id="4f2a8-125">Description</span><span class="sxs-lookup"><span data-stu-id="4f2a8-125">Description</span></span>|  
|-------------|-----------------|  
|`configuration`|<span data-ttu-id="4f2a8-126">Élément racine de chaque fichier de configuration utilisé par le Common Language Runtime et les applications .NET Framework.</span><span class="sxs-lookup"><span data-stu-id="4f2a8-126">The root element in every configuration file used by the common language runtime and .NET Framework applications.</span></span>|  
|`system.web`|<span data-ttu-id="4f2a8-127">Spécifie l'élément racine de la section de configuration ASP.NET.</span><span class="sxs-lookup"><span data-stu-id="4f2a8-127">Specifies the root element for the ASP.NET configuration section.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="4f2a8-128">Notes</span><span class="sxs-lookup"><span data-stu-id="4f2a8-128">Remarks</span></span>  
 <span data-ttu-id="4f2a8-129">Le **nom** attribut peut être le nom de l’une des classes abstraites trouvées dans le <xref:System.Security.Cryptography> espace de noms.</span><span class="sxs-lookup"><span data-stu-id="4f2a8-129">The **name** attribute can be the name of one of the abstract classes found in the <xref:System.Security.Cryptography> namespace.</span></span> <span data-ttu-id="4f2a8-130">Lorsque vous appelez le **créer** méthode sur une classe de chiffrement abstraite, le nom de classe abstraite est passé à la <xref:System.Security.Cryptography.CryptoConfig.CreateFromName%2A> (méthode).</span><span class="sxs-lookup"><span data-stu-id="4f2a8-130">When you call the **Create** method on an abstract cryptography class, the abstract class name is passed to the <xref:System.Security.Cryptography.CryptoConfig.CreateFromName%2A> method.</span></span> <span data-ttu-id="4f2a8-131">**CreateFromName** retourne une instance du type indiqué par la **classe** attribut.</span><span class="sxs-lookup"><span data-stu-id="4f2a8-131">**CreateFromName** returns an instance of the type indicated by the **class** attribute.</span></span> <span data-ttu-id="4f2a8-132">Si le **nom** attribut est un nom court, tels que RSA, vous pouvez utiliser ce nom lors de l’appel le **CreateFromName** (méthode).</span><span class="sxs-lookup"><span data-stu-id="4f2a8-132">If the **name** attribute is a short name, such as RSA, you can use that name when calling the **CreateFromName** method.</span></span>  
  
## <a name="example"></a><span data-ttu-id="4f2a8-133">Exemple</span><span class="sxs-lookup"><span data-stu-id="4f2a8-133">Example</span></span>  
 <span data-ttu-id="4f2a8-134">L’exemple suivant montre comment utiliser le  **\<nameEntry >** élément à référencer une classe de chiffrement et configurer le runtime.</span><span class="sxs-lookup"><span data-stu-id="4f2a8-134">The following example shows how to use the **\<nameEntry>** element to reference a cryptography class and to configure the runtime.</span></span> <span data-ttu-id="4f2a8-135">Vous pouvez ensuite passer la chaîne « RSA » à la <xref:System.Security.Cryptography.CryptoConfig.CreateFromName%2A?displayProperty=nameWithType> méthode et l’utilisation du <xref:System.Security.Cryptography.AsymmetricAlgorithm.Create%2A> méthode pour retourner un `MyCryptoRSAClass` objet.</span><span class="sxs-lookup"><span data-stu-id="4f2a8-135">You can then pass the string "RSA" to the <xref:System.Security.Cryptography.CryptoConfig.CreateFromName%2A?displayProperty=nameWithType> method and use the <xref:System.Security.Cryptography.AsymmetricAlgorithm.Create%2A> method to return a `MyCryptoRSAClass` object.</span></span>  
  
```xml  
<configuration>  
   <mscorlib>  
      <cryptographySettings>  
         <cryptoNameMapping>  
            <cryptoClasses>  
               <cryptoClass   MyCryptoRSA="MyCryptoRSAClass, MyAssembly  
                  Culture=neutral, PublicKeyToken=a5d015c7d5a0b012,  
                  Version=1.0.0.0"/>  
            </cryptoClasses>  
            <nameEntry name="RSA" class="MyCryptoRSA"/>  
            <nameEntry name="System.Security.Cryptography.AsymmetricAlgorithm"  
                       class="MyCryptoRSA"/>  
         </cryptoNameMapping>  
      </cryptographySettings>  
   </mscorlib>  
</configuration>  
```  
  
## <a name="see-also"></a><span data-ttu-id="4f2a8-136">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="4f2a8-136">See also</span></span>

- [<span data-ttu-id="4f2a8-137">Schéma des fichiers de configuration</span><span class="sxs-lookup"><span data-stu-id="4f2a8-137">Configuration File Schema</span></span>](../../../../../docs/framework/configure-apps/file-schema/index.md)
- [<span data-ttu-id="4f2a8-138">Schéma des paramètres de chiffrement</span><span class="sxs-lookup"><span data-stu-id="4f2a8-138">Cryptography Settings Schema</span></span>](../../../../../docs/framework/configure-apps/file-schema/cryptography/index.md)
- [<span data-ttu-id="4f2a8-139">Cryptographic Services</span><span class="sxs-lookup"><span data-stu-id="4f2a8-139">Cryptographic Services</span></span>](../../../../../docs/standard/security/cryptographic-services.md)
- [<span data-ttu-id="4f2a8-140">Configuration des classes de chiffrement</span><span class="sxs-lookup"><span data-stu-id="4f2a8-140">Configuring Cryptography Classes</span></span>](../../../../../docs/framework/configure-apps/configure-cryptography-classes.md)
