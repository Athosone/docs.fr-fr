---
title: Options du compilateur C#
ms.date: 07/20/2015
f1_keywords:
- cs.build.options
helpviewer_keywords:
- compiler options [C#]
- csc.exe
- cl.exe compiler, C# options
- Visual C# compiler
- Visual C#, compiler options
ms.assetid: d3403556-1816-4546-a782-e8223a772e44
ms.openlocfilehash: a0affaf3691d2392c9f8d7502204d0122f2ea428
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61662827"
---
# <a name="c-compiler-options"></a><span data-ttu-id="f3815-102">Options du compilateur C#</span><span class="sxs-lookup"><span data-stu-id="f3815-102">C# Compiler Options</span></span>
<span data-ttu-id="f3815-103">Le compilateur produit des fichiers exécutables (.exe), des bibliothèques de liens dynamiques (.dll) ou des modules de code (.netmodule).</span><span class="sxs-lookup"><span data-stu-id="f3815-103">The compiler produces executable (.exe) files, dynamic-link libraries (.dll), or code modules (.netmodule).</span></span>  
  
 <span data-ttu-id="f3815-104">Chaque option du compilateur est disponible sous deux formes : **-option** et **/option**.</span><span class="sxs-lookup"><span data-stu-id="f3815-104">Every compiler option is available in two forms: **-option** and **/option**.</span></span> <span data-ttu-id="f3815-105">La documentation présente uniquement la forme **-option**.</span><span class="sxs-lookup"><span data-stu-id="f3815-105">The documentation only shows the **-option** form.</span></span>  
  
 <span data-ttu-id="f3815-106">Dans Visual Studio, vous définissez les options du compilateur dans le fichier web.config.</span><span class="sxs-lookup"><span data-stu-id="f3815-106">In Visual Studio, you set compiler options in the web.config file.</span></span> <span data-ttu-id="f3815-107">Pour plus d’informations, consultez [\<compilateur> Élément](../../../framework/configure-apps/file-schema/compiler/compiler-element.md).</span><span class="sxs-lookup"><span data-stu-id="f3815-107">For more information, see [\<compiler> Element](../../../framework/configure-apps/file-schema/compiler/compiler-element.md).</span></span>  
  
## <a name="in-this-section"></a><span data-ttu-id="f3815-108">Dans cette section</span><span class="sxs-lookup"><span data-stu-id="f3815-108">In This Section</span></span>  
 [<span data-ttu-id="f3815-109">Génération à partir de la ligne de commande avec csc.exe</span><span class="sxs-lookup"><span data-stu-id="f3815-109">Command-line Building With csc.exe</span></span>](command-line-building-with-csc-exe.md)  
 <span data-ttu-id="f3815-110">Informations sur la création d’une application Visual C# à partir de la ligne de commande.</span><span class="sxs-lookup"><span data-stu-id="f3815-110">Information about building a Visual C# application from the command line.</span></span>  
  
 [<span data-ttu-id="f3815-111">Guide pratique pour définir des variables d’environnement pour la ligne de commande Visual Studio</span><span class="sxs-lookup"><span data-stu-id="f3815-111">How to: Set Environment Variables for the Visual Studio Command Line</span></span>](how-to-set-environment-variables-for-the-visual-studio-command-line.md)  
 <span data-ttu-id="f3815-112">Explique comment exécuter vsvars32.bat pour permettre les générations à partir de la ligne de commande.</span><span class="sxs-lookup"><span data-stu-id="f3815-112">Provides steps for running vsvars32.bat  to enable command-line builds.</span></span>  
  
 [<span data-ttu-id="f3815-113">Options du compilateur C# par catégorie</span><span class="sxs-lookup"><span data-stu-id="f3815-113">C# Compiler Options Listed by Category</span></span>](listed-by-category.md)  
 <span data-ttu-id="f3815-114">Liste par catégorie des options du compilateur.</span><span class="sxs-lookup"><span data-stu-id="f3815-114">A categorical listing of the compiler options.</span></span>  
  
 [<span data-ttu-id="f3815-115">Options du compilateur C# par ordre alphabétique</span><span class="sxs-lookup"><span data-stu-id="f3815-115">C# Compiler Options Listed Alphabetically</span></span>](listed-alphabetically.md)  
 <span data-ttu-id="f3815-116">Liste alphabétique des options du compilateur.</span><span class="sxs-lookup"><span data-stu-id="f3815-116">An alphabetical listing of the compiler options.</span></span>  
  
## <a name="related-sections"></a><span data-ttu-id="f3815-117">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="f3815-117">Related Sections</span></span>  
 [<span data-ttu-id="f3815-118">Page Générer, Concepteur de projets</span><span class="sxs-lookup"><span data-stu-id="f3815-118">Build Page, Project Designer</span></span>](/visualstudio/ide/reference/build-page-project-designer-csharp)  
 <span data-ttu-id="f3815-119">Définition des propriétés qui régissent la façon dont votre projet est compilé, généré et débogué.</span><span class="sxs-lookup"><span data-stu-id="f3815-119">Setting properties that govern how your project is compiled, built, and debugged.</span></span> <span data-ttu-id="f3815-120">Contient des informations sur les étapes de génération personnalisée dans les projets Visual C#.</span><span class="sxs-lookup"><span data-stu-id="f3815-120">Includes information about custom build steps in Visual C# projects.</span></span>  
  
 [<span data-ttu-id="f3815-121">Générations personnalisées et par défaut</span><span class="sxs-lookup"><span data-stu-id="f3815-121">Default and Custom Builds</span></span>](/visualstudio/ide/compiling-and-building-in-visual-studio)  
 <span data-ttu-id="f3815-122">Informations sur les configurations et les types de génération.</span><span class="sxs-lookup"><span data-stu-id="f3815-122">Information on build types and configurations.</span></span>  
  
 [<span data-ttu-id="f3815-123">Préparation et gestion des générations</span><span class="sxs-lookup"><span data-stu-id="f3815-123">Preparing and Managing Builds</span></span>](/visualstudio/ide/building-and-cleaning-projects-and-solutions-in-visual-studio)  
 <span data-ttu-id="f3815-124">Procédures de génération dans l’environnement de développement Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="f3815-124">Procedures for building within the Visual Studio development environment.</span></span>
