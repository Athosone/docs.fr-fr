---
title: MsmqBindingElementBase
ms.date: 03/30/2017
ms.assetid: 210d41ab-a2a4-4d7a-afd2-0916c08a4015
ms.openlocfilehash: 1df4b32feda246a536183a42ac11b113bc4bb259
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61963434"
---
# <a name="msmqbindingelementbase"></a><span data-ttu-id="c55f2-102">MsmqBindingElementBase</span><span class="sxs-lookup"><span data-stu-id="c55f2-102">MsmqBindingElementBase</span></span>
<span data-ttu-id="c55f2-103">MsmqBindingElementBase</span><span class="sxs-lookup"><span data-stu-id="c55f2-103">MsmqBindingElementBase</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="c55f2-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="c55f2-104">Syntax</span></span>  
  
```csharp  
class MsmqBindingElementBase : TransportBindingElement  
{  
  string CustomDeadLetterQueue;  
  string DeadLetterQueue;  
  boolean Durable;  
  boolean ExactlyOnce;  
  sint32 MaxRetryCycles;  
  string ReceiveErrorHandling;  
  sint32 ReceiveRetryCount;  
  datetime RetryCycleDelay;  
  datetime TimeToLive;  
  boolean UseMsmqTracing;  
  boolean UseSourceJournal;  
};  
```  
  
## <a name="methods"></a><span data-ttu-id="c55f2-105">Méthodes</span><span class="sxs-lookup"><span data-stu-id="c55f2-105">Methods</span></span>  
 <span data-ttu-id="c55f2-106">La classe MsmqBindingElementBase ne définit pas de méthode.</span><span class="sxs-lookup"><span data-stu-id="c55f2-106">The MsmqBindingElementBase class does not define any methods.</span></span>  
  
## <a name="properties"></a><span data-ttu-id="c55f2-107">Properties</span><span class="sxs-lookup"><span data-stu-id="c55f2-107">Properties</span></span>  
 <span data-ttu-id="c55f2-108">La classe MsmqBindingElementBase a les propriétés suivantes :</span><span class="sxs-lookup"><span data-stu-id="c55f2-108">The MsmqBindingElementBase class has the following properties:</span></span>  
  
### <a name="customdeadletterqueue"></a><span data-ttu-id="c55f2-109">CustomDeadLetterQueue</span><span class="sxs-lookup"><span data-stu-id="c55f2-109">CustomDeadLetterQueue</span></span>  
 <span data-ttu-id="c55f2-110">Type de données : chaîne</span><span class="sxs-lookup"><span data-stu-id="c55f2-110">Data type: string</span></span>  
  
 <span data-ttu-id="c55f2-111">Type d’accès : Propriétés en lecture seule</span><span class="sxs-lookup"><span data-stu-id="c55f2-111">Access type: Read-only</span></span>  
  
 <span data-ttu-id="c55f2-112">URI qui contient l'emplacement de la file d'attente de lettres mortes pour chaque application, dans laquelle les messages expirés ou dont le transfert ou la remise a échoué sont placés.</span><span class="sxs-lookup"><span data-stu-id="c55f2-112">A URI that contains the location of the dead letter queue for each application, where messages that have expired or that have failed transfer or delivery are placed.</span></span>  
  
### <a name="deadletterqueue"></a><span data-ttu-id="c55f2-113">DeadLetterQueue</span><span class="sxs-lookup"><span data-stu-id="c55f2-113">DeadLetterQueue</span></span>  
 <span data-ttu-id="c55f2-114">Type de données : chaîne</span><span class="sxs-lookup"><span data-stu-id="c55f2-114">Data type: string</span></span>  
  
 <span data-ttu-id="c55f2-115">Type d’accès : Propriétés en lecture seule</span><span class="sxs-lookup"><span data-stu-id="c55f2-115">Access type: Read-only</span></span>  
  
 <span data-ttu-id="c55f2-116">Valeur d'énumération qui indique le type de la file d'attente de lettres mortes à utiliser.</span><span class="sxs-lookup"><span data-stu-id="c55f2-116">An enumeration value that indicates the type of dead letter queue to use.</span></span>  
  
