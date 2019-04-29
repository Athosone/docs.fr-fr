---
title: -resource (Visual Basic)
ms.date: 03/13/2018
helpviewer_keywords:
- /resource compiler option [Visual Basic]
- -resource compiler option [Visual Basic]
- /res compiler option [Visual Basic]
- res compiler option [Visual Basic]
- -res compiler option [Visual Basic]
- resource compiler option [Visual Basic]
ms.assetid: eee2f227-91f2-4f2b-a9d6-1c51c5320858
ms.openlocfilehash: 46122eaa7ca54679c9a52b939f9100c9a0747e7b
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61639084"
---
# <a name="-resource-visual-basic"></a><span data-ttu-id="09581-102">-resource (Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="09581-102">-resource (Visual Basic)</span></span>
<span data-ttu-id="09581-103">Incorpore une ressource managée dans un assembly.</span><span class="sxs-lookup"><span data-stu-id="09581-103">Embeds a managed resource in an assembly.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="09581-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="09581-104">Syntax</span></span>  
  
```  
-resource:filename[,identifier[,public|private]]  
' -or-  
-res:filename[,identifier[,public|private]]  
```  
  
## <a name="arguments"></a><span data-ttu-id="09581-105">Arguments</span><span class="sxs-lookup"><span data-stu-id="09581-105">Arguments</span></span>  
  
|<span data-ttu-id="09581-106">Terme</span><span class="sxs-lookup"><span data-stu-id="09581-106">Term</span></span>|<span data-ttu-id="09581-107">Définition</span><span class="sxs-lookup"><span data-stu-id="09581-107">Definition</span></span>|  
|---|---|  
|`filename`|<span data-ttu-id="09581-108">Obligatoire.</span><span class="sxs-lookup"><span data-stu-id="09581-108">Required.</span></span> <span data-ttu-id="09581-109">Le nom du fichier de ressources à incorporer dans le fichier de sortie.</span><span class="sxs-lookup"><span data-stu-id="09581-109">The name of the resource file to embed in the output file.</span></span> <span data-ttu-id="09581-110">Par défaut, `filename` est public dans l’assembly.</span><span class="sxs-lookup"><span data-stu-id="09581-110">By default, `filename` is public in the assembly.</span></span> <span data-ttu-id="09581-111">Placez le nom de fichier entre guillemets ( » «) s’il contient un espace.</span><span class="sxs-lookup"><span data-stu-id="09581-111">Enclose the file name in quotation marks (" ") if it contains a space.</span></span>|  
|`identifier`|<span data-ttu-id="09581-112">Facultatif.</span><span class="sxs-lookup"><span data-stu-id="09581-112">Optional.</span></span> <span data-ttu-id="09581-113">Le nom logique de la ressource ; nom utilisé pour le charger.</span><span class="sxs-lookup"><span data-stu-id="09581-113">The logical name for the resource; the name used to load it.</span></span> <span data-ttu-id="09581-114">La valeur par défaut est le nom du fichier.</span><span class="sxs-lookup"><span data-stu-id="09581-114">The default is the name of the file.</span></span> <span data-ttu-id="09581-115">Si vous le souhaitez, vous pouvez spécifier si la ressource est publique ou privée dans le manifeste d’assembly, comme avec les éléments suivants : `-res:filename.res, myname.res, public`</span><span class="sxs-lookup"><span data-stu-id="09581-115">Optionally, you can specify whether the resource is public or private in the assembly manifest, as with the following: `-res:filename.res, myname.res, public`</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="09581-116">Notes</span><span class="sxs-lookup"><span data-stu-id="09581-116">Remarks</span></span>  
 <span data-ttu-id="09581-117">Utilisez `-linkresource` pour lier une ressource à un assembly sans placer le fichier de ressources dans le fichier de sortie.</span><span class="sxs-lookup"><span data-stu-id="09581-117">Use `-linkresource` to link a resource to an assembly without placing the resource file in the output file.</span></span>  
  
 <span data-ttu-id="09581-118">Si `filename` est un [!INCLUDE[dnprdnshort](~/includes/dnprdnshort-md.md)] fichier de ressources créé, par exemple, par le [Resgen.exe (Resource File Generator)](../../../framework/tools/resgen-exe-resource-file-generator.md) ou dans l’environnement de développement, il est accessible à l’aide des membres de la <xref:System.Resources> (voir del’espacedenoms<xref:System.Resources.ResourceManager> pour plus d’informations).</span><span class="sxs-lookup"><span data-stu-id="09581-118">If `filename` is a [!INCLUDE[dnprdnshort](~/includes/dnprdnshort-md.md)] resource file created, for example, by the [Resgen.exe (Resource File Generator)](../../../framework/tools/resgen-exe-resource-file-generator.md) or in the development environment, it can be accessed with members in the <xref:System.Resources> namespace (see <xref:System.Resources.ResourceManager> for more information).</span></span> <span data-ttu-id="09581-119">Pour accéder à toutes les autres ressources au moment de l’exécution, utilisez une des méthodes suivantes : <xref:System.Reflection.Assembly.GetManifestResourceInfo%2A>, <xref:System.Reflection.Assembly.GetManifestResourceNames%2A>, ou <xref:System.Reflection.Assembly.GetManifestResourceStream%2A>.</span><span class="sxs-lookup"><span data-stu-id="09581-119">To access all other resources at run time, use one of the following methods: <xref:System.Reflection.Assembly.GetManifestResourceInfo%2A>, <xref:System.Reflection.Assembly.GetManifestResourceNames%2A>, or <xref:System.Reflection.Assembly.GetManifestResourceStream%2A>.</span></span>  
  
 <span data-ttu-id="09581-120">La forme abrégée de `-resource` est `-res`.</span><span class="sxs-lookup"><span data-stu-id="09581-120">The short form of `-resource` is `-res`.</span></span>  
  
 <span data-ttu-id="09581-121">Pour plus d’informations sur la définition `-resource` dans l’IDE de Visual Studio, consultez [gestion des ressources Application (.NET)](/visualstudio/ide/managing-application-resources-dotnet).</span><span class="sxs-lookup"><span data-stu-id="09581-121">For information about how to set `-resource` in the Visual Studio IDE, see [Managing Application Resources (.NET)](/visualstudio/ide/managing-application-resources-dotnet).</span></span>  
  
