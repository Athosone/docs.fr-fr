---
title: Déploiement d'applications WCF à l'aide de ClickOnce
ms.date: 03/30/2017
ms.assetid: 1a11feee-2a47-4d3e-a28a-ad69d5ff93e0
ms.openlocfilehash: 1820b00aa903633750f74f319f9cf8038ba2b043
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61785089"
---
# <a name="deploying-wcf-applications-with-clickonce"></a>Déploiement d'applications WCF à l'aide de ClickOnce
Les applications clientes à l’aide de Windows Communication Foundation (WCF) peuvent être déployées à l’aide de la technologie ClickOnce. Cette technologie leur permet de tirer parti des protections de sécurité d'exécution fournies par la sécurité d'accès du code, sous réserve qu'elles soient signées numériquement avec un certificat approuvé. Le certificat utilisé pour signer l'application ClickOnce doit résider dans le magasin d'éditeurs approuvés, et la stratégie de sécurité locale sur l'ordinateur client doit être configurée pour accorder des autorisations Confiance totale aux applications signées avec le certificat de l'éditeur.  
  
 Pour plus d’informations sur la configuration des applications ClickOnce et éditeurs approuvés, consultez [configuration d’éditeurs approuvés ClickOnce](https://go.microsoft.com/fwlink/?LinkId=94774).  
  
## <a name="see-also"></a>Voir aussi

- [Vue d’ensemble du déploiement d’applications approuvées](https://go.microsoft.com/fwlink/?LinkId=94775)
- [Applications de déploiement ClickOnce pour les Windows Forms](https://go.microsoft.com/fwlink/?LinkId=94776)
