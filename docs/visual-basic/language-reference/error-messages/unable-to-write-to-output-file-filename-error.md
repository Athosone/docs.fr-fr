---
title: "Impossible d'écrire dans le fichier de sortie '<filename>' : <error>"
ms.date: 07/20/2015
f1_keywords:
- vbc31019
- bc31019
helpviewer_keywords:
- BC31019
ms.assetid: 0845b245-11bb-46fd-95ca-f6cef3c318ef
ms.openlocfilehash: f29eb628c079f65a520cf5e1ccd8afed549f7cad
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61787411"
---
# <a name="unable-to-write-to-output-file-filename-error"></a><span data-ttu-id="74a4b-102">Impossible d’écrire dans le fichier de sortie '\<nom_fichier >': \<erreur ></span><span class="sxs-lookup"><span data-stu-id="74a4b-102">Unable to write to output file '\<filename>': \<error></span></span>
<span data-ttu-id="74a4b-103">Un problème s'est produit pendant la création du fichier.</span><span class="sxs-lookup"><span data-stu-id="74a4b-103">There was a problem creating the file.</span></span>  
  
 <span data-ttu-id="74a4b-104">Vous ne pouvez pas ouvrir un fichier de sortie pour écriture.</span><span class="sxs-lookup"><span data-stu-id="74a4b-104">An output file cannot be opened for writing.</span></span> <span data-ttu-id="74a4b-105">Le fichier (ou le dossier qui le contient) est peut être ouvert pour un usage exclusif par un autre processus, ou a son attribut de lecture seule défini.</span><span class="sxs-lookup"><span data-stu-id="74a4b-105">The file (or the folder containing the file) may be opened for exclusive use by another process, or it may have its read-only attribute set.</span></span>  
  
 <span data-ttu-id="74a4b-106">Les situations courantes dans lesquelles un fichier est ouvert de manière exclusive sont les suivantes :</span><span class="sxs-lookup"><span data-stu-id="74a4b-106">Common situations where a file is opened exclusively are:</span></span>  
  
- <span data-ttu-id="74a4b-107">L'application est déjà en cours d'exécution et utilise ses fichiers.</span><span class="sxs-lookup"><span data-stu-id="74a4b-107">The application is already running and using its files.</span></span> <span data-ttu-id="74a4b-108">Pour résoudre ce problème, vérifiez que l'application n'est pas en cours d'exécution.</span><span class="sxs-lookup"><span data-stu-id="74a4b-108">To solve this problem, make sure that the application is not running.</span></span>  
  
- <span data-ttu-id="74a4b-109">Une autre application a ouvert le fichier.</span><span class="sxs-lookup"><span data-stu-id="74a4b-109">Another application has opened the file.</span></span> <span data-ttu-id="74a4b-110">Pour résoudre ce problème, vérifiez qu'aucune autre application n'accède aux fichiers.</span><span class="sxs-lookup"><span data-stu-id="74a4b-110">To solve this problem, make sure that no other application is accessing the files.</span></span> <span data-ttu-id="74a4b-111">Il n'est pas toujours évident de savoir quelle application accède à vos fichiers ; le cas échéant, le plus facile est de redémarrer l'ordinateur pour arrêter l'application.</span><span class="sxs-lookup"><span data-stu-id="74a4b-111">It is not always obvious which application is accessing your files; in that case, restarting the computer might be the easiest way to terminate the application.</span></span>  
  
 <span data-ttu-id="74a4b-112">Si au moins un des fichiers de sortie du projet est marqué en lecture seule, cette exception est levée.</span><span class="sxs-lookup"><span data-stu-id="74a4b-112">If even one of the project output files is marked as read-only, this exception will be thrown.</span></span>  
  
 <span data-ttu-id="74a4b-113">**ID d’erreur :** BC31019</span><span class="sxs-lookup"><span data-stu-id="74a4b-113">**Error ID:** BC31019</span></span>  
  
