---
title: -netcf
ms.date: 03/13/2018
f1_keywords:
- /netcf
- -netcf
helpviewer_keywords:
- -netcf compiler option [Visual Basic]
- netcf compiler option [Visual Basic]
- /netcf compiler option [Visual Basic]
ms.assetid: db7cfa59-c315-401c-a59b-0daf355343d6
ms.openlocfilehash: d7c3bcba8e62d62904ed778a48d0e8ae6738ce00
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59480766"
---
# <a name="-netcf"></a><span data-ttu-id="3bbb5-102">-netcf</span><span class="sxs-lookup"><span data-stu-id="3bbb5-102">-netcf</span></span>

<span data-ttu-id="3bbb5-103">Configure le compilateur pour cibler le [!INCLUDE[Compact](~/includes/compact-md.md)].</span><span class="sxs-lookup"><span data-stu-id="3bbb5-103">Sets the compiler to target the [!INCLUDE[Compact](~/includes/compact-md.md)].</span></span>

## <a name="syntax"></a><span data-ttu-id="3bbb5-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="3bbb5-104">Syntax</span></span>

```
-netcf
```

## <a name="remarks"></a><span data-ttu-id="3bbb5-105">Notes</span><span class="sxs-lookup"><span data-stu-id="3bbb5-105">Remarks</span></span>

<span data-ttu-id="3bbb5-106">Le `-netcf` option, le compilateur Visual Basic à cibler le [!INCLUDE[Compact](~/includes/compact-md.md)] au lieu de la version complète [!INCLUDE[dnprdnshort](~/includes/dnprdnshort-md.md)].</span><span class="sxs-lookup"><span data-stu-id="3bbb5-106">The `-netcf` option causes the Visual Basic compiler to target the [!INCLUDE[Compact](~/includes/compact-md.md)] rather than the full [!INCLUDE[dnprdnshort](~/includes/dnprdnshort-md.md)].</span></span> <span data-ttu-id="3bbb5-107">Fonctionnalités de langage qui sont trouve uniquement dans la version complète [!INCLUDE[dnprdnshort](~/includes/dnprdnshort-md.md)] est désactivé.</span><span class="sxs-lookup"><span data-stu-id="3bbb5-107">Language functionality that is present only in the full [!INCLUDE[dnprdnshort](~/includes/dnprdnshort-md.md)] is disabled.</span></span>

<span data-ttu-id="3bbb5-108">Le `-netcf` option est conçue pour être utilisée avec [- sdkpath](../../../visual-basic/reference/command-line-compiler/sdkpath.md).</span><span class="sxs-lookup"><span data-stu-id="3bbb5-108">The `-netcf` option is designed to be used with [-sdkpath](../../../visual-basic/reference/command-line-compiler/sdkpath.md).</span></span> <span data-ttu-id="3bbb5-109">Les fonctionnalités de langage désactivées par `-netcf` sont les mêmes fonctionnalités de langage pas présentes dans les fichiers ciblés avec `-sdkpath`.</span><span class="sxs-lookup"><span data-stu-id="3bbb5-109">The language features disabled by `-netcf` are the same language features not present in the files targeted with `-sdkpath`.</span></span>

> [!NOTE]
> <span data-ttu-id="3bbb5-110">Le `-netcf` option n’est pas disponible dans l’environnement de développement Visual Studio ; il est disponible uniquement lors de la compilation à partir de la ligne de commande.</span><span class="sxs-lookup"><span data-stu-id="3bbb5-110">The `-netcf` option is not available from within the Visual Studio development environment; it is available only when compiling from the command line.</span></span> <span data-ttu-id="3bbb5-111">Le `-netcf` option est définie lorsqu’un projet smart device de Visual Basic est chargé.</span><span class="sxs-lookup"><span data-stu-id="3bbb5-111">The `-netcf` option is set when a Visual Basic device project is loaded.</span></span>

<span data-ttu-id="3bbb5-112">Le `-netcf` option modifie les fonctionnalités de langage suivantes :</span><span class="sxs-lookup"><span data-stu-id="3bbb5-112">The `-netcf` option changes the following language features:</span></span>

