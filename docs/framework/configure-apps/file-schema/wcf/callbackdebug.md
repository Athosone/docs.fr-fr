---
title: <callbackDebug>
ms.date: 03/30/2017
ms.assetid: 4073feda-1857-4be4-9947-227afb847ced
ms.openlocfilehash: a1190eb1c015ba07488ff5a5952f2f5f1b10974c
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59152267"
---
# <a name="callbackdebug"></a><span data-ttu-id="13016-101">\<callbackDebug></span><span class="sxs-lookup"><span data-stu-id="13016-101">\<callbackDebug></span></span>
<span data-ttu-id="13016-102">Spécifie le débogage de service pour un objet de rappel Windows Communication Foundation (WCF).</span><span class="sxs-lookup"><span data-stu-id="13016-102">Specifies service debugging for a Windows Communication Foundation (WCF) callback object.</span></span>  
  
 <span data-ttu-id="13016-103">\<system.ServiceModel></span><span class="sxs-lookup"><span data-stu-id="13016-103">\<system.ServiceModel></span></span>  
<span data-ttu-id="13016-104">\<behaviors></span><span class="sxs-lookup"><span data-stu-id="13016-104">\<behaviors></span></span>  
<span data-ttu-id="13016-105">\<endpointBehaviors></span><span class="sxs-lookup"><span data-stu-id="13016-105">\<endpointBehaviors></span></span>  
<span data-ttu-id="13016-106">\<behavior></span><span class="sxs-lookup"><span data-stu-id="13016-106">\<behavior></span></span>  
<span data-ttu-id="13016-107">\<callbackDebug></span><span class="sxs-lookup"><span data-stu-id="13016-107">\<callbackDebug></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="13016-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="13016-108">Syntax</span></span>  
  
```xml  
<callbackDebug includeExceptionDetailInFaults="Boolean" />
```  
  
## <a name="type"></a><span data-ttu-id="13016-109">Type</span><span class="sxs-lookup"><span data-stu-id="13016-109">Type</span></span>  
 `Type`  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="13016-110">Attributs et éléments</span><span class="sxs-lookup"><span data-stu-id="13016-110">Attributes and Elements</span></span>  
 <span data-ttu-id="13016-111">Les sections suivantes décrivent des attributs, des éléments enfants et des éléments parents.</span><span class="sxs-lookup"><span data-stu-id="13016-111">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="13016-112">Attributs</span><span class="sxs-lookup"><span data-stu-id="13016-112">Attributes</span></span>  
  
|<span data-ttu-id="13016-113">Attribut</span><span class="sxs-lookup"><span data-stu-id="13016-113">Attribute</span></span>|<span data-ttu-id="13016-114">Description</span><span class="sxs-lookup"><span data-stu-id="13016-114">Description</span></span>|  
|---------------|-----------------|  
|`includeExceptionDetailInFaults`|<span data-ttu-id="13016-115">Valeur qui spécifie si les objets de rappel client retournent au service des informations sur les exceptions managées dans les erreurs SOAP.</span><span class="sxs-lookup"><span data-stu-id="13016-115">A value that specifies whether client callback objects return managed exception information in SOAP faults back to the service.</span></span><br /><br /> <span data-ttu-id="13016-116">Si vous définissez cet attribut par programme à `true`, vous pouvez activer le retour du flux d'informations sur les exceptions managées dans un objet de rappel client, à des fins de débogage.</span><span class="sxs-lookup"><span data-stu-id="13016-116">If you set this attribute to `true` programmatically, you can enable the flow of managed exception information in a client callback object back to the service for debugging purposes.</span></span> <span data-ttu-id="13016-117">**Attention :**  Le retour des informations sur les exceptions managées aux clients peut entraîner un problème de sécurité.</span><span class="sxs-lookup"><span data-stu-id="13016-117">**Caution:**  Returning managed exception information to clients can be a security risk.</span></span> <span data-ttu-id="13016-118">En effet, les détails de l'exception exposent des informations relatives à l'implémentation d'un service interne qui peuvent être utilisées par des clients non autorisés.</span><span class="sxs-lookup"><span data-stu-id="13016-118">This is because exception details expose information about the internal service implementation that could be used by unauthorized clients.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="13016-119">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="13016-119">Child Elements</span></span>  
 <span data-ttu-id="13016-120">Aucun.</span><span class="sxs-lookup"><span data-stu-id="13016-120">None.</span></span>  
  
### <a name="parent-elements"></a><span data-ttu-id="13016-121">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="13016-121">Parent Elements</span></span>  
  
|<span data-ttu-id="13016-122">Élément</span><span class="sxs-lookup"><span data-stu-id="13016-122">Element</span></span>|<span data-ttu-id="13016-123">Description</span><span class="sxs-lookup"><span data-stu-id="13016-123">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="13016-124">\<behavior></span><span class="sxs-lookup"><span data-stu-id="13016-124">\<behavior></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/behavior-of-endpointbehaviors.md)|<span data-ttu-id="13016-125">Spécifie un comportement de point de terminaison.</span><span class="sxs-lookup"><span data-stu-id="13016-125">Specifies an endpoint behavior.</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="13016-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="13016-126">See also</span></span>

- <xref:System.ServiceModel.Configuration.CallbackDebugElement>
- <xref:System.ServiceModel.Description.CallbackDebugBehavior>
