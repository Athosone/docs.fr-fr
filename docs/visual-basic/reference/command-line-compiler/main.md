---
title: -main
ms.date: 03/13/2018
helpviewer_keywords:
- main compiler option [Visual Basic]
- /main compiler option [Visual Basic]
- -main compiler option [Visual Basic]
ms.assetid: 83fc339d-6652-415d-b205-b5133319b5b0
ms.openlocfilehash: fd6240faf702ccb5e543bfd6a7779284f38d8850
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61793911"
---
# <a name="-main"></a><span data-ttu-id="7642a-102">-main</span><span class="sxs-lookup"><span data-stu-id="7642a-102">-main</span></span>
<span data-ttu-id="7642a-103">Spécifie la classe ou le module qui contient la procédure `Sub Main`.</span><span class="sxs-lookup"><span data-stu-id="7642a-103">Specifies the class or module that contains the `Sub Main` procedure.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="7642a-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="7642a-104">Syntax</span></span>  
  
```  
-main:location  
```  
  
## <a name="arguments"></a><span data-ttu-id="7642a-105">Arguments</span><span class="sxs-lookup"><span data-stu-id="7642a-105">Arguments</span></span>  
 `location`  
 <span data-ttu-id="7642a-106">Obligatoire.</span><span class="sxs-lookup"><span data-stu-id="7642a-106">Required.</span></span> <span data-ttu-id="7642a-107">Le nom de la classe ou le module qui contient le `Sub Main` procédure à appeler lorsque le programme démarre.</span><span class="sxs-lookup"><span data-stu-id="7642a-107">The name of the class or module that contains the `Sub Main` procedure to be called when the program starts.</span></span> <span data-ttu-id="7642a-108">Cela peut être sous la forme **-module : principal** ou **-main:namespace.module**.</span><span class="sxs-lookup"><span data-stu-id="7642a-108">This may be in the form **-main:module** or **-main:namespace.module**.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="7642a-109">Notes</span><span class="sxs-lookup"><span data-stu-id="7642a-109">Remarks</span></span>  
 <span data-ttu-id="7642a-110">Utilisez cette option lorsque vous créez un fichier exécutable ou un programme exécutable Windows.</span><span class="sxs-lookup"><span data-stu-id="7642a-110">Use this option when you create an executable file or Windows executable program.</span></span> <span data-ttu-id="7642a-111">Si le **-principal** option est omise, le compilateur recherche les valide partagé `Sub Main` dans tous les modules et les classes publiques.</span><span class="sxs-lookup"><span data-stu-id="7642a-111">If the **-main** option is omitted, the compiler searches for a valid shared `Sub Main` in all public classes and modules.</span></span>  
  
 <span data-ttu-id="7642a-112">Consultez [procédure Main dans Visual Basic](../../../visual-basic/programming-guide/program-structure/main-procedure.md) pour une description des différentes formes de la `Main` procédure.</span><span class="sxs-lookup"><span data-stu-id="7642a-112">See [Main Procedure in Visual Basic](../../../visual-basic/programming-guide/program-structure/main-procedure.md) for a discussion of the various forms of the `Main` procedure.</span></span>  
  
 <span data-ttu-id="7642a-113">Lorsque `location` est une classe qui hérite de <xref:System.Windows.Forms.Form>, le compilateur fournit une valeur par défaut `Main` procédure qui démarre l’application si la classe n’a pas `Main` procédure.</span><span class="sxs-lookup"><span data-stu-id="7642a-113">When `location` is a class that inherits from <xref:System.Windows.Forms.Form>, the compiler provides a default `Main` procedure that starts the application if the class has no `Main` procedure.</span></span> <span data-ttu-id="7642a-114">Cela vous permet de compiler du code à la ligne de commande qui a été créée dans l’environnement de développement.</span><span class="sxs-lookup"><span data-stu-id="7642a-114">This lets you compile code at the command line that was created in the development environment.</span></span>  
  
 [!code-vb[VbVbalrCompiler#16](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbalrCompiler/VB/Class1.vb#16)]  
  
### <a name="to-set--main-in-the-visual-studio-integrated-development-environment"></a><span data-ttu-id="7642a-115">Pour définir - main dans l’environnement de développement intégré Visual Studio</span><span class="sxs-lookup"><span data-stu-id="7642a-115">To set -main in the Visual Studio integrated development environment</span></span>  
  
1. <span data-ttu-id="7642a-116">Sélectionnez un projet dans l' **Explorateur de solutions**.</span><span class="sxs-lookup"><span data-stu-id="7642a-116">Have a project selected in **Solution Explorer**.</span></span> <span data-ttu-id="7642a-117">Dans le menu **Projet**, cliquez sur **Propriétés**.</span><span class="sxs-lookup"><span data-stu-id="7642a-117">On the **Project** menu, click **Properties**.</span></span>  
  
2. <span data-ttu-id="7642a-118">Cliquez sur l’onglet **Application** .</span><span class="sxs-lookup"><span data-stu-id="7642a-118">Click the **Application** tab.</span></span>  
  
3. <span data-ttu-id="7642a-119">Assurez-vous que le **activer l’infrastructure application** case à cocher n’est pas activée.</span><span class="sxs-lookup"><span data-stu-id="7642a-119">Make sure the **Enable application framework** check box is not checked.</span></span>  
  
4. <span data-ttu-id="7642a-120">Modifiez la valeur dans le **objet de démarrage** boîte.</span><span class="sxs-lookup"><span data-stu-id="7642a-120">Modify the value in the **Startup object** box.</span></span>  
  
## <a name="example"></a><span data-ttu-id="7642a-121">Exemple</span><span class="sxs-lookup"><span data-stu-id="7642a-121">Example</span></span>  
 <span data-ttu-id="7642a-122">Le code suivant compile `T2.vb` et `T3.vb`, en spécifiant que le `Sub Main` procédure se trouve dans le `Test2` classe.</span><span class="sxs-lookup"><span data-stu-id="7642a-122">The following code compiles `T2.vb` and `T3.vb`, specifying that the `Sub Main` procedure will be found in the `Test2` class.</span></span>  
  
```console
vbc t2.vb t3.vb -main:Test2  
```  
  
## <a name="see-also"></a><span data-ttu-id="7642a-123">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="7642a-123">See also</span></span>

- [<span data-ttu-id="7642a-124">Compilateur de ligne de commande de Visual Basic</span><span class="sxs-lookup"><span data-stu-id="7642a-124">Visual Basic Command-Line Compiler</span></span>](../../../visual-basic/reference/command-line-compiler/index.md)
- [<span data-ttu-id="7642a-125">-target (Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="7642a-125">-target (Visual Basic)</span></span>](../../../visual-basic/reference/command-line-compiler/target.md)
- [<span data-ttu-id="7642a-126">Exemples de lignes de commande de compilation</span><span class="sxs-lookup"><span data-stu-id="7642a-126">Sample Compilation Command Lines</span></span>](../../../visual-basic/reference/command-line-compiler/sample-compilation-command-lines.md)
- [<span data-ttu-id="7642a-127">Procédure Main dans Visual Basic</span><span class="sxs-lookup"><span data-stu-id="7642a-127">Main Procedure in Visual Basic</span></span>](../../../visual-basic/programming-guide/program-structure/main-procedure.md)
