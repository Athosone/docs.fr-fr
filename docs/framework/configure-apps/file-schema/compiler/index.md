---
title: Schéma des paramètres du fournisseur de langage et du compilateur
ms.date: 03/30/2017
helpviewer_keywords:
  - 'configuration settings [.NET Framework], compilers'
  - 'compiler configuration elements, schema'
  - compiler configuration elements
  - language providers
  - 'compiler configuration settings, schema'
  - 'configuration schema [.NET Framework], compiler settings'
  - 'language providers, settings schema'
  - compiler configuration settings
ms.assetid: c020b139-8699-4f0d-9ac9-70d0c5b2a8c8
---
# <a name="compiler-and-language-provider-settings-schema"></a><span data-ttu-id="8d350-102">Schéma des paramètres du fournisseur de langage et du compilateur</span><span class="sxs-lookup"><span data-stu-id="8d350-102">Compiler and Language Provider Settings Schema</span></span>
<span data-ttu-id="8d350-103">Les paramètres du compilateur et du fournisseur de langage spécifient les éléments de configuration du compilateur pour les fournisseurs de langages disponibles.</span><span class="sxs-lookup"><span data-stu-id="8d350-103">Compiler and language provider settings specify compiler configuration elements for available language providers.</span></span> <span data-ttu-id="8d350-104">Chaque élément de configuration du compilateur spécifie le nom du type de fournisseur de code, les paramètres du compilateur, les noms des langages pris en charge et les extensions de fichier prises en charge.</span><span class="sxs-lookup"><span data-stu-id="8d350-104">Each compiler configuration element specifies the code provider type name, compiler parameters, supported language names, and supported file extensions.</span></span>  
  
 <span data-ttu-id="8d350-105">Le .NET Framework définit les paramètres de compilateur initiaux dans le fichier de configuration de l’ordinateur (Machine.config).</span><span class="sxs-lookup"><span data-stu-id="8d350-105">The .NET Framework defines the initial compiler settings in the machine configuration file (Machine.config).</span></span> <span data-ttu-id="8d350-106">Les développeurs et les éditeurs de compilateurs peuvent ajouter des paramètres de configuration pour une nouvelle implémentation <xref:System.CodeDom.Compiler.CodeDomProvider>.</span><span class="sxs-lookup"><span data-stu-id="8d350-106">Developers and compiler vendors can add configuration settings for a new <xref:System.CodeDom.Compiler.CodeDomProvider> implementation.</span></span> <span data-ttu-id="8d350-107">Utilisez la méthode <xref:System.CodeDom.Compiler.CodeDomProvider.GetAllCompilerInfo%2A?displayProperty=nameWithType> pour énumérer par programmation les paramètres de configuration du compilateur et du fournisseur de langage sur un ordinateur.</span><span class="sxs-lookup"><span data-stu-id="8d350-107">Use the <xref:System.CodeDom.Compiler.CodeDomProvider.GetAllCompilerInfo%2A?displayProperty=nameWithType> method to programmatically enumerate language provider and compiler configuration settings on a computer.</span></span>  
  
 [<span data-ttu-id="8d350-108">\<configuration>, élément</span><span class="sxs-lookup"><span data-stu-id="8d350-108">\<configuration> Element</span></span>](../../../../../docs/framework/configure-apps/file-schema/configuration-element.md)  
  
 [<span data-ttu-id="8d350-109">\<system.codedom></span><span class="sxs-lookup"><span data-stu-id="8d350-109">\<system.codedom></span></span>](../../../../../docs/framework/configure-apps/file-schema/compiler/system-codedom-element.md)  
  
 [<span data-ttu-id="8d350-110">\<compilers></span><span class="sxs-lookup"><span data-stu-id="8d350-110">\<compilers></span></span>](../../../../../docs/framework/configure-apps/file-schema/compiler/compilers-element.md)  
  
 [<span data-ttu-id="8d350-111">\<compiler></span><span class="sxs-lookup"><span data-stu-id="8d350-111">\<compiler></span></span>](../../../../../docs/framework/configure-apps/file-schema/compiler/compiler-element.md)  
  
