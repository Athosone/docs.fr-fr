---
title: 'Bonnes pratiques : Intermédiaires'
ms.date: 03/30/2017
ms.assetid: 2d41b337-8132-4ac2-bea2-6e9ae2f00f8d
ms.openlocfilehash: 0bd553486bfb89a0ec14c42a1bb7d2ed9c4c540d
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59131727"
---
# <a name="best-practices-intermediaries"></a>Bonnes pratiques : Intermédiaires
La prudence est de mise pour une gestion correcte des erreurs lors de l'appel des intermédiaires afin de s'assurer que les canaux du côté service sur l'intermédiaire sont fermés.  
  
 Prenons le scénario suivant : Un client appelle un intermédiaire qui appelle un service principal.  Le service principal ne définit pas de contrat d'erreur ; par conséquent, les erreurs détectées par ce service seront traitées comme une erreur non typée.  Le service back-end lève une <xref:System.ApplicationException> et WCF abandonne le canal côté service. <xref:System.ApplicationException> apparaît ensuite en tant qu'exception <xref:System.ServiceModel.FaultException> levée sur l'intermédiaire. L'intermédiaire relève l'exception <xref:System.ApplicationException>. WCF interprète cette erreur comme une erreur non typée de l'intermédiaire et la transfère au client. Lors de la réception de l'erreur, l'intermédiaire et le client entraînent la défaillance de leurs canaux côté client. Le canal côté service de l'intermédiaire reste cependant ouvert, car WCF ignore que l'erreur est irrécupérable.  
  
 La meilleure pratique dans ce scénario consiste à détecter si l'erreur provenant du service est irrécupérable, et le cas échéant, si l'intermédiaire doit provoquer une défaillance de son canal côté service comme l'illustre l'extrait de code suivant.  
  
```csharp  
catch (Exception e)  
{  
    bool faulted = service.State == CommunicationState.Faulted;  
    service.Abort();  
    if (faulted)  
    {  
        throw new ApplicationException(e.Message);  
    }  
    else  
    {  
        throw;  
    }  
}  
```  
  
## <a name="see-also"></a>Voir aussi

- [Gestion des erreurs WCF](../../../docs/framework/wcf/wcf-error-handling.md)
- [Spécification et gestion des erreurs dans les contrats et les services](../../../docs/framework/wcf/specifying-and-handling-faults-in-contracts-and-services.md)
