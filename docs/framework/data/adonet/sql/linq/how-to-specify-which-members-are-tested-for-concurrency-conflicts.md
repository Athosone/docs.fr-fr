---
title: 'Procédure : Spécifier les membres dont les conflits d’accès concurrentiel doivent être vérifiés'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
ms.assetid: d2cda293-1e2f-4878-af0e-5aaf0d092120
ms.openlocfilehash: 9a1b4ab2dc28c569473eddbf50b96d10298d8d3c
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59310432"
---
# <a name="how-to-specify-which-members-are-tested-for-concurrency-conflicts"></a>Procédure : Spécifier les membres dont les conflits d’accès concurrentiel doivent être vérifiés
Appliquer l’une des trois enums à la [!INCLUDE[vbtecdlinq](../../../../../../includes/vbtecdlinq-md.md)] <xref:System.Data.Linq.Mapping.ColumnAttribute.UpdateCheck%2A> propriété sur un <xref:System.Data.Linq.Mapping.ColumnAttribute> attribut pour spécifier quels membres doivent être incluses dans la mise à jour vérifie pour la détection de conflits d’accès concurrentiel optimiste.  
  
 La propriété <xref:System.Data.Linq.Mapping.ColumnAttribute.UpdateCheck%2A> (mappée au moment du design) est utilisée avec des fonctionnalités d’accès concurrentiel à l’exécution dans [!INCLUDE[vbtecdlinq](../../../../../../includes/vbtecdlinq-md.md)]. Pour plus d’informations, consultez [d’accès concurrentiel optimiste : Vue d’ensemble](../../../../../../docs/framework/data/adonet/sql/linq/optimistic-concurrency-overview.md).  
  
> [!NOTE]
>  Les valeurs membres d'origine sont comparées avec l'état actuel de la base de données tant qu'aucun membre n'est désigné comme `IsVersion=true`. Pour plus d'informations, consultez <xref:System.Data.Linq.Mapping.ColumnAttribute.IsVersion%2A>.  
  
 Pour obtenir des exemples de code, consultez <xref:System.Data.Linq.Mapping.ColumnAttribute.UpdateCheck%2A>.  
  
### <a name="to-always-use-this-member-for-detecting-conflicts"></a>Pour utiliser systématiquement ce membre pour détecter les conflits  
  
1. Ajoutez la propriété <xref:System.Data.Linq.Mapping.ColumnAttribute.UpdateCheck%2A> à l'attribut <xref:System.Data.Linq.Mapping.ColumnAttribute>.  
  
2. Affectez la valeur <xref:System.Data.Linq.Mapping.ColumnAttribute.UpdateCheck%2A> à la propriété `Always`.  
  
### <a name="to-never-use-this-member-for-detecting-conflicts"></a>Pour ne jamais utiliser ce membre pour détecter des conflits  
  
1. Ajoutez la propriété <xref:System.Data.Linq.Mapping.ColumnAttribute.UpdateCheck%2A> à l'attribut <xref:System.Data.Linq.Mapping.ColumnAttribute>.  
  
2. Affectez la valeur <xref:System.Data.Linq.Mapping.ColumnAttribute.UpdateCheck%2A> à la propriété `Never`.  
  
### <a name="to-use-this-member-for-detecting-conflicts-only-when-the-application-has-changed-the-value-of-the-member"></a>Pour utiliser ce membre pour détecter des conflits uniquement lorsque l'application a modifié la valeur du membre  
  
1. Ajoutez la propriété <xref:System.Data.Linq.Mapping.ColumnAttribute.UpdateCheck%2A> à l'attribut <xref:System.Data.Linq.Mapping.ColumnAttribute>.  
  
2. Affectez la valeur <xref:System.Data.Linq.Mapping.ColumnAttribute.UpdateCheck%2A> à la propriété `WhenChanged`.  
  
## <a name="example"></a>Exemple  
 L'exemple suivant spécifie que les objets `HomePage` ne doivent jamais être testés pendant des contrôles de mise à jour. Pour plus d'informations, consultez <xref:System.Data.Linq.Mapping.ColumnAttribute.UpdateCheck%2A>.  
  
 [!code-csharp[System.Data.Linq.Mapping.UpdateCheck#1](../../../../../../samples/snippets/csharp/VS_Snippets_Data/system.data.linq.mapping.updatecheck/cs/northwind.cs#1)]
 [!code-vb[System.Data.Linq.Mapping.UpdateCheck#1](../../../../../../samples/snippets/visualbasic/VS_Snippets_Data/system.data.linq.mapping.updatecheck/vb/northwind.vb#1)]  
  
## <a name="see-also"></a>Voir aussi

- [Guide pratique pour Gérer les conflits de changement](../../../../../../docs/framework/data/adonet/sql/linq/how-to-manage-change-conflicts.md)
- [Apport et soumission de modifications de données](../../../../../../docs/framework/data/adonet/sql/linq/making-and-submitting-data-changes.md)
