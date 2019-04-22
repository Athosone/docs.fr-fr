---
title: -keycontainer
ms.date: 03/10/2018
helpviewer_keywords:
- -keycontainer compiler option [Visual Basic]
- keycontainer compiler option [Visual Basic]
- /keycontainer compiler option [Visual Basic]
ms.assetid: 6a9bc861-1752-4db1-9f64-b5252f0482cc
ms.openlocfilehash: 51cfe4a52af2fbcd51a4f9e2dc738e83fe0852c1
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "58839596"
---
# <a name="-keycontainer"></a><span data-ttu-id="23fe2-102">-keycontainer</span><span class="sxs-lookup"><span data-stu-id="23fe2-102">-keycontainer</span></span>
<span data-ttu-id="23fe2-103">Spécifie un nom de conteneur de clé pour une paire de clés afin d'attribuer un nom fort à un assembly.</span><span class="sxs-lookup"><span data-stu-id="23fe2-103">Specifies a key container name for a key pair to give an assembly a strong name.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="23fe2-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="23fe2-104">Syntax</span></span>  
  
```  
-keycontainer:container  
```  
  
## <a name="arguments"></a><span data-ttu-id="23fe2-105">Arguments</span><span class="sxs-lookup"><span data-stu-id="23fe2-105">Arguments</span></span>  
  
|<span data-ttu-id="23fe2-106">Terme</span><span class="sxs-lookup"><span data-stu-id="23fe2-106">Term</span></span>|<span data-ttu-id="23fe2-107">Définition</span><span class="sxs-lookup"><span data-stu-id="23fe2-107">Definition</span></span>|  
|---|---|  
|`container`|<span data-ttu-id="23fe2-108">Obligatoire.</span><span class="sxs-lookup"><span data-stu-id="23fe2-108">Required.</span></span> <span data-ttu-id="23fe2-109">Fichier conteneur qui contient la clé.</span><span class="sxs-lookup"><span data-stu-id="23fe2-109">Container file that contains the key.</span></span> <span data-ttu-id="23fe2-110">Placez le nom de fichier entre guillemets (" ») si le nom contient un espace.</span><span class="sxs-lookup"><span data-stu-id="23fe2-110">Enclose the file name in quotation marks ("") if the name contains a space.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="23fe2-111">Notes</span><span class="sxs-lookup"><span data-stu-id="23fe2-111">Remarks</span></span>  
 <span data-ttu-id="23fe2-112">Le compilateur crée le composant partageable en insérant une clé publique dans le manifeste d’assembly et en signant l’assembly final avec la clé privée.</span><span class="sxs-lookup"><span data-stu-id="23fe2-112">The compiler creates the sharable component by inserting a public key into the assembly manifest and by signing the final assembly with the private key.</span></span> <span data-ttu-id="23fe2-113">Pour générer un fichier de clé, tapez `sn -k file` à la ligne de commande.</span><span class="sxs-lookup"><span data-stu-id="23fe2-113">To generate a key file, type `sn -k file` at the command line.</span></span> <span data-ttu-id="23fe2-114">Le `-i` option installe la paire de clés dans un conteneur.</span><span class="sxs-lookup"><span data-stu-id="23fe2-114">The `-i` option installs the key pair into a container.</span></span> <span data-ttu-id="23fe2-115">Pour plus d’informations, consultez [Sn.exe (Strong Name Tool)](../../../framework/tools/sn-exe-strong-name-tool.md)).</span><span class="sxs-lookup"><span data-stu-id="23fe2-115">For more information, see [Sn.exe (Strong Name Tool)](../../../framework/tools/sn-exe-strong-name-tool.md)).</span></span>  
  
 <span data-ttu-id="23fe2-116">Si vous compilez avec `-target:module`, le nom du fichier de clé est conservé dans le module et incorporé dans l’assembly qui est créé lorsque vous compilez un assembly avec [- addmodule](../../../visual-basic/reference/command-line-compiler/addmodule.md).</span><span class="sxs-lookup"><span data-stu-id="23fe2-116">If you compile with `-target:module`, the name of the key file is held in the module and incorporated into the assembly that is created when you compile an assembly with [-addmodule](../../../visual-basic/reference/command-line-compiler/addmodule.md).</span></span>  
  
 <span data-ttu-id="23fe2-117">Vous pouvez également spécifier cette option comme attribut personnalisé (<xref:System.Reflection.AssemblyKeyNameAttribute>) dans le code source de n'importe quel module MSIL (Microsoft Intermediate Language).</span><span class="sxs-lookup"><span data-stu-id="23fe2-117">You can also specify this option as a custom attribute (<xref:System.Reflection.AssemblyKeyNameAttribute>) in the source code for any Microsoft intermediate language (MSIL) module.</span></span>  
  
 <span data-ttu-id="23fe2-118">Vous pouvez également passer vos informations de chiffrement au compilateur avec [-keyfile](../../../visual-basic/reference/command-line-compiler/keyfile.md).</span><span class="sxs-lookup"><span data-stu-id="23fe2-118">You can also pass your encryption information to the compiler with [-keyfile](../../../visual-basic/reference/command-line-compiler/keyfile.md).</span></span> <span data-ttu-id="23fe2-119">Utilisez [-delaysign](../../../visual-basic/reference/command-line-compiler/delaysign.md) si vous voulez obtenir un assembly partiellement signé.</span><span class="sxs-lookup"><span data-stu-id="23fe2-119">Use [-delaysign](../../../visual-basic/reference/command-line-compiler/delaysign.md) if you want a partially signed assembly.</span></span>  
  
 <span data-ttu-id="23fe2-120">Consultez [création et assemblys avec nom fort](../../../framework/app-domains/create-and-use-strong-named-assemblies.md) pour plus d’informations sur la signature d’un assembly.</span><span class="sxs-lookup"><span data-stu-id="23fe2-120">See [Creating and Using Strong-Named Assemblies](../../../framework/app-domains/create-and-use-strong-named-assemblies.md) for more information on signing an assembly.</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="23fe2-121">Le `-keycontainer` option n’est pas disponible dans l’environnement de développement Visual Studio ; il est disponible uniquement lors de la compilation à partir de la ligne de commande.</span><span class="sxs-lookup"><span data-stu-id="23fe2-121">The `-keycontainer` option is not available from within the Visual Studio development environment; it is available only when compiling from the command line.</span></span>  
  
