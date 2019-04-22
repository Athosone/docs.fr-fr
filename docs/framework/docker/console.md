---
title: Exécution d’applications console dans Docker
description: Découvrez comment prendre une application console .NET Framework existante et l’exécuter dans un conteneur Docker Windows.
author: spboyer
ms.date: 09/28/2016
ms.assetid: 85cca1d5-c9a4-4eb2-93e6-4f878de07fd7
ms.openlocfilehash: da3c814e2ae3ae646072deaf7aa932272160ce49
ms.sourcegitcommit: 438919211260bb415fc8f96ca3eabc33cf2d681d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/16/2019
ms.locfileid: "59611495"
---
# <a name="running-console-applications-in-windows-containers"></a><span data-ttu-id="08234-103">Exécution d’applications console dans des conteneurs Windows</span><span class="sxs-lookup"><span data-stu-id="08234-103">Running console applications in Windows containers</span></span>

<span data-ttu-id="08234-104">Les applications console sont utilisées à de nombreuses fins, allant de la simple interrogation d’un état à l’exécution de longues tâches de traitement d’images de document.</span><span class="sxs-lookup"><span data-stu-id="08234-104">Console applications are used for many purposes; from simple querying of a status to long running document image processing tasks.</span></span> <span data-ttu-id="08234-105">Dans tous les cas, vous pouvez démarrer et faire évoluer ces applications dans les limites des acquisitions matérielles, des temps de démarrage et de l’exécution de plusieurs instances.</span><span class="sxs-lookup"><span data-stu-id="08234-105">In any case, the ability to start up and scale these applications are met with limitations of hardware acquisitions, startup times or running multiple instances.</span></span>

<span data-ttu-id="08234-106">En déplaçant vos applications console pour utiliser des conteneurs Windows Server et Docker, vous pouvez les démarrer à partir d’un état propre, leur permettant d’effectuer l’opération, puis de s’arrêter proprement.</span><span class="sxs-lookup"><span data-stu-id="08234-106">Moving your console applications to use Docker and Windows Server containers allows for starting these applications from a clean state, enabling them to perform the operation and then shutdown cleanly.</span></span> <span data-ttu-id="08234-107">Cette rubrique décrit les étapes nécessaires pour déplacer une application console vers un conteneur Windows et la démarrer à l’aide d’un script PowerShell.</span><span class="sxs-lookup"><span data-stu-id="08234-107">This topic will show the steps needed to move a console application to a Windows based container and start it using a PowerShell script.</span></span>

<span data-ttu-id="08234-108">L’exemple d’application console est un exemple simple qui prend un argument, en l’occurrence une question, et retourne une réponse aléatoire.</span><span class="sxs-lookup"><span data-stu-id="08234-108">The sample console application is a simple example which takes an argument, a question in this case, and returns a random answer.</span></span> <span data-ttu-id="08234-109">Cette opération pourrait traiter les taxes d’un client à partir de son `customer_id` ou créer une miniature pour un argument `image_url`.</span><span class="sxs-lookup"><span data-stu-id="08234-109">This could take a `customer_id` and process their taxes, or create a thumbnail for an `image_url` argument.</span></span>

<span data-ttu-id="08234-110">`Environment.MachineName` a été ajouté à la réponse pour afficher la différence entre l’exécution de l’application localement et son exécution dans un conteneur Windows.</span><span class="sxs-lookup"><span data-stu-id="08234-110">In addition to the answer, the `Environment.MachineName` has been added to the response to show the difference between running the application locally and in a Windows container.</span></span> <span data-ttu-id="08234-111">Selon que vous exécutez l’application localement ou dans un conteneur Windows, c’est le nom de votre ordinateur local ou l’ID de session du conteneur qui est retourné.</span><span class="sxs-lookup"><span data-stu-id="08234-111">When running the application locally, your local machine name should be returned and when running in a Windows Container; the container session id is returned.</span></span>

