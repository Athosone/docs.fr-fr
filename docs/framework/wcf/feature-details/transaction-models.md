---
title: Modèles de transaction
ms.date: 03/30/2017
ms.assetid: 48a8bc1b-128b-4cf1-a421-8cc73223c340
ms.openlocfilehash: 8731b72d0657aa420dbb020e216c3af059916ce9
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62050777"
---
# <a name="transaction-models"></a><span data-ttu-id="cb442-102">Modèles de transaction</span><span class="sxs-lookup"><span data-stu-id="cb442-102">Transaction Models</span></span>
<span data-ttu-id="cb442-103">Cette rubrique décrit la relation entre les modèles de programmation de transactions et les composants d'infrastructure que Microsoft fournit.</span><span class="sxs-lookup"><span data-stu-id="cb442-103">This topic describes the relationship between the transaction programming models and the infrastructure components Microsoft provides.</span></span>  
  
 <span data-ttu-id="cb442-104">Lorsque vous utilisez des transactions dans Windows Communication Foundation (WCF), il est important de comprendre que vous en sélectionnant ne pas entre différents modèles transactionnelles, mais plutôt d’exploitation sur les différentes couches d’un modèle intégré et cohérent.</span><span class="sxs-lookup"><span data-stu-id="cb442-104">When using transactions in Windows Communication Foundation (WCF), it is important to understand that you are not selecting between different transactional models, but rather operating at different layers of an integrated and consistent model.</span></span>  
  
 <span data-ttu-id="cb442-105">Les sections suivantes décrivent les trois composants principaux d'une transaction.</span><span class="sxs-lookup"><span data-stu-id="cb442-105">The following sections describe the three primary transaction components.</span></span>  
  
## <a name="windows-communication-foundation-transactions"></a><span data-ttu-id="cb442-106">Transactions WCF (Windows Communication Foundation)</span><span class="sxs-lookup"><span data-stu-id="cb442-106">Windows Communication Foundation Transactions</span></span>  
 <span data-ttu-id="cb442-107">La prise en charge de transactions dans WCF vous permet de que écrire des services transactionnels.</span><span class="sxs-lookup"><span data-stu-id="cb442-107">The transaction support in WCF allows you write transactional services.</span></span> <span data-ttu-id="cb442-108">En outre, avec sa prise en charge pour le protocole WS-AtomicTransaction (WS-AT), les applications peuvent transférer des transactions aux services Web construits à l’aide de WCF ou une technologie tierce.</span><span class="sxs-lookup"><span data-stu-id="cb442-108">In addition, with its support for the WS-AtomicTransaction (WS-AT) protocol, applications can flow transactions to Web services built using either WCF or third-party technology.</span></span>  
  
 <span data-ttu-id="cb442-109">Dans une application ou un service WCF, fonctionnalités de transaction WCF fournissent des attributs et configuration pour spécifier de façon déclarative comment et quand l’infrastructure doit créer, flux et synchroniser des transactions.</span><span class="sxs-lookup"><span data-stu-id="cb442-109">In a WCF service or application, WCF transaction features provide attributes and configuration for declaratively specifying how and when the infrastructure should create, flow, and synchronize transactions.</span></span>  
  
## <a name="systemtransactions-transactions"></a><span data-ttu-id="cb442-110">Transactions System.Transactions</span><span class="sxs-lookup"><span data-stu-id="cb442-110">System.Transactions Transactions</span></span>  
 <span data-ttu-id="cb442-111">L’espace de noms <xref:System.Transactions> fournit un modèle de programmation explicite basé sur la classe <xref:System.Transactions.Transaction>, ainsi qu’un modèle de programmation implicite à utilisant la classe <xref:System.Transactions.TransactionScope>, dans lequel l’infrastructure gère automatiquement les transactions.</span><span class="sxs-lookup"><span data-stu-id="cb442-111">The <xref:System.Transactions> namespace provides both an explicit programming model based on the <xref:System.Transactions.Transaction> class, as well as an implicit programming model using the <xref:System.Transactions.TransactionScope> class, in which the infrastructure automatically manages transactions.</span></span>  
  
 <span data-ttu-id="cb442-112">Pour plus d’informations sur la création d’une application transactionnelle à l’aide de ces deux modèles, consultez [écriture d’une Application transactionnelle](https://go.microsoft.com/fwlink/?LinkId=94947).</span><span class="sxs-lookup"><span data-stu-id="cb442-112">For more information about how to create a transactional application using these two models, see [Writing a Transactional Application](https://go.microsoft.com/fwlink/?LinkId=94947).</span></span>  
  
 <span data-ttu-id="cb442-113">Dans une application, ou un service WCF <xref:System.Transactions> fournit le modèle de programmation pour la création de transactions au sein d’une application cliente et pour interagir explicitement avec une transaction, lorsque nécessaire, au sein d’un service.</span><span class="sxs-lookup"><span data-stu-id="cb442-113">In a WCF service or application, <xref:System.Transactions> provides the programming model for creating transactions within a client application and for explicitly interacting with a transaction, when required, within a service.</span></span>  
  
## <a name="msdtc-transactions"></a><span data-ttu-id="cb442-114">Transactions MSDTC</span><span class="sxs-lookup"><span data-stu-id="cb442-114">MSDTC Transactions</span></span>  
 <span data-ttu-id="cb442-115">MSDTC (Microsoft Distributed Transaction Coordinator) est un gestionnaire de transactions qui prend en charge les transactions distribuées.</span><span class="sxs-lookup"><span data-stu-id="cb442-115">The Microsoft Distributed Transaction Coordinator (MSDTC) is a transaction manager that provides support for distributed transactions.</span></span>  
  
 <span data-ttu-id="cb442-116">Pour plus d’informations, consultez le [de référence du programmeur DTC](https://go.microsoft.com/fwlink/?LinkId=94948).</span><span class="sxs-lookup"><span data-stu-id="cb442-116">For more information, see the [DTC Programmer's Reference](https://go.microsoft.com/fwlink/?LinkId=94948).</span></span>  
  
 <span data-ttu-id="cb442-117">Dans une application ou un service WCF, MSDTC fournit l’infrastructure pour la coordination de transactions créées au sein d’un client ou un service.</span><span class="sxs-lookup"><span data-stu-id="cb442-117">In a WCF service or application, MSDTC provides the infrastructure for the coordination of transactions created within a client or service.</span></span>
