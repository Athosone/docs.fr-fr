---
title: <system.codedom>, élément
ms.date: 03/30/2017
f1_keywords:
- http://schemas.microsoft.com/.NetConfiguration/v2.0#configuration/system.codedom
- http://schemas.microsoft.com/.NetConfiguration/v2.0#system.codedom
helpviewer_keywords:
- compiler configuration elements, <system.codedom> element
- system.codedom element
- <system.codedom> element
ms.assetid: 672a68f7-e69f-4479-ac30-e980085ec4fe
ms.openlocfilehash: 0f47255bb4073007a847e4a8b85ccfd34100582b
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59101612"
---
# <a name="systemcodedom-element"></a>\<System.CodeDom > élément
Spécifie les paramètres de configuration du compilateur pour les fournisseurs de langages disponibles.  
  
 \<configuration > élément  
\<System.CodeDom > élément  
  
## <a name="syntax"></a>Syntaxe  
  
```xml  
<system.codedom>  
  <compilers> ... </compilers>  
</system.codedom>  
```  
  
## <a name="attributes-and-elements"></a>Attributs et éléments  
 Les sections suivantes décrivent des attributs, des éléments enfants et des éléments parents.  
  
### <a name="attributes"></a>Attributs  
 Aucun.  
  
### <a name="child-elements"></a>Éléments enfants  
  
|Élément|Description|  
|-------------|-----------------|  
|[\<compilers>](../../../../../docs/framework/configure-apps/file-schema/compiler/compilers-element.md)|Conteneur des éléments de configuration du compilateur ; contient zéro ou plusieurs éléments [\<compiler>](../../../../../docs/framework/configure-apps/file-schema/compiler/compiler-element.md).|  
  
### <a name="parent-elements"></a>Éléments parents  
  
|Élément|Description|  
|-------------|-----------------|  
|[\<configuration>](../../../../../docs/framework/configure-apps/file-schema/configuration-element.md)|Élément racine de chaque fichier de configuration utilisé par le Common Language Runtime et les applications .NET Framework.|  
  
## <a name="remarks"></a>Notes  
  
## <a name="net-framework-version-20"></a>Version du .NET framework 2.0  
 Le [ \<system.codedom >](../../../../../docs/framework/configure-apps/file-schema/compiler/system-codedom-element.md) élément contient des paramètres de configuration de compilateur pour les fournisseurs de langages installés sur un ordinateur en plus les fournisseurs par défaut qui sont installés avec le .NET Framework, tel que le <xref:Microsoft.CSharp.CSharpCodeProvider> et <xref:Microsoft.VisualBasic.VBCodeProvider>. Le [ \<compilateurs >](../../../../../docs/framework/configure-apps/file-schema/compiler/compilers-element.md) élément contient zéro ou plusieurs [ \<compilateur >](../../../../../docs/framework/configure-apps/file-schema/compiler/compiler-element.md) éléments. Chaque [ \<compilateur >](../../../../../docs/framework/configure-apps/file-schema/compiler/compiler-element.md) élément spécifie les attributs de configuration du compilateur pour un fournisseur de langage spécifique.  
  
 Les développeurs et éditeurs de compilateurs peuvent ajouter des paramètres de configuration au fichier de configuration de l’ordinateur (Machine.config) pour une nouvelle <xref:System.CodeDom.Compiler.CodeDomProvider> implémentation. Utilisez le <xref:System.CodeDom.Compiler.CodeDomProvider.GetAllCompilerInfo%2A?displayProperty=nameWithType> méthode pour énumérer par programme les fournisseurs de langages par défaut et les fournisseurs de langages identifiés par les paramètres de configuration du compilateur sur un ordinateur.  
  
> [!NOTE]
>  Dans les versions de .NET Framework 1.0 et 1.1, la langue par défaut fournisseurs fournis par le .NET Framework sont identifiés dans le [ \<compilateurs >](../../../../../docs/framework/configure-apps/file-schema/compiler/compilers-element.md) élément. Dans le .NET Framework version 2.0, les fournisseurs de langage par défaut ne sont pas identifiées dans le [ \<compilateurs >](../../../../../docs/framework/configure-apps/file-schema/compiler/compilers-element.md) élément, mais peuvent être énumérés à l’aide de la <xref:System.CodeDom.Compiler.CodeDomProvider.GetAllCompilerInfo%2A> (méthode).  
  
## <a name="net-framework-versions-10-and-11"></a>Versions 1.0 et 1.1 du .NET framework  
 Le [ \<system.codedom >](../../../../../docs/framework/configure-apps/file-schema/compiler/system-codedom-element.md) élément contient les paramètres de configuration du compilateur pour les fournisseurs de langages sur un ordinateur. Le [ \<compilateurs >](../../../../../docs/framework/configure-apps/file-schema/compiler/compilers-element.md) élément contient zéro ou plusieurs [ \<compilateur >](../../../../../docs/framework/configure-apps/file-schema/compiler/compiler-element.md) éléments. Chaque [ \<compilateur >](../../../../../docs/framework/configure-apps/file-schema/compiler/compiler-element.md) élément spécifie les attributs de configuration du compilateur pour un fournisseur de langage spécifique.  
  
 Le .NET Framework définit les paramètres de compilateur initiaux dans le fichier de configuration de l’ordinateur (Machine.config). Les développeurs et les éditeurs de compilateurs peuvent ajouter des paramètres de configuration pour une nouvelle implémentation <xref:System.CodeDom.Compiler.CodeDomProvider>. Utilisez la méthode <xref:System.CodeDom.Compiler.CodeDomProvider.GetAllCompilerInfo%2A?displayProperty=nameWithType> pour énumérer par programmation les paramètres de configuration du compilateur et du fournisseur de langage sur un ordinateur.  
  
## <a name="configuration-file"></a>Fichier de configuration  
 Cet élément peut être utilisé dans le fichier de configuration machine et le fichier de configuration d’application.  
  
## <a name="example"></a>Exemple  
 L’exemple suivant illustre une configuration de compilateur classique.  
  
```xml  
<configuration>  
  <system.codedom>  
    <compilers>  
      <!-- zero or more compiler elements -->  
      <compiler   
        language="c#;cs;csharp"  
        extension=".cs"  
        type="Microsoft.CSharp.CSharpCodeProvider, System,   
          Version=1.0.5000.0, Culture=neutral,   
          PublicKeyToken=b77a5c561934e089"  
        compilerOptions=""  
        warningLevel="1" />  
    </compilers>  
  </system.codedom>  
</configuration>  
```  
  
## <a name="see-also"></a>Voir aussi

- <xref:System.CodeDom.Compiler.CompilerInfo>
- <xref:System.CodeDom.Compiler.CodeDomProvider>
- [Schéma des fichiers de configuration](../../../../../docs/framework/configure-apps/file-schema/index.md)
- [Schéma des paramètres du fournisseur de langage et du compilateur](../../../../../docs/framework/configure-apps/file-schema/compiler/index.md)
- [\<compiler> Element](../../../../../docs/framework/configure-apps/file-schema/compiler/compiler-element.md)
