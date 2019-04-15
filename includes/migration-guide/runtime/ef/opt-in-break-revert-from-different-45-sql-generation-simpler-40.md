---
ms.openlocfilehash: e5d81d791e1a2f1a2dbdafc787dec1227423883d
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59236649"
---
### <a name="opt-in-break-to-revert-from-different-45-sql-generation-to-simpler-40-sql-generation"></a><span data-ttu-id="b6a9e-101">Rupture d’adhésion pour rétrograder de la génération 4.5 de SQL à la génération 4.0 de SQL plus simple</span><span class="sxs-lookup"><span data-stu-id="b6a9e-101">Opt-in break to revert from different 4.5 SQL generation to simpler 4.0 SQL generation</span></span>

|   |   |
|---|---|
|<span data-ttu-id="b6a9e-102">Détails</span><span class="sxs-lookup"><span data-stu-id="b6a9e-102">Details</span></span>|<span data-ttu-id="b6a9e-103">Les requêtes, qui produisent des instructions JOIN et contiennent un appel à une opération de limitation sans préalablement utiliser OrderBy, produisent à présent un langage SQL plus simple.</span><span class="sxs-lookup"><span data-stu-id="b6a9e-103">Queries that produce JOIN statements and contain a call to a limiting operation without first using OrderBy now produce simpler SQL.</span></span> <span data-ttu-id="b6a9e-104">Après la mise à niveau vers .NET Framework 4.5, ces requêtes produisaient un langage SQL plus compliqué que les versions antérieures.</span><span class="sxs-lookup"><span data-stu-id="b6a9e-104">After upgrading to .NET Framework 4.5, these queries produced more complicated SQL than previous versions.</span></span>|
|<span data-ttu-id="b6a9e-105">Suggestion</span><span class="sxs-lookup"><span data-stu-id="b6a9e-105">Suggestion</span></span>|<span data-ttu-id="b6a9e-106">Cette fonctionnalité est désactivée par défaut.</span><span class="sxs-lookup"><span data-stu-id="b6a9e-106">This feature is disabled by default.</span></span> <span data-ttu-id="b6a9e-107">Si Entity Framework génère des instructions JOIN supplémentaires qui entraînent une dégradation des performances, vous pouvez activer cette fonctionnalité en ajoutant l’entrée suivante à la section <code>&lt;appSettings&gt;</code> du fichier de configuration de l’application (app.config) :</span><span class="sxs-lookup"><span data-stu-id="b6a9e-107">If Entity Framework generates extra JOIN statements that cause performance degradation, you can enable this feature by adding the following entry to the <code>&lt;appSettings&gt;</code> section of the application configuration (app.config) file:</span></span><pre><code class="lang-xml">&lt;add key=&quot;EntityFramework_SimplifyLimitOperations&quot; value=&quot;true&quot; /&gt;&#13;&#10;</code></pre>|
|<span data-ttu-id="b6a9e-108">Portée</span><span class="sxs-lookup"><span data-stu-id="b6a9e-108">Scope</span></span>|<span data-ttu-id="b6a9e-109">Transparent</span><span class="sxs-lookup"><span data-stu-id="b6a9e-109">Transparent</span></span>|
|<span data-ttu-id="b6a9e-110">Version</span><span class="sxs-lookup"><span data-stu-id="b6a9e-110">Version</span></span>|<span data-ttu-id="b6a9e-111">4.5.2</span><span class="sxs-lookup"><span data-stu-id="b6a9e-111">4.5.2</span></span>|
|<span data-ttu-id="b6a9e-112">Type</span><span class="sxs-lookup"><span data-stu-id="b6a9e-112">Type</span></span>|<span data-ttu-id="b6a9e-113">Runtime</span><span class="sxs-lookup"><span data-stu-id="b6a9e-113">Runtime</span></span>|
