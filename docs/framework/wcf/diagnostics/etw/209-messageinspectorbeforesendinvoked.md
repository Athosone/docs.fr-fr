---
title: 209 - MessageInspectorBeforeSendInvoked
ms.date: 03/30/2017
ms.assetid: 7d710875-fb77-4463-978b-bc86d59d84cd
ms.openlocfilehash: 24184c24b9affdf3a56d7968c02cf5354d690749
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61781877"
---
# <a name="209---messageinspectorbeforesendinvoked"></a><span data-ttu-id="00d7e-102">209 - MessageInspectorBeforeSendInvoked</span><span class="sxs-lookup"><span data-stu-id="00d7e-102">209 - MessageInspectorBeforeSendInvoked</span></span>
## <a name="properties"></a><span data-ttu-id="00d7e-103">Properties</span><span class="sxs-lookup"><span data-stu-id="00d7e-103">Properties</span></span>  
  
|||  
|-|-|  
|<span data-ttu-id="00d7e-104">Id</span><span class="sxs-lookup"><span data-stu-id="00d7e-104">ID</span></span>|<span data-ttu-id="00d7e-105">209</span><span class="sxs-lookup"><span data-stu-id="00d7e-105">209</span></span>|  
|<span data-ttu-id="00d7e-106">Mots clés</span><span class="sxs-lookup"><span data-stu-id="00d7e-106">Keywords</span></span>|<span data-ttu-id="00d7e-107">Dépannage, ServiceModel</span><span class="sxs-lookup"><span data-stu-id="00d7e-107">Troubleshooting, ServiceModel</span></span>|  
|<span data-ttu-id="00d7e-108">Niveau</span><span class="sxs-lookup"><span data-stu-id="00d7e-108">Level</span></span>|<span data-ttu-id="00d7e-109">Information</span><span class="sxs-lookup"><span data-stu-id="00d7e-109">Information</span></span>|  
|<span data-ttu-id="00d7e-110">Canal</span><span class="sxs-lookup"><span data-stu-id="00d7e-110">Channel</span></span>|<span data-ttu-id="00d7e-111">Microsoft-Windows-Application Server-Applications/Analyse</span><span class="sxs-lookup"><span data-stu-id="00d7e-111">Microsoft-Windows-Application Server-Applications/Analytic</span></span>|  
  
## <a name="description"></a><span data-ttu-id="00d7e-112">Description</span><span class="sxs-lookup"><span data-stu-id="00d7e-112">Description</span></span>  
 <span data-ttu-id="00d7e-113">Cet événement est émis après que le modèle de service a appelé la méthode `BeforeSend` sur un inspecteur de message.</span><span class="sxs-lookup"><span data-stu-id="00d7e-113">This event is emitted after the Service Model has invoked the `BeforeSend` method on a message inspector.</span></span>  
  
## <a name="message"></a><span data-ttu-id="00d7e-114">Message</span><span class="sxs-lookup"><span data-stu-id="00d7e-114">Message</span></span>  
 <span data-ttu-id="00d7e-115">Le répartiteur a appelé 'BeforeSendRequest' sur un MessageInspector de type '%1'.</span><span class="sxs-lookup"><span data-stu-id="00d7e-115">The Dispatcher invoked 'BeforeSendRequest' on a MessageInspector of type '%1'.</span></span>  
  
## <a name="details"></a><span data-ttu-id="00d7e-116">Détails</span><span class="sxs-lookup"><span data-stu-id="00d7e-116">Details</span></span>  
  
|<span data-ttu-id="00d7e-117">Nom d'élément de données</span><span class="sxs-lookup"><span data-stu-id="00d7e-117">Data Item Name</span></span>|<span data-ttu-id="00d7e-118">Type d'élément de données</span><span class="sxs-lookup"><span data-stu-id="00d7e-118">Data Item Type</span></span>|<span data-ttu-id="00d7e-119">Description</span><span class="sxs-lookup"><span data-stu-id="00d7e-119">Description</span></span>|  
|--------------------|--------------------|-----------------|  
|<span data-ttu-id="00d7e-120">TypeName</span><span class="sxs-lookup"><span data-stu-id="00d7e-120">TypeName</span></span>|`xs:string`|<span data-ttu-id="00d7e-121">CLR FullName du type de `MessageInspector` appelé.</span><span class="sxs-lookup"><span data-stu-id="00d7e-121">The CLR FullName of the type of the invoked `MessageInspector`.</span></span>|  
|<span data-ttu-id="00d7e-122">HostReference</span><span class="sxs-lookup"><span data-stu-id="00d7e-122">HostReference</span></span>|`xs:string`|<span data-ttu-id="00d7e-123">Pour les services hébergés par le Web, ce champ identifie de manière unique le service dans la hiérarchie Web.</span><span class="sxs-lookup"><span data-stu-id="00d7e-123">For Web-hosted services, this field uniquely identifies the service in the Web hierarchy.</span></span> <span data-ttu-id="00d7e-124">Son format est défini en tant que « chemin d’accès virtuel de Site Web nom Application&#124;chemin d’accès virtuel du Service&#124;ServiceName'.</span><span class="sxs-lookup"><span data-stu-id="00d7e-124">Its format is defined as 'Web Site Name Application Virtual Path&#124;Service Virtual Path&#124;ServiceName'.</span></span> <span data-ttu-id="00d7e-125">Exemple : « Default Web Site/CalculatorApplication&#124;/CalculatorService.svc&#124;CalculatorService ».</span><span class="sxs-lookup"><span data-stu-id="00d7e-125">Example: 'Default Web Site/CalculatorApplication&#124;/CalculatorService.svc&#124;CalculatorService'.</span></span>|  
|<span data-ttu-id="00d7e-126">AppDomain</span><span class="sxs-lookup"><span data-stu-id="00d7e-126">AppDomain</span></span>|`xs:string`|<span data-ttu-id="00d7e-127">Chaîne retournée par AppDomain.CurrentDomain.FriendlyName.</span><span class="sxs-lookup"><span data-stu-id="00d7e-127">The string returned by AppDomain.CurrentDomain.FriendlyName.</span></span>|
