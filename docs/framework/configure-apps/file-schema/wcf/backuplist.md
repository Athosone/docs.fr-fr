---
title: <backupList>
ms.date: 03/30/2017
ms.assetid: a3d9d1f9-4a53-45e9-a880-86c8bee0b833
ms.openlocfilehash: b0a6c604b5741c1355c35fca510cd10544dab9f3
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61704425"
---
# <a name="backuplist"></a><span data-ttu-id="63577-101">\<backupList></span><span class="sxs-lookup"><span data-stu-id="63577-101">\<backupList></span></span>
<span data-ttu-id="63577-102">Représente une section de configuration pour définir une liste de sauvegarde qui énumère un ensemble de points de terminaison que vous souhaitez que le Service de routage à utiliser au cas où le point de terminaison principal n’est pas accessible.</span><span class="sxs-lookup"><span data-stu-id="63577-102">Represents a configuration section for defining a backup list that enumerates a set of endpoints that you would like the Routing Service to use in case the primary endpoint can't be reached.</span></span> <span data-ttu-id="63577-103">Si le premier point de terminaison de la liste est inactif, le service de routage bascule automatiquement sur le suivant dans la liste.</span><span class="sxs-lookup"><span data-stu-id="63577-103">If the first endpoint in the list is down, the Routing Service will automatically fail-over to the next one in the list.</span></span>  <span data-ttu-id="63577-104">Vous disposez ainsi d’une méthode rapide pour renforcer la fiabilité de votre application sans avoir à apprendre à votre application cliente à gérer des modèles complexes ou à rechercher l’emplacement de tous vos services déployés.</span><span class="sxs-lookup"><span data-stu-id="63577-104">This gives you a quick way to add reliability to your application without having to teach your client application how to handle complex patterns or where all of your services are deployed.</span></span>  
  
 <span data-ttu-id="63577-105">\<system.serviceModel></span><span class="sxs-lookup"><span data-stu-id="63577-105">\<system.serviceModel></span></span>  
<span data-ttu-id="63577-106">\<routing></span><span class="sxs-lookup"><span data-stu-id="63577-106">\<routing></span></span>  
<span data-ttu-id="63577-107">\<backupLists></span><span class="sxs-lookup"><span data-stu-id="63577-107">\<backupLists></span></span>  
<span data-ttu-id="63577-108">\<backupList></span><span class="sxs-lookup"><span data-stu-id="63577-108">\<backupList></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="63577-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="63577-109">Syntax</span></span>  
  
