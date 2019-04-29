---
title: 'Procédure : Déclarer des erreurs dans les contrats de service'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
ms.assetid: e8da98e7-d22f-4f60-ac82-3fb0928a353f
ms.openlocfilehash: 0e173f71201d5f98a04d2ad922469e4ff6666681
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61929283"
---
# <a name="how-to-declare-faults-in-service-contracts"></a><span data-ttu-id="2fd18-102">Procédure : Déclarer des erreurs dans les contrats de service</span><span class="sxs-lookup"><span data-stu-id="2fd18-102">How to: Declare Faults in Service Contracts</span></span>
<span data-ttu-id="2fd18-103">Dans le code managé, des exceptions sont levées en cas de conditions d'erreur.</span><span class="sxs-lookup"><span data-stu-id="2fd18-103">In managed code, exceptions are thrown when error conditions occur.</span></span> <span data-ttu-id="2fd18-104">Dans les applications Windows Communication Foundation (WCF), toutefois, contrats de service spécifient les informations d’erreur sont retournées aux clients en déclarant des erreurs SOAP dans le contrat de service.</span><span class="sxs-lookup"><span data-stu-id="2fd18-104">In Windows Communication Foundation (WCF) applications, however, service contracts specify what error information is returned to clients by declaring SOAP faults in the service contract.</span></span> <span data-ttu-id="2fd18-105">Pour une vue d’ensemble de la relation entre les exceptions et erreurs, consultez [spécification et gestion des erreurs dans les contrats et Services](../../../docs/framework/wcf/specifying-and-handling-faults-in-contracts-and-services.md).</span><span class="sxs-lookup"><span data-stu-id="2fd18-105">For an overview of the relationship between exceptions and faults, see [Specifying and Handling Faults in Contracts and Services](../../../docs/framework/wcf/specifying-and-handling-faults-in-contracts-and-services.md).</span></span>  
  
### <a name="create-a-service-contract-that-specifies-a-soap-fault"></a><span data-ttu-id="2fd18-106">Créer un contrat de service qui spécifie une erreur SOAP</span><span class="sxs-lookup"><span data-stu-id="2fd18-106">Create a service contract that specifies a SOAP fault</span></span>  
  
1. <span data-ttu-id="2fd18-107">Créez un contrat de service qui contient au moins une opération.</span><span class="sxs-lookup"><span data-stu-id="2fd18-107">Create a service contract that contains at least one operation.</span></span> <span data-ttu-id="2fd18-108">Pour voir un exemple, consultez [Comment : Définir un contrat de Service](../../../docs/framework/wcf/how-to-define-a-wcf-service-contract.md).</span><span class="sxs-lookup"><span data-stu-id="2fd18-108">For an example, see [How to: Define a Service Contract](../../../docs/framework/wcf/how-to-define-a-wcf-service-contract.md).</span></span>  
  
2. <span data-ttu-id="2fd18-109">Sélectionnez une opération qui peut spécifier une condition d'erreur dont les clients peuvent s'attendre à être notifiés.</span><span class="sxs-lookup"><span data-stu-id="2fd18-109">Select an operation that can specify an error condition about which clients can expect to be notified.</span></span> <span data-ttu-id="2fd18-110">Pour déterminer les conditions d’erreur justifient de retourner des erreurs SOAP aux clients, consultez [spécification et gestion des erreurs dans les contrats et Services](../../../docs/framework/wcf/specifying-and-handling-faults-in-contracts-and-services.md).</span><span class="sxs-lookup"><span data-stu-id="2fd18-110">To decide which error conditions justify returning SOAP faults to clients, see [Specifying and Handling Faults in Contracts and Services](../../../docs/framework/wcf/specifying-and-handling-faults-in-contracts-and-services.md).</span></span>  
  
