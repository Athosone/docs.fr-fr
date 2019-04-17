---
title: ETW Tracing
ms.date: 03/30/2017
ms.assetid: ac99a063-e2d2-40cc-b659-d23c2f783f92
ms.openlocfilehash: a5c2f173978f514aa4627caa476a595d8d45d4f9
ms.sourcegitcommit: 438919211260bb415fc8f96ca3eabc33cf2d681d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/16/2019
ms.locfileid: "59613744"
---
# <a name="etw-tracing"></a>ETW Tracing
Cet exemple montre comment implémenter le suivi de bout en bout (E2E) à l'aide du suivi d'événements pour Windows (ETW, Event Tracing for Windows) et du `ETWTraceListener` fourni dans cet exemple. L’exemple est basé sur le [mise en route](../../../../docs/framework/wcf/samples/getting-started-sample.md) et intègre le suivi ETW.  
  
> [!NOTE]
>  La procédure d'installation ainsi que les instructions de génération correspondant à cet exemple figurent en fin de rubrique.  
  
 Cet exemple part du principe que vous êtes familiarisé avec [Tracing and Message Logging](../../../../docs/framework/wcf/samples/tracing-and-message-logging.md).  
  
 Chaque source de suivi du modèle de suivi <xref:System.Diagnostics> peut disposer de plusieurs écouteurs de suivi qui déterminent où et comment les données sont suivies. Le type de ces écouteurs définit le format auquel les données de suivi sont enregistrées. L'exemple de code suivant indique comment ajouter un écouteur à la configuration.  
  
```xml  
<system.diagnostics>  
    <sources>  
        <source name="System.ServiceModel"   
             switchValue="Verbose,ActivityTracing"  
             propagateActivity="true">  
            <listeners>  
                <add type=  
                   "System.Diagnostics.DefaultTraceListener"  
                   name="Default">  
                   <filter type="" />  
                </add>  
                <add name="ETW">  
                    <filter type="" />  
                </add>  
            </listeners>  
        </source>  
    </sources>  
    <sharedListeners>  
        <add type=  
            "Microsoft.ServiceModel.Samples.EtwTraceListener, ETWTraceListener"  
            name="ETW" traceOutputOptions="Timestamp">  
            <filter type="" />  
       </add>  
    </sharedListeners>  
</system.diagnostics>  
```  
  
 Avant d'utiliser cet écouteur, une session de suivi ETW doit être démarrée. Pour ce faire, Logman.exe ou Tracelog.exe peut être utilisé. Cet exemple contient un fichier SetupETW.bat vous permettant de configurer une session de suivi ETW ainsi qu'un fichier CleanupETW.bat vous permettant de fermer la session et de compléter le fichier journal.  
  
> [!NOTE]
>  La procédure d'installation ainsi que les instructions de génération relatives à cet exemple figurent à la fin de cette rubrique. Pour plus d’informations sur ces outils, consultez <https://go.microsoft.com/fwlink/?LinkId=56580>  
  
 Lorsque l'écouteur ETWTraceListener est utilisé, les suivis sont enregistrés dans des fichiers .etl binaires. Si le suivi ServiceModel est activé, tous les suivis générés apparaissent dans le même fichier. Utilisez [outil Service Trace Viewer (SvcTraceViewer.exe)](../../../../docs/framework/wcf/service-trace-viewer-tool-svctraceviewer-exe.md) pour l’affichage des fichiers journaux .etl et .svclog. La visionneuse affiche une vue de bout en bout du système, ce qui permet de suivre un message de sa source à ses destination et point de consommation.  
  
 L'écouteur de suivi ETW prend en charge l'enregistrement circulaire. Pour activer cette fonctionnalité, accédez à **Démarrer**, **exécuter** et type `cmd` pour démarrer une console de commande. Dans la commande suivante, remplacez le paramètre `<logfilename>` par le nom de votre fichier journal.  
  
```  
logman create trace Wcf -o <logfilename> -p "{411a0819-c24b-428c-83e2-26b41091702e}" -f bincirc -max 1000  
```  
  
 Les commutateurs `-f` et `-max` sont facultatifs. Ils spécifient respectivement le format circulaire binaire et la taille maximale du journal, à savoir 1 000 Mo. Le commutateur `-p` est utilisé pour spécifier le fournisseur du suivi. Dans notre exemple, `"{411a0819-c24b-428c-83e2-26b41091702e}"` correspond au GUID du fournisseur d'exemples ETW XML.  
  
 Pour démarrer la session, tapez la commande suivante.  
  
