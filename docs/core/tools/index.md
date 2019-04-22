---
title: Outils de l’interface de ligne de commande (CLI) de .NET Core
description: Présentation des outils et fonctionnalités de l’interface de ligne de commande (CLI) de .NET Core.
ms.date: 08/14/2017
ms.custom: seodec18
ms.openlocfilehash: e174867ce06e573fc85579183df0196d8276fb37
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "58826312"
---
# <a name="net-core-command-line-interface-cli-tools"></a><span data-ttu-id="73c62-103">Outils de l’interface de ligne de commande (CLI) de .NET Core</span><span class="sxs-lookup"><span data-stu-id="73c62-103">.NET Core command-line interface (CLI) tools</span></span>

<span data-ttu-id="73c62-104">L’interface de ligne de commande (CLI) de .NET Core est une nouvelle chaîne d’outils multiplateforme pour le développement d’applications .NET.</span><span class="sxs-lookup"><span data-stu-id="73c62-104">The .NET Core command-line interface (CLI) is a new cross-platform toolchain for developing .NET applications.</span></span> <span data-ttu-id="73c62-105">CLI est une fondation sur laquelle les autres outils de niveau supérieur, tels que les environnements de développement intégré (IDE), les éditeurs et les orchestrateurs de builds, peuvent se baser.</span><span class="sxs-lookup"><span data-stu-id="73c62-105">The CLI is a foundation upon which higher-level tools, such as Integrated Development Environments (IDEs), editors, and build orchestrators, can rest.</span></span>

## <a name="installation"></a><span data-ttu-id="73c62-106">Installation</span><span class="sxs-lookup"><span data-stu-id="73c62-106">Installation</span></span>

<span data-ttu-id="73c62-107">Utilisez les programmes d’installation natifs ou les scripts shell d’installation :</span><span class="sxs-lookup"><span data-stu-id="73c62-107">Either use the native installers or use the installation shell scripts:</span></span>

