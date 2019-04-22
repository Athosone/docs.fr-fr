---
title: -nostdlib (Visual Basic)
ms.date: 03/13/2018
helpviewer_keywords:
- nostdlib compiler option [Visual Basic]
- -nostdlib compiler option [Visual Basic]
- /nostdlib compiler option [Visual Basic]
ms.assetid: 140381b8-dc96-4ad5-ae11-792c9ed0be4d
ms.openlocfilehash: 4f3dc61a6e78b0fb2135d4132c53e7efc22447a2
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "58814979"
---
# <a name="-nostdlib-visual-basic"></a><span data-ttu-id="f5137-102">-nostdlib (Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="f5137-102">-nostdlib (Visual Basic)</span></span>
<span data-ttu-id="f5137-103">Indique au compilateur pour ne pas automatiquement de référencer les bibliothèques standards.</span><span class="sxs-lookup"><span data-stu-id="f5137-103">Causes the compiler not to automatically reference the standard libraries.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="f5137-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="f5137-104">Syntax</span></span>  
  
```  
-nostdlib  
```  
  
## <a name="remarks"></a><span data-ttu-id="f5137-105">Notes</span><span class="sxs-lookup"><span data-stu-id="f5137-105">Remarks</span></span>  
 <span data-ttu-id="f5137-106">Le `-nostdlib` option supprime la référence automatique à l’assembly System.dll et empêche le compilateur de lire le fichier Vbc.rsp.</span><span class="sxs-lookup"><span data-stu-id="f5137-106">The `-nostdlib` option removes the automatic reference to the System.dll assembly and prevents the compiler from reading the Vbc.rsp file.</span></span> <span data-ttu-id="f5137-107">Le fichier Vbc.rsp, qui se trouve dans le même répertoire que le fichier Vbc.exe, référence couramment utilisées [!INCLUDE[dnprdnshort](~/includes/dnprdnshort-md.md)] assemblys et des importations le `System` et `Microsoft.VisualBasic` espaces de noms.</span><span class="sxs-lookup"><span data-stu-id="f5137-107">The Vbc.rsp file, which is located in the same directory as the Vbc.exe file, references the commonly used [!INCLUDE[dnprdnshort](~/includes/dnprdnshort-md.md)] assemblies and imports the `System` and `Microsoft.VisualBasic` namespaces.</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="f5137-108">Les assemblys Mscorlib.dll et de Microsoft.VisualBasic.dll sont toujours référencés.</span><span class="sxs-lookup"><span data-stu-id="f5137-108">The Mscorlib.dll and Microsoft.VisualBasic.dll assemblies are always referenced.</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="f5137-109">Le `-nostdlib` option n’est pas disponible dans l’environnement de développement Visual Studio ; il est disponible uniquement lors de la compilation à partir de la ligne de commande.</span><span class="sxs-lookup"><span data-stu-id="f5137-109">The `-nostdlib` option is not available from within the Visual Studio development environment; it is available only when compiling from the command line.</span></span>  
  
## <a name="example"></a><span data-ttu-id="f5137-110">Exemple</span><span class="sxs-lookup"><span data-stu-id="f5137-110">Example</span></span>  
 <span data-ttu-id="f5137-111">Le code suivant compile `T2.vb` sans référencer les bibliothèques standards.</span><span class="sxs-lookup"><span data-stu-id="f5137-111">The following code compiles `T2.vb` without referencing the standard libraries.</span></span> <span data-ttu-id="f5137-112">Vous devez définir le `_MYTYPE` constante de compilation conditionnelle à la chaîne « Vide » si vous souhaitez supprimer le `My` objet.</span><span class="sxs-lookup"><span data-stu-id="f5137-112">You must set the `_MYTYPE` conditional-compilation constant to the string "Empty" to remove the `My` object.</span></span>  
  
```console
vbc -nostdlib -define:_MYTYPE=\"Empty\" T2.vb  
```  
  
## <a name="see-also"></a><span data-ttu-id="f5137-113">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f5137-113">See also</span></span>

- [<span data-ttu-id="f5137-114">-noconfig</span><span class="sxs-lookup"><span data-stu-id="f5137-114">-noconfig</span></span>](../../../visual-basic/reference/command-line-compiler/noconfig.md)
- [<span data-ttu-id="f5137-115">Compilateur de ligne de commande de Visual Basic</span><span class="sxs-lookup"><span data-stu-id="f5137-115">Visual Basic Command-Line Compiler</span></span>](../../../visual-basic/reference/command-line-compiler/index.md)
- [<span data-ttu-id="f5137-116">Exemples de lignes de commande de compilation</span><span class="sxs-lookup"><span data-stu-id="f5137-116">Sample Compilation Command Lines</span></span>](../../../visual-basic/reference/command-line-compiler/sample-compilation-command-lines.md)
- [<span data-ttu-id="f5137-117">Personnalisation de la disponibilité ou non des objets dans My</span><span class="sxs-lookup"><span data-stu-id="f5137-117">Customizing Which Objects are Available in My</span></span>](../../../visual-basic/developing-apps/customizing-extending-my/customizing-which-objects-are-available-in-my.md)
