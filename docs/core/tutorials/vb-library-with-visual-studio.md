---
title: Générer une bibliothèque de classes Visual Basic .NET Standard dans Visual Studio 2017
description: Découvrez comment générer une bibliothèque de classes .NET Standard écrite en Visual Basic à l’aide de Visual Studio 2017
author: rpetrusha
ms.author: ronpet
ms.date: 08/07/2017
dev_langs:
- vb
ms.custom: vs-dotnet, seodec18
ms.openlocfilehash: f14e4ffbebfe0d7e01d548a6d4f2dc8924633682
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59157298"
---
# <a name="build-a-net-standard-library-with-visual-basic-and-the-net-core-sdk-in-visual-studio-2017"></a><span data-ttu-id="9a366-103">Générer une bibliothèque .NET Standard avec Visual Basic et le kit SDK .NET Core dans Visual Studio 2017</span><span class="sxs-lookup"><span data-stu-id="9a366-103">Build a .NET Standard library with Visual Basic and the .NET Core SDK in Visual Studio 2017</span></span>

<span data-ttu-id="9a366-104">Une *bibliothèque de classes* définit des types et des méthodes qui peuvent être appelés par une application.</span><span class="sxs-lookup"><span data-stu-id="9a366-104">A *class library* defines types and methods that are called by an application.</span></span> <span data-ttu-id="9a366-105">Une bibliothèque de classes qui cible .NET Standard 2.0 permet à votre bibliothèque d’être appelée par n’importe quelle implémentation .NET qui prend en charge cette version de .NET Standard.</span><span class="sxs-lookup"><span data-stu-id="9a366-105">A class library that targets the .NET Standard 2.0 allows your library to be called by any .NET implementation that supports that version of the .NET Standard.</span></span> <span data-ttu-id="9a366-106">Quand vous avez terminé votre bibliothèque de classes, vous pouvez décider de la distribuer ou non comme un composant tiers, ou de l’inclure ou non dans un composant groupé avec une ou plusieurs applications.</span><span class="sxs-lookup"><span data-stu-id="9a366-106">When you finish your class library, you can decide whether you want to distribute it as a third-party component or whether you want to include it as a bundled component with one or more applications.</span></span>

> [!NOTE]
> <span data-ttu-id="9a366-107">Pour obtenir la liste des versions de .NET Standard et des plateformes prises en charge, consultez [.NET Standard](../../standard/net-standard.md).</span><span class="sxs-lookup"><span data-stu-id="9a366-107">For a list of the .NET Standard versions and the platforms they support, see [.NET Standard](../../standard/net-standard.md).</span></span>

<span data-ttu-id="9a366-108">Dans cette rubrique, vous créez une bibliothèque d’utilitaire simple qui contient une seule méthode de gestion de chaîne.</span><span class="sxs-lookup"><span data-stu-id="9a366-108">In this topic, you'll create a simple utility library that contains a single string-handling method.</span></span> <span data-ttu-id="9a366-109">Vous l’implémentez en tant que [méthode d’extension](../../visual-basic/programming-guide/language-features/procedures/extension-methods.md), pour pouvoir l’appeler comme s’il s’agissait d’un membre de la classe <xref:System.String>.</span><span class="sxs-lookup"><span data-stu-id="9a366-109">You'll implement it as an [extension method](../../visual-basic/programming-guide/language-features/procedures/extension-methods.md) so that you can call it as if it were a member of the <xref:System.String> class.</span></span>

## <a name="creating-a-class-library-solution"></a><span data-ttu-id="9a366-110">Création d'une solution de bibliothèque de classes</span><span class="sxs-lookup"><span data-stu-id="9a366-110">Creating a class library solution</span></span>

<span data-ttu-id="9a366-111">Commencez par créer une solution pour votre projet de bibliothèque de classes et ses projets connexes.</span><span class="sxs-lookup"><span data-stu-id="9a366-111">Start by creating a solution for your class library project and its related projects.</span></span> <span data-ttu-id="9a366-112">Une solution Visual Studio sert simplement de conteneur pour un ou plusieurs projets.</span><span class="sxs-lookup"><span data-stu-id="9a366-112">A Visual Studio Solution just serves as a container for one or more projects.</span></span> <span data-ttu-id="9a366-113">Pour créer la solution :</span><span class="sxs-lookup"><span data-stu-id="9a366-113">To create the solution:</span></span>