```xml  
<routing>
  <backupLists>
    <backupList name="String">
      <add endpointName="String" />
    </backupList>
  </backupLists>
</routing>
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="63577-110">Attributs et éléments</span><span class="sxs-lookup"><span data-stu-id="63577-110">Attributes and Elements</span></span>  
 <span data-ttu-id="63577-111">Les sections suivantes décrivent des attributs, des éléments enfants et des éléments parents.</span><span class="sxs-lookup"><span data-stu-id="63577-111">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="63577-112">Attributs</span><span class="sxs-lookup"><span data-stu-id="63577-112">Attributes</span></span>  
  
|<span data-ttu-id="63577-113">Attribut</span><span class="sxs-lookup"><span data-stu-id="63577-113">Attribute</span></span>|<span data-ttu-id="63577-114">Description</span><span class="sxs-lookup"><span data-stu-id="63577-114">Description</span></span>|  
|---------------|-----------------|  
|<span data-ttu-id="63577-115">name</span><span class="sxs-lookup"><span data-stu-id="63577-115">name</span></span>|<span data-ttu-id="63577-116">Chaîne qui spécifie le nom permettant d'identifier la liste de points de terminaison.</span><span class="sxs-lookup"><span data-stu-id="63577-116">A string that specifies the name used to identify this endpoint list.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="63577-117">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="63577-117">Child Elements</span></span>  
  
|<span data-ttu-id="63577-118">Élément</span><span class="sxs-lookup"><span data-stu-id="63577-118">Element</span></span>|<span data-ttu-id="63577-119">Description</span><span class="sxs-lookup"><span data-stu-id="63577-119">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="63577-120">\<filter></span><span class="sxs-lookup"><span data-stu-id="63577-120">\<filter></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/filter.md)||  
  
### <a name="parent-elements"></a><span data-ttu-id="63577-121">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="63577-121">Parent Elements</span></span>  
  
|<span data-ttu-id="63577-122">Élément</span><span class="sxs-lookup"><span data-stu-id="63577-122">Element</span></span>|<span data-ttu-id="63577-123">Description</span><span class="sxs-lookup"><span data-stu-id="63577-123">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="63577-124">\<routing></span><span class="sxs-lookup"><span data-stu-id="63577-124">\<routing></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/routing.md)|<span data-ttu-id="63577-125">Liste de points de terminaison de sauvegarde.</span><span class="sxs-lookup"><span data-stu-id="63577-125">A list of backup endpoints.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="63577-126">Notes</span><span class="sxs-lookup"><span data-stu-id="63577-126">Remarks</span></span>  
 <span data-ttu-id="63577-127">Cette section contient une collection ordonnée de points de terminaison auxquels un message sera transmis si une exception de communication se produit lors de l'envoi au point de terminaison primaire.</span><span class="sxs-lookup"><span data-stu-id="63577-127">This section contains an ordered collection of endpoints that a message will be transmitted to in the event of a communications exception when sending to the primary endpoint.</span></span>  
  
 <span data-ttu-id="63577-128">Si un envoi au point de terminaison primaire répertorié dans le `endpointName` attribut de [ \<Ajouter >](../../../../../docs/framework/configure-apps/file-schema/wcf/add-of-entries.md) échoue avec une exception de communication, le Service de routage essaiera d’envoyer le message au premier point de terminaison dans ce section de configuration.</span><span class="sxs-lookup"><span data-stu-id="63577-128">If a send to the primary endpoint listed in the `endpointName` attribute of [\<add>](../../../../../docs/framework/configure-apps/file-schema/wcf/add-of-entries.md) fails with a communications exception, the Routing Service will attempt to send the message to the first endpoint in this configuration section.</span></span> <span data-ttu-id="63577-129">Si l’opération échoue également avec une exception de communication, le service de routage essaie d’envoyer le message au point de terminaison suivant contenu dans cette section jusqu’à ce que la tentative d’envoi aboutisse, retourne une erreur autre qu’une exception de communication, ou que tous les points de terminaison de la collection retournent une erreur.</span><span class="sxs-lookup"><span data-stu-id="63577-129">If this also fails with a communications exception, the Routing Service will attempt to send the message to the next message contained in this section until the send attempt succeeds, returns a failure other than a communication exception, or all endpoints in the collection have returned a failure.</span></span>  
  
 <span data-ttu-id="63577-130">Dans l’exemple suivant, si un envoi au point de terminaison primaire appelé « Destination » retourne une exception de communication, le service essaiera d’envoyer le message à « alternateServiceQueue ».</span><span class="sxs-lookup"><span data-stu-id="63577-130">In the following example, if a send to the primary endpoint named "Destination" returns a communication exception, the service will attempt to send the message to the "alternateServiceQueue".</span></span> <span data-ttu-id="63577-131">Si cette tentative retourne également une exception de communication, le service de routage essaiera d’envoyer le message au point de terminaison suivant dans la collection.</span><span class="sxs-lookup"><span data-stu-id="63577-131">If this attempt also returns a communication exception, the Routing Service will attempt to send the message to the next endpoint in the collection.</span></span>  
  
```xml  
<filterTables>
  <filterTable name="filterTable1">
    <add filterName="MatchAllFilter1"
         endpointName="Destination"
         backupList="backupEndpointList" />
  </filterTable>
</filterTables>
<backupLists>
  <backupList name="backupEndpointList">
    <add endpointName="backupServiceQueue" />
    <add endpointName="alternateServiceQueue" />
  </backupList>
</backupLists>
```  
  
## <a name="see-also"></a><span data-ttu-id="63577-132">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="63577-132">See also</span></span>

- <xref:System.ServiceModel.Routing.Configuration.BackupEndpointCollection?displayProperty=nameWithType>
