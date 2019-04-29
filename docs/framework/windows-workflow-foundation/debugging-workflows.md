---
title: Débogage de workflows
ms.date: 03/30/2017
ms.assetid: b23b4814-ebb1-4c51-b7a9-469f4da7a96d
ms.openlocfilehash: 17cee1f1b509e777edd3f08c55d473d768b19b55
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61945871"
---
# <a name="debugging-workflows"></a>Débogage de workflows
[!INCLUDE[netfx_current_long](../../../includes/netfx-current-long-md.md)] offre plusieurs options permettant de déboguer des workflows en cours d'exécution à partir de l'environnement de développement. Les workflows peuvent être débogués dans le concepteur, dans XAML et dans le code.  
  
## <a name="debugging-in-the-workflow-designer"></a>Débogage dans le concepteur de workflow  
 Points d’arrêt peuvent être définies sur des activités dans le Concepteur de workflow soit mise en surbrillance de l’activité et en appuyant sur **F9** ou à l’aide du menu contextuel de l’activité. Ainsi, l'exécution du workflow s'arrête lorsque l'hôte de workflow est exécuté en mode débogage. Dans la capture d'écran suivante, l'exécution du workflow est suspendue à un point d'arrêt. Pour plus d’informations, consultez [débogage de flux de travail avec le Concepteur de Workflow](/visualstudio/workflow-designer/debugging-workflows-with-the-workflow-designer).  
  
## <a name="debugging-in-xaml"></a>Débogage dans XAML  
 Si un workflow a suspendu son exécution à un point d'arrêt dans le concepteur, le workflow peut également être débogué dans XAML. Pour afficher le point d’exécution dans XAML, sélectionnez **XAML vue** dans le Concepteur de flux de travail lors de l’exécution du workflow est suspendue. Il est possible de revenir au mode de débogage dans le concepteur de workflow en rouvrant le workflow dans le concepteur à partir de l'Explorateur de solutions. Pour plus d'informations, voir [Procédure : Déboguer XAML avec Workflow Designer](/visualstudio/workflow-designer/how-to-debug-xaml-with-the-workflow-designer).  
  
## <a name="debugging-in-code"></a>Débogage dans le code  
 Des points d'arrêt de code peuvent être utilisés dans [!INCLUDE[netfx_current_short](../../../includes/netfx-current-short-md.md)] de la même façon que dans d'autres applications impératives. Cliquez sur la marge de gauche du volet de code pour créer un point d’arrêt du code, ou appuyez sur **F9** pour placer un point d’arrêt à l’emplacement du curseur.  
  
## <a name="attaching-to-a-workflow-process"></a>Attachement à un processus de workflow  
 Le débogage de workflow permet également d'utiliser l'infrastructure de Visual Studio pour attacher un processus. Cela permet à l'auteur de workflow de déboguer un workflow qui est exécuté dans un environnement hôte différent, tel qu'Internet Information Services 7.0 (IIS).  
  
## <a name="remote-debugging"></a>Remote Debugging  
 Débogage à distance de Windows Workflow Foundation (WF) fonctionne comme un débogage à distance pour les autres composants de Visual Studio. Pour plus d’informations sur l’utilisation du débogage à distance, consultez [Comment : Activer le débogage distant](https://go.microsoft.com/fwlink/?LinkId=196257).  
  
> [!NOTE]
>  Si l’application de flux de travail cible le x86 architecture et est hébergée sur un ordinateur exécutant un système d’exploitation 64 bits, le débogage à distance ne fonctionnera que si Visual Studio est installé sur l’ordinateur distant ou la cible pour l’application de flux de travail est remplacée par **N’importe quelle UC**.  
  
## <a name="extending-the-workflow-debugging-service"></a>Extension du service de débogage de workflow  
 Le service de débogage de workflow est maintenant public et peut être utilisé pour créer des applications personnalisées, notamment pour la surveillance, la simulation et le débogage dans un concepteur réhébergé. Pour plus d'informations, voir la rubrique <xref:System.Activities.Presentation.Debug.DebuggerService>.
