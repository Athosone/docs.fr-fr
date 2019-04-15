---
ms.openlocfilehash: 3b7309347c643d89a28331c6ef3cac36085a969a
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59234133"
---
### <a name="wpf-windows-are-rendered-without-clipping-when-extending-outside-a-single-monitor"></a><span data-ttu-id="717ad-101">Les fenêtres WPF sont restituées sans découpage lors de l’extension en dehors d’un même écran</span><span class="sxs-lookup"><span data-stu-id="717ad-101">WPF windows are rendered without clipping when extending outside a single monitor</span></span>

|   |   |
|---|---|
|<span data-ttu-id="717ad-102">Détails</span><span class="sxs-lookup"><span data-stu-id="717ad-102">Details</span></span>|<span data-ttu-id="717ad-103">Dans .NET Framework 4.6 s’exécutant sur Windows 8 et ultérieur, la totalité de la fenêtre est restituée sans découpage quand elle s’étend en dehors d’un même écran dans un scénario à plusieurs écrans.</span><span class="sxs-lookup"><span data-stu-id="717ad-103">In the .NET Framework 4.6 running on Windows 8 and above, the entire window is rendered without clipping when it extends outside of single display in a multi-monitor scenario.</span></span> <span data-ttu-id="717ad-104">Ceci diffère des versions précédentes du .NET Framework, qui découpait les fenêtres WPF étendues au-delà d’un même écran.</span><span class="sxs-lookup"><span data-stu-id="717ad-104">This is different from previous versions of the .NET Framework which would clip WPF windows that extended beyond a single display.</span></span>|
|<span data-ttu-id="717ad-105">Suggestion</span><span class="sxs-lookup"><span data-stu-id="717ad-105">Suggestion</span></span>|<span data-ttu-id="717ad-106">Ce comportement (découper ou non) peut être défini explicitement avec l’élément <code>&lt;EnableMultiMonitorDisplayClipping&gt;</code> de <code>&lt;appSettings&gt;</code> dans le fichier de configuration d’une application, ou en définissant la propriété <code>EnableMultiMonitorDisplayClipping</code> au démarrage de l’application.</span><span class="sxs-lookup"><span data-stu-id="717ad-106">This behavior (whether to clip or not) can be explicitly set using the <code>&lt;EnableMultiMonitorDisplayClipping&gt;</code> element in <code>&lt;appSettings&gt;</code> in an application's configuration file, or by setting the <code>EnableMultiMonitorDisplayClipping</code> property at app startup.</span></span>|
|<span data-ttu-id="717ad-107">Portée</span><span class="sxs-lookup"><span data-stu-id="717ad-107">Scope</span></span>|<span data-ttu-id="717ad-108">Mineur</span><span class="sxs-lookup"><span data-stu-id="717ad-108">Minor</span></span>|
|<span data-ttu-id="717ad-109">Version</span><span class="sxs-lookup"><span data-stu-id="717ad-109">Version</span></span>|<span data-ttu-id="717ad-110">4.6</span><span class="sxs-lookup"><span data-stu-id="717ad-110">4.6</span></span>|
|<span data-ttu-id="717ad-111">Type</span><span class="sxs-lookup"><span data-stu-id="717ad-111">Type</span></span>|<span data-ttu-id="717ad-112">Runtime</span><span class="sxs-lookup"><span data-stu-id="717ad-112">Runtime</span></span>|
