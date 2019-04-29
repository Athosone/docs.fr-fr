---
title: -rootnamespace
ms.date: 03/13/2018
f1_keywords:
- /rootnamespace
- rootnamespace
helpviewer_keywords:
- /rootnamespace compiler option [Visual Basic]
- -rootnamespace compiler option [Visual Basic]
- rootnamespace compiler option [Visual Basic]
ms.assetid: e9245edf-6bef-420d-a7c7-324117752783
ms.openlocfilehash: ff4b1729f1b9fb1d698b4b5b1e3711ce3d27b4db
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61639033"
---
# <a name="-rootnamespace"></a><span data-ttu-id="0a7bc-102">-rootnamespace</span><span class="sxs-lookup"><span data-stu-id="0a7bc-102">-rootnamespace</span></span>
<span data-ttu-id="0a7bc-103">Spécifie un espace de noms pour toutes les déclarations de type.</span><span class="sxs-lookup"><span data-stu-id="0a7bc-103">Specifies a namespace for all type declarations.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="0a7bc-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="0a7bc-104">Syntax</span></span>  
  
```  
-rootnamespace:namespace  
```  
  
## <a name="arguments"></a><span data-ttu-id="0a7bc-105">Arguments</span><span class="sxs-lookup"><span data-stu-id="0a7bc-105">Arguments</span></span>  
  
|<span data-ttu-id="0a7bc-106">Terme</span><span class="sxs-lookup"><span data-stu-id="0a7bc-106">Term</span></span>|<span data-ttu-id="0a7bc-107">Définition</span><span class="sxs-lookup"><span data-stu-id="0a7bc-107">Definition</span></span>|  
|---|---|  
|`namespace`|<span data-ttu-id="0a7bc-108">Le nom de l’espace de noms dans lequel encadrer toutes les déclarations de type pour le projet actuel.</span><span class="sxs-lookup"><span data-stu-id="0a7bc-108">The name of the namespace in which to enclose all type declarations for the current project.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="0a7bc-109">Notes</span><span class="sxs-lookup"><span data-stu-id="0a7bc-109">Remarks</span></span>  
 <span data-ttu-id="0a7bc-110">Si vous utilisez le fichier exécutable de Visual Studio (Devenv.exe) pour compiler un projet créé dans l’environnement de développement intégré Visual Studio, utilisez `-rootnamespace` pour spécifier la valeur de la <xref:VSLangProj80.VBProjectProperties3.RootNamespace%2A> propriété.</span><span class="sxs-lookup"><span data-stu-id="0a7bc-110">If you use the Visual Studio executable file (Devenv.exe) to compile a project created in the Visual Studio integrated development environment, use `-rootnamespace` to specify the value of the <xref:VSLangProj80.VBProjectProperties3.RootNamespace%2A> property.</span></span> <span data-ttu-id="0a7bc-111">Consultez [commutateurs de ligne de commande Devenv](/visualstudio/ide/reference/devenv-command-line-switches) pour plus d’informations.</span><span class="sxs-lookup"><span data-stu-id="0a7bc-111">See [Devenv Command Line Switches](/visualstudio/ide/reference/devenv-command-line-switches) for more information.</span></span>  
  
 <span data-ttu-id="0a7bc-112">Utiliser le common language runtime MSIL Disassembler (`Ildasm.exe`) pour afficher les noms d’espace de noms dans votre fichier de sortie.</span><span class="sxs-lookup"><span data-stu-id="0a7bc-112">Use the common language runtime MSIL Disassembler (`Ildasm.exe`) to view the namespace names in your output file.</span></span>  
  
|<span data-ttu-id="0a7bc-113">Pour définir - rootnamespace dans l’environnement de développement intégré Visual Studio</span><span class="sxs-lookup"><span data-stu-id="0a7bc-113">To set -rootnamespace in the Visual Studio integrated development environment</span></span>|  
|---|  
|<span data-ttu-id="0a7bc-114">1.  Sélectionnez un projet dans l' **Explorateur de solutions**.</span><span class="sxs-lookup"><span data-stu-id="0a7bc-114">1.  Have a project selected in **Solution Explorer**.</span></span> <span data-ttu-id="0a7bc-115">Dans le menu **Projet**, cliquez sur **Propriétés**.</span><span class="sxs-lookup"><span data-stu-id="0a7bc-115">On the **Project** menu, click **Properties**.</span></span> <br /><span data-ttu-id="0a7bc-116">2.  Cliquez sur l’onglet **Application** .</span><span class="sxs-lookup"><span data-stu-id="0a7bc-116">2.  Click the **Application** tab.</span></span><br /><span data-ttu-id="0a7bc-117">3.  Modifiez la valeur dans le **racine Namespace** boîte.</span><span class="sxs-lookup"><span data-stu-id="0a7bc-117">3.  Modify the value in the **Root Namespace** box.</span></span>|  
  
## <a name="example"></a><span data-ttu-id="0a7bc-118">Exemple</span><span class="sxs-lookup"><span data-stu-id="0a7bc-118">Example</span></span>  
 <span data-ttu-id="0a7bc-119">Le code suivant compile `In.vb` et englobe toutes les déclarations de type dans l’espace de noms `mynamespace`.</span><span class="sxs-lookup"><span data-stu-id="0a7bc-119">The following code compiles `In.vb` and encloses all type declarations in the namespace `mynamespace`.</span></span>  
  
```console
vbc -rootnamespace:mynamespace in.vb  
```  
  
## <a name="see-also"></a><span data-ttu-id="0a7bc-120">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0a7bc-120">See also</span></span>

- [<span data-ttu-id="0a7bc-121">Compilateur de ligne de commande de Visual Basic</span><span class="sxs-lookup"><span data-stu-id="0a7bc-121">Visual Basic Command-Line Compiler</span></span>](../../../visual-basic/reference/command-line-compiler/index.md)
- [<span data-ttu-id="0a7bc-122">Ildasm.exe (désassembleur IL)</span><span class="sxs-lookup"><span data-stu-id="0a7bc-122">Ildasm.exe (IL Disassembler)</span></span>](../../../framework/tools/ildasm-exe-il-disassembler.md)
- [<span data-ttu-id="0a7bc-123">Exemples de lignes de commande de compilation</span><span class="sxs-lookup"><span data-stu-id="0a7bc-123">Sample Compilation Command Lines</span></span>](../../../visual-basic/reference/command-line-compiler/sample-compilation-command-lines.md)
