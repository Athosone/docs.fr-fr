---
title: 'Procédure : configurer des paramètres de service COM+'
ms.date: 03/30/2017
helpviewer_keywords:
- COM+ [WCF], configuring service settings
ms.assetid: f42a55a8-3af8-4394-9fdd-bf12a93780eb
ms.openlocfilehash: dd5625fd3f2c0cc2e1e2a261b091a029cd4226ed
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62039414"
---
# <a name="how-to-configure-com-service-settings"></a>Procédure : configurer des paramètres de service COM+
Lorsqu'une interface d'application est ajoutée ou supprimée en utilisant l'outil de configuration de service COM+, la configuration de service Web est mise à jour dans le fichier de configuration de l'application. Dans le mode hébergé COM +, le fichier Application.config est placé dans le répertoire racine de l’Application (%PROGRAMFILES%\ComPlus Applications\\{appid} est la valeur par défaut). Dans l'un ou l'autre des modes hébergés sur le Web, le fichier Web.config est placé dans le répertoire vroot spécifié.  
  
> [!NOTE]
>  La signature du message doit être utilisée pour éviter la falsification des messages entre un client et un serveur. De plus, le chiffrement de la couche transport ou message doit être utilisé pour se protéger contre la divulgation d'informations de messages entre un client et un serveur. Comme avec les services Windows Communication Foundation (WCF), vous devez utiliser la limitation pour limiter le nombre d’appels simultanés, les connexions, les instances et les opérations en attente. Elle permet d'empêcher la surconsommation de ressources. La fonctionnalité de limitation est spécifiée à l'aide des paramètres de fichier de configuration de service.  
  
## <a name="example"></a>Exemple  
 Prenons l'exemple d'un composant qui implémente l'interface suivante :  
  
```  
[Guid("C551FBA9-E3AA-4272-8C2A-84BD8D290AC7")]  
public interface IFinances  
{  
    string Debit(string accountNo, double amount);  
    string Credit(string accountNo, double amount);  
}  
```  
  
 Si le composant est exposé en tant que service Web, le contrat de service correspondant qui est exposé, et auquel les clients doivent se conformer, est le suivant :  
  
```  
[ServiceContract(Session = true,  
Namespace = "http://tempuri.org/C551FBA9-E3AA-4272-8C2A-84BD8D290AC7",  
Name = "IFinances")]  
public interface IFinancesContract : IDisposable  
{  
    [OperationContract]  
    string Debit(string accountNo, double amount);  
    [OperationContract]  
    string Credit(string accountNo, double amount);  
}  
```  
  
> [!NOTE]
>  IID fait partie intégrante de l'espace de noms initial pour le contrat.  
  
 Les applications clientes qui utilisent ce service doivent se conformer à ce contrat et utiliser une liaison compatible avec celui spécifié dans la configuration de l’application.  
  
 L'exemple de code suivant affiche un fichier de configuration par défaut. En étant un service Web de Windows Communication Foundation (WCF), cela est conforme au schéma de configuration de modèle de service standard et peut être modifiée dans la même façon que les autres fichiers de configuration de services WCF.  
  
 Les changements standard incluent :  
  
- Remplacer l'adresse de point de terminaison de la forme par défaut ApplicationName/ComponentName/InterfaceName par une forme plus utilisable.  
  
- Modification de l’espace de noms du service à partir de la valeur par défaut `http://tempuri.org/InterfaceID` formulaire à une forme plus pertinente.  
  
- Modifier le point de terminaison pour utiliser une liaison de transport différente.  
  
     Dans le cas hébergé par COM+, le transport de canaux nommés est utilisé par défaut, mais un transport off-machine, tel que TCP, peut être utilisé à la place.  
  
```xml  
<?xml version="1.0" encoding="utf-8"?>  
<configuration>  
    <system.serviceModel>  
        <bindings>  
            <netNamedPipeBinding>  
                <binding name="comNonTransactionalBinding" />  
                <binding name="comTransactionalBinding" transactionFlow="true" />  
            </netNamedPipeBinding>  
        </bindings>  
        <comContracts>  
            <comContract contract="{C551FBA9-E3AA-4272-8C2A-84BD8D290AC7}"  
                name="IFinances" namespace="http://tempuri.org/C551FBA9-E3AA-4272-8C2A-84BD8D290AC7"  
                requiresSession="true">  
                <exposedMethods>  
                    <add exposedMethod="Debit" />  
                    <add exposedMethod="Credit" />  
                </exposedMethods>  
            </comContract>  
        </comContracts>  
        <services>  
            <service name="{DCDB24CC-0B19-4534-95CD-FBBFF4D67DD9},{C942B840-AD54-4A44-B5F7-928130980AB9}">  
                <endpoint address="IFinances" binding="netNamedPipeBinding" bindingConfiguration="comNonTransactionalBinding"  
                    contract="{C551FBA9-E3AA-4272-8C2A-84BD8D290AC7}" />  
                <host>  
                    <baseAddresses>  
                        <add baseAddress="net.pipe://localhost/ServiceModelDocSampleApp/ServiceModelDocSample.esFinance" />  
                    </baseAddresses>  
                </host>  
            </service>  
        </services>  
    </system.serviceModel>  
</configuration>  
```  
  
## <a name="see-also"></a>Voir aussi

- [Intégration à des applications COM+](../../../../docs/framework/wcf/feature-details/integrating-with-com-plus-applications.md)
