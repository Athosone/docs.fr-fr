---
title: Élément <loadFromRemoteSources>
ms.date: 05/24/2018
helpviewer_keywords:
- loadFromRemoteSources element
- <loadFromRemoteSources> element
ms.assetid: 006d1280-2ac3-4db6-a984-a3d4e275046a
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 7568129f30267b212737ec8aa688cf882e19bbff
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61704594"
---
# <a name="loadfromremotesources-element"></a><span data-ttu-id="4c05a-102">\<loadFromRemoteSources > élément</span><span class="sxs-lookup"><span data-stu-id="4c05a-102">\<loadFromRemoteSources> element</span></span>
<span data-ttu-id="4c05a-103">Spécifie si les assemblys chargés à partir de sources distantes doivent être accordés une confiance totale dans .NET Framework 4 et versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="4c05a-103">Specifies whether assemblies loaded from remote sources should be granted full trust in .NET Framework 4 and later.</span></span>
  
> [!NOTE]
>  <span data-ttu-id="4c05a-104">Si vous avez été redirigé vers cet article en raison d’un message d’erreur dans la liste d’erreurs de projet Visual Studio ou une erreur de build, consultez [Comment : Utiliser un Assembly à partir du Web dans Visual Studio](https://docs.microsoft.com/previous-versions/visualstudio/visual-studio-2010/ee890038(v=vs.100)).</span><span class="sxs-lookup"><span data-stu-id="4c05a-104">If you were directed to this article because of an error message in the Visual Studio project error list or a build error, see [How to: Use an Assembly from the Web in Visual Studio](https://docs.microsoft.com/previous-versions/visualstudio/visual-studio-2010/ee890038(v=vs.100)).</span></span>  
  
 <span data-ttu-id="4c05a-105">\<configuration></span><span class="sxs-lookup"><span data-stu-id="4c05a-105">\<configuration></span></span>  
<span data-ttu-id="4c05a-106">\<runtime></span><span class="sxs-lookup"><span data-stu-id="4c05a-106">\<runtime></span></span>  
<span data-ttu-id="4c05a-107">\<loadFromRemoteSources></span><span class="sxs-lookup"><span data-stu-id="4c05a-107">\<loadFromRemoteSources></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="4c05a-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="4c05a-108">Syntax</span></span>  
  
```xml  
<loadFromRemoteSources    
   enabled="true|false"/>  
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="4c05a-109">Attributs et éléments</span><span class="sxs-lookup"><span data-stu-id="4c05a-109">Attributes and elements</span></span>
 <span data-ttu-id="4c05a-110">Les sections suivantes décrivent des attributs, des éléments enfants et des éléments parents.</span><span class="sxs-lookup"><span data-stu-id="4c05a-110">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="4c05a-111">Attributs</span><span class="sxs-lookup"><span data-stu-id="4c05a-111">Attributes</span></span>  
  
|<span data-ttu-id="4c05a-112">Attribut</span><span class="sxs-lookup"><span data-stu-id="4c05a-112">Attribute</span></span>|<span data-ttu-id="4c05a-113">Description</span><span class="sxs-lookup"><span data-stu-id="4c05a-113">Description</span></span>|  
|---------------|-----------------|  
|`enabled`|<span data-ttu-id="4c05a-114">Attribut requis.</span><span class="sxs-lookup"><span data-stu-id="4c05a-114">Required attribute.</span></span><br /><br /> <span data-ttu-id="4c05a-115">Spécifie si un assembly est chargé à partir d’une source distante doit être de confiance totale.</span><span class="sxs-lookup"><span data-stu-id="4c05a-115">Specifies whether an assembly that is loaded from a remote source should be granted full trust.</span></span>|  
  
## <a name="enabled-attribute"></a><span data-ttu-id="4c05a-116">attribut activé</span><span class="sxs-lookup"><span data-stu-id="4c05a-116">enabled attribute</span></span>  
  
|<span data-ttu-id="4c05a-117">Value</span><span class="sxs-lookup"><span data-stu-id="4c05a-117">Value</span></span>|<span data-ttu-id="4c05a-118">Description</span><span class="sxs-lookup"><span data-stu-id="4c05a-118">Description</span></span>|  
|-----------|-----------------|  
|`false`|<span data-ttu-id="4c05a-119">N’accordez pas une confiance totale aux applications à partir de sources distantes.</span><span class="sxs-lookup"><span data-stu-id="4c05a-119">Do not grant full trust to applications from remote sources.</span></span> <span data-ttu-id="4c05a-120">Il s'agit de la valeur par défaut.</span><span class="sxs-lookup"><span data-stu-id="4c05a-120">This is the default.</span></span>|  
|`true`|<span data-ttu-id="4c05a-121">Accorder une confiance totale aux applications à partir de sources distantes.</span><span class="sxs-lookup"><span data-stu-id="4c05a-121">Grant full trust to applications from remote sources.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="4c05a-122">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="4c05a-122">Child elements</span></span>  
 <span data-ttu-id="4c05a-123">Aucun.</span><span class="sxs-lookup"><span data-stu-id="4c05a-123">None.</span></span>  
  
### <a name="parent-elements"></a><span data-ttu-id="4c05a-124">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="4c05a-124">Parent elements</span></span>  
  
|<span data-ttu-id="4c05a-125">Élément</span><span class="sxs-lookup"><span data-stu-id="4c05a-125">Element</span></span>|<span data-ttu-id="4c05a-126">Description</span><span class="sxs-lookup"><span data-stu-id="4c05a-126">Description</span></span>|  
|-------------|-----------------|  
|`configuration`|<span data-ttu-id="4c05a-127">Élément racine de chaque fichier de configuration utilisé par le Common Language Runtime et les applications .NET Framework.</span><span class="sxs-lookup"><span data-stu-id="4c05a-127">The root element in every configuration file used by the common language runtime and .NET Framework applications.</span></span>|  
|`runtime`|<span data-ttu-id="4c05a-128">Contient des informations sur les options d'initialisation du runtime.</span><span class="sxs-lookup"><span data-stu-id="4c05a-128">Contains information about runtime initialization options.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="4c05a-129">Notes</span><span class="sxs-lookup"><span data-stu-id="4c05a-129">Remarks</span></span>

<span data-ttu-id="4c05a-130">Dans le .NET Framework 3.5 et les versions antérieures, si vous chargez un assembly à partir d’un emplacement distant, le code dans l’assembly s’exécute en confiance partielle avec un jeu d’autorisations qui dépend de la zone à partir de laquelle il est chargé.</span><span class="sxs-lookup"><span data-stu-id="4c05a-130">In the .NET Framework 3.5 and earlier versions, if you load an assembly from a remote location, code in the assembly runs in partial trust with a grant set that depends on the zone from which it is loaded.</span></span> <span data-ttu-id="4c05a-131">Par exemple, si vous chargez un assembly à partir d’un site Web, il est chargé dans la zone Internet et accordé le jeu d’autorisations Internet.</span><span class="sxs-lookup"><span data-stu-id="4c05a-131">For example, if you load an assembly from a website, it is loaded into the Internet zone and granted the Internet permission set.</span></span> <span data-ttu-id="4c05a-132">En d’autres termes, il s’exécute dans un bac à sable d’Internet.</span><span class="sxs-lookup"><span data-stu-id="4c05a-132">In other words, it executes in an Internet sandbox.</span></span>

<span data-ttu-id="4c05a-133">À compter de .NET Framework 4, la stratégie de sécurité (CA) d’accès au code est désactivée et les assemblys sont chargés avec une confiance totale.</span><span class="sxs-lookup"><span data-stu-id="4c05a-133">Starting with the .NET Framework 4, code access security (CAS) policy is disabled and assemblies are loaded in full trust.</span></span> <span data-ttu-id="4c05a-134">En règle générale, cela revient à accorder une confiance totale aux assemblys chargés avec le <xref:System.Reflection.Assembly.LoadFrom%2A?displayProperty=nameWithType> méthode avait été précédemment sandbox.</span><span class="sxs-lookup"><span data-stu-id="4c05a-134">Ordinarily, this would grant full trust to assemblies loaded with the <xref:System.Reflection.Assembly.LoadFrom%2A?displayProperty=nameWithType> method that previously had been sandboxed.</span></span> <span data-ttu-id="4c05a-135">Pour éviter ce problème, la possibilité d’exécuter du code dans les assemblys chargés à partir d’une source distante est désactivée par défaut.</span><span class="sxs-lookup"><span data-stu-id="4c05a-135">To prevent this, the ability to run code in assemblies loaded from a remote source is disabled by default.</span></span> <span data-ttu-id="4c05a-136">Par défaut, si vous essayez de charger un assembly distant, un <xref:System.IO.FileLoadException> avec un message d’exception, comme ce qui suit est levé :</span><span class="sxs-lookup"><span data-stu-id="4c05a-136">By default, if you attempt to load a remote assembly, a <xref:System.IO.FileLoadException> with an exception message like the following is thrown:</span></span>

```text
System.IO.FileNotFoundException: Could not load file or assembly 'file:assem.dll' or one of its dependencies. Operation is not supported. 
(Exception from HRESULT: 0x80131515)
File name: 'file:assem.dll' ---> 
System.NotSupportedException: An attempt was made to load an assembly from a network location which would have caused the assembly 
to be sandboxed in previous versions of the .NET Framework. This release of the .NET Framework does not enable CAS policy by default, 
so this load may be dangerous. If this load is not intended to sandbox the assembly, please enable the loadFromRemoteSources switch. 
```

<span data-ttu-id="4c05a-137">Pour charger l’assembly et exécuter son code, vous devez :</span><span class="sxs-lookup"><span data-stu-id="4c05a-137">To load the assembly and execute its code, you must either:</span></span>

- <span data-ttu-id="4c05a-138">Créer explicitement un bac à sable pour l’assembly (consultez [Comment : Exécuter le Code de confiance partiel dans un bac à sable](../../../../../docs/framework/misc/how-to-run-partially-trusted-code-in-a-sandbox.md)).</span><span class="sxs-lookup"><span data-stu-id="4c05a-138">Explicitly create a sandbox for the assembly (see [How to: Run Partially Trusted Code in a Sandbox](../../../../../docs/framework/misc/how-to-run-partially-trusted-code-in-a-sandbox.md)).</span></span>

- <span data-ttu-id="4c05a-139">Exécutez le code de l’assembly avec une confiance totale.</span><span class="sxs-lookup"><span data-stu-id="4c05a-139">Run the assembly's code in full trust.</span></span> <span data-ttu-id="4c05a-140">Pour cela, vous devez configurer le `<loadFromRemoteSources>` élément.</span><span class="sxs-lookup"><span data-stu-id="4c05a-140">You do this by configuring the `<loadFromRemoteSources>` element.</span></span> <span data-ttu-id="4c05a-141">Il vous permet de spécifier que les assemblys qui s’exécutent en confiance partielle dans les versions antérieures du .NET Framework s’exécutent maintenant en mode confiance totale dans le .NET Framework 4 et versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="4c05a-141">It lets you specify that the assemblies that run in partial trust in earlier versions of the .NET Framework now run in full trust in the .NET Framework 4 and later versions.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="4c05a-142">Si l’assembly ne doit pas s’exécuter en mode confiance totale, ne définissez pas cet élément de configuration.</span><span class="sxs-lookup"><span data-stu-id="4c05a-142">If the assembly should not run in full trust, do not set this configuration element.</span></span> <span data-ttu-id="4c05a-143">Au lieu de cela, créez un bac à sable <xref:System.AppDomain> dans lequel charger l’assembly.</span><span class="sxs-lookup"><span data-stu-id="4c05a-143">Instead, create a sandboxed <xref:System.AppDomain> in which to load the assembly.</span></span>

<span data-ttu-id="4c05a-144">Le `enabled` d’attribut pour le `<loadFromRemoteSources>` élément est efficace uniquement lorsque la sécurité d’accès de code (CAS) est désactivée.</span><span class="sxs-lookup"><span data-stu-id="4c05a-144">The `enabled` attribute for the `<loadFromRemoteSources>` element is effective only when code access security (CAS) is disabled.</span></span> <span data-ttu-id="4c05a-145">Par défaut, la stratégie CAS est désactivée dans le .NET Framework 4 et versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="4c05a-145">By default, CAS policy is disabled in the .NET Framework 4 and later versions.</span></span> <span data-ttu-id="4c05a-146">Si vous définissez `enabled` à `true`, une confiance totale est accordée aux assemblys à distance.</span><span class="sxs-lookup"><span data-stu-id="4c05a-146">If you set `enabled` to `true`, remote assemblies are granted full trust.</span></span>

<span data-ttu-id="4c05a-147">Si `enabled` n’a pas la valeur `true`, un <xref:System.IO.FileLoadException> est levée dans l’une des conditions suivantes :</span><span class="sxs-lookup"><span data-stu-id="4c05a-147">If `enabled` is not set to `true`, a <xref:System.IO.FileLoadException> is thrown under the either of the following conditions:</span></span>

- <span data-ttu-id="4c05a-148">Le comportement de bac à sable du domaine actuel est différent de son comportement dans le .NET Framework 3.5.</span><span class="sxs-lookup"><span data-stu-id="4c05a-148">The sandboxing behavior of the current domain is different from its behavior in the .NET Framework 3.5.</span></span> <span data-ttu-id="4c05a-149">Cela nécessite la stratégie CAS doit être désactivée et le domaine actuel ne pas à sable (sandbox).</span><span class="sxs-lookup"><span data-stu-id="4c05a-149">This requires CAS policy to be disabled, and the current domain not to be sandboxed.</span></span>

- <span data-ttu-id="4c05a-150">L’assembly en cours de chargement n’est pas à partir de la `MyComputer` zone.</span><span class="sxs-lookup"><span data-stu-id="4c05a-150">The assembly being loaded is not from the `MyComputer` zone.</span></span>

<span data-ttu-id="4c05a-151">Définition de la `<loadFromRemoteSources>` élément à `true` empêche cette exception ne soit levée.</span><span class="sxs-lookup"><span data-stu-id="4c05a-151">Setting the `<loadFromRemoteSources>` element to `true` prevents this exception from being thrown.</span></span> <span data-ttu-id="4c05a-152">Il vous permet de spécifier que vous ne comptez pas sur le common language runtime pour le bac à sable les assemblys chargés pour la sécurité, et qu’il peut être autorisé à exécuter dans une confiance totale.</span><span class="sxs-lookup"><span data-stu-id="4c05a-152">It enables you to specify that you are not relying on the common language runtime to sandbox the loaded assemblies for security, and that they can be allowed to execute in full trust.</span></span>

## <a name="notes"></a><span data-ttu-id="4c05a-153">Notes</span><span class="sxs-lookup"><span data-stu-id="4c05a-153">Notes</span></span>

- <span data-ttu-id="4c05a-154">Dans le .NET Framework 4.5 et les versions ultérieures, les assemblys sur des partages de réseau local s’exécutent en confiance totale par défaut ; vous n’avez pas à activer le `<loadFromRemoteSources>` élément.</span><span class="sxs-lookup"><span data-stu-id="4c05a-154">In the .NET Framework 4.5 and later versions, assemblies on local network shares run in full trust by default; you do not have to enable the `<loadFromRemoteSources>` element.</span></span>

- <span data-ttu-id="4c05a-155">Si une application a été copiée à partir du web, il est signalé par Windows comme étant une application web, même s’il se trouve sur l’ordinateur local.</span><span class="sxs-lookup"><span data-stu-id="4c05a-155">If an application has been copied from the web, it is flagged by Windows as being a web application, even if it resides on the local computer.</span></span> <span data-ttu-id="4c05a-156">Vous pouvez modifier cette désignation en modifiant ses propriétés de fichier, ou vous pouvez utiliser le `<loadFromRemoteSources>` élément à accorder à l’assembly de confiance totale.</span><span class="sxs-lookup"><span data-stu-id="4c05a-156">You can change that designation by changing its file properties, or you can use the `<loadFromRemoteSources>` element to grant the assembly full trust.</span></span> <span data-ttu-id="4c05a-157">Comme alternative, vous pouvez utiliser la <xref:System.Reflection.Assembly.UnsafeLoadFrom%2A> méthode pour charger un assembly local que le système d’exploitation a signalé comme ayant été chargé à partir du web.</span><span class="sxs-lookup"><span data-stu-id="4c05a-157">As an alternative, you can use the <xref:System.Reflection.Assembly.UnsafeLoadFrom%2A> method to load a local assembly that the operating system has flagged as having been loaded from the web.</span></span>

- <span data-ttu-id="4c05a-158">Vous risquez d’obtenir un <xref:System.IO.FileLoadException> dans une application qui s’exécute dans une application Windows Virtual PC.</span><span class="sxs-lookup"><span data-stu-id="4c05a-158">You may get a <xref:System.IO.FileLoadException> in an application that is running in a Windows Virtual PC application.</span></span> <span data-ttu-id="4c05a-159">Cela peut se produire lorsque vous essayez de charger un fichier à partir des dossiers liés sur l’ordinateur hôte.</span><span class="sxs-lookup"><span data-stu-id="4c05a-159">This can happen when you try to load a file from linked folders on the hosting computer.</span></span> <span data-ttu-id="4c05a-160">Il peut également se produire lorsque vous essayez de charger un fichier à partir d’un dossier lié au fil du [Services Bureau à distance](https://go.microsoft.com/fwlink/?LinkId=182775) (Terminal Services).</span><span class="sxs-lookup"><span data-stu-id="4c05a-160">It can also occur when you try to load a file from a folder linked over [Remote Desktop Services](https://go.microsoft.com/fwlink/?LinkId=182775) (Terminal Services).</span></span> <span data-ttu-id="4c05a-161">Pour éviter l’exception, définissez `enabled` à `true`.</span><span class="sxs-lookup"><span data-stu-id="4c05a-161">To avoid the exception, set `enabled` to `true`.</span></span>

## <a name="configuration-file"></a><span data-ttu-id="4c05a-162">fichier de configuration</span><span class="sxs-lookup"><span data-stu-id="4c05a-162">Configuration file</span></span>

<span data-ttu-id="4c05a-163">Cet élément est généralement utilisé dans le fichier de configuration d’application, mais il peut être utilisé dans d’autres fichiers de configuration selon le contexte.</span><span class="sxs-lookup"><span data-stu-id="4c05a-163">This element is typically used in the application configuration file, but can be used in other configuration files depending upon the context.</span></span> <span data-ttu-id="4c05a-164">Pour plus d’informations, consultez l’article [plus implicite utilise de stratégie CAS : loadFromRemoteSources](https://go.microsoft.com/fwlink/p/?LinkId=266839) dans le blog de sécurité .NET.</span><span class="sxs-lookup"><span data-stu-id="4c05a-164">For more information, see the article [More Implicit Uses of CAS Policy: loadFromRemoteSources](https://go.microsoft.com/fwlink/p/?LinkId=266839) in the .NET Security blog.</span></span>  

## <a name="example"></a><span data-ttu-id="4c05a-165">Exemple</span><span class="sxs-lookup"><span data-stu-id="4c05a-165">Example</span></span>

<span data-ttu-id="4c05a-166">L’exemple suivant montre comment accorder une confiance totale aux assemblys chargés à partir de sources distantes.</span><span class="sxs-lookup"><span data-stu-id="4c05a-166">The following example shows how to grant full trust to assemblies loaded from remote sources.</span></span>

```xml
<configuration>  
   <runtime>  
      <loadFromRemoteSources enabled="true"/>  
   </runtime>  
</configuration>  
```

## <a name="see-also"></a><span data-ttu-id="4c05a-167">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="4c05a-167">See also</span></span>

- [<span data-ttu-id="4c05a-168">Utilise plus implicite de stratégie CAS : loadFromRemoteSources</span><span class="sxs-lookup"><span data-stu-id="4c05a-168">More Implicit Uses of CAS Policy: loadFromRemoteSources</span></span>](https://go.microsoft.com/fwlink/p/?LinkId=266839)
- [<span data-ttu-id="4c05a-169">Guide pratique pour exécuter du code d’un niveau de confiance partiel dans un bac à sable (sandbox)</span><span class="sxs-lookup"><span data-stu-id="4c05a-169">How to: Run Partially Trusted Code in a Sandbox</span></span>](../../../../../docs/framework/misc/how-to-run-partially-trusted-code-in-a-sandbox.md)
- [<span data-ttu-id="4c05a-170">Schéma des paramètres d’exécution</span><span class="sxs-lookup"><span data-stu-id="4c05a-170">Runtime Settings Schema</span></span>](../../../../../docs/framework/configure-apps/file-schema/runtime/index.md)
- [<span data-ttu-id="4c05a-171">Schéma des fichiers de configuration</span><span class="sxs-lookup"><span data-stu-id="4c05a-171">Configuration File Schema</span></span>](../../../../../docs/framework/configure-apps/file-schema/index.md)
- <xref:System.Reflection.Assembly.LoadFrom%2A?displayProperty=nameWithType>
