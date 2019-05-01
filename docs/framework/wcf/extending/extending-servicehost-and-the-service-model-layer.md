---
title: Extension de ServiceHost et de la couche de modèle de service
ms.date: 03/30/2017
helpviewer_keywords:
- extending service models [WCF]
ms.assetid: 954c138a-1cd0-45a0-8abe-e4d2b8ff5400
ms.openlocfilehash: 9e08b5b7b11848262d2cb7b6ed5715799d597889
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61991768"
---
# <a name="extending-servicehost-and-the-service-model-layer"></a>Extension de ServiceHost et de la couche de modèle de service
La couche du modèle de service est chargée d'extraire des messages entrants des canaux sous-jacents, de les traduire dans des appels de méthode dans le code d'application et de renvoyer les résultats à l'appelant. Les extensions de modèle de service modifient ou implémentent le comportement et les fonctionnalités d’exécution ou de communication qui impliquent des fonctionnalités de répartiteur ou client, des comportements personnalisés, l’interception de messages et de paramètres, ainsi que d’autres fonctionnalités d’extensibilité.  
  
## <a name="in-this-section"></a>Dans cette section  
 [Extension de clients](../../../../docs/framework/wcf/extending/extending-clients.md)  
 Décrit les interfaces qui peuvent intercepter et modifier l’exécution du client, ainsi que les classes dans lesquelles vous pouvez insérer vos extensions personnalisées dans les applications clientes. Par exemple, vous pouvez exécuter la journalisation des messages client personnalisée, exécuter une sérialisation personnalisée des messages, et ainsi de suite.  
  
 [Extension des répartiteurs](../../../../docs/framework/wcf/extending/extending-dispatchers.md)  
 Décrit les interfaces qui peuvent intercepter et modifier l’exécution d’un service, ainsi que les classes dans lesquelles vous pouvez insérer vos extensions personnalisées dans les applications de service. Par exemple, vous pouvez exécuter la journalisation personnalisée du service, une validation des messages côté service, une répartition personnalisée, et ainsi de suite.  
  
 [Objets extensibles](../../../../docs/framework/wcf/extending/extensible-objects.md)  
 Décrit les cinq objets extensibles et le modèle <xref:System.ServiceModel.IExtensibleObject%601>. Le modèle d’objet extensible est utilisé pour étendre des classes d’exécution existantes à l’aide de nouvelles fonctionnalités ou ajouter un nouvel état à un objet. Les extensions, attachées à l’un des objets extensibles, permettent aux comportements à des étapes différentes du traitement, d’accéder à l’état partagé et aux fonctionnalités attachés à un objet extensible commun qui leur est accessible.  
  
 [Configuration et extension de l’exécution à l’aide de comportements](../../../../docs/framework/wcf/extending/configuring-and-extending-the-runtime-with-behaviors.md)  
 Pour modifier des paramètres ou insérer des extensions dans le runtime WCF, vous utilisez des comportements. WCF inclut des comportements implémentés par le système pour contrôler la limitation, l'instanciation et de nombreux autres aspects des services et des opérations. Cette section décrit comment créer vos propres comportements personnalisés et les rendre disponibles pour les utiliser par programme et à l'aide de fichiers de configuration.  
  
 [Extension de l’hébergement à l’aide de ServiceHostFactory](../../../../docs/framework/wcf/extending/extending-hosting-using-servicehostfactory.md)  
 Décrit comment développer <xref:System.ServiceModel.ServiceHostBase?displayProperty=nameWithType> et <xref:System.ServiceModel.ServiceHost?displayProperty=nameWithType> et comment utiliser les classes <xref:System.ServiceModel.Activation.ServiceHostFactory?displayProperty=nameWithType> pour personnaliser l'environnement hôte.  
  
## <a name="reference"></a>Référence  
  
## <a name="related-sections"></a>Rubriques connexes
