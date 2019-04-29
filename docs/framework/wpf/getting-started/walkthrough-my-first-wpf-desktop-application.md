---
title: Créer une application WPF dans Visual Studio
ms.date: 10/26/2018
dev_langs:
- csharp
- vb
helpviewer_keywords:
- getting started [WPF], WPF
- WPF [WPF], getting started
ms.assetid: b96bed40-8946-4285-8fe4-88045ab854ed
author: mairaw
ms.author: mairaw
ms.custom: vs-dotnet
ms.openlocfilehash: dbfc40bd1fcc97810ea1397731bd8c232297cbd1
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61922959"
---
# <a name="walkthrough-my-first-wpf-desktop-application"></a><span data-ttu-id="8a2c5-102">Procédure pas à pas : Ma première application de bureau WPF</span><span class="sxs-lookup"><span data-stu-id="8a2c5-102">Walkthrough: My first WPF desktop application</span></span>

<span data-ttu-id="8a2c5-103">Cet article vous explique comment développer une application Windows Presentation Foundation (WPF) simple qui inclut les éléments qui sont communes à la plupart des applications WPF : Extensible Application Markup Language (XAML) balisage, code-behind, définitions d’application, contrôles, disposition, liaison de données et styles.</span><span class="sxs-lookup"><span data-stu-id="8a2c5-103">This article shows you how to develop a simple Windows Presentation Foundation (WPF) application that includes the elements that are common to most WPF applications: Extensible Application Markup Language (XAML) markup, code-behind, application definitions, controls, layout, data binding, and styles.</span></span>

<span data-ttu-id="8a2c5-104">Cette procédure pas à pas comprend les étapes suivantes :</span><span class="sxs-lookup"><span data-stu-id="8a2c5-104">This walkthrough includes the following steps:</span></span>

- <span data-ttu-id="8a2c5-105">XAML permet de concevoir l’apparence de l’interface utilisateur de l’application (IU).</span><span class="sxs-lookup"><span data-stu-id="8a2c5-105">Use XAML to design the appearance of the application's user interface (UI).</span></span>

- <span data-ttu-id="8a2c5-106">Écrire du code pour générer le comportement de l’application.</span><span class="sxs-lookup"><span data-stu-id="8a2c5-106">Write code to build the application's behavior.</span></span>

- <span data-ttu-id="8a2c5-107">Créer une définition d’application pour gérer l’application.</span><span class="sxs-lookup"><span data-stu-id="8a2c5-107">Create an application definition to manage the application.</span></span>

- <span data-ttu-id="8a2c5-108">Ajouter des contrôles et créer la disposition pour composer l’interface utilisateur de l’application.</span><span class="sxs-lookup"><span data-stu-id="8a2c5-108">Add controls and create the layout to compose the application UI.</span></span>

- <span data-ttu-id="8a2c5-109">Créer des styles pour une apparence cohérente tout au long de l’interface utilisateur d’une application.</span><span class="sxs-lookup"><span data-stu-id="8a2c5-109">Create styles for a consistent appearance throughout an application's UI.</span></span>

- <span data-ttu-id="8a2c5-110">Lier l’interface utilisateur aux données pour remplir l’interface utilisateur à partir des données et de conserver les données et l’interface utilisateur synchronisé.</span><span class="sxs-lookup"><span data-stu-id="8a2c5-110">Bind the UI to data to both populate the UI from data and keep the data and UI synchronized.</span></span>

<span data-ttu-id="8a2c5-111">À la fin de la procédure pas à pas, vous aurez créé une application Windows qui permet aux utilisateurs d’afficher les notes de frais pour certaines personnes autonome.</span><span class="sxs-lookup"><span data-stu-id="8a2c5-111">By the end of the walkthrough, you'll have built a standalone Windows application that allows users to view expense reports for selected people.</span></span> <span data-ttu-id="8a2c5-112">L’application est composée de plusieurs pages WPF sont hébergées dans une fenêtre de style navigateur.</span><span class="sxs-lookup"><span data-stu-id="8a2c5-112">The application is composed of several WPF pages that are hosted in a browser-style window.</span></span>

> [!TIP]
> <span data-ttu-id="8a2c5-113">L’exemple de code qui est utilisé pour générer cette procédure pas à pas est disponible pour Visual Basic et c# dans [Introduction to Building WPF Applications](https://go.microsoft.com/fwlink/?LinkID=160008).</span><span class="sxs-lookup"><span data-stu-id="8a2c5-113">The sample code that is used to build this walkthrough is available for both Visual Basic and C# at [Introduction to Building WPF Applications](https://go.microsoft.com/fwlink/?LinkID=160008).</span></span>

## <a name="prerequisites"></a><span data-ttu-id="8a2c5-114">Prérequis</span><span class="sxs-lookup"><span data-stu-id="8a2c5-114">Prerequisites</span></span>

- <span data-ttu-id="8a2c5-115">Visual Studio 2017 ou version ultérieure</span><span class="sxs-lookup"><span data-stu-id="8a2c5-115">Visual Studio 2017 or later</span></span>

   <span data-ttu-id="8a2c5-116">Pour plus d’informations sur l’installation de la dernière version de Visual Studio, consultez [installer Visual Studio](/visualstudio/install/install-visual-studio).</span><span class="sxs-lookup"><span data-stu-id="8a2c5-116">For more information about installing the latest version of Visual Studio, see [Install Visual Studio](/visualstudio/install/install-visual-studio).</span></span>

## <a name="create-the-application-project"></a><span data-ttu-id="8a2c5-117">Créer le projet d’application</span><span class="sxs-lookup"><span data-stu-id="8a2c5-117">Create the application project</span></span>

<span data-ttu-id="8a2c5-118">La première étape consiste à créer l’infrastructure d’application, qui inclut une définition d’application, deux pages et une image.</span><span class="sxs-lookup"><span data-stu-id="8a2c5-118">The first step is to create the application infrastructure, which includes an application definition, two pages, and an image.</span></span>

1. <span data-ttu-id="8a2c5-119">Créer un nouveau projet d’Application WPF en Visual Basic ou Visual c# nommé **`ExpenseIt`**:</span><span class="sxs-lookup"><span data-stu-id="8a2c5-119">Create a new WPF Application project in Visual Basic or Visual C# named **`ExpenseIt`**:</span></span>

   1. <span data-ttu-id="8a2c5-120">Ouvrez Visual Studio et sélectionnez **fichier** > **New** > **projet**.</span><span class="sxs-lookup"><span data-stu-id="8a2c5-120">Open Visual Studio and select **File** > **New** > **Project**.</span></span>

      <span data-ttu-id="8a2c5-121">Le **nouveau projet** boîte de dialogue s’ouvre.</span><span class="sxs-lookup"><span data-stu-id="8a2c5-121">The **New Project** dialog opens.</span></span>

   2. <span data-ttu-id="8a2c5-122">Sous le **installé** catégorie, développez le **Visual C#**  ou **Visual Basic** nœud, puis sélectionnez **Windows Desktop**.</span><span class="sxs-lookup"><span data-stu-id="8a2c5-122">Under the **Installed** category, expand either the **Visual C#** or **Visual Basic** node, and then select **Windows Desktop**.</span></span>

   3. <span data-ttu-id="8a2c5-123">Sélectionnez le **application WPF (.NET Framework)** modèle.</span><span class="sxs-lookup"><span data-stu-id="8a2c5-123">Select the **WPF App (.NET Framework)** template.</span></span> <span data-ttu-id="8a2c5-124">Entrez le nom **`ExpenseIt`** , puis sélectionnez **OK**.</span><span class="sxs-lookup"><span data-stu-id="8a2c5-124">Enter the name **`ExpenseIt`** and then select **OK**.</span></span>

      ![Boîte de dialogue Nouveau projet avec une application WPF sélectionnée](./media/new-project-dialog.png)

      <span data-ttu-id="8a2c5-126">Visual Studio crée le projet et ouvre le concepteur pour la fenêtre d’application par défaut nommé **MainWindow.xaml**.</span><span class="sxs-lookup"><span data-stu-id="8a2c5-126">Visual Studio creates the project and opens the designer for the default application window named **MainWindow.xaml**.</span></span>

   > [!NOTE]
   > <span data-ttu-id="8a2c5-127">Cette procédure pas à pas utilise le <xref:System.Windows.Controls.DataGrid> contrôle qui est disponible dans le .NET Framework 4 et versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="8a2c5-127">This walkthrough uses the <xref:System.Windows.Controls.DataGrid> control that is available in the .NET Framework 4 and later.</span></span> <span data-ttu-id="8a2c5-128">Être sûr que votre projet cible le .NET Framework 4 ou version ultérieure.</span><span class="sxs-lookup"><span data-stu-id="8a2c5-128">Be sure that your project targets the .NET Framework 4 or later.</span></span> <span data-ttu-id="8a2c5-129">Pour plus d'informations, voir [Procédure : Cibler une version du .NET Framework](/visualstudio/ide/how-to-target-a-version-of-the-dotnet-framework).</span><span class="sxs-lookup"><span data-stu-id="8a2c5-129">For more information, see [How to: Target a Version of the .NET Framework](/visualstudio/ide/how-to-target-a-version-of-the-dotnet-framework).</span></span>