* <span data-ttu-id="73c62-108">Les programmes d’installation natifs sont principalement utilisés sur les ordinateurs des développeurs et s’appuient sur le mécanisme d’installation natif de chaque plateforme prise en charge, par exemple des packages DEB sur Ubuntu ou des ensembles MSI sur Windows.</span><span class="sxs-lookup"><span data-stu-id="73c62-108">The native installers are primarily used on developer's machines and use each supported platform's native install mechanism, for instance, DEB packages on Ubuntu or MSI bundles on Windows.</span></span> <span data-ttu-id="73c62-109">Ces programmes d’installation installent et configurent l’environnement pour une utilisation immédiate par le développeur, mais requièrent des privilèges d’administrateur sur l’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="73c62-109">These installers install and configure the environment for immediate use by the developer but require administrative privileges on the machine.</span></span> <span data-ttu-id="73c62-110">Vous pouvez consulter les instructions d’installation dans le [guide d’installation de .NET Core](https://aka.ms/dotnetcoregs).</span><span class="sxs-lookup"><span data-stu-id="73c62-110">You can view the installation instructions in the [.NET Core installation guide](https://aka.ms/dotnetcoregs).</span></span>
* <span data-ttu-id="73c62-111">Les scripts de shell servent principalement à configurer les serveurs de builds et permettent d’installer les outils sans privilèges d’administration.</span><span class="sxs-lookup"><span data-stu-id="73c62-111">Shell scripts are primarily used for setting up build servers or when you wish to install the tools without administrative privileges.</span></span> <span data-ttu-id="73c62-112">Les scripts d’installation n’installent pas les composants requis sur l’ordinateur, qui doivent être installés manuellement.</span><span class="sxs-lookup"><span data-stu-id="73c62-112">Install scripts don't install prerequisites on the machine, which must be installed manually.</span></span> <span data-ttu-id="73c62-113">Pour plus d’informations, consultez la [rubrique de référence sur les scripts d’installation](dotnet-install-script.md).</span><span class="sxs-lookup"><span data-stu-id="73c62-113">For more information, see the [install script reference topic](dotnet-install-script.md).</span></span> <span data-ttu-id="73c62-114">Pour plus d’informations sur la configuration de l’interface CLI sur votre serveur de builds avec intégration continue (CI), consultez [Utilisation du SDK et des outils .NET Core avec l’intégration continue](using-ci-with-cli.md).</span><span class="sxs-lookup"><span data-stu-id="73c62-114">For information on how to set up CLI on your continuous integration (CI) build server, see [Using .NET Core SDK and tools in Continuous Integration (CI)](using-ci-with-cli.md).</span></span>

<span data-ttu-id="73c62-115">Par défaut, l’interface CLI s’installe en parallèle (SxS) et plusieurs versions des outils CLI peuvent donc coexister sur un même ordinateur.</span><span class="sxs-lookup"><span data-stu-id="73c62-115">By default, the CLI installs in a side-by-side (SxS) manner, so multiple versions of the CLI tools can coexist on a single machine.</span></span> <span data-ttu-id="73c62-116">La méthode permettant d’identifier la version utilisée sur un ordinateur sur lequel plusieurs versions sont installées est expliquée plus en détail dans la section [Pilote](#driver).</span><span class="sxs-lookup"><span data-stu-id="73c62-116">Determining which version is used on a machine where multiple versions are installed is explained in more detail in the [Driver](#driver) section.</span></span>

## <a name="cli-commands"></a><span data-ttu-id="73c62-117">Commandes CLI</span><span class="sxs-lookup"><span data-stu-id="73c62-117">CLI commands</span></span>

<span data-ttu-id="73c62-118">Les commandes suivantes sont installées par défaut :</span><span class="sxs-lookup"><span data-stu-id="73c62-118">The following commands are installed by default:</span></span>

# <a name="net-core-2xtabnetcore2x"></a>[<span data-ttu-id="73c62-119">.NET Core 2.x</span><span class="sxs-lookup"><span data-stu-id="73c62-119">.NET Core 2.x</span></span>](#tab/netcore2x)

<span data-ttu-id="73c62-120">**Commandes de base**</span><span class="sxs-lookup"><span data-stu-id="73c62-120">**Basic commands**</span></span>

* [<span data-ttu-id="73c62-121">new</span><span class="sxs-lookup"><span data-stu-id="73c62-121">new</span></span>](dotnet-new.md)
* [<span data-ttu-id="73c62-122">restore</span><span class="sxs-lookup"><span data-stu-id="73c62-122">restore</span></span>](dotnet-restore.md)
* [<span data-ttu-id="73c62-123">build</span><span class="sxs-lookup"><span data-stu-id="73c62-123">build</span></span>](dotnet-build.md)
* [<span data-ttu-id="73c62-124">publish</span><span class="sxs-lookup"><span data-stu-id="73c62-124">publish</span></span>](dotnet-publish.md)
* [<span data-ttu-id="73c62-125">run</span><span class="sxs-lookup"><span data-stu-id="73c62-125">run</span></span>](dotnet-run.md)
* [<span data-ttu-id="73c62-126">test</span><span class="sxs-lookup"><span data-stu-id="73c62-126">test</span></span>](dotnet-test.md)
* [<span data-ttu-id="73c62-127">vstest</span><span class="sxs-lookup"><span data-stu-id="73c62-127">vstest</span></span>](dotnet-vstest.md)
* [<span data-ttu-id="73c62-128">pack</span><span class="sxs-lookup"><span data-stu-id="73c62-128">pack</span></span>](dotnet-pack.md)
* [<span data-ttu-id="73c62-129">migrate</span><span class="sxs-lookup"><span data-stu-id="73c62-129">migrate</span></span>](dotnet-migrate.md)
* [<span data-ttu-id="73c62-130">clean</span><span class="sxs-lookup"><span data-stu-id="73c62-130">clean</span></span>](dotnet-clean.md)
* [<span data-ttu-id="73c62-131">sln</span><span class="sxs-lookup"><span data-stu-id="73c62-131">sln</span></span>](dotnet-sln.md)
* [<span data-ttu-id="73c62-132">help</span><span class="sxs-lookup"><span data-stu-id="73c62-132">help</span></span>](dotnet-help.md)
* [<span data-ttu-id="73c62-133">store</span><span class="sxs-lookup"><span data-stu-id="73c62-133">store</span></span>](dotnet-store.md)

<span data-ttu-id="73c62-134">**Commandes de modification de projets**</span><span class="sxs-lookup"><span data-stu-id="73c62-134">**Project modification commands**</span></span>

* [<span data-ttu-id="73c62-135">add package</span><span class="sxs-lookup"><span data-stu-id="73c62-135">add package</span></span>](dotnet-add-package.md)
* [<span data-ttu-id="73c62-136">add reference</span><span class="sxs-lookup"><span data-stu-id="73c62-136">add reference</span></span>](dotnet-add-reference.md)
* [<span data-ttu-id="73c62-137">remove package</span><span class="sxs-lookup"><span data-stu-id="73c62-137">remove package</span></span>](dotnet-remove-package.md)
* [<span data-ttu-id="73c62-138">remove reference</span><span class="sxs-lookup"><span data-stu-id="73c62-138">remove reference</span></span>](dotnet-remove-reference.md)
* [<span data-ttu-id="73c62-139">list reference</span><span class="sxs-lookup"><span data-stu-id="73c62-139">list reference</span></span>](dotnet-list-reference.md)

<span data-ttu-id="73c62-140">**Commandes avancées**</span><span class="sxs-lookup"><span data-stu-id="73c62-140">**Advanced commands**</span></span>

* [<span data-ttu-id="73c62-141">nuget delete</span><span class="sxs-lookup"><span data-stu-id="73c62-141">nuget delete</span></span>](dotnet-nuget-delete.md)
* [<span data-ttu-id="73c62-142">nuget locals</span><span class="sxs-lookup"><span data-stu-id="73c62-142">nuget locals</span></span>](dotnet-nuget-locals.md)
* [<span data-ttu-id="73c62-143">nuget push</span><span class="sxs-lookup"><span data-stu-id="73c62-143">nuget push</span></span>](dotnet-nuget-push.md)
* [<span data-ttu-id="73c62-144">msbuild</span><span class="sxs-lookup"><span data-stu-id="73c62-144">msbuild</span></span>](dotnet-msbuild.md)
* [<span data-ttu-id="73c62-145">dotnet install script</span><span class="sxs-lookup"><span data-stu-id="73c62-145">dotnet install script</span></span>](dotnet-install-script.md)

# <a name="net-core-1xtabnetcore1x"></a>[<span data-ttu-id="73c62-146">.NET Core 1.x</span><span class="sxs-lookup"><span data-stu-id="73c62-146">.NET Core 1.x</span></span>](#tab/netcore1x)

<span data-ttu-id="73c62-147">**Commandes de base**</span><span class="sxs-lookup"><span data-stu-id="73c62-147">**Basic commands**</span></span>

* [<span data-ttu-id="73c62-148">new</span><span class="sxs-lookup"><span data-stu-id="73c62-148">new</span></span>](dotnet-new.md)
* [<span data-ttu-id="73c62-149">restore</span><span class="sxs-lookup"><span data-stu-id="73c62-149">restore</span></span>](dotnet-restore.md)
* [<span data-ttu-id="73c62-150">build</span><span class="sxs-lookup"><span data-stu-id="73c62-150">build</span></span>](dotnet-build.md)
* [<span data-ttu-id="73c62-151">publish</span><span class="sxs-lookup"><span data-stu-id="73c62-151">publish</span></span>](dotnet-publish.md)
* [<span data-ttu-id="73c62-152">run</span><span class="sxs-lookup"><span data-stu-id="73c62-152">run</span></span>](dotnet-run.md)
* [<span data-ttu-id="73c62-153">test</span><span class="sxs-lookup"><span data-stu-id="73c62-153">test</span></span>](dotnet-test.md)
* [<span data-ttu-id="73c62-154">vstest</span><span class="sxs-lookup"><span data-stu-id="73c62-154">vstest</span></span>](dotnet-vstest.md)
* [<span data-ttu-id="73c62-155">pack</span><span class="sxs-lookup"><span data-stu-id="73c62-155">pack</span></span>](dotnet-pack.md)
* [<span data-ttu-id="73c62-156">migrate</span><span class="sxs-lookup"><span data-stu-id="73c62-156">migrate</span></span>](dotnet-migrate.md)
* [<span data-ttu-id="73c62-157">clean</span><span class="sxs-lookup"><span data-stu-id="73c62-157">clean</span></span>](dotnet-clean.md)
* [<span data-ttu-id="73c62-158">sln</span><span class="sxs-lookup"><span data-stu-id="73c62-158">sln</span></span>](dotnet-sln.md)

<span data-ttu-id="73c62-159">**Commandes de modification de projets**</span><span class="sxs-lookup"><span data-stu-id="73c62-159">**Project modification commands**</span></span>

* [<span data-ttu-id="73c62-160">add package</span><span class="sxs-lookup"><span data-stu-id="73c62-160">add package</span></span>](dotnet-add-package.md)
* [<span data-ttu-id="73c62-161">add reference</span><span class="sxs-lookup"><span data-stu-id="73c62-161">add reference</span></span>](dotnet-add-reference.md)
* [<span data-ttu-id="73c62-162">remove package</span><span class="sxs-lookup"><span data-stu-id="73c62-162">remove package</span></span>](dotnet-remove-package.md)
* [<span data-ttu-id="73c62-163">remove reference</span><span class="sxs-lookup"><span data-stu-id="73c62-163">remove reference</span></span>](dotnet-remove-reference.md)
* [<span data-ttu-id="73c62-164">list reference</span><span class="sxs-lookup"><span data-stu-id="73c62-164">list reference</span></span>](dotnet-list-reference.md)

<span data-ttu-id="73c62-165">**Commandes avancées**</span><span class="sxs-lookup"><span data-stu-id="73c62-165">**Advanced commands**</span></span>

* [<span data-ttu-id="73c62-166">nuget delete</span><span class="sxs-lookup"><span data-stu-id="73c62-166">nuget delete</span></span>](dotnet-nuget-delete.md)
* [<span data-ttu-id="73c62-167">nuget locals</span><span class="sxs-lookup"><span data-stu-id="73c62-167">nuget locals</span></span>](dotnet-nuget-locals.md)
* [<span data-ttu-id="73c62-168">nuget push</span><span class="sxs-lookup"><span data-stu-id="73c62-168">nuget push</span></span>](dotnet-nuget-push.md)
* [<span data-ttu-id="73c62-169">msbuild</span><span class="sxs-lookup"><span data-stu-id="73c62-169">msbuild</span></span>](dotnet-msbuild.md)
* [<span data-ttu-id="73c62-170">dotnet install script</span><span class="sxs-lookup"><span data-stu-id="73c62-170">dotnet install script</span></span>](dotnet-install-script.md)

---

<span data-ttu-id="73c62-171">L’interface CLI adopte un modèle d’extensibilité qui vous permet de spécifier des outils supplémentaires pour vos projets.</span><span class="sxs-lookup"><span data-stu-id="73c62-171">The CLI adopts an extensibility model that allows you to specify additional tools for your projects.</span></span> <span data-ttu-id="73c62-172">Pour plus d’informations, consultez la rubrique [Modèle d’extensibilité des outils CLI .NET Core](extensibility.md).</span><span class="sxs-lookup"><span data-stu-id="73c62-172">For more information, see the [.NET Core CLI extensibility model](extensibility.md) topic.</span></span>

## <a name="command-structure"></a><span data-ttu-id="73c62-173">Structure de commande</span><span class="sxs-lookup"><span data-stu-id="73c62-173">Command structure</span></span>

<span data-ttu-id="73c62-174">La structure de commande CLI se compose du [pilote (« dotnet »)](#driver), de [la commande (« verbe ») ](#command-verb) et éventuellement des [arguments](#arguments) et [options](#options) de la commande.</span><span class="sxs-lookup"><span data-stu-id="73c62-174">CLI command structure consists of [the driver ("dotnet")](#driver), [the command (or "verb")](#command-verb), and possibly command [arguments](#arguments) and [options](#options).</span></span> <span data-ttu-id="73c62-175">Ce modèle apparaît dans la plupart des opérations de l’interface CLI, notamment la création d’une application console et son exécution à partir de la ligne de commande, comme le montrent les commandes suivantes, exécutées à partir d’un répertoire nommé *my_app* :</span><span class="sxs-lookup"><span data-stu-id="73c62-175">You see this pattern in most CLI operations, such as creating a new console app and running it from the command line as the following commands show when executed from a directory named *my_app*:</span></span>

# <a name="net-core-2xtabnetcore2x"></a>[<span data-ttu-id="73c62-176">.NET Core 2.x</span><span class="sxs-lookup"><span data-stu-id="73c62-176">.NET Core 2.x</span></span>](#tab/netcore2x)

```console
dotnet new console
dotnet build --output /build_output
dotnet /build_output/my_app.dll
```

# <a name="net-core-1xtabnetcore1x"></a>[<span data-ttu-id="73c62-177">.NET Core 1.x</span><span class="sxs-lookup"><span data-stu-id="73c62-177">.NET Core 1.x</span></span>](#tab/netcore1x)

```console
dotnet new console
dotnet restore
dotnet build --output /build_output
dotnet /build_output/my_app.dll
```

---

### <a name="driver"></a><span data-ttu-id="73c62-178">Pilote</span><span class="sxs-lookup"><span data-stu-id="73c62-178">Driver</span></span>

<span data-ttu-id="73c62-179">Le pilote s’intitule [dotnet](dotnet.md) et gère deux tâches : l’exécution d’une [application dépendant du framework](../deploying/index.md) ou l’exécution d’une commande.</span><span class="sxs-lookup"><span data-stu-id="73c62-179">The driver is named [dotnet](dotnet.md) and has two responsibilities, either running a [framework-dependent app](../deploying/index.md) or executing a command.</span></span> 

<span data-ttu-id="73c62-180">Pour exécuter une application dépendant du framework, spécifiez l’application après le pilote, par exemple `dotnet /path/to/my_app.dll`.</span><span class="sxs-lookup"><span data-stu-id="73c62-180">To run a framework-dependent app, specify the app after the driver, for example, `dotnet /path/to/my_app.dll`.</span></span> <span data-ttu-id="73c62-181">Lors de l’exécution de la commande à partir du dossier où se trouve la DLL de l’application, vous devez simplement exécuter `dotnet my_app.dll`.</span><span class="sxs-lookup"><span data-stu-id="73c62-181">When executing the command from the folder where the app's DLL resides, simply execute `dotnet my_app.dll`.</span></span> <span data-ttu-id="73c62-182">Si vous souhaitez utiliser une version spécifique de .NET Core Runtime, choisissez l’option `--fx-version <VERSION>` (voir la référence [dotnet command](dotnet.md)).</span><span class="sxs-lookup"><span data-stu-id="73c62-182">If you want to use a specific version of the .NET Core Runtime, use the `--fx-version <VERSION>` option (see the [dotnet command](dotnet.md) reference).</span></span>

<span data-ttu-id="73c62-183">Lorsque vous fournissez une commande au pilote, `dotnet.exe` démarre le processus d’exécution de la commande CLI.</span><span class="sxs-lookup"><span data-stu-id="73c62-183">When you supply a command to the driver, `dotnet.exe` starts the CLI command execution process.</span></span> <span data-ttu-id="73c62-184">Par exemple :</span><span class="sxs-lookup"><span data-stu-id="73c62-184">For example:</span></span>

```bash
> dotnet build
```

<span data-ttu-id="73c62-185">D’abord, le pilote détermine la version du kit SDK à utiliser.</span><span class="sxs-lookup"><span data-stu-id="73c62-185">First, the driver determines the version of the SDK to use.</span></span> <span data-ttu-id="73c62-186">S’il n’existe pas de ['global.json'](global-json.md), la dernière version du SDK disponible est utilisée.</span><span class="sxs-lookup"><span data-stu-id="73c62-186">If there is no ['global.json'](global-json.md), the latest version of the SDK available is used.</span></span> <span data-ttu-id="73c62-187">Il s’agit peut-être d’une préversion ou d’une version stable, selon la plus récente qui se trouve sur l’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="73c62-187">This might be either a preview or stable version, depending on what is latest on the machine.</span></span>  <span data-ttu-id="73c62-188">Une fois que la version du SDK est déterminée, elle exécute la commande.</span><span class="sxs-lookup"><span data-stu-id="73c62-188">Once the SDK version is determined, it executes the command.</span></span>

### <a name="command-verb"></a><span data-ttu-id="73c62-189">Commande (« verbe »)</span><span class="sxs-lookup"><span data-stu-id="73c62-189">Command ("verb")</span></span>

<span data-ttu-id="73c62-190">La commande (ou « verbe ») est une commande qui exécute une action.</span><span class="sxs-lookup"><span data-stu-id="73c62-190">The command (or "verb") is simply a command that performs an action.</span></span> <span data-ttu-id="73c62-191">Par exemple, `dotnet build` génère votre code.</span><span class="sxs-lookup"><span data-stu-id="73c62-191">For example, `dotnet build` builds your code.</span></span> <span data-ttu-id="73c62-192">`dotnet publish` publie le code.</span><span class="sxs-lookup"><span data-stu-id="73c62-192">`dotnet publish` publishes your code.</span></span> <span data-ttu-id="73c62-193">Les commandes sont implémentées comme une application console à l’aide d’une convention `dotnet {verb}`.</span><span class="sxs-lookup"><span data-stu-id="73c62-193">The commands are implemented as a console application using a `dotnet {verb}` convention.</span></span>

### <a name="arguments"></a><span data-ttu-id="73c62-194">Arguments</span><span class="sxs-lookup"><span data-stu-id="73c62-194">Arguments</span></span>

<span data-ttu-id="73c62-195">Les arguments que vous passez sur la ligne de commande sont les arguments de la commande appelée.</span><span class="sxs-lookup"><span data-stu-id="73c62-195">The arguments you pass on the command line are the arguments to the command invoked.</span></span> <span data-ttu-id="73c62-196">Par exemple, lorsque vous exécutez `dotnet publish my_app.csproj`, l’argument `my_app.csproj` indique le projet à publier et est transmis à la commande `publish`.</span><span class="sxs-lookup"><span data-stu-id="73c62-196">For example when you execute `dotnet publish my_app.csproj`, the `my_app.csproj` argument indicates the project to publish and is passed to the `publish` command.</span></span>

### <a name="options"></a><span data-ttu-id="73c62-197">Options</span><span class="sxs-lookup"><span data-stu-id="73c62-197">Options</span></span>

<span data-ttu-id="73c62-198">Les options que vous passez sur la ligne de commande sont les options de la commande appelée.</span><span class="sxs-lookup"><span data-stu-id="73c62-198">The options you pass on the command line are the options to the command invoked.</span></span> <span data-ttu-id="73c62-199">Par exemple, lorsque vous exécutez `dotnet publish --output /build_output`, l’option `--output` et sa valeur sont passés à la commande `publish`.</span><span class="sxs-lookup"><span data-stu-id="73c62-199">For example when you execute `dotnet publish --output /build_output`, the `--output` option and its value are passed to the `publish` command.</span></span>

## <a name="migration-from-projectjson"></a><span data-ttu-id="73c62-200">Migration à partir de project.json</span><span class="sxs-lookup"><span data-stu-id="73c62-200">Migration from project.json</span></span>

<span data-ttu-id="73c62-201">Si vous avez utilisé les outils Preview 2 pour produire des projets *project.json*, consultez la rubrique [dotnet migrate](dotnet-migrate.md) pour plus d’informations sur la migration de votre projet vers MSBuild/*.csproj*.</span><span class="sxs-lookup"><span data-stu-id="73c62-201">If you used Preview 2 tooling to produce *project.json*-based projects, consult the [dotnet migrate](dotnet-migrate.md) topic for information on migrating your project to MSBuild/*.csproj* for use with release tooling.</span></span> <span data-ttu-id="73c62-202">Pour les projets .NET Core créés avant la version des outils de Preview 2, mettez à jour manuellement le projet en suivant les instructions dans [Migration de DNX vers l’interface CLI .NET Core (project.json)](../migration/from-dnx.md), puis utilisez `dotnet migrate` ou mettez directement à niveau vos projets.</span><span class="sxs-lookup"><span data-stu-id="73c62-202">For .NET Core projects created prior to the release of Preview 2 tooling, either manually update the project following the guidance in [Migrating from DNX to .NET Core CLI (project.json)](../migration/from-dnx.md) and then use `dotnet migrate` or directly upgrade your projects.</span></span>

## <a name="see-also"></a><span data-ttu-id="73c62-203">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="73c62-203">See also</span></span>

- [<span data-ttu-id="73c62-204">Référentiel GitHub dotnet/CLI</span><span class="sxs-lookup"><span data-stu-id="73c62-204">dotnet/CLI GitHub Repository</span></span>](https://github.com/dotnet/cli/)
- [<span data-ttu-id="73c62-205">Guide d’installation de .NET Core</span><span class="sxs-lookup"><span data-stu-id="73c62-205">.NET Core installation guide</span></span>](https://aka.ms/dotnetcoregs)