- <span data-ttu-id="3bbb5-113">Le [fin \<mot clé > instruction](../../../visual-basic/language-reference/statements/end-keyword-statement.md) mot clé, qui termine l’exécution d’un programme, est désactivé.</span><span class="sxs-lookup"><span data-stu-id="3bbb5-113">The [End \<keyword> Statement](../../../visual-basic/language-reference/statements/end-keyword-statement.md) keyword, which terminates execution of a program, is disabled.</span></span> <span data-ttu-id="3bbb5-114">Le programme suivant se compile et s’exécute sans `-netcf` mais échoue au moment de la compilation avec `-netcf`.</span><span class="sxs-lookup"><span data-stu-id="3bbb5-114">The following program compiles and runs without `-netcf` but fails at compile time with `-netcf`.</span></span>

  [!code-vb[VbVbalrCompiler#34](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbalrCompiler/VB/netcf.vb#34)]

- <span data-ttu-id="3bbb5-115">Liaison tardive dans chacun des formulaires est désactivée.</span><span class="sxs-lookup"><span data-stu-id="3bbb5-115">Late binding, in all forms, is disabled.</span></span> <span data-ttu-id="3bbb5-116">Erreurs de compilation sont générées lorsque des scénarios de liaison tardive reconnus sont rencontrées.</span><span class="sxs-lookup"><span data-stu-id="3bbb5-116">Compile-time errors are generated when recognized late-binding scenarios are encountered.</span></span> <span data-ttu-id="3bbb5-117">Le programme suivant se compile et s’exécute sans `-netcf` mais échoue au moment de la compilation avec `-netcf`.</span><span class="sxs-lookup"><span data-stu-id="3bbb5-117">The following program compiles and runs without `-netcf` but fails at compile time with `-netcf`.</span></span>

  [!code-vb[VbVbalrCompiler#35](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbalrCompiler/VB/OptionStrictOff.vb#35)]

- <span data-ttu-id="3bbb5-118">Le [automatique](../../../visual-basic/language-reference/modifiers/auto.md), [Ansi](../../../visual-basic/language-reference/modifiers/ansi.md), et [Unicode](../../../visual-basic/language-reference/modifiers/unicode.md) modificateurs sont désactivées.</span><span class="sxs-lookup"><span data-stu-id="3bbb5-118">The [Auto](../../../visual-basic/language-reference/modifiers/auto.md), [Ansi](../../../visual-basic/language-reference/modifiers/ansi.md), and [Unicode](../../../visual-basic/language-reference/modifiers/unicode.md) modifiers are disabled.</span></span> <span data-ttu-id="3bbb5-119">La syntaxe de la [instruction Declare](../../../visual-basic/language-reference/statements/declare-statement.md) instruction est également modifiée pour `Declare Sub|Function name Lib "library" [Alias "alias"] [([arglist])]`.</span><span class="sxs-lookup"><span data-stu-id="3bbb5-119">The syntax of the [Declare Statement](../../../visual-basic/language-reference/statements/declare-statement.md) statement is also modified to `Declare Sub|Function name Lib "library" [Alias "alias"] [([arglist])]`.</span></span> <span data-ttu-id="3bbb5-120">Le code suivant montre l’effet de `-netcf` sur une compilation.</span><span class="sxs-lookup"><span data-stu-id="3bbb5-120">The following code shows the effect of `-netcf` on a compilation.</span></span>

  [!code-vb[VbVbalrCompiler#36](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbalrCompiler/VB/OptionStrictOff.vb#36)]

- <span data-ttu-id="3bbb5-121">À l’aide de mots clés Visual Basic 6.0 qui ont été supprimés à partir de Visual Basic génère une erreur différente lorsque `-netcf` est utilisé.</span><span class="sxs-lookup"><span data-stu-id="3bbb5-121">Using Visual Basic 6.0 keywords that were removed from Visual Basic generates a different error when `-netcf` is used.</span></span> <span data-ttu-id="3bbb5-122">Cela affecte les messages d’erreur pour les mots clés suivants :</span><span class="sxs-lookup"><span data-stu-id="3bbb5-122">This affects the error messages for the following keywords:</span></span>

  - `Open`

  - `Close`

  - `Put`

  - `Print`

  - `Write`

  - `Input`

  - `Lock`

  - `Unlock`

  - `Seek`

  - `Width`

  - `Name`

  - `FreeFile`

  - `EOF`

  - `Loc`

  - `LOF`

  - `Line`

## <a name="example"></a><span data-ttu-id="3bbb5-123">Exemple</span><span class="sxs-lookup"><span data-stu-id="3bbb5-123">Example</span></span>

<span data-ttu-id="3bbb5-124">Le code suivant compile `Myfile.vb` avec la [!INCLUDE[Compact](~/includes/compact-md.md)], l’utilisation des versions de mscorlib.dll et de Microsoft.VisualBasic.dll trouvées dans le répertoire d’installation par défaut de la [!INCLUDE[Compact](~/includes/compact-md.md)] sur le lecteur C.</span><span class="sxs-lookup"><span data-stu-id="3bbb5-124">The following code compiles `Myfile.vb` with the [!INCLUDE[Compact](~/includes/compact-md.md)], using the versions of mscorlib.dll and Microsoft.VisualBasic.dll found in the default installation directory of the [!INCLUDE[Compact](~/includes/compact-md.md)] on the C drive.</span></span> <span data-ttu-id="3bbb5-125">En règle générale, vous utiliseriez la version la plus récente de la [!INCLUDE[Compact](~/includes/compact-md.md)].</span><span class="sxs-lookup"><span data-stu-id="3bbb5-125">Typically, you would use the most recent version of the [!INCLUDE[Compact](~/includes/compact-md.md)].</span></span>

```console
vbc -netcf -sdkpath:"c:\Program Files\Microsoft Visual Studio .NET 2003\CompactFrameworkSDK\v1.0.5000\Windows CE " myfile.vb
```

## <a name="see-also"></a><span data-ttu-id="3bbb5-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="3bbb5-126">See also</span></span>

- [<span data-ttu-id="3bbb5-127">Compilateur de ligne de commande de Visual Basic</span><span class="sxs-lookup"><span data-stu-id="3bbb5-127">Visual Basic Command-Line Compiler</span></span>](../../../visual-basic/reference/command-line-compiler/index.md)
- [<span data-ttu-id="3bbb5-128">Exemples de lignes de commande de compilation</span><span class="sxs-lookup"><span data-stu-id="3bbb5-128">Sample Compilation Command Lines</span></span>](../../../visual-basic/reference/command-line-compiler/sample-compilation-command-lines.md)
- [<span data-ttu-id="3bbb5-129">-sdkpath</span><span class="sxs-lookup"><span data-stu-id="3bbb5-129">-sdkpath</span></span>](../../../visual-basic/reference/command-line-compiler/sdkpath.md)
