---
title: Définition et spécification des erreurs
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- handling faults [WCF], specifying
- handling faults [WCF], defining
ms.assetid: c00c84f1-962d-46a7-b07f-ebc4f80fbfc1
ms.openlocfilehash: 24c05bf41152fba2f54636cd0c15dde6fa71aa2b
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59299323"
---
# <a name="defining-and-specifying-faults"></a>Définition et spécification des erreurs
Les erreurs SOAP acheminent des informations de condition d'erreur d'un service à un client et, dans le cas duplex, d'un client à un service d'une manière interopérable. Cette rubrique explique quand et comment définir le contenu d'erreur personnalisé et spécifier quelles opérations peuvent les retourner. Pour plus d’informations sur la façon dont un service, ou un client duplex peut envoyer ces erreurs et comment une application cliente ou le service gère ces erreurs, consultez [Sending and Receiving Faults](../../../docs/framework/wcf/sending-and-receiving-faults.md). Pour une vue d’ensemble de la gestion des erreurs dans les applications Windows Communication Foundation (WCF), consultez [spécification et gestion des erreurs dans les contrats et Services](../../../docs/framework/wcf/specifying-and-handling-faults-in-contracts-and-services.md).  
  
## <a name="overview"></a>Vue d'ensemble  
 Les erreurs SOAP déclarées sont celles dans lesquelles une opération contient un <xref:System.ServiceModel.FaultContractAttribute?displayProperty=nameWithType> qui spécifie un type d'erreur SOAP personnalisé. Les erreurs SOAP non déclarées sont celles qui ne sont pas spécifiées dans le contrat d'une opération. Cette rubrique vous permet d'identifier ces conditions d'erreur et crée un contrat d'erreur pour votre service que les clients peuvent utiliser pour traiter correctement ces conditions d'erreur lorsqu'elles sont notifiées par des erreurs SOAP personnalisées. Les tâches de base sont, dans l’ordre :  
  
1. Définir les conditions d'erreur qu'un client de votre service doit connaître.  
  
2. Définir le contenu personnalisé des erreurs SOAP pour ces conditions d'erreur.  
  
3. Marquer vos opérations afin que les erreurs SOAP spécifiques qu'elles génèrent soient exposées aux clients dans WSDL.  
  
### <a name="defining-error-conditions-that-clients-should-know-about"></a>Définition des conditions d'erreur que les clients doivent connaître  
 Les erreurs SOAP sont des messages décrits publiquement qui contiennent des informations d'erreur pour une opération particulière. Comme elles sont décrites avec d'autres messages d'opération dans WSDL, les clients savent et, par conséquent, s'attendent à gérer ces erreurs lors de l'appel d'une opération. Mais étant donné que les services WCF sont écrits en code managé, décider quelle erreur doivent être converties en erreurs de conditions dans le code managé et retourné au client vous offre la possibilité de séparer les conditions d’erreur et les bogues dans votre service à partir de l’erreur formelle conversation avec un client.  
  
 Par exemple, l'exemple de code suivant affiche une opération qui accepte deux entiers et retourne un autre entier. Plusieurs exceptions peuvent être levées dans ce contexte, donc lorsque vous concevez le contrat d'erreur, vous devez déterminer quelles conditions d'erreur sont importantes pour votre client. Dans ce cas, le service doit détecter l'exception <xref:System.DivideByZeroException?displayProperty=nameWithType>.  
  
```csharp  
[ServiceContract]  
public class CalculatorService  
{  
    [OperationContract]   
    int Divide(int a, int b)  
    {  
      if (b==0) throw new Exception("Division by zero!");  
      return a/b;  
    }  
}  
```  
  
```vb  
<ServiceContract> _  
Public Class CalculatorService  
    <OperationContract]> _  
    Public Function Divide(ByVal a As Integer, ByVal b As Integer) _  
       As Integer  
      If (b==0) Then   
            Throw New Exception("Division by zero!")  
      Return a/b  
    End Function  
End Class  
```  
  
 Dans l'exemple précédent, l'opération retourne une erreur SOAP personnalisée qui est spécifique à une division par zéro, une erreur personnalisée qui est spécifique aux opérations de mathématique mais qui contient des informations spécifiques à une division par zéro, des erreurs multiples pour plusieurs situations d'erreur différentes ou aucune erreur SOAP.  
  
