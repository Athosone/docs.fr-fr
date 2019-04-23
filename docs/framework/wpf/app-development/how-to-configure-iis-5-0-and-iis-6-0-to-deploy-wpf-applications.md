---
title: 'Procédure : Configurer IIS 5.0 et IIS 6.0 pour déployer des applications WPF'
ms.date: 03/30/2017
helpviewer_keywords:
- MIME types [WPF], registering
- adjusting content expiration setting [WPF]
- registering file extensions [WPF]
- deploying applications [WPF]
- applications [WPF], deploying
- Web servers [WPF], configuring to deploy WPF applications
- configuring Web servers to deploy WPF applications [WPF]
- content expiration setting [WPF], adjusting
- file extensions [WPF], registering
- registering MIME types [WPF]
ms.assetid: c6e8c2cb-9ba2-4e75-a0d5-180ec9639433
ms.openlocfilehash: 6fa00c4ced8c05d056703560e5740689c6dcfe39
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/22/2019
ms.locfileid: "59973666"
---
# <a name="how-to-configure-iis-50-and-iis-60-to-deploy-wpf-applications"></a><span data-ttu-id="68fb6-102">Procédure : Configurer IIS 5.0 et IIS 6.0 pour déployer des applications WPF</span><span class="sxs-lookup"><span data-stu-id="68fb6-102">How to: Configure IIS 5.0 and IIS 6.0 to Deploy WPF Applications</span></span>