### <a name="durable"></a><span data-ttu-id="c55f2-117">Durable</span><span class="sxs-lookup"><span data-stu-id="c55f2-117">Durable</span></span>  
 <span data-ttu-id="c55f2-118">Type de données : booléen</span><span class="sxs-lookup"><span data-stu-id="c55f2-118">Data type: boolean</span></span>  
  
 <span data-ttu-id="c55f2-119">Type d’accès : Propriétés en lecture seule</span><span class="sxs-lookup"><span data-stu-id="c55f2-119">Access type: Read-only</span></span>  
  
 <span data-ttu-id="c55f2-120">Valeur qui indique si les messages traités par cette liaison sont durables ou volatils.</span><span class="sxs-lookup"><span data-stu-id="c55f2-120">A value that indicates whether the messages processed by this binding are durable or volatile.</span></span>  
  
### <a name="exactlyonce"></a><span data-ttu-id="c55f2-121">ExactlyOnce</span><span class="sxs-lookup"><span data-stu-id="c55f2-121">ExactlyOnce</span></span>  
 <span data-ttu-id="c55f2-122">Type de données : booléen</span><span class="sxs-lookup"><span data-stu-id="c55f2-122">Data type: boolean</span></span>  
  
 <span data-ttu-id="c55f2-123">Type d’accès : Propriétés en lecture seule</span><span class="sxs-lookup"><span data-stu-id="c55f2-123">Access type: Read-only</span></span>  
  
 <span data-ttu-id="c55f2-124">Valeur booléenne qui indique si les messages traités par cette liaison sont reçus exactement une fois.</span><span class="sxs-lookup"><span data-stu-id="c55f2-124">A Boolean value that indicates whether messages processed by this binding are received exactly once.</span></span>  
  
### <a name="maxretrycycles"></a><span data-ttu-id="c55f2-125">MaxRetryCycles</span><span class="sxs-lookup"><span data-stu-id="c55f2-125">MaxRetryCycles</span></span>  
 <span data-ttu-id="c55f2-126">Type de données : sint32</span><span class="sxs-lookup"><span data-stu-id="c55f2-126">Data type: sint32</span></span>  
  
 <span data-ttu-id="c55f2-127">Type d’accès : Propriétés en lecture seule</span><span class="sxs-lookup"><span data-stu-id="c55f2-127">Access type: Read-only</span></span>  
  
 <span data-ttu-id="c55f2-128">Nombre maximal de cycles de nouvelle tentative de livraison de messages à l'application de réception.</span><span class="sxs-lookup"><span data-stu-id="c55f2-128">The maximum number of retry cycles to attempt delivery of messages to the receiving application.</span></span>  
  
### <a name="receiveerrorhandling"></a><span data-ttu-id="c55f2-129">ReceiveErrorHandling</span><span class="sxs-lookup"><span data-stu-id="c55f2-129">ReceiveErrorHandling</span></span>  
 <span data-ttu-id="c55f2-130">Type de données : chaîne</span><span class="sxs-lookup"><span data-stu-id="c55f2-130">Data type: string</span></span>  
  
 <span data-ttu-id="c55f2-131">Type d’accès : Propriétés en lecture seule</span><span class="sxs-lookup"><span data-stu-id="c55f2-131">Access type: Read-only</span></span>  
  
 <span data-ttu-id="c55f2-132">Paramètres de gestion de messages incohérents.</span><span class="sxs-lookup"><span data-stu-id="c55f2-132">The settings for poison message handling.</span></span>  
  
### <a name="receiveretrycount"></a><span data-ttu-id="c55f2-133">ReceiveRetryCount</span><span class="sxs-lookup"><span data-stu-id="c55f2-133">ReceiveRetryCount</span></span>  
 <span data-ttu-id="c55f2-134">Type de données : sint32</span><span class="sxs-lookup"><span data-stu-id="c55f2-134">Data type: sint32</span></span>  
  
 <span data-ttu-id="c55f2-135">Type d’accès : Propriétés en lecture seule</span><span class="sxs-lookup"><span data-stu-id="c55f2-135">Access type: Read-only</span></span>  
  
 <span data-ttu-id="c55f2-136">Nombre maximal de nouvelles tentatives immédiates sur un message qui est lu à partir de la file d'attente d'application.</span><span class="sxs-lookup"><span data-stu-id="c55f2-136">The maximum number of immediate retry attempts on a message that is read from the application queue.</span></span>  
  
