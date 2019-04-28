---
title: Traces de diagnostic
ms.date: 03/30/2017
ms.assetid: 28e77a63-d20d-4b6a-9caf-ddad86550427
ms.openlocfilehash: 56f79fb9140785188996cc413eca4dd530037ccd
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61934795"
---
# <a name="diagnostic-traces"></a>Traces de diagnostic
Les suivis correspondent à la publication de messages spécifiques générés au cours de l'exécution de l'application. Pour utiliser le suivi, vous devez disposer d'un mécanisme de collecte et d'enregistrement des messages envoyés. Les messages de suivi sont reçus par des écouteurs. Le but d'un écouteur est de collecter, de stocker et de router les messages de suivi. Les écouteurs dirigent la sortie de suivi vers une cible appropriée, telle qu'un journal, une fenêtre ou un fichier de texte.  
  
 L'un de ces écouteurs, le <xref:System.Diagnostics.DefaultTraceListener>, est automatiquement créé et initialisé lorsque le suivi est activé. Pour que la sortie de suivi soit dirigée vers d'autres sources, créez et initialisez des écouteurs de suivi supplémentaires. Les écouteurs que vous créez doivent refléter vos besoins individuels. Par exemple, vous pouvez avoir besoin d'un enregistrement texte de toutes les données de sortie de suivi. Dans ce cas, vous devez créer un écouteur qui écrit toutes les données de sortie dans un nouveau fichier texte lorsque celui-ci est activé. En revanche, il est possible que vous ayez seulement besoin de consulter la sortie lors de l'exécution de l'application. Dans ce cas, vous pouvez créer un écouteur qui dirige toutes les données de sortie vers une fenêtre de console. <xref:System.Diagnostics.EventLogTraceListener> permet de diriger la sortie de suivi vers un journal des événements et <xref:System.Diagnostics.TextWriterTraceListener> permet de l'écrire dans un flux.  
  
## <a name="enabling-tracing"></a>Activation du suivi  
 Pour activer les suivis lors du traitement transactionnel, vous devez modifier le fichier de configuration de votre application. Voici un exemple.  
  
```xml  
<configuration>  
<system.diagnostics>  
     <sources>  
          <source name="System.Transactions" switchValue="Warning">  
               <listeners>  
                    <add name="tx"   
                     type="System.Diagnostics.XmlWriterTraceListener"   
                     initializeData= "tx.log" />  
               </listeners>  
          </source>  
     </sources>  
</system.diagnostics>  
</configuration>  
```  
  
 Les suivis <xref:System.Transactions> sont écrits dans la source nommée "System.Transactions". Vous pouvez utiliser `add` pour indiquer les nom et type de l'écouteur de suivi à utiliser. Dans notre configuration exemple, nous avons nommé l'écouteur "tx" et ajouté l'écouteur de suivi standard .NET Framework (<xref:System.Diagnostics.XmlWriterTraceListener>) en tant que type à utiliser. Utilisez `initializeData` pour définir le nom du fichier journal de cet écouteur. Vous pouvez également substituer un chemin complet par un nom de fichier simple.  
  
 Chaque type de message de suivi se voit assigner un niveau indiquant son degré d'importance. Si le niveau de suivi du domaine d'application est inférieur ou égal au niveau d'un type d'événement, le message est généré. Le niveau de suivi est contrôlé par le paramètre `switchValue` du fichier de configuration. Les niveaux associés aux messages de suivi de diagnostic sont définis dans le tableau suivant.  
  
|Niveau de suivi|Description|  
|-----------------|-----------------|  
|Critique|Des défaillances sérieuses, telles que les défaillances suivantes, se sont produites :<br /><br /> -Une erreur qui peut entraîner une perte immédiate des fonctionnalités de l’utilisateur.<br />-Un événement qui requiert un administrateur de prendre des mesures pour éviter la perte de fonctionnalité.<br />-Code se bloque.<br />-Ce niveau de suivi peut également fournir un contexte suffisant pour interpréter les autres suivis critiques. Cela peut aider à l'identification de la séquence d'opérations causant une défaillance sérieuse.|  
|Error|Une erreur (par exemple, une configuration invalide ou un comportement du réseau) susceptible d'entraîner une perte des fonctionnalités utilisateur s'est produite.|  
|Warning|Il existe une condition susceptible d'entraîner une erreur ou une défaillance critique (par exemple, un échec d'allocation ou l'approche d'une limite). Le traitement normal d'erreurs dans le code utilisateur (par exemple, l'abandon d'une transaction, l'expiration d'un délai d'attente, un échec d'authentification) peut également entraîner la génération d'un avertissement.|  
|Information|Des messages d'aide au contrôle et au diagnostic de l'état système, à la mesure des performances ou au profilage sont générés. Ils peuvent inclure des événements de durée de vie de transaction et d'inscription, tels qu'une transaction en cours de création ou de validation, le dépassement d'une limite importante ou l'allocation de ressources significatives. Un développeur peut ensuite utiliser ces informations pour la planification de capacité et la gestion des performances.|  
  
