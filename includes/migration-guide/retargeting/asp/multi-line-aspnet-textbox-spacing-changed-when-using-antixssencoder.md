---
ms.openlocfilehash: e2bca42daebd25667ab2f312d5e59089b986503c
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59234692"
---
### <a name="multi-line-aspnet-textbox-spacing-changed-when-using-antixssencoder"></a><span data-ttu-id="c7d78-101">L’espacement de la zone de texte multiligne ASP.NET a été modifié pour l’utilisation d’AntiXSSEncoder</span><span class="sxs-lookup"><span data-stu-id="c7d78-101">Multi-line ASP.Net TextBox spacing changed when using AntiXSSEncoder</span></span>

|   |   |
|---|---|
|<span data-ttu-id="c7d78-102">Détails</span><span class="sxs-lookup"><span data-stu-id="c7d78-102">Details</span></span>|<span data-ttu-id="c7d78-103">Dans le .NET Framework 4.0, des lignes supplémentaires étaient insérées dans la zone de texte multiligne lors de la publication (postback), quand vous utilisiez <xref:System.Web.Security.AntiXss.AntiXssEncoder?displayProperty=name>.</span><span class="sxs-lookup"><span data-stu-id="c7d78-103">In .NET Framework 4.0, extra lines were inserted between lines of a multi-line text box on postback, if using the <xref:System.Web.Security.AntiXss.AntiXssEncoder?displayProperty=name>.</span></span> <span data-ttu-id="c7d78-104">Dans .NET Framework 4.5, ces sauts de ligne supplémentaires ne sont pas inclus si l’application web cible .NET Framework 4.5.</span><span class="sxs-lookup"><span data-stu-id="c7d78-104">In .NET Framework 4.5, those extra line breaks are not included, but only if the web app is targeting .NET Framework 4.5</span></span>|
|<span data-ttu-id="c7d78-105">Suggestion</span><span class="sxs-lookup"><span data-stu-id="c7d78-105">Suggestion</span></span>|<span data-ttu-id="c7d78-106">Notez que les applications web 4.0 reciblées vers .NET Framework 4.5 peuvent avoir des zones de texte multilignes améliorées qui ne comportent plus de sauts de ligne supplémentaires.</span><span class="sxs-lookup"><span data-stu-id="c7d78-106">Be aware that 4.0 web apps retargeted to .NET Framework 4.5 may have multi-line text boxes improved to no longer insert extra line breaks.</span></span> <span data-ttu-id="c7d78-107">Si vous ne souhaitez pas ce changement, vous pouvez obtenir l’ancien comportement dans .NET Framework 4.5 en ciblant .NET Framework 4.0.</span><span class="sxs-lookup"><span data-stu-id="c7d78-107">If this is not desirable, the app  can have the old behavior when running on .NET Framework 4.5 by targeting the .NET Framework 4.0.</span></span>|
|<span data-ttu-id="c7d78-108">Portée</span><span class="sxs-lookup"><span data-stu-id="c7d78-108">Scope</span></span>|<span data-ttu-id="c7d78-109">Mineur</span><span class="sxs-lookup"><span data-stu-id="c7d78-109">Minor</span></span>|
|<span data-ttu-id="c7d78-110">Version</span><span class="sxs-lookup"><span data-stu-id="c7d78-110">Version</span></span>|<span data-ttu-id="c7d78-111">4.5</span><span class="sxs-lookup"><span data-stu-id="c7d78-111">4.5</span></span>|
|<span data-ttu-id="c7d78-112">Type</span><span class="sxs-lookup"><span data-stu-id="c7d78-112">Type</span></span>|<span data-ttu-id="c7d78-113">Reciblage</span><span class="sxs-lookup"><span data-stu-id="c7d78-113">Retargeting</span></span>|
