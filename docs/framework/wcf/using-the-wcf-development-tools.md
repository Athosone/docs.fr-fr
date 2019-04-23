---
title: Utilisation des outils de développement WCF
ms.date: 03/30/2017
ms.assetid: 054adb87-c244-4d5a-83d1-0b2b44bd454b
ms.openlocfilehash: 1ffa3be4a6b8976ab978ea995e8b2c1faaacf0ae
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59144636"
---
# <a name="using-the-wcf-development-tools"></a><span data-ttu-id="46294-102">Utilisation des outils de développement WCF</span><span class="sxs-lookup"><span data-stu-id="46294-102">Using the WCF Development Tools</span></span>
<span data-ttu-id="46294-103">Cette section décrit les outils de développement Visual Studio qui peuvent vous aider à développer votre WCFservice.</span><span class="sxs-lookup"><span data-stu-id="46294-103">This section describes the Visual Studio development tools that can assist you in developing your WCFservice.</span></span>  
  
 <span data-ttu-id="46294-104">Vous pouvez utiliser les modèles Visual Studio en tant que base pour créer rapidement votre propre service, puis utiliser l’hôte de Service WCF et le Client Test WCF pour déboguer et tester votre service.</span><span class="sxs-lookup"><span data-stu-id="46294-104">You can use the Visual Studio templates as a foundation to quickly build your own service, then use WCF Service Auto Host and WCF Test Client to debug and test your service.</span></span> <span data-ttu-id="46294-105">Ces outils offrent un cycle de débogage et de test rapide et transparent tout en supprimant l'obligation de se limiter à un modèle d'hébergement à un stade précoce.</span><span class="sxs-lookup"><span data-stu-id="46294-105">These tools together provide a fast and seamless debug and testing cycle, and preclude the need to commit to a hosting model at an early stage.</span></span>  
  
## <a name="the-wcf-developer-tools"></a><span data-ttu-id="46294-106">Outils WCF Developer</span><span class="sxs-lookup"><span data-stu-id="46294-106">The WCF Developer Tools</span></span>  
 [<span data-ttu-id="46294-107">Modèles Visual Studio WCF</span><span class="sxs-lookup"><span data-stu-id="46294-107">WCF Visual Studio Templates</span></span>](../../../docs/framework/wcf/wcf-vs-templates.md)  
  
 <span data-ttu-id="46294-108">Vous pouvez utiliser les modèles de projet et d’élément Visual Studio prédéfinis dans Visual Studio pour créer rapidement des services WCF et les applications s’y rapportant.</span><span class="sxs-lookup"><span data-stu-id="46294-108">You can use the predefined Visual Studio project and item templates in Visual Studio to quickly build WCF services and surrounding applications.</span></span>  
  
 [<span data-ttu-id="46294-109">WCF Service Host (WcfSvcHost.exe)</span><span class="sxs-lookup"><span data-stu-id="46294-109">WCF Service Host (WcfSvcHost.exe)</span></span>](../../../docs/framework/wcf/wcf-service-host-wcfsvchost-exe.md)  
  
 <span data-ttu-id="46294-110">L’hôte de Service WCF (WcfSvcHost.exe) vous permet de lancer le débogueur de Visual Studio (F5) pour héberger et tester un service que vous avez implémenté automatiquement.</span><span class="sxs-lookup"><span data-stu-id="46294-110">The WCF Service Auto Host (WcfSvcHost.exe) allows you to launch the Visual Studio debugger (F5) to automatically host and test a service you have implemented.</span></span> <span data-ttu-id="46294-111">Vous pouvez ensuite tester le service en utilisant le Client de Test WCF (wcfTestClient.exe) ou votre propre client pour rechercher et corriger les erreurs potentielles.</span><span class="sxs-lookup"><span data-stu-id="46294-111">You can then test the service using the WCF Test Client (wcfTestClient.exe) or your own client to find and fix any potential errors.</span></span>  
  
 [<span data-ttu-id="46294-112">Client test WCF (WcfTestClient.exe)</span><span class="sxs-lookup"><span data-stu-id="46294-112">WCF Test Client (WcfTestClient.exe)</span></span>](../../../docs/framework/wcf/wcf-test-client-wcftestclient-exe.md)  
  
 <span data-ttu-id="46294-113">Client Test WCF (WcfTestClient.exe) est un outil GUI qui vous permet d’entrer des paramètres de types arbitraires, envoyer ces entrées au service et d’afficher que la réponse que le service renvoie.</span><span class="sxs-lookup"><span data-stu-id="46294-113">WCF Test Client (WcfTestClient.exe) is a GUI tool that allows you to input parameters of arbitrary types, submit that input to the service, and view the response the service sends back.</span></span> <span data-ttu-id="46294-114">Il offre de service transparentes lorsqu’il est associé avec l’hôte de Service WCF de test.</span><span class="sxs-lookup"><span data-stu-id="46294-114">It provides a seamless service testing experience when combined with WCF Service Auto Host.</span></span>  
  
 [<span data-ttu-id="46294-115">Génération de classes de type de données à partir de XML</span><span class="sxs-lookup"><span data-stu-id="46294-115">Generating Data Type Classes from XML</span></span>](../../../docs/framework/wcf/generating-data-type-classes-from-xml.md)  
  
 <span data-ttu-id="46294-116">Les données XML stockées dans le presse-papiers peuvent être collées dans une page de codes.</span><span class="sxs-lookup"><span data-stu-id="46294-116">XML data stored in the clipboard can be pasted into a code page.</span></span> <span data-ttu-id="46294-117">Les classes définies dans les données sont converties en types de codes.</span><span class="sxs-lookup"><span data-stu-id="46294-117">The classes defined in the data will be converted to code types.</span></span>  
  
