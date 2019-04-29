---
title: Période de renouvellement du verrou de l'hôte
ms.date: 03/30/2017
ms.assetid: f8ba94fc-27e0-4d8e-8f85-50a6d2a3cd43
ms.openlocfilehash: 91d83259c766120f7e3ffc9e49f1cf1b18c32a18
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61945611"
---
# <a name="host-lock-renewal-period"></a>Période de renouvellement du verrou de l'hôte
Le **Host Lock Renewal Period** propriété du Store d’Instance de Workflow SQL vous permet de spécifier la période de temps pendant lequel l’hôte renouvelle son verrou sur une instance de workflow. Le verrou reste valide pendant la période spécifiée pour la propriété Host Lock Renewal Period + 30 secondes. Si l'hôte ne renouvelle pas le verrou (en d'autres termes, s'il étend le bail) durant cette période, le verrou expire et le fournisseur de persistance déverrouille l'instance. La valeur de cette propriété est de type TimeSpan au format « hh ». La valeur minimale autorisée est « 00 : 00:01 » (1 seconde). La valeur par défaut de cette propriété est « 00 : 00:30 » (30 secondes).  
  
 Cette propriété est significative dans les scénarios où un hôte du service de workflow échoue avant d'avoir pu déverrouiller une instance de service du workflow qu'il possède. Dans ce scénario, le verrou de l'instance du service de workflow dans la base de données de persistance est supprimé par le fournisseur de persistance après l'expiration du verrou afin qu'un autre hôte du service de workflow qui s'exécute sur le même ordinateur ou sur un autre ordinateur dans une batterie de serveurs puisse acquérir le verrou et charger l'instance du service de workflow en mémoire pour reprendre son exécution à partir de son dernier état persistant.  
  
 Le fait de définir une valeur plus élevée pour cette propriété a pour effet de verrouiller les instances du service de workflow dans la base de données de persistance pendant plus longtemps et par conséquent de retarder la récupération de l'instance à partir du dernier point de persistance. Si vous définissez un intervalle court pour cette propriété, la nouvelle instance de l'hôte du service de workflow récupère rapidement l'instance du service de workflow ayant échoué, mais provoque une augmentation dans la charge de travail pour l'hôte du service de workflow et la base de données SQL Server.  
  
 Le magasin d’instances de workflow SQL exécute une tâche interne qui se réveille régulièrement et détecte les instances dont les verrous sont périmés. Lorsqu'il trouve des instances dont les verrous sont périmés, il place les instances dans la table RunnableInstances afin qu'un hôte de workflow puisse récupérer et exécuter ces instances.
