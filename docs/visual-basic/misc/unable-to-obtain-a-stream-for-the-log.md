---
title: Impossible d’obtenir un flux pour le journal
ms.date: 07/20/2015
f1_keywords:
- vbrApplicationLog_ExhaustedPossibleStreamNames
ms.assetid: 33994f52-8efb-4790-a459-033e5c1db632
ms.openlocfilehash: 540ff3fbba72d33b2efaa58ad7a8019628f5e83f
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59344752"
---
# <a name="unable-to-obtain-a-stream-for-the-log"></a>Impossible d’obtenir un flux pour le journal
Impossible d’obtenir un flux pour le journal. Les noms de fichiers potentiels basés sur \<nom > sont déjà en cours d’utilisation.  
  
 Le <xref:Microsoft.VisualBasic.Logging.FileLogTraceListener> classe n’a pas pu créer un fichier de journal nouvelle, car tous les noms de fichier journal potentiels basent sur \<nom > sont déjà en cours d’utilisation.  
  
 Un nombre trop élevé de fichiers journaux peut indiquer un problème architectural avec l’application. Pour plus d’informations, consultez la documentation de la classe <xref:Microsoft.VisualBasic.Logging.FileLogTraceListener> .  
  
## <a name="to-correct-this-error"></a>Pour corriger cette erreur  
  
1. Affectez à la propriété <xref:Microsoft.VisualBasic.Logging.FileLogTraceListener.LogFileCreationSchedule%2A> la valeur <xref:Microsoft.VisualBasic.Logging.LogFileCreationScheduleOption.Daily> ou <xref:Microsoft.VisualBasic.Logging.LogFileCreationScheduleOption.Weekly> pour inclure un horodatage dans le nom du fichier journal.  
  
2. Archivez les journaux existants et supprimez-les de l’ordinateur pour permettre à l’objet <xref:Microsoft.VisualBasic.Logging.FileLogTraceListener> de créer des journaux.  
  
## <a name="see-also"></a>Voir aussi

- <xref:Microsoft.VisualBasic.Logging.FileLogTraceListener>
- <xref:Microsoft.VisualBasic.Logging.FileLogTraceListener.LogFileCreationSchedule%2A>
- [My.Application.Log](xref:Microsoft.VisualBasic.ApplicationServices.ApplicationBase.Log)
- [My.Application.Info.DirectoryPath](xref:Microsoft.VisualBasic.ApplicationServices.ApplicationBase.Log)
