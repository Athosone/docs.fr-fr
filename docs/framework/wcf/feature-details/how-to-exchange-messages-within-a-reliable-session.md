---
title: 'Procédure : échanger des messages au sein d’une session fiable'
ms.date: 03/30/2017
ms.assetid: 87cd0e75-dd2c-44c1-8da0-7b494bbdeaea
ms.openlocfilehash: aad4eae870e3ba603c56a28a620fe8bc0e31ceb6
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59342984"
---
# <a name="how-to-exchange-messages-within-a-reliable-session"></a>Procédure : échanger des messages au sein d’une session fiable

Cette rubrique décrit les étapes requises pour activer une session fiable utilisant l’une des liaisons fournies par le système qui prennent en charge une telle session, mais pas par défaut. Vous activez une session fiable de façon impérative à l’aide de code ou de façon déclarative dans votre fichier de configuration. Cette procédure utilise les fichiers de configuration client et le service pour activer la session fiable et pour stipuler que les messages arrivent dans le même ordre que celui dans lequel ils ont été envoyés.

La partie clé de cette procédure est que l’élément de configuration de point de terminaison contiennent un `bindingConfiguration` attribut qui fait référence à une configuration de liaison nommée `Binding1`. Le [  **\<liaison >** ](../../../../docs/framework/misc/binding.md) élément de configuration fait référence à ce nom pour activer les sessions fiables en définissant le `enabled` attribut de la [  **\<reliableSession >** ](https://docs.microsoft.com/previous-versions/dotnet/netframework-4.0/ms731302(v=vs.100)) élément à `true`. Vous spécifiez les assurances de remise ordonnée pour la session fiable en affectant à l'attribut `ordered` la valeur `true`.

Pour la copie de la source de cet exemple, consultez [Session fiable WS](../../../../docs/framework/wcf/samples/ws-reliable-session.md).

### <a name="configure-the-service-with-a-wshttpbinding-to-use-a-reliable-session"></a>Configurer le service avec une liaison WSHttpBinding afin d’utiliser une session fiable

1. Définissez un contrat de service pour le type de service.

   [!code-csharp[c_HowTo_UseReliableSession#1121](../../../../samples/snippets/csharp/VS_Snippets_CFX/c_howto_usereliablesession/cs/service.cs#1121)]

1. Implémentez le contrat de service dans une classe de service. Notez que les informations de liaison ou d’adresse n’est pas spécifiées dans l’implémentation du service. Vous n’êtes pas obligé d’écrire du code pour extraire les informations de liaison ou d’adresse à partir du fichier de configuration.

   [!code-csharp[c_HowTo_UseReliableSession#1122](../../../../samples/snippets/csharp/VS_Snippets_CFX/c_howto_usereliablesession/cs/service.cs#1122)]

1. Créer un *Web.config* fichier pour configurer un point de terminaison pour le `CalculatorService` qui utilise le <xref:System.ServiceModel.WSHttpBinding> avec une session fiable activée et la livraison chronologique des messages requis.

   [!code-xml[c_HowTo_UseReliableSession#2111](../../../../samples/snippets/csharp/VS_Snippets_CFX/c_howto_usereliablesession/common/web.config#2111)]

1. Créer un *Service.svc* fichier qui contient la ligne :

   ```
   <%@ServiceHost language=c# Service="CalculatorService" %>
   ```

1. Place le *Service.svc* fichier dans votre répertoire virtuel Internet Information Services (IIS).

### <a name="configure-the-client-with-a-wshttpbinding-to-use-a-reliable-session"></a>Configurer le client avec une liaison WSHttpBinding afin d’utiliser une session fiable

1. Utilisez le [ServiceModel Metadata Utility Tool (*Svcutil.exe*)](../../../../docs/framework/wcf/servicemodel-metadata-utility-tool-svcutil-exe.md) à partir de la ligne de commande pour générer le code à partir des métadonnées de service :

   ```console
   Svcutil.exe <service's Metadata Exchange (MEX) address or HTTP GET address>
   ```

1. Le client généré contient la `ICalculator` interface qui définit le contrat de service que l’implémentation du client doit satisfaire.

   [!code-csharp[C_HowTo_UseReliableSession#1221](../../../../samples/snippets/csharp/VS_Snippets_CFX/c_howto_usereliablesession/cs/client.cs#1221)]

1. L'application cliente générée contient également l'implémentation de `ClientCalculator`. Notez que les informations d’adresse et la liaison n’est pas spécifiées de n’importe où à l’intérieur de l’implémentation du service. Vous n’êtes pas obligé d’écrire du code pour extraire les informations de liaison ou d’adresse à partir du fichier de configuration.

   [!code-csharp[C_HowTo_UseReliableSession#1222](../../../../samples/snippets/csharp/VS_Snippets_CFX/c_howto_usereliablesession/cs/client.cs#1222)]

1. *SvcUtil.exe* génère également la configuration pour le client qui utilise le <xref:System.ServiceModel.WSHttpBinding> classe. Nommez le fichier de configuration *App.config* lors de l’utilisation de Visual Studio.

   [!code-xml[C_HowTo_UseReliableSession#2211](../../../../samples/snippets/csharp/VS_Snippets_CFX/c_howto_usereliablesession/common/app.config#2211)]

1. Créez une instance de la `ClientCalculator` dans une application et appeler les opérations de service.

   [!code-csharp[C_HowTo_UseReliableSession#1223](../../../../samples/snippets/csharp/VS_Snippets_CFX/c_howto_usereliablesession/cs/client.cs#1223)]

1. Compilez, puis exécutez le client.

## <a name="example"></a>Exemple

Plusieurs liaisons fournies par le système prennent en charge des sessions fiables par défaut. Elles incluent notamment :

- <xref:System.ServiceModel.WSDualHttpBinding>

- <xref:System.ServiceModel.NetNamedPipeBinding>

- <xref:System.ServiceModel.MsmqIntegration.MsmqIntegrationBinding>

Pour obtenir un exemple montrant comment créer une liaison personnalisée qui prend en charge des sessions fiables, consultez [Comment : Créer une liaison de Session fiable personnalisée avec le protocole HTTPS](../../../../docs/framework/wcf/feature-details/how-to-create-a-custom-reliable-session-binding-with-https.md).

## <a name="see-also"></a>Voir aussi

- [Sessions fiables](../../../../docs/framework/wcf/feature-details/reliable-sessions.md)