3. <span data-ttu-id="2fd18-111">Appliquez <xref:System.ServiceModel.FaultContractAttribute?displayProperty=nameWithType> à l'opération sélectionnée et passez un type d'erreur sérialisable au constructeur.</span><span class="sxs-lookup"><span data-stu-id="2fd18-111">Apply a <xref:System.ServiceModel.FaultContractAttribute?displayProperty=nameWithType> to the selected operation and pass a serializable fault type to the constructor.</span></span> <span data-ttu-id="2fd18-112">Pour plus d’informations sur la création et à l’aide de types sérialisables, consultez [Specifying Data Transfer in Service Contracts](../../../docs/framework/wcf/feature-details/specifying-data-transfer-in-service-contracts.md).</span><span class="sxs-lookup"><span data-stu-id="2fd18-112">For details about creating and using serializable types, see [Specifying Data Transfer in Service Contracts](../../../docs/framework/wcf/feature-details/specifying-data-transfer-in-service-contracts.md).</span></span> <span data-ttu-id="2fd18-113">L'exemple suivant montre comment spécifier que l'opération `SampleMethod` peut provoquer `GreetingFault`.</span><span class="sxs-lookup"><span data-stu-id="2fd18-113">The following example shows how to specify that the `SampleMethod` operation can result in a `GreetingFault`.</span></span>  
  
     [!code-csharp[FaultContractAttribute#4](../../../samples/snippets/csharp/VS_Snippets_CFX/faultcontractattribute/cs/services.cs#4)]
     [!code-vb[FaultContractAttribute#4](../../../samples/snippets/visualbasic/VS_Snippets_CFX/faultcontractattribute/vb/services.vb#4)]  
  
4. <span data-ttu-id="2fd18-114">Répétez les étapes 2 et 3 pour toutes les opérations dans le contrat qui communiquent des conditions d'erreur aux clients.</span><span class="sxs-lookup"><span data-stu-id="2fd18-114">Repeat steps 2 and 3 for all operations in the contract that communicate error conditions to clients.</span></span>  
  
## <a name="implementing-an-operation-to-return-a-specified-soap-fault"></a><span data-ttu-id="2fd18-115">Implémentation d'une opération pour retourner une erreur SOAP spécifiée</span><span class="sxs-lookup"><span data-stu-id="2fd18-115">Implementing an Operation to Return a Specified SOAP Fault</span></span>  
 <span data-ttu-id="2fd18-116">Une fois qu'une opération a spécifié qu'une erreur SOAP spécifique peut être retournée (tel que dans la procédure précédente) pour communiquer une condition d'erreur à une application appelante, l'étape suivante consiste à implémenter cette spécification.</span><span class="sxs-lookup"><span data-stu-id="2fd18-116">Once an operation has specified that a specific SOAP fault can be returned (such as in the preceding procedure) to communicate an error condition to a calling application, the next step is to implement that specification.</span></span>  
  
#### <a name="throw-the-specified-soap-fault-in-the-operation"></a><span data-ttu-id="2fd18-117">Générer l'erreur SOAP spécifiée dans l'opération</span><span class="sxs-lookup"><span data-stu-id="2fd18-117">Throw the specified SOAP fault in the operation</span></span>  
  
1. <span data-ttu-id="2fd18-118">Lorsqu’une condition d’erreur spécifique à <xref:System.ServiceModel.FaultContractAttribute> se produit dans une opération, levez une nouvelle <xref:System.ServiceModel.FaultException%601?displayProperty=nameWithType> où l’erreur SOAP spécifiée est le paramètre de type.</span><span class="sxs-lookup"><span data-stu-id="2fd18-118">When a <xref:System.ServiceModel.FaultContractAttribute>-specified error condition occurs in an operation, throw a new <xref:System.ServiceModel.FaultException%601?displayProperty=nameWithType> where the specified SOAP fault is the type parameter.</span></span> <span data-ttu-id="2fd18-119">L'exemple suivant montre comment générer `GreetingFault` dans le `SampleMethod` présenté dans la procédure précédente et dans la section de code suivante.</span><span class="sxs-lookup"><span data-stu-id="2fd18-119">The following example shows how to throw the `GreetingFault` in the `SampleMethod` shown in the preceding procedure and in the following Code section.</span></span>  
  
     [!code-csharp[FaultContractAttribute#5](../../../samples/snippets/csharp/VS_Snippets_CFX/faultcontractattribute/cs/services.cs#5)]
     [!code-vb[FaultContractAttribute#5](../../../samples/snippets/visualbasic/VS_Snippets_CFX/faultcontractattribute/vb/services.vb#5)]  
  
## <a name="example"></a><span data-ttu-id="2fd18-120">Exemple</span><span class="sxs-lookup"><span data-stu-id="2fd18-120">Example</span></span>  
 <span data-ttu-id="2fd18-121">L'exemple de code suivant montre une implémentation d'une opération unique qui spécifie `GreetingFault` pour l'opération `SampleMethod`.</span><span class="sxs-lookup"><span data-stu-id="2fd18-121">The following code example shows an implementation of a single operation that specifies a `GreetingFault` for the `SampleMethod` operation.</span></span>  
  
 [!code-csharp[FaultContractAttribute#1](../../../samples/snippets/csharp/VS_Snippets_CFX/faultcontractattribute/cs/services.cs#1)]
 [!code-vb[FaultContractAttribute#1](../../../samples/snippets/visualbasic/VS_Snippets_CFX/faultcontractattribute/vb/services.vb#1)]  
  
## <a name="see-also"></a><span data-ttu-id="2fd18-122">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="2fd18-122">See also</span></span>

- <xref:System.ServiceModel.FaultContractAttribute?displayProperty=nameWithType>
- <xref:System.ServiceModel.FaultException%601?displayProperty=nameWithType>
