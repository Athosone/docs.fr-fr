---
title: <metadata>
ms.date: 03/30/2017
ms.assetid: d09653eb-e355-4c73-b87b-28f93d56480d
ms.openlocfilehash: c0c9848d073c799e1f97dd79b375848dfab71e99
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61763904"
---
# <a name="metadata"></a><span data-ttu-id="239a0-101">\<metadata></span><span class="sxs-lookup"><span data-stu-id="239a0-101">\<metadata></span></span>
<span data-ttu-id="239a0-102">Indique la façon dont les métadonnées peuvent être traitées.</span><span class="sxs-lookup"><span data-stu-id="239a0-102">Specifies how service metadata can be processed.</span></span>  
  
 <span data-ttu-id="239a0-103">\<system.ServiceModel></span><span class="sxs-lookup"><span data-stu-id="239a0-103">\<system.ServiceModel></span></span>  
<span data-ttu-id="239a0-104">\<client></span><span class="sxs-lookup"><span data-stu-id="239a0-104">\<client></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="239a0-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="239a0-105">Syntax</span></span>  
  
```xml  
<system.serviceModel>
  <client>
    <metadata>
      <policyImporters>
        <policyImporter type="string" />
      </policyImporters>
      <wsdlImporters>
        <wsdlImporter type="string" />
      </wsdlImporters>
    </metadata>
  </client>
</system.serviceModel>
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="239a0-106">Attributs et éléments</span><span class="sxs-lookup"><span data-stu-id="239a0-106">Attributes and Elements</span></span>  
 <span data-ttu-id="239a0-107">Les sections suivantes décrivent des attributs, des éléments enfants et des éléments parents.</span><span class="sxs-lookup"><span data-stu-id="239a0-107">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="239a0-108">Attributs</span><span class="sxs-lookup"><span data-stu-id="239a0-108">Attributes</span></span>  
 <span data-ttu-id="239a0-109">Aucun.</span><span class="sxs-lookup"><span data-stu-id="239a0-109">None.</span></span>  
  
### <a name="child-elements"></a><span data-ttu-id="239a0-110">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="239a0-110">Child Elements</span></span>  
  
|<span data-ttu-id="239a0-111">Élément</span><span class="sxs-lookup"><span data-stu-id="239a0-111">Element</span></span>|<span data-ttu-id="239a0-112">Description</span><span class="sxs-lookup"><span data-stu-id="239a0-112">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="239a0-113">\<policyImporters></span><span class="sxs-lookup"><span data-stu-id="239a0-113">\<policyImporters></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/policyimporters.md)|<span data-ttu-id="239a0-114">Indique tous les importateurs de stratégie contrôlant l'importation d'assertions de stratégie personnalisées concernant les liaisons.</span><span class="sxs-lookup"><span data-stu-id="239a0-114">Specifies all the policy importers that control the import of custom policy assertions about bindings.</span></span> <span data-ttu-id="239a0-115">Un importateur de stratégie permet de rechercher des assertions de stratégie personnalisées concernant les fonctionnalités de liaison et de joindre un élément de liaison personnalisé qui implémente les fonctionnalités requises par l’assertion.</span><span class="sxs-lookup"><span data-stu-id="239a0-115">A policy importer is used to search custom policy assertions about binding features, as well as attach a custom binding element that implements the features the assertion requires.</span></span>|  
|[<span data-ttu-id="239a0-116">\<wsdlImporters></span><span class="sxs-lookup"><span data-stu-id="239a0-116">\<wsdlImporters></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/wsdlimporters.md)|<span data-ttu-id="239a0-117">Indique tous les importateurs WSDL qui importent des métadonnées Web Services Description Language (WSDL) 1.1 avec des pièces jointes WS-Policy.</span><span class="sxs-lookup"><span data-stu-id="239a0-117">Specifies all the WSDL importers that import Web Services Description Language (WSDL) 1.1 metadata with WS-Policy attachments.</span></span> <span data-ttu-id="239a0-118">Un importateur WSDL permet d'importer des métadonnées et de convertir ces informations en différentes classes représentant les informations de contrat et de point de terminaison.</span><span class="sxs-lookup"><span data-stu-id="239a0-118">A WSDL importer is used to import metadata as well as convert that information into various classes that represent contract and endpoint information.</span></span> <span data-ttu-id="239a0-119">Il peut importer sélectivement des informations de contrat et de point de terminaison ainsi que des propriétés qui exposent toute erreur d'importation et accepte des informations de types liées au processus d'importation et de conversion.</span><span class="sxs-lookup"><span data-stu-id="239a0-119">It can selectively import contract and endpoint information and properties that expose any import errors and accept type information relevant to the import and conversion process.</span></span> <span data-ttu-id="239a0-120">Il prend également en charge les informations et les propriétés de liaison qui donnent accès aux documents de stratégie, documents WSDL, extensions WSDL et documents de schéma XML.</span><span class="sxs-lookup"><span data-stu-id="239a0-120">It also supports importing binding information and properties that provide access to any policy documents, WSDL documents, WSDL extensions, and XML schema documents.</span></span>|  
  
### <a name="parent-elements"></a><span data-ttu-id="239a0-121">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="239a0-121">Parent Elements</span></span>  
  
|<span data-ttu-id="239a0-122">Élément</span><span class="sxs-lookup"><span data-stu-id="239a0-122">Element</span></span>|<span data-ttu-id="239a0-123">Description</span><span class="sxs-lookup"><span data-stu-id="239a0-123">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="239a0-124">\<client></span><span class="sxs-lookup"><span data-stu-id="239a0-124">\<client></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/client.md)|<span data-ttu-id="239a0-125">La section client définit la liste de points de terminaison auxquels un client peut se connecter.</span><span class="sxs-lookup"><span data-stu-id="239a0-125">The client section defines a list of endpoints that a client can connect to.</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="239a0-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="239a0-126">See also</span></span>

- <xref:System.ServiceModel.Configuration.MetadataElement>
- <xref:System.ServiceModel.Configuration.PolicyImporterElementCollection>
- <xref:System.ServiceModel.Configuration.WsdlImporterElementCollection>
- <xref:System.ServiceModel.Description.MetadataImporter>
- <xref:System.ServiceModel.Description.WsdlImporter>
- [<span data-ttu-id="239a0-127">Configuration du client WCF</span><span class="sxs-lookup"><span data-stu-id="239a0-127">WCF Client Configuration</span></span>](../../../../../docs/framework/wcf/feature-details/client-configuration.md)
- [<span data-ttu-id="239a0-128">Clients</span><span class="sxs-lookup"><span data-stu-id="239a0-128">Clients</span></span>](../../../../../docs/framework/wcf/feature-details/clients.md)
