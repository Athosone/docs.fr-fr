---
title: Le nom de source spécifié dans le journal est inscrit auprès d’un journal autre que celui spécifié dans EventLogName
ms.date: 07/20/2015
ms.assetid: 7317e100-098b-408d-86e5-7c74cf8558c7
ms.openlocfilehash: 22129ab0c4f7fe0a78300907a949d9368028c9fa
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61594995"
---
# <a name="source-name-specified-in-eventlogsource-is-registered-to-a-log-other-than-that-specified-in-eventlogname"></a>Le nom de source spécifié dans le journal est inscrit auprès d’un journal autre que celui spécifié dans EventLogName
Le `EventLog` essaie de faire référence à une source qui est inscrite auprès d’un autre journal. Si vous écrivez des entrées dans le journal des événements, vous devez spécifier la propriété <xref:System.Diagnostics.EventLog.Source%2A> . La propriété <xref:System.Diagnostics.EventLog.Source%2A> inscrit votre composant auprès du journal des événements comme source d’entrées valide. Une même source ne peut être associée (et donc écrire des entrées) qu’à un seul journal des événements à la fois.  
  
 Par défaut, si vous tentez d’écrire une entrée sans avoir d’abord inscrit votre composant en tant que source valide, le système inscrit automatiquement la source auprès du journal des événements, en utilisant la valeur de la propriété <xref:System.Diagnostics.EventLog.Source%2A> comme chaîne source.  
  
## <a name="to-correct-this-error"></a>Pour corriger cette erreur  
  
- Vérifiez que la source est inscrite auprès du journal approprié. Pour ce faire, utilisez la méthode <xref:System.Diagnostics.EventLog.CreateEventSource%2A> ou l’une de ses surcharges pour spécifier une chaîne qui identifie votre composant auprès du journal des événements.  
  
## <a name="see-also"></a>Voir aussi

- [Administration des journaux des événements](https://docs.microsoft.com/previous-versions/visualstudio/visual-studio-2008/4f69axw4(v=vs.90))
- [Références du journal des événements](https://docs.microsoft.com/previous-versions/visualstudio/visual-studio-2008/k43k9z2a(v=vs.90))
- [Guide pratique pour Ajouter votre Application en tant que Source d’entrées de journal des événements](https://docs.microsoft.com/previous-versions/visualstudio/visual-studio-2008/xz73e171(v=vs.90))
- [Guide pratique pour Supprimer une Source d’événement](https://docs.microsoft.com/previous-versions/visualstudio/visual-studio-2008/k57466fc(v=vs.90))