<span data-ttu-id="08234-112">[L’exemple terminé](https://github.com/dotnet/samples/tree/master/framework/docker/ConsoleRandomAnswerGenerator) est disponible dans le dépôt dotnet/samples sur GitHub.</span><span class="sxs-lookup"><span data-stu-id="08234-112">The [complete example](https://github.com/dotnet/samples/tree/master/framework/docker/ConsoleRandomAnswerGenerator) is available in the dotnet/samples repository on GitHub.</span></span> <span data-ttu-id="08234-113">Pour obtenir des instructions de téléchargement, consultez [Exemples et didacticiels](../../samples-and-tutorials/index.md#viewing-and-downloading-samples).</span><span class="sxs-lookup"><span data-stu-id="08234-113">For download instructions, see [Samples and Tutorials](../../samples-and-tutorials/index.md#viewing-and-downloading-samples).</span></span>

<span data-ttu-id="08234-114">Vous devez être familiarisé avec certains termes Docker avant de procéder au déplacement de votre application vers un conteneur.</span><span class="sxs-lookup"><span data-stu-id="08234-114">You need to be familiar with some Docker terms before you begin working on moving your application to a container.</span></span>

> [!NOTE]
> <span data-ttu-id="08234-115">Une *image Docker* est un modèle en lecture seule qui définit l’environnement pour un conteneur en cours d’exécution, notamment le système d’exploitation (SE), les composants système et l’application (ou les applications).</span><span class="sxs-lookup"><span data-stu-id="08234-115">A *Docker image* is a read-only template that defines the environment for a running container, including the operating system (OS), system components, and application(s).</span></span>

<span data-ttu-id="08234-116">Une fonctionnalité importante des images Docker est qu’elles sont composées à partir d’une image de base.</span><span class="sxs-lookup"><span data-stu-id="08234-116">One important feature of Docker images is that images are composed from a base image.</span></span> <span data-ttu-id="08234-117">Chaque nouvelle image ajoute un petit ensemble de fonctionnalités à une image existante.</span><span class="sxs-lookup"><span data-stu-id="08234-117">Each new image adds a small set of features to an existing image.</span></span>

> [!NOTE]
> <span data-ttu-id="08234-118">Un *conteneur Docker* est une instance en cours d’exécution d’une image.</span><span class="sxs-lookup"><span data-stu-id="08234-118">A *Docker container* is a running instance of an image.</span></span>

<span data-ttu-id="08234-119">Vous faites évoluer une application en exécutant la même image dans plusieurs conteneurs.</span><span class="sxs-lookup"><span data-stu-id="08234-119">You scale an application by running the same image in many containers.</span></span>
<span data-ttu-id="08234-120">Conceptuellement, cette opération est similaire à l’exécution de la même application dans plusieurs hôtes.</span><span class="sxs-lookup"><span data-stu-id="08234-120">Conceptually, this is similar to running the same application in multiple hosts.</span></span>

<span data-ttu-id="08234-121">Vous pouvez en savoir plus sur l’architecture de Docker en consultant [Docker Overview](https://docs.docker.com/engine/understanding-docker/) (Vue d’ensemble de Docker) sur le site Docker.</span><span class="sxs-lookup"><span data-stu-id="08234-121">You can learn more about the Docker architecture by reading the [Docker Overview](https://docs.docker.com/engine/understanding-docker/) on the Docker site.</span></span>

<span data-ttu-id="08234-122">Le déplacement de votre application console se fait en quelques étapes.</span><span class="sxs-lookup"><span data-stu-id="08234-122">Moving your console application is a matter of a few steps.</span></span>

1. [<span data-ttu-id="08234-123">Générer l’application</span><span class="sxs-lookup"><span data-stu-id="08234-123">Build the application</span></span>](#building-the-application)
1. [<span data-ttu-id="08234-124">Création d’un fichier Dockerfile pour l’image</span><span class="sxs-lookup"><span data-stu-id="08234-124">Creating a Dockerfile for the image</span></span>](#creating-the-dockerfile)
1. [<span data-ttu-id="08234-125">Processus pour générer et exécuter le conteneur Docker</span><span class="sxs-lookup"><span data-stu-id="08234-125">Process to build and run the Docker container</span></span>](#creating-the-image)

## <a name="prerequisites"></a><span data-ttu-id="08234-126">Prérequis</span><span class="sxs-lookup"><span data-stu-id="08234-126">Prerequisites</span></span>

<span data-ttu-id="08234-127">Les conteneurs Windows sont pris en charge sur [Mise à jour anniversaire Windows 10](https://www.microsoft.com/en-us/software-download/windows10/) ou [Windows Server 2016](https://www.microsoft.com/en-us/cloud-platform/windows-server).</span><span class="sxs-lookup"><span data-stu-id="08234-127">Windows containers are supported on [Windows 10 Anniversary Update](https://www.microsoft.com/en-us/software-download/windows10/) or [Windows Server 2016](https://www.microsoft.com/en-us/cloud-platform/windows-server).</span></span>

> [!NOTE]
><span data-ttu-id="08234-128">Si vous utilisez Windows Server 2016, vous devez activer manuellement les conteneurs dans la mesure où le programme d’installation de Docker pour Windows n’active pas cette fonctionnalité.</span><span class="sxs-lookup"><span data-stu-id="08234-128">If you are using Windows Server 2016, you must enable containers manually since the Docker for Windows installer will not enable the feature.</span></span> <span data-ttu-id="08234-129">Vérifiez que toutes les mises à jour ont été exécutées pour le système d’exploitation, puis suivez les instructions indiquées dans l’article [Déploiement d’un hôte de conteneurs](/virtualization/windowscontainers/deploy-containers/deploy-containers-on-server) pour installer les fonctionnalités Docker et les conteneurs.</span><span class="sxs-lookup"><span data-stu-id="08234-129">Make sure all updates have run for the OS and then follow the instructions from the [Container Host Deployment](/virtualization/windowscontainers/deploy-containers/deploy-containers-on-server) article to install the containers and Docker features.</span></span>

<span data-ttu-id="08234-130">Vous devez disposer de Docker pour Windows, version 1.12 bêta 26 ou ultérieure, pour prendre en charge les conteneurs Windows.</span><span class="sxs-lookup"><span data-stu-id="08234-130">You need to have Docker for Windows, version 1.12 Beta 26 or higher to support Windows containers.</span></span> <span data-ttu-id="08234-131">Par défaut, Docker autorise les conteneurs Linux ; basculez vers les conteneurs Windows en cliquant avec le bouton droit sur l’icône Docker dans la barre d’état système et en sélectionnant **Switch to Windows containers** (Basculer vers les conteneurs Windows).</span><span class="sxs-lookup"><span data-stu-id="08234-131">By default, Docker enables Linux based containers; switch to Windows containers by right clicking the Docker icon in the system tray and select **Switch to Windows containers**.</span></span> <span data-ttu-id="08234-132">Docker exécute le processus de modification et un redémarrage peut être nécessaire.</span><span class="sxs-lookup"><span data-stu-id="08234-132">Docker will run the process to change and a restart may be required.</span></span>

![Capture d’écran de l’option de menu du conteneur Windows.](./media/console/windows-container-option.png)

## <a name="building-the-application"></a><span data-ttu-id="08234-134">Génération de l’application</span><span class="sxs-lookup"><span data-stu-id="08234-134">Building the application</span></span>

<span data-ttu-id="08234-135">En général, les applications console sont distribuées par le biais d’un programme d’installation, de FTP ou d’un déploiement avec partage de fichiers.</span><span class="sxs-lookup"><span data-stu-id="08234-135">Typically console applications are distributed through an installer, FTP, or File Share deployment.</span></span> <span data-ttu-id="08234-136">Pendant le déploiement sur un conteneur, les ressources doivent être compilées et transférées vers un emplacement qui peut être utilisé au moment de la création de l’image Docker.</span><span class="sxs-lookup"><span data-stu-id="08234-136">When deploying to a container, the assets need to be compiled and staged to a location that can be used when the Docker image is created.</span></span>

<span data-ttu-id="08234-137">Voici l’exemple d’application : [ConsoleRandomAnswerGenerator](https://github.com/dotnet/samples/tree/master/framework/docker/ConsoleRandomAnswerGenerator)</span><span class="sxs-lookup"><span data-stu-id="08234-137">Here is the sample application: [ConsoleRandomAnswerGenerator](https://github.com/dotnet/samples/tree/master/framework/docker/ConsoleRandomAnswerGenerator)</span></span>

<span data-ttu-id="08234-138">Dans *build.ps1*<sup>[[source]](https://github.com/dotnet/samples/blob/master/framework/docker/ConsoleRandomAnswerGenerator/ConsoleRandomAnswerGenerator/build.ps1)</sup>, le script utilise [MSBuild](/visualstudio/msbuild/msbuild) pour compiler l’application afin de terminer la tâche de création des ressources.</span><span class="sxs-lookup"><span data-stu-id="08234-138">In *build.ps1*<sup>[[source]](https://github.com/dotnet/samples/blob/master/framework/docker/ConsoleRandomAnswerGenerator/ConsoleRandomAnswerGenerator/build.ps1)</sup>, the script uses [MSBuild](/visualstudio/msbuild/msbuild) to compile the application to complete the task of building the assets.</span></span> <span data-ttu-id="08234-139">Quelques paramètres sont passés à MSBuild pour finaliser les ressources nécessaires :</span><span class="sxs-lookup"><span data-stu-id="08234-139">There are a few parameters passed to MSBuild to finalize the needed assets.</span></span> <span data-ttu-id="08234-140">le nom de la solution ou du fichier de projet à compiler, l’emplacement de la sortie et enfin la configuration (débogage ou release).</span><span class="sxs-lookup"><span data-stu-id="08234-140">The name of the project file or solution to be compiled, the location for the output and finally the configuration (Release or Debug).</span></span>

<span data-ttu-id="08234-141">Dans l’appel à `Invoke-MSBuild`, `OutputPath` est défini sur **publish** et `Configuration` sur **Release**.</span><span class="sxs-lookup"><span data-stu-id="08234-141">In the call to `Invoke-MSBuild` the `OutputPath` is set to **publish** and  `Configuration` set to **Release**.</span></span>

```powershell
function Invoke-MSBuild ([string]$MSBuildPath, [string]$MSBuildParameters) {
    Invoke-Expression "$MSBuildPath $MSBuildParameters"
}

Invoke-MSBuild -MSBuildPath "MSBuild.exe" -MSBuildParameters ".\ConsoleRandomAnswerGenerator.csproj -p:OutputPath=.\publish -p:Configuration=Release"
```

## <a name="creating-the-dockerfile"></a><span data-ttu-id="08234-142">Création du fichier Dockerfile</span><span class="sxs-lookup"><span data-stu-id="08234-142">Creating the Dockerfile</span></span>
<span data-ttu-id="08234-143">L’image de base utilisée pour une application console .NET Framework est `microsoft/windowsservercore`, disponible publiquement sur le [Hub Docker](https://hub.docker.com/r/microsoft/windowsservercore/).</span><span class="sxs-lookup"><span data-stu-id="08234-143">The base image used for a console .NET Framework application is `microsoft/windowsservercore`, publicly available on [Docker Hub](https://hub.docker.com/r/microsoft/windowsservercore/).</span></span> <span data-ttu-id="08234-144">L’image de base contient une installation minimale de Windows Server 2016, .NET Framework 4.6.2, et sert d’image de système d’exploitation de base pour les conteneurs Windows.</span><span class="sxs-lookup"><span data-stu-id="08234-144">The base image contains a minimal installation of Windows Server 2016, .NET Framework 4.6.2 and serves as the base OS image for Windows Containers.</span></span>

```Dockerfile
FROM microsoft/windowsservercore
ADD publish/ /
ENTRYPOINT ConsoleRandomAnswerGenerator.exe
```

<span data-ttu-id="08234-145">La première ligne du fichier Dockerfile désigne l’image de base à l’aide de l’instruction [`FROM`](https://docs.docker.com/engine/reference/builder/#/from).</span><span class="sxs-lookup"><span data-stu-id="08234-145">The first line in the Dockerfile designates the base image using the [`FROM`](https://docs.docker.com/engine/reference/builder/#/from) instruction.</span></span> <span data-ttu-id="08234-146">Ensuite, l’instruction [`ADD`](https://docs.docker.com/engine/reference/builder/#/add) dans le fichier copie les ressources de l’application à partir du dossier **publish** vers le dossier racine du conteneur. Enfin, le paramètre [`ENTRYPOINT`](https://docs.docker.com/engine/reference/builder/#/entrypoint) de l’image indique qu’il s’agit de la commande ou de l’application qui s’exécute au démarrage du conteneur.</span><span class="sxs-lookup"><span data-stu-id="08234-146">Next, [`ADD`](https://docs.docker.com/engine/reference/builder/#/add) in the file copies the application assets from the **publish** folder to root folder of the container and last; setting the [`ENTRYPOINT`](https://docs.docker.com/engine/reference/builder/#/entrypoint) of the image states that this is the command or application that will run when the container starts.</span></span>

## <a name="creating-the-image"></a><span data-ttu-id="08234-147">Création de l’image</span><span class="sxs-lookup"><span data-stu-id="08234-147">Creating the image</span></span>

<span data-ttu-id="08234-148">Pour créer l’image Docker, le code suivant est ajouté au script *build.ps1*.</span><span class="sxs-lookup"><span data-stu-id="08234-148">In order to create the Docker image, the following code is added to the *build.ps1* script.</span></span> <span data-ttu-id="08234-149">Quand le script est exécuté, l’image `console-random-answer-generator` est créée en utilisant les ressources compilées à partir de MSBuild, comme défini dans la section [Génération de l’application](#building-the-application).</span><span class="sxs-lookup"><span data-stu-id="08234-149">When the script is run, the `console-random-answer-generator` image is created using the assets compiled from MSBuild defined in the [Building the application](#building-the-application) section.</span></span>

```powershell
$ImageName="console-random-answer-generator"

function Invoke-Docker-Build ([string]$ImageName, [string]$ImagePath, [string]$DockerBuildArgs = "") {
    echo "docker build -t $ImageName $ImagePath $DockerBuildArgs"
    Invoke-Expression "docker build -t $ImageName $ImagePath $DockerBuildArgs"
}

Invoke-Docker-Build -ImageName $ImageName -ImagePath "."
```

<span data-ttu-id="08234-150">Exécutez le script à l’aide de `.\build.ps1` à partir de l’invite de commandes PowerShell.</span><span class="sxs-lookup"><span data-stu-id="08234-150">Run the script using `.\build.ps1` from the PowerShell command prompt.</span></span>

<span data-ttu-id="08234-151">Quand la build est terminée, vous pouvez utiliser la commande `docker images` à partir d’une ligne de commande ou d’une invite de commandes PowerShell pour constater que l’image est créée et prête à être exécutée.</span><span class="sxs-lookup"><span data-stu-id="08234-151">When the build is complete, using the `docker images` command from a command line or PowerShell prompt; you'll see that the image is created and ready to be run.</span></span>

```
REPOSITORY                        TAG                 IMAGE ID            CREATED             SIZE
console-random-answer-generator   latest              8f7c807db1b5        8 seconds ago       7.33 GB
```

## <a name="running-the-container"></a><span data-ttu-id="08234-152">Exécution du conteneur</span><span class="sxs-lookup"><span data-stu-id="08234-152">Running the container</span></span>

<span data-ttu-id="08234-153">Vous pouvez démarrer le conteneur à partir de la ligne de commande en utilisant les commandes Docker.</span><span class="sxs-lookup"><span data-stu-id="08234-153">You can start the container from the command line using the Docker commands.</span></span>

```
docker run console-random-answer-generator "Are you a square container?"
```

<span data-ttu-id="08234-154">La sortie est la suivante :</span><span class="sxs-lookup"><span data-stu-id="08234-154">The output is</span></span>

```
The answer to your question: 'Are you a square container?' is Concentrate and ask again on (70C3D48F4343)
```

<span data-ttu-id="08234-155">Si vous exécutez la commande `docker ps -a` à partir de PowerShell, vous pouvez voir que le conteneur existe toujours.</span><span class="sxs-lookup"><span data-stu-id="08234-155">If you run the `docker ps -a` command from PowerShell, you can see that the container still exists.</span></span>

```
CONTAINER ID        IMAGE                             COMMAND                  CREATED             STATUS
70c3d48f4343        console-random-answer-generator   "cmd /S /C ConsoleRan"   2 minutes ago       Exited (0) About a minute ago
```

<span data-ttu-id="08234-156">La colonne STATUS indique que l’application s’est terminée et qu’elle a pu être arrêtée environ une minute auparavant (« About a minute ago »).</span><span class="sxs-lookup"><span data-stu-id="08234-156">The STATUS column shows at "About a minute ago", the application was complete and could be shut down.</span></span> <span data-ttu-id="08234-157">Si la commande était exécutée une centaine de fois, une centaine de conteneurs demeureraient statiques sans aucune tâche à effectuer.</span><span class="sxs-lookup"><span data-stu-id="08234-157">If the command was run a hundred times, there would be a hundred containers left static with no work to do.</span></span> <span data-ttu-id="08234-158">Dans le scénario initial, l’opération idéale était d’effectuer le travail, puis de procéder à un arrêt ou nettoyage.</span><span class="sxs-lookup"><span data-stu-id="08234-158">In the beginning scenario the ideal operation was to do the work and shutdown or cleanup.</span></span> <span data-ttu-id="08234-159">Pour accomplir ce flux de travail, l’ajout de l’option `--rm` à la commande `docker run` permet de supprimer le conteneur dès la réception du signal `Exited`.</span><span class="sxs-lookup"><span data-stu-id="08234-159">To accomplish that workflow, adding the `--rm` option to the `docker run` command will remove the container as soon as the `Exited` signal is received.</span></span>

```
docker run --rm console-random-answer-generator "Are you a square container?"
```

<span data-ttu-id="08234-160">Exécutez la commande avec cette option, puis consultez le résultat de la commande `docker ps -a` ; vous pouvez constater que l’ID de conteneur (`Environment.MachineName`) n’est pas dans la liste.</span><span class="sxs-lookup"><span data-stu-id="08234-160">Running the command with this option and then looking at the output of `docker ps -a` command; notice that the container id (the `Environment.MachineName`) is not in the list.</span></span>

### <a name="running-the-container-using-powershell"></a><span data-ttu-id="08234-161">Exécution du conteneur à l’aide de PowerShell</span><span class="sxs-lookup"><span data-stu-id="08234-161">Running the container using PowerShell</span></span>

<span data-ttu-id="08234-162">Les exemples de fichiers de projet contiennent également un script *run.ps1* qui montre comment utiliser PowerShell pour exécuter l’application acceptant les arguments.</span><span class="sxs-lookup"><span data-stu-id="08234-162">In the sample project files there is also a *run.ps1* which is an example of how to use PowerShell to run the application accepting the arguments.</span></span>

<span data-ttu-id="08234-163">Pour ce faire, ouvrez PowerShell et utilisez la commande suivante :</span><span class="sxs-lookup"><span data-stu-id="08234-163">To run, open PowerShell and use the following command:</span></span>

```powershell
.\run.ps1 "Is this easy or what?"
```

## <a name="summary"></a><span data-ttu-id="08234-164">Récapitulatif</span><span class="sxs-lookup"><span data-stu-id="08234-164">Summary</span></span>

<span data-ttu-id="08234-165">Simplement en ajoutant un fichier Dockerfile et en publiant l’application, vous pouvez exécuter vos applications console .NET Framework dans des conteneurs et tirer enfin parti de l’exécution de plusieurs instances, d’un démarrage/arrêt propre et d’autres fonctionnalités de Windows Server 2016 sans apporter de modification au code de l’application.</span><span class="sxs-lookup"><span data-stu-id="08234-165">Just by adding a Dockerfile and publishing the application, you can containerize your .NET Framework console applications and now take the advantage of running multiple instances, clean start and stop and more Windows Server 2016 capabilities without making any changes to the application code at all.</span></span>
