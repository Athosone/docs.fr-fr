---
ms.openlocfilehash: 6dc3669433804a4524c18d5a932f9879343ab508
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59235245"
---
### <a name="the-replace-method-in-odata-urls-is-disabled-by-default"></a><span data-ttu-id="ffaa0-101">La méthode Replace est désactivée par défaut dans les URL OData</span><span class="sxs-lookup"><span data-stu-id="ffaa0-101">The Replace method in OData URLs is disabled by default</span></span>

|   |   |
|---|---|
|<span data-ttu-id="ffaa0-102">Détails</span><span class="sxs-lookup"><span data-stu-id="ffaa0-102">Details</span></span>|<span data-ttu-id="ffaa0-103">À compter de la version 4.5 du .NET Framework, la méthode Replace des URL OData est désactivée par défaut.</span><span class="sxs-lookup"><span data-stu-id="ffaa0-103">Beginning in the .NET Framework 4.5, the Replace method in OData URLs is disabled by default.</span></span> <span data-ttu-id="ffaa0-104">Quand la méthode Replace OData est désactivée (ce qui est désormais le cas par défaut), toutes les demandes utilisateur, y compris les fonctions de remplacement (qui sont rares) échouent.</span><span class="sxs-lookup"><span data-stu-id="ffaa0-104">When OData Replace is disabled (now by default), any user requests including replace functions (which are uncommon) will fail.</span></span>|
|<span data-ttu-id="ffaa0-105">Suggestion</span><span class="sxs-lookup"><span data-stu-id="ffaa0-105">Suggestion</span></span>|<span data-ttu-id="ffaa0-106">Si la méthode Replace est nécessaire (ce qui est rare), elle peut être réactivée via les paramètres de configuration (<xref:System.Data.Services.Configuration.DataServicesFeaturesSection.ReplaceFunction?displayProperty=name>).</span><span class="sxs-lookup"><span data-stu-id="ffaa0-106">If the replace method is required (which is uncommon), it can be re-enabled through a config settings (<xref:System.Data.Services.Configuration.DataServicesFeaturesSection.ReplaceFunction?displayProperty=name>).</span></span> <span data-ttu-id="ffaa0-107">Toutefois, l’activation d’une méthode Replace peut créer des failles de sécurité et ne doit donc être utilisée qu’après un examen minutieux.</span><span class="sxs-lookup"><span data-stu-id="ffaa0-107">However, an enabled replace method can open security vulnerabilities and should only be used after careful review.</span></span>|
|<span data-ttu-id="ffaa0-108">Portée</span><span class="sxs-lookup"><span data-stu-id="ffaa0-108">Scope</span></span>|<span data-ttu-id="ffaa0-109">Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="ffaa0-109">Edge</span></span>|
|<span data-ttu-id="ffaa0-110">Version</span><span class="sxs-lookup"><span data-stu-id="ffaa0-110">Version</span></span>|<span data-ttu-id="ffaa0-111">4.5</span><span class="sxs-lookup"><span data-stu-id="ffaa0-111">4.5</span></span>|
|<span data-ttu-id="ffaa0-112">Type</span><span class="sxs-lookup"><span data-stu-id="ffaa0-112">Type</span></span>|<span data-ttu-id="ffaa0-113">Runtime</span><span class="sxs-lookup"><span data-stu-id="ffaa0-113">Runtime</span></span>|
|<span data-ttu-id="ffaa0-114">API affectées</span><span class="sxs-lookup"><span data-stu-id="ffaa0-114">Affected APIs</span></span>|<ul><li><xref:System.Data.Services.DataService%601?displayProperty=nameWithType></li></ul>|
