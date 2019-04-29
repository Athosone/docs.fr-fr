---
title: <namespaceTable>
ms.date: 03/30/2017
ms.assetid: 64801766-01b7-4c65-9ce6-70ad5af67689
ms.openlocfilehash: ee7a0c23adca883af279addf9d1f221bd4056d00
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61772409"
---
# <a name="namespacetable"></a><span data-ttu-id="1b3f6-101">\<namespaceTable></span><span class="sxs-lookup"><span data-stu-id="1b3f6-101">\<namespaceTable></span></span>

<span data-ttu-id="1b3f6-102">Représente une section de configuration qui permet de définir un ensemble d’éléments contenant des mappages espace de noms-préfixe qui peuvent ensuite être utilisés dans des filtres XPath pour le routage.</span><span class="sxs-lookup"><span data-stu-id="1b3f6-102">Represents a configuration section for defining a set of elements that contain namespace to prefix mappings that can then be used in XPath filters for routing.</span></span>

<span data-ttu-id="1b3f6-103">**\<system.serviceModel>** </span><span class="sxs-lookup"><span data-stu-id="1b3f6-103">**\<system.serviceModel>** </span></span>  
<span data-ttu-id="1b3f6-104">&nbsp;&nbsp;**\<routing>** </span><span class="sxs-lookup"><span data-stu-id="1b3f6-104">&nbsp;&nbsp;**\<routing>** </span></span>  
<span data-ttu-id="1b3f6-105">&nbsp;&nbsp;&nbsp;&nbsp;**\<namespaceTable>**</span><span class="sxs-lookup"><span data-stu-id="1b3f6-105">&nbsp;&nbsp;&nbsp;&nbsp;**\<namespaceTable>**</span></span>
  
## <a name="syntax"></a><span data-ttu-id="1b3f6-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="1b3f6-106">Syntax</span></span>  
  
```xml  
<system.serviceModel>
  <routing>
    <namespaceTable>
      <add namespace="String"
           prefix="String" />
    </namespaceTable>
  </routing>
</system.serviceModel>
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="1b3f6-107">Attributs et éléments</span><span class="sxs-lookup"><span data-stu-id="1b3f6-107">Attributes and elements</span></span>

<span data-ttu-id="1b3f6-108">Les sections suivantes décrivent des attributs, des éléments enfants et des éléments parents.</span><span class="sxs-lookup"><span data-stu-id="1b3f6-108">The following sections describe attributes, child elements, and parent elements.</span></span>

### <a name="attributes"></a><span data-ttu-id="1b3f6-109">Attributs</span><span class="sxs-lookup"><span data-stu-id="1b3f6-109">Attributes</span></span>

<span data-ttu-id="1b3f6-110">Aucun.</span><span class="sxs-lookup"><span data-stu-id="1b3f6-110">None</span></span>

### <a name="child-elements"></a><span data-ttu-id="1b3f6-111">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="1b3f6-111">Child elements</span></span>

|     | <span data-ttu-id="1b3f6-112">Description</span><span class="sxs-lookup"><span data-stu-id="1b3f6-112">Description</span></span> |
| --- | ----------- |
| [<span data-ttu-id="1b3f6-113">**\<filter>**</span><span class="sxs-lookup"><span data-stu-id="1b3f6-113">**\<filter>**</span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/filter.md) | <span data-ttu-id="1b3f6-114">Définit un mappage préfixe-espace de noms utilisé pour les expressions XPath.</span><span class="sxs-lookup"><span data-stu-id="1b3f6-114">Defines a namespace prefix mapping used for XPath expressions.</span></span> |

### <a name="parent-elements"></a><span data-ttu-id="1b3f6-115">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="1b3f6-115">Parent elements</span></span>

|     | <span data-ttu-id="1b3f6-116">Description</span><span class="sxs-lookup"><span data-stu-id="1b3f6-116">Description</span></span> |
| --- | ----------- |
| [<span data-ttu-id="1b3f6-117">**\<routing>**</span><span class="sxs-lookup"><span data-stu-id="1b3f6-117">**\<routing>**</span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/routing.md) | <span data-ttu-id="1b3f6-118">Représente une section de configuration pour définir un ensemble de filtres de routage, déterminant le type de Windows Communication Foundation (WCF)<xref:System.ServiceModel.Dispatcher.MessageFilter> à utiliser lors de l’évaluation des messages entrants, ainsi que le routage des tables qui définissent les points de terminaison cible à envoyer des messages lorsqu’un filtre correspond.</span><span class="sxs-lookup"><span data-stu-id="1b3f6-118">Represents a configuration section for defining a set of routing filters, which determine the type of Windows Communication Foundation (WCF)<xref:System.ServiceModel.Dispatcher.MessageFilter> to be used when evaluating incoming messages, as well as routing tables that define the target endpoints to send messages to when a filter matches.</span></span> |

## <a name="see-also"></a><span data-ttu-id="1b3f6-119">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1b3f6-119">See also</span></span>

- <xref:System.ServiceModel.Routing.Configuration.NamespaceElementCollection?displayProperty=nameWithType>