### <a name="retrycycledelay"></a><span data-ttu-id="c55f2-137">RetryCycleDelay</span><span class="sxs-lookup"><span data-stu-id="c55f2-137">RetryCycleDelay</span></span>  
 <span data-ttu-id="c55f2-138">Type de données : datetime</span><span class="sxs-lookup"><span data-stu-id="c55f2-138">Data type: datetime</span></span>  
  
 <span data-ttu-id="c55f2-139">Type d’accès : Propriétés en lecture seule</span><span class="sxs-lookup"><span data-stu-id="c55f2-139">Access type: Read-only</span></span>  
  
 <span data-ttu-id="c55f2-140">Valeur qui indique l'intervalle entre des cycles de nouvelle tentative de remise d'un message n'ayant pas pu être remis immédiatement.</span><span class="sxs-lookup"><span data-stu-id="c55f2-140">A value that indicates the time delay between retry cycles when attempting to deliver a message that could not be delivered immediately.</span></span>  
  
### <a name="timetolive"></a><span data-ttu-id="c55f2-141">TimeToLive</span><span class="sxs-lookup"><span data-stu-id="c55f2-141">TimeToLive</span></span>  
 <span data-ttu-id="c55f2-142">Type de données : datetime</span><span class="sxs-lookup"><span data-stu-id="c55f2-142">Data type: datetime</span></span>  
  
 <span data-ttu-id="c55f2-143">Type d’accès : Propriétés en lecture seule</span><span class="sxs-lookup"><span data-stu-id="c55f2-143">Access type: Read-only</span></span>  
  
 <span data-ttu-id="c55f2-144">Intervalle qui indique combien de temps les messages traités par cette liaison peuvent séjourner dans la file d’attente avant expiration.</span><span class="sxs-lookup"><span data-stu-id="c55f2-144">The interval of time that indicates how long the messages processed by this binding can be in the queue before they expire.</span></span>  
  
### <a name="usemsmqtracing"></a><span data-ttu-id="c55f2-145">UseMsmqTracing</span><span class="sxs-lookup"><span data-stu-id="c55f2-145">UseMsmqTracing</span></span>  
 <span data-ttu-id="c55f2-146">Type de données : booléen</span><span class="sxs-lookup"><span data-stu-id="c55f2-146">Data type: boolean</span></span>  
  
 <span data-ttu-id="c55f2-147">Type d’accès : Propriétés en lecture seule</span><span class="sxs-lookup"><span data-stu-id="c55f2-147">Access type: Read-only</span></span>  
  
 <span data-ttu-id="c55f2-148">Valeur booléenne qui indique si les messages traités par cette liaison doivent être suivis.</span><span class="sxs-lookup"><span data-stu-id="c55f2-148">A Boolean value that indicates whether messages processed by this binding should be traced.</span></span>  
  
### <a name="usesourcejournal"></a><span data-ttu-id="c55f2-149">UseSourceJournal</span><span class="sxs-lookup"><span data-stu-id="c55f2-149">UseSourceJournal</span></span>  
 <span data-ttu-id="c55f2-150">Type de données : booléen</span><span class="sxs-lookup"><span data-stu-id="c55f2-150">Data type: boolean</span></span>  
  
 <span data-ttu-id="c55f2-151">Type d’accès : Propriétés en lecture seule</span><span class="sxs-lookup"><span data-stu-id="c55f2-151">Access type: Read-only</span></span>  
  
 <span data-ttu-id="c55f2-152">Valeur booléenne qui indique si les copies des messages traités par cette liaison doivent être stockées dans la file d’attente du journal source.</span><span class="sxs-lookup"><span data-stu-id="c55f2-152">A Boolean value that indicates whether copies of messages processed by this binding should be stored in the source journal queue.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="c55f2-153">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="c55f2-153">Requirements</span></span>  
  
|<span data-ttu-id="c55f2-154">MOF</span><span class="sxs-lookup"><span data-stu-id="c55f2-154">MOF</span></span>|<span data-ttu-id="c55f2-155">Déclaré dans Servicemodel.mof.</span><span class="sxs-lookup"><span data-stu-id="c55f2-155">Declared in Servicemodel.mof.</span></span>|  
|---------|-----------------------------------|  
|<span data-ttu-id="c55f2-156">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="c55f2-156">Namespace</span></span>|<span data-ttu-id="c55f2-157">Défini dans root\ServiceModel</span><span class="sxs-lookup"><span data-stu-id="c55f2-157">Defined in root\ServiceModel</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="c55f2-158">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c55f2-158">See also</span></span>

- <xref:System.ServiceModel.NetMsmqBinding>
- <xref:System.ServiceModel.MsmqBindingBase>
