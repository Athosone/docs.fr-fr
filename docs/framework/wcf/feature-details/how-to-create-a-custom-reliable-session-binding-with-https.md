---
title: 'Procédure : créer une liaison de session fiable personnalisée avec HTTPS'
ms.date: 03/30/2017
ms.assetid: fa772232-da1f-4c66-8c94-e36c0584b549
ms.openlocfilehash: f39325829cf4b548482a6a570a5aa1fd65e61a1d
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62039531"
---
# <a name="how-to-create-a-custom-reliable-session-binding-with-https"></a>Procédure : créer une liaison de session fiable personnalisée avec HTTPS

Cette rubrique décrit l'utilisation de la sécurité de transport SSL (Secure Socket Layer) avec les sessions fiables. Pour utiliser une session fiable sur HTTPS, vous devez créer une liaison personnalisée qui utilise une session fiable et le transport HTTPS. Vous activez la session fiable soit impérativement en utilisant du code ou de façon déclarative dans le fichier de configuration. Cette procédure utilise les fichiers de configuration client et le service pour activer la session fiable et le [  **\<httpsTransport >** ](../../../../docs/framework/configure-apps/file-schema/wcf/httpstransport.md) élément.

La partie clé de cette procédure est que le  **\<point de terminaison >** élément de configuration contiennent un `bindingConfiguration` attribut qui fait référence à une configuration de liaison personnalisée nommée `reliableSessionOverHttps`. Le [  **\<liaison >** ](../../../../docs/framework/misc/binding.md) élément de configuration fait référence à ce nom pour spécifier qu’une session fiable et le transport HTTPS sont utilisés en incluant  **\< reliableSession >** et  **\<httpsTransport >** éléments.

Pour la copie de la source de cet exemple, consultez [personnalisé de liaison de Session fiable sur HTTPS](../../../../docs/framework/wcf/samples/custom-binding-reliable-session-over-https.md).

### <a name="configure-the-service-with-a-custombinding-to-use-a-reliable-session-with-https"></a>Configurer le service avec une liaison personnalisée afin d’utiliser une session fiable avec HTTPS

1. Définissez un contrat de service pour le type de service.

   [!code-csharp[c_HowTo_CreateReliableSessionHTTPS#1121](../../../../samples/snippets/csharp/VS_Snippets_CFX/c_howto_createreliablesessionhttps/cs/service.cs#1121)]

1. Implémentez le contrat de service dans une classe de service. Notez que les informations de liaison ou d’adresse n’est pas spécifiées dans l’implémentation du service. Vous n’êtes pas obligé d’écrire du code pour extraire les informations de liaison ou d’adresse à partir du fichier de configuration.

   [!code-csharp[c_HowTo_CreateReliableSessionHTTPS#1122](../../../../samples/snippets/csharp/VS_Snippets_CFX/c_howto_createreliablesessionhttps/cs/service.cs#1122)]

1. Créer un *Web.config* fichier pour configurer un point de terminaison pour le `CalculatorService` avec une liaison personnalisée nommée `reliableSessionOverHttps` qui utilise une session fiable et le transport HTTPS.

   [!code-xml[c_HowTo_CreateReliableSessionHTTPS#2111](../../../../samples/snippets/csharp/VS_Snippets_CFX/c_howto_createreliablesessionhttps/common/web.config#2111)]

1. Créer un *Service.svc* fichier qui contient la ligne :

   ```
   <%@ServiceHost language=c# Service="CalculatorService" %>
   ```

1. Place le *Service.svc* fichier dans votre répertoire virtuel Internet Information Services (IIS).

### <a name="configure-the-client-with-a-custombinding-to-use-a-reliable-session-with-https"></a>Configurer le client avec une liaison personnalisée afin d’utiliser une session fiable avec HTTPS

1. Utilisez le [ServiceModel Metadata Utility Tool (*Svcutil.exe*)](../../../../docs/framework/wcf/servicemodel-metadata-utility-tool-svcutil-exe.md) à partir de la ligne de commande pour générer le code à partir des métadonnées de service.

   ```console
   Svcutil.exe <Metadata Exchange (MEX) address or HTTP GET address>
   ```

1. Le client généré contient la `ICalculator` interface qui définit le contrat de service que l’implémentation du client doit satisfaire.

   [!code-csharp[C_HowTo_CreateReliableSessionHTTPS#1221](../../../../samples/snippets/csharp/VS_Snippets_CFX/c_howto_createreliablesessionhttps/cs/client.cs#1221)]

1. L'application cliente générée contient également l'implémentation de `ClientCalculator`. Notez que les informations d’adresse et la liaison n’est pas spécifiées dans l’implémentation du service. Vous n’êtes pas obligé d’écrire du code pour extraire les informations de liaison et l’adresse à partir du fichier de configuration.

   [!code-csharp[C_HowTo_CreateReliableSessionHTTPS#1222](../../../../samples/snippets/csharp/VS_Snippets_CFX/c_howto_createreliablesessionhttps/cs/client.cs#1222)]

1. Configurer une liaison personnalisée nommée `reliableSessionOverHttps` à utiliser le transport HTTPS et les sessions fiables.

   [!code-xml[C_HowTo_CreateReliableSessionHTTPS#2211](../../../../samples/snippets/csharp/VS_Snippets_CFX/c_howto_createreliablesessionhttps/common/app.config#2211)]

1. Créez une instance `ClientCalculator` dans une application, puis appelez les opérations de service.

   [!code-csharp[C_HowTo_CreateReliableSessionHTTPS#1223](../../../../samples/snippets/csharp/VS_Snippets_CFX/c_howto_createreliablesessionhttps/cs/client.cs#1223)]

1. Compilez, puis exécutez le client.  

## <a name="net-framework-security"></a>sécurité du .NET Framework

Étant donné que le certificat utilisé dans cet exemple est un certificat de test créé avec *Makecert.exe*, une alerte de sécurité s’affiche lorsque vous essayez d’accéder à une adresse HTTPS, comme `https://localhost/servicemodelsamples/service.svc`, à partir de votre navigateur.

## <a name="see-also"></a>Voir aussi

- [Sessions fiables](../../../../docs/framework/wcf/feature-details/reliable-sessions.md)
