---
title: <add>, élément d’authenticationModules (paramètres réseau)
ms.date: 03/30/2017
f1_keywords:
- http://schemas.microsoft.com/.NetConfiguration/v2.0#add
- http://schemas.microsoft.com/.NetConfiguration/v2.0#configuration/system.net/authenticationModules/add
helpviewer_keywords:
- authenticationModules, add element
- add element, authenticationModules
- <authenticationModules>, add element
- <add> element, authenticationModules
ms.assetid: 333c5fb0-a2ab-4db8-8531-a7fe37bb9b5b
ms.openlocfilehash: a46e6af97f37974805812fb0d19801d618eee4d4
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59105870"
---
# <a name="add-element-for-authenticationmodules-network-settings"></a><span data-ttu-id="dc97b-102">\<Ajouter > élément d’authenticationModules (paramètres réseau)</span><span class="sxs-lookup"><span data-stu-id="dc97b-102">\<add> Element for authenticationModules (Network Settings)</span></span>
<span data-ttu-id="dc97b-103">Ajoute un module d’authentification à l’application.</span><span class="sxs-lookup"><span data-stu-id="dc97b-103">Adds an authentication module to the application.</span></span>  
  
 <span data-ttu-id="dc97b-104">\<configuration></span><span class="sxs-lookup"><span data-stu-id="dc97b-104">\<configuration></span></span>  
<span data-ttu-id="dc97b-105">\<system.net></span><span class="sxs-lookup"><span data-stu-id="dc97b-105">\<system.net></span></span>  
<span data-ttu-id="dc97b-106">\<authenticationModules></span><span class="sxs-lookup"><span data-stu-id="dc97b-106">\<authenticationModules></span></span>  
<span data-ttu-id="dc97b-107">\<add></span><span class="sxs-lookup"><span data-stu-id="dc97b-107">\<add></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="dc97b-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="dc97b-108">Syntax</span></span>  
  
