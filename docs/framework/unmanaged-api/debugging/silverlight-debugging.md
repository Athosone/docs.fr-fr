---
title: Débogage Silverlight
ms.date: 03/30/2017
helpviewer_keywords:
- debugging API [Silverlight]
- Silverlight, debugging
ms.assetid: 5e903e04-17d0-4014-ac9a-a43330ec8b1c
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 1d20bc002e52c3c6a42b45c0d1c5d559e65dc52c
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61763661"
---
# <a name="silverlight-debugging"></a><span data-ttu-id="af460-102">Débogage Silverlight</span><span class="sxs-lookup"><span data-stu-id="af460-102">Silverlight Debugging</span></span>
<span data-ttu-id="af460-103">Les rubriques de cette section décrivent l'environnement et les interfaces fournis par le Common Language Runtime (CLR) pour prendre en charge le débogage des applications Silverlight qui s'exécutent sur le système d'exploitation Windows ou sur la plateforme Macintosh.</span><span class="sxs-lookup"><span data-stu-id="af460-103">The topics in this section describe the environment and interfaces that the common language runtime (CLR) provides to support debugging Silverlight-based applications that are running on the Windows operating system, or on the Macintosh platform.</span></span>  
  
## <a name="in-this-section"></a><span data-ttu-id="af460-104">Dans cette section</span><span class="sxs-lookup"><span data-stu-id="af460-104">In This Section</span></span>  
 [<span data-ttu-id="af460-105">EnumerateCLRs, fonction</span><span class="sxs-lookup"><span data-stu-id="af460-105">EnumerateCLRs Function</span></span>](../../../../docs/framework/unmanaged-api/debugging/enumerateclrs-function.md)  
 <span data-ttu-id="af460-106">Fournit un mécanisme pour énumérer les CLR dans un processus.</span><span class="sxs-lookup"><span data-stu-id="af460-106">Provides a mechanism for enumerating the CLRs in a process.</span></span>  
  
 [<span data-ttu-id="af460-107">CloseCLREnumeration, fonction</span><span class="sxs-lookup"><span data-stu-id="af460-107">CloseCLREnumeration Function</span></span>](../../../../docs/framework/unmanaged-api/debugging/closeclrenumeration-function.md)  
 <span data-ttu-id="af460-108">Ferme les événements de continuer-démarrage CLR valides situés dans un tableau de handles retourné par la [fonction EnumerateCLRs](../../../../docs/framework/unmanaged-api/debugging/enumerateclrs-function.md)et libère la mémoire pour les tableaux de chemin d’accès de handles et de chaînes.</span><span class="sxs-lookup"><span data-stu-id="af460-108">Closes any valid CLR continue-startup events located in an array of handles returned by the [EnumerateCLRs Function](../../../../docs/framework/unmanaged-api/debugging/enumerateclrs-function.md), and frees the memory for the handle and string path arrays.</span></span>  
  
 [<span data-ttu-id="af460-109">CreateCoreClrDebugTarget, fonction</span><span class="sxs-lookup"><span data-stu-id="af460-109">CreateCoreClrDebugTarget Function</span></span>](../../../../docs/framework/unmanaged-api/debugging/createcoreclrdebugtarget-function.md)  
 <span data-ttu-id="af460-110">Crée une connexion à une cible distante pour l'énumération des processus et du runtime.</span><span class="sxs-lookup"><span data-stu-id="af460-110">Creates a connection to a remote target for process and runtime enumeration.</span></span>  
  
 [<span data-ttu-id="af460-111">CreateCordbObject, fonction</span><span class="sxs-lookup"><span data-stu-id="af460-111">CreateCordbObject Function</span></span>](../../../../docs/framework/unmanaged-api/debugging/createcordbobject-function.md)  
 <span data-ttu-id="af460-112">Crée une interface de débogueur qui fournit les fonctionnalités d'instanciation d'une session de débogage managée sur un processus distant.</span><span class="sxs-lookup"><span data-stu-id="af460-112">Creates a debugger interface that provides functionality for instantiating a managed debugging session on a remote process.</span></span>  
  
 [<span data-ttu-id="af460-113">CreateVersionStringFromModule, fonction</span><span class="sxs-lookup"><span data-stu-id="af460-113">CreateVersionStringFromModule Function</span></span>](../../../../docs/framework/unmanaged-api/debugging/createversionstringfrommodule-function.md)  
 <span data-ttu-id="af460-114">Crée une chaîne de version à partir d'un chemin d'accès au CLR dans un processus cible.</span><span class="sxs-lookup"><span data-stu-id="af460-114">Creates a version string from a CLR path in a target process.</span></span>  
  
 [<span data-ttu-id="af460-115">CreateDebuggingInterfaceFromVersion, fonction</span><span class="sxs-lookup"><span data-stu-id="af460-115">CreateDebuggingInterfaceFromVersion Function</span></span>](../../../../docs/framework/unmanaged-api/debugging/createdebugginginterfacefromversion-function-for-silverlight.md)  
 <span data-ttu-id="af460-116">Accepte une chaîne de version CLR retournée à partir de [fonction CreateVersionStringFromModule](../../../../docs/framework/unmanaged-api/debugging/createversionstringfrommodule-function.md)de fonction et retourne une interface de débogueur correspondante.</span><span class="sxs-lookup"><span data-stu-id="af460-116">Accepts a CLR version string returned from [CreateVersionStringFromModule Function](../../../../docs/framework/unmanaged-api/debugging/createversionstringfrommodule-function.md)function, and returns a corresponding debugger interface.</span></span>  
  
 [<span data-ttu-id="af460-117">CoreClrDebugProcInfo, structure</span><span class="sxs-lookup"><span data-stu-id="af460-117">CoreClrDebugProcInfo Structure</span></span>](../../../../docs/framework/unmanaged-api/debugging/coreclrdebugprocinfo-structure.md)  
 <span data-ttu-id="af460-118">Représente un processus qui s'exécute sur un ordinateur distant.</span><span class="sxs-lookup"><span data-stu-id="af460-118">Represents a process that is running on a remote machine.</span></span>  
  
 [<span data-ttu-id="af460-119">CoreClrDebugRuntimeInfo, structure</span><span class="sxs-lookup"><span data-stu-id="af460-119">CoreClrDebugRuntimeInfo Structure</span></span>](../../../../docs/framework/unmanaged-api/debugging/coreclrdebugruntimeinfo-structure.md)  
 <span data-ttu-id="af460-120">Représente une instance du CLR qui est chargée dans un processus sur un ordinateur distant.</span><span class="sxs-lookup"><span data-stu-id="af460-120">Represents a CLR instance that is loaded in a process on a remote machine.</span></span>  
  
 [<span data-ttu-id="af460-121">GetStartupNotificationEvent, fonction</span><span class="sxs-lookup"><span data-stu-id="af460-121">GetStartupNotificationEvent Function</span></span>](../../../../docs/framework/unmanaged-api/debugging/getstartupnotificationevent-function.md)  
 <span data-ttu-id="af460-122">Crée ou ouvre un gestionnaire d'événements qui sera signalé par un Common Language Runtime (CLR) qui est chargé dans le processus cible spécifié.</span><span class="sxs-lookup"><span data-stu-id="af460-122">Creates or opens an event handle that will be signaled upon by any common language runtime (CLR) that is loading in the specified target process.</span></span>  
  
 [<span data-ttu-id="af460-123">ICoreClrDebugTarget, interface</span><span class="sxs-lookup"><span data-stu-id="af460-123">ICoreClrDebugTarget Interface</span></span>](../../../../docs/framework/unmanaged-api/debugging/icoreclrdebugtarget-interface.md)  
 <span data-ttu-id="af460-124">Crée une connexion à une cible distante pour l'énumération des processus et du runtime.</span><span class="sxs-lookup"><span data-stu-id="af460-124">Creates a connection to a remote target for process and runtime enumeration.</span></span>  
  
 [<span data-ttu-id="af460-125">InitDbgTransportManager, fonction</span><span class="sxs-lookup"><span data-stu-id="af460-125">InitDbgTransportManager Function</span></span>](../../../../docs/framework/unmanaged-api/debugging/initdbgtransportmanager-function.md)  
 <span data-ttu-id="af460-126">Initialise le gestionnaire de transport pour se connecter à une cible distante pour l'énumération des processus et du runtime.</span><span class="sxs-lookup"><span data-stu-id="af460-126">Initializes the transport manager to connect to a remote target for process and runtime enumeration.</span></span>  
  
 [<span data-ttu-id="af460-127">ShutdownDbgTransportManager, fonction</span><span class="sxs-lookup"><span data-stu-id="af460-127">ShutdownDbgTransportManager Function</span></span>](../../../../docs/framework/unmanaged-api/debugging/shutdowndbgtransportmanager-function.md)  
 <span data-ttu-id="af460-128">Arrête le gestionnaire de transport pour une connexion à un ordinateur cible distant.</span><span class="sxs-lookup"><span data-stu-id="af460-128">Shuts down the transport manager for a connection to a remote target machine.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="af460-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="af460-129">See also</span></span>