```  
Logman start Wcf  
```  
  
 L'enregistrement terminé, vous pouvez arrêter la session à l'aide de la commande suivante.  
  
```  
Logman stop Wcf  
```  
  
 Ce processus génère des journaux circulaires binaires que vous pouvez traiter avec l’outil de votre choix, y compris [outil Service Trace Viewer (SvcTraceViewer.exe)](../../../../docs/framework/wcf/service-trace-viewer-tool-svctraceviewer-exe.md) ou Tracerpt.  
  
 Vous pouvez également consulter le [suivi circulaire](../../../../docs/framework/wcf/samples/circular-tracing.md) exemple pour plus d’informations sur les autres écouteurs d’effectuer une journalisation circulaire.  
  
### <a name="to-set-up-build-and-run-the-sample"></a>Pour configurer, générer et exécuter l'exemple  
  
1. Vérifiez que vous avez effectué la [procédure d’installation unique pour les exemples Windows Communication Foundation](../../../../docs/framework/wcf/samples/one-time-setup-procedure-for-the-wcf-samples.md).  
  
2. Pour générer la solution, suivez les instructions de [génération des exemples Windows Communication Foundation](../../../../docs/framework/wcf/samples/building-the-samples.md).  
  
    > [!NOTE]
    >  Pour exécuter les commandes RegisterProvider.bat, SetupETW.bat et CleanupETW.bat, vous devez utiliser un compte d'administrateur local. Si vous utilisez [!INCLUDE[wv](../../../../includes/wv-md.md)] ou version ultérieure, vous devez également exécuter l'invite de commandes avec des privilèges élevés. Pour ce faire, cliquez sur l’icône de l’invite de commandes, puis cliquez sur **exécuter en tant qu’administrateur**.  
  
3. Avant d'exécuter l'exemple, exécutez RegisterProvider.bat sur le client et le serveur. Cette opération installe le fichier ETWTracingSampleLog.etl qui permet de générer les suivis que vous pourrez ensuite afficher dans Service Trace Viewer. Ce fichier se trouve dans le dossier C:\logs. Si ce dossier n'existe pas, il doit être créé. Si vous ne respectez pas cette consigne, aucun suivi ne pourra être généré. Exécutez ensuite SetupETW.bat sur le client et le serveur pour démarrer la session de suivi ETW. Le fichier SetupETW.bat se trouve sous le dossier CS\Client.  
  
4. Pour exécuter l’exemple dans une configuration unique ou plusieurs ordinateurs, suivez les instructions de [en cours d’exécution les exemples Windows Communication Foundation](../../../../docs/framework/wcf/samples/running-the-samples.md).  
  
5. L'exécution de l'exemple terminée, exécutez CleanupETW.bat pour compléter la création du fichier ETWTracingSampleLog.etl.  
  
6. Ouvrez le fichier ETWTracingSampleLog.etl dans Service Trace Viewer. Vous serez alors invité à enregistrer ce fichier au format binaire comme fichier .svclog.  
  
7. Ouvrez ce nouveau fichier .svclog dans Service Trace Viewer pour afficher les suivis ETW et ServiceModel.  
  
> [!IMPORTANT]
>  Les exemples peuvent déjà être installés sur votre ordinateur. Recherchez le répertoire (par défaut) suivant avant de continuer.  
>   
>  `<InstallDrive>:\WF_WCF_Samples`  
>   
>  Si ce répertoire n’existe pas, accédez à [Windows Communication Foundation (WCF) et des exemples de Windows Workflow Foundation (WF) pour .NET Framework 4](https://go.microsoft.com/fwlink/?LinkId=150780) pour télécharger tous les Windows Communication Foundation (WCF) et [!INCLUDE[wf1](../../../../includes/wf1-md.md)] exemples. Cet exemple se trouve dans le répertoire suivant.  
>   
>  `<InstallDrive>:\WF_WCF_Samples\WCF\Basic\Management\AnalyticTrace`  
  
## <a name="see-also"></a>Voir aussi

- [Exemples d’analyse AppFabric](https://go.microsoft.com/fwlink/?LinkId=193959)