|<span data-ttu-id="8d350-112">Élément</span><span class="sxs-lookup"><span data-stu-id="8d350-112">Element</span></span>|<span data-ttu-id="8d350-113">Description</span><span class="sxs-lookup"><span data-stu-id="8d350-113">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="8d350-114">\<system.codedom></span><span class="sxs-lookup"><span data-stu-id="8d350-114">\<system.codedom></span></span>](../../../../../docs/framework/configure-apps/file-schema/compiler/system-codedom-element.md)|<span data-ttu-id="8d350-115">Spécifie les paramètres de configuration du compilateur pour les fournisseurs de langages disponibles.</span><span class="sxs-lookup"><span data-stu-id="8d350-115">Specifies compiler configuration settings for available language providers.</span></span>|  
|[<span data-ttu-id="8d350-116">\<compilers></span><span class="sxs-lookup"><span data-stu-id="8d350-116">\<compilers></span></span>](../../../../../docs/framework/configure-apps/file-schema/compiler/compilers-element.md)|<span data-ttu-id="8d350-117">Conteneur des éléments de configuration du compilateur ; contient zéro ou plusieurs éléments [\<compiler>](../../../../../docs/framework/configure-apps/file-schema/compiler/compiler-element.md).</span><span class="sxs-lookup"><span data-stu-id="8d350-117">Container for compiler configuration elements; contains zero or more [\<compiler>](../../../../../docs/framework/configure-apps/file-schema/compiler/compiler-element.md) elements.</span></span>|  
|[<span data-ttu-id="8d350-118">\<compiler></span><span class="sxs-lookup"><span data-stu-id="8d350-118">\<compiler></span></span>](../../../../../docs/framework/configure-apps/file-schema/compiler/compiler-element.md)|<span data-ttu-id="8d350-119">Spécifie les attributs de configuration du compilateur pour un fournisseur de langage.</span><span class="sxs-lookup"><span data-stu-id="8d350-119">Specifies the compiler configuration attributes for a language provider.</span></span>|  
  
## <a name="example"></a><span data-ttu-id="8d350-120">Exemple</span><span class="sxs-lookup"><span data-stu-id="8d350-120">Example</span></span>  
 <span data-ttu-id="8d350-121">L’exemple suivant illustre un élément de configuration du compilateur classique.</span><span class="sxs-lookup"><span data-stu-id="8d350-121">The following example illustrates a typical compiler configuration element.</span></span>  
  
```xml  
<configuration>  
   <system.codedom>  
     <compilers>  
       <!-- zero or more compiler elements -->  
       <compiler  
          language="c#;cs;csharp"  
          extension=".cs"  
          type="Microsoft.CSharp.CSharpCodeProvider, System, Version=1.0.5000.0, Culture=neutral, PublicKeyToken=b77a5c561934e089"  
          compilerOptions=""  
          warningLevel="1" />  
     </compilers>  
   </system.codedom>  
</configuration>  
```  
  
## <a name="see-also"></a><span data-ttu-id="8d350-122">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="8d350-122">See also</span></span>

- <xref:System.CodeDom.Compiler.CompilerInfo>
- <xref:System.CodeDom.Compiler.CodeDomProvider>
- [<span data-ttu-id="8d350-123">Schéma des fichiers de configuration</span><span class="sxs-lookup"><span data-stu-id="8d350-123">Configuration File Schema</span></span>](../../../../../docs/framework/configure-apps/file-schema/index.md)
- [<span data-ttu-id="8d350-124">\<compiler> Element</span><span class="sxs-lookup"><span data-stu-id="8d350-124">\<compiler> Element</span></span>](../../../../../docs/framework/configure-apps/file-schema/compiler/compiler-element.md)
