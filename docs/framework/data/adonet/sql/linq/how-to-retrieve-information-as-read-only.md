---
title: 'Procédure : Récupérer des informations en lecture seule'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
ms.assetid: fb09e298-0b53-47e5-97fb-ab318bcd4fad
ms.openlocfilehash: 131562e9ee0fbfde8c94f580bcb6d452918f42ee
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62037581"
---
# <a name="how-to-retrieve-information-as-read-only"></a>Procédure : Récupérer des informations en lecture seule
Lorsque vous ne projetez pas de modifier les données, vous pouvez augmenter les performances des requêtes en recherchant des résultats en lecture seule.  
  
 Implémentez le traitement en lecture seule en affectant la valeur <xref:System.Data.Linq.DataContext.ObjectTrackingEnabled%2A> à `false`.  
  
> [!NOTE]
>  Lorsque la valeur <xref:System.Data.Linq.DataContext.ObjectTrackingEnabled%2A> est affectée à `false`, <xref:System.Data.Linq.DataContext.DeferredLoadingEnabled%2A> a implicitement la valeur `false`.  
  
## <a name="example"></a>Exemple  
 Le code suivant récupère une collection en lecture seule de dates d’embauche d’employés.  
  
 [!code-csharp[DLinqQuerying#2](../../../../../../samples/snippets/csharp/VS_Snippets_Data/DLinqQuerying/cs/Program.cs#2)]
 [!code-vb[DLinqQuerying#2](../../../../../../samples/snippets/visualbasic/VS_Snippets_Data/DLinqQuerying/vb/Module1.vb#2)]  
  
## <a name="see-also"></a>Voir aussi

- [Concepts relatifs aux requêtes](../../../../../../docs/framework/data/adonet/sql/linq/query-concepts.md)
- [Interrogation de la base de données](../../../../../../docs/framework/data/adonet/sql/linq/querying-the-database.md)
- [Comparaison entre le chargement différé et le chargement immédiat](../../../../../../docs/framework/data/adonet/sql/linq/deferred-versus-immediate-loading.md)