## <a name="to-correct-this-error"></a><span data-ttu-id="74a4b-114">Pour corriger cette erreur</span><span class="sxs-lookup"><span data-stu-id="74a4b-114">To correct this error</span></span>  
  
1. <span data-ttu-id="74a4b-115">Recompilez le programme pour voir si l'erreur se produit à nouveau.</span><span class="sxs-lookup"><span data-stu-id="74a4b-115">Compile the program again to see if the error recurs.</span></span>  
  
2. <span data-ttu-id="74a4b-116">Si l’erreur persiste, enregistrez votre travail et redémarrez Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="74a4b-116">If the error continues, save your work and restart Visual Studio.</span></span>  
  
3. <span data-ttu-id="74a4b-117">Si l'erreur continue, redémarrez l'ordinateur.</span><span class="sxs-lookup"><span data-stu-id="74a4b-117">If the error continues, restart the computer.</span></span>  
  
4. <span data-ttu-id="74a4b-118">Si l’erreur se reproduit, réinstallez Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="74a4b-118">If the error recurs, reinstall Visual Basic.</span></span>  
  
5. <span data-ttu-id="74a4b-119">Si l'erreur persiste après la réinstallation, avertissez les services de support technique Microsoft.</span><span class="sxs-lookup"><span data-stu-id="74a4b-119">If the error persists after reinstallation, notify Microsoft Product Support Services.</span></span>  
  
### <a name="to-check-file-attributes-in-file-explorer"></a><span data-ttu-id="74a4b-120">Pour vérifier les attributs de fichier dans l'Explorateur de fichiers</span><span class="sxs-lookup"><span data-stu-id="74a4b-120">To check file attributes in File Explorer</span></span>  
  
1. <span data-ttu-id="74a4b-121">Ouvrez le dossier qui vous intéresse.</span><span class="sxs-lookup"><span data-stu-id="74a4b-121">Open the folder you are interested in.</span></span>  
  
2. <span data-ttu-id="74a4b-122">Cliquez sur le **vues** icône et choisissez **détails**.</span><span class="sxs-lookup"><span data-stu-id="74a4b-122">Click the **Views** icon and choose **Details**.</span></span>  
  
3. <span data-ttu-id="74a4b-123">Cliquez sur l’en-tête de colonne, puis choisissez **attributs** dans la liste déroulante.</span><span class="sxs-lookup"><span data-stu-id="74a4b-123">Right-click the column header, and choose **Attributes** from the drop-down list.</span></span>  
  
### <a name="to-change-the-attributes-of-a-file-or-folder"></a><span data-ttu-id="74a4b-124">Pour modifier les attributs d’un fichier ou d’un dossier</span><span class="sxs-lookup"><span data-stu-id="74a4b-124">To change the attributes of a file or folder</span></span>  
  
1. <span data-ttu-id="74a4b-125">Dans **Explorateur de fichiers**, cliquez sur le fichier ou dossier et choisissez **propriétés**.</span><span class="sxs-lookup"><span data-stu-id="74a4b-125">In **File Explorer**, right-click the file or folder and choose **Properties**.</span></span>  
  
2. <span data-ttu-id="74a4b-126">Dans le **attributs** section de la **général** onglet, désactivez le **en lecture seule** boîte.</span><span class="sxs-lookup"><span data-stu-id="74a4b-126">In the **Attributes** section of the **General** tab, clear the **Read-only** box.</span></span>  
  
3. <span data-ttu-id="74a4b-127">Appuyez sur **OK**.</span><span class="sxs-lookup"><span data-stu-id="74a4b-127">Press **OK**.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="74a4b-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="74a4b-128">See also</span></span>

- [<span data-ttu-id="74a4b-129">Nous contacter</span><span class="sxs-lookup"><span data-stu-id="74a4b-129">Talk to Us</span></span>](/visualstudio/ide/talk-to-us)
