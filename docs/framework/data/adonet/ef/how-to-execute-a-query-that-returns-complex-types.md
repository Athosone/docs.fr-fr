---
title: 'Procédure : Exécuter une requête qui retourne des types complexes'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
ms.assetid: c2209fdb-70ef-4dea-8bb8-097fe96f5563
ms.openlocfilehash: a428f54c3834ccdf6a0c7a5bfce8307172724524
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61607204"
---
# <a name="how-to-execute-a-query-that-returns-complex-types"></a>Procédure : Exécuter une requête qui retourne des types complexes
Cette rubrique indique comment exécuter une requête [!INCLUDE[esql](../../../../../includes/esql-md.md)] qui retourne des objets de type d'entité qui contiennent une propriété d'un type complexe.  
  
### <a name="to-run-the-code-in-this-example"></a>Pour exécuter le code de cet exemple  
  
1. Ajouter le [AdventureWorks Sales Model](https://github.com/Microsoft/sql-server-samples/releases/tag/adventureworks) à votre projet et configurez votre projet pour utiliser le [!INCLUDE[adonet_ef](../../../../../includes/adonet-ef-md.md)]. Pour plus d'informations, voir [Procédure : Utilisez l’Assistant Entity Data Model](https://docs.microsoft.com/previous-versions/dotnet/netframework-4.0/bb738677(v=vs.100)).  
  
2. Dans la page de codes de votre application, ajoutez les instructions `using` (`Imports` en Visual Basic) suivantes :  
  
     [!code-csharp[DP EntityServices Concepts#Namespaces](../../../../../samples/snippets/csharp/VS_Snippets_Data/dp entityservices concepts/cs/source.cs#namespaces)]
     [!code-vb[DP EntityServices Concepts#Namespaces](../../../../../samples/snippets/visualbasic/VS_Snippets_Data/dp entityservices concepts/vb/source.vb#namespaces)]  
  
3. Double-cliquez sur le fichier .edmx pour afficher le modèle dans le [fenêtre Explorateur de modèles](https://docs.microsoft.com/previous-versions/dotnet/netframework-4.0/bb738483(v=vs.100)) du Concepteur d’entités. Sur la surface du Concepteur d’entités, sélectionnez le `Email` et `Phone` propriétés de la `Contact` type d’entité, puis avec le bouton droit et sélectionnez **refactoriser en nouveau Type complexe**.  
  
4. Un nouveau type complexe avec le texte sélectionné `Email` et `Phone` propriétés est ajouté à la **Explorateur de modèles**. Le type complex est donné un nom par défaut : Renommez le type en `EmailPhone` dans le **propriétés** fenêtre. Une nouvelle propriété `ComplexProperty` est également ajoutée au type d'entité `Contact`. Renommez la propriété en `EmailPhoneComplexType.`.  
  
     Pour plus d’informations sur la création et modification des types complexes à l’aide de l’Assistant Entity Data Model, consultez [Comment : Refactoriser des propriétés existantes en propriété de Type complexe](https://docs.microsoft.com/previous-versions/dotnet/netframework-4.0/dd456814(v=vs.100)) et [Comment : Créer et modifier des Types complexes](https://docs.microsoft.com/previous-versions/dotnet/netframework-4.0/dd456820(v=vs.100)).  
  
## <a name="example"></a>Exemple  
 L’exemple suivant exécute une requête qui retourne une collection de `Contact` les objets et les affiche deux propriétés de la `Contact` objets : `ContactID` et les valeurs de la `EmailPhoneComplexType` type complexe.  
  
 [!code-csharp[DP EntityServices Concepts#ComplexTypeWithEntityCommand](../../../../../samples/snippets/csharp/VS_Snippets_Data/dp entityservices concepts/cs/source.cs#complextypewithentitycommand)]
 [!code-vb[DP EntityServices Concepts#ComplexTypeWithEntityCommand](../../../../../samples/snippets/visualbasic/VS_Snippets_Data/dp entityservices concepts/vb/source.vb#complextypewithentitycommand)]
