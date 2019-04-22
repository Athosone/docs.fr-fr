---
title: -importe (Visual Basic)
ms.date: 03/10/2018
helpviewer_keywords:
- /imports compiler option [Visual Basic]
- imports compiler option [Visual Basic]
- -imports compiler option [Visual Basic]
ms.assetid: 9a93fb53-c080-497b-bf9b-441022dbbc39
ms.openlocfilehash: 075eeccc7d80943d2757a97b9a355bbea3ef9d4e
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "58833605"
---
# <a name="-imports-visual-basic"></a><span data-ttu-id="d944c-102">-importe (Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="d944c-102">-imports (Visual Basic)</span></span>
<span data-ttu-id="d944c-103">Importe des espaces de noms à partir d’un assembly spécifié.</span><span class="sxs-lookup"><span data-stu-id="d944c-103">Imports namespaces from a specified assembly.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="d944c-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="d944c-104">Syntax</span></span>  
  
```  
-imports:namespaceList  
```  
  
## <a name="arguments"></a><span data-ttu-id="d944c-105">Arguments</span><span class="sxs-lookup"><span data-stu-id="d944c-105">Arguments</span></span>  
  
|<span data-ttu-id="d944c-106">Terme</span><span class="sxs-lookup"><span data-stu-id="d944c-106">Term</span></span>|<span data-ttu-id="d944c-107">Définition</span><span class="sxs-lookup"><span data-stu-id="d944c-107">Definition</span></span>|  
|---|---|  
|`namespaceList`|<span data-ttu-id="d944c-108">Obligatoire.</span><span class="sxs-lookup"><span data-stu-id="d944c-108">Required.</span></span> <span data-ttu-id="d944c-109">Liste délimitée par des virgules des espaces de noms à importer.</span><span class="sxs-lookup"><span data-stu-id="d944c-109">Comma-delimited list of namespaces to be imported.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="d944c-110">Notes</span><span class="sxs-lookup"><span data-stu-id="d944c-110">Remarks</span></span>  
 <span data-ttu-id="d944c-111">Le `-imports` option importe n’importe quel espace de noms défini dans l’ensemble des fichiers sources ou à partir de n’importe quel assembly référencé actuel.</span><span class="sxs-lookup"><span data-stu-id="d944c-111">The `-imports` option imports any namespace defined within the current set of source files or from any referenced assembly.</span></span>  
  
 <span data-ttu-id="d944c-112">Les membres dans un espace de noms spécifiés avec `-imports` sont disponibles pour tous les fichiers de code source dans la compilation.</span><span class="sxs-lookup"><span data-stu-id="d944c-112">The members in a namespace specified with `-imports` are available to all source-code files in the compilation.</span></span> <span data-ttu-id="d944c-113">Utiliser le [instruction Imports (.NET Namespace et Type)](../../../visual-basic/language-reference/statements/imports-statement-net-namespace-and-type.md) à utiliser un espace de noms dans un fichier de code source unique.</span><span class="sxs-lookup"><span data-stu-id="d944c-113">Use the [Imports Statement (.NET Namespace and Type)](../../../visual-basic/language-reference/statements/imports-statement-net-namespace-and-type.md) to use a namespace in a single source-code file.</span></span>  
  
|<span data-ttu-id="d944c-114">Pour définir /Imports dans l’environnement de développement intégré Visual Studio</span><span class="sxs-lookup"><span data-stu-id="d944c-114">To set /imports in the Visual Studio integrated development environment</span></span>|  
|---|  
|<span data-ttu-id="d944c-115">1.  Sélectionnez un projet dans l' **Explorateur de solutions**.</span><span class="sxs-lookup"><span data-stu-id="d944c-115">1.  Have a project selected in **Solution Explorer**.</span></span> <span data-ttu-id="d944c-116">Dans le menu **Projet**, cliquez sur **Propriétés**.</span><span class="sxs-lookup"><span data-stu-id="d944c-116">On the **Project** menu, click **Properties**.</span></span> <br /><span data-ttu-id="d944c-117">2.  Cliquez sur l’onglet **Références**.</span><span class="sxs-lookup"><span data-stu-id="d944c-117">2.  Click the **References** tab.</span></span><br /><span data-ttu-id="d944c-118">3.  Entrez le nom de l’espace de noms dans la zone en regard de la **ajouter une importation utilisateur** bouton.</span><span class="sxs-lookup"><span data-stu-id="d944c-118">3.  Enter the namespace name in the box beside the **Add User Import** button.</span></span><br /><span data-ttu-id="d944c-119">4.  Cliquez sur le **ajouter une importation utilisateur** bouton.</span><span class="sxs-lookup"><span data-stu-id="d944c-119">4.  Click the **Add User Import** button.</span></span>|  
  
## <a name="example"></a><span data-ttu-id="d944c-120">Exemple</span><span class="sxs-lookup"><span data-stu-id="d944c-120">Example</span></span>  
 <span data-ttu-id="d944c-121">Le code suivant compile si `/imports:system.globalization` est spécifié.</span><span class="sxs-lookup"><span data-stu-id="d944c-121">The following code compiles when `/imports:system.globalization` is specified.</span></span> <span data-ttu-id="d944c-122">Sans cela, de compilation réussie nécessite qu’un `Imports System.Globalization` instruction inclus au début du fichier de code source ou que la propriété être qualifié en tant que `System.Globalization.CultureInfo.CurrentCulture.Name`.</span><span class="sxs-lookup"><span data-stu-id="d944c-122">Without it, successful compilation requires either that an `Imports System.Globalization` statement be included at the beginning of the source code file, or that the property be fully qualified as `System.Globalization.CultureInfo.CurrentCulture.Name`.</span></span>

```vb
Module Example
   Public Sub Main()
      Console.WriteLine($"The current culture is {CultureInfo.CurrentCulture.Name}")
   End Sub
End Module
```

## <a name="see-also"></a><span data-ttu-id="d944c-123">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d944c-123">See also</span></span>

- [<span data-ttu-id="d944c-124">Compilateur de ligne de commande de Visual Basic</span><span class="sxs-lookup"><span data-stu-id="d944c-124">Visual Basic Command-Line Compiler</span></span>](../../../visual-basic/reference/command-line-compiler/index.md)
- [<span data-ttu-id="d944c-125">Références et l’instruction Imports</span><span class="sxs-lookup"><span data-stu-id="d944c-125">References and the Imports Statement</span></span>](../../../visual-basic/programming-guide/program-structure/references-and-the-imports-statement.md)
- [<span data-ttu-id="d944c-126">Exemples de lignes de commande de compilation</span><span class="sxs-lookup"><span data-stu-id="d944c-126">Sample Compilation Command Lines</span></span>](../../../visual-basic/reference/command-line-compiler/sample-compilation-command-lines.md)
