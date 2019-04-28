---
title: Applications Windows Forms et non managées
ms.date: 03/30/2017
helpviewer_keywords:
- ActiveX controls [Windows Forms]
- COM interop [Windows Forms], Windows Forms
- COM [Windows Forms]
- Windows Forms, unmanaged
- Windows Forms, interop
ms.assetid: 81bc100c-fa49-4614-85a6-0f7ab59eac8a
ms.openlocfilehash: 65465f22b1806d385523c894cce2103afe33c2f0
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61746698"
---
# <a name="windows-forms-and-unmanaged-applications"></a>Applications Windows Forms et non managées
Les contrôles et les applications Windows Forms peuvent interagir avec des applications non managées, avec certaines restrictions. Les sections suivantes décrivent les scénarios et les configurations pris en charge et non pris en charge par les applications et les contrôles Windows Forms.  
  
## <a name="in-this-section"></a>Dans cette section  
 [Vue d'ensemble des applications Windows Forms et non managées](windows-forms-and-unmanaged-applications-overview.md)  
 Propose des informations générales sur l'utilisation et l'implémentation des contrôles Windows Forms qui fonctionnent avec les applications non managées.  
  
 [Guide pratique pour Prennent en charge COM Interop en affichant un formulaire Windows avec la méthode ShowDialog](com-interop-by-displaying-a-windows-form-shadow.md)  
 Fournit un exemple de code qui montre comment utiliser la méthode <xref:System.Windows.Forms.Form.ShowDialog%2A?displayProperty=nameWithType> pour exécuter un Windows Form dans une application non managée.  
  
 [Guide pratique pour Prennent en charge COM Interop en affichant chaque formulaire Windows sur son propre Thread](how-to-support-com-interop-by-displaying-each-windows-form-on-its-own-thread.md)  
 Fournit un exemple de code qui montre comment exécuter un Windows Form sur son propre thread.  
  
 Consultez également [procédure pas à pas : Prise en charge COM Interop en affichant chaque formulaire Windows sur son propre Thread](https://docs.microsoft.com/previous-versions/visualstudio/visual-studio-2010/ms233639(v=vs.100)).  
  
## <a name="reference"></a>Référence  
 <xref:System.Windows.Forms.Form.ShowDialog%2A?displayProperty=nameWithType>  
 Permet de créer un thread distinct pour un Windows Form.  
  
 <xref:System.Windows.Forms.Application.Run%2A?displayProperty=nameWithType>  
 Démarre une boucle de message pour un thread.  
  
 <xref:System.Windows.Forms.Control.Invoke%2A>  
 Marshale les appels à partir d’une application non managée vers un formulaire.  
  
## <a name="related-sections"></a>Rubriques connexes  
 [Exposition de composants .NET Framework à COM](../../interop/exposing-dotnet-components-to-com.md)  
 Propose des informations générales sur l'utilisation de types .NET Framework dans les applications non managées.
