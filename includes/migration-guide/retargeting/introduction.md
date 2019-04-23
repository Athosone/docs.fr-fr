---
ms.openlocfilehash: d4f22aa41eb7aeffd655d980cb8418649462273e
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61757758"
---
## <a name="introduction"></a><span data-ttu-id="df66d-101">Introduction</span><span class="sxs-lookup"><span data-stu-id="df66d-101">Introduction</span></span>
<span data-ttu-id="df66d-102">Les changements de reciblage affectent les applications qui sont recompilées pour cibler un autre .NET Framework.</span><span class="sxs-lookup"><span data-stu-id="df66d-102">Retargeting changes affect apps that are recompiled to target a different .NET Framework.</span></span> <span data-ttu-id="df66d-103">Elles comprennent :</span><span class="sxs-lookup"><span data-stu-id="df66d-103">They include:</span></span>

* <span data-ttu-id="df66d-104">Modifications de l'environnement au moment du design.</span><span class="sxs-lookup"><span data-stu-id="df66d-104">Changes in the design-time environment.</span></span> <span data-ttu-id="df66d-105">Par exemple, les outils de génération peuvent émettre des avertissements, ce qu'ils ne faisaient pas auparavant.</span><span class="sxs-lookup"><span data-stu-id="df66d-105">For example, build tools may emit warnings when previously they did not.</span></span>

* <span data-ttu-id="df66d-106">Modifications de l'environnement d'exécution.</span><span class="sxs-lookup"><span data-stu-id="df66d-106">Changes in the runtime environment.</span></span> <span data-ttu-id="df66d-107">Ces changements affectent uniquement les applications qui ciblent particulièrement le .NET Framework reciblé.</span><span class="sxs-lookup"><span data-stu-id="df66d-107">These affect only apps that specifically target the retargeted .NET Framework.</span></span> <span data-ttu-id="df66d-108">Les applications qui ciblent des versions antérieures de .NET Framework se comportent comme elles le faisaient dans ces versions.</span><span class="sxs-lookup"><span data-stu-id="df66d-108">Apps that target previous versions of the .NET Framework behave as they did when running under those versions.</span></span>

<span data-ttu-id="df66d-109">Dans les rubriques qui décrivent les changements de reciblage, nous avons classé les éléments individuels en fonction de leur impact, comme suit :</span><span class="sxs-lookup"><span data-stu-id="df66d-109">In the topics that describe retargeting changes, we have classified individual items by their expected impact, as follows:</span></span>

<span data-ttu-id="df66d-110">**Majeur** Il s’agit d’un changement important qui affecte un grand nombre d'applications ou qui nécessite de modifier significativement le code.</span><span class="sxs-lookup"><span data-stu-id="df66d-110">**Major** This is a significant change that affects a large number of apps or that requires substantial modification of code.</span></span>

<span data-ttu-id="df66d-111">**Mineur** Il s’agit d’un changement qui affecte un petit nombre d’applications ou qui nécessite peu de modifications du code.</span><span class="sxs-lookup"><span data-stu-id="df66d-111">**Minor** This is a change that affects a small number of apps or that requires minor modification of code.</span></span>

<span data-ttu-id="df66d-112">**Cas particulier** Il s’agit d’un changement qui affecte des applications dans des scénarios très spécifiques qui ne sont pas courants.</span><span class="sxs-lookup"><span data-stu-id="df66d-112">**Edge case** This is a change that affects apps under very specific scenarios that are not common.</span></span>

<span data-ttu-id="df66d-113">**Transparent** Il s’agit d’un changement qui n’a pas d’effet visible pour le développeur ou l’utilisateur de l’application.</span><span class="sxs-lookup"><span data-stu-id="df66d-113">**Transparent** This is a change that has no noticeable effect on the app's developer or user.</span></span> <span data-ttu-id="df66d-114">L'application n'a pas besoin d'être modifiée en raison de cette modification.</span><span class="sxs-lookup"><span data-stu-id="df66d-114">The app should not require modification because of this change.</span></span>