- [<span data-ttu-id="af460-130">Coclasses de débogage</span><span class="sxs-lookup"><span data-stu-id="af460-130">Debugging Coclasses</span></span>](../../../../docs/framework/unmanaged-api/debugging/debugging-coclasses.md)
- [<span data-ttu-id="af460-131">Interfaces de débogage</span><span class="sxs-lookup"><span data-stu-id="af460-131">Debugging Interfaces</span></span>](../../../../docs/framework/unmanaged-api/debugging/debugging-interfaces.md)
- [<span data-ttu-id="af460-132">Fonctions statiques globales de débogage</span><span class="sxs-lookup"><span data-stu-id="af460-132">Debugging Global Static Functions</span></span>](../../../../docs/framework/unmanaged-api/debugging/debugging-global-static-functions.md)
- [<span data-ttu-id="af460-133">Énumérations de débogage</span><span class="sxs-lookup"><span data-stu-id="af460-133">Debugging Enumerations</span></span>](../../../../docs/framework/unmanaged-api/debugging/debugging-enumerations.md)
- [<span data-ttu-id="af460-134">Structures de débogage</span><span class="sxs-lookup"><span data-stu-id="af460-134">Debugging Structures</span></span>](../../../../docs/framework/unmanaged-api/debugging/debugging-structures.md)
