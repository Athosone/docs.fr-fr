---
title: Outil d'inscription ServiceModel (ServiceModelReg.exe)
ms.date: 03/30/2017
ms.assetid: 396ec5ae-e34f-4c64-a164-fcf50e86b6ac
ms.openlocfilehash: 5fab1a356cd035ed006bfe90d713e179907e0137
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62051778"
---
# <a name="servicemodel-registration-tool-servicemodelregexe"></a>Outil d'inscription ServiceModel (ServiceModelReg.exe)
Cet outil en ligne de commande permet de gérer l'inscription des composants WCF et WF sur un ordinateur unique. Dans des circonstances normales vous n'avez pas à utiliser cet outil, car les composants WCF et WF sont configurés lors de l'installation. Mais si vous rencontrez des problèmes avec l'activation de service, vous pouvez essayer d'inscrire les composants à l'aide de cet outil.  
  
## <a name="syntax"></a>Syntaxe  
  
```  
ServiceModelReg.exe[(-ia|-ua|-r)|((-i|-u) -c:<command>)] [-v|-q] [-nologo] [-?]  
```  
  
## <a name="remarks"></a>Notes  
 Cet outil se trouve à l'emplacement suivant :  
  
 %SystemRoot%\Microsoft.Net\Framework\v3.0\Windows Communication Foundation\  
  
> [!NOTE]
>  Quand l’outil d’inscription ServiceModel est exécutée sur [!INCLUDE[wv](../../../includes/wv-md.md)], le **les fonctionnalités de Windows** boîte de dialogue peut ne pas refléter qui le **Activation HTTP de Windows Communication Foundation** option sous **Microsoft .NET Framework 3.0** est activé. Le **les fonctionnalités de Windows** boîte de dialogue est accessible en cliquant sur **Démarrer**, puis cliquez sur **exécuter** , puis en tapant **OptionalFeatures**.  
  
 Les tableaux suivants décrivent les options qui peuvent être utilisées avec ServiceModelReg.exe.  
  
|Option|Description|  
|------------|-----------------|  
|`-ia`|Installe les composants WCF et WF.|  
|`-ua`|Désinstalle les composants WCF et WF.|  
|`-r`|Répare les composants WCF et WF.|  
|`-i`|Installe les composants WCF et WF spécifiés avec –c.|  
|`-u`|Désinstalle les composants WCF et WF spécifiés avec –c.|  
|`-c`|Installe ou désinstalle un composant :<br /><br /> -httpnamespace – réservation de Namespace HTTP<br />port - tcpportsharing – TCP service de partage<br />service d’activation - tcpactivation – TCP (non pris en charge sur .NET 4 Client Profile)<br />service - namedpipeactivation – l’activation de canal nommé (non pris en charge sur .NET 4 Client Profile<br />service d’activation - msmqactivation – MSMQ (non pris en charge sur .NET 4 Client Profile<br />manifestes de suivi des événements - etw – ETW (Windows Vista ou version ultérieure)|  
|`-q`|Mode silencieux (enregistrement des erreurs d'affichage uniquement)|  
|`-v`|Mode documenté.|  
|`-nologo`|Supprime le message de copyright et de bannière.|  
|`-?`|Affiche le texte de l'aide.|  
  
## <a name="fixing-the-fileloadexception-error"></a>Résolution de l'erreur FileLoadException  
 Si vous avez installé des versions antérieures de WCF sur votre ordinateur, vous pouvez obtenir un `FileLoadFoundException` erreur lorsque vous exécutez l’outil ServiceModelReg pour enregistrer une nouvelle installation. Cela peut se produire même si vous avez supprimé manuellement les fichiers de la précédente installation, mais que vous avez conservé les paramètres machine.config.  
  
 Le message d'erreur est semblable au message suivant.  
  
```  
Error: System.IO.FileLoadException: Could not load file or assembly 'System.ServiceModel, Version=2.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089' or one of its dependencies. The located assembly's manifest definition does not match the assembly reference. (Exception from HRESULT: 0x80131040)  
File name: 'System.ServiceModel, Version=2.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089'  
```  
  
 Ce message d’erreur indique que l’assembly de la version 2.0.0.0 de System.ServiceModel a été installé par une mise en production antérieure de CTP (Customer Technology Preview). La version actuelle de l’assembly System.ServiceModel est la version 3.0.0.0. Par conséquent, ce problème survient lorsque vous souhaitez installer la version officielle de WCF sur un ordinateur où une version CTP de WCF a été installée, mais pas complètement désinstallée.  
  
 ServiceModelReg.exe ne peut pas nettoyer les entrées de versions antérieures ; il ne peut pas non plus enregistrer les entrées de la nouvelle version. La seule solution consiste à modifier manuellement le fichier machine.config. Vous trouverez ce fichier à l'emplacement suivant :  
  
```  
%windir%\Microsoft.NET\Framework\v2.0.50727\config\machine.config   
```  
  
 Si WCF sont en cours d’exécution sur un ordinateur 64 bits, vous devez également modifier le même fichier à cet emplacement.  
  
```  
%windir%\Microsoft.NET\Framework64\v2.0.50727\config\machine.config   
```  
  
 Recherchez tous les nœuds XML dans ce fichier qui font référence à « System.ServiceModel, Version = 2.0.0.0 », supprimez les et les nœuds enfants. Enregistrez le fichier et réexécutez ServiceModelReg.exe afin de résoudre ce problème.  
  
## <a name="examples"></a>Exemples  
 Les exemples suivants indiquent comment utiliser les options les plus courantes de l'outil ServiceModelReg.exe.  
  
```  
ServiceModelReg.exe -ia  
  Installs all components  
ServiceModelReg.exe -i -c:httpnamespace -c:etw  
  Installs HTTP namespace reservation and ETW manifests  
ServiceModelReg.exe -u -c:etw  
  Uninstalls ETW manifests  
ServiceModelReg.exe -r  
  Repairs an extended install  
```