## <a name="trace-codes"></a>Codes de suivi  
 Le tableau suivant répertorie les codes de suivi générés par l'infrastructure <xref:System.Transactions>. Inclus dans la table sont l’identificateur de code de trace, la <xref:System.Diagnostics.EventTypeFilter.EventType%2A> niveau d’énumération pour la trace et les données supplémentaires contenues dans le **TraceRecord** pour la trace. En outre, le niveau de trace correspondante de la trace est également stocké dans le **TraceRecord**.  
  
|TraceCode|EventType|Données supplémentaires contenues dans TraceRecord|  
|---------------|---------------|-------------------------------|  
|TransactionCreated|Info|TransactionTraceId|  
|TransactionPromoted|Info|TransactionTraceId local, TransactionTraceId distribué|  
|EnlistmentCreated|Info|TransactionTraceId, EnlistmentTraceId, EnlistmentType (durable/volatile), EnlistmentOptions|  
|EnlistmentCallbackNegative|Warning|TransactionTraceId, EnlistmentTraceId,<br /><br /> Callback (forcerollback/aborted/indoubt)|  
|TransactionRollbackCalled|Warning|TransactionTraceId|  
|TransactionAborted|Warning|TransactionTraceId|  
|TransactionInDoubt|Warning|TransactionTraceId|  
|TransactionScopeCreated|Info|TransactionScopeResult, qui peut correspondre à l'un des éléments suivants :<br /><br /> -Nouvelle transaction.<br />-La transaction passée.<br />-Transaction dépendante passée.<br />-À l’aide de la transaction en cours.<br />-Aucune transaction.<br /><br /> nouveau TransactionTraceId en cours|  
|TransactionScopeDisposed|Info|TransactionTraceId de la portée « attendu « transaction en cours.|  
|TransactionScopeIncomplete|Warning|TransactionTraceId de la portée « attendu « transaction en cours.|  
|TransactionScopeNestedIncorrectly|Warning|TransactionTraceId de la portée « attendu « transaction en cours.|  
|TransactionScopeCurrentTransactionChanged|Warning|Ancien TransactionTraceId en cours, autre TransactionTraceId|  
|TransactionScopeTimeout|Warning|TransactionTraceId de la portée « attendu « transaction en cours.|  
|DependentCloneCreated|Info|TransactionTraceId, type de transaction dépendante créée (RollbackIfNotComplete/BlockCommitUntilComplete)|  
|DependentCloneComplete|Info|TransactionTraceId|  
|RecoveryComplete|Info|GUID de gestionnaire de ressources (de base)|  
|Reenlist|Info|GUID de gestionnaire de ressources (de base)|  
|TransactionSerialized|Info|TransactionTraceId.|  
|TransactionException|Error|Message d'exception|  
|InvalidOperationException|Error|Message d'exception|  
|InternalError|Critique|Message d'exception|  
|TransferEvent||Lorsqu'une transaction est désérialisée ou promue de transaction <xref:System.Transactions> à transaction distribuée, l'actuel ActivityID issu d'ExecutionContext et l'ID de la transaction distribuée sont écrits.<br /><br /> Lorsque le DTC rappelle le code managé, l'ID de la transaction distribuée est défini en tant qu'ActivityID dans ExecutionContext pour la durée du rappel.|  
|ConfiguredDefaultTimeoutAdjusted|Warning|Aucune donnée supplémentaire|  
|TransactionTimeout|Warning|Le TransactionTraceId de la transaction est sur le point d'expirer.|  
  
 Le schéma XML des éléments de données supplémentaires précédents se présente au format suivant.  
  
### <a name="transactiontraceidentifier"></a>TransactionTraceIdentifier  
 `<TransactionTraceIdentifier>`  
  
 `<TransactionIdentifier >`  
  
 `string representation of transaction id`  
  
 `</TransactionIdentifier>`  
  
 `< CloneIdentifier >`  
  
 `the clone id number`  
  
 `</CloneIdentifier>`  
  
 `</TransactionTraceIdentifier>`  
  
### <a name="enlistmenttraceidentifier"></a>EnlistmentTraceIdentifier  
 `<EnlistmentTraceIdentifier>`  
  
 `<ResourceManagerId>`  
  
 `string form of guid`  
  
 `</ResourceManagerId>`  
  
 `<TransactionTraceIdentifier>`  
  
 `<TransactionIdentifier >`  
  
 `string representation of transaction id`  
  
 `</TransactionIdentifier>`  
  
 `<CloneIdentifier >`  
  
 `the clone id number`  
  
 `</CloneIdentifier>`  
  
 `<TransactionTraceIdentifier>`  
  
 `<EnlistmentIdentifier>`  
  
 `the enlistment id number`  
  
 `</EnlistmentIdentifier>`  
  
 `</EnlistmentTraceIdentifier>`  
  
### <a name="resource-manager-identifier"></a>Identificateur de gestionnaire de ressources  
 `<ResourceManagerId>`  
  
 `string form of guid`  
  
 `</ResourceManagerId>`  
  
## <a name="security-issues-for-tracing"></a>Problèmes de sécurité liés au suivi  
 Lorsque vous en tant qu’administrateur activer le suivi, les informations sensibles peuvent être écrits dans un journal des traces qui est visible publiquement par défaut. Pour atténuer toute menace de sécurité, vous devez envisager de stocker le journal des traces dans un emplacement sécurisé contrôlé par des autorisations d’accès système du partage et du fichier.