## <a name="example"></a><span data-ttu-id="23fe2-122">Exemple</span><span class="sxs-lookup"><span data-stu-id="23fe2-122">Example</span></span>  
 <span data-ttu-id="23fe2-123">Le code suivant compile le fichier source `Input.vb` et spécifie un conteneur de clé.</span><span class="sxs-lookup"><span data-stu-id="23fe2-123">The following code compiles source file `Input.vb` and specifies a key container.</span></span>  
  
```  
vbc -keycontainer:key1 input.vb  
```  
  
## <a name="see-also"></a><span data-ttu-id="23fe2-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="23fe2-124">See also</span></span>

- [<span data-ttu-id="23fe2-125">Assemblys dans .NET</span><span class="sxs-lookup"><span data-stu-id="23fe2-125">Assemblies in .NET</span></span>](../../../standard/assembly/index.md)
- [<span data-ttu-id="23fe2-126">Compilateur de ligne de commande de Visual Basic</span><span class="sxs-lookup"><span data-stu-id="23fe2-126">Visual Basic Command-Line Compiler</span></span>](../../../visual-basic/reference/command-line-compiler/index.md)
- [<span data-ttu-id="23fe2-127">-keyfile</span><span class="sxs-lookup"><span data-stu-id="23fe2-127">-keyfile</span></span>](../../../visual-basic/reference/command-line-compiler/keyfile.md)
- [<span data-ttu-id="23fe2-128">Exemples de lignes de commande de compilation</span><span class="sxs-lookup"><span data-stu-id="23fe2-128">Sample Compilation Command Lines</span></span>](../../../visual-basic/reference/command-line-compiler/sample-compilation-command-lines.md)
