---
title: PNRP dans le développement d’applications
ms.date: 03/30/2017
ms.assetid: 265615d6-4423-4b5d-8626-752e456f4f4e
ms.openlocfilehash: 4cd0d739e58cd252213e8d5c16d29cc612338df6
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59178137"
---
# <a name="pnrp-in-application-development"></a><span data-ttu-id="da4c3-102">PNRP dans le développement d’applications</span><span class="sxs-lookup"><span data-stu-id="da4c3-102">PNRP in Application Development</span></span>
<span data-ttu-id="da4c3-103">Dans Windows Vista, les applications réseau peuvent accéder aux fonctions de résolution et de publication des noms via une API PNRP simplifiée.</span><span class="sxs-lookup"><span data-stu-id="da4c3-103">In Windows Vista, networking applications can access name publication and resolution functions through a simplified PNRP application programming interface (API).</span></span>  
  
## <a name="implementing-the-peer-name-resolution-protocol"></a><span data-ttu-id="da4c3-104">Implémentation du protocole PNRP</span><span class="sxs-lookup"><span data-stu-id="da4c3-104">Implementing the Peer Name Resolution Protocol</span></span>  
 <span data-ttu-id="da4c3-105">Avec l’API PNRP simplifiée, les clouds ne sont pas explicitement spécifiés pour inscrire des noms et des adresses. Le composant PNRP détermine automatiquement les clouds qu’il est possible de rejoindre, ainsi que les adresses à publier dans les clouds.</span><span class="sxs-lookup"><span data-stu-id="da4c3-105">With the simplified PNRP API, clouds are not explicitly specified to register the name and addresses; the PNRP component automatically determines the appropriate clouds to join and the addresses to publish within the clouds.</span></span>  
  
 <span data-ttu-id="da4c3-106">Pour une résolution beaucoup plus simple des noms PNRP dans Windows Vista, ceux-ci sont désormais intégrés dans la fonction getaddrinfo() de Windows Sockets.</span><span class="sxs-lookup"><span data-stu-id="da4c3-106">For highly simplified PNRP name resolution in Windows Vista, PNRP names are now integrated into the getaddrinfo() Windows Sockets function.</span></span> <span data-ttu-id="da4c3-107">Pour utiliser PNRP afin de résoudre un nom en une adresse IPv6, les applications peuvent utiliser la fonction getaddrinfo() pour résoudre le nom de domaine complet (FQDN) « nom.prnp.net », où « nom » correspond au nom de pair en cours de résolution.</span><span class="sxs-lookup"><span data-stu-id="da4c3-107">To use PNRP to resolve a name to an IPv6 address, applications can use the getaddrinfo() function to resolve the Fully Qualified Domain Name (FQDN) name.prnp.net, in which name is peer name being resolved.</span></span> <span data-ttu-id="da4c3-108">Le domaine pnrp.net est un domaine réservé dans Windows Vista pour la résolution de noms PNRP.</span><span class="sxs-lookup"><span data-stu-id="da4c3-108">The pnrp.net domain is a reserved domain in Windows Vista for PNRP name resolution.</span></span>  
  
 <span data-ttu-id="da4c3-109">La transmission de messages entre applications PeerToPeer est toujours gérée par des architectures sous-jacentes telles que PeerChannel et WCF. [Données volumineuses et streaming](https://go.microsoft.com/fwlink/?LinkID=179652).</span><span class="sxs-lookup"><span data-stu-id="da4c3-109">Message passing between PeerToPeer applications is still handled by underlying architectures such as PeerChannel and WCF [Large Data and Streaming](https://go.microsoft.com/fwlink/?LinkID=179652).</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="da4c3-110">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="da4c3-110">See also</span></span>

- <xref:System.Net.PeerToPeer>