2. <span data-ttu-id="8a2c5-130">Ouvrez *Application.xaml* (Visual Basic) ou *App.xaml* (c#).</span><span class="sxs-lookup"><span data-stu-id="8a2c5-130">Open *Application.xaml* (Visual Basic) or *App.xaml* (C#).</span></span>

    <span data-ttu-id="8a2c5-131">Ce fichier XAML définit une application WPF et les ressources de l’application.</span><span class="sxs-lookup"><span data-stu-id="8a2c5-131">This XAML file defines a WPF application and any application resources.</span></span> <span data-ttu-id="8a2c5-132">Vous utilisez également ce fichier pour spécifier l’interface utilisateur qui s’affiche automatiquement quand l’application démarre ; Dans ce cas, *MainWindow.xaml*.</span><span class="sxs-lookup"><span data-stu-id="8a2c5-132">You also use this file to specify the UI that automatically shows when the application starts; in this case, *MainWindow.xaml*.</span></span>

    <span data-ttu-id="8a2c5-133">Votre XAML doit ressembler à ceci en Visual Basic :</span><span class="sxs-lookup"><span data-stu-id="8a2c5-133">Your XAML should look like this in Visual Basic:</span></span>

    [!code-xaml[ExpenseIt#1_A](~/samples/snippets/visualbasic/VS_Snippets_Wpf/ExpenseIt/VB/ExpenseIt1_A/Application.xaml#1_a)]

    <span data-ttu-id="8a2c5-134">Ou à cela en C# :</span><span class="sxs-lookup"><span data-stu-id="8a2c5-134">Or like this in C#:</span></span>

    [!code-xaml[ExpenseIt#1](~/samples/snippets/csharp/VS_Snippets_Wpf/ExpenseIt/CSharp/ExpenseIt/App.xaml#1)]

3. <span data-ttu-id="8a2c5-135">Ouvrez *MainWindow.xaml*.</span><span class="sxs-lookup"><span data-stu-id="8a2c5-135">Open *MainWindow.xaml*.</span></span>

    <span data-ttu-id="8a2c5-136">Ce fichier XAML est la fenêtre principale de votre application et affiche le contenu créé dans les pages.</span><span class="sxs-lookup"><span data-stu-id="8a2c5-136">This XAML file is the main window of your application and displays content created in pages.</span></span> <span data-ttu-id="8a2c5-137">Le <xref:System.Windows.Window> classe définit les propriétés d’une fenêtre, telles que son titre, taille ou icône et gère les événements, tels que la fermeture ou le masquage.</span><span class="sxs-lookup"><span data-stu-id="8a2c5-137">The <xref:System.Windows.Window> class defines the properties of a window, such as its title, size, or icon, and handles events, such as closing or hiding.</span></span>

4. <span data-ttu-id="8a2c5-138">Modifier le <xref:System.Windows.Window> élément à un <xref:System.Windows.Navigation.NavigationWindow>, comme illustré dans le XAML suivant :</span><span class="sxs-lookup"><span data-stu-id="8a2c5-138">Change the <xref:System.Windows.Window> element to a <xref:System.Windows.Navigation.NavigationWindow>, as shown in the following XAML:</span></span>

   ```xaml
   <NavigationWindow x:Class="ExpenseIt.MainWindow"
        xmlns="http://schemas.microsoft.com/winfx/2006/xaml/presentation"
        xmlns:x="http://schemas.microsoft.com/winfx/2006/xaml"
        ...
   </NavigationWindow>
   ```

   <span data-ttu-id="8a2c5-139">Cette application accède à un contenu différent en fonction de l’entrée utilisateur.</span><span class="sxs-lookup"><span data-stu-id="8a2c5-139">This app navigates to different content depending on the user input.</span></span> <span data-ttu-id="8a2c5-140">C’est pourquoi les principaux <xref:System.Windows.Window> doit être changé en un <xref:System.Windows.Navigation.NavigationWindow>.</span><span class="sxs-lookup"><span data-stu-id="8a2c5-140">This is why the main <xref:System.Windows.Window> needs to be changed to a <xref:System.Windows.Navigation.NavigationWindow>.</span></span> <span data-ttu-id="8a2c5-141"><xref:System.Windows.Navigation.NavigationWindow> hérite de toutes les propriétés de <xref:System.Windows.Window>.</span><span class="sxs-lookup"><span data-stu-id="8a2c5-141"><xref:System.Windows.Navigation.NavigationWindow> inherits all the properties of <xref:System.Windows.Window>.</span></span> <span data-ttu-id="8a2c5-142">Le <xref:System.Windows.Navigation.NavigationWindow> élément dans le fichier XAML crée une instance de la <xref:System.Windows.Navigation.NavigationWindow> classe.</span><span class="sxs-lookup"><span data-stu-id="8a2c5-142">The <xref:System.Windows.Navigation.NavigationWindow> element in the XAML file creates an instance of the <xref:System.Windows.Navigation.NavigationWindow> class.</span></span> <span data-ttu-id="8a2c5-143">Pour plus d’informations, consultez [vue d’ensemble de la Navigation](../app-development/navigation-overview.md).</span><span class="sxs-lookup"><span data-stu-id="8a2c5-143">For more information, see [Navigation overview](../app-development/navigation-overview.md).</span></span>

5. <span data-ttu-id="8a2c5-144">Modifiez les propriétés suivantes sur le <xref:System.Windows.Navigation.NavigationWindow> élément :</span><span class="sxs-lookup"><span data-stu-id="8a2c5-144">Change the following properties on the <xref:System.Windows.Navigation.NavigationWindow> element:</span></span>

    - <span data-ttu-id="8a2c5-145">Définir le <xref:System.Windows.Window.Title%2A> propriété à «`ExpenseIt`».</span><span class="sxs-lookup"><span data-stu-id="8a2c5-145">Set the <xref:System.Windows.Window.Title%2A> property to "`ExpenseIt`".</span></span>

    - <span data-ttu-id="8a2c5-146">Définir le <xref:System.Windows.FrameworkElement.Width%2A> propriété 500 pixels.</span><span class="sxs-lookup"><span data-stu-id="8a2c5-146">Set the <xref:System.Windows.FrameworkElement.Width%2A> property to 500 pixels.</span></span>

    - <span data-ttu-id="8a2c5-147">Définir le <xref:System.Windows.FrameworkElement.Height%2A> propriété sur 350 pixels.</span><span class="sxs-lookup"><span data-stu-id="8a2c5-147">Set the <xref:System.Windows.FrameworkElement.Height%2A> property to 350 pixels.</span></span>

    - <span data-ttu-id="8a2c5-148">Supprimer le <xref:System.Windows.Controls.Grid> éléments entre le <xref:System.Windows.Navigation.NavigationWindow> balises.</span><span class="sxs-lookup"><span data-stu-id="8a2c5-148">Remove the <xref:System.Windows.Controls.Grid> elements between the <xref:System.Windows.Navigation.NavigationWindow> tags.</span></span>

    <span data-ttu-id="8a2c5-149">Votre XAML doit ressembler à ceci en Visual Basic :</span><span class="sxs-lookup"><span data-stu-id="8a2c5-149">Your XAML should look like this in Visual Basic:</span></span>

    [!code-xaml[ExpenseIt#2_A](~/samples/snippets/visualbasic/VS_Snippets_Wpf/ExpenseIt/VB/ExpenseIt/MainWindow.xaml#2_a)]

    <span data-ttu-id="8a2c5-150">Ou à cela en C# :</span><span class="sxs-lookup"><span data-stu-id="8a2c5-150">Or like this in C#:</span></span>

    [!code-xaml[ExpenseIt#2](~/samples/snippets/csharp/VS_Snippets_Wpf/ExpenseIt/CSharp/ExpenseIt/MainWindow.xaml#2)]

6. <span data-ttu-id="8a2c5-151">Ouvrez *MainWindow.xaml.vb* ou *MainWindow.xaml.cs*.</span><span class="sxs-lookup"><span data-stu-id="8a2c5-151">Open *MainWindow.xaml.vb* or *MainWindow.xaml.cs*.</span></span>

    <span data-ttu-id="8a2c5-152">Ce fichier est un fichier code-behind qui contient le code pour gérer les événements déclarés dans *MainWindow.xaml*.</span><span class="sxs-lookup"><span data-stu-id="8a2c5-152">This file is a code-behind file that contains code to handle the events declared in *MainWindow.xaml*.</span></span> <span data-ttu-id="8a2c5-153">Ce fichier contient une classe partielle pour la fenêtre définie en XAML.</span><span class="sxs-lookup"><span data-stu-id="8a2c5-153">This file contains a partial class for the window defined in XAML.</span></span>

7. <span data-ttu-id="8a2c5-154">Si vous utilisez c#, modifiez le `MainWindow` classe à dériver de <xref:System.Windows.Navigation.NavigationWindow>.</span><span class="sxs-lookup"><span data-stu-id="8a2c5-154">If you are using C#, change the `MainWindow` class to derive from <xref:System.Windows.Navigation.NavigationWindow>.</span></span> <span data-ttu-id="8a2c5-155">(En Visual Basic, cela se produit automatiquement lorsque vous modifiez la fenêtre en XAML.)</span><span class="sxs-lookup"><span data-stu-id="8a2c5-155">(In Visual Basic, this happens automatically when you change the window in XAML.)</span></span>

   <span data-ttu-id="8a2c5-156">Votre code doit ressembler à ceci :</span><span class="sxs-lookup"><span data-stu-id="8a2c5-156">Your code should look like this:</span></span>

   [!code-csharp[ExpenseIt#3](~/samples/snippets/csharp/VS_Snippets_Wpf/ExpenseIt/CSharp/ExpenseIt/MainWindow.xaml.cs#3)]
   [!code-vb[ExpenseIt#3](~/samples/snippets/visualbasic/VS_Snippets_Wpf/ExpenseIt/VB/ExpenseIt1_A/MainWindow.xaml.vb#3)]

   > [!TIP]
   > <span data-ttu-id="8a2c5-157">Vous pouvez activer/désactiver le langage de code de l’exemple de code entre c# et Visual Basic dans le **langage** déroulante sur le coin supérieur droit de cet article.</span><span class="sxs-lookup"><span data-stu-id="8a2c5-157">You can toggle the code language of the sample code between C# and Visual Basic in the **Language** drop-down on the upper right side of this article.</span></span>

## <a name="add-files-to-the-application"></a><span data-ttu-id="8a2c5-158">Ajouter des fichiers à l’application</span><span class="sxs-lookup"><span data-stu-id="8a2c5-158">Add files to the application</span></span>

<span data-ttu-id="8a2c5-159">Dans cette section, vous allez ajouter deux pages et une image à l’application.</span><span class="sxs-lookup"><span data-stu-id="8a2c5-159">In this section, you'll add two pages and an image to the application.</span></span>

1. <span data-ttu-id="8a2c5-160">Ajouter une nouvelle page WPF au projet et nommez-le *`ExpenseItHome.xaml`*:</span><span class="sxs-lookup"><span data-stu-id="8a2c5-160">Add a new WPF page to the project, and name it *`ExpenseItHome.xaml`*:</span></span>

   1. <span data-ttu-id="8a2c5-161">Dans **l’Explorateur de solutions**, avec le bouton droit sur le **`ExpenseIt`** nœud de projet et choisissez **ajouter** > **Page**.</span><span class="sxs-lookup"><span data-stu-id="8a2c5-161">In **Solution Explorer**, right-click on the **`ExpenseIt`** project node and choose **Add** > **Page**.</span></span>

   1. <span data-ttu-id="8a2c5-162">Dans le **ajouter un nouvel élément** boîte de dialogue, le **Page (WPF)** modèle est déjà sélectionné.</span><span class="sxs-lookup"><span data-stu-id="8a2c5-162">In the **Add New Item** dialog, the **Page (WPF)** template is already selected.</span></span> <span data-ttu-id="8a2c5-163">Entrez le nom **`ExpenseItHome`**, puis sélectionnez **ajouter**.</span><span class="sxs-lookup"><span data-stu-id="8a2c5-163">Enter the name **`ExpenseItHome`**, and then select **Add**.</span></span>

    <span data-ttu-id="8a2c5-164">Cette page est la première page qui s’affiche lorsque l’application est lancée.</span><span class="sxs-lookup"><span data-stu-id="8a2c5-164">This page is the first page that's displayed when the application is launched.</span></span> <span data-ttu-id="8a2c5-165">Il affiche une liste de personnes, pour afficher une note de frais.</span><span class="sxs-lookup"><span data-stu-id="8a2c5-165">It will show a list of people to select from, to show an expense report for.</span></span>

2. <span data-ttu-id="8a2c5-166">Ouvrez *`ExpenseItHome.xaml`*.</span><span class="sxs-lookup"><span data-stu-id="8a2c5-166">Open *`ExpenseItHome.xaml`*.</span></span>

3. <span data-ttu-id="8a2c5-167">Définir le <xref:System.Windows.Controls.Page.Title%2A> à «`ExpenseIt - Home`».</span><span class="sxs-lookup"><span data-stu-id="8a2c5-167">Set the <xref:System.Windows.Controls.Page.Title%2A> to "`ExpenseIt - Home`".</span></span>

    <span data-ttu-id="8a2c5-168">Votre XAML doit ressembler à ceci en Visual Basic :</span><span class="sxs-lookup"><span data-stu-id="8a2c5-168">Your XAML should look like this in Visual Basic:</span></span>

    [!code-xaml[ExpenseIt#6_A](~/samples/snippets/visualbasic/VS_Snippets_Wpf/ExpenseIt/VB/ExpenseIt1_A/ExpenseItHome.xaml#6_a)]

    <span data-ttu-id="8a2c5-169">Ou à cela en C# :</span><span class="sxs-lookup"><span data-stu-id="8a2c5-169">Or this in C#:</span></span>

    [!code-xaml[ExpenseIt#6](~/samples/snippets/csharp/VS_Snippets_Wpf/ExpenseIt/CSharp/ExpenseIt2/ExpenseItHome.xaml#6)]

4. <span data-ttu-id="8a2c5-170">Ouvrez *MainWindow.xaml*.</span><span class="sxs-lookup"><span data-stu-id="8a2c5-170">Open *MainWindow.xaml*.</span></span>

5. <span data-ttu-id="8a2c5-171">Définir le <xref:System.Windows.Navigation.NavigationWindow.Source%2A> propriété sur le <xref:System.Windows.Navigation.NavigationWindow> à «`ExpenseItHome.xaml`».</span><span class="sxs-lookup"><span data-stu-id="8a2c5-171">Set the <xref:System.Windows.Navigation.NavigationWindow.Source%2A> property on the <xref:System.Windows.Navigation.NavigationWindow> to "`ExpenseItHome.xaml`".</span></span>

    <span data-ttu-id="8a2c5-172">Cela définit *`ExpenseItHome.xaml`* être la première page ouverte au démarrage de l’application.</span><span class="sxs-lookup"><span data-stu-id="8a2c5-172">This sets *`ExpenseItHome.xaml`* to be the first page opened when the application starts.</span></span> <span data-ttu-id="8a2c5-173">Votre XAML doit ressembler à ceci en Visual Basic :</span><span class="sxs-lookup"><span data-stu-id="8a2c5-173">Your XAML should look like this in Visual Basic:</span></span>

    [!code-xaml[ExpenseIt#7_A](~/samples/snippets/visualbasic/VS_Snippets_Wpf/ExpenseIt/VB/ExpenseIt1_A/MainWindow.xaml#7_a)]

    <span data-ttu-id="8a2c5-174">Ou à cela en C# :</span><span class="sxs-lookup"><span data-stu-id="8a2c5-174">Or this in C#:</span></span>

    [!code-xaml[ExpenseIt#7](~/samples/snippets/csharp/VS_Snippets_Wpf/ExpenseIt/CSharp/ExpenseIt2/MainWindow.xaml#7)]

   > [!TIP]
   > <span data-ttu-id="8a2c5-175">Vous pouvez également définir le **Source** propriété dans le **divers** catégorie de la **propriétés** fenêtre.</span><span class="sxs-lookup"><span data-stu-id="8a2c5-175">You can also set the **Source** property in the **Miscellaneous** category of the **Properties** window.</span></span>
   >
   > ![Propriété de source dans la fenêtre Propriétés](./media/properties-source.png)

6. <span data-ttu-id="8a2c5-177">Ajoutez une autre nouvelle page WPF au projet et nommez-le *ExpenseReportPage.xaml*::</span><span class="sxs-lookup"><span data-stu-id="8a2c5-177">Add another new WPF page to the project, and name it *ExpenseReportPage.xaml*::</span></span>

   1. <span data-ttu-id="8a2c5-178">Dans **l’Explorateur de solutions**, avec le bouton droit sur le **`ExpenseIt`** nœud de projet et choisissez **ajouter** > **Page**.</span><span class="sxs-lookup"><span data-stu-id="8a2c5-178">In **Solution Explorer**, right-click on the **`ExpenseIt`** project node and choose **Add** > **Page**.</span></span>

   1. <span data-ttu-id="8a2c5-179">Dans le **ajouter un nouvel élément** boîte de dialogue, le **Page (WPF)** modèle est déjà sélectionné.</span><span class="sxs-lookup"><span data-stu-id="8a2c5-179">In the **Add New Item** dialog, the **Page (WPF)** template is already selected.</span></span> <span data-ttu-id="8a2c5-180">Entrez le nom **ExpenseReportPage**, puis sélectionnez **ajouter**.</span><span class="sxs-lookup"><span data-stu-id="8a2c5-180">Enter the name **ExpenseReportPage**, and then select **Add**.</span></span>

    <span data-ttu-id="8a2c5-181">Cette page affiche la note de frais pour la personne sélectionnée sur le **`ExpenseItHome`** page.</span><span class="sxs-lookup"><span data-stu-id="8a2c5-181">This page will show the expense report for the person that is selected on the **`ExpenseItHome`** page.</span></span>

7. <span data-ttu-id="8a2c5-182">Ouvrez *ExpenseReportPage.xaml*.</span><span class="sxs-lookup"><span data-stu-id="8a2c5-182">Open *ExpenseReportPage.xaml*.</span></span>

8. <span data-ttu-id="8a2c5-183">Définir le <xref:System.Windows.Controls.Page.Title%2A> à «`ExpenseIt - View Expense`».</span><span class="sxs-lookup"><span data-stu-id="8a2c5-183">Set the <xref:System.Windows.Controls.Page.Title%2A> to "`ExpenseIt - View Expense`".</span></span>

    <span data-ttu-id="8a2c5-184">Votre XAML doit ressembler à ceci en Visual Basic :</span><span class="sxs-lookup"><span data-stu-id="8a2c5-184">Your XAML should look like this in Visual Basic:</span></span>

    [!code-xaml[ExpenseIt#4_A](~/samples/snippets/visualbasic/VS_Snippets_Wpf/ExpenseIt/VB/ExpenseIt1_A/ExpenseReportPage.xaml#4_a)]

    <span data-ttu-id="8a2c5-185">Ou à cela en C# :</span><span class="sxs-lookup"><span data-stu-id="8a2c5-185">Or this in C#:</span></span>

    [!code-xaml[ExpenseIt#4](~/samples/snippets/csharp/VS_Snippets_Wpf/ExpenseIt/CSharp/ExpenseIt/ExpenseReportPage.xaml#4)]

9. <span data-ttu-id="8a2c5-186">Ouvrez *ExpenseItHome.xaml.vb* et *ExpenseReportPage.xaml.vb*, ou *ExpenseItHome.xaml.cs* et *ExpenseReportPage.xaml.cs*.</span><span class="sxs-lookup"><span data-stu-id="8a2c5-186">Open *ExpenseItHome.xaml.vb* and *ExpenseReportPage.xaml.vb*, or *ExpenseItHome.xaml.cs* and *ExpenseReportPage.xaml.cs*.</span></span>

    <span data-ttu-id="8a2c5-187">Lorsque vous créez un nouveau fichier de Page, Visual Studio crée automatiquement un *code-behind* fichier.</span><span class="sxs-lookup"><span data-stu-id="8a2c5-187">When you create a new Page file, Visual Studio automatically creates a *code-behind* file.</span></span> <span data-ttu-id="8a2c5-188">Ces fichiers code-behind gèrent la logique pour répondre à une saisie de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="8a2c5-188">These code-behind files handle the logic for responding to user input.</span></span>

    <span data-ttu-id="8a2c5-189">Votre code doit ressembler à ceci pour **`ExpenseItHome`**:</span><span class="sxs-lookup"><span data-stu-id="8a2c5-189">Your code should look like this for **`ExpenseItHome`**:</span></span>

    [!code-csharp[ExpenseIt#2_5](~/samples/snippets/csharp/VS_Snippets_Wpf/ExpenseIt/CSharp/ExpenseIt2/ExpenseItHome.xaml.cs#2_5)]
    [!code-vb[ExpenseIt#2_5](~/samples/snippets/visualbasic/VS_Snippets_Wpf/ExpenseIt/VB/ExpenseIt1_A/ExpenseItHome.xaml.vb#2_5)]

    <span data-ttu-id="8a2c5-190">Et comme suit pour **ExpenseReportPage**:</span><span class="sxs-lookup"><span data-stu-id="8a2c5-190">And like this for **ExpenseReportPage**:</span></span>

    [!code-csharp[ExpenseIt#5](~/samples/snippets/csharp/VS_Snippets_Wpf/ExpenseIt/CSharp/ExpenseIt/ExpenseReportPage.xaml.cs#5)]
    [!code-vb[ExpenseIt#5](~/samples/snippets/visualbasic/VS_Snippets_Wpf/ExpenseIt/VB/ExpenseIt1_A/ExpenseReportPage.xaml.vb#5)]

10. <span data-ttu-id="8a2c5-191">Ajouter une image nommée *watermark.png* au projet.</span><span class="sxs-lookup"><span data-stu-id="8a2c5-191">Add an image named *watermark.png* to the project.</span></span> <span data-ttu-id="8a2c5-192">Vous pouvez créer votre propre image, copiez le fichier à partir de l’exemple de code ou obtenez-le [ici](https://github.com/dotnet/docs/blob/master/docs/framework/wpf/getting-started/./media/watermark.png).</span><span class="sxs-lookup"><span data-stu-id="8a2c5-192">You can create your own image, copy the file from the sample code, or get it [here](https://github.com/dotnet/docs/blob/master/docs/framework/wpf/getting-started/./media/watermark.png).</span></span>

    1. <span data-ttu-id="8a2c5-193">Avec le bouton droit sur le nœud du projet et sélectionnez **ajouter** > **élément existant**, ou appuyez sur **MAJ**+**Alt** + **A**.</span><span class="sxs-lookup"><span data-stu-id="8a2c5-193">Right-click on the project node and select **Add** > **Existing Item**, or press **Shift**+**Alt**+**A**.</span></span>

    2. <span data-ttu-id="8a2c5-194">Dans le **ajouter un élément existant** boîte de dialogue, accédez au fichier image que vous souhaitez utiliser, puis sélectionnez **ajouter**.</span><span class="sxs-lookup"><span data-stu-id="8a2c5-194">In the **Add Existing Item** dialog, browse to the image file you want to use, and then select **Add**.</span></span>

## <a name="build-and-run-the-application"></a><span data-ttu-id="8a2c5-195">Générez et exécutez l'application.</span><span class="sxs-lookup"><span data-stu-id="8a2c5-195">Build and run the application</span></span>

1. <span data-ttu-id="8a2c5-196">Pour générer et exécuter l’application, appuyez sur **F5** ou sélectionnez **démarrer le débogage** à partir de la **déboguer** menu.</span><span class="sxs-lookup"><span data-stu-id="8a2c5-196">To build and run the application, press **F5** or select **Start Debugging** from the **Debug** menu.</span></span>

    <span data-ttu-id="8a2c5-197">L’illustration suivante montre l’application avec le <xref:System.Windows.Navigation.NavigationWindow> boutons :</span><span class="sxs-lookup"><span data-stu-id="8a2c5-197">The following illustration shows the application with the <xref:System.Windows.Navigation.NavigationWindow> buttons:</span></span>

    ![Capture d’écran exemple ExpenseIt](./media/gettingstartedfigure1.png)

2. <span data-ttu-id="8a2c5-199">Fermez l’application pour revenir à Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="8a2c5-199">Close the application to return to Visual Studio.</span></span>

## <a name="create-the-layout"></a><span data-ttu-id="8a2c5-200">Créer la disposition</span><span class="sxs-lookup"><span data-stu-id="8a2c5-200">Create the layout</span></span>

<span data-ttu-id="8a2c5-201">Mise en page offre un moyen ordonné de placer des éléments d’interface utilisateur et gère également la taille et la position de ces éléments lors du redimensionnée d’une interface utilisateur.</span><span class="sxs-lookup"><span data-stu-id="8a2c5-201">Layout provides an ordered way to place UI elements, and also manages the size and position of those elements when a UI is resized.</span></span> <span data-ttu-id="8a2c5-202">En règle générale, vous allez créer une disposition avec l’un des contrôles de disposition suivants :</span><span class="sxs-lookup"><span data-stu-id="8a2c5-202">You typically create a layout with one of the following layout controls:</span></span>

- <xref:System.Windows.Controls.Canvas>
- <xref:System.Windows.Controls.DockPanel>
- <xref:System.Windows.Controls.Grid>
- <xref:System.Windows.Controls.StackPanel>
- <xref:System.Windows.Controls.VirtualizingStackPanel>
- <xref:System.Windows.Controls.WrapPanel>

<span data-ttu-id="8a2c5-203">Chacun de ces contrôles de disposition prend en charge un type spécial de disposition pour ses éléments enfants.</span><span class="sxs-lookup"><span data-stu-id="8a2c5-203">Each of these layout controls supports a special type of layout for its child elements.</span></span> <span data-ttu-id="8a2c5-204">`ExpenseIt` pages peuvent être redimensionnés, et chaque page comporte des éléments organisés horizontalement et verticalement en même temps que d’autres éléments.</span><span class="sxs-lookup"><span data-stu-id="8a2c5-204">`ExpenseIt` pages can be resized, and each page has elements that are arranged horizontally and vertically alongside other elements.</span></span> <span data-ttu-id="8a2c5-205">Par conséquent, le <xref:System.Windows.Controls.Grid> est l’élément de disposition idéal pour l’application.</span><span class="sxs-lookup"><span data-stu-id="8a2c5-205">Consequently, the <xref:System.Windows.Controls.Grid> is the ideal layout element for the application.</span></span>

> [!TIP]
> <span data-ttu-id="8a2c5-206">Pour plus d’informations sur <xref:System.Windows.Controls.Panel> éléments, consultez [vue d’ensemble de panneaux](../controls/panels-overview.md).</span><span class="sxs-lookup"><span data-stu-id="8a2c5-206">For more information about <xref:System.Windows.Controls.Panel> elements, see [Panels overview](../controls/panels-overview.md).</span></span> <span data-ttu-id="8a2c5-207">Pour plus d’informations sur la disposition, consultez [disposition](../advanced/layout.md).</span><span class="sxs-lookup"><span data-stu-id="8a2c5-207">For more information about layout, see [Layout](../advanced/layout.md).</span></span>

<span data-ttu-id="8a2c5-208">Dans la section, vous créez une seule colonne de table avec trois lignes et une marge de 10 pixels en ajoutant des définitions de colonne et de ligne à la <xref:System.Windows.Controls.Grid> dans *`ExpenseItHome.xaml`*.</span><span class="sxs-lookup"><span data-stu-id="8a2c5-208">In the section, you create a single-column table with three rows and a 10-pixel margin by adding column and row definitions to the <xref:System.Windows.Controls.Grid> in *`ExpenseItHome.xaml`*.</span></span>

1. <span data-ttu-id="8a2c5-209">Ouvrez *`ExpenseItHome.xaml`*.</span><span class="sxs-lookup"><span data-stu-id="8a2c5-209">Open *`ExpenseItHome.xaml`*.</span></span>

2. <span data-ttu-id="8a2c5-210">Définir le <xref:System.Windows.FrameworkElement.Margin%2A> propriété sur le <xref:System.Windows.Controls.Grid> élément valeur « 10,0,10,10 » qui correspond aux marges gauche, haut, droite et bas :</span><span class="sxs-lookup"><span data-stu-id="8a2c5-210">Set the <xref:System.Windows.FrameworkElement.Margin%2A> property on the <xref:System.Windows.Controls.Grid> element to "10,0,10,10", which corresponds to left, top, right and bottom margins:</span></span>

   ```xaml
   <Grid Margin="10,0,10,10">
   ```

   > [!TIP]
   > <span data-ttu-id="8a2c5-211">Vous pouvez également définir le **marge** des valeurs dans le **propriétés** fenêtre, sous le **disposition** catégorie :</span><span class="sxs-lookup"><span data-stu-id="8a2c5-211">You can also set the **Margin** values in the **Properties** window, under the **Layout** category:</span></span>
   >
   > ![Valeurs de marge dans la fenêtre Propriétés](./media/properties-margin.png)

3. <span data-ttu-id="8a2c5-213">Ajoutez le XAML suivant entre les <xref:System.Windows.Controls.Grid> balises pour créer les définitions de ligne et de colonne :</span><span class="sxs-lookup"><span data-stu-id="8a2c5-213">Add the following XAML between the <xref:System.Windows.Controls.Grid> tags to create the row and column definitions:</span></span>

    [!code-xaml[ExpenseIt#8](~/samples/snippets/csharp/VS_Snippets_Wpf/ExpenseIt/CSharp/ExpenseIt3/ExpenseItHome.xaml#8)]

    <span data-ttu-id="8a2c5-214">Le <xref:System.Windows.Controls.RowDefinition.Height%2A> de deux lignes est définie sur <xref:System.Windows.GridLength.Auto%2A>, ce qui signifie que les lignes sont dimensionnés en fonction du contenu dans les lignes.</span><span class="sxs-lookup"><span data-stu-id="8a2c5-214">The <xref:System.Windows.Controls.RowDefinition.Height%2A> of two rows is set to <xref:System.Windows.GridLength.Auto%2A>, which means that the rows are sized based on the content in the rows.</span></span> <span data-ttu-id="8a2c5-215">La valeur par défaut <xref:System.Windows.Controls.RowDefinition.Height%2A> est <xref:System.Windows.GridUnitType.Star> dimensionnement, ce qui signifie que la hauteur de ligne est une proportion pondérée de l’espace disponible.</span><span class="sxs-lookup"><span data-stu-id="8a2c5-215">The default <xref:System.Windows.Controls.RowDefinition.Height%2A> is <xref:System.Windows.GridUnitType.Star> sizing, which means that the row height is a weighted proportion of the available space.</span></span> <span data-ttu-id="8a2c5-216">Par exemple, si deux lignes ont une <xref:System.Windows.Controls.RowDefinition.Height%2A> de « \* », ils ont chacun une hauteur qui représente la moitié de l’espace disponible.</span><span class="sxs-lookup"><span data-stu-id="8a2c5-216">For example if two rows each have a <xref:System.Windows.Controls.RowDefinition.Height%2A> of "\*", they each have a height that is half of the available space.</span></span>

    <span data-ttu-id="8a2c5-217">Votre <xref:System.Windows.Controls.Grid> doit maintenant ressembler au XAML suivant :</span><span class="sxs-lookup"><span data-stu-id="8a2c5-217">Your <xref:System.Windows.Controls.Grid> should now look like the following XAML:</span></span>

    [!code-xaml[ExpenseIt#9](~/samples/snippets/csharp/VS_Snippets_Wpf/ExpenseIt/CSharp/ExpenseIt3/ExpenseItHome.xaml#9)]

## <a name="add-controls"></a><span data-ttu-id="8a2c5-218">Ajouter des contrôles</span><span class="sxs-lookup"><span data-stu-id="8a2c5-218">Add controls</span></span>

<span data-ttu-id="8a2c5-219">Dans cette section, vous allez mettre à jour l’interface utilisateur pour afficher la liste des personnes avec lesquelles un utilisateur peut sélectionner pour afficher la note de frais pour la page d’accueil.</span><span class="sxs-lookup"><span data-stu-id="8a2c5-219">In this section, you'll update the home page UI to show a list of people that a user can select from to show the expense report for.</span></span> <span data-ttu-id="8a2c5-220">Les contrôles sont des objets d’interface utilisateur qui permettent aux utilisateurs d’interagir avec votre application.</span><span class="sxs-lookup"><span data-stu-id="8a2c5-220">Controls are UI objects that allow users to interact with your application.</span></span> <span data-ttu-id="8a2c5-221">Pour plus d’informations, consultez [Contrôles](../controls/index.md).</span><span class="sxs-lookup"><span data-stu-id="8a2c5-221">For more information, see [Controls](../controls/index.md).</span></span>

<span data-ttu-id="8a2c5-222">Pour créer cette interface utilisateur, vous allez ajouter les éléments suivants à *`ExpenseItHome.xaml`*:</span><span class="sxs-lookup"><span data-stu-id="8a2c5-222">To create this UI, you'll add the following elements to *`ExpenseItHome.xaml`*:</span></span>

- <span data-ttu-id="8a2c5-223"><xref:System.Windows.Controls.ListBox> (pour la liste de personnes).</span><span class="sxs-lookup"><span data-stu-id="8a2c5-223"><xref:System.Windows.Controls.ListBox> (for the list of people).</span></span>
- <span data-ttu-id="8a2c5-224"><xref:System.Windows.Controls.Label> (pour l’en-tête de liste).</span><span class="sxs-lookup"><span data-stu-id="8a2c5-224"><xref:System.Windows.Controls.Label> (for the list header).</span></span>
- <span data-ttu-id="8a2c5-225"><xref:System.Windows.Controls.Button> (sur lequel cliquer pour afficher la note de frais pour la personne qui est sélectionnée dans la liste).</span><span class="sxs-lookup"><span data-stu-id="8a2c5-225"><xref:System.Windows.Controls.Button> (to click to view the expense report for the person that is selected in the list).</span></span>

<span data-ttu-id="8a2c5-226">Chaque contrôle est placé dans une ligne de la <xref:System.Windows.Controls.Grid> en définissant le <xref:System.Windows.Controls.Grid.Row%2A?displayProperty=nameWithType> propriété jointe.</span><span class="sxs-lookup"><span data-stu-id="8a2c5-226">Each control is placed in a row of the <xref:System.Windows.Controls.Grid> by setting the <xref:System.Windows.Controls.Grid.Row%2A?displayProperty=nameWithType> attached property.</span></span> <span data-ttu-id="8a2c5-227">Pour plus d’informations sur les propriétés jointes, consultez [vue d’ensemble des propriétés jointes](../advanced/attached-properties-overview.md).</span><span class="sxs-lookup"><span data-stu-id="8a2c5-227">For more information about attached properties, see [Attached Properties Overview](../advanced/attached-properties-overview.md).</span></span>

1. <span data-ttu-id="8a2c5-228">Ouvrez *`ExpenseItHome.xaml`*.</span><span class="sxs-lookup"><span data-stu-id="8a2c5-228">Open *`ExpenseItHome.xaml`*.</span></span>

2. <span data-ttu-id="8a2c5-229">Ajoutez le XAML suivant quelque part entre le <xref:System.Windows.Controls.Grid> balises :</span><span class="sxs-lookup"><span data-stu-id="8a2c5-229">Add the following XAML somewhere between the <xref:System.Windows.Controls.Grid> tags:</span></span>

   [!code-xaml[ExpenseIt#10](~/samples/snippets/csharp/VS_Snippets_Wpf/ExpenseIt/CSharp/ExpenseIt4/ExpenseItHome.xaml#10)]

   > [!TIP]
   > <span data-ttu-id="8a2c5-230">Vous pouvez également créer les contrôles en les faisant glisser à partir de la **boîte à outils** fenêtre sur la fenêtre de conception, puis en définissant leurs propriétés le **propriétés** fenêtre.</span><span class="sxs-lookup"><span data-stu-id="8a2c5-230">You can also create the controls by dragging them from the **Toolbox** window onto the design window, and then setting their properties in the **Properties** window.</span></span>

3. <span data-ttu-id="8a2c5-231">Générez et exécutez l’application.</span><span class="sxs-lookup"><span data-stu-id="8a2c5-231">Build and run the application.</span></span>

<span data-ttu-id="8a2c5-232">L’illustration suivante montre les contrôles que vous venez de créer :</span><span class="sxs-lookup"><span data-stu-id="8a2c5-232">The following illustration shows the controls you just created:</span></span>

![Capture d’écran exemple ExpenseIt](./media/gettingstartedfigure2.png)

## <a name="add-an-image-and-a-title"></a><span data-ttu-id="8a2c5-234">Ajouter une image et un titre</span><span class="sxs-lookup"><span data-stu-id="8a2c5-234">Add an image and a title</span></span>

<span data-ttu-id="8a2c5-235">Dans cette section, vous allez mettre à jour l’interface utilisateur de la page d’accueil avec une image et un titre de page.</span><span class="sxs-lookup"><span data-stu-id="8a2c5-235">In this section, you'll update the home page UI with an image and a page title.</span></span>

1. <span data-ttu-id="8a2c5-236">Ouvrez *`ExpenseItHome.xaml`*.</span><span class="sxs-lookup"><span data-stu-id="8a2c5-236">Open *`ExpenseItHome.xaml`*.</span></span>

2. <span data-ttu-id="8a2c5-237">Ajouter une autre colonne à la <xref:System.Windows.Controls.Grid.ColumnDefinitions%2A> fixe <xref:System.Windows.Controls.ColumnDefinition.Width%2A> de 230 pixels :</span><span class="sxs-lookup"><span data-stu-id="8a2c5-237">Add another column to the <xref:System.Windows.Controls.Grid.ColumnDefinitions%2A> with a fixed <xref:System.Windows.Controls.ColumnDefinition.Width%2A> of 230 pixels:</span></span>

    [!code-xaml[ExpenseIt#11](~/samples/snippets/csharp/VS_Snippets_Wpf/ExpenseIt/CSharp/ExpenseIt5/ExpenseItHome.xaml#11)]

3. <span data-ttu-id="8a2c5-238">Ajouter une autre ligne à la <xref:System.Windows.Controls.Grid.RowDefinitions%2A>, pour un total de quatre lignes :</span><span class="sxs-lookup"><span data-stu-id="8a2c5-238">Add another row to the <xref:System.Windows.Controls.Grid.RowDefinitions%2A>, for a total of four rows:</span></span>

    [!code-xaml[ExpenseIt#11b](~/samples/snippets/csharp/VS_Snippets_Wpf/ExpenseIt/CSharp/ExpenseIt5/ExpenseItHome.xaml#11b)]

4. <span data-ttu-id="8a2c5-239">Déplacer les contrôles vers la deuxième colonne en définissant le <xref:System.Windows.Controls.Grid.Column%2A?displayProperty=nameWithType> propriété sur 1 dans chacun des trois contrôles (bordure, ListBox et bouton).</span><span class="sxs-lookup"><span data-stu-id="8a2c5-239">Move the controls to the second column by setting the <xref:System.Windows.Controls.Grid.Column%2A?displayProperty=nameWithType> property to 1 in each of the three controls (Border, ListBox, and Button).</span></span>

5. <span data-ttu-id="8a2c5-240">Déplacez chaque contrôle d’une ligne, vers le bas en incrémentant son <xref:System.Windows.Controls.Grid.Row%2A?displayProperty=nameWithType> valeur par 1.</span><span class="sxs-lookup"><span data-stu-id="8a2c5-240">Move each control down a row, by incrementing its <xref:System.Windows.Controls.Grid.Row%2A?displayProperty=nameWithType> value by 1.</span></span>

   <span data-ttu-id="8a2c5-241">Le XAML pour les trois contrôles ressemble maintenant à ceci :</span><span class="sxs-lookup"><span data-stu-id="8a2c5-241">The XAML for the three controls now looks like this:</span></span>

    [!code-xaml[ExpenseIt#12](~/samples/snippets/csharp/VS_Snippets_Wpf/ExpenseIt/CSharp/ExpenseIt5/ExpenseItHome.xaml#12)]

6. <span data-ttu-id="8a2c5-242">Définir le <xref:System.Windows.Controls.Panel.Background%2A> de la <xref:System.Windows.Controls.Grid> pour être le *watermark.png* fichier image, en ajoutant le XAML suivant quelque part entre le `<Grid>` et `</Grid>` balises :</span><span class="sxs-lookup"><span data-stu-id="8a2c5-242">Set the <xref:System.Windows.Controls.Panel.Background%2A> of the <xref:System.Windows.Controls.Grid> to be the *watermark.png* image file, by adding the following XAML somewhere between the `<Grid>` and `</Grid>` tags:</span></span>

    [!code-xaml[ExpenseIt#14](~/samples/snippets/csharp/VS_Snippets_Wpf/ExpenseIt/CSharp/ExpenseIt5/ExpenseItHome.xaml#14)]

7. <span data-ttu-id="8a2c5-243">Avant du <xref:System.Windows.Controls.Border> élément, ajoutez un <xref:System.Windows.Controls.Label> avec le contenu « View Expense Report ».</span><span class="sxs-lookup"><span data-stu-id="8a2c5-243">Before the <xref:System.Windows.Controls.Border> element, add a <xref:System.Windows.Controls.Label> with the content "View Expense Report".</span></span> <span data-ttu-id="8a2c5-244">Il s’agit du titre de la page.</span><span class="sxs-lookup"><span data-stu-id="8a2c5-244">This is the title of the page.</span></span>

    [!code-xaml[ExpenseIt#13](~/samples/snippets/csharp/VS_Snippets_Wpf/ExpenseIt/CSharp/ExpenseIt5/ExpenseItHome.xaml#13)]

8. <span data-ttu-id="8a2c5-245">Générez et exécutez l’application.</span><span class="sxs-lookup"><span data-stu-id="8a2c5-245">Build and run the application.</span></span>

<span data-ttu-id="8a2c5-246">L’illustration suivante montre les résultats de ce que vous venez d’ajouter :</span><span class="sxs-lookup"><span data-stu-id="8a2c5-246">The following illustration shows the results of what you just added:</span></span>

![Capture d’écran exemple ExpenseIt](./media/gettingstartedfigure3.png)

## <a name="add-code-to-handle-events"></a><span data-ttu-id="8a2c5-248">Ajoutez du code pour gérer les événements</span><span class="sxs-lookup"><span data-stu-id="8a2c5-248">Add code to handle events</span></span>

1. <span data-ttu-id="8a2c5-249">Ouvrez *`ExpenseItHome.xaml`*.</span><span class="sxs-lookup"><span data-stu-id="8a2c5-249">Open *`ExpenseItHome.xaml`*.</span></span>

2. <span data-ttu-id="8a2c5-250">Ajouter un <xref:System.Windows.Controls.Primitives.ButtonBase.Click> Gestionnaire d’événements à la <xref:System.Windows.Controls.Button> élément.</span><span class="sxs-lookup"><span data-stu-id="8a2c5-250">Add a <xref:System.Windows.Controls.Primitives.ButtonBase.Click> event handler to the <xref:System.Windows.Controls.Button> element.</span></span> <span data-ttu-id="8a2c5-251">Pour plus d'informations, voir [Procédure : Créez un gestionnaire d’événements simple](https://docs.microsoft.com/previous-versions/visualstudio/visual-studio-2010/bb675300(v=vs.100)).</span><span class="sxs-lookup"><span data-stu-id="8a2c5-251">For more information, see [How to: Create a simple event handler](https://docs.microsoft.com/previous-versions/visualstudio/visual-studio-2010/bb675300(v=vs.100)).</span></span>

    [!code-xaml[ExpenseIt#15](~/samples/snippets/csharp/VS_Snippets_Wpf/ExpenseIt/CSharp/ExpenseIt6/ExpenseItHome.xaml#15)]

3. <span data-ttu-id="8a2c5-252">Ouvrez *`ExpenseItHome.xaml.vb`* ou *`ExpenseItHome.xaml.cs`*.</span><span class="sxs-lookup"><span data-stu-id="8a2c5-252">Open *`ExpenseItHome.xaml.vb`* or *`ExpenseItHome.xaml.cs`*.</span></span>

4. <span data-ttu-id="8a2c5-253">Ajoutez le code suivant à la `ExpenseItHome` classe pour ajouter un bouton Gestionnaire d’événements click.</span><span class="sxs-lookup"><span data-stu-id="8a2c5-253">Add the following code to the `ExpenseItHome` class to add a button click event handler.</span></span> <span data-ttu-id="8a2c5-254">Le Gestionnaire d’événements ouvre le **ExpenseReportPage** page.</span><span class="sxs-lookup"><span data-stu-id="8a2c5-254">The event handler opens the **ExpenseReportPage** page.</span></span>

    [!code-csharp[ExpenseIt#16](~/samples/snippets/csharp/VS_Snippets_Wpf/ExpenseIt/CSharp/ExpenseIt6/ExpenseItHome.xaml.cs#16)]
    [!code-vb[ExpenseIt#16](~/samples/snippets/visualbasic/VS_Snippets_Wpf/ExpenseIt/VB/ExpenseIt6/ExpenseItHome.xaml.vb#16)]

## <a name="create-the-ui-for-expensereportpage"></a><span data-ttu-id="8a2c5-255">Créer l’interface utilisateur pour ExpenseReportPage</span><span class="sxs-lookup"><span data-stu-id="8a2c5-255">Create the UI for ExpenseReportPage</span></span>

<span data-ttu-id="8a2c5-256">*ExpenseReportPage.xaml* affiche la note de frais de la personne qui est sélectionnée sur la **`ExpenseItHome`** page.</span><span class="sxs-lookup"><span data-stu-id="8a2c5-256">*ExpenseReportPage.xaml* displays the expense report for the person that's selected on the **`ExpenseItHome`** page.</span></span> <span data-ttu-id="8a2c5-257">Dans cette section, vous allez créer l’interface utilisateur pour **ExpenseReportPage**.</span><span class="sxs-lookup"><span data-stu-id="8a2c5-257">In this section, you'll create the UI for **ExpenseReportPage**.</span></span> <span data-ttu-id="8a2c5-258">Vous également ajouter d’arrière-plan et les couleurs aux divers éléments d’interface utilisateur de remplissage.</span><span class="sxs-lookup"><span data-stu-id="8a2c5-258">You'll also add background and fill colors to the various UI elements.</span></span>

1. <span data-ttu-id="8a2c5-259">Ouvrez *ExpenseReportPage.xaml*.</span><span class="sxs-lookup"><span data-stu-id="8a2c5-259">Open *ExpenseReportPage.xaml*.</span></span>

2. <span data-ttu-id="8a2c5-260">Ajoutez le XAML suivant entre les <xref:System.Windows.Controls.Grid> balises :</span><span class="sxs-lookup"><span data-stu-id="8a2c5-260">Add the following XAML between the <xref:System.Windows.Controls.Grid> tags:</span></span>

    [!code-xaml[ExpenseIt#17](~/samples/snippets/csharp/VS_Snippets_Wpf/ExpenseIt/CSharp/ExpenseIt6/ExpenseReportPage.xaml#17)]

    <span data-ttu-id="8a2c5-261">Cette interface utilisateur est similaire à *`ExpenseItHome.xaml`*, sauf que les données du rapport s’affiche dans un <xref:System.Windows.Controls.DataGrid>.</span><span class="sxs-lookup"><span data-stu-id="8a2c5-261">This UI is similar to *`ExpenseItHome.xaml`*, except the report data is displayed in a <xref:System.Windows.Controls.DataGrid>.</span></span>

3. <span data-ttu-id="8a2c5-262">Générez et exécutez l’application.</span><span class="sxs-lookup"><span data-stu-id="8a2c5-262">Build and run the application.</span></span>

    > [!NOTE]
    > <span data-ttu-id="8a2c5-263">Si vous obtenez une erreur le <xref:System.Windows.Controls.DataGrid> est introuvable ou n’existe pas, vérifiez que votre projet cible le .NET Framework 4 ou version ultérieur.</span><span class="sxs-lookup"><span data-stu-id="8a2c5-263">If you get an error that the <xref:System.Windows.Controls.DataGrid> was not found or does not exist, make sure that your project targets the .NET Framework 4 or later.</span></span> <span data-ttu-id="8a2c5-264">Pour plus d'informations, voir [Procédure : Cibler une version du .NET Framework](/visualstudio/ide/how-to-target-a-version-of-the-dotnet-framework).</span><span class="sxs-lookup"><span data-stu-id="8a2c5-264">For more information, see [How to: Target a Version of the .NET Framework](/visualstudio/ide/how-to-target-a-version-of-the-dotnet-framework).</span></span>

4. <span data-ttu-id="8a2c5-265">Sélectionnez le **vue** bouton.</span><span class="sxs-lookup"><span data-stu-id="8a2c5-265">Select the **View** button.</span></span>

    <span data-ttu-id="8a2c5-266">La page de note de frais s’affiche.</span><span class="sxs-lookup"><span data-stu-id="8a2c5-266">The expense report page appears.</span></span> <span data-ttu-id="8a2c5-267">Notez également que le bouton de navigation arrière est activé.</span><span class="sxs-lookup"><span data-stu-id="8a2c5-267">Also notice that the back navigation button is enabled.</span></span>

<span data-ttu-id="8a2c5-268">L’illustration suivante montre les éléments d’interface utilisateur ajoutés à *ExpenseReportPage.xaml*.</span><span class="sxs-lookup"><span data-stu-id="8a2c5-268">The following illustration shows the UI elements added to *ExpenseReportPage.xaml*.</span></span>

![Capture d’écran exemple ExpenseIt](./media/gettingstartedfigure4.png)

## <a name="style-controls"></a><span data-ttu-id="8a2c5-270">Style aux contrôles</span><span class="sxs-lookup"><span data-stu-id="8a2c5-270">Style controls</span></span>

<span data-ttu-id="8a2c5-271">L’apparence des différents éléments est souvent le même pour tous les éléments du même type dans une interface utilisateur.</span><span class="sxs-lookup"><span data-stu-id="8a2c5-271">The appearance of various elements is often the same for all elements of the same type in a UI.</span></span> <span data-ttu-id="8a2c5-272">Utilise l’interface utilisateur [styles](../controls/styling-and-templating.md) pour pouvoir réutiliser l’apparence des différents éléments.</span><span class="sxs-lookup"><span data-stu-id="8a2c5-272">UI uses [styles](../controls/styling-and-templating.md) to make appearances reusable across multiple elements.</span></span> <span data-ttu-id="8a2c5-273">La réutilisation des styles permet de simplifier la gestion et la création de XAML.</span><span class="sxs-lookup"><span data-stu-id="8a2c5-273">The reusability of styles helps to simplify XAML creation and management.</span></span> <span data-ttu-id="8a2c5-274">Cette section remplace par des styles les attributs d’élément qui ont été définis lors des étapes précédentes.</span><span class="sxs-lookup"><span data-stu-id="8a2c5-274">This section replaces the per-element attributes that were defined in previous steps with styles.</span></span>

1. <span data-ttu-id="8a2c5-275">Ouvrez *Application.xaml* ou *App.xaml*.</span><span class="sxs-lookup"><span data-stu-id="8a2c5-275">Open *Application.xaml* or *App.xaml*.</span></span>

2. <span data-ttu-id="8a2c5-276">Ajoutez le XAML suivant entre les <xref:System.Windows.Application.Resources%2A?displayProperty=nameWithType> balises :</span><span class="sxs-lookup"><span data-stu-id="8a2c5-276">Add the following XAML between the <xref:System.Windows.Application.Resources%2A?displayProperty=nameWithType> tags:</span></span>

    [!code-xaml[ExpenseIt#18](~/samples/snippets/csharp/VS_Snippets_Wpf/ExpenseIt/CSharp/ExpenseIt7/App.xaml#18)]

    <span data-ttu-id="8a2c5-277">Ce code XAML ajoute les styles suivants :</span><span class="sxs-lookup"><span data-stu-id="8a2c5-277">This XAML adds the following styles:</span></span>

    - <span data-ttu-id="8a2c5-278">`headerTextStyle`: Pour mettre en forme le titre de la page <xref:System.Windows.Controls.Label>.</span><span class="sxs-lookup"><span data-stu-id="8a2c5-278">`headerTextStyle`: To format the page title <xref:System.Windows.Controls.Label>.</span></span>

    - <span data-ttu-id="8a2c5-279">`labelStyle`: Pour mettre en forme le <xref:System.Windows.Controls.Label> contrôles.</span><span class="sxs-lookup"><span data-stu-id="8a2c5-279">`labelStyle`: To format the <xref:System.Windows.Controls.Label> controls.</span></span>

    - <span data-ttu-id="8a2c5-280">`columnHeaderStyle`: Pour mettre en forme le <xref:System.Windows.Controls.Primitives.DataGridColumnHeader>.</span><span class="sxs-lookup"><span data-stu-id="8a2c5-280">`columnHeaderStyle`: To format the <xref:System.Windows.Controls.Primitives.DataGridColumnHeader>.</span></span>

    - <span data-ttu-id="8a2c5-281">`listHeaderStyle`: Pour mettre en forme l’en-tête de liste <xref:System.Windows.Controls.Border> contrôles.</span><span class="sxs-lookup"><span data-stu-id="8a2c5-281">`listHeaderStyle`: To format the list header <xref:System.Windows.Controls.Border> controls.</span></span>

    - <span data-ttu-id="8a2c5-282">`listHeaderTextStyle`: Pour mettre en forme l’en-tête de liste <xref:System.Windows.Controls.Label>.</span><span class="sxs-lookup"><span data-stu-id="8a2c5-282">`listHeaderTextStyle`: To format the list header <xref:System.Windows.Controls.Label>.</span></span>

    - <span data-ttu-id="8a2c5-283">`buttonStyle`: Pour mettre en forme le <xref:System.Windows.Controls.Button> sur `ExpenseItHome.xaml`.</span><span class="sxs-lookup"><span data-stu-id="8a2c5-283">`buttonStyle`: To format the <xref:System.Windows.Controls.Button> on `ExpenseItHome.xaml`.</span></span>

    <span data-ttu-id="8a2c5-284">Notez que les styles sont des ressources et des enfants de le <xref:System.Windows.Application.Resources%2A?displayProperty=nameWithType> élément de propriété.</span><span class="sxs-lookup"><span data-stu-id="8a2c5-284">Notice that the styles are resources and children of the <xref:System.Windows.Application.Resources%2A?displayProperty=nameWithType> property element.</span></span> <span data-ttu-id="8a2c5-285">À cet emplacement, les styles sont appliqués à tous les éléments d’une application.</span><span class="sxs-lookup"><span data-stu-id="8a2c5-285">In this location, the styles are applied to all the elements in an application.</span></span> <span data-ttu-id="8a2c5-286">Pour obtenir un exemple d’utilisation des ressources dans une application .NET Framework, consultez [utiliser les ressources Application](../advanced/how-to-use-application-resources.md).</span><span class="sxs-lookup"><span data-stu-id="8a2c5-286">For an example of using resources in a .NET Framework application, see [Use Application Resources](../advanced/how-to-use-application-resources.md).</span></span>

3. <span data-ttu-id="8a2c5-287">Ouvrez *`ExpenseItHome.xaml`*.</span><span class="sxs-lookup"><span data-stu-id="8a2c5-287">Open *`ExpenseItHome.xaml`*.</span></span>

4. <span data-ttu-id="8a2c5-288">Remplacez tout le contenu entre le <xref:System.Windows.Controls.Grid> éléments avec le XAML suivant :</span><span class="sxs-lookup"><span data-stu-id="8a2c5-288">Replace everything between the <xref:System.Windows.Controls.Grid> elements with the following XAML:</span></span>

    [!code-xaml[ExpenseIt#19](~/samples/snippets/csharp/VS_Snippets_Wpf/ExpenseIt/CSharp/ExpenseIt7/ExpenseItHome.xaml#19)]

    <span data-ttu-id="8a2c5-289">Les propriétés qui définissent l’apparence de chaque contrôle, comme <xref:System.Windows.VerticalAlignment> et <xref:System.Windows.Media.FontFamily> , sont supprimées et remplacées lors de l’application de styles.</span><span class="sxs-lookup"><span data-stu-id="8a2c5-289">The properties such as <xref:System.Windows.VerticalAlignment> and <xref:System.Windows.Media.FontFamily> that define the look of each control are removed and replaced by applying the styles.</span></span> <span data-ttu-id="8a2c5-290">Par exemple, le `headerTextStyle` est appliqué à la « View Expense Report » <xref:System.Windows.Controls.Label>.</span><span class="sxs-lookup"><span data-stu-id="8a2c5-290">For example, the `headerTextStyle` is applied to the "View Expense Report" <xref:System.Windows.Controls.Label>.</span></span>

5. <span data-ttu-id="8a2c5-291">Ouvrez *ExpenseReportPage.xaml*.</span><span class="sxs-lookup"><span data-stu-id="8a2c5-291">Open *ExpenseReportPage.xaml*.</span></span>

6. <span data-ttu-id="8a2c5-292">Remplacez tout le contenu entre le <xref:System.Windows.Controls.Grid> éléments avec le XAML suivant :</span><span class="sxs-lookup"><span data-stu-id="8a2c5-292">Replace everything between the <xref:System.Windows.Controls.Grid> elements with the following XAML:</span></span>

    [!code-xaml[ExpenseIt#20](~/samples/snippets/csharp/VS_Snippets_Wpf/ExpenseIt/CSharp/ExpenseIt7/ExpenseReportPage.xaml#20)]

    <span data-ttu-id="8a2c5-293">Des styles sont ajoutés aux éléments <xref:System.Windows.Controls.Label> et <xref:System.Windows.Controls.Border> .</span><span class="sxs-lookup"><span data-stu-id="8a2c5-293">This adds styles to the <xref:System.Windows.Controls.Label> and <xref:System.Windows.Controls.Border> elements.</span></span>

## <a name="bind-data-to-a-control"></a><span data-ttu-id="8a2c5-294">Lier des données à un contrôle</span><span class="sxs-lookup"><span data-stu-id="8a2c5-294">Bind data to a control</span></span>

<span data-ttu-id="8a2c5-295">Dans cette section, vous allez créer les données XML qui sont liées à différents contrôles.</span><span class="sxs-lookup"><span data-stu-id="8a2c5-295">In this section, you'll create the XML data that is bound to various controls.</span></span>

1. <span data-ttu-id="8a2c5-296">Ouvrez *`ExpenseItHome.xaml`*.</span><span class="sxs-lookup"><span data-stu-id="8a2c5-296">Open *`ExpenseItHome.xaml`*.</span></span>

2. <span data-ttu-id="8a2c5-297">Après l’ouverture <xref:System.Windows.Controls.Grid> élément, ajoutez le XAML suivant pour créer un <xref:System.Windows.Data.XmlDataProvider> qui contient les données pour chaque personne :</span><span class="sxs-lookup"><span data-stu-id="8a2c5-297">After the opening <xref:System.Windows.Controls.Grid> element, add the following XAML to create an <xref:System.Windows.Data.XmlDataProvider> that contains the data for each person:</span></span>

    [!code-xaml[ExpenseIt#21](~/samples/snippets/csharp/VS_Snippets_Wpf/ExpenseIt/CSharp/ExpenseIt8/ExpenseItHome.xaml#21)]
    [!code-xaml[ExpenseIt#23](~/samples/snippets/csharp/VS_Snippets_Wpf/ExpenseIt/CSharp/ExpenseIt8/ExpenseItHome.xaml#23)]
    [!code-xaml[ExpenseIt#22](~/samples/snippets/csharp/VS_Snippets_Wpf/ExpenseIt/CSharp/ExpenseIt8/ExpenseItHome.xaml#22)]

    <span data-ttu-id="8a2c5-298">Les données sont créées en tant qu’un <xref:System.Windows.Controls.Grid> ressource.</span><span class="sxs-lookup"><span data-stu-id="8a2c5-298">The data is created as a <xref:System.Windows.Controls.Grid> resource.</span></span> <span data-ttu-id="8a2c5-299">Les données sont normalement chargées en tant que fichier, mais pour des raisons pratiques, elles sont ajoutées inline.</span><span class="sxs-lookup"><span data-stu-id="8a2c5-299">Normally this would be loaded as a file, but for simplicity the data is added inline.</span></span>

3. <span data-ttu-id="8a2c5-300">Dans le `<Grid.Resources>` élément, ajoutez le code suivant <xref:System.Windows.DataTemplate>, qui définit comment afficher les données dans le <xref:System.Windows.Controls.ListBox>:</span><span class="sxs-lookup"><span data-stu-id="8a2c5-300">Within the `<Grid.Resources>` element, add the following <xref:System.Windows.DataTemplate>, which defines how to display the data in the <xref:System.Windows.Controls.ListBox>:</span></span>

    [!code-xaml[ExpenseIt#21](~/samples/snippets/csharp/VS_Snippets_Wpf/ExpenseIt/CSharp/ExpenseIt8/ExpenseItHome.xaml#21)]
    [!code-xaml[ExpenseIt#24](~/samples/snippets/csharp/VS_Snippets_Wpf/ExpenseIt/CSharp/ExpenseIt8/ExpenseItHome.xaml#24)]
    [!code-xaml[ExpenseIt#22](~/samples/snippets/csharp/VS_Snippets_Wpf/ExpenseIt/CSharp/ExpenseIt8/ExpenseItHome.xaml#22)]

    <span data-ttu-id="8a2c5-301">Pour plus d’informations sur les modèles de données, consultez [vue d’ensemble de création de modèles de données](../data/data-templating-overview.md).</span><span class="sxs-lookup"><span data-stu-id="8a2c5-301">For more information about data templates, see [Data templating overview](../data/data-templating-overview.md).</span></span>

4. <span data-ttu-id="8a2c5-302">Remplacer la <xref:System.Windows.Controls.ListBox> avec le XAML suivant :</span><span class="sxs-lookup"><span data-stu-id="8a2c5-302">Replace the existing <xref:System.Windows.Controls.ListBox> with the following XAML:</span></span>

    [!code-xaml[ExpenseIt#25](~/samples/snippets/csharp/VS_Snippets_Wpf/ExpenseIt/CSharp/ExpenseIt8/ExpenseItHome.xaml#25)]

    <span data-ttu-id="8a2c5-303">Ce XAML lie le <xref:System.Windows.Controls.ItemsControl.ItemsSource%2A> propriété de la <xref:System.Windows.Controls.ListBox> à la source de données et applique le modèle de données en tant que le <xref:System.Windows.Controls.ItemsControl.ItemTemplate%2A>.</span><span class="sxs-lookup"><span data-stu-id="8a2c5-303">This XAML binds the <xref:System.Windows.Controls.ItemsControl.ItemsSource%2A> property of the <xref:System.Windows.Controls.ListBox> to the data source and applies the data template as the <xref:System.Windows.Controls.ItemsControl.ItemTemplate%2A>.</span></span>

## <a name="connect-data-to-controls"></a><span data-ttu-id="8a2c5-304">Connectez des données aux contrôles</span><span class="sxs-lookup"><span data-stu-id="8a2c5-304">Connect data to controls</span></span>

<span data-ttu-id="8a2c5-305">Ensuite, vous ajouterez du code pour récupérer le nom qui est sélectionné sur la **`ExpenseItHome`** page et le passer au constructeur de **ExpenseReportPage**.</span><span class="sxs-lookup"><span data-stu-id="8a2c5-305">Next, you'll add code to retrieve the name that's selected on the **`ExpenseItHome`** page and pass it to the constructor of **ExpenseReportPage**.</span></span> <span data-ttu-id="8a2c5-306">**ExpenseReportPage** définit son contexte de données avec l’élément passé, ce qui est définie par les contrôles dans *ExpenseReportPage.xaml* lier à.</span><span class="sxs-lookup"><span data-stu-id="8a2c5-306">**ExpenseReportPage** sets its data context with the passed item, which is what the controls defined in *ExpenseReportPage.xaml* bind to.</span></span>

1. <span data-ttu-id="8a2c5-307">Ouvrez *ExpenseReportPage.xaml.vb* ou *ExpenseReportPage.xaml.cs*.</span><span class="sxs-lookup"><span data-stu-id="8a2c5-307">Open *ExpenseReportPage.xaml.vb* or *ExpenseReportPage.xaml.cs*.</span></span>

2. <span data-ttu-id="8a2c5-308">Ajoutez un constructeur qui prend un objet de façon à pouvoir transmettre les données de note de frais de la personne sélectionnée.</span><span class="sxs-lookup"><span data-stu-id="8a2c5-308">Add a constructor that takes an object so you can pass the expense report data of the selected person.</span></span>

    [!code-csharp[ExpenseIt#26](~/samples/snippets/csharp/VS_Snippets_Wpf/ExpenseIt/CSharp/ExpenseIt8/ExpenseReportPage.xaml.cs#26)]
    [!code-vb[ExpenseIt#26](~/samples/snippets/visualbasic/VS_Snippets_Wpf/ExpenseIt/VB/ExpenseIt8/ExpenseReportPage.xaml.vb#26)]

3. <span data-ttu-id="8a2c5-309">Ouvrez *`ExpenseItHome.xaml.vb`* ou *`ExpenseItHome.xaml.cs`*.</span><span class="sxs-lookup"><span data-stu-id="8a2c5-309">Open *`ExpenseItHome.xaml.vb`* or *`ExpenseItHome.xaml.cs`*.</span></span>

4. <span data-ttu-id="8a2c5-310">Modifier le <xref:System.Windows.Controls.Primitives.ButtonBase.Click> Gestionnaire d’événements pour appeler le nouveau constructeur en passant les données de rapport de frais de la personne sélectionnée.</span><span class="sxs-lookup"><span data-stu-id="8a2c5-310">Change the <xref:System.Windows.Controls.Primitives.ButtonBase.Click> event handler to call the new constructor passing the expense report data of the selected person.</span></span>

    [!code-csharp[ExpenseIt#27](~/samples/snippets/csharp/VS_Snippets_Wpf/ExpenseIt/CSharp/ExpenseIt8/ExpenseItHome.xaml.cs#27)]
    [!code-vb[ExpenseIt#27](~/samples/snippets/visualbasic/VS_Snippets_Wpf/ExpenseIt/VB/ExpenseIt8/ExpenseItHome.xaml.vb#27)]

## <a name="style-data-with-data-templates"></a><span data-ttu-id="8a2c5-311">Données de style avec les modèles de données</span><span class="sxs-lookup"><span data-stu-id="8a2c5-311">Style data with data templates</span></span>

<span data-ttu-id="8a2c5-312">Dans cette section, vous allez mettre à jour l’interface utilisateur pour chaque élément dans les listes liées aux données à l’aide de modèles de données.</span><span class="sxs-lookup"><span data-stu-id="8a2c5-312">In this section, you'll update the UI for each item in the data-bound lists by using data templates.</span></span>

1. <span data-ttu-id="8a2c5-313">Ouvrez *ExpenseReportPage.xaml*.</span><span class="sxs-lookup"><span data-stu-id="8a2c5-313">Open *ExpenseReportPage.xaml*.</span></span>

2. <span data-ttu-id="8a2c5-314">Lier le contenu de la « Name » et « Department » <xref:System.Windows.Controls.Label> éléments pour les données appropriées de propriété source.</span><span class="sxs-lookup"><span data-stu-id="8a2c5-314">Bind the content of the "Name" and "Department" <xref:System.Windows.Controls.Label> elements to the appropriate data source property.</span></span> <span data-ttu-id="8a2c5-315">Pour plus d’informations sur la liaison de données, consultez [vue d’ensemble de liaison de données](../data/data-binding-overview.md).</span><span class="sxs-lookup"><span data-stu-id="8a2c5-315">For more information about data binding, see [Data binding overview](../data/data-binding-overview.md).</span></span>

    [!code-xaml[ExpenseIt#31](~/samples/snippets/csharp/VS_Snippets_Wpf/ExpenseIt/CSharp/ExpenseIt9/ExpenseReportPage.xaml#31)]

3. <span data-ttu-id="8a2c5-316">Après l’ouverture <xref:System.Windows.Controls.Grid> élément, ajoutez les modèles de données suivants, qui définissent comment afficher les données de rapport de frais :</span><span class="sxs-lookup"><span data-stu-id="8a2c5-316">After the opening <xref:System.Windows.Controls.Grid> element, add the following data templates, which define how to display the expense report data:</span></span>

    [!code-xaml[ExpenseIt#30](~/samples/snippets/csharp/VS_Snippets_Wpf/ExpenseIt/CSharp/ExpenseIt9/ExpenseReportPage.xaml#30)]

4. <span data-ttu-id="8a2c5-317">Remplacez le <xref:System.Windows.Controls.DataGridTextColumn> éléments avec <xref:System.Windows.Controls.DataGridTemplateColumn> sous le <xref:System.Windows.Controls.DataGrid> élément et appliquer les modèles.</span><span class="sxs-lookup"><span data-stu-id="8a2c5-317">Replace the <xref:System.Windows.Controls.DataGridTextColumn> elements with <xref:System.Windows.Controls.DataGridTemplateColumn> under the <xref:System.Windows.Controls.DataGrid> element and apply the templates to them.</span></span>

    [!code-xaml[ExpenseIt#32](~/samples/snippets/csharp/VS_Snippets_Wpf/ExpenseIt/CSharp/ExpenseIt9/ExpenseReportPage.xaml#32)]

5. <span data-ttu-id="8a2c5-318">Générez et exécutez l’application.</span><span class="sxs-lookup"><span data-stu-id="8a2c5-318">Build and run the application.</span></span>

6. <span data-ttu-id="8a2c5-319">Sélectionnez une personne, puis le **vue** bouton.</span><span class="sxs-lookup"><span data-stu-id="8a2c5-319">Select a person and then select the **View** button.</span></span>

<span data-ttu-id="8a2c5-320">L’illustration suivante montre les deux pages de le `ExpenseIt` application avec des contrôles, styles, la disposition, liaison de données et modèles de données appliqués :</span><span class="sxs-lookup"><span data-stu-id="8a2c5-320">The following illustration shows both pages of the `ExpenseIt` application with controls, layout, styles, data binding, and data templates applied:</span></span>

![Captures d’écran d’exemple ExpenseIt](./media/gettingstartedfigure5.png)

> [!NOTE]
> <span data-ttu-id="8a2c5-322">Cet exemple montre une fonctionnalité spécifique de WPF et ne respecte pas toutes les meilleures pratiques pour les éléments tels que la sécurité, la localisation et d’accessibilité.</span><span class="sxs-lookup"><span data-stu-id="8a2c5-322">This sample demonstrates a specific feature of WPF and doesn't follow all best practices for things like security, localization, and accessibility.</span></span> <span data-ttu-id="8a2c5-323">Pour une couverture complète de WPF et les .NET Framework application meilleures pratiques de développement, consultez les rubriques suivantes :</span><span class="sxs-lookup"><span data-stu-id="8a2c5-323">For comprehensive coverage of WPF and the .NET Framework application development best practices, see the following topics:</span></span>
>
> - [<span data-ttu-id="8a2c5-324">Accessibilité</span><span class="sxs-lookup"><span data-stu-id="8a2c5-324">Accessibility</span></span>](../../ui-automation/accessibility-best-practices.md)
>
> - [<span data-ttu-id="8a2c5-325">Sécurité</span><span class="sxs-lookup"><span data-stu-id="8a2c5-325">Security</span></span>](../security-wpf.md)
>
> - [<span data-ttu-id="8a2c5-326">Globalisation et localisation pour WPF</span><span class="sxs-lookup"><span data-stu-id="8a2c5-326">WPF globalization and localization</span></span>](../advanced/wpf-globalization-and-localization-overview.md)
>
> - [<span data-ttu-id="8a2c5-327">Performances WPF</span><span class="sxs-lookup"><span data-stu-id="8a2c5-327">WPF performance</span></span>](../advanced/optimizing-wpf-application-performance.md)

## <a name="next-steps"></a><span data-ttu-id="8a2c5-328">Étapes suivantes</span><span class="sxs-lookup"><span data-stu-id="8a2c5-328">Next steps</span></span>

<span data-ttu-id="8a2c5-329">Dans cette procédure pas à pas, vous avez appris un certain nombre de techniques pour la création d’une interface utilisateur à l’aide de Windows Presentation Foundation (WPF).</span><span class="sxs-lookup"><span data-stu-id="8a2c5-329">In this walkthrough you learned a number of techniques for creating a UI using Windows Presentation Foundation (WPF).</span></span> <span data-ttu-id="8a2c5-330">Vous devez maintenant avoir une compréhension élémentaire des blocs de construction d’une application .NET Framework de liaison de données.</span><span class="sxs-lookup"><span data-stu-id="8a2c5-330">You should now have a basic understanding of the building blocks of a data-bound, .NET Framework application.</span></span> <span data-ttu-id="8a2c5-331">Pour plus d’informations sur les modèles d’architecture et de programmation WPF, consultez les rubriques suivantes :</span><span class="sxs-lookup"><span data-stu-id="8a2c5-331">For more information about the WPF architecture and programming models, see the following topics:</span></span>

- [<span data-ttu-id="8a2c5-332">Architecture de WPF</span><span class="sxs-lookup"><span data-stu-id="8a2c5-332">WPF architecture</span></span>](../advanced/wpf-architecture.md)
- [<span data-ttu-id="8a2c5-333">Vue d’ensemble du langage XAML (WPF)</span><span class="sxs-lookup"><span data-stu-id="8a2c5-333">XAML overview (WPF)</span></span>](../advanced/xaml-overview-wpf.md)
- [<span data-ttu-id="8a2c5-334">Vue d’ensemble des propriétés de dépendance</span><span class="sxs-lookup"><span data-stu-id="8a2c5-334">Dependency properties overview</span></span>](../advanced/dependency-properties-overview.md)
- [<span data-ttu-id="8a2c5-335">Disposition</span><span class="sxs-lookup"><span data-stu-id="8a2c5-335">Layout</span></span>](../advanced/layout.md)

<span data-ttu-id="8a2c5-336">Pour plus d’informations sur la création d’applications, consultez les rubriques suivantes :</span><span class="sxs-lookup"><span data-stu-id="8a2c5-336">For more information about creating applications, see the following topics:</span></span>

- [<span data-ttu-id="8a2c5-337">Développement d’applications</span><span class="sxs-lookup"><span data-stu-id="8a2c5-337">Application development</span></span>](../app-development/index.md)
- [<span data-ttu-id="8a2c5-338">Contrôles</span><span class="sxs-lookup"><span data-stu-id="8a2c5-338">Controls</span></span>](../controls/index.md)
- [<span data-ttu-id="8a2c5-339">Vue d’ensemble de la liaison de données</span><span class="sxs-lookup"><span data-stu-id="8a2c5-339">Data binding overview</span></span>](../data/data-binding-overview.md)
- [<span data-ttu-id="8a2c5-340">Graphiques et multimédia</span><span class="sxs-lookup"><span data-stu-id="8a2c5-340">Graphics and multimedia</span></span>](../graphics-multimedia/index.md)
- [<span data-ttu-id="8a2c5-341">Documents dans WPF</span><span class="sxs-lookup"><span data-stu-id="8a2c5-341">Documents in WPF</span></span>](../advanced/documents-in-wpf.md)

## <a name="see-also"></a><span data-ttu-id="8a2c5-342">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="8a2c5-342">See also</span></span>

- [<span data-ttu-id="8a2c5-343">Vue d’ensemble des panneaux</span><span class="sxs-lookup"><span data-stu-id="8a2c5-343">Panels overview</span></span>](../controls/panels-overview.md)
- [<span data-ttu-id="8a2c5-344">Vue d’ensemble de création de modèles de données</span><span class="sxs-lookup"><span data-stu-id="8a2c5-344">Data templating overview</span></span>](../data/data-templating-overview.md)
- [<span data-ttu-id="8a2c5-345">Créer une application WPF</span><span class="sxs-lookup"><span data-stu-id="8a2c5-345">Build a WPF application</span></span>](../app-development/building-a-wpf-application-wpf.md)
- [<span data-ttu-id="8a2c5-346">Styles et modèles</span><span class="sxs-lookup"><span data-stu-id="8a2c5-346">Styles and templates</span></span>](../controls/styles-and-templates.md)
