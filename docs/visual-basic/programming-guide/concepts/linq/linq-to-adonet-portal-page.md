---
title: LINQ to ADO.NET (page de portail)
ms.date: 07/20/2015
ms.assetid: bbbd7c76-2981-4b91-b8d2-437547181f52
ms.openlocfilehash: 63e9c1795f8a4ee50977af6ec32b945a6e5c79be
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61663664"
---
# <a name="linq-to-adonet-portal-page"></a>LINQ to ADO.NET (page de portail)
[!INCLUDE[linq_adonet](~/includes/linq-adonet-md.md)] vous permet d’interroger tout objet énumérable dans [!INCLUDE[vstecado](~/includes/vstecado-md.md)] à l’aide du modèle de programmation [!INCLUDE[vbteclinqext](~/includes/vbteclinqext-md.md)].  
  
> [!NOTE]
>  La documentation [!INCLUDE[linq_adonet](~/includes/linq-adonet-md.md)] se trouve dans la section ADO.NET du SDK .NET Framework : [LINQ et ADO.NET](../../../../framework/data/adonet/linq-and-ado-net.md).
  
 Il existe trois technologies ADO.NET [!INCLUDE[vbteclinqext](~/includes/vbteclinqext-md.md)] différentes : [!INCLUDE[linq_dataset](~/includes/linq-dataset-md.md)], [!INCLUDE[vbtecdlinq](~/includes/vbtecdlinq-md.md)] et [!INCLUDE[linq_entities](~/includes/linq-entities-md.md)]. [!INCLUDE[linq_dataset](~/includes/linq-dataset-md.md)] assure une interrogation plus riche et optimisée du <xref:System.Data.DataSet>, [!INCLUDE[vbtecdlinq](~/includes/vbtecdlinq-md.md)] vous permet d’interroger directement des schémas de base de données SQL Server et [!INCLUDE[linq_entities](~/includes/linq-entities-md.md)] d’interroger un [!INCLUDE[adonet_edm](~/includes/adonet-edm-md.md)].  
  
## <a name="linq-to-dataset"></a>LINQ to DataSet  
 Le <xref:System.Data.DataSet> est un des composants les plus largement utilisés dans [!INCLUDE[vstecado](~/includes/vstecado-md.md)] et c’est un élément clé du modèle de programmation déconnecté sur lequel [!INCLUDE[vstecado](~/includes/vstecado-md.md)] est fondé. Toutefois, en dépit de son importance, le <xref:System.Data.DataSet> a des capacités de requête limitées.  
  
 [!INCLUDE[linq_dataset](~/includes/linq-dataset-md.md)] vous permet de générer des fonctions de requête plus complètes dans <xref:System.Data.DataSet> à l'aide des mêmes fonctionnalités de requête qui sont disponibles pour de nombreuses autres sources de données.  
  
 Pour plus d’informations, [consultez LINQ to DataSet](../../../../framework/data/adonet/linq-to-dataset.md).  
  
## <a name="linq-to-sql"></a>LINQ to SQL  
 [!INCLUDE[vbtecdlinq](~/includes/vbtecdlinq-md.md)] fournit une infrastructure runtime pour la gestion des données relationnelles comme objets. Dans [!INCLUDE[vbtecdlinq](~/includes/vbtecdlinq-md.md)], le modèle de données d’une base de données relationnelle est mappé à un modèle objet exprimé dans le langage de programmation du développeur. Lors de l’exécution de l’application, [!INCLUDE[vbtecdlinq](~/includes/vbtecdlinq-md.md)] traduit les requêtes intégrées au langage du modèle objet en SQL et les envoie à la base de données pour exécution. Quand la base de données retourne les résultats, [!INCLUDE[vbtecdlinq](~/includes/vbtecdlinq-md.md)] les retraduit en objets que vous pouvez utiliser.  
  
 [!INCLUDE[vbtecdlinq](~/includes/vbtecdlinq-md.md)] inclut la prise en charge des procédures stockées et fonctions définies par l’utilisateur dans la base de données, et de l’héritage dans le modèle objet.  
  
 Pour plus d’informations, consultez [LINQ to SQL](../../../../framework/data/adonet/sql/linq/index.md).  
  
## <a name="linq-to-entities"></a>LINQ to Entities  
 Via le [!INCLUDE[adonet_edm](~/includes/adonet-edm-md.md)], les données relationnelles sont exposées comme objets dans l'environnement .NET. Cela fait de la couche objet une cible idéale pour la prise en charge [!INCLUDE[vbteclinq](~/includes/vbteclinq-md.md)], permettant aux développeurs de formuler des requêtes sur la base de données à partir du langage utilisé pour générer la logique métier. Cette capacité porte le nom de [!INCLUDE[linq_entities](~/includes/linq-entities-md.md)]. Pour plus d’informations, consultez [LINQ to Entities](../../../../framework/data/adonet/ef/language-reference/linq-to-entities.md).  
  
## <a name="see-also"></a>Voir aussi

- [LINQ et ADO.NET](../../../../framework/data/adonet/linq-and-ado-net.md)
- [Language-Integrated Query (LINQ) (Visual Basic)](../../../../visual-basic/programming-guide/concepts/linq/index.md)
