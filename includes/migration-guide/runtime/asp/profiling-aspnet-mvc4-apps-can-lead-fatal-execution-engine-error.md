---
ms.openlocfilehash: 439a4976482639cd2e4e17315ec1a53ca54aa477
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59803912"
---
### <a name="profiling-aspnet-mvc4-apps-can-lead-to-fatal-execution-engine-error"></a><span data-ttu-id="02f67-101">Le profilage des applications ASP.NET MVC4 peut aboutir à une erreur irrécupérable du moteur d’exécution</span><span class="sxs-lookup"><span data-stu-id="02f67-101">Profiling ASP.Net MVC4 apps can lead to Fatal Execution Engine Error</span></span>

|   |   |
|---|---|
|<span data-ttu-id="02f67-102">Détails</span><span class="sxs-lookup"><span data-stu-id="02f67-102">Details</span></span>|<span data-ttu-id="02f67-103">Les profileurs qui utilisent des assemblys NGEN /profil peuvent planter des applications ASP.NET MVC4 profilées au démarrage avec une exception irrécupérable du moteur d’exécution</span><span class="sxs-lookup"><span data-stu-id="02f67-103">Profilers using NGEN /Profile assemblies may crash profiled ASP.NET MVC4 applications on startup with a 'Fatal Execution Engine Exception'</span></span>|
|<span data-ttu-id="02f67-104">Suggestion</span><span class="sxs-lookup"><span data-stu-id="02f67-104">Suggestion</span></span>|<span data-ttu-id="02f67-105">Ce problème a été résolu dans .NET Framework 4.5.2.</span><span class="sxs-lookup"><span data-stu-id="02f67-105">This issue is fixed in the .NET Framework 4.5.2.</span></span> <span data-ttu-id="02f67-106">Le profileur peut aussi éviter ce problème en spécifiant <code>COR_PRF_DISABLE_ALL_NGEN_IMAGES</code> dans son masque d’événement.</span><span class="sxs-lookup"><span data-stu-id="02f67-106">Alternatively, the profiler may avoid this issue by specifying <code>COR_PRF_DISABLE_ALL_NGEN_IMAGES</code> in its event mask.</span></span>|
|<span data-ttu-id="02f67-107">Portée</span><span class="sxs-lookup"><span data-stu-id="02f67-107">Scope</span></span>|<span data-ttu-id="02f67-108">Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="02f67-108">Edge</span></span>|
|<span data-ttu-id="02f67-109">Version</span><span class="sxs-lookup"><span data-stu-id="02f67-109">Version</span></span>|<span data-ttu-id="02f67-110">4.5</span><span class="sxs-lookup"><span data-stu-id="02f67-110">4.5</span></span>|
|<span data-ttu-id="02f67-111">Type</span><span class="sxs-lookup"><span data-stu-id="02f67-111">Type</span></span>|<span data-ttu-id="02f67-112">Runtime</span><span class="sxs-lookup"><span data-stu-id="02f67-112">Runtime</span></span>|
