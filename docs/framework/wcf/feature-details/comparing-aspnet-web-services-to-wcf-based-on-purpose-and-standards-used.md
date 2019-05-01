---
title: Comparaison des services Web ASP.NET et de WCF en fonction de l'objectif et des normes utilisées
ms.date: 03/30/2017
ms.assetid: d3890278-fa9b-4902-91ea-8da73b7143cc
ms.openlocfilehash: f57e895680b5cc043dad365b9f25f32477f42e72
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62048060"
---
# <a name="comparing-aspnet-web-services-to-wcf-based-on-purpose-and-standards-used"></a>Comparaison des services Web ASP.NET et de WCF en fonction de l'objectif et des normes utilisées
Les services Web ASP.NET ont été développés pour générer des applications qui envoient et reçoivent des messages à l'aide du protocole SOAP (Simple Object Access Protocol) sur HTTP. La structure des messages peut être définie à l'aide d'un schéma XML et un outil est fourni pour faciliter la sérialisation des messages vers et à partir d'objets .NET Framework. La technologie peut générer automatiquement des métadonnées afin de décrire des services Web dans le langage WSDL (Web Services Description Language) et un deuxième outil est fourni pour générer des clients pour les services Web à partir du WSDL.  
  
 WCF est d’activation des applications .NET Framework échanger des messages avec d’autres entités logicielles. SOAP est utilisé par défaut, mais les messages peuvent se présenter sous tout format et sont acheminés en utilisant tout protocole de transport. La structure des messages peut être définie à l'aide d'un schéma XML et il existe plusieurs options de sérialisation des messages vers et à partir d'objets .NET Framework. WCF peut générer automatiquement des métadonnées pour décrire les applications générées à l’aide de la technologie dans WSDL, et il fournit également un outil pour générer des clients pour ces applications à partir de WSDL.  
  
 Les normes prises en charge par les services Web ASP.NET sont documentées dans [les Services Web XML créés à l’aide d’ASP.NET](https://go.microsoft.com/fwlink/?LinkId=94872). La liste plus complète des normes prises en charge par WCF sont répertoriés au [Web Services protocoles pris en charge par les liaisons d’interopérabilité fournies](../../../../docs/framework/wcf/feature-details/web-services-protocols-supported-by-system-provided-interoperability-bindings.md).  
  
## <a name="see-also"></a>Voir aussi

- [Comparaison des services web ASP.NET et de WCF du point de vue du développement](../../../../docs/framework/wcf/feature-details/comparing-aspnet-web-services-to-wcf-based-on-development.md)
