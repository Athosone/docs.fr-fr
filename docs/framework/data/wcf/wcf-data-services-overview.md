---
title: Vue d'ensemble des services de données WCF
ms.date: 03/30/2017
helpviewer_keywords:
- WCF Data Services
- WCF Data Services, about
ms.assetid: 7924cf94-c9a6-4015-afc9-f5d22b1743bb
ms.openlocfilehash: ca52b725f5fad4b591b95bf6a6dd778c7a72d235
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59202039"
---
# <a name="wcf-data-services-overview"></a>Vue d'ensemble des services de données WCF
[!INCLUDE[ssAstoria](../../../../includes/ssastoria-md.md)] permet la création et la consommation de services de données pour le Web ou un intranet à l’aide de la [!INCLUDE[ssODataFull](../../../../includes/ssodatafull-md.md)]. [!INCLUDE[ssODataShort](../../../../includes/ssodatashort-md.md)] vous permet d’exposer vos données en tant que ressources adressables par URI. Cela vous permet d'accéder et de modifier des données en utilisant la sémantique REST (Representational State Transfer), en particulier les verbes HTTP standard GET, PUT, POST et DELETE. Cette rubrique fournit une vue d'ensemble des modèles et des pratiques définies par [!INCLUDE[ssODataShort](../../../../includes/ssodatashort-md.md)], ainsi que des outils fournis par [!INCLUDE[ssAstoria](../../../../includes/ssastoria-md.md)] pour tirer parti d'[!INCLUDE[ssODataShort](../../../../includes/ssodatashort-md.md)] dans les applications basées sur .NET Framework.  
  
## <a name="address-data-as-resources"></a>Adresser des données comme ressources  
 [!INCLUDE[ssODataShort](../../../../includes/ssodatashort-md.md)] expose des données comme des ressources adressables par des URI. Les chemins d'accès aux ressources sont construits selon les conventions de relation d'entité de l'Entity Data Model. Dans ce modèle, les entités représentent des unités opérationnelles de données dans un domaine d’application, telles que les clients, les commandes, les éléments et les produits. Pour plus d’informations, consultez [Entity Data Model](../../../../docs/framework/data/adonet/entity-data-model.md).  
  
 Dans [!INCLUDE[ssODataShort](../../../../includes/ssodatashort-md.md)], vous adressez des ressources d'entité comme un jeu d'entités qui contient des instances de types d'entité. Par exemple, l’URI `http://services.odata.org/Northwind/Northwind.svc/Customers('ALFKI')/Orders` retourne toutes les commandes à partir de la `Northwind` service de données qui sont associées au client avec un `CustomerID` valeur de `ALFKI.`  
  
 Les expressions de requête vous permettent d'effectuer des opérations de requête traditionnelles sur des ressources, telles que filtrer, trier et paginer. Par exemple, l'URI `http://services.odata.org/Northwind/Northwind.svc/Customers('ALFKI')/Orders?$filter=Freight gt 50` filtre les ressources de façon à retourner uniquement les commandes dont le coût de fret est supérieur à 50 $. Pour plus d’informations, consultez [accès aux ressources de Service de données](../../../../docs/framework/data/wcf/accessing-data-service-resources-wcf-data-services.md).  
  
