---
title: Gestionnaire de jetons Web JSON
ms.date: 03/30/2017
ms.assetid: 9968f12e-e05d-4e6a-9b65-6896c0e31ab1
ms.openlocfilehash: 27c01a3d0ce0f2891b00ad28526d4753b9be4ce0
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61790128"
---
# <a name="json-web-token-handler"></a>Gestionnaire de jetons Web JSON
L’extension du gestionnaire de jetons Web JSON pour Windows Identity Foundation vous permet de créer et de valider des jetons Web JSON dans vos applications. Le gestionnaire de jetons JWT peut être configuré pour s’exécuter dans le pipeline WIF comme d’autres gestionnaires de jetons de sécurité intégrés, mais il peut également être utilisé de façon indépendante pour exécuter la validation de jetons dans des applications légères. Le gestionnaire de jetons JWT est particulièrement utile lorsque vous utilisez un modèle de jeton de porteur OAuth 2.0, comme l'authentification auprès de Microsoft Azure Active Directory.  
  
 Le gestionnaire de jetons JWT est disponible sous forme de package NuGet. Pour plus d’informations, consultez [Téléchargement du package du Gestionnaire de jetons Web JSON](../../../docs/framework/security/downloading-the-json-web-token-handler-package.md).  
  
## <a name="scenarios"></a>Scénarios  
 Le gestionnaire de jetons JWT active les principaux scénarios suivants :  
  
- **Valider un jeton JWT dans une Application serveur**: Dans ce scénario, une société nommée Litware dispose d’une application serveur qui utilise WIF pour gérer les demandes de connexion web. Litware souhaite activer son application pour utiliser des jetons JWT pour l'authentification. L'application est mise à jour à l'aide du gestionnaire de jetons JWT, puis sa configuration est mise à jour pour ajouter le gestionnaire de jetons JWT dans le pipeline WIF. Une fois que les mises à jour ont été effectuées et qu'une nouvelle demande entre dans le pipeline WIF, le jeton JWT est validé à l'aide du nouveau gestionnaire et l'authentification se produit.  
  
- **Valider un jeton JWT dans un Service Web REST**: Dans ce scénario, une société nommée Litware a un service web REST sécurisé par Windows Azure Active Directory. Les requêtes au service Web doivent être authentifiées par Microsoft Azure AD, qui publie un jeton JWT si l'authentification réussit. Litware a une application cliente qui doit accéder au service Web. Le client envoie une requête au service Web et présente son jeton JWT provenant de Microsoft Azure AD, qui est ensuite validé par le service Web à l'aide du Gestionnaire de jetons JWT. Lorsque le gestionnaire de jetons de JWT a validé le jeton, la ressource souhaitée est retournée au client par le service Web.  
  
## <a name="features"></a>Fonctionnalités  
 Le gestionnaire de jetons JWT offre les fonctionnalités suivantes :  
  
- **Valider un jeton JWT**: Jetons JWT peuvent être facilement validés par la logique de validation du Gestionnaire de jetons, soit dans le cadre du pipeline WIF de l’application ou appelés indépendamment de WIF  
  
- **Créer un jeton JWT jeton**: Le Gestionnaire de jetons JWT peut être utilisé pour créer des jetons JWT pour l’autorisation dans les services en aval
