---
title: WCF Services et suivi d'événements Windows
ms.date: 03/30/2017
ms.assetid: eda4355d-0bd0-4dc9-80a2-d2c832152272
ms.openlocfilehash: 35d0202a3b9cf4060240dc521554644d419a5c23
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59338967"
---
# <a name="wcf-services-and-event-tracing-for-windows"></a>WCF Services et suivi d'événements Windows
Cet exemple montre comment utiliser le traçage analytique dans Windows Communication Foundation (WCF) pour émettre des événements Event Tracing for Windows (ETW). Les traces analytiques sont des événements émis à des points clés dans la pile de WCF qui permettent la résolution des problèmes des services WCF dans un environnement de production.

 Trace analytique dans les services WCF qui est le suivi peut être activé dans un environnement de production avec un impact minimal sur les performances. Ces traces sont émises en tant qu'événements dans une session de suivi ETW.

 Cet exemple inclut un service WCF de base dans lequel les événements sont émis à partir du service dans le journal des événements, qui peut être affiché à l’aide de l’Observateur d’événements. Il est également possible de démarrer une session ETW dédiée qui écoute les événements à partir du service WCF. L'exemple comprend un script permettant de créer une session de suivi ETW dédiée qui stocke des événements dans un fichier binaire pouvant être lu à l'aide de l'Observateur d'événements.

#### <a name="to-use-this-sample"></a>Pour utiliser cet exemple

1. À l’aide de Visual Studio 2012, ouvrez le fichier solution EtwAnalyticTraceSample.sln.

2. Pour générer la solution, appuyez sur Ctrl+Maj+B.

3. Pour exécuter la solution, appuyez sur Ctrl+F5.

     Dans le navigateur Web, cliquez sur **Calculator.svc**. L'URI du document WSDL du service doit s'afficher dans le navigateur. Copiez cet URI.

     Par défaut, le service commence à écouter les demandes sur le port 1378 `http://localhost:1378/Calculator.svc`.

4. Exécutez le client de test WCF (WcfTestClient.exe).

     Le client de test WCF (WcfTestClient.exe) se trouve dans `\<Visual Studio 2012 Install Dir>\Common7\IDE\WcfTestClient.exe`.  Le répertoire d’installation de Visual Studio 2012 par défaut est `C:\Program Files\Microsoft Visual Studio 10.0`.

5. Dans le client test WCF, ajoutez le service en sélectionnant **fichier**, puis **ajouter un Service**.

     Ajoutez l'adresse du point de terminaison dans la zone d'entrée. La valeur par défaut est `http://localhost:1378/Calculator.svc`.

6. Ouvrez l'application Observateur d'événements.

     Avant d’appeler le service, démarrez l’Observateur d’événements et vérifiez que le journal des événements écoute les événements de suivi émis à partir du service WCF.

7. À partir de la **Démarrer** menu, sélectionnez **outils d’administration**, puis **Observateur d’événements**.  Activer la **analyse** et **déboguer** journaux.

8. Dans l’arborescence de commandes dans l’Observateur d’événements, accédez à **Observateur d’événements**, **journaux des Applications et Services**, **Microsoft**, **Windows**, puis **Serveur d’applications-Applications**. Avec le bouton droit **serveur d’applications-Applications**, sélectionnez **vue**, puis **afficher les journaux d’analyse et de débogage**.

     Vérifiez que le **afficher les journaux d’analyse et de débogage** option est activée.

9. Activer la **analyse** journal.

     Dans l’arborescence de commandes dans l’Observateur d’événements, accédez à **Observateur d’événements**, **journaux des Applications et Services**, **Microsoft**, **Windows**, puis **Serveur d’applications-Applications**. Avec le bouton droit **analyse** et sélectionnez **activer le journal**.

#### <a name="to-test-the-service"></a>Pour tester le service

1. Basculez vers le client test WCF et double-cliquez sur `Divide` et conservez les valeurs par défaut, qui spécifient le dénominateur 0.

     Si le dénominateur est 0, le service génère une erreur.

2. Observez les événements émis par le service.

     Revenez à l’Observateur d’événements et accédez à **Observateur d’événements**, **journaux des Applications et Services**, **Microsoft**, **Windows**, puis **Serveur d’applications-Applications**. Avec le bouton droit **analyse** et sélectionnez **Actualiser**.

     Les événements du traçage analytique de WCF s'affichent dans l'Observateur d'événements. Notez qu'en raison de l'erreur générée par le service, un événement de trace d'erreur est visible dans l'Observateur d'événements.

3. Répétez les étapes 1 et 2, mais avec des entrées valides. La valeur du paramètre `N2` peut être n'importe quel nombre différent de 0.

     Actualisez le canal analytique pour constater que les événements WCF n'incluent aucun événement d'erreur.

 L'exemple montre les événements de trace analytique émis par un service WCF.

#### <a name="to-cleanup-optional"></a>Pour effectuer un nettoyage (facultatif)

1. Ouvrez l'observateur d'événements.

2. Accédez à **Observateur d’événements**, **journaux des Applications et Services**, **Microsoft**, **Windows**, puis  **Serveur d’applications-Applications**. Avec le bouton droit **analyse** et sélectionnez **désactiver le journal**.

3. Accédez à **Observateur d’événements**, **journaux des Applications et Services**, **Microsoft**, **Windows**, puis  **Serveur d’applications-Applications**. Avec le bouton droit **analyse** et sélectionnez **effacer le journal**.

4. Choisissez le **effacer** option pour effacer les événements.

> [!IMPORTANT]
>  Les exemples peuvent déjà être installés sur votre ordinateur. Recherchez le répertoire (par défaut) suivant avant de continuer.  
>   
>  `<InstallDrive>:\WF_WCF_Samples`  
>   
>  Si ce répertoire n’existe pas, accédez à [Windows Communication Foundation (WCF) et des exemples de Windows Workflow Foundation (WF) pour .NET Framework 4](https://go.microsoft.com/fwlink/?LinkId=150780) pour télécharger tous les Windows Communication Foundation (WCF) et [!INCLUDE[wf1](../../../../includes/wf1-md.md)] exemples. Cet exemple se trouve dans le répertoire suivant.  
>   
>  `<InstallDrive>:\WF_WCF_Samples\WCF\Basic\Management\ETWTracing`  
  
## <a name="see-also"></a>Voir aussi

- [Exemples d’analyse AppFabric](https://go.microsoft.com/fwlink/?LinkId=193959)
