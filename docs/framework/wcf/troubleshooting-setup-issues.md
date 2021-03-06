---
title: Résolution des problèmes d’installation
ms.date: 03/30/2017
ms.assetid: 1644f885-c408-4d5f-a5c7-a1a907bc8acd
ms.openlocfilehash: 69242ec745f2a5b945ae64eb558070dbf0d39c10
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61791532"
---
# <a name="troubleshooting-setup-issues"></a>Résolution des problèmes d’installation
Cette rubrique décrit comment résoudre les problèmes d’installation Windows Communication Foundation (WCF).  
  
## <a name="some-windows-communication-foundation-registry-keys-are-not-repaired-by-performing-an-msi-repair-operation-on-the-net-framework-30"></a>Certaines clés de registre Windows Communication Foundation ne sont pas réparées par l'exécution d'une opération de réparation MSI sur le .NET Framework 3.0  
 Si vous supprimez l'une des clés de registre suivantes :  
  
- HKEY_LOCAL_MACHINE\SYSTEM\CurrentControlSet\Services\ServiceModelService 3.0.0.0  
  
- HKEY_LOCAL_MACHINE\SYSTEM\CurrentControlSet\Services\ServiceModelOperation 3.0.0.0  
  
- HKEY_LOCAL_MACHINE\SYSTEM\CurrentControlSet\Services\ServiceModelEndpoint 3.0.0.0  
  
- HKEY_LOCAL_MACHINE\SYSTEM\CurrentControlSet\Services\SMSvcHost 3.0.0.0  
  
- HKEY_LOCAL_MACHINE\SYSTEM\CurrentControlSet\Services\MSDTC Bridge 3.0.0.0  
  
 Les clés ne sont pas recréées si vous exécutez la réparation à l’aide du programme d’installation de .NET Framework 3.0 lancée à partir de la **Ajout/Suppression de programmes** applet **le panneau de configuration**. Pour recréer ces clés correctement, l'utilisateur doit désinstaller, puis réinstaller le .NET Framework 3.0.  
  
## <a name="wmi-service-corruption-blocks-installation-of-the-windows-communication-foundation-wmi-provider-during-installation-of-net-framework-30-package"></a>La corruption des services WMI bloque l'installation du fournisseur WMI Windows Communication Foundation pendant l'installation du package .NET Framework 3.0  
 La corruption des services WMI peut bloquer l'installation du fournisseur WMI Windows Communication Foundation. Pendant l'installation, le programme d'installation de Windows Communication Foundation ne peut pas enregistrer le fichier WCF .mof à l'aide du composant mofcomp.exe. La section suivante présente la liste des symptômes :  
  
1. .NET Framework 3.0 s'installe correctement, mais le fournisseur WMI WCF n'est pas enregistré.  
  
2. Un événement d'erreur apparaît dans le journal des événements de l'application qui référence les problèmes d'enregistrement du fournisseur WMI pour WCF, ou d'exécution du fichier mofcomp.exe.  
  
3. Le fichier journal d'installation dd_wcf_retCA* qui se trouve dans le répertoire % temp% de l'utilisateur contient des références relatives à l'échec de l'enregistrement du fournisseur WMI WCF.  
  
4. Une exception du type de celle présentée ci-après peut être répertoriée dans le journal des événements ou le fichier journal de suivi de l'installation :  
  
     ServiceModelReg [11:09:59:046] : System.ApplicationException: Résultat inattendu 3 l’exécution de E:\WINDOWS\system32\wbem\mofcomp.exe avec « E:\WINDOWS\Microsoft.NET\Framework\v3.0\Windows Communication foundation\servicemodel.MOF »  
  
     ou :  
  
     ServiceModelReg [07:19:33:843] : System.TypeInitializationException: L’initialiseur de type de 'System.Management.ManagementPath' a levé une exception. ---> System.Runtime.InteropServices.COMException (0 x 80040154) : Récupération de la fabrique de classe COM pour le composant avec le CLSID {CF4CC405-E2C5-4DDD-B3CE-5E7582D8C9FA} a échoué en raison de l’erreur suivante : 80040154.  
  
     ou :  
  
     ServiceModelReg [07:19:32:750] : System.IO.FileNotFoundException: Impossible de charger le fichier ou l’assembly 'C:\WINDOWS\system32\wbem\mofcomp.exe' ou une de ses dépendances. Le système ne trouve pas le fichier spécifié.  
  
     Nom du fichier : 'C:\WINDOWS\system32\wbem\mofcomp.exe  
  
 Suivez la procédure suivante pour résoudre le problème décrit précédemment.  
  
