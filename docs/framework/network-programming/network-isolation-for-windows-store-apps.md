---
title: Isolement réseau pour les applications du Windows Store
ms.date: 03/30/2017
ms.assetid: b064497c-d956-46b8-838d-7a0223c7e200
ms.openlocfilehash: 0d08b09f4ed0314d4f235f10b69bbf1343935841
ms.sourcegitcommit: 558d78d2a68acd4c95ef23231c8b4e4c7bac3902
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/09/2019
ms.locfileid: "59333260"
---
# <a name="network-isolation-for-windows-store-apps"></a>Isolement réseau pour les applications du Windows Store
Les classes des espaces de noms <xref:System.Net>, <xref:System.Net.Http> et <xref:System.Net.Http.Headers> peuvent être utilisées pour développer des applications Windows Store et des applications de bureau. Lorsqu’elles sont utilisées dans une application du Windows Store, les classes de ces espaces de noms sont affectées par l’isolement réseau, qui fait partie du modèle de sécurité des applications utilisé par [!INCLUDE[win8](../../../includes/win8-md.md)]. Les fonctionnalités réseau appropriées doivent être activées dans le manifeste d’une application du Windows Store pour que le système autorise l’accès réseau.  
  
## <a name="checklist-for-network-isolation"></a>Liste de vérification pour l’isolement réseau  
 Utilisez cette liste de vérification pour vérifier que l’isolement réseau est configuré pour votre application du Windows Store.  
  
1. Déterminez la direction des requêtes d’accès réseau dont a besoin l’application. Il peut s’agir de requêtes sortantes lancées par le client, de requêtes entrantes non sollicitées, ou d’une combinaison de ces deux types de requêtes réseau.  
  
2. Déterminez le type de ressources réseau avec lesquelles l’application va communiquer. Une application peut avoir besoin de communiquer avec des ressources approuvées appartenant à un réseau domestique ou d’entreprise. Une application peut avoir besoin de communiquer avec des ressources Internet. Une application peut avoir besoin d’accéder à ces deux types de ressources réseau.  
  
3. Configurez les fonctionnalités d’isolement réseau minimales dans le manifeste d’application.  
  
4. Déployez et exécutez votre application pour la tester à l’aide des outils d’isolement réseau fournis pour la résolution des problèmes.  
  
 Pour plus d’informations sur la configuration des fonctionnalités réseau et des outils utilisés pour le dépannage de l’isolement réseau, consultez [Comment définir les fonctionnalités réseau (HTML)](https://go.microsoft.com/fwlink/?LinkID=228265) dans la documentation du développeur de [!INCLUDE[win8_appname_long](../../../includes/win8-appname-long-md.md)].  
  
## <a name="see-also"></a>Voir aussi

- [Se connecter à un service web](https://go.microsoft.com/fwlink/?LinkID=245696)
- [Recommandations et liste de contrôle de l’isolement réseau](https://go.microsoft.com/fwlink/?LinkID=228265)
- [Démarrage rapide : Se connecter avec HttpClient](https://go.microsoft.com/fwlink/?LinkId=245697)
- [Guide pratique pour utiliser les gestionnaires HttpClient](https://go.microsoft.com/fwlink/?LinkId=245699)
- [Guide pratique pour sécuriser les connexions HttpClient](https://go.microsoft.com/fwlink/?LinkId=245698)
- [Exemple HttpClient](https://go.microsoft.com/fwlink/?LinkId=242550)