<span data-ttu-id="68fb6-103">Vous pouvez déployer une application [!INCLUDE[TLA#tla_winclient](../../../../includes/tlasharptla-winclient-md.md)] à partir de la plupart des serveurs web, tant qu’ils sont configurés avec les types [!INCLUDE[TLA#tla_mime](../../../../includes/tlasharptla-mime-md.md)] appropriés.</span><span class="sxs-lookup"><span data-stu-id="68fb6-103">You can deploy a [!INCLUDE[TLA#tla_winclient](../../../../includes/tlasharptla-winclient-md.md)] application from most Web servers, as long as they are configured with the appropriate [!INCLUDE[TLA#tla_mime](../../../../includes/tlasharptla-mime-md.md)] types.</span></span> <span data-ttu-id="68fb6-104">Par défaut, [!INCLUDE[TLA#tla_iis70](../../../../includes/tlasharptla-iis70-md.md)] est configuré avec ces types [!INCLUDE[TLA2#tla_mime](../../../../includes/tla2sharptla-mime-md.md)], mais [!INCLUDE[TLA#tla_iis50](../../../../includes/tlasharptla-iis50-md.md)] et [!INCLUDE[TLA#tla_iis60](../../../../includes/tlasharptla-iis60-md.md)] ne le sont pas.</span><span class="sxs-lookup"><span data-stu-id="68fb6-104">By default, [!INCLUDE[TLA#tla_iis70](../../../../includes/tlasharptla-iis70-md.md)] is configured with these [!INCLUDE[TLA2#tla_mime](../../../../includes/tla2sharptla-mime-md.md)] types, but [!INCLUDE[TLA#tla_iis50](../../../../includes/tlasharptla-iis50-md.md)] and [!INCLUDE[TLA#tla_iis60](../../../../includes/tlasharptla-iis60-md.md)] are not.</span></span>

<span data-ttu-id="68fb6-105">Cette rubrique décrit comment configurer [!INCLUDE[TLA#tla_iis50](../../../../includes/tlasharptla-iis50-md.md)] et [!INCLUDE[TLA#tla_iis60](../../../../includes/tlasharptla-iis60-md.md)] pour déployer des applications [!INCLUDE[TLA2#tla_winclient](../../../../includes/tla2sharptla-winclient-md.md)].</span><span class="sxs-lookup"><span data-stu-id="68fb6-105">This topic describes how to configure [!INCLUDE[TLA#tla_iis50](../../../../includes/tlasharptla-iis50-md.md)] and [!INCLUDE[TLA#tla_iis60](../../../../includes/tlasharptla-iis60-md.md)] to deploy [!INCLUDE[TLA2#tla_winclient](../../../../includes/tla2sharptla-winclient-md.md)] applications.</span></span>

> [!NOTE]
> <span data-ttu-id="68fb6-106">Vous pouvez vérifier le *UserAgent* chaîne dans le Registre pour déterminer si un système dispose de .NET Framework est installé.</span><span class="sxs-lookup"><span data-stu-id="68fb6-106">You can check the *UserAgent* string in the registry to determine whether a system has .NET Framework installed.</span></span> <span data-ttu-id="68fb6-107">Pour plus d’informations et un script qui examine le *UserAgent* chaîne pour déterminer si .NET Framework est installée sur un système, consultez [détecter si le .NET Framework 3.0 est installé](how-to-detect-whether-the-net-framework-3-0-is-installed.md).</span><span class="sxs-lookup"><span data-stu-id="68fb6-107">For details and a script that examines the *UserAgent* string to determine whether .NET Framework is installed on a system, see [Detect Whether the .NET Framework 3.0 Is Installed](how-to-detect-whether-the-net-framework-3-0-is-installed.md).</span></span>

<a name="content_expiration"></a>

## <a name="adjust-the-content-expiration-setting"></a><span data-ttu-id="68fb6-108">Régler le paramètre d’expiration du contenu</span><span class="sxs-lookup"><span data-stu-id="68fb6-108">Adjust the Content Expiration Setting</span></span>

<span data-ttu-id="68fb6-109">Vous devez régler le paramètre d’expiration du contenu sur 1 minute.</span><span class="sxs-lookup"><span data-stu-id="68fb6-109">You should adjust the content expiration setting to 1 minute.</span></span> <span data-ttu-id="68fb6-110">La procédure suivante décrit comment faire avec [!INCLUDE[TLA2#tla_iis5](../../../../includes/tla2sharptla-iis5-md.md)].</span><span class="sxs-lookup"><span data-stu-id="68fb6-110">The following procedure outlines how to do this with [!INCLUDE[TLA2#tla_iis5](../../../../includes/tla2sharptla-iis5-md.md)].</span></span>

1. <span data-ttu-id="68fb6-111">Cliquez sur le menu **Démarrer**, pointez sur **Outils d’administration**, puis cliquez sur **Gestionnaire des services Internet (IIS)**.</span><span class="sxs-lookup"><span data-stu-id="68fb6-111">Click the **Start** menu, point to **Administrative Tools**, and click **Internet Information Services (IIS) Manager**.</span></span> <span data-ttu-id="68fb6-112">Vous pouvez également lancer cette application à partir de la ligne de commande avec « %SystemRoot%\system32\inetsrv\iis.msc ».</span><span class="sxs-lookup"><span data-stu-id="68fb6-112">You can also launch this application from the command line with "%SystemRoot%\system32\inetsrv\iis.msc".</span></span>

2. <span data-ttu-id="68fb6-113">Développez l’arborescence [!INCLUDE[TLA2#tla_iis5](../../../../includes/tla2sharptla-iis5-md.md)] jusqu’à trouver le nœud **Site Web par défaut**.</span><span class="sxs-lookup"><span data-stu-id="68fb6-113">Expand the [!INCLUDE[TLA2#tla_iis5](../../../../includes/tla2sharptla-iis5-md.md)] tree until you find the **Default Web site** node.</span></span>

3. <span data-ttu-id="68fb6-114">Cliquez avec le bouton droit sur **Site Web par défaut** et sélectionnez **Propriétés** dans le menu contextuel.</span><span class="sxs-lookup"><span data-stu-id="68fb6-114">Right-click **Default Web site** and select **Properties** from the context menu.</span></span>

4. <span data-ttu-id="68fb6-115">Sélectionnez l’onglet **En-têtes HTTP** et cliquez sur « Activer l’expiration de contenu ».</span><span class="sxs-lookup"><span data-stu-id="68fb6-115">Select the **HTTP Headers** tab and click "Enable Content Expiration".</span></span>

5. <span data-ttu-id="68fb6-116">Paramétrez le contenu pour qu’il expire après une minute.</span><span class="sxs-lookup"><span data-stu-id="68fb6-116">Set the content to expire after 1 minute.</span></span>

<a name="register_mime_types"></a>

## <a name="register-mime-types-and-file-extensions"></a><span data-ttu-id="68fb6-117">Inscrire des types MIME et des extensions de fichiers</span><span class="sxs-lookup"><span data-stu-id="68fb6-117">Register MIME Types and File Extensions</span></span>

<span data-ttu-id="68fb6-118">Vous devez inscrire plusieurs extensions de fichiers et types [!INCLUDE[TLA2#tla_mime](../../../../includes/tla2sharptla-mime-md.md)] pour que le navigateur du système client puisse charger le gestionnaire approprié.</span><span class="sxs-lookup"><span data-stu-id="68fb6-118">You must register several [!INCLUDE[TLA2#tla_mime](../../../../includes/tla2sharptla-mime-md.md)] types and file extensions so that the browser on the client's system can load the correct handler.</span></span> <span data-ttu-id="68fb6-119">Vous devez ajouter les types suivants :</span><span class="sxs-lookup"><span data-stu-id="68fb6-119">You need to add the following types:</span></span>

|<span data-ttu-id="68fb6-120">Extension</span><span class="sxs-lookup"><span data-stu-id="68fb6-120">Extension</span></span>|<span data-ttu-id="68fb6-121">Type MIME</span><span class="sxs-lookup"><span data-stu-id="68fb6-121">MIME Type</span></span>|
|---------------|---------------|
|<span data-ttu-id="68fb6-122">.manifest</span><span class="sxs-lookup"><span data-stu-id="68fb6-122">.manifest</span></span>|<span data-ttu-id="68fb6-123">application/manifest</span><span class="sxs-lookup"><span data-stu-id="68fb6-123">application/manifest</span></span>|
|<span data-ttu-id="68fb6-124">.xaml</span><span class="sxs-lookup"><span data-stu-id="68fb6-124">.xaml</span></span>|<span data-ttu-id="68fb6-125">application/xaml+xml</span><span class="sxs-lookup"><span data-stu-id="68fb6-125">application/xaml+xml</span></span>|
|<span data-ttu-id="68fb6-126">.application</span><span class="sxs-lookup"><span data-stu-id="68fb6-126">.application</span></span>|<span data-ttu-id="68fb6-127">application/x-ms-application</span><span class="sxs-lookup"><span data-stu-id="68fb6-127">application/x-ms-application</span></span>|
|<span data-ttu-id="68fb6-128">.xbap</span><span class="sxs-lookup"><span data-stu-id="68fb6-128">.xbap</span></span>|<span data-ttu-id="68fb6-129">application/x-ms-xbap</span><span class="sxs-lookup"><span data-stu-id="68fb6-129">application/x-ms-xbap</span></span>|
|<span data-ttu-id="68fb6-130">.deploy</span><span class="sxs-lookup"><span data-stu-id="68fb6-130">.deploy</span></span>|<span data-ttu-id="68fb6-131">application/octet-stream</span><span class="sxs-lookup"><span data-stu-id="68fb6-131">application/octet-stream</span></span>|
|<span data-ttu-id="68fb6-132">.xps</span><span class="sxs-lookup"><span data-stu-id="68fb6-132">.xps</span></span>|<span data-ttu-id="68fb6-133">application/vnd.ms-xpsdocument</span><span class="sxs-lookup"><span data-stu-id="68fb6-133">application/vnd.ms-xpsdocument</span></span>|

> [!NOTE]
> <span data-ttu-id="68fb6-134">Vous n’avez pas besoin d’inscrire d’extensions de fichiers ou de types [!INCLUDE[TLA2#tla_mime](../../../../includes/tla2sharptla-mime-md.md)] sur les systèmes clients.</span><span class="sxs-lookup"><span data-stu-id="68fb6-134">You do not need to register [!INCLUDE[TLA2#tla_mime](../../../../includes/tla2sharptla-mime-md.md)] types or file extensions on client systems.</span></span> <span data-ttu-id="68fb6-135">Ils sont inscrits automatiquement lorsque vous installez Microsoft .NET Framework.</span><span class="sxs-lookup"><span data-stu-id="68fb6-135">They are registered automatically when you install Microsoft .NET Framework.</span></span>

<span data-ttu-id="68fb6-136">L’exemple Microsoft Visual Basic Scripting Edition (VBScript) suivant ajoute automatiquement le nécessaire [!INCLUDE[TLA2#tla_mime](../../../../includes/tla2sharptla-mime-md.md)] types [!INCLUDE[TLA2#tla_iis5](../../../../includes/tla2sharptla-iis5-md.md)].</span><span class="sxs-lookup"><span data-stu-id="68fb6-136">The following Microsoft Visual Basic Scripting Edition (VBScript) sample automatically adds the necessary [!INCLUDE[TLA2#tla_mime](../../../../includes/tla2sharptla-mime-md.md)] types to [!INCLUDE[TLA2#tla_iis5](../../../../includes/tla2sharptla-iis5-md.md)].</span></span> <span data-ttu-id="68fb6-137">Pour utiliser le script, copiez le code dans un fichier .vbs sur votre serveur.</span><span class="sxs-lookup"><span data-stu-id="68fb6-137">To use the script, copy the code to a .vbs file on your server.</span></span> <span data-ttu-id="68fb6-138">Ensuite, exécutez le script en exécutant le fichier à partir de la ligne de commande ou en double-cliquant sur le fichier dans [!INCLUDE[TLA#tla_winexpl](../../../../includes/tlasharptla-winexpl-md.md)].</span><span class="sxs-lookup"><span data-stu-id="68fb6-138">Then, run the script by running the file from the command line or double-clicking the file in [!INCLUDE[TLA#tla_winexpl](../../../../includes/tlasharptla-winexpl-md.md)].</span></span>

```vb
' This script adds the necessary Windows Presentation Foundation MIME types
' to an IIS Server.
' To use this script, just double-click or execute it from a command line.
' Running this script multiple times results in multiple entries in the IIS MimeMap.

Dim MimeMapObj, MimeMapArray, MimeTypesToAddArray, WshShell, oExec
Const ADS_PROPERTY_UPDATE = 2

' Set the MIME types to be added
MimeTypesToAddArray = Array(".manifest", "application/manifest", ".xaml", _
    "application/xaml+xml", ".application", "application/x-ms-application", _
    ".deploy", "application/octet-stream", ".xbap", "application/x-ms-xbap", _
    ".xps", "application/vnd.ms-xpsdocument")

' Get the MimeMap object
Set MimeMapObj = GetObject("IIS://LocalHost/MimeMap")

' Call AddMimeType for every pair of extension/MIME type
For counter = 0 to UBound(MimeTypesToAddArray) Step 2
    AddMimeType MimeTypesToAddArray(counter), MimeTypesToAddArray(counter+1)
Next

' Create a Shell object
Set WshShell = CreateObject("WScript.Shell")

' Stop and Start the IIS Service
Set oExec = WshShell.Exec("net stop w3svc")
Do While oExec.Status = 0
    WScript.Sleep 100
Loop

Set oExec = WshShell.Exec("net start w3svc")
Do While oExec.Status = 0
    WScript.Sleep 100
Loop

Set oExec = Nothing

' Report status to user
WScript.Echo "Windows Presentation Foundation MIME types have been registered."

' AddMimeType Sub
Sub AddMimeType (Ext, MType)

    ' Get the mappings from the MimeMap property.
    MimeMapArray = MimeMapObj.GetEx("MimeMap")

    ' Add a new mapping.
    i = UBound(MimeMapArray) + 1
    ReDim Preserve MimeMapArray(i)
    Set MimeMapArray(i) = CreateObject("MimeMap")
    MimeMapArray(i).Extension = Ext
    MimeMapArray(i).MimeType = MType
    MimeMapObj.PutEx ADS_PROPERTY_UPDATE, "MimeMap", MimeMapArray
    MimeMapObj.SetInfo

End Sub
```

> [!NOTE]
> <span data-ttu-id="68fb6-139">Si vous exécutez ce script plusieurs fois, plusieurs entrées de mappage [!INCLUDE[TLA2#tla_mime](../../../../includes/tla2sharptla-mime-md.md)] sont créées dans la métabase [!INCLUDE[TLA#tla_iis50](../../../../includes/tlasharptla-iis50-md.md)] ou [!INCLUDE[TLA#tla_iis60](../../../../includes/tlasharptla-iis60-md.md)].</span><span class="sxs-lookup"><span data-stu-id="68fb6-139">Running this script multiple times creates multiple [!INCLUDE[TLA2#tla_mime](../../../../includes/tla2sharptla-mime-md.md)] map entries in the [!INCLUDE[TLA#tla_iis50](../../../../includes/tlasharptla-iis50-md.md)] or [!INCLUDE[TLA#tla_iis60](../../../../includes/tlasharptla-iis60-md.md)] metabase.</span></span>

<span data-ttu-id="68fb6-140">Après avoir exécuté ce script, vous ne verrez peut-être pas de types [!INCLUDE[TLA2#tla_mime](../../../../includes/tla2sharptla-mime-md.md)] supplémentaires à partir de la [!INCLUDE[TLA#tla_mmc](../../../../includes/tlasharptla-mmc-md.md)] [!INCLUDE[TLA#tla_iis50](../../../../includes/tlasharptla-iis50-md.md)] ou [!INCLUDE[TLA#tla_iis60](../../../../includes/tlasharptla-iis60-md.md)].</span><span class="sxs-lookup"><span data-stu-id="68fb6-140">After you have run this script, you may not see additional [!INCLUDE[TLA2#tla_mime](../../../../includes/tla2sharptla-mime-md.md)] types from the [!INCLUDE[TLA#tla_iis50](../../../../includes/tlasharptla-iis50-md.md)] or [!INCLUDE[TLA#tla_iis60](../../../../includes/tlasharptla-iis60-md.md)] [!INCLUDE[TLA#tla_mmc](../../../../includes/tlasharptla-mmc-md.md)].</span></span> <span data-ttu-id="68fb6-141">Toutefois, ces types [!INCLUDE[TLA2#tla_mime](../../../../includes/tla2sharptla-mime-md.md)] ont été ajoutés à la métabase [!INCLUDE[TLA#tla_iis50](../../../../includes/tlasharptla-iis50-md.md)] ou [!INCLUDE[TLA#tla_iis60](../../../../includes/tlasharptla-iis60-md.md)].</span><span class="sxs-lookup"><span data-stu-id="68fb6-141">However, these [!INCLUDE[TLA2#tla_mime](../../../../includes/tla2sharptla-mime-md.md)] types have been added to the [!INCLUDE[TLA#tla_iis50](../../../../includes/tlasharptla-iis50-md.md)] or [!INCLUDE[TLA#tla_iis60](../../../../includes/tlasharptla-iis60-md.md)] metabase.</span></span> <span data-ttu-id="68fb6-142">Le script suivant affichera tous les types [!INCLUDE[TLA2#tla_mime](../../../../includes/tla2sharptla-mime-md.md)] dans la métabase [!INCLUDE[TLA#tla_iis50](../../../../includes/tlasharptla-iis50-md.md)] ou [!INCLUDE[TLA#tla_iis60](../../../../includes/tlasharptla-iis60-md.md)].</span><span class="sxs-lookup"><span data-stu-id="68fb6-142">The following script will display all the [!INCLUDE[TLA2#tla_mime](../../../../includes/tla2sharptla-mime-md.md)] types in the [!INCLUDE[TLA#tla_iis50](../../../../includes/tlasharptla-iis50-md.md)] or [!INCLUDE[TLA#tla_iis60](../../../../includes/tlasharptla-iis60-md.md)] metabase.</span></span>

```vb
' This script lists the MIME types for an IIS Server.
' To use this script, just double-click or execute it from a command line
' by calling cscript.exe

dim mimeMapEntry, allMimeMaps

' Get the MimeMap object.
Set mimeMapEntry = GetObject("IIS://localhost/MimeMap")
allMimeMaps = mimeMapEntry.GetEx("MimeMap")

' Display the mappings in the table.
For Each mimeMap In allMimeMaps
    WScript.Echo(mimeMap.MimeType & " (" & mimeMap.Extension + ")")
Next
```

<span data-ttu-id="68fb6-143">Enregistrez le script en tant que fichier `.vbs` (par exemple, `DiscoverIISMimeTypes.vbs`) et exécutez-le à partir de l’invite de commandes à l’aide de la commande suivante :</span><span class="sxs-lookup"><span data-stu-id="68fb6-143">Save the script as a `.vbs` file (for example, `DiscoverIISMimeTypes.vbs`) and run it from the command prompt using the following command:</span></span>

```console
cscript DiscoverIISMimeTypes.vbs
```