1. Exécutez [l’utilitaire de diagnostic WMI, version 2.0](https://go.microsoft.com/fwlink/?LinkId=94685) pour réparer le service WMI. Pour plus d’informations sur l’utilisation de cet outil, consultez le [utilitaire de diagnostic WMI](https://go.microsoft.com/fwlink/?LinkId=94686) rubrique.  
  
 Réparer l’installation de .NET Framework 3.0 à l’aide de la **Ajout/Suppression de programmes** applet situé dans **le panneau de configuration**, ou désinstaller/réinstaller de .NET Framework 3.0.  
  
## <a name="repairing-net-framework-30-after-net-framework-35-installation-removes-configuration-elements-introduced-by-net-framework-35-in-machineconfig"></a>La réparation du .NET Framework 3.0 après l'installation du .NET Framework 3.5 supprime les éléments de configuration introduits par le .NET Framework 3.5 dans machine.config  
 Si vous réparez le .NET Framework 3.0 après l'installation du [!INCLUDE[netfx35_short](../../../includes/netfx35-short-md.md)], les éléments de configuration introduits par le [!INCLUDE[netfx35_short](../../../includes/netfx35-short-md.md)] dans machine.config sont supprimés. Cependant, web.config reste intact. La solution de contournement consiste à réparer [!INCLUDE[netfx35_short](../../../includes/netfx35-short-md.md)] par l’intermédiaire de ARP, ou utilisez le [outil WorkFlow Service Registration (WFServicesReg.exe)](../../../docs/framework/wcf/workflow-service-registration-tool-wfservicesreg-exe.md) avec la `/c` basculer.  
  
 [Outil workFlow Service Registration (WFServicesReg.exe)](../../../docs/framework/wcf/workflow-service-registration-tool-wfservicesreg-exe.md) trouverez %windir%\Microsoft.NET\framework\v3.5\ ou %windir%\Microsoft.NET\framework64\v3.5\  
  
## <a name="configure-iis-properly-for-wcfwf-webhost-after-installing-net-framework-35"></a>Configurer IIS correctement pour WCF/WF Webhost après l'installation du .NET Framework 3.5  
 Lorsque [!INCLUDE[netfx35_short](../../../includes/netfx35-short-md.md)] installation ne parvient pas à configurer les paramètres de configuration supplémentaires liées à WCF de IIS, il consigne une erreur dans le journal d’installation et continue. Toute tentative d'exécution des applications WorkflowServices échoue, étant donné que les paramètres de configuration sont manquants. Par exemple, le chargement du service xoml ou de règles peut échouer.  
  
 Pour contourner ce problème, utilisez le [outil WorkFlow Service Registration (WFServicesReg.exe)](../../../docs/framework/wcf/workflow-service-registration-tool-wfservicesreg-exe.md) avec la `/c` commutateur à configurer correctement les mappages de script IIS sur l’ordinateur. [Outil workFlow Service Registration (WFServicesReg.exe)](../../../docs/framework/wcf/workflow-service-registration-tool-wfservicesreg-exe.md) trouverez %windir%\Microsoft.NET\framework\v3.5\ ou %windir%\Microsoft.NET\framework64\v3.5\  
  
## <a name="could-not-load-type-systemservicemodelactivationhttpmodule-from-assembly-systemservicemodel-version-3000-cultureneutral-publickeytokenb77a5c561934e089"></a>Impossible de charger le type ‘System.ServiceModel.Activation.HttpModule’ à partir de l'assembly ‘System.ServiceModel, Version 3.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089’  
 Cette erreur se produit si [!INCLUDE[netfx40_short](../../../includes/netfx40-short-md.md)] est installé et puis Activation HTTP de WCF est activée. Pour résoudre le problème, exécutez la commande suivante à la ligne de commande à partir d’à l’intérieur de l’invite de commandes développeur pour Visual Studio :  
  
```Output  
aspnet_regiis.exe -i -enable  
```  
  
## <a name="see-also"></a>Voir aussi

- [Instructions d’installation](../../../docs/framework/wcf/samples/set-up-instructions.md)
