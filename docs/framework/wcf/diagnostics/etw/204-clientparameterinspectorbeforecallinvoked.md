---
title: 204 - ClientParameterInspectorBeforeCallInvoked
ms.date: 03/30/2017
ms.assetid: 8253555a-9002-4565-8ede-33d7a33a895f
ms.openlocfilehash: eb060cfa79b75452deae67705126a24b7ca9ffef
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61782036"
---
# <a name="204---clientparameterinspectorbeforecallinvoked"></a><span data-ttu-id="4e6c0-102">204 - ClientParameterInspectorBeforeCallInvoked</span><span class="sxs-lookup"><span data-stu-id="4e6c0-102">204 - ClientParameterInspectorBeforeCallInvoked</span></span>
## <a name="properties"></a><span data-ttu-id="4e6c0-103">Properties</span><span class="sxs-lookup"><span data-stu-id="4e6c0-103">Properties</span></span>  
  
|||  
|-|-|  
|<span data-ttu-id="4e6c0-104">Id</span><span class="sxs-lookup"><span data-stu-id="4e6c0-104">ID</span></span>|<span data-ttu-id="4e6c0-105">204</span><span class="sxs-lookup"><span data-stu-id="4e6c0-105">204</span></span>|  
|<span data-ttu-id="4e6c0-106">Mots clés</span><span class="sxs-lookup"><span data-stu-id="4e6c0-106">Keywords</span></span>|<span data-ttu-id="4e6c0-107">Dépannage, ServiceModel</span><span class="sxs-lookup"><span data-stu-id="4e6c0-107">Troubleshooting, ServiceModel</span></span>|  
|<span data-ttu-id="4e6c0-108">Niveau</span><span class="sxs-lookup"><span data-stu-id="4e6c0-108">Level</span></span>|<span data-ttu-id="4e6c0-109">Information</span><span class="sxs-lookup"><span data-stu-id="4e6c0-109">Information</span></span>|  
|<span data-ttu-id="4e6c0-110">Canal</span><span class="sxs-lookup"><span data-stu-id="4e6c0-110">Channel</span></span>|<span data-ttu-id="4e6c0-111">Microsoft-Windows-Application Server-Applications/Analyse</span><span class="sxs-lookup"><span data-stu-id="4e6c0-111">Microsoft-Windows-Application Server-Applications/Analytic</span></span>|  
  
## <a name="description"></a><span data-ttu-id="4e6c0-112">Description</span><span class="sxs-lookup"><span data-stu-id="4e6c0-112">Description</span></span>  
 <span data-ttu-id="4e6c0-113">Cet événement est émis après que le modèle de service a appelé la méthode `BeforeCall` sur un inspecteur de paramètre client.</span><span class="sxs-lookup"><span data-stu-id="4e6c0-113">This event is emitted after the Service Model has invoked the `BeforeCall` method on a client parameter inspector.</span></span>  
  
## <a name="message"></a><span data-ttu-id="4e6c0-114">Message</span><span class="sxs-lookup"><span data-stu-id="4e6c0-114">Message</span></span>  
 <span data-ttu-id="4e6c0-115">Le répartiteur a appelé 'BeforeCall' sur un ClientParameterInspector de type '%1.'</span><span class="sxs-lookup"><span data-stu-id="4e6c0-115">The Dispatcher invoked 'BeforeCall' on a ClientParameterInspector of type '%1'.</span></span>  
  
## <a name="details"></a><span data-ttu-id="4e6c0-116">Détails</span><span class="sxs-lookup"><span data-stu-id="4e6c0-116">Details</span></span>  
  
|<span data-ttu-id="4e6c0-117">Nom d'élément de données</span><span class="sxs-lookup"><span data-stu-id="4e6c0-117">Data Item Name</span></span>|<span data-ttu-id="4e6c0-118">Type d'élément de données</span><span class="sxs-lookup"><span data-stu-id="4e6c0-118">Data Item Type</span></span>|<span data-ttu-id="4e6c0-119">Description</span><span class="sxs-lookup"><span data-stu-id="4e6c0-119">Description</span></span>|  
|--------------------|--------------------|-----------------|  
|<span data-ttu-id="4e6c0-120">TypeName</span><span class="sxs-lookup"><span data-stu-id="4e6c0-120">TypeName</span></span>|`xs:string`|<span data-ttu-id="4e6c0-121">CLR FullName du type d'inspecteur appelé.</span><span class="sxs-lookup"><span data-stu-id="4e6c0-121">The CLR FullName of the invoked inspector's type.</span></span>|  
|<span data-ttu-id="4e6c0-122">HostReference</span><span class="sxs-lookup"><span data-stu-id="4e6c0-122">HostReference</span></span>|`xs:string`|<span data-ttu-id="4e6c0-123">Pour les services hébergés par le Web, ce champ identifie de manière unique le service dans la hiérarchie Web.</span><span class="sxs-lookup"><span data-stu-id="4e6c0-123">For Web-hosted services, this field uniquely identifies the service in the Web hierarchy.</span></span> <span data-ttu-id="4e6c0-124">Son format est défini en tant que « chemin d’accès virtuel de Site Web nom Application&#124;chemin d’accès virtuel du Service&#124;ServiceName'.</span><span class="sxs-lookup"><span data-stu-id="4e6c0-124">Its format is defined as 'Web Site Name Application Virtual Path&#124;Service Virtual Path&#124;ServiceName'.</span></span> <span data-ttu-id="4e6c0-125">Exemple : « Default Web Site/CalculatorApplication&#124;/CalculatorService.svc&#124;CalculatorService ».</span><span class="sxs-lookup"><span data-stu-id="4e6c0-125">Example: 'Default Web Site/CalculatorApplication&#124;/CalculatorService.svc&#124;CalculatorService'.</span></span>|  
|<span data-ttu-id="4e6c0-126">AppDomain</span><span class="sxs-lookup"><span data-stu-id="4e6c0-126">AppDomain</span></span>|`xs:string`|<span data-ttu-id="4e6c0-127">Chaîne retournée par AppDomain.CurrentDomain.FriendlyName.</span><span class="sxs-lookup"><span data-stu-id="4e6c0-127">The string returned by AppDomain.CurrentDomain.FriendlyName.</span></span>|
