---
title: 3552 - MaxPendingMessagesPerChannelExceeded
ms.date: 03/30/2017
ms.assetid: fc8309d9-eb3a-4636-a6f0-dd0018c1361d
ms.openlocfilehash: a163ed216cbdfbf2b9d77d25979733d6bdb121d3
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61945936"
---
# <a name="3552---maxpendingmessagesperchannelexceeded"></a><span data-ttu-id="1687e-102">3552 - MaxPendingMessagesPerChannelExceeded</span><span class="sxs-lookup"><span data-stu-id="1687e-102">3552 - MaxPendingMessagesPerChannelExceeded</span></span>
## <a name="properties"></a><span data-ttu-id="1687e-103">Properties</span><span class="sxs-lookup"><span data-stu-id="1687e-103">Properties</span></span>  
  
|||  
|-|-|  
|<span data-ttu-id="1687e-104">Id</span><span class="sxs-lookup"><span data-stu-id="1687e-104">ID</span></span>|<span data-ttu-id="1687e-105">3552</span><span class="sxs-lookup"><span data-stu-id="1687e-105">3552</span></span>|  
|<span data-ttu-id="1687e-106">Mots clés</span><span class="sxs-lookup"><span data-stu-id="1687e-106">Keywords</span></span>|<span data-ttu-id="1687e-107">Quota, WFServices</span><span class="sxs-lookup"><span data-stu-id="1687e-107">Quota, WFServices</span></span>|  
|<span data-ttu-id="1687e-108">Niveau</span><span class="sxs-lookup"><span data-stu-id="1687e-108">Level</span></span>|<span data-ttu-id="1687e-109">Warning</span><span class="sxs-lookup"><span data-stu-id="1687e-109">Warning</span></span>|  
|<span data-ttu-id="1687e-110">Canal</span><span class="sxs-lookup"><span data-stu-id="1687e-110">Channel</span></span>|<span data-ttu-id="1687e-111">Microsoft-Windows-Application Server-Applications/Analyse</span><span class="sxs-lookup"><span data-stu-id="1687e-111">Microsoft-Windows-Application Server-Applications/Analytic</span></span>|  
  
## <a name="description"></a><span data-ttu-id="1687e-112">Description</span><span class="sxs-lookup"><span data-stu-id="1687e-112">Description</span></span>  
 <span data-ttu-id="1687e-113">Indique que la limitation « MaxPendingMessagesPerChannel » a été atteinte.</span><span class="sxs-lookup"><span data-stu-id="1687e-113">Indicates the throttle 'MaxPendingMessagesPerChannel' limit was hit.</span></span>  
  
## <a name="message"></a><span data-ttu-id="1687e-114">Message</span><span class="sxs-lookup"><span data-stu-id="1687e-114">Message</span></span>  
 <span data-ttu-id="1687e-115">La limitation « maxpendingmessagesperchannel » de '%1' a été atteint.</span><span class="sxs-lookup"><span data-stu-id="1687e-115">The throttle 'MaxPendingMessagesPerChannel' limit of  '%1' was hit.</span></span> <span data-ttu-id="1687e-116">Pour accroître cette limite, modifiez la propriété MaxPendingMessagesPerChannel sur BufferedReceiveServiceBehavior.</span><span class="sxs-lookup"><span data-stu-id="1687e-116">To increase this limit, adjust the MaxPendingMessagesPerChannel property on BufferedReceiveServiceBehavior.</span></span>  
  
## <a name="details"></a><span data-ttu-id="1687e-117">Détails</span><span class="sxs-lookup"><span data-stu-id="1687e-117">Details</span></span>  
  
|<span data-ttu-id="1687e-118">Nom d'élément de données</span><span class="sxs-lookup"><span data-stu-id="1687e-118">Data Item Name</span></span>|<span data-ttu-id="1687e-119">Type d'élément de données</span><span class="sxs-lookup"><span data-stu-id="1687e-119">Data Item Type</span></span>|<span data-ttu-id="1687e-120">Description</span><span class="sxs-lookup"><span data-stu-id="1687e-120">Description</span></span>|  
|--------------------|--------------------|-----------------|  
|<span data-ttu-id="1687e-121">Limitation</span><span class="sxs-lookup"><span data-stu-id="1687e-121">Limit</span></span>|<span data-ttu-id="1687e-122">xs:string</span><span class="sxs-lookup"><span data-stu-id="1687e-122">xs:string</span></span>|<span data-ttu-id="1687e-123">La limite de MaxPendingMessagesPerChannel.</span><span class="sxs-lookup"><span data-stu-id="1687e-123">The limit of the MaxPendingMessagesPerChannel throttle.</span></span>|  
|<span data-ttu-id="1687e-124">AppDomain</span><span class="sxs-lookup"><span data-stu-id="1687e-124">AppDomain</span></span>|<span data-ttu-id="1687e-125">xs:string</span><span class="sxs-lookup"><span data-stu-id="1687e-125">xs:string</span></span>|<span data-ttu-id="1687e-126">Chaîne retournée par AppDomain.CurrentDomain.FriendlyName.</span><span class="sxs-lookup"><span data-stu-id="1687e-126">The string returned by AppDomain.CurrentDomain.FriendlyName.</span></span>|