```xml  
<add
  type="type_fullname, assembly_fullname"   
/>  
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="dc97b-109">Attributs et éléments</span><span class="sxs-lookup"><span data-stu-id="dc97b-109">Attributes and Elements</span></span>  
 <span data-ttu-id="dc97b-110">Les sections suivantes décrivent des attributs, des éléments enfants et des éléments parents.</span><span class="sxs-lookup"><span data-stu-id="dc97b-110">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="dc97b-111">Attributs</span><span class="sxs-lookup"><span data-stu-id="dc97b-111">Attributes</span></span>  
  
|<span data-ttu-id="dc97b-112">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="dc97b-112">**Attribute**</span></span>|<span data-ttu-id="dc97b-113">**Description**</span><span class="sxs-lookup"><span data-stu-id="dc97b-113">**Description**</span></span>|  
|-------------------|---------------------|  
|`type`|<span data-ttu-id="dc97b-114">Le nom de type qualifié complet (indiqué par le <xref:System.Type.FullName%2A> propriété) et le nom d’assembly (indiqué par le <xref:System.Reflection.Assembly.FullName%2A> propriété), séparés par une virgule.</span><span class="sxs-lookup"><span data-stu-id="dc97b-114">The fully qualified type name (indicated by the <xref:System.Type.FullName%2A> property) and the assembly name (indicated by the <xref:System.Reflection.Assembly.FullName%2A> property), separated by a comma.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="dc97b-115">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="dc97b-115">Child Elements</span></span>  
 <span data-ttu-id="dc97b-116">Aucun.</span><span class="sxs-lookup"><span data-stu-id="dc97b-116">None.</span></span>  
  
### <a name="parent-elements"></a><span data-ttu-id="dc97b-117">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="dc97b-117">Parent Elements</span></span>  
  
|<span data-ttu-id="dc97b-118">**Élément**</span><span class="sxs-lookup"><span data-stu-id="dc97b-118">**Element**</span></span>|<span data-ttu-id="dc97b-119">**Description**</span><span class="sxs-lookup"><span data-stu-id="dc97b-119">**Description**</span></span>|  
|-----------------|---------------------|  
|[<span data-ttu-id="dc97b-120">authenticationModules</span><span class="sxs-lookup"><span data-stu-id="dc97b-120">authenticationModules</span></span>](../../../../../docs/framework/configure-apps/file-schema/network/authenticationmodules-element-network-settings.md)|<span data-ttu-id="dc97b-121">Spécifie les modules utilisés pour authentifier les demandes du réseau.</span><span class="sxs-lookup"><span data-stu-id="dc97b-121">Specifies modules used to authenticate network requests.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="dc97b-122">Notes</span><span class="sxs-lookup"><span data-stu-id="dc97b-122">Remarks</span></span>  
 <span data-ttu-id="dc97b-123">Le `add` élément ajoute un module d’authentification à la fin de la liste des modules d’authentification inscrits.</span><span class="sxs-lookup"><span data-stu-id="dc97b-123">The `add` element adds an authentication module to the end of the list of registered authentication modules.</span></span> <span data-ttu-id="dc97b-124">Modules d’authentification sont appelés dans l’ordre dans lequel ils ont été ajoutés à la liste.</span><span class="sxs-lookup"><span data-stu-id="dc97b-124">Authentication modules are called in the order in which they were added to the list.</span></span>  
  
 <span data-ttu-id="dc97b-125">La valeur de la `type` attribut doit être un nom de type valide et le nom de l’assembly correspondant, séparés par une virgule.</span><span class="sxs-lookup"><span data-stu-id="dc97b-125">The value for the `type` attribute should be a valid type name and corresponding assembly name, separated by a comma.</span></span>  
  
## <a name="configuration-files"></a><span data-ttu-id="dc97b-126">Fichiers de configuration</span><span class="sxs-lookup"><span data-stu-id="dc97b-126">Configuration Files</span></span>  
 <span data-ttu-id="dc97b-127">Cet élément peut être défini dans le fichier de configuration de l'application ou dans le fichier de configuration de l'ordinateur (Machine.config).</span><span class="sxs-lookup"><span data-stu-id="dc97b-127">This element can be used in the application configuration file or the machine configuration file (Machine.config).</span></span>  
  
## <a name="example"></a><span data-ttu-id="dc97b-128">Exemple</span><span class="sxs-lookup"><span data-stu-id="dc97b-128">Example</span></span>  
 <span data-ttu-id="dc97b-129">L’exemple suivant active les modules d’authentification par défaut.</span><span class="sxs-lookup"><span data-stu-id="dc97b-129">The following example enables the default authentication modules.</span></span> <span data-ttu-id="dc97b-130">Vous devez remplacer les valeurs de Version et PublicKeyToken par les valeurs correctes pour le module spécifié.</span><span class="sxs-lookup"><span data-stu-id="dc97b-130">You should replace the values for Version and PublicKeyToken with the correct values for the specified module.</span></span>  
  
```xml  
<configuration>  
  <system.net>  
        <authenticationModules>  
            <add type="System.Net.DigestClient, System, Version=2.0.3600.0,  
                 Culture=neutral, PublicKeyToken=b77a5c561934e089" />  
            <add type="System.Net.NegotiateClient, System, Version=2.0.3600.0,  
                 Culture=neutral, PublicKeyToken=b77a5c561934e089" />  
            <add type="System.Net.KerberosClient, System, Version=2.0.3600.0,  
                 Culture=neutral, PublicKeyToken=b77a5c561934e089" />  
            <add type="System.Net.NtlmClient, System, Version=2.0.3600.0,  
                 Culture=neutral, PublicKeyToken=b77a5c561934e089" />  
            <add type="System.Net.BasicClient, System, Version=2.0.3600.0,  
                 Culture=neutral, PublicKeyToken=b77a5c561934e089" />  
        </authenticationModules>  
  </system.net>  
</configuration>  
```  
  
## <a name="see-also"></a><span data-ttu-id="dc97b-131">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="dc97b-131">See also</span></span>

- <xref:System.Net.IAuthenticationModule>
- <xref:System.Net.AuthenticationManager>
- [<span data-ttu-id="dc97b-132">Schéma des paramètres réseau</span><span class="sxs-lookup"><span data-stu-id="dc97b-132">Network Settings Schema</span></span>](../../../../../docs/framework/configure-apps/file-schema/network/index.md)