1. <span data-ttu-id="9a366-114">Dans la barre de menus de Visual Studio, choisissez **Fichier** > **Nouveau** > **Projet**.</span><span class="sxs-lookup"><span data-stu-id="9a366-114">On the Visual Studio menu bar, choose **File** > **New** > **Project**.</span></span>

1. <span data-ttu-id="9a366-115">Dans la boîte de dialogue **Nouveau projet**, développez le nœud **Autres types de projets** et sélectionnez **Solutions Visual Studio**.</span><span class="sxs-lookup"><span data-stu-id="9a366-115">In the **New Project** dialog, expand the **Other Project Types** node, and select **Visual Studio Solutions**.</span></span> <span data-ttu-id="9a366-116">Nommez la solution « ClassLibraryProjects » puis sélectionnez le bouton **OK**.</span><span class="sxs-lookup"><span data-stu-id="9a366-116">Name the solution "ClassLibraryProjects" and select the **OK** button.</span></span>

   ![Boîte de dialogue Créer un projet de test dans Visual Studio](./media/library-with-visual-studio/new-project-dialog.png)

## <a name="creating-the-class-library-project"></a><span data-ttu-id="9a366-118">Création du projet de bibliothèque de classes</span><span class="sxs-lookup"><span data-stu-id="9a366-118">Creating the class library project</span></span>

<span data-ttu-id="9a366-119">Créez votre projet de bibliothèque de classes :</span><span class="sxs-lookup"><span data-stu-id="9a366-119">Create your class library project:</span></span>

1. <span data-ttu-id="9a366-120">Dans **l’Explorateur de solutions**, cliquez avec le bouton droit sur la solution **ClassLibraryProjects** et, dans le menu contextuel, sélectionnez **Ajouter** > **Nouveau projet**.</span><span class="sxs-lookup"><span data-stu-id="9a366-120">In **Solution Explorer**, right-click on the **ClassLibraryProjects** solution file and from the context menu, select **Add** > **New Project**.</span></span>

1. <span data-ttu-id="9a366-121">Dans la boîte de dialogue **Ajouter un nouveau projet**, développez le nœud **Visual Basic**, puis sélectionnez le nœud **.NET Standard** et choisissez le modèle de projet **Bibliothèque de classes (.NET Standard)**.</span><span class="sxs-lookup"><span data-stu-id="9a366-121">In the **Add New Project** dialog, expand the **Visual Basic** node, then select the **.NET Standard** node followed by the **Class Library (.NET Standard)** project template.</span></span> <span data-ttu-id="9a366-122">Dans la zone de texte **Nom**, entrez « StringLibrary » comme nom de projet.</span><span class="sxs-lookup"><span data-stu-id="9a366-122">In the **Name** text box, enter "StringLibrary" as the name of the project.</span></span> <span data-ttu-id="9a366-123">Sélectionnez **OK** pour créer le projet de bibliothèque de classes.</span><span class="sxs-lookup"><span data-stu-id="9a366-123">Select **OK** to create the class library project.</span></span>

   ![Boîte de dialogue Ajouter un nouveau projet de test dans Visual Studio](./media/vb-library-with-visual-studio/create-new-library-project.png)

   <span data-ttu-id="9a366-125">Ensuite, la fenêtre de code s’ouvre dans l’environnement de développement Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="9a366-125">The code window then opens in the Visual Studio development environment.</span></span> 
 
   ![Fenêtre d’application Visual Studio montrant le code du modèle de bibliothèque de classes par défaut](./media/vb-library-with-visual-studio/visual-studio-library.png)

1. <span data-ttu-id="9a366-127">Vérifiez que notre bibliothèque cible la version appropriée de .NET Standard.</span><span class="sxs-lookup"><span data-stu-id="9a366-127">Check to make sure that the library targets the correct version of the .NET Standard.</span></span> <span data-ttu-id="9a366-128">Dans la fenêtre **Explorateur de solutions**, cliquez avec le bouton droit sur le projet de bibliothèque, puis sélectionnez **Propriétés**.</span><span class="sxs-lookup"><span data-stu-id="9a366-128">Right-click on the library project in the **Solution Explorer** windows, then select **Properties**.</span></span> <span data-ttu-id="9a366-129">La zone de texte **framework cible** indique que nous ciblons .NET Standard 2.0.</span><span class="sxs-lookup"><span data-stu-id="9a366-129">The **Target Framework** text box shows that we're targeting .NET Standard 2.0.</span></span>

   ![Propriétés de projet pour la bibliothèque de classes](./media/library-with-visual-studio/library-project-properties.png)

