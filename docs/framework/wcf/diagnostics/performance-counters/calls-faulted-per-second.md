---
title: Appels ayant renvoyé une erreur par seconde
ms.date: 03/30/2017
ms.assetid: 81c88073-8e32-4520-a71a-2c56b71ee515
ms.openlocfilehash: 5b7569b6a00757fbb863b90b25b44815a349ab07
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59115516"
---
# <a name="calls-faulted-per-second"></a>Appels ayant renvoyé une erreur par seconde
Nom du compteur : Appels ayant renvoyé une erreur par seconde  
  
## <a name="description"></a>Description  
 Nombre d'appels qui ont retourné des erreurs pour cette opération en une seconde.  
  
 Ce compteur est de type de compteur de performances [PERF_COUNTER_COUNTER](https://go.microsoft.com/fwlink/?LinkID=94649), dont la valeur est calculée à l’aide de la formule suivante.  
  
 (N 1 - N 0 ) / ( (D 1 -D 0 ) / F)  
  
 Dans les applications Windows Communication Foundation (WCF), les méthodes de service communiquent des informations d’erreur de traitement à l’aide de messages d’erreur SOAP. Les erreurs SOAP sont des types de message inclus dans les métadonnées d'une opération de service et créent, par conséquent, un contrat d'erreur permettant aux clients d'améliorer la fiabilité ou l'interactivité de leur exécution. Les erreurs SOAP étant exprimées aux clients dans un format XML, elles sont très interopérables.  
  
## <a name="see-also"></a>Voir aussi

- [Spécification et gestion des erreurs dans les contrats et les services](../../../../../docs/framework/wcf/specifying-and-handling-faults-in-contracts-and-services.md)