## <a name="example"></a><span data-ttu-id="09581-122">Exemple</span><span class="sxs-lookup"><span data-stu-id="09581-122">Example</span></span>  
 <span data-ttu-id="09581-123">Le code suivant compile `In.vb` et le fichier de ressources attache `Rf.resource`.</span><span class="sxs-lookup"><span data-stu-id="09581-123">The following code compiles `In.vb` and attaches resource file `Rf.resource`.</span></span>  
  
```console
vbc -res:rf.resource in.vb  
```  
  
## <a name="see-also"></a><span data-ttu-id="09581-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="09581-124">See also</span></span>

- [<span data-ttu-id="09581-125">Compilateur de ligne de commande de Visual Basic</span><span class="sxs-lookup"><span data-stu-id="09581-125">Visual Basic Command-Line Compiler</span></span>](../../../visual-basic/reference/command-line-compiler/index.md)
- [<span data-ttu-id="09581-126">-win32resource</span><span class="sxs-lookup"><span data-stu-id="09581-126">-win32resource</span></span>](../../../visual-basic/reference/command-line-compiler/win32resource.md)
- [<span data-ttu-id="09581-127">-linkresource (Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="09581-127">-linkresource (Visual Basic)</span></span>](../../../visual-basic/reference/command-line-compiler/linkresource.md)
- [<span data-ttu-id="09581-128">-target (Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="09581-128">-target (Visual Basic)</span></span>](../../../visual-basic/reference/command-line-compiler/target.md)
- [<span data-ttu-id="09581-129">Exemples de lignes de commande de compilation</span><span class="sxs-lookup"><span data-stu-id="09581-129">Sample Compilation Command Lines</span></span>](../../../visual-basic/reference/command-line-compiler/sample-compilation-command-lines.md)