1. <span data-ttu-id="9a366-131">Dans la boîte de dialogue **Propriétés**, effacez le texte de la zone de texte **Espace de noms racine**.</span><span class="sxs-lookup"><span data-stu-id="9a366-131">Also in the **Properties** dialog, clear the text in the **Root namespace** text box.</span></span> <span data-ttu-id="9a366-132">Pour chaque projet, Visual Basic crée automatiquement un espace de noms qui correspond au nom du projet, et tous les espaces de noms définis dans les fichiers de code source sont des parents de cet espace de noms.</span><span class="sxs-lookup"><span data-stu-id="9a366-132">For each project, Visual Basic automatically creates a namespace that corresponds to the project name, and any namespaces defined in source code files are parents of that namespace.</span></span> <span data-ttu-id="9a366-133">Nous souhaitons définir un espace de noms de niveau supérieur à l’aide du mot clé [`namespace`](../../visual-basic/language-reference/statements/namespace-statement.md).</span><span class="sxs-lookup"><span data-stu-id="9a366-133">We want to define a top-level namespace by using the [`namespace`](../../visual-basic/language-reference/statements/namespace-statement.md) keyword.</span></span>
  
1. <span data-ttu-id="9a366-134">Remplacez le code de la fenêtre de code par le code suivant et enregistrez le fichier :</span><span class="sxs-lookup"><span data-stu-id="9a366-134">Replace the code in the code window with the following code and save the file:</span></span>

  [!CODE-vb[ClassLib#1](../../../samples/snippets/core/tutorials/vb-library-with-visual-studio/stringlibrary.vb)]

   <span data-ttu-id="9a366-135">La bibliothèque de classes, `UtilityLibraries.StringLibrary`, contient une méthode nommée `StartsWithUpper`, qui retourne une valeur <xref:System.Boolean> qui indique si l’instance actuelle de la chaîne commence par une majuscule.</span><span class="sxs-lookup"><span data-stu-id="9a366-135">The class library, `UtilityLibraries.StringLibrary`, contains a method named `StartsWithUpper`, which returns a <xref:System.Boolean> value that indicates whether the current string instance begins with an uppercase character.</span></span> <span data-ttu-id="9a366-136">La norme Unicode distingue les caractères minuscules des caractères majuscules.</span><span class="sxs-lookup"><span data-stu-id="9a366-136">The Unicode standard distinguishes uppercase characters from lowercase characters.</span></span> <span data-ttu-id="9a366-137">La méthode <xref:System.Char.IsUpper(System.Char)?displayProperty=nameWithType> retourne `true` si un caractère est en majuscule.</span><span class="sxs-lookup"><span data-stu-id="9a366-137">The <xref:System.Char.IsUpper(System.Char)?displayProperty=nameWithType> method returns `true` if a character is uppercase.</span></span>

1. <span data-ttu-id="9a366-138">Dans la barre de menus, sélectionnez **Générer** > **Générer la solution**.</span><span class="sxs-lookup"><span data-stu-id="9a366-138">On the menu bar, select **Build** > **Build Solution**.</span></span> <span data-ttu-id="9a366-139">Le projet devrait être compilé sans erreur.</span><span class="sxs-lookup"><span data-stu-id="9a366-139">The project should compile without error.</span></span>

   ![Volet de sortie indiquant que la génération a réussi](./media/library-with-visual-studio/output-pane-successful-build.png)

## <a name="next-step"></a><span data-ttu-id="9a366-141">Étape suivante</span><span class="sxs-lookup"><span data-stu-id="9a366-141">Next step</span></span>

<span data-ttu-id="9a366-142">Vous avez créé la bibliothèque correctement.</span><span class="sxs-lookup"><span data-stu-id="9a366-142">You've successfully built the library.</span></span> <span data-ttu-id="9a366-143">Comme vous n’avez appelé aucune de ses méthodes, vous ne savez pas si elle fonctionne comme prévu.</span><span class="sxs-lookup"><span data-stu-id="9a366-143">Because you haven't called any of its methods, you don't know whether it works as expected.</span></span> <span data-ttu-id="9a366-144">L’étape suivante du développement de votre bibliothèque consiste à la tester en utilisant un [Projet de test unitaire](testing-library-with-visual-studio.md).</span><span class="sxs-lookup"><span data-stu-id="9a366-144">The next step in developing your library is to test it by using a [Unit Test Project](testing-library-with-visual-studio.md).</span></span>