## <a name="interoperable-data-access"></a>Accès aux données interopérables  
 [!INCLUDE[ssODataShort](../../../../includes/ssodatashort-md.md)] s’appuie sur des protocoles Internet standard pour rendre les services de données interactifs avec les applications qui n’utilisent pas le .NET Framework. Étant donné que vous pouvez utiliser l’URI standard pour les données d’adresse, votre application peut accéder et modifier des données en utilisant la sémantique representational state Transfer (REST), en particulier les verbes HTTP standard GET, PUT, POST et DELETE. De cette manière, vous pouvez accéder à ces services depuis tout client qui peut analyser et accéder aux données transmises sur des protocoles HTTP standard.  
  
 [!INCLUDE[ssODataShort](../../../../includes/ssodatashort-md.md)] définit un jeu d'extensions à Atom Publishing Protocol (AtomPub). Il prend en charge les requêtes et les réponses HTTP sous plusieurs formats de données pour prendre en charge des plateformes et des applications clientes diverses. Un flux [!INCLUDE[ssODataShort](../../../../includes/ssodatashort-md.md)] peut représenter des données dans Atom, JSON (JavaScript Object Notation), et sous forme de XML ordinaire. Bien qu'Atom soit le format par défaut, le format du flux est spécifié dans l'en-tête de la requête HTTP. Pour plus d’informations, consultez [OData : Format Atom](https://go.microsoft.com/fwlink/?LinkID=185794) et [OData : Format JSON](https://go.microsoft.com/fwlink/?LinkID=185795).  
  
 Lors de la publication des données comme un [!INCLUDE[ssODataShort](../../../../includes/ssodatashort-md.md)] flux, [!INCLUDE[ssAstoria](../../../../includes/ssastoria-md.md)] s’appuie sur d’autres fonctions Internet existantes pour des opérations telles que la mise en cache et l’authentification. Pour ce faire, [!INCLUDE[ssAstoria](../../../../includes/ssastoria-md.md)] s’intègre avec les applications d’hébergement existantes et de services, tels que ASP.NET, Windows Communication Foundation (WCF) et Internet Information Services (IIS).  
  
## <a name="storage-independence"></a>Indépendance du stockage  
 Même si les ressources sont adressées selon un modèle relation-entité, [!INCLUDE[ssAstoria](../../../../includes/ssastoria-md.md)] expose les flux [!INCLUDE[ssODataShort](../../../../includes/ssodatashort-md.md)] indépendamment de la source de données sous-jacente. Après l'acceptation par [!INCLUDE[ssAstoria](../../../../includes/ssastoria-md.md)] d'une requête HTTP pour une ressource identifiée par un URI, la requête est désérialisée et une représentation de cette requête est passée à un fournisseur [!INCLUDE[ssAstoria](../../../../includes/ssastoria-md.md)]. Ce fournisseur traduit la demande dans un format spécifique à la source de données et exécute la demande sur la source de données sous-jacente. [!INCLUDE[ssAstoria](../../../../includes/ssastoria-md.md)] effectue l'indépendance de stockage en séparant le modèle conceptuel qui adresse des ressources prescrites par [!INCLUDE[ssODataShort](../../../../includes/ssodatashort-md.md)] du schéma spécifique de la source de données sous-jacente.  
  
 [!INCLUDE[ssAstoria](../../../../includes/ssastoria-md.md)] s'intègre à ADO.NET Entity Framework pour vous permettre de créer des services de données qui exposent des données relationnelles. Vous pouvez utiliser les outils Entity Data Model pour créer un modèle de données qui contient des ressources adressables en tant qu'entités et définir en même temps le mappage entre ce modèle et les tables dans la base de données sous-jacente. Pour plus d’informations, consultez [fournisseur Entity Framework](../../../../docs/framework/data/wcf/entity-framework-provider-wcf-data-services.md).  
  
 [!INCLUDE[ssAstoria](../../../../includes/ssastoria-md.md)] vous permet également de créer des services de données qui exposent les structures de données qui retournent une implémentation de la <xref:System.Linq.IQueryable%601> interface. De cette manière, vous pouvez créer des services de données qui exposent des données à partir de types .NET Framework. Les opérations de création, de mise à jour et de suppression sont prises en charge lorsque vous implémentez également l'interface <xref:System.Data.Services.IUpdatable>. Pour plus d’informations, consultez [fournisseur de réflexion](../../../../docs/framework/data/wcf/reflection-provider-wcf-data-services.md).  
  
 Pour obtenir une illustration de la façon [!INCLUDE[ssAstoria](../../../../includes/ssastoria-md.md)] s’intègre avec ces fournisseurs de données, consultez le diagramme architectural plus loin dans cette rubrique.  
  
