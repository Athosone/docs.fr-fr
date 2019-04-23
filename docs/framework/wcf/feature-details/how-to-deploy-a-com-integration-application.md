---
title: 'Procédure : déployer une application d’intégration COM+'
ms.date: 03/30/2017
ms.assetid: 2e5a0510-db3c-4988-a09c-696285836650
ms.openlocfilehash: fcf525943e6e453253c6f4d3bcfa8a1a08df6909
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59343374"
---
# <a name="how-to-deploy-a-com-integration-application"></a>Procédure : déployer une application d’intégration COM+
Après avoir écrit une application d'intégration COM+, vous pouvez la déployer sur un autre ordinateur. Cette rubrique décrit comment déplacer une application d'intégration COM+ d'un ordinateur vers un autre.  
  
### <a name="moving-a-com-hosted-integration-app"></a>Déplacement d'une application d'intégration hébergée COM+  
  
1. Vérifiez que WCF est installé sur les deux ordinateurs.  
  
2. Exportez l'application de l'ordinateur A.  
  
3. Importez l'application sur l'ordinateur B.  
  
4. Définissez le répertoire racine de l'application. Par convention, il s'agit de %PROGRAMFILES%/ComPlus Applications/{AppGUID}.  
  
5. Copiez les fichiers Application.config et Application.manifest du répertoire racine de l'application sur l'ordinateur A vers le répertoire racine de l'application sur l'ordinateur B.  
  
6. Modifiez les adresses de point de terminaison de service dans le fichier Application.config sur l'ordinateur B pour identifier l'ordinateur approprié. Par exemple, remplacez `http://machineA/MyService` par `http://machineB/MyService`.  
  
### <a name="moving-a-web-hosted-integration-application"></a>Déplacement d'une application d'intégration hébergée sur le Web  
  
1. Vérifiez que WCF est installé sur les deux ordinateurs.  
  
2. Exportez l'application de l'ordinateur A.  
  
3. Importez l'application sur l'ordinateur B.  
  
4. Créez une racine virtuelle IIS sur l'ordinateur B.  
  
5. Copiez le fichier .svc (componentName.svc) et le fichier Web.config de la racine virtuelle sur l'ordinateur A vers la racine virtuelle que vous venez de créer sur l'ordinateur B.  
  
## <a name="see-also"></a>Voir aussi

- [Vue d’ensemble de l’intégration à des applications COM+](../../../../docs/framework/wcf/feature-details/integrating-with-com-plus-applications-overview.md)
- [Guide pratique pour Configurer les paramètres de Service COM +](../../../../docs/framework/wcf/feature-details/how-to-configure-com-service-settings.md)
- [Guide pratique pour Utilisez l’outil de Configuration de modèle de Service COM +](../../../../docs/framework/wcf/feature-details/how-to-use-the-com-service-model-configuration-tool.md)
