---
ms.openlocfilehash: ce8e162e11802de1b06bfbc63d5c55de67ef23df
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59803923"
---
### <a name="wcf-msmqsecurehashalgorithm-default-value-is-now-sha256"></a><span data-ttu-id="7e488-101">La valeur par défaut de MsmqSecureHashAlgorithm dans WCF est désormais SHA256</span><span class="sxs-lookup"><span data-stu-id="7e488-101">WCF MsmqSecureHashAlgorithm default value is now SHA256</span></span>

|   |   |
|---|---|
|<span data-ttu-id="7e488-102">Détails</span><span class="sxs-lookup"><span data-stu-id="7e488-102">Details</span></span>|<span data-ttu-id="7e488-103">À compter de .NET Framework 4.7.1, l’algorithme de signature des messages par défaut dans WCF pour les messages Msmq est SHA256.</span><span class="sxs-lookup"><span data-stu-id="7e488-103">Starting with the .NET Framework 4.7.1, the default message signing algorithm in WCF for Msmq messages is SHA256.</span></span> <span data-ttu-id="7e488-104">Dans .NET Framework 4.7 et versions antérieures, l’algorithme de signature des messages par défaut est SHA1.</span><span class="sxs-lookup"><span data-stu-id="7e488-104">In the .NET Framework 4.7 and earlier versions, the default message signing algorithm is SHA1.</span></span>|
|<span data-ttu-id="7e488-105">Suggestion</span><span class="sxs-lookup"><span data-stu-id="7e488-105">Suggestion</span></span>|<span data-ttu-id="7e488-106">Si vous rencontrez des problèmes de compatibilité avec cette modification dans .NET Framework 4.7.1 ou version ultérieure, vous pouvez choisir de ne pas adhérer à la modification en ajoutant la ligne suivante à la section <code>&lt;runtime&gt;</code> de votre fichier app.config :</span><span class="sxs-lookup"><span data-stu-id="7e488-106">If you run into compatibility issues with this change on the .NET Framework 4.7.1 or later, you can opt-out the change by adding the following line to the <code>&lt;runtime&gt;</code>section of your app.config file:</span></span><pre><code class="lang-xml">&lt;configuration&gt;&#13;&#10;&lt;runtime&gt;&#13;&#10;&lt;AppContextSwitchOverrides value=&quot;Switch.System.ServiceModel.UseSha1InMsmqEncryptionAlgorithm=true&quot; /&gt;&#13;&#10;&lt;/runtime&gt;&#13;&#10;&lt;/configuration&gt;&#13;&#10;</code></pre>|
|<span data-ttu-id="7e488-107">Portée</span><span class="sxs-lookup"><span data-stu-id="7e488-107">Scope</span></span>|<span data-ttu-id="7e488-108">Mineur</span><span class="sxs-lookup"><span data-stu-id="7e488-108">Minor</span></span>|
|<span data-ttu-id="7e488-109">Version</span><span class="sxs-lookup"><span data-stu-id="7e488-109">Version</span></span>|<span data-ttu-id="7e488-110">4.7.1</span><span class="sxs-lookup"><span data-stu-id="7e488-110">4.7.1</span></span>|
|<span data-ttu-id="7e488-111">Type</span><span class="sxs-lookup"><span data-stu-id="7e488-111">Type</span></span>|<span data-ttu-id="7e488-112">Runtime</span><span class="sxs-lookup"><span data-stu-id="7e488-112">Runtime</span></span>|