### <a name="define-the-content-of-error-conditions"></a>Définir le contenu des conditions d'erreur  
 Une fois qu'une condition d'erreur a été identifiée comme une condition qui peut retourner de façon utile une erreur SOAP personnalisée, l'étape suivante consiste à définir le contenu de cette erreur et garantir que la structure de contenu peut être sérialisée. L'exemple de code dans la section précédente affiche une erreur spécifique à une opération `Divide`, mais s'il y a d'autres opérations sur le service `Calculator`, une erreur SOAP personnalisée unique peut informer le client de toutes les conditions d'erreur de calculatrice, y compris `Divide`. L'exemple de code suivant affiche la création d'une erreur SOAP personnalisée, `MathFault`, qui peut signaler des erreurs faites à l'aide de toutes les opérations mathématique, y compris `Divide`. Si la classe peut spécifier une opération (la propriété `Operation`) et une valeur qui décrit le problème (la propriété `ProblemType`), la classe et ces propriétés doivent être sérialisables pour être transférées au client dans une erreur SOAP personnalisée. Par conséquent, les attributs <xref:System.Runtime.Serialization.DataContractAttribute?displayProperty=nameWithType> et <xref:System.Runtime.Serialization.DataMemberAttribute?displayProperty=nameWithType> sont utilisés pour rendre le type et ses propriétés sérialisables et aussi interopérables que possible.  
  
 [!code-csharp[Faults#2](../../../samples/snippets/csharp/VS_Snippets_CFX/faults/cs/service.cs#2)]
 [!code-vb[Faults#2](../../../samples/snippets/visualbasic/VS_Snippets_CFX/faults/vb/service.vb#2)]  
  
 Pour plus d’informations sur comment garantir que vos données est sérialisable, consultez [Specifying Data Transfer in Service Contracts](../../../docs/framework/wcf/feature-details/specifying-data-transfer-in-service-contracts.md). Pour obtenir la liste de la sérialisation prend en charge que <xref:System.Runtime.Serialization.DataContractSerializer?displayProperty=nameWithType> fournit, consultez [Types pris en charge par le sérialiseur de contrat de données](../../../docs/framework/wcf/feature-details/types-supported-by-the-data-contract-serializer.md).  
  
### <a name="mark-operations-to-establish-the-fault-contract"></a>Marquer des opérations pour établir le contrat d'erreur  
 Une fois qu'une structure de données sérialisable retournée dans le cadre d'une erreur SOAP personnalisée est définie, la dernière étape consiste à marquer votre contrat d'opération comme ayant retourné une erreur SOAP de ce type. Pour cela, utilisez l'attribut <xref:System.ServiceModel.FaultContractAttribute?displayProperty=nameWithType> et passez le type du type de données personnalisé que vous avez construit. L'exemple de code suivant montre comment utiliser l'attribut <xref:System.ServiceModel.FaultContractAttribute> pour spécifier que l'opération `Divide` peut retourner une erreur SOAP de type `MathFault`. D'autres opérations de mathématique peuvent désormais aussi spécifier qu'elles peuvent retourner une `MathFault`.  
  
 [!code-csharp[Faults#1](../../../samples/snippets/csharp/VS_Snippets_CFX/faults/cs/service.cs#1)]
 [!code-vb[Faults#1](../../../samples/snippets/visualbasic/VS_Snippets_CFX/faults/vb/service.vb#1)]  
  
 Une opération peut spécifier qu'elle retourne plusieurs erreurs personnalisées en marquant cette opération avec plusieurs attributs <xref:System.ServiceModel.FaultContractAttribute>.  
  
 L’étape suivante, pour implémenter le contrat d’erreur dans votre implémentation d’opération est décrite dans la rubrique [Sending and Receiving Faults](../../../docs/framework/wcf/sending-and-receiving-faults.md).  
  
#### <a name="soap-wsdl-and-interoperability-considerations"></a>Considérations sur SOAP, WSDL et l'interopérabilité  
 Dans certaines circonstances, en particulier lors de l'interaction avec d'autres plateformes, il peut être important de contrôler la manière dont se manifeste une erreur dans un message SOAP ou sa description dans les métadonnées WSDL.  
  
 L'attribut <xref:System.ServiceModel.FaultContractAttribute> a une propriété <xref:System.ServiceModel.FaultContractAttribute.Name%2A> qui autorise le contrôle du nom d'élément d'erreur WSDL généré dans les métadonnées pour cette erreur.  
  
 Selon la norme SOAP, une erreur peut avoir une `Action`, un `Code` et une `Reason`. `Action` est contrôlé par la propriété <xref:System.ServiceModel.FaultContractAttribute.Action%2A>. La propriété <xref:System.ServiceModel.FaultException.Code%2A> et la propriété <xref:System.ServiceModel.FaultException.Reason%2A> sont deux propriétés de la classe <xref:System.ServiceModel.FaultException?displayProperty=nameWithType> qui est la classe parente du <xref:System.ServiceModel.FaultException%601?displayProperty=nameWithType> générique. La propriété `Code` comprend un membre <xref:System.ServiceModel.FaultCode.SubCode%2A>.  
  
 Lors de l'accès à des non-services sources d'erreurs, certaines limitations existent. WCF prend en charge uniquement les erreurs avec des types de détail que le schéma décrit et qui sont compatibles avec les contrats de données. Par exemple, comme indiqué plus haut, WCF ne prend pas en charge erreurs qui utilisent des attributs XML dans leur type de détail ou des erreurs avec plus d’un élément de niveau supérieur dans la section détail.  
  
## <a name="see-also"></a>Voir aussi

- <xref:System.ServiceModel.FaultContractAttribute>
- <xref:System.Runtime.Serialization.DataContractAttribute>
- <xref:System.Runtime.Serialization.DataMemberAttribute>
- [Spécification et gestion des erreurs dans les contrats et les services](../../../docs/framework/wcf/specifying-and-handling-faults-in-contracts-and-services.md)
- [Envoi et réception des erreurs](../../../docs/framework/wcf/sending-and-receiving-faults.md)
- [Guide pratique pour Déclarer des erreurs dans les contrats de Service](../../../docs/framework/wcf/how-to-declare-faults-in-service-contracts.md)
- [Présentation du niveau de protection](../../../docs/framework/wcf/understanding-protection-level.md)
- [Guide pratique pour Définissez la propriété ProtectionLevel](../../../docs/framework/wcf/how-to-set-the-protectionlevel-property.md)
- [Spécification du transfert de données dans des contrats de service](../../../docs/framework/wcf/feature-details/specifying-data-transfer-in-service-contracts.md)
