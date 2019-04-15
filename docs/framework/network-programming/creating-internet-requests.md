---
title: Création de requêtes Internet
ms.date: 03/30/2017
helpviewer_keywords:
- WebRequest class, sending and receiving data
- Networking
- HttpWebResponse class, sending and receiving data
- requesting data from Internet, creating requests
- Network Resources
- Internet, requesting data
- data requests, creating requests
ms.assetid: faab683e-3f1e-4eee-b5e9-59f7245033d5
ms.openlocfilehash: 2a4915796310e4f6899d833f20bc5260e0ee032b
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59171028"
---
# <a name="creating-internet-requests"></a><span data-ttu-id="79196-102">Création de requêtes Internet</span><span class="sxs-lookup"><span data-stu-id="79196-102">Creating Internet Requests</span></span>
<span data-ttu-id="79196-103">Les applications créent des instances de <xref:System.Net.WebRequest> par le biais de la méthode <xref:System.Net.WebRequest.Create%2A?displayProperty=nameWithType>.</span><span class="sxs-lookup"><span data-stu-id="79196-103">Applications create <xref:System.Net.WebRequest> instances through the <xref:System.Net.WebRequest.Create%2A?displayProperty=nameWithType> method.</span></span> <span data-ttu-id="79196-104">Il s’agit d’une méthode statique qui crée une classe dérivée de **WebRequest** basée sur le schéma d’URI qui lui est passé.</span><span class="sxs-lookup"><span data-stu-id="79196-104">This is a static method that creates a class derived from **WebRequest** based on the URI scheme passed to it.</span></span>  
  
## <a name="web-file-and-ftp-requests"></a><span data-ttu-id="79196-105">Requêtes web, FTP et de fichier</span><span class="sxs-lookup"><span data-stu-id="79196-105">Web, File and FTP Requests</span></span>  
 <span data-ttu-id="79196-106">Le .NET Framework fournit la classe <xref:System.Net.HttpWebRequest>, qui est dérivée de **WebRequest**, pour gérer les requêtes HTTP et HTTPS.</span><span class="sxs-lookup"><span data-stu-id="79196-106">The .NET Framework provides the <xref:System.Net.HttpWebRequest> class, which is derived from **WebRequest**, to handle HTTP and HTTPS requests.</span></span> <span data-ttu-id="79196-107">Dans la plupart des cas, la classe **WebRequest** fournit toutes les propriétés dont vous avez besoin pour effectuer une requête ; toutefois, si nécessaire, vous pouvez effectuer un cast d’objets **WebRequest** créés par la méthode **WebRequest.Create** vers le type **HttpWebRequest** pour accéder aux propriétés de la requête propres à HTTP.</span><span class="sxs-lookup"><span data-stu-id="79196-107">In most cases, the **WebRequest** class provides all the properties you need to make a request; however, if necessary, you can cast **WebRequest** objects created by the **WebRequest.Create** method to the **HttpWebRequest** type to access the HTTP-specific properties of the request.</span></span> <span data-ttu-id="79196-108">De même, l’objet **HttpWebResponse** gère les réponses aux requêtes HTTP et HTTPS.</span><span class="sxs-lookup"><span data-stu-id="79196-108">Similarly, the **HttpWebResponse** object handles the responses from HTTP and HTTPS requests.</span></span> <span data-ttu-id="79196-109">Pour accéder aux propriétés de l’objet **HttpWebResponse** propres à HTTP, vous devez effectuer un cast des objets **WebResponse** vers le type **HttpWebResponse**.</span><span class="sxs-lookup"><span data-stu-id="79196-109">To access the HTTP-specific properties of the **HttpWebResponse** object, you need to cast **WebResponse** objects to the **HttpWebResponse** type.</span></span>  
  
 <span data-ttu-id="79196-110">Le .NET Framework fournit également les classes <xref:System.Net.FileWebRequest> et <xref:System.Net.FileWebResponse> afin de gérer les requêtes pour les ressources qui utilisent le schéma d’URI « file: » .</span><span class="sxs-lookup"><span data-stu-id="79196-110">The .NET Framework also provides the <xref:System.Net.FileWebRequest> and <xref:System.Net.FileWebResponse> classes to handle requests for resources that use the "file:" URI scheme.</span></span> <span data-ttu-id="79196-111">De même, les classes <xref:System.Net.FtpWebRequest> et <xref:System.Net.FtpWebResponse> sont fournies pour gérer les requêtes pour les ressources qui utilisent le schéma d’URI « ftp: ».</span><span class="sxs-lookup"><span data-stu-id="79196-111">Likewise, the <xref:System.Net.FtpWebRequest> and <xref:System.Net.FtpWebResponse> classes are provided to handle requests for resources that use the "ftp:" scheme.</span></span> <span data-ttu-id="79196-112">Si votre requête concerne une ressource qui utilise l’un de ces schémas, vous pouvez utiliser la méthode **WebRequest.Create** pour obtenir un objet avec lequel effectuer votre requête.</span><span class="sxs-lookup"><span data-stu-id="79196-112">If your request is for a resource that uses any of these schemes, you can use the **WebRequest.Create** method to obtain an object with which to make your request.</span></span>  
  
 <span data-ttu-id="79196-113">Pour gérer les requêtes qui utilisent d’autres protocoles au niveau de l’application, vous devez implémenter des classes propres au protocole dérivées de **WebRequest** et **WebResponse**.</span><span class="sxs-lookup"><span data-stu-id="79196-113">To handle requests that use other application-level protocols, you need to implement protocol-specific classes derived from **WebRequest** and **WebResponse**.</span></span> <span data-ttu-id="79196-114">Pour plus d’informations, consultez [Programmation de protocoles enfichables](../../../docs/framework/network-programming/programming-pluggable-protocols.md).</span><span class="sxs-lookup"><span data-stu-id="79196-114">For more information, see [Programming Pluggable Protocols](../../../docs/framework/network-programming/programming-pluggable-protocols.md).</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="79196-115">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="79196-115">See also</span></span>

- [<span data-ttu-id="79196-116">Procédure : demander des données à l’aide de la classe WebRequest</span><span class="sxs-lookup"><span data-stu-id="79196-116">How to: Request Data Using the WebRequest Class</span></span>](../../../docs/framework/network-programming/how-to-request-data-using-the-webrequest-class.md)
- [<span data-ttu-id="79196-117">Demande de données</span><span class="sxs-lookup"><span data-stu-id="79196-117">Requesting Data</span></span>](../../../docs/framework/network-programming/requesting-data.md)