## <a name="using-the-tools-without-administrator-privilege"></a><span data-ttu-id="46294-118">Utilisation des outils sans privilège d'administrateur</span><span class="sxs-lookup"><span data-stu-id="46294-118">Using the Tools without Administrator privilege</span></span>  
 <span data-ttu-id="46294-119">Pour permettre aux utilisateurs sans privilège d’administrateur développer des services WCF, une liste ACL (Access Control List) est créée pour l’espace de noms « http://+:8731/Design_Time_Addresses» lors de l’installation de Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="46294-119">To enable users without administrator privilege to develop WCF services, an ACL (Access Control List) is created for the namespace "http://+:8731/Design_Time_Addresses" during the installation of Visual Studio.</span></span> <span data-ttu-id="46294-120">La liste ACL a la valeur (UI), qui inclut tous les utilisateurs interactifs ayant ouvert une session sur l'ordinateur.</span><span class="sxs-lookup"><span data-stu-id="46294-120">The ACL is set to (UI), which includes all interactive users logged on to the machine.</span></span> <span data-ttu-id="46294-121">Les administrateurs peuvent ajouter ou supprimer des utilisateurs de cette liste ACL ou ouvrir des ports supplémentaires. Cette liste ACL permet aux modèles WCF ou WF d'envoyer et de recevoir des données dans leur configuration par défaut.</span><span class="sxs-lookup"><span data-stu-id="46294-121">Administrators can add or remove users from this ACL, or open additional ports.This ACL enables WCF or WF templates to send and receive data in their default configuration.</span></span> <span data-ttu-id="46294-122">Il permet également aux utilisateurs d’utiliser l’hôte de Service WCF (wcfSvcHost.exe) sans leur accorder des privilèges d’administrateur.</span><span class="sxs-lookup"><span data-stu-id="46294-122">It also enables users to use the WCF Service Auto Host (wcfSvcHost.exe) without granting them administrator privileges.</span></span>  
  
 <span data-ttu-id="46294-123">Vous pouvez modifier l'accès à l'aide de l'outil Netsh.exe dans [!INCLUDE[wv](../../../includes/wv-md.md)] par le biais du compte d'administrateur supérieur.</span><span class="sxs-lookup"><span data-stu-id="46294-123">You can modify access using the Netsh.exe tool in [!INCLUDE[wv](../../../includes/wv-md.md)] under the elevated administrator account.</span></span> <span data-ttu-id="46294-124">L'utilisation de Netsh.exe est illustrée dans l'exemple suivant.</span><span class="sxs-lookup"><span data-stu-id="46294-124">The following is an example of using Netsh.exe.</span></span>  
  
```  
netsh http add urlacl url=http://+:8001/MyService user=<domain>\<user>  
```  
  
 <span data-ttu-id="46294-125">Pour plus d’informations sur Netsh.exe, consultez [comment utiliser l’outil Netsh.exe et les commutateurs de ligne de commande](https://go.microsoft.com/fwlink/?LinkId=97877).</span><span class="sxs-lookup"><span data-stu-id="46294-125">For more information about Netsh.exe, see [How to Use the Netsh.exe Tool and Command-Line Switches](https://go.microsoft.com/fwlink/?LinkId=97877).</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="46294-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="46294-126">See also</span></span>

- [<span data-ttu-id="46294-127">Modèles Visual Studio WCF</span><span class="sxs-lookup"><span data-stu-id="46294-127">WCF Visual Studio Templates</span></span>](../../../docs/framework/wcf/wcf-vs-templates.md)
- [<span data-ttu-id="46294-128">WCF Service Host (WcfSvcHost.exe)</span><span class="sxs-lookup"><span data-stu-id="46294-128">WCF Service Host (WcfSvcHost.exe)</span></span>](../../../docs/framework/wcf/wcf-service-host-wcfsvchost-exe.md)
- [<span data-ttu-id="46294-129">Client test WCF (WcfTestClient.exe)</span><span class="sxs-lookup"><span data-stu-id="46294-129">WCF Test Client (WcfTestClient.exe)</span></span>](../../../docs/framework/wcf/wcf-test-client-wcftestclient-exe.md)