## <a name="custom-business-logic"></a>Logique métier personnalisée  
 [!INCLUDE[ssAstoria](../../../../includes/ssastoria-md.md)] rend plus facile ajouter une logique métier personnalisée à un service de données via des intercepteurs et des opérations de service. Les opérations de service sont des méthodes définies sur le serveur qui sont adressables par des URI sous la même forme que des ressources de données. Les opérations de service peuvent également utiliser la syntaxe d'expression de requête pour filtrer, classer et paginer des données retournées par une opération. Par exemple, l'URI `http://localhost:12345/Northwind.svc/GetOrdersByCity?city='London'&$orderby=OrderDate&$top=10&$skip=10` représente un appel à une opération de service nommée `GetOrdersByCity` sur le service de données Northwind qui retourne des commandes de clients de Londres et des résultats paginés triés par `OrderDate`. Pour plus d’informations, consultez [opérations de Service](../../../../docs/framework/data/wcf/service-operations-wcf-data-services.md).  
  
 Les intercepteurs permettent à la logique d'application personnalisée d'être intégrée dans le traitement des messages de réponse ou de demande par un service de données. Les intercepteurs sont appelés lorsqu'une action de requête, d'insertion, de mise à jour ou de suppression a lieu dans le jeu d'entités spécifié. Un intercepteur peut alors modifier les données, appliquer la stratégie d'autorisation ou même mettre fin à l'opération. Les méthodes d'intercepteur doivent être enregistrées explicitement pour un jeu d'entités donné exposé par un service de données. Pour plus d’informations, consultez [intercepteurs](../../../../docs/framework/data/wcf/interceptors-wcf-data-services.md).  
  
## <a name="client-libraries"></a>Bibliothèque clientes  
 [!INCLUDE[ssODataShort](../../../../includes/ssodatashort-md.md)] définit un ensemble de modèles uniformes pour l’interaction avec les services de données. Cela fournit une opportunité de créer des composants réutilisables qui reposent sur ces services, telles que les bibliothèques côté client qui le rendent plus faciles à utiliser les services de données.  
  
 [!INCLUDE[ssAstoria](../../../../includes/ssastoria-md.md)] inclut des bibliothèques clientes pour les applications clientes .NET Framework et Silverlight. Ces bibliothèques clientes vous permettent d'interagir avec les services de données en utilisant des objets .NET Framework. Elles prennent également en charge des requêtes basées sur des objets et des requêtes LINQ, le chargement des objets connexes, le suivi des modifications et la résolution d'identité. Pour plus d’informations, consultez [bibliothèque de Client WCF Data Services](../../../../docs/framework/data/wcf/wcf-data-services-client-library.md).  
  
 Outre le [!INCLUDE[ssODataShort](../../../../includes/ssodatashort-md.md)] bibliothèques clientes incluses avec le .NET Framework et Silverlight, il existe d’autres bibliothèques de client qui vous permettent de consommer un [!INCLUDE[ssODataShort](../../../../includes/ssodatashort-md.md)] flux dans les applications clientes, telles que les applications PHP, AJAX et Java. Pour plus d’informations, consultez le [OData SDK](https://go.microsoft.com/fwlink/?LinkID=185796).  
  
## <a name="architecture-overview"></a>Vue d'ensemble de l'architecture  
 Le diagramme suivant illustre la [!INCLUDE[ssAstoria](../../../../includes/ssastoria-md.md)] architecture pour l’exposition [!INCLUDE[ssODataShort](../../../../includes/ssodatashort-md.md)] flux et l’utilisation de ces flux dans [!INCLUDE[ssODataShort](../../../../includes/ssodatashort-md.md)]-bibliothèques clientes :  
  
 ![Capture d’écran montrant un diagramme d’architecture WCF Data Services.](./media/wcf-data-services-overview/windows-communication-foundation-data-services-architecture.gif)  
  
## <a name="see-also"></a>Voir aussi

- [WCF Data Services 4.5](../../../../docs/framework/data/wcf/index.md)
- [Prise en main](../../../../docs/framework/data/wcf/getting-started-with-wcf-data-services.md)
- [Définition de WCF Data Services](../../../../docs/framework/data/wcf/defining-wcf-data-services.md)
- [Accès aux ressources de Service de données (WCF Data Services)](https://docs.microsoft.com/previous-versions/dotnet/netframework-4.0/dd728283(v=vs.100))
- [Bibliothèque cliente WCF Data Services](../../../../docs/framework/data/wcf/wcf-data-services-client-library.md)
- [Representational State Transfer (REST)](https://go.microsoft.com/fwlink/?LinkId=113919)
